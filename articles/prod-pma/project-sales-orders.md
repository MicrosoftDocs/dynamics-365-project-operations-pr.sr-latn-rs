---
title: Ulazne porudžbine projekta za projekte vremena i materijala
description: Ova tema objašnjava kako se kreiraju ulazne porudžbine zasnovane na projektima vremena i materijala.
author: Yowelle
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: dec9bc700d18f71ec7c9e976b38cb8cbb41f21b5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009678"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="859b6-103">Ulazne porudžbine projekta za projekte vremena i materijala</span><span class="sxs-lookup"><span data-stu-id="859b6-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="859b6-104">Ovaj tema opisuje kako se kreira ulazna porudžbina za projekat.</span><span class="sxs-lookup"><span data-stu-id="859b6-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="859b6-105">Ulazne porudžbine mogu se kreirati samo za projekte tog tipa **vreme i materijal**.</span><span class="sxs-lookup"><span data-stu-id="859b6-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="859b6-106">Ako projekat vremena i materijala sadrži više izvora finansiranja u ugovoru o projektu, morate omogućiti parametar **Dozvoli ulazne porudžbine za projekte sa više izvora finansiranja** na stranici **Upravljanje projektom i računovodstveni parametri**.</span><span class="sxs-lookup"><span data-stu-id="859b6-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="859b6-107">Podrška za ulazne porudžbine projekata sa više izvora finansiranja dostupna je počev od izdanja aplikacije 10.0.2 i novije.</span><span class="sxs-lookup"><span data-stu-id="859b6-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="859b6-108">Parametar koji će omogućiti podršku za ulazne porudžbine projekata sa više izvora finansiranja ukloniće se u talasu izdanja iz aprila 2020. godine, nakon čega će funkcionalnost uvek biti omogućena.</span><span class="sxs-lookup"><span data-stu-id="859b6-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="859b6-109">Ulazne porudžbine zasnovane na projektu možete kreirati na dva načina:</span><span class="sxs-lookup"><span data-stu-id="859b6-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="859b6-110">Idite na sam projekat.</span><span class="sxs-lookup"><span data-stu-id="859b6-110">Go to the project itself.</span></span> <span data-ttu-id="859b6-111">U oknu radnji izaberite **Upravljanje > Zadaci predmeta > Ulazna porudžbina**.</span><span class="sxs-lookup"><span data-stu-id="859b6-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="859b6-112">Informacije o projektu podrazumevano se stavljaju u ulaznu porudžbinu iz projekta.</span><span class="sxs-lookup"><span data-stu-id="859b6-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="859b6-113">Ako ugovor o projektu ima više izvora finansiranja, moraćete da izaberete izvor finansiranja da biste postavili klijenta za ulaznu porudžbinu.</span><span class="sxs-lookup"><span data-stu-id="859b6-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="859b6-114">Ako postoji samo jedan izvor finansiranja za projekat, klijent će biti automatski podešen.</span><span class="sxs-lookup"><span data-stu-id="859b6-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="859b6-115">Idite na stranicu liste **Sve ulazne porudžbine** i kreirajte novu ulaznu porudžbinu.</span><span class="sxs-lookup"><span data-stu-id="859b6-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="859b6-116">Za ulaznu porudžbinu ćete morati da izaberete projekat.</span><span class="sxs-lookup"><span data-stu-id="859b6-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="859b6-117">Kada izaberete projekat, klijent će biti postavljen iz izvora finansiranja ili ćete morati izabrati izvor finansiranja ako ugovor o projektu ima više izvora finansiranja.</span><span class="sxs-lookup"><span data-stu-id="859b6-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]