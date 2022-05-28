---
title: Primena usluge Project Operations – jednostavno
description: Ova tema pruža informacije o tome kako da instalirate primenu usluge Project Operations Lite – od pogodbe do profakture.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: e33506504665f2e7ef7ad48469082f9f64a2a44b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580749"
---
# <a name="deploy-project-operations---lite"></a>Primena usluge Project Operations – jednostavno

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_



Project Operations podržava više modela primene. Da biste utvrdili najbolji model primene, pogledajte članak [Vrste primena](determine-deployment-type.md).


> [!IMPORTANT]
> Ova primena, Lite primena – od pogodbe do profakture, rezultira **samo u Project Operations primeni u usluzi Dataverse**.

- [Instaliranje operacija projekta u novo Dataverse okruženje](#new)
- [Instaliranje u postojeće Dataverse okruženje](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a> Instaliranje operacija projekta u novo Dataverse okruženje

1. Kao globalni [ili administrator sa Power Platform licencom](/power-platform/admin/global-service-administrators-can-administer-without-license) za projektne operacije, kreirajte novo Dataverse okruženje u [PowerPlatform admin centru](https://admin.powerplatform.com). Uverite se da **je omogućeno kreiranje baze podataka** za **ovo okruženje i Dynamics 365** aplikacije. Za više informacija, pogledajte odeljak [Kreiranje i upravljanje okruženjima u Power Platform centru administracije](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Izaberite **Microsoft Dynamics 365 Project Operations** sa liste za primenu Dynamics 365 aplikacija.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a> Instaliranje projektnih operacija u postojeće Dataverse okruženje
1. Uverite se da okruženje nije konfigurisano sa dvostrukim [upisivanja kao](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) instalacijom, a zatim ćete [instalirati operacije projekta za mogućnosti scenarija zasnovanih na resursima/neodovršenim](project-operations-integrated-deployment-overview.md) scenarijima.
2. Kao [globalni ili Power Platform administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) sa licencom za Project Operations, locirajte okruženje u [PowerPlatform centru administracije](https://admin.powerplatform.com) gde želite da instalirate Project Operations.
3. Instalirajte **Microsoft Dynamics 365 Project Operations** sa liste za primenu Dynamics 365 aplikacija. Više informacija potražite u članku [Upravljanje Dynamics 365 aplikacijama](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
