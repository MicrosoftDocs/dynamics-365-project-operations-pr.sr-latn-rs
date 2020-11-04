---
title: Podešavanje prodajnog cenovnika
description: Ova tema pruža informacije o radu sa prodajnim cenovnicima za određivanje cena proizvoda u projektu.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d2c797b72666123eb0a18d2d0c1df9fe3d207f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083635"
---
# <a name="sales-price-list-setup"></a><span data-ttu-id="5a4bd-103">Podešavanje prodajnog cenovnika</span><span class="sxs-lookup"><span data-stu-id="5a4bd-103">Sales price list setup</span></span>

<span data-ttu-id="5a4bd-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="5a4bd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5a4bd-105">Za projektne ponude i ugovore, cenovnik projekta ima različit obrazac za zamenu cena u odnosu na cenovnik proizvoda.</span><span class="sxs-lookup"><span data-stu-id="5a4bd-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="5a4bd-106">U stavci ponude zasnovanoj na katalogu proizvoda možete da zamenite cenu za uloge i kategorije direktno u stavci ponude, jer svaka stavka ponude ukazuje na tačno jednu stavku kataloga.</span><span class="sxs-lookup"><span data-stu-id="5a4bd-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="5a4bd-107">Međutim, u stavci ponude zasnovanoj na projektu ne možete da zamenite cenu za uloge i kategorije direktno u stavci ponude.</span><span class="sxs-lookup"><span data-stu-id="5a4bd-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="5a4bd-108">Cenovnik projekata možete koristiti za rad sa dva različita obrasca zamene.</span><span class="sxs-lookup"><span data-stu-id="5a4bd-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="5a4bd-109">Preporučujemo da imate poseban cenovnik za resurse projekta i stavke kataloga, zbog razlika u ponašanju između njih kada zamenite cene.</span><span class="sxs-lookup"><span data-stu-id="5a4bd-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="5a4bd-110">Svaki od sledećih entiteta može imati jednu ili više pridruženih cenovnika prodaje za cenu projekata:</span><span class="sxs-lookup"><span data-stu-id="5a4bd-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="5a4bd-111">Klijent (poslovni kontakt)</span><span class="sxs-lookup"><span data-stu-id="5a4bd-111">Customer (account)</span></span> 
- <span data-ttu-id="5a4bd-112">Mogućnost za poslovanje</span><span class="sxs-lookup"><span data-stu-id="5a4bd-112">Opportunity</span></span> 
- <span data-ttu-id="5a4bd-113">Ponuda</span><span class="sxs-lookup"><span data-stu-id="5a4bd-113">Quote</span></span> 
- <span data-ttu-id="5a4bd-114">Ugovor za projekat</span><span class="sxs-lookup"><span data-stu-id="5a4bd-114">Project Contract</span></span>

<span data-ttu-id="5a4bd-115">Povezivanje ovih entiteta sa cenovnikom je naznačeno cenovnikom projekta.</span><span class="sxs-lookup"><span data-stu-id="5a4bd-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="5a4bd-116">Možete da povežete neke cenovnike sa entitetima prodaje Klijent, Mogućnost za poslovanje, Ponuda i Ugovor o projektu.</span><span class="sxs-lookup"><span data-stu-id="5a4bd-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="5a4bd-117">Podrazumevani cenovnik projekta se ne unosi automatski u zapis klijenta.</span><span class="sxs-lookup"><span data-stu-id="5a4bd-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="5a4bd-118">Međutim, cenovnik projekta možete ručno priložiti zapisu klijenta.</span><span class="sxs-lookup"><span data-stu-id="5a4bd-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="5a4bd-119">Ipak, trebalo bi ručno da priložite cenovnik projekta samo kada imate prilagođeni ugovor o određivanju cena sa klijentom.</span><span class="sxs-lookup"><span data-stu-id="5a4bd-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="5a4bd-120">Kada je cenovnik projekta priložen entitetu prodaje, proveravaju se sledeće informacije:</span><span class="sxs-lookup"><span data-stu-id="5a4bd-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="5a4bd-121">Da li cenovnik ima kontekst **prodaje**.</span><span class="sxs-lookup"><span data-stu-id="5a4bd-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="5a4bd-122">Da li se valuta cenovnika podudara sa valutom klijenta.</span><span class="sxs-lookup"><span data-stu-id="5a4bd-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="5a4bd-123">U ugovoru o projektu se koristi sledeći redosled prioriteta da bi se automatski podesili povezani cenovnici projekta:</span><span class="sxs-lookup"><span data-stu-id="5a4bd-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="5a4bd-124">Ponuda</span><span class="sxs-lookup"><span data-stu-id="5a4bd-124">Quote</span></span>
2. <span data-ttu-id="5a4bd-125">Mogućnost za poslovanje</span><span class="sxs-lookup"><span data-stu-id="5a4bd-125">Opportunity</span></span>
3. <span data-ttu-id="5a4bd-126">Klijent</span><span class="sxs-lookup"><span data-stu-id="5a4bd-126">Customer</span></span> 
4. <span data-ttu-id="5a4bd-127">Globalna podešavanja</span><span class="sxs-lookup"><span data-stu-id="5a4bd-127">Global settings</span></span> 

<span data-ttu-id="5a4bd-128">Kada se cenovnik projekta unese podrazumevano, sistem proverava da li se valuta podudara sa valutom klijenta i da li podrazumevani cenovnici koji su uneti imaju kontekst **prodaje**.</span><span class="sxs-lookup"><span data-stu-id="5a4bd-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="5a4bd-129">Možete da povežete više cenovnika projekta sa entitetima Klijent, Mogućnost za poslovanje, Ponuda i Ugovor o projektu.</span><span class="sxs-lookup"><span data-stu-id="5a4bd-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="5a4bd-130">Ova mogućnost podržava podrazumevane cene za određeni datum za dugoročni ugovor o projektu, gde možete da zahtevate više od jednog cenovnika kako biste u obzir uzeli izmene cena do kojih dolazi zbog inflacije.</span><span class="sxs-lookup"><span data-stu-id="5a4bd-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="5a4bd-131">Međutim, ako se za cenovnike koje povežete sa entitetom Klijent, Mogućnost za poslovanje, Ponuda ili Ugovor o projektu preklapaju datumi stupanja na snagu, podrazumevane cene mogu biti netačne.</span><span class="sxs-lookup"><span data-stu-id="5a4bd-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="5a4bd-132">Zbog toga bi trebalo da proverite da cenovnici projekata sa datumima stupanja na snagu koji se preklapaju nisu povezani sa tim entitetima.</span><span class="sxs-lookup"><span data-stu-id="5a4bd-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>
