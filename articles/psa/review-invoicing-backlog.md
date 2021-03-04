---
title: Pregled preostalog fakturiranja za projekte i ugovore o projektima
description: Ova tema pruža informacije o tome kako pregledati preostalo vreme, troškove i proizvode i kako ih označiti kao spremne za fakturiranje.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 092455a131f556e4f943f6bb89d7e38358f0a697
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150505"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="e2289-103">Pregled preostalog fakturiranja za projekte i ugovore o projektima</span><span class="sxs-lookup"><span data-stu-id="e2289-103">Review the invoicing backlog on projects and project contracts</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e2289-104">Kada transakcija bude bila spremna za kreiranje i obradu fakture, transakcija treba biti obeležena kao **Spremno za fakturiranje**.</span><span class="sxs-lookup"><span data-stu-id="e2289-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="e2289-105">Ova tema opisuje vrste transakcija koje se mogu kreirati.</span><span class="sxs-lookup"><span data-stu-id="e2289-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="e2289-106">Pregled preostale naplate vremena i materijala</span><span class="sxs-lookup"><span data-stu-id="e2289-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="e2289-107">Kada se stavka vremena i troškova prosledi i odobri za projekt, PSA kreira stvarnu vrednost projekta.</span><span class="sxs-lookup"><span data-stu-id="e2289-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="e2289-108">Ako se kombinacija projekta i klase transakcije mapiraju u predmet ugovora za projekat zasnovan na vremenu i materijalu, kada se stavka odobri, kreiraju se dve stvarne vrednosti:</span><span class="sxs-lookup"><span data-stu-id="e2289-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="e2289-109">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="e2289-109">Cost actual</span></span> 
- <span data-ttu-id="e2289-110">Stvarna vrednost nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="e2289-110">Unbilled sales actual</span></span>

<span data-ttu-id="e2289-111">Stvarne vrednosti nenaplaćene prodaje predstavljaju preostalu naplatu i njihov status naplate mora biti podešen na **Spremno za fakturisanje**.</span><span class="sxs-lookup"><span data-stu-id="e2289-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="e2289-112">Kada se kreira faktura za projekat, stvarne vrednosti nenaplaćene prodaje označene kao **Spremno za fakturisanje** kopiraju se kao detalji stavke fakture.</span><span class="sxs-lookup"><span data-stu-id="e2289-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="e2289-113">Da biste pregledali preostale naplate za vreme i materijale, idite na **Prodaja** \> **Naplata** \> **Preostala naplata vremena i materijala**.</span><span class="sxs-lookup"><span data-stu-id="e2289-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="e2289-114">Odaberite sve stvarne vrednosti nenaplaćene prodaje koje su spremne za fakturisanje, a zatim izaberite **Spremno za fakturisanje**.</span><span class="sxs-lookup"><span data-stu-id="e2289-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="e2289-115">Status naplate ovih stvarnih vrednosti je promenjen u **Spremno za fakturisanje**.</span><span class="sxs-lookup"><span data-stu-id="e2289-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Preostala naplata vremena i materijala](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="e2289-117">Pregled preostale naplate za proizvod</span><span class="sxs-lookup"><span data-stu-id="e2289-117">Review the product billing backlog</span></span>

<span data-ttu-id="e2289-118">U aplikaciji PSA, kada projektni ugovor ima predmete ugovora zasnovane na proizvodima, ti predmeti se uzimaju u obzir za fakturisanje svaki put kada se kreira faktura za projektni ugovor.</span><span class="sxs-lookup"><span data-stu-id="e2289-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="e2289-119">Svaki proizvod koji ima predmete ugovora obeležene kao **Spremno za fakturisanje** kopira se u fakturu projekta kao stavke fakture za projekat.</span><span class="sxs-lookup"><span data-stu-id="e2289-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="e2289-120">Da biste pregledali preostalu naplatu za proizvod, idite na **Prodaja** \> **Naplata** \> **Preostala naplata za proizvod**.</span><span class="sxs-lookup"><span data-stu-id="e2289-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="e2289-121">Odaberite sve predmete ugovora zasnovane na proizvodima koji su spremni za fakturisanje, a zatim izaberite **Spremno za fakturisanje**.</span><span class="sxs-lookup"><span data-stu-id="e2289-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="e2289-122">Status naplate ovih stavki je promenjen u **Spremno za fakturisanje**.</span><span class="sxs-lookup"><span data-stu-id="e2289-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Preostala naplata za proizvod](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="e2289-124">Preged kontrolnih tačaka naplate u ugovorima sa fiksnom cenom</span><span class="sxs-lookup"><span data-stu-id="e2289-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="e2289-125">Svaki predmet ugovora za projekat koji koristi način naplate fiksne cene mora definisati kontrolne tačke u ugovoru.</span><span class="sxs-lookup"><span data-stu-id="e2289-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="e2289-126">Ove kontrolne tačke u ugovoru mogu se fakturisati samo ako su označene kao **Spremno za fakturisanje**.</span><span class="sxs-lookup"><span data-stu-id="e2289-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="e2289-127">Da biste pregledali kontrolne tačke naplate, idite na **Prodaja** \> **Naplata** \> **Kontrolne tačke sa fiksnom cenom**.</span><span class="sxs-lookup"><span data-stu-id="e2289-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="e2289-128">Odaberite kontrolne tačke koje su spremne za fakturisanje, a zatim izaberite **Spremno za fakturisanje**.</span><span class="sxs-lookup"><span data-stu-id="e2289-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="e2289-129">Status naplate ovih kontrolnih tačaka je promenjen u **Spremno za fakturisanje**.</span><span class="sxs-lookup"><span data-stu-id="e2289-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Kontrolne tačke sa fiksnom cenom](media/FPBacklog.png)
