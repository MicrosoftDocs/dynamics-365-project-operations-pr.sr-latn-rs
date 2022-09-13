---
title: Podrazumevani cenovnici
description: Ovaj članak pruža informacije o podrazumevanim cenovničima prodaje i troškova u operacijama projekta.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50dbf74e31b9eb8d63c378e5fd718dc17c9691f4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410280"
---
# <a name="default-price-lists"></a>Podrazumevani cenovnici

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

## <a name="sales-price-lists"></a>Prodajni cenovnici

Svaka projektna ponuda i ugovor u usluzi Dynamics 365 Project Operations sadrži podrazumevani prodajni cenovnik. 

### <a name="price-list-default-on-project-quotes"></a>Podrazumevana vrednost cenovnika prema ponudama za projekat
Sistem dovršava sledeći postupak da bi utvrdio koji će se cenovnik podrazumevati za ponudu za projekat:

1. Sistem pregleda cenovnike koji su priloženi cenovnicima projektata poslovnih kontakata. 
1. Ako nema priloženih cenovnika projekta uz zapis konta, sistem gleda prodajne cenovnike priložene parametrima projekta koji se podudaraju sa valutom ponude za projekat.
1. Dalje, sistem proverava datum stupanja na snagu cenovnika koji se podudaraju sa opsegom datuma ponude za projekat. Konkretno, datum pravljenja ponude.
1. Ako postoji više cenovnika koji su na snazi na datum projektne ponude, svi cenovnici se podrazumevaju na projektnoj ponudi.
1. Ako nijedan cenovnik nije na snazi za datum projektne ponude, ne postoji podrazumevani projektni cenovnik projektne ponude. Na ponudi projekta pojaviće se poruka upozorenja. U poruci se navodi da pošto ne postoje priloženi cenovnici projekata, neće biti određena cena za procenjeni i stvarni rad i troškove na projektu.

### <a name="price-list-default-on-project-contracts"></a>Podrazumevana vrednost cenovnika prema ugovorima za projekat 
Sistem dovršava sledeći postupak da bi utvrdio koji će se cenovnik podrazumevati za ugovor za projekat:

1. Ako se ugovor kreira iz ponude, cenovnici projekata na ponudi se kopiraju odvojeno i prilažu uz ugovor o projektu.
1. Ako se ugovor kreira od početka, sistem pregleda cenovnike koji su priloženi projektnim cenovnicima poslovnog kontakta. Ako su uz evidenciju poslovnih kontakata nisu priloženi cenovnici projekata, sistem traži prodajne cenovnike koji su priloženi uz parametre projekta koji odgovaraju valuti ugovora za projekat.
1. Dalje, sistem proverava datum stupanja na snagu cenovnika koji se podudaraju sa opsegom datuma ugovora za projekat. Konkretno, datum pravljenja ugovora.
1. Ako postoji više cenovnika koji su na snazi na datum ugovora, svi cenovnici se podrazumevaju na ugovoru.
1. Ako nijedan cenovnik nije na snazi za datum ugovora, ne postoji podrazumevani projektni cenovnik na ugovoru. Na ugovoru projekta pojaviće se poruka upozorenja. U poruci se navodi da pošto ne postoje priloženi cenovnici projekata, neće biti određena cena za procenjeni i stvarni rad i troškove na projektu.

## <a name="cost-price-lists"></a>Cenovnici troškova

Cenovnici troškova ne podrazumevaju nijedan entitet u usluzi Project Operations. Određivanje cenovnik troška koji će se koristiti za troškove projekta uvek se obavlja po transakciji. Sistem dovršava sledeći postupak da bi utvrdio koji će se cenovnik koristiti za cene projekta:

1. Sistem gleda cenovnike koji su priloženi jedinici ugovaranja projekta.
1. Zatim sistem posmatra efekat datuma cenovnika koji se podudaraju sa datumom dolaznog konteksta procene ili stvarnog konteksta.

    - *Kontekst procene* se odnosi na bilo koji od tri konteksta procene u projektnom radu:

        - Linija procene za projekat
        - Detalj stavke ponude
        - Detalj predmeta ugovora

    - *Stvarni kontekst* se odnosi na bilo koji od tri izvora za stvarne u operacijama projekta:

       - Redovi naloga stavki koji su ručno kreirani ili korektivni redovi naloga koji su kreirani u korektivnom nalogu
       - Redovi naloga koji se kreiraju tokom prosleđivanja evidencija vremena, troškova ili korišćenja materijala
       - Detalj stavke fakture

    Kada se operacije projekta podudaraju sa efektivnošću datuma dolaznog reda naloga ili detalja reda fakture *u stvarnom* kontekstu, on koristi polje "Datum **transakcije** ".

    - Ako je više cenovnika efikasno za datum konteksta dolazne procene ili stvarnog konteksta, bira se poslednji kreirani cenovnik.
    - Ako nijedan cenovnik nije priložen jedinici ugovaranja projekta, sistem gleda cenovnike troškova koji su priloženi parametrima projekta koji odgovaraju valuti projekta.

## <a name="enable-multi-currency-cost-price-list"></a>Omogući cenovnik troškova u više valuta

Ovu postavku možete pronaći u **podešavanjima** \> **Parametara.** Podrazumevana vrednost je **Ne**.

Kada je ova postavka omogućena (to jest, vrednost je postavljena na **"Da**"), sistem se ponaša na sledeći način:

- Omogućava da cenovnici troškova u bilo kojoj valuti budu povezani sa organizacionom jedinicom. Na primer, cenovnik troška u valuti EUR može biti priložen organizacionoj jedinici u USD valuti. Sistem će nastaviti da proverava da li cenovnici troškova koji su priloženi organizacionoj jedinici nemaju efekat preklapanja datuma.
- Potvrđuje da cenovnici troškova koji su priloženi parametrima projekta nemaju efekat preklapanja datuma, čak i ako imaju različite valute. Ovo ponašanje se razlikuje od podrazumevanog ponašanja (to jest ponašanja kada je vrednost postavljena na vrednost "Ne **"**). U podrazumevanom ponašanju, samo cenovnici troškova koji imaju istu **valutu** proveravaju se za efekat datuma koji se ne preklapa.
- Za kontekst dolazne transakcije određuje cenovnik troškova samo na osnovu efektivnosti datuma. Ovo ponašanje se razlikuje od podrazumevanog ponašanja, gde sistem bira cenovnik troškova koji se podudara i sa valutom projekta i sa efektivnošću datuma.

Zbog ovih promena u ponašanju, kupci Projektnih operacija će moći da održe globalni cenovnik troškova koji će biti relevantan za celu kompaniju. Neće morati da imaju cenovnike u svakoj valuti poslovanja. Globalni cenovnik će imati efekat datuma i omogućiće podešavanje stope troškova u bilo kojoj valuti za određenu kombinaciju vrednosti dimenzija cena. Valuta cenovnik troška se koristi samo za unos podrazumevanih vrednosti prilikom kreiranja **cena uloga,** cena kategorija **i** zapisa artikala **cenovnik**. Neće se koristiti za određivanje cenovnka.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
