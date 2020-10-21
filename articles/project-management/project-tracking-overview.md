---
title: Pregled praćenja projekata
description: Ova tema pruža informacije o tome kako da pratite napredak projekta i troškove korišćenja.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c998addbbdbbea8fe69c95f65e58a24146f394c8
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907380"
---
# <a name="project-tracking-overview"></a>Pregled praćenja projekata

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Potreba da se prati napredak u odnosu na raspored razlikuje se od delatnosti do delatnosti. Neke delatnosti obavljaju praćenje na najdetaljnijem nivou, dok druge to rade na višem nivou. Ova tema pokazuje kako obaviti zakazivanje da biste ispunili potrebe svoje organizacije.

## <a name="effort-tracking-view"></a>Prikaz za praćenje angažovanja

Prikaz **Praćenje angažovanja** prati napredak zadataka u rasporedu upoređujući stvarne sate angažovanja utrošene na zadatku sa planiranim satima angažovanja na zadatku. Dynamics 365 Project Operations koristi sledeće formule za izračunavanje metrika za praćenje:

- **Procenat napretka**: Stvarno vreme angažovanja do danas ÷ Procena pri završetku (EAC) 
- **Procena do završetka (ETC)**: Planirano angažovanje – Stvarno vreme angažovanja do danas 
- **EAC**: Preostalo angažovanje + Stvarno vreme angažovanja do danas 
- **Odstupanje od projektovanog angažovanja**: Planirano angažovanje – EAC

Project Operations prikazuje projekciju odstupanja od angažovanja na zadatku. Ako je EAC veći od planiranog angažovanja, predviđa se da će zadatak oduzeti više vremena nego što je prvobitno planirano i kasniće. Ako je EAC manji od planiranog angažovanja, predviđa se da će zadatak oduzeti manje vremena nego što je prvobitno planirano i biće ispred planiranog vremena.

## <a name="reprojecting-effort"></a>Ponovno projektovanje angažovanja

Menadžeri projekta često revidiraju originalne procene zadatka. Ponovne projekcije projekata predstavljaju način na koji menadžer projekta percipira procene, s obzirom na trenutni status projekta. Međutim, ne preporučujemo menadžerima projekata da menjaju osnovne vrednosti. To je zato što osnovne vrednosti projekta predstavljaju uspostavljen izvor istine za raspored projekta i procenu troškova, a svi zainteresovani za projekat su je prihvatili.

Postoje dva načina na koje menadžer projekta može ponovo da projektuje angažovanje na zadacima:

- Izmenite podrazumevani ETC novom procenom stvarnog preostalog angažovanja na zadatku. 
- Izmenite podrazumevani procenat napretka novom procenom stvarnog napretka zadatka.

Svaki od ovih pristupa dovodi do toga da se ponovo izračunaju ETC, EAC i procenat napretka zadatka, kao i odstupanje od projektovanog angažovanja na zadatku. EAC, ETC i procenat napretka u rezimiranim zadacima takođe se ponovo izračunavaju i stvaraju novu projekciju odstupanja od angažovanja.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Ponovna projekcija angažovanja za rezimirane zadatke

Angažovanje na rezimiranim zadacima ili zadacima kontejnera može se ponovno projektovati. Bez obzira da li korisnik ponovo projektuje pomoću preostalog angažovanja ili procenta napretka rezimiranih zadataka, započinje sledeći niz izračunavanja:

- EAC, ETC i procenat napretka zadatka se izračunavaju.
- Novi EAC se distribuira do nadređenih zadataka u istoj proporciji kao i izvorni EAC za zadatak.
- Izračunava se novi EAC za svaki od pojedinačnih zadataka sve do zadataka čvora lista. 
- Nadređeni zadaci na koje ovo utiče, sve do čvorova lista, imaju ponovno izračunat ETC i procenat napretka na osnovu EAC vrednosti. To rezultira novom projekcijom odstupanja od angažovanja na zadatku. 
- Ponovo se izračunavaju EAC-ovi rezimiranih zadataka sve do osnovnog čvora.

### <a name="cost-tracking-view"></a>Prikaz praćenja troškova 

Prikaz **Praćenje troškova** upoređuje stvarne troškove potrošene na zadatak i planirane troškove zadatka. 

> [!NOTE]
> Ovaj prikaz prikazuje samo troškove rada i ne uključuje troškove iz procena troškova. Project Operations koristi sledeće formule za izračunavanje metrika za praćenje:

- **Procenat ostvarenih troškova**: Stvarni troškovi do danas ÷ Procenjeni troškovi po završetku
- **Troškovi do završetka (CTC)**: Planirani troškovi – Stvarni troškovi ostvareni do danas
- **EAC**: Preostali troškovi + Stvarni troškovi ostvareni do danas
- **Odstupanje od projektovanih troškova**: Planirani troškovi – EAC

Projekcija odstupanja od troškova je prikazana na zadatku. Ako je EAC veći od planiranih troškova, predviđa se da će zadatak koštati više nego što je prvobitno planirano. Zbog toga ima trend prekoračenja budžeta. Ako je EAC manji od planiranih troškova, predviđa se da će zadatak koštati manje nego što je prvobitno planirano. Zbog toga ima trend neiskorišćenog budžeta.

## <a name="project-managers-reprojection-of-cost"></a>Ponovna projekcija troškova od strane menadžera projekta

Kada se angažovanje ponovo projektuje, CTC, EAC, procenat ostvarenih troškova i odstupanja od projektovanih troškova se ponovo izračunavaju u prikazu **Praćenje troškova**.

## <a name="project-status-summary"></a>Rezime statusa projekta

Podaci za praćenje u prikazima **Praćenje aktivnosti** i **Praćenje troškova** prikazuju napredak i troškove korišćenja na nivou osnovnog čvora projekta, rezimiranih zadataka i zadataka čvorova lista. Odeljak **Status** na stranici **Entitet projekta** prikazuje rezime statusa na nivou projekta.

## <a name="status-summary-fields"></a>Polja rezimea statusa

Polje **Opšti status projekta** je polje koje može da se uređuje i koje pokazuje opšti status projekta. Koristi kodiranje u boji, kao što su zelena, žuta i crvena, da ukaže na povećani rizik. Polje **Komentari** omogućava menadžeru projekta da unese konkretne komentare o statusu. Polje **Status ažuriran dana** nije moguće uređivati i vrednost je vremenska oznaka koja pokazuje kada je status zadnji put ažuriran.

Polja **Performanse rasporeda** i **Performanse troškova** su podešena od datuma praćenja. Kada su odstupanja od rasporeda i troškova za osnovni čvor u prikazu **Praćenje angažovanja** pozitivna, možete podesiti ova polja na **Pre plana**. Kada su odstupanja od rasporeda i troškova za osnovni čvor negativna, možete ih podesiti na **Zaostaje za planom**.
