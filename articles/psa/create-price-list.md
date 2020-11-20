---
title: Kreiranje cenovnika
description: Kako da kreirate cenovnik u aplikaciji Project Service
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 08d93ad86d782922df6b22370749628ddbdc0718
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122045"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="ab861-103">Kreiranje cenovnika (Project Service)</span><span class="sxs-lookup"><span data-stu-id="ab861-103">Create a price list (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="ab861-104">Cenovnici menadžerima naloga pružaju šablon koji mogu koristiti za kreiranje ponuda i projekata, kao i za uspostavljanja troškova projekta.</span><span class="sxs-lookup"><span data-stu-id="ab861-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="ab861-105">Oni obezbeđuju spisak stavki predmeta sa ulogama i troškovima, kao i cenom koju ćete naplatiti za svaku.</span><span class="sxs-lookup"><span data-stu-id="ab861-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="ab861-106">Možete da kreirate više cenovnika tako da možete da održavate posebne strukture cena za različite regione u kojima prodajete vaše proizvode ili za različite kanale prodaje.</span><span class="sxs-lookup"><span data-stu-id="ab861-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="ab861-107">Bilo bi dobro da kreirate barem jedan cenovnik za svaku valutu u kojoj planirate da fakturišete klijentima.</span><span class="sxs-lookup"><span data-stu-id="ab861-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="ab861-108">Da biste kreirali finansijske procene za rad koji će biti obavljen, uverite se da svaki projekat ima odgovarajuću listu troškova i cenovnik prodaje.</span><span class="sxs-lookup"><span data-stu-id="ab861-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="ab861-109">Podesite podrazumevanu listu troškova i cenovnik prodaje koji se primenjuje na sve projekte kreirane u vašoj organizaciji.</span><span class="sxs-lookup"><span data-stu-id="ab861-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="ab861-110">Cenovnici se oslanjaju na uloge i kategorije troškova, tako da, pre nego što kreirate cenovnik, uverite se da ste već konfigurisali uloge i kategorije troškova koje želite da koristite prilikom kreiranja cenovnika.</span><span class="sxs-lookup"><span data-stu-id="ab861-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="ab861-111">Idite na **Project Service > Cenovnici**.</span><span class="sxs-lookup"><span data-stu-id="ab861-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="ab861-112">Kliknite na dugme **Novo**.</span><span class="sxs-lookup"><span data-stu-id="ab861-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="ab861-113">U opciji **Kontekst**, izaberite da li je ovaj cenovnik za **Trošak**, **Kupovinu** ili **Prodaju**.</span><span class="sxs-lookup"><span data-stu-id="ab861-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="ab861-114">U opciji **Ime** unesite ime za cenovnik.</span><span class="sxs-lookup"><span data-stu-id="ab861-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="ab861-115">U opciji **Valuta** izaberite valutu koju ćete da koristite za naplatu ili uspostavljanje troškova.</span><span class="sxs-lookup"><span data-stu-id="ab861-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="ab861-116">U opciji **Jedinica za vreme**, navedite vremenski period na koji se cena primenjuje, kao što su dan ili čas.</span><span class="sxs-lookup"><span data-stu-id="ab861-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="ab861-117">Popunite polja **Datum početka**, **Datum završetka** i **Opis**, a po potrebi.</span><span class="sxs-lookup"><span data-stu-id="ab861-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="ab861-118">Kliknite na dugme **Sačuvaj** za kreiranje zapisa tako da možete da nastavite ga uređujete.</span><span class="sxs-lookup"><span data-stu-id="ab861-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="ab861-119">Da biste dodali cenu uloge u cenovnik, kliknite na dugme **+** u okviru **Cene uloga**.</span><span class="sxs-lookup"><span data-stu-id="ab861-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="ab861-120">Popunite polja u obrascu **Cena uloge** i kliknite na dugme **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="ab861-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="ab861-121">Nastavite da dodajete cene uloge po potrebi.</span><span class="sxs-lookup"><span data-stu-id="ab861-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="ab861-122">Kada završite, kliknite na dugme **Sačuvaj** u donjem desnom uglu ekrana.</span><span class="sxs-lookup"><span data-stu-id="ab861-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="ab861-123">Da biste dodali cenu kategorije troška u cenovnik, kliknite na dugme **+** u okviru **Cene kategorija**.</span><span class="sxs-lookup"><span data-stu-id="ab861-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="ab861-124">Popunite polja u obrascu **Cena kategorije transakcije** i kliknite na dugme **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="ab861-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="ab861-125">Nastavite da dodajete cene kategorija po potrebi.</span><span class="sxs-lookup"><span data-stu-id="ab861-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="ab861-126">Kada završite, kliknite na dugme **Sačuvaj** u donjem desnom uglu ekrana.</span><span class="sxs-lookup"><span data-stu-id="ab861-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="ab861-127">Da biste dodali stavke cenovnika u cenovnik, kliknite na dugme **+** u okviru **Stavke cenovnika**.</span><span class="sxs-lookup"><span data-stu-id="ab861-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="ab861-128">Popunite polja u oknu **Stavka cenovnika** i kliknite na dugme **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="ab861-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="ab861-129">Nastavite da dodajete stavke cenovnika po potrebi.</span><span class="sxs-lookup"><span data-stu-id="ab861-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="ab861-130">Kada završite, kliknite na dugme **Sačuvaj** u donjem desnom uglu ekrana.</span><span class="sxs-lookup"><span data-stu-id="ab861-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="ab861-131">Da biste dodali odnose teritorije u cenovnik, kliknite na dugme **+** u okviru **Odnosi teritorije**.</span><span class="sxs-lookup"><span data-stu-id="ab861-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="ab861-132">Popunite polja u prozoru **Nova veza** i kliknite na dugme **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="ab861-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="ab861-133">Nastavite dodavanje odnosa teritorije po potrebi.</span><span class="sxs-lookup"><span data-stu-id="ab861-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="ab861-134">Kada završite, kliknite na dugme **Sačuvaj** u donjem desnom uglu ekrana.</span><span class="sxs-lookup"><span data-stu-id="ab861-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="ab861-135">Takođe pogledajte</span><span class="sxs-lookup"><span data-stu-id="ab861-135">See Also</span></span>  
 [<span data-ttu-id="ab861-136">Konfigurišite program Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ab861-136">Configure Project Service Automation</span></span>](../psa/configure.md)
