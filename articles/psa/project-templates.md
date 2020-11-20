---
title: Predlošci projekata
description: Ova tema pruža informacije o tome kako koristiti predloške projekta za brzo podešavanje projekta.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 4fd618e15524c5cef5b6da9b282f449e3dfb7973
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123048"
---
# <a name="project-templates"></a><span data-ttu-id="3e575-103">Predlošci projekata</span><span class="sxs-lookup"><span data-stu-id="3e575-103">Project templates</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="3e575-104">Predložak projekta je unapred definisan okvir koji vam pomaže da brzo i lako pokrenete projekat.</span><span class="sxs-lookup"><span data-stu-id="3e575-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="3e575-105">Možete da koristite unapred definisani predložak za kreiranje novog projekta jednim klikom.</span><span class="sxs-lookup"><span data-stu-id="3e575-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="3e575-106">Što se tiče projekata, morate definisati preduslove za predloške projekata.</span><span class="sxs-lookup"><span data-stu-id="3e575-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="3e575-107">Morate definisati kalendar projekta za svaki predložak projekta, a uloge i cenovnici moraju biti unapred definisani u organizaciji kako bi komponente predloška imale korisne podatke.</span><span class="sxs-lookup"><span data-stu-id="3e575-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="3e575-108">Predložak projekta sastoji se od tri komponente: raspored, procene projekta i članovi projektnog tima.</span><span class="sxs-lookup"><span data-stu-id="3e575-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="3e575-109">Raspored</span><span class="sxs-lookup"><span data-stu-id="3e575-109">Schedule</span></span>

<span data-ttu-id="3e575-110">Raspored u predlošku projekta ima isti skup elemenata kao i raspored u projektu.</span><span class="sxs-lookup"><span data-stu-id="3e575-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="3e575-111">Možete da kreirate hijerarhiju zadatka, povezujete uloge sa zadacima, definišete raspored atributa i podešavate zavisne elemente.</span><span class="sxs-lookup"><span data-stu-id="3e575-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="3e575-112">Raspored u predlošku projekta takođe podržava režime zadataka za svaki zadatak.</span><span class="sxs-lookup"><span data-stu-id="3e575-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="3e575-113">Stoga podržava i sistem za zakazivanje.</span><span class="sxs-lookup"><span data-stu-id="3e575-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="3e575-114">Morate povezati kalendar projekta sa projektom.</span><span class="sxs-lookup"><span data-stu-id="3e575-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="3e575-115">Kada kreirate radni raspored, nema razlike između predloška projekta i projekta.</span><span class="sxs-lookup"><span data-stu-id="3e575-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="3e575-116">Procene za projekat</span><span class="sxs-lookup"><span data-stu-id="3e575-116">Project estimates</span></span>

<span data-ttu-id="3e575-117">Procene projekta u obrascu projekta funkcionišu na isti način kao procene projekta u projektu.</span><span class="sxs-lookup"><span data-stu-id="3e575-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="3e575-118">Međutim, cene troškova i prodajne cene se preuzimaju iz podrazumevanih cenovnika troškova i prodajnih cenovnika koje su definisani u parametrima.</span><span class="sxs-lookup"><span data-stu-id="3e575-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="3e575-119">Kreiranje projekta iz predloška</span><span class="sxs-lookup"><span data-stu-id="3e575-119">Creating a project from a template</span></span>
 
<span data-ttu-id="3e575-120">Postoji nekoliko načina za kreiranje projekta iz predloška projekta:</span><span class="sxs-lookup"><span data-stu-id="3e575-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="3e575-121">Kada kreirate projekat iz ponude, možete odabrati predložak projekta u dijalogu za **brzo kreiranje projekta**.</span><span class="sxs-lookup"><span data-stu-id="3e575-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Dijalog za brzo kreiranje projekta](media/project-11.png)

- <span data-ttu-id="3e575-123">Kada kreirate projekat odabirom opcije **Novi projekat**, stranica **Projekat** se pojavljuje pre nego što se zapis sačuva.</span><span class="sxs-lookup"><span data-stu-id="3e575-123">When you create a project by selecting **New Project**, the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="3e575-124">U polju **Izbor predloška** izaberite jedan od unapred definisanih predložaka projekata u organizaciji.</span><span class="sxs-lookup"><span data-stu-id="3e575-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="3e575-125">Upotrebite **Kreiranje projekta iz predloška** na stranici **Entitet predloška**.</span><span class="sxs-lookup"><span data-stu-id="3e575-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="3e575-126">Kopiranje komponenti predloška u projekat</span><span class="sxs-lookup"><span data-stu-id="3e575-126">Copying components of template to project</span></span>

<span data-ttu-id="3e575-127">Kada kopirate komponente predloška projekta u projekat, može se dogoditi nekoliko zamena, zavisno od podešavanja u projektu.</span><span class="sxs-lookup"><span data-stu-id="3e575-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="3e575-128">Kopiranje rasporeda</span><span class="sxs-lookup"><span data-stu-id="3e575-128">Copying the schedule</span></span>

<span data-ttu-id="3e575-129">Kada kopirate raspored iz predloška projekta, ako projekat ima drugačiji kalendar projekta nego predložak, radno vreme iz kalendara projekta se primenjuje na raspored zadataka.</span><span class="sxs-lookup"><span data-stu-id="3e575-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="3e575-130">Na ovaj način se raspored prilagođava kako bi odgovarao kalendaru koji podržava projekat.</span><span class="sxs-lookup"><span data-stu-id="3e575-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="3e575-131">Slično, prvi zadatak u rasporedu počinje na datum početka projekta, a ostatak rasporeda hijerarhije se ažurira na osnovu trajanja i zavisnih elemenata navedenih u predlošku.</span><span class="sxs-lookup"><span data-stu-id="3e575-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="3e575-132">Kopiranje procena projekta</span><span class="sxs-lookup"><span data-stu-id="3e575-132">Copying project estimates</span></span> 

<span data-ttu-id="3e575-133">Kada kopirate više stavki procene projekata, cenovnici se ažuriraju.</span><span class="sxs-lookup"><span data-stu-id="3e575-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="3e575-134">U cenovniku troškova, ove ispravke su zasnovane na jedinici koja je vlasnik projekta.</span><span class="sxs-lookup"><span data-stu-id="3e575-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="3e575-135">U cenovniku prodaje zasnovane su na klijentu.</span><span class="sxs-lookup"><span data-stu-id="3e575-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="3e575-136">Kada su u pitanju projekti koji su povezani sa entitetom prodaje, troškovi po jedinici i prodajne cene se utvrđuju na osnovu ovih cenovnika.</span><span class="sxs-lookup"><span data-stu-id="3e575-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="3e575-137">Kopiranje projektnog tima</span><span class="sxs-lookup"><span data-stu-id="3e575-137">Copying a project team</span></span>

<span data-ttu-id="3e575-138">Kada kopirate projektni tim iz predloška projekta u projekat, kopiraju se generički resursi, zajedno sa veštinama i stručnošću definisanim u predlošku.</span><span class="sxs-lookup"><span data-stu-id="3e575-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="3e575-139">Dodele generičkih resursa takođe se održavaju kao u predlošku projekta.</span><span class="sxs-lookup"><span data-stu-id="3e575-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="3e575-140">Imenovani resursi nisu podržani u predlošcima projekata.</span><span class="sxs-lookup"><span data-stu-id="3e575-140">Named resources aren't supported in project templates.</span></span>
