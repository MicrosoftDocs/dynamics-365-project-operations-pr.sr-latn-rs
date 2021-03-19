---
title: Ugovori o projektu
description: Ova tema daje primere ugovora o projektu koje možete kreirati za različite vrste projekata i izvore finansiranja, kao i kako možete upravljati ugovorima i fakturisati klijentima projekata.
author: Yowelle
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b53eb6ff3f98e7efc3d6b997cd4d877025225936
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289566"
---
# <a name="project-contracts"></a><span data-ttu-id="58c85-103">Ugovori o projektu</span><span class="sxs-lookup"><span data-stu-id="58c85-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="58c85-104">Ovaj članak daje primere ugovora o projektu koje možete kreirati za različite vrste projekata i izvore finansiranja, kao i kako možete upravljati ugovorima i fakturisati klijentima projekata.</span><span class="sxs-lookup"><span data-stu-id="58c85-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="58c85-105">Tip projekta koji kreirate za ugovor o projektu određuje metodu koji se koristi za fakturisanje klijenata projekta.</span><span class="sxs-lookup"><span data-stu-id="58c85-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="58c85-106">Možete da promenite ugovor o projektu i s njim povezani projekat, ali ne možete da promenite tip projekta.</span><span class="sxs-lookup"><span data-stu-id="58c85-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="58c85-107">Korišćenjem ugovora o projektu možete istovremeno fakturisati jedan ili više projekata.</span><span class="sxs-lookup"><span data-stu-id="58c85-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="58c85-108">Ugovor o projektu takođe garantuje dosledne procedure fakturisanja za svaki podprojekat u strukturi projekta.</span><span class="sxs-lookup"><span data-stu-id="58c85-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="58c85-109">Svaki projekat koji će biti fakturisan mora biti povezan sa ugovorom o projektu.</span><span class="sxs-lookup"><span data-stu-id="58c85-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="58c85-110">Postavke za ugovor o projektu odnose se na sve projekte i potprojekte koji su povezani sa tim ugovorom o projektu.</span><span class="sxs-lookup"><span data-stu-id="58c85-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="58c85-111">U ugovoru o projektu može se navesti jedan ili više izvora finansiranja.</span><span class="sxs-lookup"><span data-stu-id="58c85-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="58c85-112">Prema tome, možete podeliti obračun između više donatora, postaviti ograničenja finansiranja tako da se izvorima finansiranja ne naplaćuje više od određenog iznosa i konfigurisati pravila finansiranja za naplatu troškova.</span><span class="sxs-lookup"><span data-stu-id="58c85-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="58c85-113">Finansiranje ugovora o projektu</span><span class="sxs-lookup"><span data-stu-id="58c85-113">Funding for project contracts</span></span>
<span data-ttu-id="58c85-114">Neki ugovori o projektu navode da više strana deli odgovornost za finansiranje troškova projekta.</span><span class="sxs-lookup"><span data-stu-id="58c85-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="58c85-115">U nastavku su navedeni neki primeri:</span><span class="sxs-lookup"><span data-stu-id="58c85-115">Here are some examples:</span></span>

-   <span data-ttu-id="58c85-116">Veliki klijent koji ima više odeljenja zahteva da se finansiranje projekta podeli po odsecima.</span><span class="sxs-lookup"><span data-stu-id="58c85-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="58c85-117">Vaša kompanija deli troškove velikog projekta sa spoljnom organizacijom.</span><span class="sxs-lookup"><span data-stu-id="58c85-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="58c85-118">Projekat puta sufinansiraju dve opštine.</span><span class="sxs-lookup"><span data-stu-id="58c85-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="58c85-119">Projekt mosta finansira se iz državnih grantova i privatne korporacije.</span><span class="sxs-lookup"><span data-stu-id="58c85-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="58c85-120">U usluzi Dynamics 365 Finance, možete da podelite naplatu za jednu transakciju ili ceo projekat između više klijenata, grantova ili organizacija.</span><span class="sxs-lookup"><span data-stu-id="58c85-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="58c85-121">U projektima koji imaju više donatora, sve strane koje doprinose finansiranju naprednog projekta finansiranja nazivaju se izvorima finansiranja.</span><span class="sxs-lookup"><span data-stu-id="58c85-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="58c85-122">Nakon što se klijent, organizacija ili grant definiše kao izvor finansiranja, može se dodeliti jednom ili više pravila finansiranja.</span><span class="sxs-lookup"><span data-stu-id="58c85-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="58c85-123">Pravila finansiranja sadrže kriterijume koji određuju način na koji se troškovi dodeljuju različitim izvorima finansiranja za projekat.</span><span class="sxs-lookup"><span data-stu-id="58c85-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="58c85-124">Budući da se zalihe stavki, poput onih koje se pojavljuju u zahtevima za kupovinu i porudžbenicama, ne mogu podeliti, iznos troškova ne može se podeliti između više izvora finansiranja u trenutku distribucije.</span><span class="sxs-lookup"><span data-stu-id="58c85-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="58c85-125">Stoga, vrednost izvora finansiranja ostaje 0 (nula) dok se problem sa inventarom ne proknjiži.</span><span class="sxs-lookup"><span data-stu-id="58c85-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="58c85-126">Kada se problem sa inventarom proknjiži, iznos troškova se raspoređuje prema pravilima raspodele računa za projekat.</span><span class="sxs-lookup"><span data-stu-id="58c85-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="58c85-127">Evo nekih koraka koje možete preduzeti da biste olakšali podelu naplate između više izvora finansiranja:</span><span class="sxs-lookup"><span data-stu-id="58c85-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="58c85-128">Navedite da sve transakcije koje se unose za projekat koriste istu valutu prodaje kao i ugovor o projektu.</span><span class="sxs-lookup"><span data-stu-id="58c85-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="58c85-129">Postavite ograničenja finansiranja, tako da izvor finansiranja ne fakturiše više od određenog iznosa za projekat.</span><span class="sxs-lookup"><span data-stu-id="58c85-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="58c85-130">Konfigurišite pravila finansiranja i ograničenja finansiranja za svakog radnika, stavku, kategoriju, grupu kategorija i vrstu transakcije (ili za sve vrste transakcija).</span><span class="sxs-lookup"><span data-stu-id="58c85-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="58c85-131">Izaberite neobavezne datume početka i završetka da biste definisali period kada važi svako pravilo finansiranja.</span><span class="sxs-lookup"><span data-stu-id="58c85-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="58c85-132">Navedite procenat za koji je odgovoran svaki izvor finansiranja.</span><span class="sxs-lookup"><span data-stu-id="58c85-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="58c85-133">Navedite koji je izvor finansiranja odgovoran za zaokruživanje razlika uzrokovanih proračunima dodele sredstava.</span><span class="sxs-lookup"><span data-stu-id="58c85-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="58c85-134">Postavite pravila koja određuju kako će se troškovi projekta fakturisati spoljnim klijentima, a naplaćivati internim organizacijama.</span><span class="sxs-lookup"><span data-stu-id="58c85-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="58c85-135">Evidentirajte transakcije na računu za finansiranje na čekanju dok ne bude moguće dobiti dodatna sredstva ili dok ne odlučite da snosite troškove interno.</span><span class="sxs-lookup"><span data-stu-id="58c85-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="58c85-136">Da bi se utvrdilo koju poresku grupu treba povezati sa transakcijom, u projektu se traži dodeljivanje poreske grupe.</span><span class="sxs-lookup"><span data-stu-id="58c85-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="58c85-137">Ako na nivou projekta nije izvršeno dodeljivanje poreske grupe, pretražuje se ugovor o projektu.</span><span class="sxs-lookup"><span data-stu-id="58c85-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="58c85-138">Primer: Više izvora finansiranja (jednostavno)</span><span class="sxs-lookup"><span data-stu-id="58c85-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="58c85-139">Sledeća tabela daje scenarije za upravljanje raspodelom sredstava između više izvora finansiranja.</span><span class="sxs-lookup"><span data-stu-id="58c85-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="58c85-140">Ovi scenariji zasnovani su na sledećim pretpostavkama:</span><span class="sxs-lookup"><span data-stu-id="58c85-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="58c85-141">Postavke prioriteta uzimaju se u obzir u raspodeli sredstava pre nego što se primene drugi kriterijumi pravila finansiranja.</span><span class="sxs-lookup"><span data-stu-id="58c85-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="58c85-142">Nije naveden nijedan datumski period koji bi definisao period od kada važi pravilo finansiranja.</span><span class="sxs-lookup"><span data-stu-id="58c85-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="58c85-143"><strong>Scenario</strong></span><span class="sxs-lookup"><span data-stu-id="58c85-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="58c85-144"><strong>Izvor finansiranja</strong></span><span class="sxs-lookup"><span data-stu-id="58c85-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="58c85-145"><strong>Procenat dodele</strong></span><span class="sxs-lookup"><span data-stu-id="58c85-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="58c85-146"><strong>Prioritet dodele</strong></span><span class="sxs-lookup"><span data-stu-id="58c85-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58c85-147">Želite da dodelite troškove jednom izvoru finansiranja dok se njegova sredstva ne iscrpe, dodelite troškove drugom izvoru finansiranja dok se njegova sredstva ne iscrpe i konačno dodelite preostale troškove trećem izvoru finansiranja.</span><span class="sxs-lookup"><span data-stu-id="58c85-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="58c85-148">Izvor　finansiranja　1</span><span class="sxs-lookup"><span data-stu-id="58c85-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="58c85-149">Izvor　finansiranja　2</span><span class="sxs-lookup"><span data-stu-id="58c85-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="58c85-150">Izvor　finansiranja　3</span><span class="sxs-lookup"><span data-stu-id="58c85-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="58c85-151">100%</span><span class="sxs-lookup"><span data-stu-id="58c85-151">100%</span></span></li>
<li><span data-ttu-id="58c85-152">100%</span><span class="sxs-lookup"><span data-stu-id="58c85-152">100%</span></span></li>
<li><span data-ttu-id="58c85-153">100%</span><span class="sxs-lookup"><span data-stu-id="58c85-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="58c85-154">1</span><span class="sxs-lookup"><span data-stu-id="58c85-154">1</span></span></li>
<li><span data-ttu-id="58c85-155">2</span><span class="sxs-lookup"><span data-stu-id="58c85-155">2</span></span></li>
<li><span data-ttu-id="58c85-156">3</span><span class="sxs-lookup"><span data-stu-id="58c85-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="58c85-157">Želite da dodelite 75 procenata troškova jednom izvoru finansiranja, a 25 procenata drugom izvoru finansiranja.</span><span class="sxs-lookup"><span data-stu-id="58c85-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="58c85-158">Kada se iscrpi bilo koji od tih izvora finansiranja, preostale troškove želite da platite iz trećeg izvora finansiranja.</span><span class="sxs-lookup"><span data-stu-id="58c85-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="58c85-159">Izvor　finansiranja　1</span><span class="sxs-lookup"><span data-stu-id="58c85-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="58c85-160">Izvor　finansiranja　2</span><span class="sxs-lookup"><span data-stu-id="58c85-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="58c85-161">Izvor　finansiranja　3</span><span class="sxs-lookup"><span data-stu-id="58c85-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="58c85-162">75%</span><span class="sxs-lookup"><span data-stu-id="58c85-162">75%</span></span></li>
<li><span data-ttu-id="58c85-163">25%</span><span class="sxs-lookup"><span data-stu-id="58c85-163">25%</span></span></li>
<li><span data-ttu-id="58c85-164">100%</span><span class="sxs-lookup"><span data-stu-id="58c85-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="58c85-165">1</span><span class="sxs-lookup"><span data-stu-id="58c85-165">1</span></span></li>
<li><span data-ttu-id="58c85-166">1</span><span class="sxs-lookup"><span data-stu-id="58c85-166">1</span></span></li>
<li><span data-ttu-id="58c85-167">2</span><span class="sxs-lookup"><span data-stu-id="58c85-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58c85-168">Želite da dodelite 75 procenata troškova jednom izvoru finansiranja, a 25 procenata drugom izvoru finansiranja.</span><span class="sxs-lookup"><span data-stu-id="58c85-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="58c85-169">Kada se iscrpi bilo koji od tih izvora finansiranja, preostale troškove želite da podelite između trećeg i četvrtog izvora finansiranja.</span><span class="sxs-lookup"><span data-stu-id="58c85-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="58c85-170">Izvor　finansiranja　1</span><span class="sxs-lookup"><span data-stu-id="58c85-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="58c85-171">Izvor　finansiranja　2</span><span class="sxs-lookup"><span data-stu-id="58c85-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="58c85-172">Izvor　finansiranja　3</span><span class="sxs-lookup"><span data-stu-id="58c85-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="58c85-173">Izvor　finansiranja　4</span><span class="sxs-lookup"><span data-stu-id="58c85-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="58c85-174">75%</span><span class="sxs-lookup"><span data-stu-id="58c85-174">75%</span></span></li>
<li><span data-ttu-id="58c85-175">25%</span><span class="sxs-lookup"><span data-stu-id="58c85-175">25%</span></span></li>
<li><span data-ttu-id="58c85-176">50%</span><span class="sxs-lookup"><span data-stu-id="58c85-176">50%</span></span></li>
<li><span data-ttu-id="58c85-177">50%</span><span class="sxs-lookup"><span data-stu-id="58c85-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="58c85-178">1</span><span class="sxs-lookup"><span data-stu-id="58c85-178">1</span></span></li>
<li><span data-ttu-id="58c85-179">1</span><span class="sxs-lookup"><span data-stu-id="58c85-179">1</span></span></li>
<li><span data-ttu-id="58c85-180">2</span><span class="sxs-lookup"><span data-stu-id="58c85-180">2</span></span></li>
<li><span data-ttu-id="58c85-181">2</span><span class="sxs-lookup"><span data-stu-id="58c85-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="58c85-182">Želite da dodelite prvih 25 procenata troškova jednom izvoru finansiranja, a ostatak drugom izvoru finansiranja.</span><span class="sxs-lookup"><span data-stu-id="58c85-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="58c85-183">Izvor　finansiranja　1</span><span class="sxs-lookup"><span data-stu-id="58c85-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="58c85-184">Izvor　finansiranja　2</span><span class="sxs-lookup"><span data-stu-id="58c85-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="58c85-185">25%</span><span class="sxs-lookup"><span data-stu-id="58c85-185">25%</span></span></li>
<li><span data-ttu-id="58c85-186">100%</span><span class="sxs-lookup"><span data-stu-id="58c85-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="58c85-187">1</span><span class="sxs-lookup"><span data-stu-id="58c85-187">1</span></span></li>
<li><span data-ttu-id="58c85-188">2</span><span class="sxs-lookup"><span data-stu-id="58c85-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="58c85-189">Primer: Više izvora finansiranja (složeno)</span><span class="sxs-lookup"><span data-stu-id="58c85-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="58c85-190">Imate tri izvora finansiranja koja želite da koristite po sledećem redosledu:</span><span class="sxs-lookup"><span data-stu-id="58c85-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="58c85-191">Koristite izvor finansiranja 2 i izvor 3 jednako dok se izvor 2 ne iscrpi.</span><span class="sxs-lookup"><span data-stu-id="58c85-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="58c85-192">Nastavljate da koristite izvor finansiranja 3 dok se ne iscrpi.</span><span class="sxs-lookup"><span data-stu-id="58c85-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="58c85-193">Koristite izvor finansiranja 1 nakon što se izvor 3 iscrpi.</span><span class="sxs-lookup"><span data-stu-id="58c85-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="58c85-194">Da biste postigli taj cilj, prvo morate da uradite sledeće:</span><span class="sxs-lookup"><span data-stu-id="58c85-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="58c85-195">Postavite ograničenja finansiranja za izvor finansiranja 2 i izvor finansiranja 3, za njihove odgovarajuće iznose.</span><span class="sxs-lookup"><span data-stu-id="58c85-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="58c85-196">Kreirajte sledeća pravila finansiranja:</span><span class="sxs-lookup"><span data-stu-id="58c85-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="58c85-197">Pravilo 1 (Prioritet 1): Dodeli 50 procenata transakcija izvoru finansiranja 2 i 50 procenta izvoru finansiranja 3.</span><span class="sxs-lookup"><span data-stu-id="58c85-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="58c85-198">Pravilo 2 (Prioritet 2): Dodeli 100% transakcija izvoru finansiranja 3.</span><span class="sxs-lookup"><span data-stu-id="58c85-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="58c85-199">Pravilo 3 (Prioritet 3): Dodeli 100% transakcija izvoru finansiranja 1.</span><span class="sxs-lookup"><span data-stu-id="58c85-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="58c85-200">Ovo podešavanje funkcioniše jer se proverava da li transakcije poštuju pravila i ograničenja kako bi se utvrdilo da li se neko od njih odnosi na transakciju.</span><span class="sxs-lookup"><span data-stu-id="58c85-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="58c85-201">Ako se na transakciju ne primenjuju posebna pravila ili ograničenja, primenjuje se pravilo Sve transakcije.</span><span class="sxs-lookup"><span data-stu-id="58c85-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="58c85-202">Pravilo Sve transakcije podudara se sa svim transakcijama.</span><span class="sxs-lookup"><span data-stu-id="58c85-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="58c85-203">Ako se pronađe pravilo koje se podudara sa transakcijom, prvo se primenjuje procenat koji je dodeljen u tom pravilu, ali tek nakon što se podudaranja provere prema bilo kojim ograničenjima koja su postavljena.</span><span class="sxs-lookup"><span data-stu-id="58c85-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="58c85-204">Ako je ograničenje ispunjeno, a sredstva izvora finansiranja su iscrpljena, pravilo finansiranja koje je povezano sa ograničenjem finansiranja se zanemaruje, a program proverava sledeće pravilo koje se primenjuje.</span><span class="sxs-lookup"><span data-stu-id="58c85-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="58c85-205">U nekim slučajevima, samo deo transakcije može biti dodeljen po pravilu.</span><span class="sxs-lookup"><span data-stu-id="58c85-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="58c85-206">To se može dogoditi jer se dostigne ograničenje kada se transakcija dodeli.</span><span class="sxs-lookup"><span data-stu-id="58c85-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="58c85-207">U ovom slučaju, samo se određeni iznos dodeljuje prema tom pravilu, poput 50 procenata za svaki izvor finansiranja.</span><span class="sxs-lookup"><span data-stu-id="58c85-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="58c85-208">To je slučaj u pravilu 1, koje je opisano ranije u ovom odeljku.</span><span class="sxs-lookup"><span data-stu-id="58c85-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="58c85-209">Ostatak se dodeljuje prema sledećem pravilu u nizu.</span><span class="sxs-lookup"><span data-stu-id="58c85-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="58c85-210">Sledeća tabela detaljnije ispituje ovaj scenario.</span><span class="sxs-lookup"><span data-stu-id="58c85-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="58c85-211"><strong>Fokus</strong></span><span class="sxs-lookup"><span data-stu-id="58c85-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="58c85-212"><strong>Detalji</strong></span><span class="sxs-lookup"><span data-stu-id="58c85-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58c85-213">Pravila finansiranja</span><span class="sxs-lookup"><span data-stu-id="58c85-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="58c85-214">Pravilo 1 (Prioritet 1): Sve transakcije.</span><span class="sxs-lookup"><span data-stu-id="58c85-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="58c85-215">Dodeli izvor finansiranja 2 sa 50% i izvor finansiranja 3 sa 50%.</span><span class="sxs-lookup"><span data-stu-id="58c85-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="58c85-216">Pravilo 2 (Prioritet 2): Sve transakcije.</span><span class="sxs-lookup"><span data-stu-id="58c85-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="58c85-217">Izdvoj izvor finansiranja 3 na 100%.</span><span class="sxs-lookup"><span data-stu-id="58c85-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="58c85-218">Pravilo 3 (Prioritet 2): Sve transakcije.</span><span class="sxs-lookup"><span data-stu-id="58c85-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="58c85-219">Izdvoj izvor finansiranja 1 na 100%.</span><span class="sxs-lookup"><span data-stu-id="58c85-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="58c85-220">Ograničenja finansiranja</span><span class="sxs-lookup"><span data-stu-id="58c85-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="58c85-221">Ograničenje izvora finansiranja 1 = 10.000,00</span><span class="sxs-lookup"><span data-stu-id="58c85-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="58c85-222">Ograničenje izvora finansiranja 2 = 500,00</span><span class="sxs-lookup"><span data-stu-id="58c85-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="58c85-223">Ograničenje izvora finansiranja 3 = 750,00</span><span class="sxs-lookup"><span data-stu-id="58c85-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58c85-224">Transakcija 1</span><span class="sxs-lookup"><span data-stu-id="58c85-224">Transaction 1</span></span></td>
<td><span data-ttu-id="58c85-225"><strong>Iznos transakcije:</strong> 100,00<strong>Finansiranje:</strong> Transakcija se plaća samo prema pravilu 1, jer se transakcija u potpunosti plaća nakon primene pravila 1.</span><span class="sxs-lookup"><span data-stu-id="58c85-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="58c85-226">Transakcija se finansira na jednak način između izvora finansiranja 2 i izvora finansiranja 3.</span><span class="sxs-lookup"><span data-stu-id="58c85-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="58c85-227">Izvor finansiranja 2: 50,00</span><span class="sxs-lookup"><span data-stu-id="58c85-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="58c85-228">Izvor finansiranja 3: 50,00</span><span class="sxs-lookup"><span data-stu-id="58c85-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="58c85-229">Transakcija 2</span><span class="sxs-lookup"><span data-stu-id="58c85-229">Transaction 2</span></span></td>
<td><span data-ttu-id="58c85-230"><strong>Iznos transakcije:</strong> 5.000,00<strong>Finansiranje:</strong> Transakcija se plaća prema sva tri pravila.</span><span class="sxs-lookup"><span data-stu-id="58c85-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="58c85-231"><strong>Pravilo 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="58c85-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="58c85-232">Izvor finansiranja 2: 450,00</span><span class="sxs-lookup"><span data-stu-id="58c85-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="58c85-233">Izvor finansiranja 3: 450,00</span><span class="sxs-lookup"><span data-stu-id="58c85-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="58c85-234">
<strong>Pravilo 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="58c85-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="58c85-235">Izvor finansiranja 3: 250,00 (= 750,00 – 50,00 – 450,00)</span><span class="sxs-lookup"><span data-stu-id="58c85-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="58c85-236">
<strong>Pravilo 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="58c85-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="58c85-237">Izvor finansiranja 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</span><span class="sxs-lookup"><span data-stu-id="58c85-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58c85-238">Ukupna sredstva koja se raspoređuju za svaki izvor finansiranja</span><span class="sxs-lookup"><span data-stu-id="58c85-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="58c85-239">Izvor finansiranja 1: 3.850,00</span><span class="sxs-lookup"><span data-stu-id="58c85-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="58c85-240">Izvor finansiranja 2: 500,00</span><span class="sxs-lookup"><span data-stu-id="58c85-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="58c85-241">Izvor finansiranja 3: 750,00</span><span class="sxs-lookup"><span data-stu-id="58c85-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="58c85-242">Pravila za naplate</span><span class="sxs-lookup"><span data-stu-id="58c85-242">Billing rules</span></span>
<span data-ttu-id="58c85-243">Kada pregovarate o ugovoru o projektu sa klijentom, vi definišete kako i kada možete fakturisati klijentu za rad na projektu.</span><span class="sxs-lookup"><span data-stu-id="58c85-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="58c85-244">Nakon što postavite ugovor o projektu i projekat, možete postaviti pravila naplate za projekat.</span><span class="sxs-lookup"><span data-stu-id="58c85-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="58c85-245">Pravila za naplate zasnivaju se na uslovima projekta koji su navedeni u ugovoru o projektu.</span><span class="sxs-lookup"><span data-stu-id="58c85-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="58c85-246">Pravila za naplatu koja možete kreirati zavise od uslova ugovora o projektu i vrste projekta, kao što su vreme i materijal ili fiksna cena, koje povezujete sa pravilom za naplatu.</span><span class="sxs-lookup"><span data-stu-id="58c85-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="58c85-247">Za ugovor o projektu možete kreirati više pravila za naplatu.</span><span class="sxs-lookup"><span data-stu-id="58c85-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="58c85-248">Pravilo naplate možete dodeliti i više za projekata koji su povezani sa istim ugovorom o projektu i imaju slične uslove naplate.</span><span class="sxs-lookup"><span data-stu-id="58c85-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="58c85-249">Možete da podesite sledeće vrste naplate:</span><span class="sxs-lookup"><span data-stu-id="58c85-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="58c85-250">**Jedinica isporuke** – Fakturišite klijentu kada završite jedinicu isporuke.</span><span class="sxs-lookup"><span data-stu-id="58c85-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="58c85-251">Jedinice isporuke definišete u ugovoru.</span><span class="sxs-lookup"><span data-stu-id="58c85-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="58c85-252">**Napredak** – Fakturišite klijentu kada završite određeni procenat projekta.</span><span class="sxs-lookup"><span data-stu-id="58c85-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="58c85-253">Možete da podesite pravilo naplate tako da automatski izračunava procenat obavljenog posla ili možete ručno da izračunate procenat završenog posla i iznos za fakturisanje klijentu.</span><span class="sxs-lookup"><span data-stu-id="58c85-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="58c85-254">**Kontrolna tačka** – Fakturišite klijentu puni iznos kontrolne tačke projekta kada ta kontrolna tačka bude dostignuta.</span><span class="sxs-lookup"><span data-stu-id="58c85-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="58c85-255">**Naknada** – Fakturišite klijentu za vaše usluge plus naknadu za upravljanje, koja je obično procenat troškova usluga.</span><span class="sxs-lookup"><span data-stu-id="58c85-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="58c85-256">**Vreme i materijal** – Fakturišite klijentu za vrednost vremena i materijala koji se koriste na projektu.</span><span class="sxs-lookup"><span data-stu-id="58c85-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="58c85-257">Za sve vrste pravila naplate, možete odrediti procenat zadržavanja koji se oduzima od faktura klijenta dok projekat ne dostigne neku dogovorenu fazu.</span><span class="sxs-lookup"><span data-stu-id="58c85-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="58c85-258">Procenat zadržavanja plaćanja se navodi u ugovoru o projektu.</span><span class="sxs-lookup"><span data-stu-id="58c85-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="58c85-259">Iznos se izračunava na osnovu i oduzima od ukupne vrednosti linija u fakturi klijenta.</span><span class="sxs-lookup"><span data-stu-id="58c85-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="58c85-260">Za pravila obračuna **Vreme i materijal** i **Napredak**, možete dodeliti naplative kategorije.</span><span class="sxs-lookup"><span data-stu-id="58c85-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="58c85-261">Naplative kategorije označavaju transakcije koje treba da budu uključene u fakture klijenata.</span><span class="sxs-lookup"><span data-stu-id="58c85-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="58c85-262">Kada budete spremni da fakturišete klijentu, iznos fakture za projekat se izračunava na osnovu pravila naplate i generiše se predlog fakture za projekat.</span><span class="sxs-lookup"><span data-stu-id="58c85-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="58c85-263">Sledeći odeljci pružaju primere koji pokazuju kako se postavljaju pravila naplate za projekat i njima upravlja.</span><span class="sxs-lookup"><span data-stu-id="58c85-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="58c85-264">Primer: Kreirajte pravilo naplate koje se zasniva na broju isporučenih jedinica</span><span class="sxs-lookup"><span data-stu-id="58c85-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="58c85-265">Vaša organizacija zaključuje ugovor o pružanju ukupno pet obuka zaposlenima po ceni od 10.000 po sesiji.</span><span class="sxs-lookup"><span data-stu-id="58c85-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="58c85-266">Klijentu fakturišete nakon svake sesije obuke.</span><span class="sxs-lookup"><span data-stu-id="58c85-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="58c85-267">Kada postavite pravila naplate za ugovor, koristite sledeće vrednosti:</span><span class="sxs-lookup"><span data-stu-id="58c85-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="58c85-268">Jedinica isporuke je jedna sesija obuke.</span><span class="sxs-lookup"><span data-stu-id="58c85-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="58c85-269">Jedinična cena je 10.000 po sesiji obuke.</span><span class="sxs-lookup"><span data-stu-id="58c85-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="58c85-270">Ukupan broj jedinica je pet sesija obuke.</span><span class="sxs-lookup"><span data-stu-id="58c85-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="58c85-271">Kada završite jednu sesiju obuke, možete da napravite fakturu za 10.000 za prvu isporučenu jedinicu i pošaljite fakturu klijentu.</span><span class="sxs-lookup"><span data-stu-id="58c85-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="58c85-272">Primer: Kreirajte pravilo naplate koje se zasniva na određenom procentu završetka projekta (ručni proračun)</span><span class="sxs-lookup"><span data-stu-id="58c85-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="58c85-273">Vaša organizacija, firma za softversko savetovanje, sklapa ugovor sa klijentom o razvoju dela proizvoda koji klijent razvija.</span><span class="sxs-lookup"><span data-stu-id="58c85-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="58c85-274">Vaša organizacija pristaje na isporuku softverskog koda u periodu od šest meseci.</span><span class="sxs-lookup"><span data-stu-id="58c85-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="58c85-275">Klijent se slaže da će vašoj organizaciji platiti ukupno 100.000 za rad.</span><span class="sxs-lookup"><span data-stu-id="58c85-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="58c85-276">Pravilo naplate kreirate da biste fakturisali klijentu na osnovu procenta posla koji je završen na projektu, kako je navedeno u ugovoru.</span><span class="sxs-lookup"><span data-stu-id="58c85-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="58c85-277">Na kraju prvog meseca, sastajete se sa klijentom da biste utvrdili procenat obavljenog posla.</span><span class="sxs-lookup"><span data-stu-id="58c85-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="58c85-278">Nakon što vi i klijent pregledate projekat, odlučujete da je projekat završen 15 posto.</span><span class="sxs-lookup"><span data-stu-id="58c85-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="58c85-279">Kreirate fakturu na 15.000 (15 procenta od 100.000) i šaljete je klijentu.</span><span class="sxs-lookup"><span data-stu-id="58c85-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="58c85-280">Primer: Kreirajte pravilo naplate koje se zasniva na određenom procentu završetka projekta (automatski proračun)</span><span class="sxs-lookup"><span data-stu-id="58c85-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="58c85-281">Vaša organizacija, firma za razvoj softvera, pristaje da razvije paket obračuna zarada za klijenta po ceni od 30.000.</span><span class="sxs-lookup"><span data-stu-id="58c85-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="58c85-282">Klijent se slaže da će vašoj organizaciji platiti na osnovu procenta završenog posla.</span><span class="sxs-lookup"><span data-stu-id="58c85-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="58c85-283">Procenjujete da troškovi projekta iznose 20.000.</span><span class="sxs-lookup"><span data-stu-id="58c85-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="58c85-284">Ugovor o projektu navodi kategorije posla koje koristite u postupku naplate.</span><span class="sxs-lookup"><span data-stu-id="58c85-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="58c85-285">Postavljate pravila naplate koja automatski izračunavaju iznose faktura za procenat završenog posla za svaku kategoriju.</span><span class="sxs-lookup"><span data-stu-id="58c85-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="58c85-286">Podesili ste budžet za svaku kategoriju:</span><span class="sxs-lookup"><span data-stu-id="58c85-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="58c85-287">**Razvoj** – Trošak od 15.000 i prihod od 20.000</span><span class="sxs-lookup"><span data-stu-id="58c85-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="58c85-288">**Instalacija** – Trošak od 5.000 i prihod od 10.000</span><span class="sxs-lookup"><span data-stu-id="58c85-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="58c85-289">Kada prvi put kreirate fakturu klijenta, iznos fakture se automatski izračunava na osnovu sledećih informacija:</span><span class="sxs-lookup"><span data-stu-id="58c85-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="58c85-290">Posle mesec dana, radnik na projektu podnosi vremenski raspored za projekat.</span><span class="sxs-lookup"><span data-stu-id="58c85-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="58c85-291">Troškovi radnih sati radnika su 5.000 za razvoj i 1.000 za instalaciju.</span><span class="sxs-lookup"><span data-stu-id="58c85-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="58c85-292">Razvojni radovi su završeni 33 procenta (5.000 stvarnih troškova / 15.000 troškova budžeta), a instalacioni radovi su završeni 20 procenata (1.000 stvarnih troškova / 5.000 troškova budžeta).</span><span class="sxs-lookup"><span data-stu-id="58c85-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="58c85-293">Iznos fakture od 8.667 se automatski izračunava (33 procenta od 20.000 + 20 procenata od 10.000).</span><span class="sxs-lookup"><span data-stu-id="58c85-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="58c85-294">Kreirate fakturu na 8.667 i šaljete je klijentu.</span><span class="sxs-lookup"><span data-stu-id="58c85-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="58c85-295">Primer: Kreirajte pravilo naplate koje se zasniva na dogovorenim kontrolnim tačkama</span><span class="sxs-lookup"><span data-stu-id="58c85-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="58c85-296">Vaša organizacija, konsultantska firma za menadžment, pristaje da sprovede istraživanje tržišta za potrošački proizvod koji klijent planira da proda.</span><span class="sxs-lookup"><span data-stu-id="58c85-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="58c85-297">Klijent se slaže da će koristiti vaše usluge u periodu od tri meseca, počev od marta, i slaže se da će vašoj organizaciji platiti 50.000.</span><span class="sxs-lookup"><span data-stu-id="58c85-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="58c85-298">Projekat ima tri kontrolne tačke:</span><span class="sxs-lookup"><span data-stu-id="58c85-298">The project has three milestones:</span></span>

-   <span data-ttu-id="58c85-299">Kontrolna tačka 1: Prikupljanje podataka o potrošačima – 31. mart</span><span class="sxs-lookup"><span data-stu-id="58c85-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="58c85-300">Kontrolna tačka 2: Analiza podataka potrošača – 30. april</span><span class="sxs-lookup"><span data-stu-id="58c85-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="58c85-301">Kontrolna tačka 3: Predstavljanje predloga održivosti proizvoda – 31. maj</span><span class="sxs-lookup"><span data-stu-id="58c85-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="58c85-302">Klijent se slaže da će vašoj organizaciji platiti 10.000 za prvu kontrolnu tačku, 20.000 za drugu kontrolnu tačku i 20.000 za treću kontrolnu tačku.</span><span class="sxs-lookup"><span data-stu-id="58c85-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="58c85-303">Kada postavite ugovor o projektu, slažete se da ćete klijentu naplatiti na osnovu kontrolne tačke koja je završena.</span><span class="sxs-lookup"><span data-stu-id="58c85-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="58c85-304">Postavljanje pravila naplate uključuje sledeće korake:</span><span class="sxs-lookup"><span data-stu-id="58c85-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="58c85-305">Definišite kontrolne tačke projekta.</span><span class="sxs-lookup"><span data-stu-id="58c85-305">Define the project milestones.</span></span>
-   <span data-ttu-id="58c85-306">Definišite iznos za fakturisanje klijentu kada se završi svaka kontrolna tačka.</span><span class="sxs-lookup"><span data-stu-id="58c85-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="58c85-307">Kada se prva kontrolna tačka završi 31. marta, označite je kao ispunjenu, a zatim napravite fakturu na iznos od 10.000 i pošaljite je klijentu.</span><span class="sxs-lookup"><span data-stu-id="58c85-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="58c85-308">Ne možete da kreirate fakturu za kontrolnu tačku dok je ne označite kao završenu.</span><span class="sxs-lookup"><span data-stu-id="58c85-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="58c85-309">Primer: Kreirajte pravilo naplate koje se zasniva na uslugama uz naknadu za upravljanje</span><span class="sxs-lookup"><span data-stu-id="58c85-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="58c85-310">Vaša organizacija, konsultantska firma za menadžment, pristaje da sprovede istraživanje tržišta kako bi procenila održivost proizvoda koji klijent, maloprodajna kompanija, upravo razvija.</span><span class="sxs-lookup"><span data-stu-id="58c85-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="58c85-311">Uslovi ugovora preciziraju da ćete pružati usluge svoja tri najbolja savetnika za menadžment, koji će sprovoditi istraživanje na osnovu vremena i materijala.</span><span class="sxs-lookup"><span data-stu-id="58c85-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="58c85-312">Klijent se slaže da plaća 100 na sat, plus 10 posto naknade za upravljanje za konsultantske sate koji se naplaćuju za projekat.</span><span class="sxs-lookup"><span data-stu-id="58c85-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="58c85-313">Kada postavite ugovor o projektu, kreirajte pravilo naplate da biste dodali naknadu od 10% za menadžment na savetodavne sate koji se naplaćuju projektu.</span><span class="sxs-lookup"><span data-stu-id="58c85-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="58c85-314">Kada kreirate fakturu za klijenta, njemu se naplaćuje 10% naknade za upravljanje uz troškove konsultantskih sati.</span><span class="sxs-lookup"><span data-stu-id="58c85-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="58c85-315">Na primer, ako su tri konsultanta radila ukupno 200 sati na projektu, faktura na iznos od 22.000 kreira se na osnovu sledećeg proračuna:</span><span class="sxs-lookup"><span data-stu-id="58c85-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="58c85-316">200 sati po 100 na sat = 20.000</span><span class="sxs-lookup"><span data-stu-id="58c85-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="58c85-317">Naknada za menadžment od 10% = 2.000</span><span class="sxs-lookup"><span data-stu-id="58c85-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="58c85-318">Ukupan iznos fakture = 22.000</span><span class="sxs-lookup"><span data-stu-id="58c85-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="58c85-319">Ako su naknade klijentu oporezive, a u ugovoru o projektu odaberete grupu za porez na promet, grupa poreza na promet automatski se unosi u pravilo naplate naknada.</span><span class="sxs-lookup"><span data-stu-id="58c85-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="58c85-320">Primer: Kreirajte pravilo naplate vrednosti vremena i materijala</span><span class="sxs-lookup"><span data-stu-id="58c85-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="58c85-321">Vaša organizacija, firma za softversko savetovanje, pristaje da obezbedi pet tehničkih konsultanata koji će raditi na projektu razvoja softvera za klijenta u narednih šest meseci.</span><span class="sxs-lookup"><span data-stu-id="58c85-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="58c85-322">Klijent se slaže da plati 150 za svaki sat konsultovanja, uz troškove kancelarijskog materijala.</span><span class="sxs-lookup"><span data-stu-id="58c85-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="58c85-323">Vaša organizacija šalje fakturu klijentu na kraju svakog meseca.</span><span class="sxs-lookup"><span data-stu-id="58c85-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="58c85-324">Kada postavljate ugovor o projektu, saglasni ste da klijentu svakog meseca obračunavate vreme i materijale na projektu.</span><span class="sxs-lookup"><span data-stu-id="58c85-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="58c85-325">Kreirate pravilo naplate koje uključuje sledeće informacije:</span><span class="sxs-lookup"><span data-stu-id="58c85-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="58c85-326">Period ugovora je šest meseci.</span><span class="sxs-lookup"><span data-stu-id="58c85-326">The contract period is six months.</span></span>
-   <span data-ttu-id="58c85-327">Vreme konsultacija izračunava se po ceni od 150 na sat.</span><span class="sxs-lookup"><span data-stu-id="58c85-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="58c85-328">Kancelarijski materijal se fakturiše po ceni koštanja, a ukupni troškovi projekta ne smeju preći 10.000.</span><span class="sxs-lookup"><span data-stu-id="58c85-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="58c85-329">Fakturu za klijenta kreirate na kraju svakog kalendarskog meseca tokom trajanja projekta.</span><span class="sxs-lookup"><span data-stu-id="58c85-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="58c85-330">Tokom prvog meseca, konsultanti na projektu beleže ukupno 800 sati.</span><span class="sxs-lookup"><span data-stu-id="58c85-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="58c85-331">Troškovi kancelarijskog materijala koji se naplaćuju za projekat su 2.000.</span><span class="sxs-lookup"><span data-stu-id="58c85-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="58c85-332">Stoga na kraju meseca kreirate fakturu na iznos od 122.000, što je izračunato kao 800 sati po 150 na sat, plus 2.000 za kancelarijski materijal.</span><span class="sxs-lookup"><span data-stu-id="58c85-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>





[!INCLUDE[footer-include](../includes/footer-banner.md)]