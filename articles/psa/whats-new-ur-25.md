---
title: Šta je novo ili promenjeno u izdanju 25 ispravke Project Service Automation verzije 3
description: U ovoj temi su navedene funkcije i ispravke koje su dostupne u izdanju 25 ispravke za Project Service Automation verzije 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: a5a81893c4a804deb09cf33e0ac3f1a25b8bca36
ms.sourcegitcommit: a2b810219d381716d3eedb14c4eb6cdefb5b5845
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/02/2020
ms.locfileid: "4183560"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Šta je novo ili promenjeno u izdanju 25 ispravke Project Service Automation verzije 3

Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x. Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

U ovoj temi su navedene funkcije i ispravke koje su nove ili promenjene za Project Service Automation verzije 3, izdanje 25 ispravke. Ova verzija ima broj verzije V 3.10.43.76 i postala je opšte dostupna putem samostalne ispravke u oktobru 2020.

## <a name="update-release-25"></a>Izdanje ispravke 25

### <a name="bug-fixes"></a>Ispravke grešaka

**Vreme i trošak**

Sledeći problem je ispravljen:

- Grafikon stavke vremena koji prikazuje dodatne podatke na osnovu prevelikog intervala koji se preuzima.

**Upravljanje resursima**

Sledeći problem je ispravljen:

- Dodat je Package Deployer kôd za preskakanje uvoza zakrpe za uslugu Universal Resource Scheduling ako zakrpa više verzije već postoji.

**Upravljanje projektima**

Popravljeni su sledeći problemi:

- Ispravljene su razlike u zaokruživanju i kursnoj listi koje su dovodile do netačnih planiranih troškova u mreži za praćenje projekta.
- Podrška mogućnosti prikazivanja dve ili više mreža za reakcije na obrascu **Projekat**.
- Obezbeđena je validacija koja rešava problem sa mogućnošću dodeljivanja zadatka nakon datuma završetka kalendara, što je dovodilo do neuspele dodele resursa.
- Poboljšano je rukovanje greškama za rešavanje izuzetka prazne reference generisane iz sledećeg:

    - Dodatna komponenta **PreValidateProjectTeamMemberCreate**
    - **PreValidateProjectTaskCreate** kada se projektni zadatak kreira bez povezanog projekta
    - Dodatna komponenta **PreProjectTeamMemberCreate**
    - Dodatna komponenta **PostProjectTeamMemberDelete**
    - Dodatna komponenta **PreValidateProjectTaskDelete**

**Sales**

Popravljeni su sledeći problemi:

- Poboljšano je rukovanje greškama za rešavanje problema izuzetka prazne reference generisane iz **Kopiranje projekta: Procene za HelperResource Management**.
- **Nije spremno za fakturisanje** na stranici **Neizvršavanje naplate vremena i materijala** ne briše status naplate.
- Ispravljena su pogrešno označena dugmad **Cene** na karticama **Cena uloge** i **Stavke kataloga**.
