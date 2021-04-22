---
title: Konfigurišite naplative komponente stavke ponude
description: Ova tema pruža informacije o podešavanju naplativih i nenaplativih komponenata na liniji ponude zasnovanoj na projektu.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858310"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="b0fc2-103">Konfigurišite naplative komponente stavke ponude</span><span class="sxs-lookup"><span data-stu-id="b0fc2-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="b0fc2-104">_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture, Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="b0fc2-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b0fc2-105">Linija ponude zasnovana na projektu ima koncept *uključenih* komponenti i *naplativih* komponenti.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="b0fc2-106">Uključene komponente podležu:</span><span class="sxs-lookup"><span data-stu-id="b0fc2-106">Included components are subject to:</span></span>

  - <span data-ttu-id="b0fc2-107">Načinu naplate i podelama klijenata</span><span class="sxs-lookup"><span data-stu-id="b0fc2-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="b0fc2-108">Ograničenja koja ne smeju da se prekorače</span><span class="sxs-lookup"><span data-stu-id="b0fc2-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="b0fc2-109">Podešavanja učestalosti fakture definisane u liniji ponude zasnovane na projektu</span><span class="sxs-lookup"><span data-stu-id="b0fc2-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="b0fc2-110">Podskup uključenih komponenti može se označiti kao naplativ pomoću polja **Tip obračuna**.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="b0fc2-111">Polje **Tip obračuna** je skup opcija koji omogućava sledeće vrednosti u kontekstu linije ponude:</span><span class="sxs-lookup"><span data-stu-id="b0fc2-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="b0fc2-112">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-112">Chargeable</span></span>
  - <span data-ttu-id="b0fc2-113">Nenaplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-113">Non-chargeable</span></span>

<span data-ttu-id="b0fc2-114">Komponente koje se naplaćuju mogu se definisati na zadacima, ulogama i kategorijama transakcija.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="b0fc2-115">Naplativost je definisana na zadacima za liniju ponude i odnosi se na sve klase transakcija uključene u tu liniju.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="b0fc2-116">Ako je polje **Uključi zadatke** prazno ili postavljeno na **Čitav projekat**, kartica **Zadaci koji se naplaćuju** neće biti dostupna.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="b0fc2-117">Naplativost je definisana u ulogama za liniju ponude i odnosi se samo na klasu transakcija **Vreme**.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="b0fc2-118">Ako je polje **Uključi vreme** postavljeno na **Ne** na liniji ponude projekta, kartica **Uloge koje se naplaćuju** neće biti dostupna.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="b0fc2-119">Naplativost je definisana u kategorijama transakcija za liniju ponude i odnosi se samo na klasu transakcija **Trošak**.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="b0fc2-120">Ako je polje **Uključi troškove** postavljeno na **Ne** na liniji ponude projekta, kartica **Kategorije koje se naplaćuju** neće biti dostupna.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="b0fc2-121">Ažurirajte projektni zadatak tako da bude naplativ ili nenaplativ</span><span class="sxs-lookup"><span data-stu-id="b0fc2-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="b0fc2-122">Projektni zadatak može biti naplativ ili nenaplativ u kontekstu određene linije ponude zasnovane na projektu, što omogućava sledeće podešavanje.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="b0fc2-123">Ako linija ponude zasnovana na projektu uključuje **Vreme** i zadatak **T1**, zadatak je povezan sa linijom ponude kao naplativ.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="b0fc2-124">Ako postoji druga linija ponude koja uključuje **Troškove**, zadatak **T1** na liniji ponude možete povezati kao nenaplativ.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="b0fc2-125">Rezultat je da je sve vreme evidentirano u zadatku naplativo, a svi troškovi evidentirani u zadatku nenaplativi.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="b0fc2-126">Tip naplate zadatka može se konfigurisati na kartici **Naplativi zadaci** stavke ponude zasnovane na projektu ažuriranjem polja **Tip naplate** na podformi **Zadaci stavke ponude**.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="b0fc2-127">Pored toga, možete da ažurirate tip naplate za projektni zadatak u polju **Tip naplate** na podformi zadatka Postavljanje obračuna projekta koje prikazuje stavke ponude povezane sa zadatkom.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="b0fc2-128">Ažurirajte ulogu da bude naplativa ili nenaplativa</span><span class="sxs-lookup"><span data-stu-id="b0fc2-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="b0fc2-129">Uloga može biti naplativa ili nenaplativa u kontekstu određene linije ponude zasnovane na projektu.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="b0fc2-130">Tip naplate uloge se može konfigurisati na kartici **Naplativi zadaci** stavke ponude zasnovane na projektu ažuriranjem polja **Tip naplate** na podformi **Zadaci stavke ponude**.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="b0fc2-131">Ažurirajte kategoriju transakcija da bude naplativa ili nenaplativa</span><span class="sxs-lookup"><span data-stu-id="b0fc2-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="b0fc2-132">Kategorija transakcija može biti naplativa ili nenaplativa na određenoj liniji ponude.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="b0fc2-133">Tip naplate transakcije se može konfigurisati na kartici **Naplative kategorije** stavke ponude zasnovane na projektu ažuriranjem polja **Tip naplate** na podformi **Naplative kategorije**.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="b0fc2-134">Rešite naplativost</span><span class="sxs-lookup"><span data-stu-id="b0fc2-134">Resolve chargeability</span></span>
<span data-ttu-id="b0fc2-135">Procena ili stvarna vrednost kreirana za vreme smatraće se naplativom samo ako važi sledeće:</span><span class="sxs-lookup"><span data-stu-id="b0fc2-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="b0fc2-136">**Vreme** je uključeno u stavku ponude.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="b0fc2-137">**Uloga** je konfigurisana kao naplativa u stavki ponude.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="b0fc2-138">**Obuhvaćeni zadaci** su podešeni na vrednost **Izabrani zadaci** u stavki ponude.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="b0fc2-139">Ako su ove tri stvari tačne, **Zadatak** se takođe konfiguriše kao naplativ.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="b0fc2-140">Procena ili stvarna vrednost za trošak smatra se naplativom samo ako važi sledeće:</span><span class="sxs-lookup"><span data-stu-id="b0fc2-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="b0fc2-141">**Trošak** je uključen u stavku ponude.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="b0fc2-142">**Kategorija transakcije** je konfigurisana kao naplativa u stavki ponude.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="b0fc2-143">**Obuhvaćeni zadaci** su podešeni na vrednost **Izabrani zadaci** u stavki ponude.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="b0fc2-144">Ako su ove tri stvari tačne, **Zadatak** se takođe konfiguriše kao naplativ.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="b0fc2-145">Procena ili stvarna vrednost kreirana za materijal smatraće se naplativom samo ako važi sledeće:</span><span class="sxs-lookup"><span data-stu-id="b0fc2-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="b0fc2-146">**Materijali** su uključeni u stavku ponude.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="b0fc2-147">**Obuhvaćeni zadaci** su podešeni na vrednost **Izabrani zadaci** u stavki ponude.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="b0fc2-148">Ako su ove dve stvari tačne, **Zadatak** bi takođe trebalo da se konfiguriše kao naplativ.</span><span class="sxs-lookup"><span data-stu-id="b0fc2-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="b0fc2-149">
                    <strong>Sadrži vreme</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="b0fc2-150">
                    <strong>Sadrži trošak</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="b0fc2-151">
                    <strong>Sadrži materijale</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="b0fc2-152">
                    <strong>Obuhvaćeni zadaci</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b0fc2-153">
                    <strong>Uloga</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="b0fc2-154">
                    <strong>Kategorija</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b0fc2-155">
                    <strong>Zadatak</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="b0fc2-156">
                    <strong>Uticaj naplativosti</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0fc2-157">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0fc2-158">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0fc2-159">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0fc2-160">Čitav projekat</span><span class="sxs-lookup"><span data-stu-id="b0fc2-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0fc2-161">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0fc2-162">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0fc2-163">Ne može da se podesi</span><span class="sxs-lookup"><span data-stu-id="b0fc2-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0fc2-164">Obračun u stvarnom vremenu: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b0fc2-165">Tip obračuna na stvarnom trošku: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b0fc2-166">Tip obračuna na stvarnom materijalu: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0fc2-167">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0fc2-168">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0fc2-169">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0fc2-170">Samo izabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="b0fc2-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0fc2-171">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0fc2-172">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0fc2-173">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0fc2-174">Obračun u stvarnom vremenu: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b0fc2-175">Tip obračuna na stvarnom trošku: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b0fc2-176">Tip obračuna na stvarnom materijalu: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0fc2-177">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0fc2-178">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0fc2-179">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0fc2-180">Samo izabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="b0fc2-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b0fc2-181">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0fc2-182">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0fc2-183">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0fc2-184">Obračun u stvarnom vremenu: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0fc2-185">Tip obračuna na stvarnom trošku: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b0fc2-186">Tip obračuna na stvarnom materijalu: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0fc2-187">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0fc2-188">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0fc2-189">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0fc2-190">Samo izabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="b0fc2-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0fc2-191">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0fc2-192">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b0fc2-193">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0fc2-194">Obračun u stvarnom vremenu: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0fc2-195">Tip obračuna na stvarnom trošku: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0fc2-196">Tip obračuna na stvarnom materijalu: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0fc2-197">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0fc2-198">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0fc2-199">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0fc2-200">Samo izabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="b0fc2-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b0fc2-201">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0fc2-202">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b0fc2-203">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0fc2-204">Obračun u stvarnom vremenu: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0fc2-205">Tip obračuna na stvarnom trošku: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0fc2-206">Tip obračuna na stvarnom materijalu: <strong> Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0fc2-207">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0fc2-208">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0fc2-209">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0fc2-210">Samo izabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="b0fc2-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b0fc2-211">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="b0fc2-212">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0fc2-213">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0fc2-214">Obračun u stvarnom vremenu: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0fc2-215">Tip obračuna na stvarnom trošku: <strong> Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0fc2-216">Tip obračuna na stvarnom materijalu: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="b0fc2-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0fc2-218">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0fc2-219">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0fc2-220">Čitav projekat</span><span class="sxs-lookup"><span data-stu-id="b0fc2-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0fc2-221">Ne može da se podesi</span><span class="sxs-lookup"><span data-stu-id="b0fc2-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="b0fc2-222">
                    <strong>Naplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0fc2-223">Ne može da se podesi</span><span class="sxs-lookup"><span data-stu-id="b0fc2-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0fc2-224">Obračun u stvarnom vremenu: <strong>Nije dostupno</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0fc2-225">Tip obračuna na stvarnom trošku: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b0fc2-226">Tip obračuna na stvarnom materijalu: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="b0fc2-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0fc2-228">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0fc2-229">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0fc2-230">Čitav projekat</span><span class="sxs-lookup"><span data-stu-id="b0fc2-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0fc2-231">Ne može da se podesi</span><span class="sxs-lookup"><span data-stu-id="b0fc2-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="b0fc2-232">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0fc2-233">Ne može da se podesi</span><span class="sxs-lookup"><span data-stu-id="b0fc2-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0fc2-234">Obračun u stvarnom vremenu: <strong>Nije dostupno</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0fc2-235">Tip obračuna na stvarnom trošku: <strong> Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0fc2-236">Tip obračuna na stvarnom materijalu: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0fc2-237">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="b0fc2-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0fc2-239">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0fc2-240">Čitav projekat</span><span class="sxs-lookup"><span data-stu-id="b0fc2-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0fc2-241">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0fc2-242">Ne može da se podesi</span><span class="sxs-lookup"><span data-stu-id="b0fc2-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0fc2-243">Ne može da se podesi</span><span class="sxs-lookup"><span data-stu-id="b0fc2-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0fc2-244">Obračun u stvarnom vremenu: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b0fc2-245">Tip obračuna na stvarnom trošku: <strong>Nije dostupno</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0fc2-246">Tip obračuna na stvarnom materijalu: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0fc2-247">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="b0fc2-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0fc2-249">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0fc2-250">Čitav projekat</span><span class="sxs-lookup"><span data-stu-id="b0fc2-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b0fc2-251">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0fc2-252">Ne može da se podesi</span><span class="sxs-lookup"><span data-stu-id="b0fc2-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0fc2-253">Ne može da se podesi</span><span class="sxs-lookup"><span data-stu-id="b0fc2-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0fc2-254">Obračun u stvarnom vremenu: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0fc2-255">Tip obračuna na stvarnom trošku: <strong>Nije dostupno</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0fc2-256">Tip obračuna na stvarnom materijalu: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0fc2-257">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0fc2-258">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="b0fc2-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0fc2-260">Čitav projekat</span><span class="sxs-lookup"><span data-stu-id="b0fc2-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0fc2-261">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0fc2-262">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0fc2-263">Ne može da se podesi</span><span class="sxs-lookup"><span data-stu-id="b0fc2-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0fc2-264">Obračun u stvarnom vremenu: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b0fc2-265">Tip obračuna na stvarnom trošku: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0fc2-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b0fc2-266">Tip obračuna na stvarnom materijalu: <strong> Nije dostupno</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0fc2-267">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0fc2-268">Da</span><span class="sxs-lookup"><span data-stu-id="b0fc2-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="b0fc2-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0fc2-270">Čitav projekat</span><span class="sxs-lookup"><span data-stu-id="b0fc2-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b0fc2-271">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="b0fc2-272">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0fc2-273">Ne može da se podesi</span><span class="sxs-lookup"><span data-stu-id="b0fc2-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0fc2-274">Obračun u stvarnom vremenu: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0fc2-275">Tip obračuna na stvarnom trošku:<strong> Nenaplativo </strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0fc2-276">Tip obračuna na stvarnom materijalu:<strong> Nije dostupno</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0fc2-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
