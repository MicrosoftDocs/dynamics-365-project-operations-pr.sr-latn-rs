---
title: Podrazumevani cenovnici
description: Ova tema pruža informacije o podrazumevanim prodajnim i cenovnicima troškova u usluzi Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a5e38e2f0b553b789956c6d73d481ab0ed2ce3a77815e7cf8c058a0b4666c558
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989883"
---
# <a name="default-price-lists"></a>Podrazumevani cenovnici

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

## <a name="sales-price-lists"></a>Prodajni cenovnici

Svaka projektna ponuda i ugovor u usluzi Dynamics 365 Project Operations sadrži podrazumevani prodajni cenovnik. 

### <a name="price-list-default-on-project-quotes"></a>Podrazumevana vrednost cenovnika prema ponudama za projekat
Sistem dovršava sledeći postupak da bi utvrdio koji će se cenovnik podrazumevati za ponudu za projekat:

1. Sistem pregleda cenovnike koji su priloženi cenovnicima projektata poslovnih kontakata. 
2. Ako su uz evidenciju poslovnih kontakata priloženi cenovnici projekata, sistem pregleda prodajne cenovnike koji su priloženi uz parametre projekta koji odgovaraju valuti ponude za projekat.
3. Dalje, sistem proverava datum stupanja na snagu cenovnika koji se podudaraju sa opsegom datuma ponude za projekat. Konkretno, datum pravljenja ponude.
4. Ako postoji više cenovnika koji su na snazi na datum projektne ponude, svi cenovnici se podrazumevaju na projektnoj ponudi.
5. Ako nijedan cenovnik nije na snazi za datum projektne ponude, ne postoji podrazumevani projektni cenovnik projektne ponude. Na ponudi projekta pojaviće se poruka upozorenja. U poruci se navodi da pošto ne postoje priloženi cenovnici projekata, neće biti određena cena za procenjeni i stvarni rad i troškove na projektu.

### <a name="price-list-default-on-project-contracts"></a>Podrazumevana vrednost cenovnika prema ugovorima za projekat 
Sistem dovršava sledeći postupak da bi utvrdio koji će se cenovnik podrazumevati za ugovor za projekat:

1. Ako se ugovor kreira iz ponude, cenovnici projekata na ponudi se kopiraju odvojeno i prilažu uz ugovor o projektu.
2. Ako se ugovor kreira od početka, sistem pregleda cenovnike koji su priloženi projektnim cenovnicima poslovnog kontakta. Ako su uz evidenciju poslovnih kontakata nisu priloženi cenovnici projekata, sistem traži prodajne cenovnike koji su priloženi uz parametre projekta koji odgovaraju valuti ugovora za projekat.
4. Dalje, sistem proverava datum stupanja na snagu cenovnika koji se podudaraju sa opsegom datuma ugovora za projekat. Konkretno, datum pravljenja ugovora.
5. Ako postoji više cenovnika koji su na snazi na datum ugovora, svi cenovnici se podrazumevaju na ugovoru.
6. Ako nijedan cenovnik nije na snazi za datum ugovora, ne postoji podrazumevani projektni cenovnik na ugovoru. Na ugovoru projekta pojaviće se poruka upozorenja. U poruci se navodi da pošto ne postoje priloženi cenovnici projekata, neće biti određena cena za procenjeni i stvarni rad i troškove na projektu.

## <a name="cost-price-lists"></a>Cenovnici troškova

Cenovnici troškova ne podrazumevaju nijedan entitet u usluzi Project Operations. Određivanje cenovnika troškova koji će se koristiti za troškove projekta vrši se uvek u trenutku. Sistem dovršava sledeći postupak da bi utvrdio koji će se cenovnik koristiti za cene projekta:

1. Sistem prvo pregleda cenovnike koji su priloženi ugovornoj organizacionoj jedinici projekta.
2. Zatim sistem pregleda datum stupanja na snagu cenovnika koji se podudaraju sa datumom dolazne procene ili stvarne linije. U ovoj situaciji, *linija procene* odnosi se na sva tri konteksta procene u usluzi Project Operations:

    - Linija procene za projekat
    - Detalj stavke ponude
    - Detalj predmeta ugovora
  
3. Ako postoji više cenovnika koji važe za datum na dolaznoj proceni ili stvarnoj vrednosti, bira se najnoviji cenovnik.
4. Ako uz projektnu jedinicu ugovorne organizacione jedinicu nije priložen nijedan cenovnik, sistem gleda cenovnike koštanja koji su priloženi uz parametre projekta koji odgovaraju valuti ponude za projekat.
5. Zatim sistem pregleda datum stupanja na snagu cenovnika koji se podudaraju sa datumom dolazne procene ili stvarne linije. 
6. Ako postoji više cenovnika koji važe za datum na dolaznoj proceni ili stvarnoj vrednosti, bira se najnoviji cenovnik.
7. Ako uz parametre projekta nisu priloženi cenovnici troškova koji se podudaraju sa valutom i datumom stupanja na snagu, sistem podrazumevano vraća stopu troškova na nulu (0) na dolaznoj proceni ili stvarnoj liniji.


[!INCLUDE[footer-include](../includes/footer-banner.md)]