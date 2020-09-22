---
title: Uslovna rezervacija resursa
description: Ova tema pruža informacije o tome kako preliminarno ili uslovno rezervisati članove projektnog tima.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.prod: Applies to Project Service version 3.x
ms.technology: ''
ms.assetid: 04e02ff7-1024-4b65-a281-6f149921b63d
ms.author: ruhercul
audience: Admin
ms.openlocfilehash: 07e768d756732e31df82a9865b957dae09c60821
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755132"
---
# <a name="soft-book-a-resource"></a>Uslovna rezervacija resursa

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Uslovno možete da rasporedite ili „uslovno rezervišete“ resurs u projektni tim kako biste prikazali da nameravate da dodelite resurs tom projektu. Uslovne rezervacije ne troše dostupni kapacitet resursa, a možete da dodelite uslovno rezervisane članove tima projektnim zadacima. Međutim, zato što uslovna rezervacija troši kapacitet resursa, i dalje možete da „fiksno rezervišete“ resurs za ostale zadatke u okviru istog perioda. Generički resursi ne mogu biti uslovno rezervisani niti uslovno rezervisanje može da ispuni zahtev za generički resurs.

Uslovno rezervisani članovi projektnog tima su navedeni na kartici **Tim** stranice **Projekat**, a uslovno rezervisani sati su prikazani u koloni **Uslovno rezervisani sati** u prikazu **Imenovani članovi tima**. Uslovno rezervisani članovi tima su takođe navedeni u tabeli rasporeda. Zato što su uslovno rezervisani, tabela rasporeda ne prikazuje nikakvo korišćenje kapaciteta za te resurse. Uslovno rezervisano vreme se ne prikazuju na kartici **Usaglašenost** niti u polju **Produženje rezervacija** na kartici **Usaglašenost** tabele rasporeda. 

Člana tima možete uslovno da rezervišete za projekat na dva načina: direktno iz tabele rasporeda ili dodavanjem člana tima na kartici **Tim**. 

## <a name="soft-book-from-the-schedule-board"></a>Uslovno rezervisanje iz tabele rasporeda
Obavite sledeće korake da biste uslovno rezervisali resurs iz tabele rasporeda. 

1. Otvorite tabelu rasporeda, a zatim na tabli **Potrebe za rezervacijama** izaberite karticu **Projekat**.
2. Pronađite projekat za koji želite da uslovno rezervišete resurs. Ako postoji veliki broj projekata na listi, izaberite zaglavlje kolone **Projekat**, a zatim pomoću filtera potražite jedan ili više projekata.
3. Izaberite projekat, a zatim ga prevucite i otpustite na mrežu vremena resursa.
5. U tabli **Kreiranje rezervacije resursa** prilagodite datum početka i završetka, podesite **Status rezervacije** na **Uslovna**, a zatim podesite sate. 
6. Kliknite na **Rezerviši**. Resurs se sada prikazuje na kartici **Tim** kao resurs za projekat. U prikazu **Imenovani član tima** videćete uslovno rezervisane sate u koloni **Uslovno rezervisani sati**.

> [!NOTE]
> Sada možete odmah da dodelite uslovno rezervisane sate zadacima na kartici **Raspored**. Na kartici **Usaglašenost** resurs prikazuje deficit rezervacije u odnosu na njihovu dodelu zadatka jer kartica **Usaglašenost** uzima u obzir samo fiksne rezervacije. Možete da koristite funkciju **Produži rezervacije** da biste fiksno rezervisali resurs i otklonili manjak fiksnih rezervacija u odnosu na dodele resursa. Moraćete ručno da otkažete uslovnu rezervaciju resursa korišćenjem opcije **Održavanje rezervacija**.

## <a name="soft-book-on-the-team-tab"></a>Uslovno rezervisanje na kartici Tim

Možete da dodate članove tima direktno na kartici **Tim**, a zatim promenite njihov status rezervacije iz **Fiksna** u **Uslovna** pomoću opcije **Održavanje rezervacija**. Kada na ovaj način dodate člana tima, to će uvek dovesti do fiksne rezervacije osim ako ne izaberete **Nijedan** način dodele.

Da biste koristili ovaj način, obavite sledeće korake.

1. Na stranici **Projekat**, na kartici **Tim** kliknite na **Novo**.
2. Izaberite resurs koji je moguće rezervisati, ulogu, kao i datume početka i završetka.
3. Izaberite način dodele koji nije **Nijedan**.
4. Izaberite stavku **Sačuvaj**. Videćete resurs na mreži a njegove sate u koloni **Fiksno rezervisani sati**.
5. Održite rezervacije resursa izborom opcije **Održavanje rezervacija**.
6. Kada se otvori tabela rasporeda, razvijte resurs da biste prikazali njegove rezervacije. Videćete rezervaciju prikazanu kao **Fiksna**.
7. Kliknite desnim tasterom miša na rezervaciju, u okviru opcije **Promena statusa**, izaberite **Uslovno rezerviši** \> **Uslovno**. Status rezervacije je sada **Uslovna**.
8. Nakon zatvaranja tabele rasporeda, videćete da su na mreži kartice **Tim** sati za resurs premešteni iz kolone **Fiksno rezervisani sati** u **Uslovno rezervisani sati**, kada gledate u prikazu **Imenovani članovi tima**.

> [!NOTE]
> Kada koristite opciju **Održavanje rezervacija** da biste promenili status sa **Fiksna** na **Uslovna**, ako fiksno rezervišete resurs za tim, a zatim mu dodelite zadatke, dodele zadataka za resurs se čuvaju. Međutim, na kartici **Usaglašenost**, resurs će imati nedostatak rezervacije jer se samo fiksne rezervacije uzimaju u obzir prilikom usaglašavanja rezervacija u odnosu na dodele. Možete da koristite funkciju **Produži rezervacije** na kartici **Usaglašenost** da biste fiksno rezervisali resurs i otklonili manjak fiksnih rezervacija u odnosu na dodele resursa. Moraćete da otkažete uslovnu rezervaciju za resurs korišćenjem opcije **Održavanje rezervacija**.

Kada budete spremni da promenite resurs uslovno rezervisanog člana tima u fiksno rezervisanog člana tima, postupite na sledeći način:

1. Na tabeli rasporeda, razvijte resurs da biste prikazali njegove rezervacije. Videćete da je rezervacija prikazana kao **Uslovna**.
2. Kliknite desnim tasterom miša na rezervaciju, pa u okviru opcije **Promena statusa** izaberite **Fiksno rezerviši** \> **Fiksno**. Status rezervacije je sada **Fiksna**.
3. Nakon zatvaranja tabele rasporeda, vratite se u projekat i otvorite karticu **Tim**, videćete da su na kartici **Tim** sati za resurs premešteni iz kolone **Uslovno rezervisani** u kolonu **Fiksno rezervisani sati**, kada ste u prikazu **Imenovani članovi tima**. Ako je resurs bio dodeljen zadacima, oni više neće prikazivati manjak rezervacija na kartici **Usaglašenost** jer su njihove rezervacije sada fiksne.

