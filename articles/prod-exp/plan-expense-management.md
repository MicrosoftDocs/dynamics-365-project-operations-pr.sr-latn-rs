---
title: Konfigurisanje upravljanja troškovima
description: Ovaj članak opisuje razmatranja i odluke koje morate doneti tokom procesa planiranja pre nego što konfigurišete upravljanje troškovima u usluzi Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2291515cc154fb5b34ca5802135791958bea1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083728"
---
# <a name="configure-expense-management"></a><span data-ttu-id="0556c-103">Konfigurisanje upravljanja troškovima</span><span class="sxs-lookup"><span data-stu-id="0556c-103">Configure expense management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0556c-104">Ova tema opisuje razmatranja i odluke koje morate doneti tokom procesa planiranja pre nego što konfigurišete upravljanje troškovima.</span><span class="sxs-lookup"><span data-stu-id="0556c-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="0556c-105">U upravljanju troškovima možete da čuvate informacije o načinima plaćanja, putnim zahtevima, izveštajima o troškovima, smernicama itd.</span><span class="sxs-lookup"><span data-stu-id="0556c-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="0556c-106">Budući da se mnoge odluke koje donosite kada planirate konfiguraciju za upravljanje troškovima zasnivaju na hijerarhiji i finansijskoj strukturi vaše organizacije, morate pogledati dokumente za planiranje za ta područja.</span><span class="sxs-lookup"><span data-stu-id="0556c-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="0556c-107">Međukompanijski troškovi</span><span class="sxs-lookup"><span data-stu-id="0556c-107">Intercompany expenses</span></span>

<span data-ttu-id="0556c-108">Kada omogućite međukompanijske troškove, dozvoljavate pravnim licima i zaposlenima da prave troškove u ime drugog pravnog lica i prikupljaju uplate od pravnog lica zaposlenog u vašoj organizaciji.</span><span class="sxs-lookup"><span data-stu-id="0556c-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="0556c-109">Na primer, zaposleni u pravnom licu A završava projekat za pravno lice B, a projekat obuhvata putne troškove.</span><span class="sxs-lookup"><span data-stu-id="0556c-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="0556c-110">Ako su omogućeni međukompanijski troškovi, zaposleni tada može podneti izveštaj o troškovima koji će trošak knjižiti pravnom licu B, a trošak tada mora platiti pravno lice A. Ako vaša organizacija nema više pravnih lica, ne morate da omogućite međukompanijske troškove.</span><span class="sxs-lookup"><span data-stu-id="0556c-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="0556c-111">**Odluka:** Da li želite da omogućite međukompanijske troškove?</span><span class="sxs-lookup"><span data-stu-id="0556c-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="0556c-112">Finansijski menadžment</span><span class="sxs-lookup"><span data-stu-id="0556c-112">Financial management</span></span>

<span data-ttu-id="0556c-113">Upravljanje troškovima je usko integrisano sa finansijskim upravljanjem vaše organizacije.</span><span class="sxs-lookup"><span data-stu-id="0556c-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="0556c-114">Veliki deo vaše konfiguracije za upravljanje troškovima zasnivaće se na odlukama koje ste doneli o finansijama organizacije.</span><span class="sxs-lookup"><span data-stu-id="0556c-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="0556c-115">Sledeći odeljci opisuju različita područja koja zahtevaju planiranje i donošenje odluka, na osnovu finansijskih odluka vaše organizacije i smernica vašeg rukovodećeg tima.</span><span class="sxs-lookup"><span data-stu-id="0556c-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="0556c-116">Dnevnice</span><span class="sxs-lookup"><span data-stu-id="0556c-116">Per diems</span></span>

<span data-ttu-id="0556c-117">Morate definisati dnevnice za zaposlene koje pruža vaša organizacija.</span><span class="sxs-lookup"><span data-stu-id="0556c-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="0556c-118">Budući da se dnevnice obično koriste za pokrivanje troškova kao što su obroci, smeštaj i drugi slučajni troškovi, možete kreirati pravila za dnevnice koje vaša organizacija nudi.</span><span class="sxs-lookup"><span data-stu-id="0556c-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="0556c-119">Iznosi dnevnica mogu se zasnivati na dobu godine, lokaciji putovanja ili oboje.</span><span class="sxs-lookup"><span data-stu-id="0556c-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="0556c-120">Kada definišete pravilo za dnevnicu, možete da odredite da se procenat dnevnice zadržava ako radnik dobije besplatne obroke ili usluge.</span><span class="sxs-lookup"><span data-stu-id="0556c-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="0556c-121">Takođe možete da definišete nivoe dnevnica da biste odredili minimalni i maksimalni broj sati za koji dnevnica može da se primenjuje na putovanje radnika.</span><span class="sxs-lookup"><span data-stu-id="0556c-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="0556c-122">**Odluke:**</span><span class="sxs-lookup"><span data-stu-id="0556c-122">**Decisions:**</span></span>

- <span data-ttu-id="0556c-123">Podrazumevana pravila za dnevnice za prvi i poslednji dan:</span><span class="sxs-lookup"><span data-stu-id="0556c-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="0556c-124">Koji je minimalan broj sati koje zaposleni može tražiti jedan dan, a da i dalje dobije dnevnicu?</span><span class="sxs-lookup"><span data-stu-id="0556c-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="0556c-125">Da li postoji smanjenje količine koja se nudi za obroke prvog i poslednjeg dana?</span><span class="sxs-lookup"><span data-stu-id="0556c-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="0556c-126">Ako postoji smanjenje, koliki je procenat smanjenja?</span><span class="sxs-lookup"><span data-stu-id="0556c-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="0556c-127">Da li postoji smanjenje količine koja se nudi za hotel prvog i poslednjeg dana?</span><span class="sxs-lookup"><span data-stu-id="0556c-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="0556c-128">Ako postoji smanjenje, koliki je procenat smanjenja?</span><span class="sxs-lookup"><span data-stu-id="0556c-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="0556c-129">Da li postoji smanjenje količine koja se nudi za druge troškove do kojih dođe prvog i poslednjeg dana?</span><span class="sxs-lookup"><span data-stu-id="0556c-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="0556c-130">Ako postoji smanjenje, koliki je procenat smanjenja?</span><span class="sxs-lookup"><span data-stu-id="0556c-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="0556c-131">Podrazumevana pravila za dnevnice:</span><span class="sxs-lookup"><span data-stu-id="0556c-131">Default per diem rules:</span></span>

    - <span data-ttu-id="0556c-132">Da li postoji procentualno smanjenje dnevnice za svaki obrok ako je, na primer, obrok besplatan?</span><span class="sxs-lookup"><span data-stu-id="0556c-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="0556c-133">Ako postoji smanjenje, koliki je procenat smanjenja za svaki obrok?</span><span class="sxs-lookup"><span data-stu-id="0556c-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="0556c-134">Da li se smanjenje obroka izračunava dnevno, po putovanju ili po broju obroka dnevno?</span><span class="sxs-lookup"><span data-stu-id="0556c-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="0556c-135">Da li iznose dnevnica treba redovno zaokruživati ili zaokruživati nagore?</span><span class="sxs-lookup"><span data-stu-id="0556c-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="0556c-136">Da li se dnevnice obračunavaju na 24-časovni period ili na kalendarski dan?</span><span class="sxs-lookup"><span data-stu-id="0556c-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="0556c-137">Pravila za dnevnice zasnovana na lokaciji:</span><span class="sxs-lookup"><span data-stu-id="0556c-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="0556c-138">Da li se dnevnice razlikuju u zavisnosti od lokacije?</span><span class="sxs-lookup"><span data-stu-id="0556c-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="0556c-139">Koje su lokacije uključene?</span><span class="sxs-lookup"><span data-stu-id="0556c-139">What locations are included?</span></span>
    - <span data-ttu-id="0556c-140">Ako se dnevnice razlikuju u zavisnosti od lokacije, za svaku lokaciju, koliki procenat se predviđa za sledeće vrste troškova:</span><span class="sxs-lookup"><span data-stu-id="0556c-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="0556c-141">Obroci</span><span class="sxs-lookup"><span data-stu-id="0556c-141">Meals</span></span>
        - <span data-ttu-id="0556c-142">Hotel</span><span class="sxs-lookup"><span data-stu-id="0556c-142">Hotel</span></span>
        - <span data-ttu-id="0556c-143">Ostali troškovi</span><span class="sxs-lookup"><span data-stu-id="0556c-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="0556c-144">Dnevnici i računi za upravljanje troškovima</span><span class="sxs-lookup"><span data-stu-id="0556c-144">Expense management journals and accounts</span></span>

<span data-ttu-id="0556c-145">Upravljanje troškovima zahteva upotrebu više dnevnika i računa.</span><span class="sxs-lookup"><span data-stu-id="0556c-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="0556c-146">Morate da odlučite, na primer, da li se isti račun koristi za akontacije i sporove o kreditnim karticama.</span><span class="sxs-lookup"><span data-stu-id="0556c-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="0556c-147">**Odluke:**</span><span class="sxs-lookup"><span data-stu-id="0556c-147">**Decisions:**</span></span>

- <span data-ttu-id="0556c-148">U kojem se dnevniku za knjiženje objavljuju odobreni izveštaji o troškovima?</span><span class="sxs-lookup"><span data-stu-id="0556c-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="0556c-149">Koji račun se koristi za akontacije?</span><span class="sxs-lookup"><span data-stu-id="0556c-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="0556c-150">Da li treba odmah knjižiti akontacije?</span><span class="sxs-lookup"><span data-stu-id="0556c-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="0556c-151">Načini plaćanja</span><span class="sxs-lookup"><span data-stu-id="0556c-151">Payment methods</span></span>

<span data-ttu-id="0556c-152">Kada dozvoljavate zaposlenima da prave troškove u ime vašeg preduzeća, morate da definišete načine plaćanja koje zaposleni smeju da koriste.</span><span class="sxs-lookup"><span data-stu-id="0556c-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="0556c-153">Na primer, zaposlenima možete dozvoliti da koriste gotovinu ili korporativnu kreditnu karticu.</span><span class="sxs-lookup"><span data-stu-id="0556c-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="0556c-154">Takođe možete dozvoliti zaposlenima da koriste lične kreditne kartice, a zatim zaposlenima nadoknaditi novac.</span><span class="sxs-lookup"><span data-stu-id="0556c-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="0556c-155">Morate doneti sledeće odluke za svaki način plaćanja koji dozvoljavate.</span><span class="sxs-lookup"><span data-stu-id="0556c-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="0556c-156">**Odluke:**</span><span class="sxs-lookup"><span data-stu-id="0556c-156">**Decisions:**</span></span>

- <span data-ttu-id="0556c-157">Koji su načini plaćanja dozvoljeni?</span><span class="sxs-lookup"><span data-stu-id="0556c-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="0556c-158">Ko je vlasnik troškova plaćanja?</span><span class="sxs-lookup"><span data-stu-id="0556c-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="0556c-159">Da li postoji tip računa za prebijanje dugovanja?</span><span class="sxs-lookup"><span data-stu-id="0556c-159">Is there an offset account type?</span></span> <span data-ttu-id="0556c-160">Ako postoji tip računa za prebijanje dugovanja, šta je to?</span><span class="sxs-lookup"><span data-stu-id="0556c-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="0556c-161">Ako postoji tip računa za prebijanje dugovanja, koji je to račun?</span><span class="sxs-lookup"><span data-stu-id="0556c-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="0556c-162">Ako je način plaćanja kreditna kartica, da li bi način plaćanja trebalo koristiti samo kod uvezenih transakcija?</span><span class="sxs-lookup"><span data-stu-id="0556c-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="0556c-163">Kategorije troškova i deljene kategorije</span><span class="sxs-lookup"><span data-stu-id="0556c-163">Expense categories and shared categories</span></span>

<span data-ttu-id="0556c-164">Kada zaposleni kreiraju izveštaj o troškovima, svaki trošak koji evidentiraju mora biti povezan sa kategorijom troškova.</span><span class="sxs-lookup"><span data-stu-id="0556c-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="0556c-165">Kategorije troškova su izvedene iz deljenih kategorija koje se mogu deliti između pravnih lica u vašoj organizaciji.</span><span class="sxs-lookup"><span data-stu-id="0556c-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="0556c-166">Ove kategorije se takođe mogu deliti u upravljanju projektima i računovodstvu, u zavisnosti od načina na koji je vaša organizacija definisana.</span><span class="sxs-lookup"><span data-stu-id="0556c-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="0556c-167">Na osnovu definicije vaše organizacije i smernica tima za primenu, morate da odredite da li će se kategorije koje se koriste u upravljanju troškovima koristiti samo u upravljanju troškovima ili treba da se dele između upravljanja projektima i računovodstva i upravljanja troškovima.</span><span class="sxs-lookup"><span data-stu-id="0556c-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="0556c-168">Imajte na umu da se ove kategorije se mogu deliti između upravljanja projektima i troškova ili upravljanja projektima i proizvodnje, ali ne između upravljanja troškovima i proizvodnje.</span><span class="sxs-lookup"><span data-stu-id="0556c-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="0556c-169">Za svaku kategoriju troškova morate doneti sledeće odluke.</span><span class="sxs-lookup"><span data-stu-id="0556c-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="0556c-170">**Odluke:**</span><span class="sxs-lookup"><span data-stu-id="0556c-170">**Decisions:**</span></span>

- <span data-ttu-id="0556c-171">Šta je to kategorija troškova?</span><span class="sxs-lookup"><span data-stu-id="0556c-171">What is the expense category?</span></span> <span data-ttu-id="0556c-172">Primeri uključuju kategorije za letove, hotele ili kilometražu.</span><span class="sxs-lookup"><span data-stu-id="0556c-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="0556c-173">Može li se kategorija troškova takođe koristiti u upravljanju projektima i računovodstvu?</span><span class="sxs-lookup"><span data-stu-id="0556c-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="0556c-174">Šta je to tip troška?</span><span class="sxs-lookup"><span data-stu-id="0556c-174">What is the expense type?</span></span>
- <span data-ttu-id="0556c-175">Koji je podrazumevani način plaćanja za kategoriju troška?</span><span class="sxs-lookup"><span data-stu-id="0556c-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="0556c-176">Moraju li se detaljno deliti troškovi u kategoriji troškova?</span><span class="sxs-lookup"><span data-stu-id="0556c-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="0556c-177">Koji je glavni podrazumevani račun za kategoriju troška?</span><span class="sxs-lookup"><span data-stu-id="0556c-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="0556c-178">Koja je podrazumevana grupa poreza na promet proizvoda za kategoriju troškova?</span><span class="sxs-lookup"><span data-stu-id="0556c-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="0556c-179">Da li su dozvoljeni dodatni načini plaćanja za kategoriju troškova?</span><span class="sxs-lookup"><span data-stu-id="0556c-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="0556c-180">Ako su dozvoljeni dodatni načini plaćanja, koji su to?</span><span class="sxs-lookup"><span data-stu-id="0556c-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="0556c-181">Postoje li potkategorije u ovoj kategoriji troškova?</span><span class="sxs-lookup"><span data-stu-id="0556c-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="0556c-182">Ako postoje potkategorije, morate doneti i sledeće odluke:</span><span class="sxs-lookup"><span data-stu-id="0556c-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="0556c-183">Da li je neka od potkategorija izuzeta od povraćaja poreza?</span><span class="sxs-lookup"><span data-stu-id="0556c-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="0556c-184">Koja je grupa poreza na promet proizvoda za potkategorije?</span><span class="sxs-lookup"><span data-stu-id="0556c-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="0556c-185">Ako se kategorija troškova koristi i u upravljanju projektima i računovodstvu, odgovorite na preostala pitanja.</span><span class="sxs-lookup"><span data-stu-id="0556c-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="0556c-186">U suprotnom, pređite na sledeći odeljak.</span><span class="sxs-lookup"><span data-stu-id="0556c-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="0556c-187">Koji računi troškova će se koristiti za sledeće troškove?</span><span class="sxs-lookup"><span data-stu-id="0556c-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="0556c-188">Cena</span><span class="sxs-lookup"><span data-stu-id="0556c-188">Cost</span></span>
    - <span data-ttu-id="0556c-189">Raspodela zarada</span><span class="sxs-lookup"><span data-stu-id="0556c-189">Payroll allocation</span></span>
    - <span data-ttu-id="0556c-190">Prihodi u toku – vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0556c-190">WIP-cost value</span></span>
    - <span data-ttu-id="0556c-191">Stavka troškova</span><span class="sxs-lookup"><span data-stu-id="0556c-191">Cost-item</span></span>
    - <span data-ttu-id="0556c-192">Prihodi u toku – vrednost troškova – stavka</span><span class="sxs-lookup"><span data-stu-id="0556c-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="0556c-193">Obračunati gubitak</span><span class="sxs-lookup"><span data-stu-id="0556c-193">Accrued loss</span></span>
    - <span data-ttu-id="0556c-194">Prihodi u toku – obračunati gubitak</span><span class="sxs-lookup"><span data-stu-id="0556c-194">WIP-accrued loss</span></span>

- <span data-ttu-id="0556c-195">Koji računi prihoda će se koristiti za sledeće?</span><span class="sxs-lookup"><span data-stu-id="0556c-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="0556c-196">Fakturisani prihod</span><span class="sxs-lookup"><span data-stu-id="0556c-196">Invoiced revenue</span></span>
    - <span data-ttu-id="0556c-197">Obračunati prihod – Vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="0556c-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="0556c-198">Prihodi u toku – vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="0556c-198">WIP-sales value</span></span>
    - <span data-ttu-id="0556c-199">Obračunati prihod – proizvodnja</span><span class="sxs-lookup"><span data-stu-id="0556c-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="0556c-200">Prihodi u toku – proizvodnja</span><span class="sxs-lookup"><span data-stu-id="0556c-200">WIP-production</span></span>
    - <span data-ttu-id="0556c-201">Obračunati prihod – dobitak</span><span class="sxs-lookup"><span data-stu-id="0556c-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="0556c-202">Prihodi u toku – dobitak</span><span class="sxs-lookup"><span data-stu-id="0556c-202">WIP-profit</span></span>
    - <span data-ttu-id="0556c-203">Obračunati prihod – pretplata</span><span class="sxs-lookup"><span data-stu-id="0556c-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="0556c-204">Prihodi u toku – pretplata</span><span class="sxs-lookup"><span data-stu-id="0556c-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="0556c-205">Porezi</span><span class="sxs-lookup"><span data-stu-id="0556c-205">Taxes</span></span>

<span data-ttu-id="0556c-206">Za poreze povezane sa troškovima morate utvrditi šta je uključeno ili omogućeno u izveštajima o troškovima.</span><span class="sxs-lookup"><span data-stu-id="0556c-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="0556c-207">**Odluke:**</span><span class="sxs-lookup"><span data-stu-id="0556c-207">**Decisions:**</span></span>

- <span data-ttu-id="0556c-208">Da li je porez na promet uključen u iznose troškova?</span><span class="sxs-lookup"><span data-stu-id="0556c-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="0556c-209">Da li treba omogućiti povrat poreza na troškove?</span><span class="sxs-lookup"><span data-stu-id="0556c-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="0556c-210">Kada ste planirali glavnu knjigu, ako ste odlučili da primenite američki porez na promet i koristite poreska pravila, ne možete da omogućite povraćaj poreza na troškove.</span><span class="sxs-lookup"><span data-stu-id="0556c-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="0556c-211">(Da biste primenili američki porez na promet i koristili poreska pravila, postavite opciju **Primeni pravila oporezivanja za porez na promet** na **Da**.)</span><span class="sxs-lookup"><span data-stu-id="0556c-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="0556c-212">smernice/a</span><span class="sxs-lookup"><span data-stu-id="0556c-212">Policies</span></span>

<span data-ttu-id="0556c-213">Kreiranjem smernica za izveštavanje o troškovima možete da pomognete svojoj organizaciji da uštedi vreme i novac kada zaposleni naprave troškove u njeno ime.</span><span class="sxs-lookup"><span data-stu-id="0556c-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="0556c-214">Pravila pomažu da zaposleni ostanu u okviru budžeta, pruže sve potrebne informacije i troše novac samo onako kako im je potrebno.</span><span class="sxs-lookup"><span data-stu-id="0556c-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="0556c-215">Morate doneti sledeće odluke za svake smernice za izveštavanje o troškovima i svake smernice za odobravanje izveštaja o troškovima koju kreirate.</span><span class="sxs-lookup"><span data-stu-id="0556c-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="0556c-216">**Odluke:**</span><span class="sxs-lookup"><span data-stu-id="0556c-216">**Decisions:**</span></span>

- <span data-ttu-id="0556c-217">Kako se zovu smernice?</span><span class="sxs-lookup"><span data-stu-id="0556c-217">What is the name of the policy?</span></span>
- <span data-ttu-id="0556c-218">Čemu služe smernice o troškovima?</span><span class="sxs-lookup"><span data-stu-id="0556c-218">What is the expense policy for?</span></span>
- <span data-ttu-id="0556c-219">Ako ste prethodno odlučili da omogućite međukompanijske troškove, na koje kompanije u vašoj organizaciji će se primenjivati ove smernice?</span><span class="sxs-lookup"><span data-stu-id="0556c-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="0556c-220">Kada smernice stupaju na snagu?</span><span class="sxs-lookup"><span data-stu-id="0556c-220">When does the policy become effective?</span></span>
- <span data-ttu-id="0556c-221">Kada smernice ističu?</span><span class="sxs-lookup"><span data-stu-id="0556c-221">When does the policy expire?</span></span>
- <span data-ttu-id="0556c-222">Kakvo je pravilo smernica?</span><span class="sxs-lookup"><span data-stu-id="0556c-222">What is the policy rule?</span></span>
- <span data-ttu-id="0556c-223">Kakav je ishod pravila smernica?</span><span class="sxs-lookup"><span data-stu-id="0556c-223">What is the outcome of the policy rule?</span></span>
