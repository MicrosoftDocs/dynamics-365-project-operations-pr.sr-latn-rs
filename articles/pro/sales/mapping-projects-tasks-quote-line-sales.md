---
title: Mapiranje projekata i zadataka na stavku ponude zasnovane na projektu
description: Ova tema pruža informacije o tome kako da mapirate projekte i zadatke u predmet zadatka zasnovanog na projektu.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d726ab09da0e502da99191f7e7469c47f79b6e7c
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083472"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="017cd-103">Mapiranje projekata i zadataka na stavku ponude zasnovane na projektu</span><span class="sxs-lookup"><span data-stu-id="017cd-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="017cd-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="017cd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="017cd-105">U stavkama ponude zasnovane na projektu možete mapirati određene zadatke projekta koji je već povezan sa stavkom ponude.</span><span class="sxs-lookup"><span data-stu-id="017cd-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="017cd-106">Kada mapirate zadatke u stavku ponude, sledeće stavke koje ste definisali u stavci ponude primenjivaće se samo na te zadatke:</span><span class="sxs-lookup"><span data-stu-id="017cd-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="017cd-107">Način naplate</span><span class="sxs-lookup"><span data-stu-id="017cd-107">Billing method</span></span>
- <span data-ttu-id="017cd-108">Opcije naplativosti</span><span class="sxs-lookup"><span data-stu-id="017cd-108">Chargeability options</span></span>
- <span data-ttu-id="017cd-109">Ograničenja koja ne smeju da se prekorače</span><span class="sxs-lookup"><span data-stu-id="017cd-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="017cd-110">Klijenti</span><span class="sxs-lookup"><span data-stu-id="017cd-110">Customers</span></span>

<span data-ttu-id="017cd-111">Na primer, možda imate projekat gde je jedna faza fiksna cena, a sve ostale faze su vreme i materijali.</span><span class="sxs-lookup"><span data-stu-id="017cd-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="017cd-112">U tom slučaju, prvu fazu i sve njene podređene zadatke možete povezati sa stavkom ponude za tu fazu metodom obračuna sa fiksnom cenom.</span><span class="sxs-lookup"><span data-stu-id="017cd-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="017cd-113">Zatim možete povezati sve ostale faze sa stavkom ponude zasnovanom na vremenu i materijalima.</span><span class="sxs-lookup"><span data-stu-id="017cd-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="017cd-114">Povezivanje zadataka sa stavkama ponude zasnovanim na projektu</span><span class="sxs-lookup"><span data-stu-id="017cd-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="017cd-115">Zadatke možete povezati sa stavkama ponude sa sledećih lokacija:</span><span class="sxs-lookup"><span data-stu-id="017cd-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="017cd-116">Stranica **Projekat** > kartica **Obračun zadataka** (optimalno)</span><span class="sxs-lookup"><span data-stu-id="017cd-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="017cd-117">Stranica **Stavka ponude** > kartica **Zadaci koji se naplaćuju**</span><span class="sxs-lookup"><span data-stu-id="017cd-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="017cd-118">Sa stranice Projekat</span><span class="sxs-lookup"><span data-stu-id="017cd-118">From the Project page</span></span>

<span data-ttu-id="017cd-119">Stranica **Projekat** pruža optimalno iskustvo za povezivanje zadataka sa stavkama ponude.</span><span class="sxs-lookup"><span data-stu-id="017cd-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="017cd-120">Ovu stranicu možete koristiti za izbor više zadataka i povezivanje svih njih, kao i njihovih podređenih zadataka, u izabranu stavku ponude.</span><span class="sxs-lookup"><span data-stu-id="017cd-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="017cd-121">Na kartici **Opšti podaci** stavke ponude zasnovane na projektu, proverite da li je polje **Projekat** popunjeno.</span><span class="sxs-lookup"><span data-stu-id="017cd-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="017cd-122">U polju **Uključeni zadaci** izaberite **Samo izabrani zadaci**.</span><span class="sxs-lookup"><span data-stu-id="017cd-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="017cd-123">Sačuvajte stavku ponude zasnovanu na projektu.</span><span class="sxs-lookup"><span data-stu-id="017cd-123">Save the project-based quote line.</span></span> <span data-ttu-id="017cd-124">Kada se obrazac osveži, prikazaće se kartica **Zadaci koji se naplaćuju**.</span><span class="sxs-lookup"><span data-stu-id="017cd-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="017cd-125">Na kartici **Opšti podaci** izaberite vezu za polje **Projekat**.</span><span class="sxs-lookup"><span data-stu-id="017cd-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="017cd-126">Na stranici **Projekat** izaberite karticu **Obračun zadataka**.</span><span class="sxs-lookup"><span data-stu-id="017cd-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="017cd-127">U drugoj mreži, koja se odnosi na podešavanje obračuna za određeni zadatak, izaberite jedan ili više zadataka, a zatim izaberite **Povezivanje stavki ponude**.</span><span class="sxs-lookup"><span data-stu-id="017cd-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="017cd-128">Na stranici dijaloga koja se pojavi, izaberite stavku ponude koja prikazuje stavke ponude zasnovane na projektu u ponudi.</span><span class="sxs-lookup"><span data-stu-id="017cd-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="017cd-129">U polju **Tip obračuna** , naznačite da li su ovi zadaci naplativi ili nenaplativi.</span><span class="sxs-lookup"><span data-stu-id="017cd-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="017cd-130">Označite polje za potvrdu da biste naznačili da li povezivanje treba da sadrži podređene zadatke izabranih zadataka.</span><span class="sxs-lookup"><span data-stu-id="017cd-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="017cd-131">Ako označite to polje, povezaćete podređene zadatke izabranih zadataka sa stavkom ponude.</span><span class="sxs-lookup"><span data-stu-id="017cd-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="017cd-132">Izaberite **U redu** da biste zatvorili dijalog.</span><span class="sxs-lookup"><span data-stu-id="017cd-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="017cd-133">Sa stranice Stavka ponude</span><span class="sxs-lookup"><span data-stu-id="017cd-133">From the Quote line page</span></span>

<span data-ttu-id="017cd-134">Projektne zadatke možete povezati sa stavkama ponude sa kartice **Zadaci koji se naplaćuju** na stranici **Ponuda**.</span><span class="sxs-lookup"><span data-stu-id="017cd-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="017cd-135">Optimalno mesto za povezivanje projektnih zadataka sa stavkama ponude je na kartici **Obračun zadataka** na stranici **Projekat**.</span><span class="sxs-lookup"><span data-stu-id="017cd-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="017cd-136">Ako povežete zadatke sa kartice **Zadaci koji se naplaćuju** na stranici **Stavka ponude** , svaki projekat morate ručno povezati.</span><span class="sxs-lookup"><span data-stu-id="017cd-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="017cd-137">Na kartici **Opšti podaci** stavke ponude zasnovane na projektu, proverite da li je izabran projekat u polju **Projekat**.</span><span class="sxs-lookup"><span data-stu-id="017cd-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="017cd-138">U polju **Uključeni zadaci** izaberite **Samo izabrani zadaci**.</span><span class="sxs-lookup"><span data-stu-id="017cd-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="017cd-139">Sačuvajte stavku ponude zasnovanu na projektu.</span><span class="sxs-lookup"><span data-stu-id="017cd-139">Save the project-based quote line.</span></span> <span data-ttu-id="017cd-140">Kada se obrazac osveži, prikazaće se kartica **Zadaci koji se naplaćuju**.</span><span class="sxs-lookup"><span data-stu-id="017cd-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="017cd-141">Na kartici **Zadaci koji se naplaćuju** , izaberite **Dodaj zadatak stavke ponude**.</span><span class="sxs-lookup"><span data-stu-id="017cd-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="017cd-142">Na stranici **Zadatak stavke ponude** , u polju **Zadaci** izaberite zadatak i u polju **Tip obračuna** izaberite **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="017cd-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="017cd-143">Zatvorite stranicu.</span><span class="sxs-lookup"><span data-stu-id="017cd-143">Close the page.</span></span> <span data-ttu-id="017cd-144">Izabrani zadatak je sada povezan sa stavkom ponude.</span><span class="sxs-lookup"><span data-stu-id="017cd-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="017cd-145">Prekidanje veze zadataka sa stavkama ponude zasnovanim na projektu</span><span class="sxs-lookup"><span data-stu-id="017cd-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="017cd-146">Sa stranice Projekat</span><span class="sxs-lookup"><span data-stu-id="017cd-146">From the Project page</span></span>

<span data-ttu-id="017cd-147">Ovaj metod pruža optimalno iskustvo za prekidanje veze zadataka sa stavkama ponude.</span><span class="sxs-lookup"><span data-stu-id="017cd-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="017cd-148">Možete izabrati više zadataka i prekinuti vezu svih njih, kao i njihovih podređenih zadataka, sa izabranom stavkom ponude.</span><span class="sxs-lookup"><span data-stu-id="017cd-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="017cd-149">Na kartici **Opšti podaci** stavke ponude zasnovane na projektu, u polju **Projekat** izaberite vezu ka projektu.</span><span class="sxs-lookup"><span data-stu-id="017cd-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="017cd-150">Na stranici **Projekat** izaberite karticu **Obračun zadataka**.</span><span class="sxs-lookup"><span data-stu-id="017cd-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="017cd-151">U drugoj mreži, koja se odnosi na podešavanje obračuna za određeni zadatak, izaberite jedan ili više zadataka, a zatim izaberite **Prekidanje veze sa stavkama ponude**.</span><span class="sxs-lookup"><span data-stu-id="017cd-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="017cd-152">Na stranici dijaloga koja se pojavi, izaberite stavku ponude.</span><span class="sxs-lookup"><span data-stu-id="017cd-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="017cd-153">Označite polje za potvrdu da biste naznačili da li povezivanje treba takođe da se ukloni iz podređenih zadataka izabranih zadataka.</span><span class="sxs-lookup"><span data-stu-id="017cd-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="017cd-154">Ako označite to polje, prekinućete vezu podređenih zadataka izabranih zadataka sa stavkom ponude.</span><span class="sxs-lookup"><span data-stu-id="017cd-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="017cd-155">Izaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="017cd-155">Select **OK**.</span></span> <span data-ttu-id="017cd-156">Poruka upozorenja vas obaveštava da ako uklonite ovo povezivanje, sve stvarne vrednosti prethodno evidentirane u zadatku mogu da se opozovu.</span><span class="sxs-lookup"><span data-stu-id="017cd-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="017cd-157">Izaberite **U redu** da bi se nastavilo i uklanjalo povezivanje između zadatka i stavke ponude zasnovane na projektu.</span><span class="sxs-lookup"><span data-stu-id="017cd-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="017cd-158">Sa stranice Stavka ponude</span><span class="sxs-lookup"><span data-stu-id="017cd-158">From the Quote line page</span></span>

<span data-ttu-id="017cd-159">Vezu projektnih zadataka sa stavkama ponude takođe možete prekinuti sa kartice **Zadaci koji se naplaćuju** na stranici **Ponuda**.</span><span class="sxs-lookup"><span data-stu-id="017cd-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="017cd-160">Na kartici **Zadaci koji se naplaćuju** , izaberite **Izbriši zadatak stavke ponude**.</span><span class="sxs-lookup"><span data-stu-id="017cd-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="017cd-161">Izaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="017cd-161">Select **OK**.</span></span> <span data-ttu-id="017cd-162">Poruka upozorenja vas obaveštava da ako uklonite ovo povezivanje, sve stvarne vrednosti prethodno evidentirane u zadatku mogu da se opozovu.</span><span class="sxs-lookup"><span data-stu-id="017cd-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="017cd-163">Izaberite **U redu** da bi se nastavilo i uklanjalo povezivanje između zadatka i stavke ponude zasnovane na projektu.</span><span class="sxs-lookup"><span data-stu-id="017cd-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="017cd-164">Ovaj postupak ne briše zadatak iz projekta.</span><span class="sxs-lookup"><span data-stu-id="017cd-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="017cd-165">Samo uklanja povezivanje zadatka sa stavke ponude zasnovane na projektu.</span><span class="sxs-lookup"><span data-stu-id="017cd-165">It only removes the task association from the project-based quote line.</span></span>
