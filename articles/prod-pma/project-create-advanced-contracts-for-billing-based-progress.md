---
title: Kreirajte napredne ugovore za naplatu na osnovu napretka
description: Ova tema objašnjava kako se kreiraju projektni ugovori tako da možete generisati fakture za klijente na osnovu procenta završenog posla.
author: RadhikaRS
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 3b445488100e0a8335a05505405953b173ff836c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999688"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="6c586-103">Kreirajte napredne ugovore za naplatu na osnovu napretka</span><span class="sxs-lookup"><span data-stu-id="6c586-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c586-104">Ova tema objašnjava kako se kreiraju projektni ugovori tako da možete kreirati fakture za klijente na osnovu procenta završenog posla.</span><span class="sxs-lookup"><span data-stu-id="6c586-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="6c586-105">Iznosi faktura se automatski izračunavaju za budžetske kategorije posla koje ste postavili za projekat.</span><span class="sxs-lookup"><span data-stu-id="6c586-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="6c586-106">Vreme na fakturi se postavlja kada pregovarate sa klijentom o ugovoru o projektu.</span><span class="sxs-lookup"><span data-stu-id="6c586-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="6c586-107">Koristite procedure u ovoj temi za postavljanje ugovora, pridruženog projekta i pravila obračuna koji izračunavaju iznose faktura za budžetske kategorije posla koje ste postavili za projekat.</span><span class="sxs-lookup"><span data-stu-id="6c586-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="6c586-108">Nakon što napravite ugovor i projekat, možete da podesite detalje o projektu.</span><span class="sxs-lookup"><span data-stu-id="6c586-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="6c586-109">Na primer, možete definisati aktivnosti i dodeliti radnike projektu.</span><span class="sxs-lookup"><span data-stu-id="6c586-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="6c586-110">Primer</span><span class="sxs-lookup"><span data-stu-id="6c586-110">Example</span></span>

<span data-ttu-id="6c586-111">Vaša organizacija je firma za razvoj softvera.</span><span class="sxs-lookup"><span data-stu-id="6c586-111">Your organization is a software development firm.</span></span> <span data-ttu-id="6c586-112">Pristajete da razvijete paket za obračun zarada za klijenta za ukupnu naknadu od 20.000 američkih dolara (USD).</span><span class="sxs-lookup"><span data-stu-id="6c586-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="6c586-113">Vaša organizacija pristaje da fakturiše klijentu kako dovršavate određene procente projekta.</span><span class="sxs-lookup"><span data-stu-id="6c586-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="6c586-114">Za rad postavljate sledeće kategorije projekata kako biste ih mogli koristiti u procesu naplate:</span><span class="sxs-lookup"><span data-stu-id="6c586-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="6c586-115">Konsultantske usluge</span><span class="sxs-lookup"><span data-stu-id="6c586-115">Consulting</span></span>
- <span data-ttu-id="6c586-116">Dizajn</span><span class="sxs-lookup"><span data-stu-id="6c586-116">Design</span></span>
- <span data-ttu-id="6c586-117">Instalacija</span><span class="sxs-lookup"><span data-stu-id="6c586-117">Installation</span></span>

<span data-ttu-id="6c586-118">Postavljate i pravila naplate koja automatski izračunavaju iznose faktura za procenat završenog posla na projektu za svaku kategoriju.</span><span class="sxs-lookup"><span data-stu-id="6c586-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="6c586-119">Menadžer budžeta kreira budžet za kategorije projekata.</span><span class="sxs-lookup"><span data-stu-id="6c586-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="6c586-120">Količina obavljenog posla automatski se izračunava kao procenat stvarnog posla u poređenju sa planiranim iznosima.</span><span class="sxs-lookup"><span data-stu-id="6c586-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6c586-121">Preduslovi</span><span class="sxs-lookup"><span data-stu-id="6c586-121">Prerequisites</span></span>

<span data-ttu-id="6c586-122">Pre nego što kreirate projekat koji koristi pravila naplate, morate podesiti sekvence brojeva za pravila naplate i dnevnik naknada koji se koristi za knjiženje napredovanja.</span><span class="sxs-lookup"><span data-stu-id="6c586-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="6c586-123">Idite na **Upravljanje projektima i računovodstvo** \> **Podešavanje** \> **Upravljanje projektom i računovodstveni parametri**.</span><span class="sxs-lookup"><span data-stu-id="6c586-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="6c586-124">Na stranici **Upravljanje projektom i računovodstveni parametri**, na kartici **Brojčane sekvence** podesite redosled brojeva koji želite da koristite prilikom kreiranja pravila za obračun.</span><span class="sxs-lookup"><span data-stu-id="6c586-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="6c586-125">Idite na **Upravljanje projektima i računovodstvo** \> **Dnevnici** \> **Naknada**.</span><span class="sxs-lookup"><span data-stu-id="6c586-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="6c586-126">Na stranici **Dnevnik naknada**, izaberite **Novo** i unesite naziv dnevnika.</span><span class="sxs-lookup"><span data-stu-id="6c586-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="6c586-127">Napravite ugovor za napredak fakturisanja</span><span class="sxs-lookup"><span data-stu-id="6c586-127">Create a contract for progress billings</span></span>

<span data-ttu-id="6c586-128">Koristite ovaj postupak za kreiranje ugovora o projektu za projekat sa fiksnom cenom.</span><span class="sxs-lookup"><span data-stu-id="6c586-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="6c586-129">Fakturu za projekat kreirate kada posao koji je završen na projektu dostigne određeni procenat.</span><span class="sxs-lookup"><span data-stu-id="6c586-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="6c586-130">Idite na **Upravljanje projektima i računovodstvo** \> **Projekti** \> **Ugovori projekata**.</span><span class="sxs-lookup"><span data-stu-id="6c586-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="6c586-131">Na stranici **Ugovori projekata** izaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="6c586-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="6c586-132">U dijalogu **Novi ugovor o projektu** postavite sledeća polja:</span><span class="sxs-lookup"><span data-stu-id="6c586-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="6c586-133">**Ime**</span><span class="sxs-lookup"><span data-stu-id="6c586-133">**Name**</span></span>
    - <span data-ttu-id="6c586-134">**Tip finansiranja**</span><span class="sxs-lookup"><span data-stu-id="6c586-134">**Funding type**</span></span>
    - <span data-ttu-id="6c586-135">**Izvor finansiranja**</span><span class="sxs-lookup"><span data-stu-id="6c586-135">**Funding source**</span></span>
    - <span data-ttu-id="6c586-136">**Valuta prodaje** - Ova valuta se podrazumevano koristi za račune kupaca koji su povezani sa projektnim ugovorom.</span><span class="sxs-lookup"><span data-stu-id="6c586-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="6c586-137">Međutim, valutu prodaje možete promeniti na određenoj fakturi kupca.</span><span class="sxs-lookup"><span data-stu-id="6c586-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="6c586-138">Izaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="6c586-138">Select **OK**.</span></span> <span data-ttu-id="6c586-139">Podaci se kopiraju u zaglavlje stranice **Projektni ugovori**.</span><span class="sxs-lookup"><span data-stu-id="6c586-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="6c586-140">Na stranici **Projektni ugovori**, popunite ostatak potrebnih podataka za projekat.</span><span class="sxs-lookup"><span data-stu-id="6c586-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="6c586-141">Napravite projekat za napredak fakturisanja</span><span class="sxs-lookup"><span data-stu-id="6c586-141">Create a project for progress billings</span></span>

<span data-ttu-id="6c586-142">Sledite ove korake da biste kreirali projekat i sve potprojekte koji su povezani sa projektnim ugovorom.</span><span class="sxs-lookup"><span data-stu-id="6c586-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="6c586-143">Idite na **Upravljanje projektima i računovodstvo** \> **Projekti** \> **Svi projekti**.</span><span class="sxs-lookup"><span data-stu-id="6c586-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="6c586-144">Na stranici **Svi ugovori** izaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="6c586-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="6c586-145">U dijalogu **Novi projekat**, u polju **Tip projekta** izaberite **Vreme i materijal**.</span><span class="sxs-lookup"><span data-stu-id="6c586-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="6c586-146">Izaberite grupu projekata.</span><span class="sxs-lookup"><span data-stu-id="6c586-146">Select a project group.</span></span> <span data-ttu-id="6c586-147">Projektna grupa definiše informacije o objavljivanju za projekte koji su dodeljeni grupi.</span><span class="sxs-lookup"><span data-stu-id="6c586-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="6c586-148">Izaberite **Kreirajte projekat**.</span><span class="sxs-lookup"><span data-stu-id="6c586-148">Select **Create project**.</span></span>
6. <span data-ttu-id="6c586-149">Nakon kreiranja projekta, postavite fazu projekta na **U toku**.</span><span class="sxs-lookup"><span data-stu-id="6c586-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="6c586-150">Kreiranje budžeta za projekat</span><span class="sxs-lookup"><span data-stu-id="6c586-150">Create a budget for a project</span></span>

<span data-ttu-id="6c586-151">Kategorije budžeta se koriste za automatsko izračunavanje iznosa faktura za procenat završenog posla za svaku kategoriju.</span><span class="sxs-lookup"><span data-stu-id="6c586-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="6c586-152">Sledite ove korake da biste kreirali budžetske kategorije za procenjene troškove.</span><span class="sxs-lookup"><span data-stu-id="6c586-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="6c586-153">Idite na **Upravljanje projektima i računovodstvo** \> **Projekti** \> **Svi projekti**.</span><span class="sxs-lookup"><span data-stu-id="6c586-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="6c586-154">Na stranici **Svi projekti** izaberite i otvorite projekat koji želite.</span><span class="sxs-lookup"><span data-stu-id="6c586-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="6c586-155">Na stranici **Projekti**, u oknu akcija, na kartici **Plan**, u grupi **Budžet** izaberite **Budžet projekta**.</span><span class="sxs-lookup"><span data-stu-id="6c586-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="6c586-156">Na stranici **Budžet projekta** unesite procenjeni trošak za svaku kategoriju u projektu.</span><span class="sxs-lookup"><span data-stu-id="6c586-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="6c586-157">Kreirajte pravila naplate za napredovanje računa</span><span class="sxs-lookup"><span data-stu-id="6c586-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="6c586-158">Idite na **Upravljanje projektima i računovodstvo** \> **Projekti** \> **Ugovori projekata**.</span><span class="sxs-lookup"><span data-stu-id="6c586-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="6c586-159">Na stranici **Ugovori o projektima** izaberite i otvorite ugovor o projektu.</span><span class="sxs-lookup"><span data-stu-id="6c586-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="6c586-160">Na stranici ugovora o projektu, na brzoj kartici **Pravila za naplatu** izaberite **Dodaj**.</span><span class="sxs-lookup"><span data-stu-id="6c586-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="6c586-161">Na stranici **Pravilo za obračun**, u polju **Tip linije** izaberite **Napredak**.</span><span class="sxs-lookup"><span data-stu-id="6c586-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="6c586-162">Na brzoj kartici **Detalji linije pravila za obračun**, u polju **Vrednost ugovora** unesite ukupnu vrednost ugovora.</span><span class="sxs-lookup"><span data-stu-id="6c586-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="6c586-163">U polju **Kategorija** odaberite kategoriju u kojoj ćete objaviti transakciju naknade.</span><span class="sxs-lookup"><span data-stu-id="6c586-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="6c586-164">U polju **Projekat** izaberite projekat koji koristi ovo pravilo naplate.</span><span class="sxs-lookup"><span data-stu-id="6c586-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="6c586-165">Opcionalno: Dodelite pravilo naplate dodatnim projektima.</span><span class="sxs-lookup"><span data-stu-id="6c586-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="6c586-166">Na brzoj kartici **Projekat**, u odeljku **Dostupni projekti** izaberite projekat, a zatim pritisnite dugme sa strelicom udesno da biste dodali projekat u odeljak **Odabrani projekti**.</span><span class="sxs-lookup"><span data-stu-id="6c586-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="6c586-167">Opcionalno: Izračunajte procentualni iznos koji kupac zadržava od plaćanja na računu.</span><span class="sxs-lookup"><span data-stu-id="6c586-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="6c586-168">Na brzoj kartici **Uslovi zadržavanja plaćanja** izaberite izvor finansiranja, a zatim u polju **Procenat zadržavanja** unesite procenat zadržavanja.</span><span class="sxs-lookup"><span data-stu-id="6c586-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="6c586-169">Ponovite ove korake da biste kreirali dodatna pravila za obračun za projektni ugovor.</span><span class="sxs-lookup"><span data-stu-id="6c586-169">Repeat these steps to create additional billing rules for the project contract.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]