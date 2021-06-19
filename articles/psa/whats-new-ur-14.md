---
title: Šta je novo ili promenjeno u izdanju 14 ispravke Project Service Automation verzije 3
description: U ovoj temi date su informacije o tome šta je novo u izdanju ispravke 14 za Project Service Automation u verziji 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: 8754f8eace50f1fa5743c5611d94f8c86693ebc9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006888"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="0ce72-103">Project Service Automation izdanje ispravke 14, u verziji 3</span><span class="sxs-lookup"><span data-stu-id="0ce72-103">Project Service Automation Update Release 14, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="0ce72-104">Sa zadovoljstvo najavljujemo najnoviju ispravku za aplikaciju Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="0ce72-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="0ce72-105">Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="0ce72-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="0ce72-106">Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="0ce72-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="0ce72-107">Da biste ažurirali ovo izdanje, posetite centar za administraciju za Dynamics 365 online i idite do stranice sa rešenjima kako biste instalirali ispravku.</span><span class="sxs-lookup"><span data-stu-id="0ce72-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="0ce72-108">Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="0ce72-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="0ce72-109">U ovoj temi date su funkcije koje su nove ili su promenjene u rešenju PSA u verziji 3, izdanje ispravke 14.</span><span class="sxs-lookup"><span data-stu-id="0ce72-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="0ce72-110">Ova verzija ima broj verzije V3.10.4.21 i dostupna je prema sledećem planu:</span><span class="sxs-lookup"><span data-stu-id="0ce72-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="0ce72-111">**Opšta dostupnost (samo-ispravka):** januar 2020. godine</span><span class="sxs-lookup"><span data-stu-id="0ce72-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="0ce72-112">**Auto-ispravka:** februar 2020. godine</span><span class="sxs-lookup"><span data-stu-id="0ce72-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="0ce72-113">Izdanje ispravke 14</span><span class="sxs-lookup"><span data-stu-id="0ce72-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="0ce72-114">Poboljšanja</span><span class="sxs-lookup"><span data-stu-id="0ce72-114">Enhancements</span></span>

- <span data-ttu-id="0ce72-115">Sales</span><span class="sxs-lookup"><span data-stu-id="0ce72-115">Sales</span></span>

     - <span data-ttu-id="0ce72-116">Vrednosti iz prilagođenih polja iz **Detalji stavke ponude** se kopiraju u **Detalji predmeta ugovora za projekat** kada se ponuda ispravi na **Zatvorena kao dobijena**.</span><span class="sxs-lookup"><span data-stu-id="0ce72-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="0ce72-117">Potvrđeni projekti mogu imati status **Zatvorena kao izgubljena**.</span><span class="sxs-lookup"><span data-stu-id="0ce72-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="0ce72-118">Upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="0ce72-118">Resource Management</span></span>

     - <span data-ttu-id="0ce72-119">Kada produžavate rezervacije, od korisnika će biti zatraženo da u dijalogu za potvrdu rezimiraju rezultate rezervacija i navedu vezu do opcije „Održavanje rezervacija“.</span><span class="sxs-lookup"><span data-stu-id="0ce72-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="0ce72-120">Ispravke grešaka</span><span class="sxs-lookup"><span data-stu-id="0ce72-120">Bug fixes</span></span>

- <span data-ttu-id="0ce72-121">Vreme i trošak</span><span class="sxs-lookup"><span data-stu-id="0ce72-121">Time and Expense</span></span>

     - <span data-ttu-id="0ce72-122">Ispravljeno: poboljšano korisničko iskustvo kada korisnik nije izabrao nijednu stavku koju treba ispraviti.</span><span class="sxs-lookup"><span data-stu-id="0ce72-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="0ce72-123">Upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="0ce72-123">Resource Management</span></span>

     - <span data-ttu-id="0ce72-124">Ispravljeno: rezervacija resursa više puta prekoračuje ime resursa koji je moguće rezervisati.</span><span class="sxs-lookup"><span data-stu-id="0ce72-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="0ce72-125">Sales</span><span class="sxs-lookup"><span data-stu-id="0ce72-125">Sales</span></span>

     - <span data-ttu-id="0ce72-126">Ispravljeno: ukupna prodajna cena se ne izračunava sve dok korisnik ne unese i cenu koštanja za procene troškova za projekat.</span><span class="sxs-lookup"><span data-stu-id="0ce72-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="0ce72-127">Ispravljeno: zatvaranje ponude kao **Osvojena** ne uspeva ako ugovorni projekat nije u statusu **Radna verzija**.</span><span class="sxs-lookup"><span data-stu-id="0ce72-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]