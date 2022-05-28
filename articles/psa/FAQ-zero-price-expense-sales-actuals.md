---
title: Zašto se cena podrazumevano vraća na nulu u stvarnim podacima o troškovima prodaje?
description: Slede tri provere koje će vam olakšati da rešite zbog čega se cena podrazumevano vraća na vrednost 0 u stvarnim podacima o troškovima prodaje.
author: rumant
ms.prod: ''
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
ms.reviewer: johnmichalak
ms.openlocfilehash: d7221b9b5db986c8d57688893014a1bfd9ac4e41
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581945"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a>Zašto se cena podrazumevano vraća na nulu u stvarnim podacima o troškovima prodaje?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ova najčešća pitanja se odnose na stvarne podatke o troškovima u kojima je klasa transakcije podešena na Trošak, a gde je vrsta transakcije Nenaplaćena prodaja. Slede tri provere koje će vam olakšati da rešite zbog čega se cena (stopa naplate) podrazumevano vraća na vrednost 0 u stvarnim podacima o troškovima prodaje.

## <a name="check-1-identify-the-sales-price-list-for-project"></a>Provera 1: Identifikujte prodajni cenovnik za projekat

Pronađite projekat iz polja Projekat za stvarni podatak i idite na stranicu projekta. Zatim idite do kartice „Sales“. Na mreži Predmeti ugovora za projekat kliknite na vezu u polju Ugovor za projekat. Otvoriće se stranica Ugovor za projekat. Na stranici Ugovor za projekat, idite na karticu Cenovnik za projekat. Proverite da li je tamo priložen bar jedan cenovnik.

Ako nijedan cenovnik nije priložen u mreži Cenovnici projekta za Ugovor za projekat:

- Priložite cenovnik mreži Cenovnici projekta. Cenovnik koji je ovde dozvoljeno priložiti treba da ima polje konteksta podešeno na Sales, a polje valute u cenovniku treba da se podudara sa poljem valute u Ugovoru za projekat. Nakon što ste izvršili potrebne popravke, ponovo kreirajte unos troška, odobrite ga i potvrdite da stvarni podatak o nenaplaćenoj prodaji prikazuje važeću cenu.
- Ako imate jedan ili više priloženih cenovnika na mreži Cenovnici projekta u Ugovoru za projekat, idite na proveru broj 2.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a>Provera 2: Da li je bilo koji od cenovnika identifikovanih iznad važeći za određeni datum stvarnog podatka o trošku?

Da bi Project Service razmotrio cenovnik za podrazumevanu cenu, taj cenovnik treba da bude primenjiv za datum na stvarnom podatku za trošak prodaje. Proverite sledeće da biste proverili da li su cenovnici identifikovani iznad primenjivi:

- Počnite od provere da datumi početka i završetka na kartici Opšti podaci za priložene cenovnike nisu prazni. Ako su datumi početka i završetka na cenovnicima identifikovanim gore prazni, izolovali ste problem. 
- Zabeležite polje datuma početka na stvarnom podatku o trošku prodaje i proverite da li je neki od identifikovanih cenovnika primenjiv za taj datum. Na primer, datum stvarnog podatka o trošku bi trebalo da pada unutar datuma početka i završetka u cenovniku. 
    - Ako ne postoji nijedan cenovnik koji pokriva taj datum na stvarnom podatku o trošku prodaje, izolovali ste problem. Izmenite datume početka i završetka za cenovnik da biste osigurali da cenovnik pokriva datum stvarnog podatka o trošku. 
    - Ako postoji više cenovnika koji pokrivaju taj datum na stvarnom podatku o trošku prodaje, izolovali ste problem. Uredite datum početka i završetka cenovnika, tako da postoji samo jedan cenovnik koji pokriva datum stvarnog podatka o trošku. 
    - Ako postoji samo jedan cenovnik koji pokriva datum stvarnog podatka o trošku, pređite na proveru broj 3.
Nakon što ste obavili potrebne popravke, ponovo kreirajte unos troška, odobrite ga i potvrdite da stvarni podatak o nenaplaćenoj prodaji prikazuje važeću cenu.

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a>Provera 3: Da li postoji važeća cena za kategoriju troška u primenjivom cenovniku projekta? 

Ako ste uspešno dovršili proveru 1 i proveru 2, trebalo bi sada da imate samo jedan cenovnik projekta koji je primenljiv za datum stvarnog podatka o trošku prodaje. Otvorite ovaj cenovnik projekta i idite do kartice Cene kategorija. Uverite se da postoji red u mreži za navedenu kategoriju troška u stvarnom podatku o trošku.
 
- Ako ne postoji nijedan red, onda ste izolovali problem. Kreirajte red u mreži Kategorija cene za kategoriju u stvarnom podatku o trošku. Zatim ponovo kreirajte unos troška, odobrite ga i potvrdite da stvarni podatak o nenaplaćenoj prodaji prikazuje važeću cenu. 
- Ako postoji red za kategoriju troška u mreži Cene kategorije, proverite da li ima važeću cenu.

Da biste razumeli šta je važeća cena, koristite ove metode:

- Ako je polje Način određivanja cene u stavci Kategorija cena podešeno na „Po ceniׅ“, onda će jedinična stopa u stvarnom podatku o trošku prodaje podrazumevano biti vraćena na vrednost u stavci Trošak.
- Ako je polje Način određivanja cene u stavci Kategorija cena podešeno na Procenat provizije, onda proverite da li je polje Procenat podešeno na važeću vrednost. Jedinična stopa na stvarnom podatku o trošku prodaje se podrazumevano zadaje primenom ovog procenta marže na cenu u stavci Trošak.
- Ako je polje Način određivanja cene u stavci Kategorija cena podešeno na Cena po jedinici, onda proverite da li je polje Cena podešeno na važeću vrednost. Jedinična stopa na stvarnom podatku o trošku prodaje će biti podrazumevano podešena na iznos valute naveden u polju Cena.

Ako podešavanje cene za kategoriju troška nije važeće, onda ste izolovali problem. Rešenje je da uredite stavku cene za kategoriju sa važećom cenom za kategoriju troška u skladu sa pravilima iznad. Nakon što to uradite, ponovo kreirajte unos troška, odobrite ga, pa proverite da li stvarni podatak o nenaplaćenoj prodaji dobija važeću cenu.

Ako i dalje ne vidite važeću cenu u stvarnom podatku o trošku prodaje nakon obavljene gorenavedene tri provere, pošaljite tiket podršci.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
