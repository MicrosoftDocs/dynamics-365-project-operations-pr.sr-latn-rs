---
title: Najčešća pitanja o upravljanju resursima
description: Ova tema nudi odgovore na najčešća pitanja o upravljanju resursima.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: d335a12a9b478bff63b6c93809c89dac9718a4be
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144385"
---
# <a name="resource-management-faq"></a><span data-ttu-id="38b5c-103">Najčešća pitanja o upravljanju resursima</span><span class="sxs-lookup"><span data-stu-id="38b5c-103">Resource management FAQ</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="38b5c-104">Koja je razlika između člana tima i potrebe za resursom?</span><span class="sxs-lookup"><span data-stu-id="38b5c-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="38b5c-105">Član projektnog tima može biti dodeljen zadacima, rezervisan ili prebukiran, kao i podešen kao davalac odobrenja.</span><span class="sxs-lookup"><span data-stu-id="38b5c-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="38b5c-106">Potreba za resursom može postojati bez člana projektnog tima, kao radna verzija napomene o potražnji.</span><span class="sxs-lookup"><span data-stu-id="38b5c-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="38b5c-107">Koja je razlika između predloženih i uslovno rezerviranih sati?</span><span class="sxs-lookup"><span data-stu-id="38b5c-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="38b5c-108">Predloženi sati i uslovno rezervisani sati razlikuju se po vidljivosti.</span><span class="sxs-lookup"><span data-stu-id="38b5c-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="38b5c-109">Predloženi sati su vidljivi samo menadžerima resursa i menadžeru projekata koji su pokrenuli potražnju koristeći zahtev za resurs.</span><span class="sxs-lookup"><span data-stu-id="38b5c-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="38b5c-110">Uslovno rezervisani sati su vidljivi svima koji imaju pristup tabeli rasporeda.</span><span class="sxs-lookup"><span data-stu-id="38b5c-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="38b5c-111">Kako mogu da vidim uslovno rezervisane sate za resurse u timu?</span><span class="sxs-lookup"><span data-stu-id="38b5c-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="38b5c-112">Uslovne rezervacije možete da obavite kada rezervišete potrebu za resursom.</span><span class="sxs-lookup"><span data-stu-id="38b5c-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="38b5c-113">Resursi koji su uslovno rezervisani u projektnom timu prikazuju se kao članovi tima koji imaju uslovno rezervisane sate.</span><span class="sxs-lookup"><span data-stu-id="38b5c-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="38b5c-114">Prikazuju se i na tabeli rasporeda.</span><span class="sxs-lookup"><span data-stu-id="38b5c-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="38b5c-115">Kako da promenim zahtevane sate, datum početka i završetka za (generički ili imenovani) resurs koji je rezervisan?</span><span class="sxs-lookup"><span data-stu-id="38b5c-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="38b5c-116">Nakon rezervisanja resursa, izaberite **Održavanje rezervacija** da unesete promene koje su neophodne.</span><span class="sxs-lookup"><span data-stu-id="38b5c-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="38b5c-117">Koje vrste resursa podržava Project Service Automation?</span><span class="sxs-lookup"><span data-stu-id="38b5c-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="38b5c-118">**Korisnik** i **Kontakt** su jedine vrste resursa koje podržava Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="38b5c-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="38b5c-119">Iako možete da kreirate druge vrste resursa (na primer, **Oprema** i **Grupa**), nijedan slučaj njihovog kompletnog korišćenja nije podržan.</span><span class="sxs-lookup"><span data-stu-id="38b5c-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="38b5c-120">Koja je razlika između dodele i rezervacije?</span><span class="sxs-lookup"><span data-stu-id="38b5c-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="38b5c-121">Dodele predstavljaju dodele resursa projektnim zadacima u rasporedu projekata.</span><span class="sxs-lookup"><span data-stu-id="38b5c-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="38b5c-122">Resursi mogu biti stvarni ili generički resursi.</span><span class="sxs-lookup"><span data-stu-id="38b5c-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="38b5c-123">Rezervacije predstavljaju fiksnu ili uslovnu raspodelu resursa za projekat.</span><span class="sxs-lookup"><span data-stu-id="38b5c-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="38b5c-124">Fiksne rezervacije troše kapacitet resursa.</span><span class="sxs-lookup"><span data-stu-id="38b5c-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="38b5c-125">Idealno bi bilo da se za stvarne resurse slažu rezervacije i dodele, jer se ne razlikuju.</span><span class="sxs-lookup"><span data-stu-id="38b5c-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="38b5c-126">Međutim, PSA ne sprovodi ovaj dogovor.</span><span class="sxs-lookup"><span data-stu-id="38b5c-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="38b5c-127">Prikaz Usaglašenost pokazuje menadžeru projekata mesta gde se rezervacije i dodele resursa ne slažu.</span><span class="sxs-lookup"><span data-stu-id="38b5c-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
