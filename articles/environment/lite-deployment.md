---
title: Primena usluge Project Operations – jednostavno
description: Ova tema pruža informacije o tome kako da instalirate primenu usluge Project Operations Lite – od pogodbe do profakture.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2470d573f4537cb22de4dbd98caff148cbe0bda3
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950281"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="595d9-103">Primena usluge Project Operations – jednostavno</span><span class="sxs-lookup"><span data-stu-id="595d9-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="595d9-104">_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="595d9-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="595d9-105">Project Operations podržava više modela primene.</span><span class="sxs-lookup"><span data-stu-id="595d9-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="595d9-106">Da biste utvrdili najbolji model primene, pogledajte članak [Vrste primena](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="595d9-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="595d9-107">Ova primena, Lite primena – od pogodbe do profakture, rezultira **samo u Project Operations primeni u usluzi Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="595d9-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="595d9-108">Instaliranje usluge Project Operations u novo CDS okruženje</span><span class="sxs-lookup"><span data-stu-id="595d9-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="595d9-109">Instalirajte u postojeće CDS okruženje</span><span class="sxs-lookup"><span data-stu-id="595d9-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="595d9-110">Instaliranje usluge Project Operations u novo CDS okruženje</span><span class="sxs-lookup"><span data-stu-id="595d9-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="595d9-111">Kao [globalni ili Power Platform administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) sa licencom za Project Operations, kreirajte novo CDS okruženje u [PowerPlatform centru administracije](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="595d9-111">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="595d9-112">Uverite se da su omogućene **CDS baza podataka** i **Dynamics 365 aplikacije**.</span><span class="sxs-lookup"><span data-stu-id="595d9-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="595d9-113">Za više informacija, pogledajte odeljak [Kreiranje i upravljanje okruženjima u Power Platform centru administracije](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="595d9-113">For more information, see [Create and manage environments in the Power Platform admin center](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="595d9-114">Izaberite **Microsoft Dynamics 365 Project Operations** sa liste za primenu Dynamics 365 aplikacija.</span><span class="sxs-lookup"><span data-stu-id="595d9-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="595d9-115">Instaliranje usluge Project Operations u postojeće CDS okruženje</span><span class="sxs-lookup"><span data-stu-id="595d9-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="595d9-116">Kao [globalni ili Power Platform administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) sa licencom za Project Operations, locirajte okruženje u [PowerPlatform centru administracije](https://admin.powerplatform.com) gde želite da instalirate Project Operations.</span><span class="sxs-lookup"><span data-stu-id="595d9-116">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="595d9-117">Instalirajte **Microsoft Dynamics 365 Project Operations** sa liste za primenu Dynamics 365 aplikacija.</span><span class="sxs-lookup"><span data-stu-id="595d9-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="595d9-118">Više informacija potražite u članku [Upravljanje Dynamics 365 aplikacijama](/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="595d9-118">For more information, see [Manage Dynamics 365 apps](/power-platform/admin/manage-apps).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]