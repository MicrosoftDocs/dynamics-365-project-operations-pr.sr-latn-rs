---
title: Praćenje angažovanja u projektu
description: Ovaj članak pruža informacije o tome kako da pratite angažovanje u projektu i napredak posla.
author: ruhercul
ms.date: 02/15/2022
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c41dbc138f6fc92a9586de173ba5dfc89c7e44e3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929277"
---
# <a name="project-effort-tracking"></a>Praćenje angažovanja u projektu

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Potreba da se prati napredak u odnosu na raspored razlikuje se od delatnosti do delatnosti. Neke delatnosti obavljaju praćenje na najdetaljnijem nivou, dok druge to rade na višem nivou. Ovaj članak pokazuje kako obaviti zakazivanje da biste ispunili potrebe svoje organizacije.

## <a name="effort-tracking-view"></a>Prikaz za praćenje angažovanja

Prikaz **Praćenje angažovanja** prati napredak zadataka u rasporedu upoređujući stvarne sate angažovanja utrošene na zadatku sa planiranim satima angažovanja na zadatku. Dynamics 365 Project Operations koristi sledeće formule za izračunavanje metrike za praćenje:

- **Procenat napretka**: Stvarno vreme angažovanja do danas ÷ Procena pri završetku (EAC) 
- **Preostalo angažovanje**: Procenjeno angažovanje – Stvarno vreme angažovanja do danas 
- **EAC**: Preostalo angažovanje + Stvarno vreme angažovanja do danas 
- **Odstupanje od projektovanog angažovanja**: Planirano angažovanje – EAC

Project Operations prikazuje projekciju odstupanja od angažovanja na zadatku. Ako je EAC veći od planiranog angažovanja, predviđa se da će zadatak oduzeti više vremena nego što je prvobitno planirano i kasniće. Ako je EAC manji od planiranog angažovanja, predviđa se da će zadatak oduzeti manje vremena nego što je prvobitno planirano i biće ispred planiranog vremena.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>Ponovno projektovanje angažovanja na zadacima čvora lista

Menadžeri projekta često revidiraju originalne procene zadatka. Ponovne projekcije projekata predstavljaju način na koji menadžer projekta percipira procene, s obzirom na trenutni status projekta. Međutim, ne preporučujemo menadžerima projekata da promene planirane brojeve angažovanja. To je zato što planirano angažovanje u projektu predstavlja utvrđeni izvor istine za raspored projekata i procenu troškova, a svi učesnici zainteresovani za projekat su se sa tim složili.

Menadžer projekta može da ponovo projektuje angažovanje na zadacima ažuriranjem podrazumevanih vrednosti **Preostalo angažovanje** sa novom procenom zadatka. Ova ispravka dovodi do toga da se za zadatak ponovo izračunaju procena po završetku (EAC), procenat napretka i odstupanje od projektovanog angažovanja na zadatku. EAC, ETC i procenat napretka u rezimiranim zadacima takođe se ponovo izračunavaju i stvaraju novu projekciju odstupanja od angažovanja.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Ponovna projekcija angažovanja za rezimirane zadatke

Angažovanje na rezimiranim zadacima ili zadacima kontejnera može se ponovno projektovati. Menadžeri projekta mogu ažurirati preostalo angažovanje na rezimiranim zadacima. Ažuriranje preostalog angažovanja pokreće sledeći skup izračunavanja u aplikaciji:

- Izračunavaju se EAC i procenat napretka zadatka.
- Novi EAC se distribuira do nadređenih zadataka u istoj proporciji kao i izvorni EAC za zadatak.
- Izračunava se novi EAC za svaki od pojedinačnih zadataka sve do zadataka čvora lista. 
- Podređeni zadaci na koje ovo utiče, sve do čvorova lista, imaju ponovno izračunato preostalo angažovanje i procenat napretka na osnovu EAC vrednosti. To rezultira novom projekcijom odstupanja od angažovanja na zadatku. 
- Ponovo se izračunavaju EAC-ovi rezimiranih zadataka sve do osnovnog čvora.
- Odobreni napor na zadatku rezimea je zbir odobrenih napora za sve podređene zadatke, kao i odobreni napor u zadatku rezimea.
- Preostali napor zadatka rezimea je zbir preostalih napora za sve podređene zadatke, manje odobreni napor u zadatku rezimea.

## <a name="project-status-summary"></a>Rezime statusa projekta

Podaci za praćenje u prikazima **Praćenje aktivnosti** i **Praćenje troškova** prikazuju napredak i troškove korišćenja na nivou osnovnog čvora projekta, rezimiranih zadataka i zadataka čvorova lista. Odeljak **Status** na stranici **Entitet projekta** prikazuje rezime statusa na nivou projekta.

## <a name="status-summary-fields"></a>Polja rezimea statusa

Polje **Opšti status projekta** je polje koje može da se uređuje i koje pokazuje opšti status projekta. Koristi kodiranje u boji, kao što su zelena, žuta i crvena, da ukaže na povećani rizik. Polje **Komentari** omogućava menadžeru projekta da unese konkretne komentare o statusu. Polje **Status ažuriran dana** nije moguće uređivati i vrednost je vremenska oznaka koja pokazuje kada je status zadnji put ažuriran.

Polja **Performanse rasporeda** i **Performanse troškova** su podešena od datuma praćenja. Kada su odstupanja od rasporeda i troškova za osnovni čvor u prikazu **Praćenje angažovanja** pozitivna, možete podesiti ova polja na **Pre plana**. Kada su odstupanja od rasporeda i troškova za osnovni čvor negativna, možete ih podesiti na **Zaostaje za planom**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
