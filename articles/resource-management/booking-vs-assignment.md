---
title: Rezervacije u odnosu na dodele
description: Ova tema pruža informacije o razlikama između rezervisanja resursa i dodeljivanja resursa.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3aaf8dcbae0a5762879c2b1223eba3bdc33af1a7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279920"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="7c79c-103">Rezervacije u odnosu na dodele</span><span class="sxs-lookup"><span data-stu-id="7c79c-103">Bookings vs assignments</span></span>

<span data-ttu-id="7c79c-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="7c79c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7c79c-105">Rezervacije predstavljaju fiksnu ili uslovnu raspodelu resursa za projekat.</span><span class="sxs-lookup"><span data-stu-id="7c79c-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="7c79c-106">Fiksne rezervacije troše kapacitet resursa.</span><span class="sxs-lookup"><span data-stu-id="7c79c-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="7c79c-107">Rezervacije predstavljaju organizacione koncepte timova kako bi mogli da razumeju kako će se resursi angažovati na različitim projektima.</span><span class="sxs-lookup"><span data-stu-id="7c79c-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="7c79c-108">Dynamics 365 Project Operations smatra rezervacije konceptom na nivou projekta.</span><span class="sxs-lookup"><span data-stu-id="7c79c-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="7c79c-109">Za razliku od rezervacija, dodele predstavljaju obavezivanje resursa za projektne zadatke u rasporedu projekata.</span><span class="sxs-lookup"><span data-stu-id="7c79c-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="7c79c-110">Resursi mogu biti imenovani ili generički.</span><span class="sxs-lookup"><span data-stu-id="7c79c-110">The resources can be named or generic.</span></span>  <span data-ttu-id="7c79c-111">Kada se zahtev za resurs izvede iz dodele projektnog zadatka, Project Operations koristi konture aktivnosti dodele resursa za izradu kontura detalja o zahtevu za resurs.</span><span class="sxs-lookup"><span data-stu-id="7c79c-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="7c79c-112">Međutim, pozivanje na dodele resursa se ne održava.</span><span class="sxs-lookup"><span data-stu-id="7c79c-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="7c79c-113">Ažuriranja rezervacija izvedenih iz zahteva za resurs ne ažuriraju nijednu dodelu resursa.</span><span class="sxs-lookup"><span data-stu-id="7c79c-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="7c79c-114">Uobičajeno je da je zbir rezervacija za resurs jednak zbiru dodela resursa za jedan ili više zadataka.</span><span class="sxs-lookup"><span data-stu-id="7c79c-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="7c79c-115">Međutim, Project Operations ne sprovodi ovaj dogovor.</span><span class="sxs-lookup"><span data-stu-id="7c79c-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="7c79c-116">Prikaz **Usaglašenost** pokazuje menadžeru projekata mesta gde se rezervacije i dodele resursa ne slažu.</span><span class="sxs-lookup"><span data-stu-id="7c79c-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]