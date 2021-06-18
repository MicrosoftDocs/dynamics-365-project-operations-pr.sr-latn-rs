---
title: Ažuriranje projekta
description: Ova tema pruža informacije o ažuriranju projekata u usluzi Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c07542444b970430d8143a60aad6970305769b22
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993388"
---
# <a name="update-a-project"></a><span data-ttu-id="8f4bc-103">Ažuriranje projekta</span><span class="sxs-lookup"><span data-stu-id="8f4bc-103">Update a project</span></span>

<span data-ttu-id="8f4bc-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="8f4bc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8f4bc-105">U nastavku se nalazi rezime polja koja se mogu ažurirati u projektu nakon kreiranja i sve primenljive implikacije ažuriranja.</span><span class="sxs-lookup"><span data-stu-id="8f4bc-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="8f4bc-106">Polja detalja o projektu</span><span class="sxs-lookup"><span data-stu-id="8f4bc-106">Project detail fields</span></span>

- <span data-ttu-id="8f4bc-107">**Naziv**: Naslov projekta.</span><span class="sxs-lookup"><span data-stu-id="8f4bc-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="8f4bc-108">**Opis**: Pregled projekta.</span><span class="sxs-lookup"><span data-stu-id="8f4bc-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="8f4bc-109">**Klijent**: Preduzeće kojem će projekat biti isporučen.</span><span class="sxs-lookup"><span data-stu-id="8f4bc-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="8f4bc-110">**Predložak kalendara**: Radno vreme projekta.</span><span class="sxs-lookup"><span data-stu-id="8f4bc-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="8f4bc-111">Kada se polje promeni, ceo raspored se preračunava.</span><span class="sxs-lookup"><span data-stu-id="8f4bc-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="8f4bc-112">**Valuta**: Valuta projekta.</span><span class="sxs-lookup"><span data-stu-id="8f4bc-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="8f4bc-113">Ovo polje se podrazumevano zasniva na valuti definisanoj u ugovornoj jedinici.</span><span class="sxs-lookup"><span data-stu-id="8f4bc-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="8f4bc-114">Kada se ugovorna jedinica ažurira, polje se takođe ažurira.</span><span class="sxs-lookup"><span data-stu-id="8f4bc-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="8f4bc-115">**Ugovorna jedinica**: Organizaciona jedinica koja predstavlja grupu ili odeljenje preduzeća koje je prvenstveno odgovorno za povećanje prodaje i upravljanje isporukom posla i usluga klijentu.</span><span class="sxs-lookup"><span data-stu-id="8f4bc-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="8f4bc-116">**Menadžer projekta**: Član projektnog tima koji ima ovlašćenje da pregleda i odobri stavke vremena i troškove.</span><span class="sxs-lookup"><span data-stu-id="8f4bc-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="8f4bc-117">Polja za procenu</span><span class="sxs-lookup"><span data-stu-id="8f4bc-117">Estimate fields</span></span>

- <span data-ttu-id="8f4bc-118">**Procenjeni datum početka**: Datum početka projekta.</span><span class="sxs-lookup"><span data-stu-id="8f4bc-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="8f4bc-119">Kada se ovo polje ažurira, svi zadaci na projektu pomeriće svoj početak srazmerno novom datumu početka.</span><span class="sxs-lookup"><span data-stu-id="8f4bc-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="8f4bc-120">**Datum završetka**: Datum za kada je planiran završetak projekta.</span><span class="sxs-lookup"><span data-stu-id="8f4bc-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="8f4bc-121">**Angažovanje**: Procenjeno angažovanje u projektu.</span><span class="sxs-lookup"><span data-stu-id="8f4bc-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="8f4bc-122">Kada se zadaci dodaju u projekat, ovo polje više nije moguće uređivati.</span><span class="sxs-lookup"><span data-stu-id="8f4bc-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="8f4bc-123">**Procenjena cena rada**: Procenjena cena rada na projektu.</span><span class="sxs-lookup"><span data-stu-id="8f4bc-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="8f4bc-124">Kada se cene rada dodaju u projekat, ovo polje više nije moguće uređivati.</span><span class="sxs-lookup"><span data-stu-id="8f4bc-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="8f4bc-125">**Procenjeni troškovi**: Procenjeni troškovi projekta.</span><span class="sxs-lookup"><span data-stu-id="8f4bc-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="8f4bc-126">Kada se troškovi dodaju u projekat, ovo polje više nije moguće uređivati.</span><span class="sxs-lookup"><span data-stu-id="8f4bc-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="8f4bc-127">Polja stvarnih vrednosti projekta</span><span class="sxs-lookup"><span data-stu-id="8f4bc-127">Project actual fields</span></span>
- <span data-ttu-id="8f4bc-128">**Stvarni početak**: Datum kada je projekat započet.</span><span class="sxs-lookup"><span data-stu-id="8f4bc-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="8f4bc-129">**Stvarni završetak**: Biće ažuriran kada se projekat završi.</span><span class="sxs-lookup"><span data-stu-id="8f4bc-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="8f4bc-130">Polja statusa projekta</span><span class="sxs-lookup"><span data-stu-id="8f4bc-130">Project status fields</span></span>

- <span data-ttu-id="8f4bc-131">**Sveukupni status projekta**: Sveukupna ispravnost projekta koju obezbeđuje menadžer projekta.</span><span class="sxs-lookup"><span data-stu-id="8f4bc-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="8f4bc-132">**Komentari**: Opisivanje trenutne ispravnosti projekta koju je obezbedio menadžer projekta.</span><span class="sxs-lookup"><span data-stu-id="8f4bc-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]