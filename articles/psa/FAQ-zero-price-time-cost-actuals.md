---
title: Zašto se cena podrazumevano vraća na nulu u stvarnim podacima o ceni za utrošeno vreme?
description: Rešavanje problema zbog čega se cena podrazumevano vraća na 0 u stvarnim podacima o ceni za utrošeno vreme.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 124719410f89dea506d43a1b64cb91c85d4f3968
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131397"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>Zašto se cena podrazumevano vraća na nulu u stvarnim podacima o ceni za utrošeno vreme?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ova najčešća pitanja se odnose na stvarne podatke gde je klasa transakcije podešena na Vreme, a gde je vrsta transakcije Trošak. Slede tri provere koje će vam olakšati da rešite zbog čega se cena podrazumevano vraća na vrednost 0 u stvarnim podacima o ceni za utrošeno vreme.
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>Provera 1: Identifikujte cenovnik koštanja za projekat

Pronađite projekat iz polja Projekat za stvarni podatak, a zatim idite na stranicu projekta. Kliknite na vezu jedinice ugovaranja u polju. Na stranici Jedinica ugovaranja proverite da li jedinica ugovaranja ima cenovnik u mreži Cenovnici koštanja.

Ako postoji više od jednog cenovnika, izolovali ste problem. Project Service podržava samo jedan cenovnik po organizacionoj jedinici. Uklonite sve cenovnike iz ovog entiteta sve dok ne ostane samo jedan priložen cenovnik u mreži Cenovnici koštanja za organizacionu jedinicu.

Ako organizacionoj jedinici nije priložen nijedan cenovnik, zabeležite valutu organizacione jedinice. Idite u Project Service, a zatim na stavku Parametri i otvorite karticu Cenovnici. Proverite da li postoje cenovnici čiji je kontekst podešen na Cena, a da se valuta podudara sa valutom organizacione jedinice.
 
Ako ne postoje cenovnici koji ispunjavaju kriterijume, izolovali ste problem. Uverite se da imate bar jedan cenovnik čiji je kontekst podešen na Cena i čija se valuta podudara sa valutom organizacione jedinice.

Ako postoji više cenovnika koji ispunjavaju kriterijume, nastavite sa čitanjem ovog dokumenta kako biste obavili dodatne provere.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>Provera 2: Da li je bilo koji od cenovnika identifikovanih iznad važeći za određeni datum stvarnog podatka o ceni za utrošeno vreme?

Da bi Project Service razmotrio cenovnik za podrazumevanu cenu, taj cenovnik treba da bude primenjiv za datum na stvarnom podatku o ceni za utrošeno vreme. Proverite sledeće da biste proverili da li su cenovnici identifikovani iznad primenjivi:

- Proverite da li su datumi početka i završetka na kartici Opšti podaci za priložene cenovnike prazni. Ako su datumi početka i završetka na cenovnicima identifikovanim gore prazni, izolovali ste problem. 
- Zabeležite polje datuma početka na stvarnom podatku o ceni za utrošeno vreme i proverite da li je neki od identifikovanih cenovnika primenjiv za taj datum. Na primer, datum stvarnog podatka o ceni za utrošeno vreme bi trebalo da pada unutar datuma početka i završetka u cenovniku. 
    - Ako ne postoji nijedan cenovnik koji pokriva taj datum na stvarnom podatku o ceni za utrošeno vreme, izolovali ste problem. Izmenite datume početka i završetka za cenovnik da biste osigurali da cenovnik pokriva datum stvarnog podatka o ceni za utrošeno vreme. 
    - Ako postoji više cenovnika koji pokrivaju taj datum na stvarnom podatku o ceni za utrošeno vreme, izolovali ste problem. Ovo možete da ispravite uređivanjem datuma početka i završetka cenovnika, tako da postoji samo jedan cenovnik koji pokriva datum stvarnog podatka o ceni za utrošeno vreme. 
    - Ako postoji samo jedan cenovnik koji pokriva datum stvarnog podatka o ceni za utrošeno vreme, pređite na sledeću proveru u dokumentu.
Nakon što ste obavili potrebne popravke, ponovo kreirajte unos utrošenog vremena, odobrite ga i potvrdite da stvarni podatak o ceni za utrošeno vreme prikazuje važeću cenu.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>Proverite 3: Da li postoji cena u cenovniku za dimenzije formiranja cene na stvarnoj podatku o ceni za utrošeno vreme?

Ako ste uspešno dovršili proveru 1 i proveru 2, trebalo bi sada da imate samo jedan cenovnik koji je primenljiv za datum stvarnog podatka o ceni za utrošeno vreme. Otvorite ovaj cenovnik i idite do kartice Cene uloga. Uverite se da postoji red u mreži za dimenzije obrazovanja cena u stvarnom podatku o ceni za utrošeno vreme.

Ako u mreži uloge cene ne postoji red za dimenzije obrazovanja cene na stvarnom podatku o ceni za utrošeno vreme, onda ste izolovali problem. Kreirajte red u mreži Cene uloga za dimenzije određivanja cena na stvarnom podatku o ceni za utrošeno vreme. Nakon što to uradite, ponovo kreirajte unos utrošenog vremena, odobrite ga i potvrdite da stvarni podatak o ceni za utrošeno vreme prikazuje važeću cenu.
 
Ako i dalje ne vidite važeću cenu u stvarnom podatku o ceni za utrošeno vreme nakon što obavite gorenavedene tri provere, pošaljite tiket podršci.



