---
title: Podrazumevani cenovnici
description: Ovaj članak pruža informacije o podrazumevanim prodajnim i cenovnicima troškova u usluzi Project Operations.
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
1. Ako uz evidenciju poslovnih kontakata nisu priloženi cenovnici projekata, sistem pregleda prodajne cenovnike koji su priloženi uz parametre projekta koji odgovaraju valuti ponude za projekat.
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

Cenovnici troškova ne podrazumevaju nijedan entitet u usluzi Project Operations. Određivanje cenovnika troškova koji će se koristiti za troškove projekta vrši se uvek po transakciji. Sistem dovršava sledeći postupak da bi utvrdio koji će se cenovnik koristiti za cene projekta:

1. Sistem pregleda cenovnike koji su priloženi ugovornoj organizacionoj jedinici projekta.
1. Zatim sistem pregleda datum stupanja na snagu cenovnika koji se podudaraju sa datumom konteksta dolazne procene ili konteksta stvarne vrednosti.

    - *Kontekst procene* odnosi se na bilo koji od tri konteksta procene u usluzi Project Operations:

        - Linija procene za projekat
        - Detalj stavke ponude
        - Detalj predmeta ugovora

    - *Kontekst stvarne vrednosti* odnosi se na bilo koji od tri izvora za stvarne vrednosti u usluzi Project Operations:

       - Unos redova stavke knjiženja u glavnoj knjizi koji su ručno kreirani ili korektivne stavke knjiženja u glavnoj knjizi koji su kreirani u korektivnom dnevniku
       - Stavke u glavnoj knjizi koje se kreiraju tokom prosleđivanja evidencija vremena, troškova ili korišćenja materijala
       - Detalj stavke fakture

    Kada Project Operations podudara važenje datuma dolazne stavke u glavnoj knjizi ili detalju reda fakture u *kontekstu stvarne vrednosti*, on koristi polje **Datum transakcije**.

    - Ako više cenovnika važe za datum u kontekstu dolaznoj proceni ili kontekstu stvarne vrednosti, bira se poslednje kreirani cenovnik.
    - Ako uz projektnu jedinicu ugovorne organizacione jedinicu nije priložen nijedan cenovnik, sistem gleda cenovnike koštanja koji su priloženi uz parametre projekta koji odgovaraju valuti ponude za projekat.

## <a name="enable-multi-currency-cost-price-list"></a>Omogući cenovnik troškova u više valuta

Ovu postavku možete pronaći u **Postavke** \> **Parametri**. Podrazumevana vrednost je **Ne**.

Kada je ova postavka omogućena (to jest, kada je vrednost postavljena na **Da**), sistem se ponaša na sledeći način:

- Omogućava da cenovnici koštanja u bilo kojoj valuti budu povezani sa organizacionom jedinicom. Na primer, cenovnik koštanja u valuti EUR može biti priložen organizacionoj jedinici u valuti USD. Sistem će nastaviti da proverava da li cenovnici koštanja koji su priloženi organizacionoj jedinici nemaju efekat preklapanja datuma.
- Potvrđuje da cenovnici koštanja koji su priloženi parametrima projekta nemaju efekat preklapanja datuma, čak i ako imaju različite valute. Ovo ponašanje se razlikuje od podrazumevanog ponašanja (to jest ponašanja kada je vrednost postavljena na **Ne**). U podrazumevanom ponašanju, samo cenovnici koštanja koji imaju **istu** valutu proveravaju se za efekat datuma koji se ne preklapa.
- Za kontekst dolazne transakcije, određuje cenovnik koštanja samo na osnovu važenja datuma. Ovo ponašanje se razlikuje od podrazumevanog ponašanja, gde sistem bira cenovnik koštanja koji se podudara i sa valutom projekta i sa važenjem datuma.

Zbog ovih promena u ponašanju, Project Operations klijenti će moći da održavaju globalni cenovnik koštanja koji će biti relevantan za celo preduzeće. Neće morati da imaju cenovnike u svakoj valuti poslovanja. Globalni cenovnik će imati važenje datuma i omogućiće podešavanje stopa cena u bilo kojoj valuti za određenu kombinaciju vrednosti dimenzija određivanja cena. Valuta cenovnika koštanja se koristi samo za unos podrazumevanih vrednosti prilikom kreiranja zapisa stavki **Cena uloga**, **Cena kategorija** i **Cenovnik**. Neće se koristiti za određivanje cenovnika.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
