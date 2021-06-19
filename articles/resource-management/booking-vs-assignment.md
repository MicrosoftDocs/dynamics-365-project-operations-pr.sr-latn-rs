---
title: Rezervacije u odnosu na dodele
description: Ova tema pruža informacije o razlikama između rezervisanja resursa i dodeljivanja resursa.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c1a1003af0b23c4be44fefac0b3c4ea725f96b2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012783"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="1de08-103">Rezervacije u odnosu na dodele</span><span class="sxs-lookup"><span data-stu-id="1de08-103">Bookings vs assignments</span></span>

<span data-ttu-id="1de08-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="1de08-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1de08-105">Rezervacije predstavljaju fiksnu ili uslovnu raspodelu resursa za projekat.</span><span class="sxs-lookup"><span data-stu-id="1de08-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="1de08-106">Fiksne rezervacije troše kapacitet resursa.</span><span class="sxs-lookup"><span data-stu-id="1de08-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="1de08-107">Rezervacije predstavljaju organizacione koncepte timova kako bi mogli da razumeju kako će se resursi angažovati na različitim projektima.</span><span class="sxs-lookup"><span data-stu-id="1de08-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="1de08-108">Dynamics 365 Project Operations smatra rezervacije konceptom na nivou projekta.</span><span class="sxs-lookup"><span data-stu-id="1de08-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="1de08-109">Za razliku od rezervacija, dodele predstavljaju obavezivanje resursa za projektne zadatke u rasporedu projekata.</span><span class="sxs-lookup"><span data-stu-id="1de08-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="1de08-110">Resursi mogu biti imenovani ili generički.</span><span class="sxs-lookup"><span data-stu-id="1de08-110">The resources can be named or generic.</span></span>  <span data-ttu-id="1de08-111">Kada se zahtev za resurs izvede iz dodele projektnog zadatka, Project Operations koristi konture aktivnosti dodele resursa za izradu kontura detalja o zahtevu za resurs.</span><span class="sxs-lookup"><span data-stu-id="1de08-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="1de08-112">Međutim, pozivanje na dodele resursa se ne održava.</span><span class="sxs-lookup"><span data-stu-id="1de08-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="1de08-113">Ažuriranja rezervacija izvedenih iz zahteva za resurs ne ažuriraju nijednu dodelu resursa.</span><span class="sxs-lookup"><span data-stu-id="1de08-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="1de08-114">Uobičajeno je da je zbir rezervacija za resurs jednak zbiru dodela resursa za jedan ili više zadataka.</span><span class="sxs-lookup"><span data-stu-id="1de08-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="1de08-115">Međutim, Project Operations ne sprovodi ovaj dogovor.</span><span class="sxs-lookup"><span data-stu-id="1de08-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="1de08-116">Prikaz **Usaglašenost** pokazuje menadžeru projekata mesta gde se rezervacije i dodele resursa ne slažu.</span><span class="sxs-lookup"><span data-stu-id="1de08-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]