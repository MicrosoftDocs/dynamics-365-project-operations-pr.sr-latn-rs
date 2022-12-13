---
title: Primena lite projektnih operacija
description: Ovaj članak pruža informacije o tome kako da instalirate primenu usluge Project Operations jednostavna primena – od pogodbe do profakture.
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/30/2022
ms.locfileid: "9810996"
---
# <a name="deploy-project-operations-lite"></a>Primena lite projektnih operacija

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_



Project Operations podržava više modela primene. Da biste utvrdili najbolji model primene, pogledajte članak [Vrste primena](determine-deployment-type.md).


> [!IMPORTANT]
> Ova primena, Lite primena – od pogodbe do profakture, rezultira **samo u Project Operations primeni u usluzi Dataverse**.

- [Instaliranje usluge Project Operations u novo Dataverse okruženje](#new)
- [Instalirajte u postojeće Dataverse okruženje](#existing)
- [Instaliranje u postojeće okruženje Dataverse koje ima Dual write komponente](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a> Instaliranje programa Project Operations Lite u novo Dataverse okruženje

1. Kao [globalni ili Power Platform administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) sa licencom za Project Operations, kreirajte novo Dataverse okruženje u [PowerPlatform centru administracije](https://admin.powerplatform.com). Uverite se da su omogućeni **Kreiranje baze podataka za ovo okruženje** i **Dynamics 365 aplikacije**. Za više informacija, pogledajte odeljak [Kreiranje i upravljanje okruženjima u Power Platform centru administracije](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
1. Izaberite **Microsoft Dynamics 365 Project Operations** sa liste za primenu Dynamics 365 aplikacija.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a> Instaliranje programa Project Operations Lite u postojeće Dataverse okruženje 
1. Kao [globalni ili Power Platform administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) sa licencom za Project Operations, locirajte okruženje u [PowerPlatform centru administracije](https://admin.powerplatform.com) gde želite da instalirate Project Operations.
1. Instalirajte **Microsoft Dynamics 365 Project Operations** sa liste za primenu Dynamics 365 aplikacija. Više informacija potražite u članku [Upravljanje Dynamics 365 aplikacijama](/power-platform/admin/manage-apps).

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a> Instaliranje programa Project Operations Lite u postojeće okruženje gde Dataverse su dualna rešenja za pisanje već prisutna

Ako želite da nastavite sa pokretanjem operacija projekta u režimu primene lite, trebalo bi da sledite ove korake:

1. Kao [globalni ili Power Platform administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) sa licencom za Project Operations, locirajte okruženje u [PowerPlatform centru administracije](https://admin.powerplatform.com) gde želite da instalirate Project Operations.
1. Instalirajte **Microsoft Dynamics 365 Project Operations** sa liste za primenu Dynamics 365 aplikacija. Više informacija potražite u članku [Upravljanje Dynamics 365 aplikacijama](/power-platform/admin/manage-apps).
1. Pošto vaše okruženje ima instalirane Dual write komponente koje pomažu u integraciji aplikacija za finansiranje i operacije, instalacija operacija projekta će takođe instalirati mogućnosti i proširenja potrebna za integrisanje podataka vezanih za projekat za finansiranje i operacije aplikacija. Pošto želite da pokrenete operacije projekta u lite raspoređivanju, ove komponente integracije bi trebalo da budu uklonjene jer će kreirati ograničenja i indirektne troškove za scenarije primene lite. Ručno deinstalirajte rešenja Dual **Dynamics 365 Project Operations Write** i **Dynamics 365 Project Operations Dual Write Entity Maps da biste** uklonili ove komponente.
1. Idite na **lokaciju Project Operations -> Settings -> Parameters**. Otvorite stranicu **"Detalji parametra** projekta" i postavite polje **Ponašanje nadogradnje** rešenja na opciju **"Samo lite"**. Ovim se obezbeđuje da naredne nadogradnje operacija projekta neće vratiti komponente integracije u operacije projekta.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
