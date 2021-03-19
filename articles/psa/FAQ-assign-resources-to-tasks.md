---
title: Dodeljivanje resursa zadatku
description: Ova tema pruža informacije o tome kako dodeliti resurse zadacima.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 486371df2de8b400f200dbf38e66cb5e2dec7ae7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286265"
---
# <a name="assign-a-resource-to-a-task"></a>Dodeljivanje resursa zadatku

[!include [banner](../includes/psa-now-project-operations.md)]

Postoje tri načina dodele resursa zadatku u usluzi Microsoft Dynamics 365 Project Service Automation.

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Rezervisanje resursa kao člana tima i dodela resursa zadatku

Resurs možete da dodate u projektni tim, a zatim da dodeljujete resurs zadacima u rasporedu projekta.

1. Na kartici **Član tima** dodajte novog člana tima tako što ćete izabrati **Novi**. 

2. Otvara se tabla za **brzo kreiranje člana tima**, gde možete da izaberete ime resursa koji može da se rezerviše i podesite ulogu. 

    Izaberite jedan od sledećih načina dodele za rezervaciju resursa:

    - **Puni kapacitet** rezerviše puni kapacitet resursa za navedene početne i krajnje datume.
    - **Procenat kapaciteta** rezerviše određeni procenat kapaciteta resursa za navedene datume početka i završetka.
    - **Ravnomerno raspoređivanje po satima** rezerviše resurs za određeni broj časova, ravnomerno ih raspoređujući po danu tokom navedenih datuma početka i završetka.
    - **Po satima – Početno opterećenje** rezerviše resurs za određeni broj časova, raspoređujući časove rada po danu na prve dane tokom navedenih datuma početka i završetka.
    - **Nijedno** dodaje resurs timu, ali ne kreira nijednu rezervaciju koja troši njihov kapacitet.

3. Na mreži **Raspored** za zadatak, izaberite ikonu **Resurs** u ćeliji resursa, a zatim u delu **Članovi tima** izaberite člana tima kojeg ste upravo dodali. 

> [!NOTE]
> Resurs prikazuje rezervisane i dodeljene časove i na karticama **Član tima** i **Usaglašenost**. Sati bi trebalo da budu isti, ali to nije neophodno jer rezervacije i dodele nisu čvrsto povezane. Kartica **Usaglašenost** vam daje detalje kada se razlikuju, kao kada dodelite resursu više časova nego što ste rezervisali. Po potrebi možete da ispravite informacije proširivanjem rezervacije resursa ili promenom dodele.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Kreiranje generičkog člana tima preko dodele zadatka

Kada kreirate generičkog člana tima preko dodele zadatka, kreirate čuvar mesta ili generički resurs koji opisuje karakteristike imenovanog resursa za kojeg naposletku želite da radi na zadacima. Zatim generišete uslov (ili prosleđujete zahtev korišćenjem zahteva) koji se koristi za pretragu i rezervaciju imenovanog resursa.

1. Na mreži **Raspored** za zadatak, izaberite ikonu **resursa** u ćeliji Resurs.

2. Unesite ime koje će služiti kao ime čuvara mesta resursa. Na primer, Menadžer programa.

3. Izaberite **Kreiraj**, pa u polju **Brzo kreiranje člana projektnog tima** podesite ulogu za generički resurs.

4. Možete da nastavite sa dodelom zadataka u ovaj resurs čuvara mesta izborom resursa u **biraču resursa** za zadatak. Oni su navedeni u okviru opcije **Članovi tima**.

5. Kada završite sa dodeljivanjem generičkog resursa, izaberite generički resurs na kartici **Tim**, a zatim izaberite **Generiši potrebu** da biste kreirali potrebu za resursom za generički resurs.

6. Izaberite opciju **Rezerviši** za generički resurs. Zatim možete da koristite tabelu rasporeda da biste pronašli i rezervisali pravi resurs. Možete i da prosledite zahtev za ispunjenje od strane menadžera resursa.

7. Kada generički resurs bude ispunjen imenovanim resursom, generički resurs se uklanja iz tima, a dodele zadatka iz generičkog resursa se dodeljuju imenovanom resursu koji je ispunio zahtev za resursom generičkog resursa.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Dodela imenovanog resursa sa liste svih resursa koji mogu da se rezervišu

Možete da koristite polje za pretragu u **biraču resursa** da biste pretraživali sve resurse koji mogu da se rezervišu i da ih dodelite zadatku.

Resursi dodeljeni na ovaj način dodaju se u tim bez ikakvih rezervacija. To je slično dodavanju člana tima i odluci da ne izaberete nijednu metodu dodele. Resurs se prikazuju na karticama **Tim** i **Usaglašenost** kao resurs samo sa dodelama i sa nedostatkom rezervacije. Rezervišete ih ako želite da koristite njihovu dostupnost.

1. Na mreži **Raspored** za zadatak, izaberite ikonu **resursa** u ćeliji Resurs.

2. Započnite unos imena. Prikazuju se rezultati pretrage za ime u **biraču resursa** u okviru opcije **Drugi resursi**.

3. Izaberite resurs koji želite da dodelite zadatku.



[!INCLUDE[footer-include](../includes/footer-banner.md)]