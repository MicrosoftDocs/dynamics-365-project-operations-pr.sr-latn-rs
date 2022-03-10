---
title: Zašto se cena podrazumevano vraća na nulu na stvarnim podacima o utrošenom vremenu prodaje?
description: Rešavanje problema zbog čega se cena podrazumevano vraća na 0 u stvarnim podacima o utrošenom vremenu prodaje.
author: rumant
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
ms.openlocfilehash: 2df4ce2d6391e70fea8e8f15c1b5774c9a9bfbe5f5ef2e6d8da8668afd34d4c9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992583"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>Zašto se cena podrazumevano vraća na nulu na stvarnim podacima o utrošenom vremenu prodaje?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ova najčešća pitanja se odnose na stvarne podatke u kojima je klasa transakcije podešena na Vreme, a gde je vrsta transakcije Nenaplaćena prodaja. Slede tri provere koje će vam olakšati da rešite zbog čega se cena (stopa naplate) podrazumevano vraća na vrednost 0 u stvarnim podacima o utrošenom vremenu prodaje.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>Provera 1: Identifikujte prodajni cenovnik za projekat

Pronađite projekat iz polja Projekat za stvarni podatak i idite na stranicu projekta. Zatim idite do kartice „Sales“ i na a mreži Predmeti ugovora za projekat kliknite na vezu u polju Ugovor za projekat. Otvoriće se stranica Ugovor za projekat. Na stranici Ugovor za projekat, idite na karticu Cenovnik za projekat. Proverite da li je tamo priložen bar jedan cenovnik. Ako nijedan cenovnik nije priložen u mreži Cenovnici projekta za Ugovor za projekat, izolovali ste problem. Priložite cenovnik mreži Cenovnici projekta. Cenovnik koji je ovde dozvoljeno priložiti treba da ima polje konteksta podešeno na Sales, a polje valute u cenovniku treba da se podudara sa poljem valute u Ugovoru za projekat. Nakon što ste obavili potrebne popravke, ponovo kreirajte unos utrošenog vremena, odobrite ga i potvrdite da stvarni podatak o nenaplaćenoj prodaji prikazuje važeću cenu. 

Ako imate jedan ili više priloženih cenovnika na mreži Cenovnici projekta u Ugovoru za projekat, nastavite na sledeću proveru u dokumentu.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>Provera 2: Da li je bilo koji od cenovnika identifikovanih iznad važeći za određeni datum stvarnog podatka o utrošenom vremenu prodaje?

Da bi Project Service razmotrio cenovnik za podrazumevanu cenu, taj cenovnik treba da bude primenjiv za datum na stvarnom podatku o utrošenom vremenu prodaje. Proverite sledeće da biste proverili da li su cenovnici identifikovani iznad primenjivi:
- Proverite da li su datumi početka i završetka na kartici Opšti podaci za priložene cenovnike prazni. Ako su datumi početka i završetka na cenovnicima identifikovanim gore prazni, izolovali ste problem. 
- Zabeležite polje datuma početka na stvarnom podatku o utrošenom vremenu prodaje i proverite da li je neki od identifikovanih cenovnika primenjiv za taj datum. Na primer, datum stvarnog podatka o utrošenom vremenu prodaje bi trebalo da pada unutar datuma početka i završetka u cenovniku. 
    - Ako ne postoji nijedan cenovnik koji pokriva taj datum na stvarnom podatku o utrošenom vremenu prodaje, izolovali ste problem. Izmenite datume početka i završetka za cenovnik da biste osigurali da cenovnik pokriva datum stvarnog podatka o utrošenom vremenu prodaje. 
    - Ako postoji više cenovnika koji pokrivaju taj datum na stvarnom podatku o utrošenom vremenu prodaje, izolovali ste problem. Ovo možete da ispravite uređivanjem datuma početka i završetka cenovnika, tako da postoji samo jedan cenovnik koji pokriva datum stvarnog podatka o utrošenom vremenu prodaje. 
    - Ako postoji samo jedan cenovnik koji pokriva datum stvarnog podatka o utrošenom vremenu prodaje, idite na proveru broj 3.
Nakon što ste obavili potrebne popravke, ponovo kreirajte unos utrošenog vremena, odobrite ga i potvrdite da stvarni podatak o utrošenom vremenu prodaje prikazuje važeću cenu.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>Proverite 3: Da li postoji cena u cenovniku za dimenzije formiranja cene na stvarnoj podatku o utrošenom vremenu prodaje?

Ako ste uspešno dovršili proveru 1 i proveru 2, trebalo bi sada da imate samo jedan cenovnik koji je primenljiv za datum stvarnog podatka o utrošenom vremenu prodaje. Otvorite ovaj cenovnik i idite do kartice Cene uloga. Uverite se da postoji red u mreži za dimenzije obrazovanja cena u stvarnom podatku o utrošenom vremenu prodaje.

Ako u mreži uloge cene ne postoji red za dimenzije obrazovanja cene na stvarnom podatku o utrošenom vremenu prodaje, onda ste izolovali problem. Kreirajte red u mreži Cene uloga za dimenzije određivanja cena na stvarnom podatku o utrošenom vremenu prodaje. Nakon što to uradite, ponovo kreirajte unos utrošenog vremena, odobrite ga i potvrdite da stvarni podatak o utrošenom vremenu prodaje prikazuje važeću cenu.

Ako i dalje ne vidite važeću cenu u stvarnom podatku o utrošenom vremenu prodaje nakon obavljene gorenavedene tri provere, pošaljite tiket podršci. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]