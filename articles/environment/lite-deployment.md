---
title: Primena usluge Project Operations – jednostavno
description: Ovaj članak pruža informacije o tome kako da instalirate primenu usluge Project Operations jednostavna primena – od pogodbe do profakture.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 86293b725e86db3d4b8bdaf5810b16b7c670e8a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930335"
---
# <a name="deploy-project-operations---lite"></a>Primena usluge Project Operations – jednostavno

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_



Project Operations podržava više modela primene. Da biste utvrdili najbolji model primene, pogledajte članak [Vrste primena](determine-deployment-type.md).


> [!IMPORTANT]
> Ova primena, Lite primena – od pogodbe do profakture, rezultira **samo u Project Operations primeni u usluzi Dataverse**.

- [Instaliranje usluge Project Operations u novo Dataverse okruženje](#new)
- [Instalirajte u postojeće Dataverse okruženje](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>Instaliranje usluge Project Operations u novo Dataverse okruženje

1. Kao [globalni ili Power Platform administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) sa licencom za Project Operations, kreirajte novo Dataverse okruženje u [PowerPlatform centru administracije](https://admin.powerplatform.com). Uverite se da su omogućeni **Kreiranje baze podataka za ovo okruženje** i **Dynamics 365 aplikacije**. Za više informacija, pogledajte odeljak [Kreiranje i upravljanje okruženjima u Power Platform centru administracije](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Izaberite **Microsoft Dynamics 365 Project Operations** sa liste za primenu Dynamics 365 aplikacija.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>Instaliranje usluge Project Operations u postojeće Dataverse okruženje
1. Uverite se da okruženje nije konfigurisano sa [dvostrukim upisivanjem](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) jer će instalacija,tada instalirati mogućnosti [Project Operations za scenarije zasnovane na resursima/bez zaliha](project-operations-integrated-deployment-overview.md).
2. Kao [globalni ili Power Platform administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) sa licencom za Project Operations, locirajte okruženje u [PowerPlatform centru administracije](https://admin.powerplatform.com) gde želite da instalirate Project Operations.
3. Instalirajte **Microsoft Dynamics 365 Project Operations** sa liste za primenu Dynamics 365 aplikacija. Više informacija potražite u članku [Upravljanje Dynamics 365 aplikacijama](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
