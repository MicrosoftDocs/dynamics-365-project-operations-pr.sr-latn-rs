---
title: Konfigurisanje naplativih komponenti za predmet ugovora zasnovan na projektu
description: Ova tema pruža informacije o tome kako dodati naplative komponente u predmete ugovora u usluzi Project Operations.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b29c912828aa4af2d2d9cb47869012087cb834b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003738"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="014cb-103">Konfigurisanje naplativih komponenti za predmet ugovora zasnovan na projektu</span><span class="sxs-lookup"><span data-stu-id="014cb-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="014cb-104">_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture, Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="014cb-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="014cb-105">Predmet ugovora zasnovan na projektu ima *uključene* komponente i *naplative* komponente.</span><span class="sxs-lookup"><span data-stu-id="014cb-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="014cb-106">Uključene komponente su komponente koje podležu:</span><span class="sxs-lookup"><span data-stu-id="014cb-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="014cb-107">Načinu naplate i podelama klijenata</span><span class="sxs-lookup"><span data-stu-id="014cb-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="014cb-108">Ograničenja koja ne smeju da se prekorače</span><span class="sxs-lookup"><span data-stu-id="014cb-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="014cb-109">Postavke učestalosti fakture definisane u predmetu ugovora zasnovanog na projektu</span><span class="sxs-lookup"><span data-stu-id="014cb-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="014cb-110">Podskup uključenih komponenti može se označiti kao naplativ pomoću polja **Tip obračuna**.</span><span class="sxs-lookup"><span data-stu-id="014cb-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="014cb-111">Polje **Tip obračuna** je skup opcija koji omogućava sledeće vrednosti u kontekstu predmeta ugovora:</span><span class="sxs-lookup"><span data-stu-id="014cb-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="014cb-112">Naplativo</span><span class="sxs-lookup"><span data-stu-id="014cb-112">Chargeable</span></span>
  - <span data-ttu-id="014cb-113">Nenaplativo</span><span class="sxs-lookup"><span data-stu-id="014cb-113">Non-chargeable</span></span>

<span data-ttu-id="014cb-114">Komponente koje se naplaćuju mogu se definisati na zadacima, ulogama i kategorijama transakcija.</span><span class="sxs-lookup"><span data-stu-id="014cb-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="014cb-115">Naplativost je definisana na zadacima za predmet ugovora o projektu i odnosi se na sve klase transakcija uključene u liniju.</span><span class="sxs-lookup"><span data-stu-id="014cb-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="014cb-116">Ako je polje **Uključi zadatke** na predmetu ugovora prazno ili postavljeno na **Čitav projekat**, kartica **Zadaci koji se naplaćuju** neće biti dostupna.</span><span class="sxs-lookup"><span data-stu-id="014cb-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="014cb-117">Naplativost definisana u ulogama za predmet ugovora o projektu odnosi se samo na klasu transakcija **Vreme**.</span><span class="sxs-lookup"><span data-stu-id="014cb-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="014cb-118">Ako je polje **Uključi vreme** na predmetu ugovora postavljeno na **Ne**, kartica **Uloge koje se naplaćuju** neće biti dostupna.</span><span class="sxs-lookup"><span data-stu-id="014cb-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="014cb-119">Naplativost definisana u kategorijama transakcija za predmet ugovora o projektu odnosi se samo na klasu transakcija **Trošak**.</span><span class="sxs-lookup"><span data-stu-id="014cb-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="014cb-120">Ako je polje **Uključi troškove** postavljeno na **Ne**, kartica **Kategorije koje se naplaćuju** neće biti dostupna.</span><span class="sxs-lookup"><span data-stu-id="014cb-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="014cb-121">Ažurirajte projektni zadatak kao naplativi ili nenaplativi</span><span class="sxs-lookup"><span data-stu-id="014cb-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="014cb-122">Projektni zadatak može biti naplativ ili nenaplativ na određenom predmetu ugovora, što omogućava sledeće podešavanje:</span><span class="sxs-lookup"><span data-stu-id="014cb-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="014cb-123">Ako predmet ugovora zasnovan na projektu uključuje **Vreme** i određeni zadatak, **T1** je povezan sa njim kao naplativ.</span><span class="sxs-lookup"><span data-stu-id="014cb-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="014cb-124">Ako postoji drugi predmet ugovora koji uključuje **Trošak**, zadatak T1 na predmetu ugovora liniji možete povezati kao nenaplativ.</span><span class="sxs-lookup"><span data-stu-id="014cb-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="014cb-125">Rezultat je da je sve vreme evidentirano u zadatku naplativo, a svi troškovi nenaplativi.</span><span class="sxs-lookup"><span data-stu-id="014cb-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="014cb-126">Tip naplate zadatka može se konfigurisati na kartici **Zadaci koji se naplaćuju** predmeta ugovora ažuriranjem polja **Tip naplate** na podformi zadataka predmeta ugovora.</span><span class="sxs-lookup"><span data-stu-id="014cb-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="014cb-127">Pored toga, možete da ažurirate polje **Tip naplate** na podformi zadatka Postavljanje obračuna projekta koje prikazuje predmete ugovora povezane sa zadatkom.</span><span class="sxs-lookup"><span data-stu-id="014cb-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="014cb-128">Ažurirajte ulogu kao naplativu ili nenaplativu</span><span class="sxs-lookup"><span data-stu-id="014cb-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="014cb-129">Uloga može biti naplativa ili nenaplativa na određenom predmetu ugovora.</span><span class="sxs-lookup"><span data-stu-id="014cb-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="014cb-130">Tip obračuna uloge može se konfigurisati na kartici **Uloge koje se naplaćuju** predmeta ugovora.</span><span class="sxs-lookup"><span data-stu-id="014cb-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="014cb-131">Da biste to uradili, ažurirajte polje **Tip naplate** na podformi **Naplative uloge**.</span><span class="sxs-lookup"><span data-stu-id="014cb-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="014cb-132">Ažurirajte kategoriju transakcija kao naplativu ili nenaplativu</span><span class="sxs-lookup"><span data-stu-id="014cb-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="014cb-133">Kategorija transakcija može biti naplativa ili nenaplativa na određenom predmetu ugovora.</span><span class="sxs-lookup"><span data-stu-id="014cb-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="014cb-134">Tip obračuna transakcije može se konfigurisati na kartici **Kategorije koje se naplaćuju** predmeta ugovora zasnovanom na projektu.</span><span class="sxs-lookup"><span data-stu-id="014cb-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="014cb-135">Da biste to uradili, ažurirajte polje **Tip naplate** na podformi **Naplative kategorije**.</span><span class="sxs-lookup"><span data-stu-id="014cb-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="014cb-136">Rešite naplativost</span><span class="sxs-lookup"><span data-stu-id="014cb-136">Resolve chargeability</span></span>

<span data-ttu-id="014cb-137">Procena ili stvarna vrednost kreirana za vreme smatra se naplativom samo ako važi sledeće:</span><span class="sxs-lookup"><span data-stu-id="014cb-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="014cb-138">**Vreme** je uključeno u predmet ugovora.</span><span class="sxs-lookup"><span data-stu-id="014cb-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="014cb-139">**Uloga** je konfigurisana kao naplativa u predmetu ugovora.</span><span class="sxs-lookup"><span data-stu-id="014cb-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="014cb-140">**Obuhvaćeni zadaci** su podešeni na vrednost **Izabrani zadaci** u predmetu ugovora.</span><span class="sxs-lookup"><span data-stu-id="014cb-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="014cb-141">Ako su ove tri stvari tačne, zadatak se konfiguriše kao naplativ.</span><span class="sxs-lookup"><span data-stu-id="014cb-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="014cb-142">Procena ili stvarna vrednost za trošak smatra se naplativom samo ako važi sledeće:</span><span class="sxs-lookup"><span data-stu-id="014cb-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="014cb-143">**Trošak** je uključen u predmet ugovora</span><span class="sxs-lookup"><span data-stu-id="014cb-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="014cb-144">**Kategorija transakcije** je konfigurisana kao naplativa u predmetu ugovora</span><span class="sxs-lookup"><span data-stu-id="014cb-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="014cb-145">**Obuhvaćeni zadaci** su podešeni na vrednost **Izabrani zadatak** u predmetu ugovora</span><span class="sxs-lookup"><span data-stu-id="014cb-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="014cb-146">Ako su ove tri stvari tačne, **Zadatak** se konfiguriše kao naplativ.</span><span class="sxs-lookup"><span data-stu-id="014cb-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="014cb-147">Procena ili stvarna vrednost za materijal smatra se naplativom samo ako važi sledeće:</span><span class="sxs-lookup"><span data-stu-id="014cb-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="014cb-148">**Materijali** su uključeni u predmet ugovora</span><span class="sxs-lookup"><span data-stu-id="014cb-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="014cb-149">**Obuhvaćeni zadaci** su podešeni na vrednost **Izabrani zadaci** u predmetu ugovora</span><span class="sxs-lookup"><span data-stu-id="014cb-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="014cb-150">Ako su ove dve stvari tačne, **Zadatak** se konfiguriše kao naplativ.</span><span class="sxs-lookup"><span data-stu-id="014cb-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="014cb-151">
                    <strong>Sadrži vreme</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="014cb-152">
                    <strong>Sadrži trošak</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="014cb-153">
                    <strong>Sadrži materijale</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="014cb-154">
                    <strong>Obuhvaćeni zadaci</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="014cb-155">
                    <strong>Uloga</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="014cb-156">
                    <strong>Kategorija</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="014cb-157">
                    <strong>Zadatak</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="014cb-158">
                    <strong>Uticaj naplativosti</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="014cb-159">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="014cb-160">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="014cb-161">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="014cb-162">Čitav projekat</span><span class="sxs-lookup"><span data-stu-id="014cb-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="014cb-163">Naplativo</span><span class="sxs-lookup"><span data-stu-id="014cb-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="014cb-164">Naplativo</span><span class="sxs-lookup"><span data-stu-id="014cb-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="014cb-165">Nije moguće podesiti</span><span class="sxs-lookup"><span data-stu-id="014cb-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="014cb-166">Obračun u stvarnom vremenu: <strong>Naplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="014cb-167">Tip obračuna na stvarnom trošku: <strong>Naplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="014cb-168">Tip obračuna na stvarnom materijalu: <strong>Naplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="014cb-169">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="014cb-170">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="014cb-171">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="014cb-172">Samo izabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="014cb-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="014cb-173">Naplativo</span><span class="sxs-lookup"><span data-stu-id="014cb-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="014cb-174">Naplativo</span><span class="sxs-lookup"><span data-stu-id="014cb-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="014cb-175">Naplativo</span><span class="sxs-lookup"><span data-stu-id="014cb-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="014cb-176">Obračun u stvarnom vremenu: <strong>Naplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="014cb-177">Tip obračuna na stvarnom trošku: <strong>Naplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="014cb-178">Tip obračuna na stvarnom materijalu: <strong>Naplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="014cb-179">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="014cb-180">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="014cb-181">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="014cb-182">Samo izabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="014cb-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="014cb-183">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="014cb-184">Naplativo</span><span class="sxs-lookup"><span data-stu-id="014cb-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="014cb-185">Naplativo</span><span class="sxs-lookup"><span data-stu-id="014cb-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="014cb-186">Obračun u stvarnom vremenu: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="014cb-187">Tip obračuna na stvarnom trošku: Naplativo</span><span class="sxs-lookup"><span data-stu-id="014cb-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="014cb-188">Tip obračuna na stvarnom materijalu: Naplativo</span><span class="sxs-lookup"><span data-stu-id="014cb-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="014cb-189">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="014cb-190">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="014cb-191">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="014cb-192">Samo izabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="014cb-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="014cb-193">Naplativo</span><span class="sxs-lookup"><span data-stu-id="014cb-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="014cb-194">Naplativo</span><span class="sxs-lookup"><span data-stu-id="014cb-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="014cb-195">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="014cb-196">Obračun u stvarnom vremenu: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="014cb-197">Tip obračuna na stvarnom trošku: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="014cb-198">Tip obračuna na stvarnom materijalu: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="014cb-199">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="014cb-200">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="014cb-201">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="014cb-202">Samo izabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="014cb-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="014cb-203">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="014cb-204">Naplativo</span><span class="sxs-lookup"><span data-stu-id="014cb-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="014cb-205">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="014cb-206">Obračun u stvarnom vremenu: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="014cb-207">Tip obračuna na stvarnom trošku: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="014cb-208">Tip obračuna na stvarnom materijalu: <strong> Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="014cb-209">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="014cb-210">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="014cb-211">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="014cb-212">Samo izabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="014cb-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="014cb-213">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="014cb-214">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="014cb-215">Naplativo</span><span class="sxs-lookup"><span data-stu-id="014cb-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="014cb-216">Obračun u stvarnom vremenu: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="014cb-217">Tip obračuna na stvarnom trošku: <strong> Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="014cb-218">Tip obračuna na stvarnom materijalu: Naplativo</span><span class="sxs-lookup"><span data-stu-id="014cb-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="014cb-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="014cb-220">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="014cb-221">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="014cb-222">Čitav projekat</span><span class="sxs-lookup"><span data-stu-id="014cb-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="014cb-223">Nije moguće podesiti</span><span class="sxs-lookup"><span data-stu-id="014cb-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="014cb-224">
                    <strong>Naplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="014cb-225">Nije moguće podesiti</span><span class="sxs-lookup"><span data-stu-id="014cb-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="014cb-226">Obračun u stvarnom vremenu: <strong>Nije dostupno</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="014cb-227">Tip obračuna na stvarnom trošku: Naplativo</span><span class="sxs-lookup"><span data-stu-id="014cb-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="014cb-228">Tip obračuna na stvarnom materijalu: Naplativo</span><span class="sxs-lookup"><span data-stu-id="014cb-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="014cb-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="014cb-230">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="014cb-231">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="014cb-232">Čitav projekat</span><span class="sxs-lookup"><span data-stu-id="014cb-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="014cb-233">Nije moguće podesiti</span><span class="sxs-lookup"><span data-stu-id="014cb-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="014cb-234">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="014cb-235">Nije moguće podesiti</span><span class="sxs-lookup"><span data-stu-id="014cb-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="014cb-236">Obračun u stvarnom vremenu: <strong>Nije dostupno</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="014cb-237">Tip obračuna na stvarnom trošku: <strong> Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="014cb-238">Tip obračuna na stvarnom materijalu: Naplativo</span><span class="sxs-lookup"><span data-stu-id="014cb-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="014cb-239">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="014cb-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="014cb-241">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="014cb-242">Čitav projekat</span><span class="sxs-lookup"><span data-stu-id="014cb-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="014cb-243">Naplativo</span><span class="sxs-lookup"><span data-stu-id="014cb-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="014cb-244">Nije moguće podesiti</span><span class="sxs-lookup"><span data-stu-id="014cb-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="014cb-245">Nije moguće podesiti</span><span class="sxs-lookup"><span data-stu-id="014cb-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="014cb-246">Obračun u stvarnom vremenu: Naplativo</span><span class="sxs-lookup"><span data-stu-id="014cb-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="014cb-247">Tip obračuna na stvarnom trošku: <strong>Nije dostupno</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="014cb-248">Tip obračuna na stvarnom materijalu: Naplativo</span><span class="sxs-lookup"><span data-stu-id="014cb-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="014cb-249">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="014cb-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="014cb-251">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="014cb-252">Čitav projekat</span><span class="sxs-lookup"><span data-stu-id="014cb-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="014cb-253">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="014cb-254">Nije moguće podesiti</span><span class="sxs-lookup"><span data-stu-id="014cb-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="014cb-255">Nije moguće podesiti</span><span class="sxs-lookup"><span data-stu-id="014cb-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="014cb-256">Obračun u stvarnom vremenu: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="014cb-257">Tip obračuna na stvarnom trošku: <strong>Nije dostupno</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="014cb-258">Tip obračuna na stvarnom materijalu: Naplativo</span><span class="sxs-lookup"><span data-stu-id="014cb-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="014cb-259">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="014cb-260">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="014cb-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="014cb-262">Čitav projekat</span><span class="sxs-lookup"><span data-stu-id="014cb-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="014cb-263">Naplativo</span><span class="sxs-lookup"><span data-stu-id="014cb-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="014cb-264">Naplativo</span><span class="sxs-lookup"><span data-stu-id="014cb-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="014cb-265">Nije moguće podesiti</span><span class="sxs-lookup"><span data-stu-id="014cb-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="014cb-266">Obračun u stvarnom vremenu: Naplativo</span><span class="sxs-lookup"><span data-stu-id="014cb-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="014cb-267">Tip obračuna na stvarnom trošku: Naplativo</span><span class="sxs-lookup"><span data-stu-id="014cb-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="014cb-268">Tip obračuna na stvarnom materijalu: <strong> Nije dostupno</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="014cb-269">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="014cb-270">Da</span><span class="sxs-lookup"><span data-stu-id="014cb-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="014cb-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="014cb-272">Čitav projekat</span><span class="sxs-lookup"><span data-stu-id="014cb-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="014cb-273">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="014cb-274">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="014cb-275">Nije moguće podesiti</span><span class="sxs-lookup"><span data-stu-id="014cb-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="014cb-276">Obračun u stvarnom vremenu: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="014cb-277">Tip obračuna na stvarnom trošku:<strong> Nenaplativo </strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="014cb-278">Tip obračuna na stvarnom materijalu:<strong> Nije dostupno</strong>
                </span><span class="sxs-lookup"><span data-stu-id="014cb-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
