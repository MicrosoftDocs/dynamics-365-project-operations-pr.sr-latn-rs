---
title: Napredak projekta i troškovi korišćenja
description: Ova tema pruža informacije o praćenju napretka projekta i troškova korišćenja.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 56b78aa70f23a9a723f008973678bb29c4bbce1d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575275"
---
# <a name="project-progress-and-cost-consumption"></a>Napredak projekta i troškovi korišćenja

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Potreba da se prati napredak u odnosu na raspored razlikuje se od delatnosti do delatnosti. Neke delatnosti obavljaju praćenje na najdetaljnijem nivou, dok druge to rade na višem nivou. Ova tema pokazuje kako obaviti zakazivanje da biste ispunili potrebe svoje organizacije.

## <a name="effort-tracking-view"></a>Prikaz za praćenje angažovanja

Prikaz **Praćenje aktivnosti** prati napredak zadataka u rasporedu. Prikaz poredi stvarno utrošene časove angažovanja na zadatku prema planiranim časovima angažovanja za zadatak. Project Service Automation koristi sledeće formule za izračunavanje metrika za praćenje:

U početku na kreiranju zadatka: Planirani troškovi će biti postavljeni na procenjene troškove po završetku. Kada se stvarne vrednosti evidentiraju u zadatku, sledi izračunavanje na osnovu prikaza praćenja za angažovanje

- Procenat napretka = Stvarno vreme angažovanja do danas ÷ Procena pri završetku (EAC) 
- Procena do završetka (ETC) = Procena pri završetku (EAC) – Stvarno vreme angažovanja do danas 
- EAC = Preostalo angažovanje + Stvarno vreme angažovanja do danas 
- Odstupanje od projektovanog angažovanja = Planirano angažovanje - EAC

Project Service Automation prikazuje projekciju odstupanja od angažovanja na zadatku. Ako je EAC veći od planiranog angažovanja, predviđa se da će zadatak oduzeti više vremena nego što je prvobitno planirano. Stoga, zaostaje za planom. Ako je EAC manji od planiranog angažovanja, predviđa se da će zadatak oduzeti manje vremena nego što je prvobitno planirano. Stoga će biti dovršen pre nego što je planirano.

## <a name="reprojecting-effort"></a>Ponovno projektovanje angažovanja

Uobičajeno je da menadžer projekta revidira originalne procene zadatka. Ponovne projekcije projekata predstavljaju način na koji menadžer projekta percipira procene, s obzirom na trenutni status projekta. Međutim, ne preporučujemo da menadžeri projekta menjaju osnovne vrednosti zato što osnovne vrednosti projekta predstavljaju uspostavljen izvor istine za raspored projekta i procenu troškova, a svi zainteresovani za projekat su je prihvatili.

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

Prikaz **Praćenje troškova** upoređuje stvarne troškove potrošene na zadatak i planirane troškove. 

> [!NOTE]
> Ovaj prikaz prikazuje samo troškove rada i ne uključuje troškove iz procena troškova. 

Project Service Automation koristi sledeće formule za izračunavanje metrika za praćenje:

Kada se kreira zadatak, planirani trošak jednak je procenjenim troškovima pri završetku. Kada se stvarne vrednosti evidentiraju u zadatku, sledeće će biti izračunato na osnovu prikaza **Praćenje** za troškove:

 - Procenat ostvarenih troškova = Stvarni troškovi do danas ÷ Procenjeni troškovi po završetku za zadatak
 - Troškovi do završetka (CTC) = Procenjeni troškovi po završetku – Stvarni troškovi ostvareni do danas
 - Procenjeni troškovi po završetku = CTC + Stvarni troškovi ostvareni do danas
 - Predviđeno odstupanje od troškova = Planirani troškovi – Procenjeni troškovi po završetku

Projekcija odstupanja od troškova je prikazana na zadatku. Ako su procenjeni troškovi po završetku veći od planiranih troškova, predviđa se da će zadatak koštati više nego što je prvobitno planirano. Zbog toga ima trend prekoračenja budžeta. Ako su procenjeni troškovi po završetku manji od planiranih troškova, predviđa se da će zadatak koštati manje nego što je prvobitno planirano i da ima trend neiskorišćenog budžeta.

## <a name="project-managers-reprojection-of-cost"></a>Ponovna projekcija troškova od strane menadžera projekta

Kada se angažovanje ponovo projektuje, CTC, Procenjeni troškovi po završetku, procenat ostvarenih troškova i odstupanja od projektovanih troškova ponovo se izračunavaju u prikazu **Praćenje troškova**.

## <a name="project-status-summary"></a>Rezime statusa projekta

Podaci za praćenje u prikazima **Praćenje aktivnosti** i **Praćenje troškova** prikazuju napredak i troškove korišćenja na nivou osnovnog čvora projekta, rezimiranih zadataka i zadataka čvorova lista. Odeljak **Status** na stranici **Entitet projekta** prikazuje rezime statusa na nivou projekta.

## <a name="status-summary-fields"></a>Polja rezimea statusa

Polje **Opšti status projekta** je polje koje može da se uređuje i koje pokazuje opšti status projekta. Koristi kodiranje u boji, kao što su zelena, žuta i crvena, da ukaže na povećani rizik. Polje **Komentari** omogućava menadžeru projekta da unese konkretne komentare o statusu. Polje **Status ažuriran dana** nije moguće uređivati i vrednost je vremenska oznaka koja pokazuje kada je status zadnji put ažuriran.

Polja **Performanse rasporeda** i **Performanse troškova** su podešena od datuma praćenja. Kada su odstupanja od rasporeda i troškova za osnovni čvor u prikazu **Praćenje angažovanja** pozitivna, možete podesiti ova polja na **Pre plana**. Kada su odstupanja od rasporeda i troškova za osnovni čvor negativna, možete ih podesiti na **Zaostaje za planom**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
