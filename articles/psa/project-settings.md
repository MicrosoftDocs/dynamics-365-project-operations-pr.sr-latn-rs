---
title: Podešavanja projekta
description: Ova tema pruža informacije o podešavanjima upravljanja projektima.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: c9b8659f3b7ee81d2e21ef52743debd521fa9bb9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083743"
---
# <a name="project-settings"></a><span data-ttu-id="78bbf-103">Podešavanja projekta</span><span class="sxs-lookup"><span data-stu-id="78bbf-103">Project settings</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="78bbf-104">Za pristup funkcijama planiranja projekata koristite sledeća podešavanja.</span><span class="sxs-lookup"><span data-stu-id="78bbf-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="78bbf-105">Radni predložak</span><span class="sxs-lookup"><span data-stu-id="78bbf-105">Work template</span></span>

<span data-ttu-id="78bbf-106">Da biste kreirali raspored projekta, kreirajte predložak kalendara projekta koji definiše broj radnih sati po danu i sve prekide poslovnih aktivnosti.</span><span class="sxs-lookup"><span data-stu-id="78bbf-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="78bbf-107">Da biste kreirali predložak kalendara projekta, radni predložak povezujete sa poljem **Predložak kalendara** za projekat.</span><span class="sxs-lookup"><span data-stu-id="78bbf-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="78bbf-108">Sledite ove korake za kreiranje radnog predloška.</span><span class="sxs-lookup"><span data-stu-id="78bbf-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="78bbf-109">U aplikaciji PSA, u levom navigacionom oknu, kliknite na **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="78bbf-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="78bbf-110">Na stranici liste **Resursi** otvorite zapis korisnika, a zatim izaberite **Prikaži radno vreme**.</span><span class="sxs-lookup"><span data-stu-id="78bbf-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="78bbf-111">Obavezno dozvolite iskačuće prozore na stranici pregledača.</span><span class="sxs-lookup"><span data-stu-id="78bbf-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="78bbf-112">Ovo vam omogućava da vidite radno vreme podešeno za resurs.</span><span class="sxs-lookup"><span data-stu-id="78bbf-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="78bbf-113">Na kartici **Mesečni prikaz** kliknite na **Podešavanje**.</span><span class="sxs-lookup"><span data-stu-id="78bbf-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="78bbf-114">Pojaviće se lista sa tri opcije:</span><span class="sxs-lookup"><span data-stu-id="78bbf-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="78bbf-115">Novi sedmični raspored</span><span class="sxs-lookup"><span data-stu-id="78bbf-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="78bbf-116">Raspored posla za jedan dan</span><span class="sxs-lookup"><span data-stu-id="78bbf-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="78bbf-117">Slobodni dani</span><span class="sxs-lookup"><span data-stu-id="78bbf-117">Time Off</span></span>

> ![Podešavanje opcija](media/project-13.png)

4. <span data-ttu-id="78bbf-119">Izaberite **Novi sedmični raspored** , a zatim podesite opcije za ovaj raspored resursa.</span><span class="sxs-lookup"><span data-stu-id="78bbf-119">Select **New Weekly Schedule** , and then set the options for this resource schedule.</span></span> <span data-ttu-id="78bbf-120">Možete podesiti periodični sedmični raspored, parametre sata u danu, prekid poslovnih aktivnosti i još mnogo toga.</span><span class="sxs-lookup"><span data-stu-id="78bbf-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="78bbf-121">Podesite opseg datuma, izaberite **Sačuvaj** , a zatim kliknite na **Zatvori**.</span><span class="sxs-lookup"><span data-stu-id="78bbf-121">Set the date range, select **Save** , and then click **Close**.</span></span> 
6. <span data-ttu-id="78bbf-122">Vratite se na stranicu liste **Resursi** i odaberite resurs za koji ste odredili radno vreme.</span><span class="sxs-lookup"><span data-stu-id="78bbf-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="78bbf-123">Izaberite **Podesite kalendar kao** da podesite radni predložak.</span><span class="sxs-lookup"><span data-stu-id="78bbf-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="78bbf-124">U dijalog **Radni predložak** unesite ime radnog predloška, a zatim izaberite **Primeni**.</span><span class="sxs-lookup"><span data-stu-id="78bbf-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="78bbf-125">Sada možete povezati radni predložak sa predloškom kalendara projekta.</span><span class="sxs-lookup"><span data-stu-id="78bbf-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="78bbf-126">Uloge resursa</span><span class="sxs-lookup"><span data-stu-id="78bbf-126">Resource roles</span></span>

<span data-ttu-id="78bbf-127">Termin *uloga resursa* odnosi se na skup veština, kompetencija i certifikacije koje osoba mora imati da bi mogla da obavlja određeni skup zadataka u projektu.</span><span class="sxs-lookup"><span data-stu-id="78bbf-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="78bbf-128">PSA vam omogućava da odredite troškove i naplatite vreme resursa na osnovu uloge sa kojom je resurs povezan.</span><span class="sxs-lookup"><span data-stu-id="78bbf-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="78bbf-129">Svaka organizacija mora podesiti ove uloge koristeći levu navigaciju u meniju **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="78bbf-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="78bbf-130">Svaka organizacija mora podesiti ove uloge na stranici **Aktivne kategorije resursa**.</span><span class="sxs-lookup"><span data-stu-id="78bbf-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="78bbf-131">Da biste otvorili ovu stranicu, u levom navigacionom oknu izaberite **Uloge resursa**.</span><span class="sxs-lookup"><span data-stu-id="78bbf-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="78bbf-132">Cenovnici</span><span class="sxs-lookup"><span data-stu-id="78bbf-132">Price lists</span></span>

<span data-ttu-id="78bbf-133">Cenovnici vam omogućavaju da podesite cene koštanja i prodajne cene za uloge resursa, kategorije troškova, proizvode i druge elemente u organizaciji.</span><span class="sxs-lookup"><span data-stu-id="78bbf-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="78bbf-134">Da biste mogli da podesite finansijske procene za posao koji mora da se obavi za projekat, treba da kreirate odgovarajuću listu troškova i cenovnik prodaje.</span><span class="sxs-lookup"><span data-stu-id="78bbf-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="78bbf-135">U odeljku sa parametrima treba da podesite i podrazumevani cenovnik troškova i prodajni cenovnik koji se odnosi na sve projekte kreirane u organizaciji.</span><span class="sxs-lookup"><span data-stu-id="78bbf-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="78bbf-136">Na stranici **Aktivni parametri projekta** proverite da li ste podesili podrazumevani cenovnik troškova i prodajni cenovnik.</span><span class="sxs-lookup"><span data-stu-id="78bbf-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>
