---
title: Cenovnici projekta
description: Ova tema pruža informacije o entitetu cenovnika projekta.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: d09a0dd8234641ca106c37a38d1d721dfb07236c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898683"
---
# <a name="project-price-lists"></a><span data-ttu-id="6ca42-103">Cenovnici projekta</span><span class="sxs-lookup"><span data-stu-id="6ca42-103">Project price lists</span></span>

<span data-ttu-id="6ca42-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="6ca42-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6ca42-105">Dynamics 365 Project Operations proširuje entitet cenovnika u usluzi Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="6ca42-105">Dynamics 365 Project Operations extends the Price list entity in Dynamics 365 Sales.</span></span> 

## <a name="key-entities"></a><span data-ttu-id="6ca42-106">Ključni entiteti</span><span class="sxs-lookup"><span data-stu-id="6ca42-106">Key entities</span></span>

<span data-ttu-id="6ca42-107">Cenovnik sadrži informacije koje obezbeđuje četiri različita entiteta:</span><span class="sxs-lookup"><span data-stu-id="6ca42-107">A price list includes information that is provided by four different entities:</span></span>

- <span data-ttu-id="6ca42-108">**Cenovnik**: ovaj entitet skladišti informacije o kontekstu, valuti, datumu stupanja na snagu i jedinici vremena za vreme određivanja cena.</span><span class="sxs-lookup"><span data-stu-id="6ca42-108">**Price List**: This entity stores information about context, currency, date effectivity, and time unit for pricing time.</span></span> <span data-ttu-id="6ca42-109">Kontekst prikazuje da li su u cenovniku izražene stope troškova ili prodajne stope.</span><span class="sxs-lookup"><span data-stu-id="6ca42-109">Context shows whether the price list expresses cost rates or sales rates.</span></span> 
- <span data-ttu-id="6ca42-110">**Valuta**: ovaj entitet skladišti valutu cena u cenovniku.</span><span class="sxs-lookup"><span data-stu-id="6ca42-110">**Currency**:  This entity stores the currency of prices on the price list.</span></span> 
- <span data-ttu-id="6ca42-111">**Datum**: ovaj entitet se koristi kada sistem pokuša da unese podrazumevanu cenu za transakciju.</span><span class="sxs-lookup"><span data-stu-id="6ca42-111">**Date**: This entity is used when the system tries to enter a default a price on a transaction.</span></span> <span data-ttu-id="6ca42-112">Izabran je cenovnik sa datumom stupanja na snagu koji obuhvata datum transakcije.</span><span class="sxs-lookup"><span data-stu-id="6ca42-112">A price list that has date effectivity that includes the date of the transaction is selected.</span></span> <span data-ttu-id="6ca42-113">Ako se pronađe više od jednog cenovnika, koji su na snazi na datum transakcije i koji su priloženi sa povezanom ponudom, ugovorom ili organizacionom jedinicom, onda nijedna cena nije podešena kao podrazumevana.</span><span class="sxs-lookup"><span data-stu-id="6ca42-113">If  more than one price list is found that is effective for the transaction date and is attached to the related quote, contract, or organizational unit, then no price is defaulted.</span></span> 
- <span data-ttu-id="6ca42-114">**Vreme**: ovaj entitet skladišti jedinicu vremena za koju su izražene cene, kao što cene po danu ili satu.</span><span class="sxs-lookup"><span data-stu-id="6ca42-114">**Time**: This entity stores the unit of time that prices are expressed for, such as daily or hourly rates.</span></span> 

<span data-ttu-id="6ca42-115">Entitet cenovnika ima tri povezane tabele u kojima se skladište cene:</span><span class="sxs-lookup"><span data-stu-id="6ca42-115">The Price list entity has three related tables that store prices:</span></span>

  - <span data-ttu-id="6ca42-116">**Cena uloge**: ova tabela skladišti cenu za kombinaciju uloge i vrednosti organizacione jedinice i koristi se za podešavanje cena zasnovanih na ulogama za ljudske resurse.</span><span class="sxs-lookup"><span data-stu-id="6ca42-116">**Role Price**: This table stores a rate for a combination of role and organizational unit values and is used to set up role-based prices for human resources.</span></span>
  - <span data-ttu-id="6ca42-117">**Cena kategorije transakcije**: ova tabela skladišti cene po kategoriji transakcije i koristi se za podešavanje cena po kategorijama troškova.</span><span class="sxs-lookup"><span data-stu-id="6ca42-117">**Transaction Category Price**: This table stores prices by transaction category and is used to set up expense category prices.</span></span>
  - <span data-ttu-id="6ca42-118">**Stavka cenovnika**: ova tabela skladišti cene za proizvode u katalogu.</span><span class="sxs-lookup"><span data-stu-id="6ca42-118">**Price List Items**: This table stores prices for catalog products.</span></span>
 
<span data-ttu-id="6ca42-119">Cenovnik je cenovna karta.</span><span class="sxs-lookup"><span data-stu-id="6ca42-119">The price list is a rate card.</span></span> <span data-ttu-id="6ca42-120">Cenovna karta je kombinacija entiteta cenovnika i srodnih redova u tabelama Cena uloge, Cena kategorije transakcije i Stavke cenovnika.</span><span class="sxs-lookup"><span data-stu-id="6ca42-120">A rate card is a combination of the Price List entity and related rows in the Role Price, Transaction Category Price, and Price List Items tables.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="6ca42-121">Uloge resursa</span><span class="sxs-lookup"><span data-stu-id="6ca42-121">Resource roles</span></span>

<span data-ttu-id="6ca42-122">Termin *Uloga resursa* odnosi se na skup veština, kompetencija i certifikacije koje osoba mora imati da bi mogla da obavlja određeni skup zadataka u projektu.</span><span class="sxs-lookup"><span data-stu-id="6ca42-122">The term *resource role* refers to a set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span>

<span data-ttu-id="6ca42-123">Vreme ljudskih resursa se nudi na osnovu uloge koju resurs ima na određenom projektu.</span><span class="sxs-lookup"><span data-stu-id="6ca42-123">Human resources time is quoted based on the role that a resource fills on a specific project.</span></span> <span data-ttu-id="6ca42-124">Za vreme ljudskih resursa, troškovi i naplata se zasnivaju na ulozi resursa.</span><span class="sxs-lookup"><span data-stu-id="6ca42-124">For human resource time, costing and billing is based on resource role.</span></span> <span data-ttu-id="6ca42-125">Vreme može biti izraženo cenom u bilo kojoj jedinici u grupi jedinica **Vreme**.</span><span class="sxs-lookup"><span data-stu-id="6ca42-125">Time can be priced in any unit in the **Time** unit group.</span></span>

<span data-ttu-id="6ca42-126">**Vreme** grupe jedinica kreira se kada instalirate Project Operations.</span><span class="sxs-lookup"><span data-stu-id="6ca42-126">The **Time** unit group is created when you install Project Operations.</span></span> <span data-ttu-id="6ca42-127">Podrazumevana jedinica je **Čas**.</span><span class="sxs-lookup"><span data-stu-id="6ca42-127">It has a default unit of **Hour**.</span></span> <span data-ttu-id="6ca42-128">Ne možete izbrisati, preimenovati niti urediti atribute grupe jedinica **Vreme** niti **Čas**.</span><span class="sxs-lookup"><span data-stu-id="6ca42-128">You can't delete, rename, or edit the attributes fo the **Time** unit group or the **Hour** unit.</span></span> <span data-ttu-id="6ca42-129">Međutim, možete da dodate druge jedinice u grupu jedinica **Vreme**.</span><span class="sxs-lookup"><span data-stu-id="6ca42-129">However, you can add other units to the **Time** unit group.</span></span> <span data-ttu-id="6ca42-130">Ako pokušate da izbrišete grupu jedinica **Vreme** ili jedinicu **Čas**, možete uzrokovati otkazivanja poslovne logike.</span><span class="sxs-lookup"><span data-stu-id="6ca42-130">If you try to delete either the **Time** unit group or the **Hour** unit, you might cause failures in the business logic.</span></span>
 
## <a name="transaction-categories-and-expense-categories"></a><span data-ttu-id="6ca42-131">Kategorije transakcija i troškova</span><span class="sxs-lookup"><span data-stu-id="6ca42-131">Transaction categories and expense categories</span></span>

<span data-ttu-id="6ca42-132">Troškove putovanja i drugi troškovi koje ostvaruju projektni konsultanti se naplaćuju klijentu.</span><span class="sxs-lookup"><span data-stu-id="6ca42-132">Travel and other expenses that project consultants incur are billed to the customer.</span></span> <span data-ttu-id="6ca42-133">Određivanje cena kategorija troškova se završava pomoću cenovnika.</span><span class="sxs-lookup"><span data-stu-id="6ca42-133">Pricing of expense categories is completed by using price lists.</span></span> <span data-ttu-id="6ca42-134">Avionski i hotelski troškovi, kao i troškovi iznajmljivanja automobila su primeri kategorija troškova.</span><span class="sxs-lookup"><span data-stu-id="6ca42-134">Airfare, hotel, and car rental are examples fo expense categories.</span></span> <span data-ttu-id="6ca42-135">Svaka stavka cenovnika za troškove određuje cenu za određenu kategoriju troškova.</span><span class="sxs-lookup"><span data-stu-id="6ca42-135">Each price list line for expenses specifies pricing for a specific expense category.</span></span> <span data-ttu-id="6ca42-136">Sledeće tri metode se koriste za određivanje kategorija troškova:</span><span class="sxs-lookup"><span data-stu-id="6ca42-136">The following three methods are used to price expense categories:</span></span>

- <span data-ttu-id="6ca42-137">**Po ceni**: iznos troškova se naplaćuje klijentu, a provizija se ne naplaćuje.</span><span class="sxs-lookup"><span data-stu-id="6ca42-137">**At cost**: The expense cost is billed to the customer, and no markup is applied.</span></span>
- <span data-ttu-id="6ca42-138">**Procenat provizije**: procenat u odnosu na stvarnu vrednost troškova se naplaćuje klijentu.</span><span class="sxs-lookup"><span data-stu-id="6ca42-138">**Markup percentage**: The percentage over the actual cost is billed to the customer.</span></span> 
- <span data-ttu-id="6ca42-139">**Cena po jedinici**: cena naplate se podešava za svaku jedinicu kategorije troškova.</span><span class="sxs-lookup"><span data-stu-id="6ca42-139">**Price per unit**: A billing price is set for each unit of the expense category.</span></span> <span data-ttu-id="6ca42-140">Iznos koji se naplaćuje klijentu se izračunava na osnovu broja jedinica troškova koje konsultant prijavi.</span><span class="sxs-lookup"><span data-stu-id="6ca42-140">The amount that is billed ot the customer is calculated based on the number of expense units that the consultant reports.</span></span> <span data-ttu-id="6ca42-141">Kilometraža koristi metod određivanja cena po jedinici.</span><span class="sxs-lookup"><span data-stu-id="6ca42-141">Mileage uses the price-per-unit pricing method.</span></span> <span data-ttu-id="6ca42-142">Na primer, kategorija troškova za kilometražu može se konfigurisati za 30 američkih dolara (USD) dnevno ili 2 USD po milji.</span><span class="sxs-lookup"><span data-stu-id="6ca42-142">For example, the mileage expense category can be configured for 30 US dollars (USD) per day or 2 USD per mile.</span></span> <span data-ttu-id="6ca42-143">Kada konsultant prijavi kilometražu za projekat, taj iznos za naplatu se izračunava na osnovu broja milja koji je prijavio konsultant.</span><span class="sxs-lookup"><span data-stu-id="6ca42-143">When a consultant reports mileage on a project, the amount to bill is calculated based on the number of miles that the consultant reported.</span></span>
 
## <a name="project-sales-pricing-and-overrides"></a><span data-ttu-id="6ca42-144">Formiranje cena i njihova zamena za prodaju u okviru projekta</span><span class="sxs-lookup"><span data-stu-id="6ca42-144">Project sales pricing and overrides</span></span>

<span data-ttu-id="6ca42-145">Za projektne ponude i ugovore, cenovnik projekta ima različit obrazac za zamenu cena u odnosu na cenovnik proizvoda.</span><span class="sxs-lookup"><span data-stu-id="6ca42-145">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="6ca42-146">U stavci ponude zasnovanoj na katalogu proizvoda možete da zamenite cenu za uloge i kategorije direktno u stavci ponude, jer svaka stavka ponude ukazuje na tačno jednu stavku kataloga.</span><span class="sxs-lookup"><span data-stu-id="6ca42-146">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="6ca42-147">Međutim, u stavci ponude zasnovanoj na projektu ne možete da zamenite cenu za uloge i kategorije direktno u stavci ponude.</span><span class="sxs-lookup"><span data-stu-id="6ca42-147">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="6ca42-148">Koristite cenovnik projekta da biste podržali dva različita obrasca zamene.</span><span class="sxs-lookup"><span data-stu-id="6ca42-148">Use the project price list to support the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="6ca42-149">Preporučujemo da imate poseban cenovnik za resurse projekta i stavke kataloga, zbog razlika u ponašanju između njih kada zamenite cene.</span><span class="sxs-lookup"><span data-stu-id="6ca42-149">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="6ca42-150">Svaki od sledećih entiteta može imati jednu ili više pridruženih cenovnika prodaje za cenu projekata:</span><span class="sxs-lookup"><span data-stu-id="6ca42-150">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="6ca42-151">Klijent (poslovni kontakt)</span><span class="sxs-lookup"><span data-stu-id="6ca42-151">Customer (account)</span></span> 
- <span data-ttu-id="6ca42-152">Mogućnost za poslovanje</span><span class="sxs-lookup"><span data-stu-id="6ca42-152">Opportunity</span></span> 
- <span data-ttu-id="6ca42-153">Ponuda</span><span class="sxs-lookup"><span data-stu-id="6ca42-153">Quote</span></span> 
- <span data-ttu-id="6ca42-154">Ugovor za projekat</span><span class="sxs-lookup"><span data-stu-id="6ca42-154">Project Contract</span></span>

<span data-ttu-id="6ca42-155">Povezivanje ovih entiteta sa cenovnikom je naznačeno cenovnikom projekta.</span><span class="sxs-lookup"><span data-stu-id="6ca42-155">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="6ca42-156">Možete da povežete neke cenovnike sa entitetima prodaje Klijent, Mogućnost za poslovanje, Ponuda i Ugovor o projektu.</span><span class="sxs-lookup"><span data-stu-id="6ca42-156">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="6ca42-157">Podrazumevani cenovnik projekta se ne unosi automatski u zapis klijenta.</span><span class="sxs-lookup"><span data-stu-id="6ca42-157">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="6ca42-158">Međutim, cenovnik projekta možete ručno priložiti zapisu klijenta.</span><span class="sxs-lookup"><span data-stu-id="6ca42-158">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="6ca42-159">Ipak, trebalo bi ručno da priložite cenovnik projekta samo kada imate prilagođeni ugovor o određivanju cena sa klijentom.</span><span class="sxs-lookup"><span data-stu-id="6ca42-159">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="6ca42-160">Kada je cenovnik projekta priložen entitetu prodaje, proveravaju se sledeće informacije:</span><span class="sxs-lookup"><span data-stu-id="6ca42-160">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="6ca42-161">Da li cenovnik ima kontekst **prodaje**.</span><span class="sxs-lookup"><span data-stu-id="6ca42-161">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="6ca42-162">Da li se valuta cenovnika podudara sa valutom klijenta.</span><span class="sxs-lookup"><span data-stu-id="6ca42-162">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="6ca42-163">U ugovoru o projektu, koristi sledeći redosled prioriteta da bi automatski podesio povezane cenovnike projekta:</span><span class="sxs-lookup"><span data-stu-id="6ca42-163">On a project contract, the following order of precedence to automatically set related project price lists:</span></span>

1. <span data-ttu-id="6ca42-164">Ponuda</span><span class="sxs-lookup"><span data-stu-id="6ca42-164">Quote</span></span>
2. <span data-ttu-id="6ca42-165">Mogućnost za poslovanje</span><span class="sxs-lookup"><span data-stu-id="6ca42-165">Opportunity</span></span>
3. <span data-ttu-id="6ca42-166">Klijent</span><span class="sxs-lookup"><span data-stu-id="6ca42-166">Customer</span></span> 
4. <span data-ttu-id="6ca42-167">Globalna podešavanja</span><span class="sxs-lookup"><span data-stu-id="6ca42-167">Global settings</span></span> 

<span data-ttu-id="6ca42-168">Kada se cenovnik projekta unese podrazumevano, sistem proverava da li se valuta podudara sa valutom klijenta i da li podrazumevani cenovnici koji su uneti imaju kontekst **prodaje**.</span><span class="sxs-lookup"><span data-stu-id="6ca42-168">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="6ca42-169">Možete da povežete više cenovnika projekta sa entitetima Klijent, Mogućnost za poslovanje, Ponuda i Ugovor o projektu.</span><span class="sxs-lookup"><span data-stu-id="6ca42-169">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="6ca42-170">Ova mogućnost podržava podrazumevane cene za određeni datum za dugoročni ugovor o projektu, gde možete da zahtevate više od jednog cenovnika kako biste u obzir uzeli izmene cena do kojih dolazi zbog inflacije.</span><span class="sxs-lookup"><span data-stu-id="6ca42-170">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="6ca42-171">Međutim, ako se za cenovnike koje povežete sa entitetom Klijent, Mogućnost za poslovanje, Ponuda ili Ugovor o projektu preklapaju datumi stupanja na snagu, podrazumevane cene mogu biti netačne.</span><span class="sxs-lookup"><span data-stu-id="6ca42-171">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="6ca42-172">Zbog toga bi trebalo da proverite da cenovnici projekata sa datumima stupanja na snagu koji se preklapaju nisu povezani sa tim entitetima.</span><span class="sxs-lookup"><span data-stu-id="6ca42-172">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>

### <a name="deal-specific-price-overrides"></a><span data-ttu-id="6ca42-173">Zamene cena za određenu pogodbu</span><span class="sxs-lookup"><span data-stu-id="6ca42-173">Deal-specific price overrides</span></span>

<span data-ttu-id="6ca42-174">Možete kreirati zamene cena za određenu pogodbu za željene cene u cenovnicima projekata koje se podrazumevano unose za ponudu ili ugovor o projektu.</span><span class="sxs-lookup"><span data-stu-id="6ca42-174">You can create deal-specific overrides for selected prices on project price lists that are entered by default on a quote or project contract.</span></span>

<span data-ttu-id="6ca42-175">Ugovor o projektu uvek podrazumevano dobija kopiju glavnog cenovnika prodaje umesto direktne veze do njega.</span><span class="sxs-lookup"><span data-stu-id="6ca42-175">By default, a project contract always gets a copy of the master sales price list instead of a direct link to it.</span></span> <span data-ttu-id="6ca42-176">Ovo ponašanje garantuje da se sporazumi o cenama koji su napravljeni sa klijentom za izjave o radu ne menjaju ako se promeni glavni cenovnik.</span><span class="sxs-lookup"><span data-stu-id="6ca42-176">This behavior helps guarantee that price agreements that are made with a customer for a statement of work (SOW) don't change if the master price list is changed.</span></span>

<span data-ttu-id="6ca42-177">Međutim, u ponudi možete koristiti glavni cenovnik.</span><span class="sxs-lookup"><span data-stu-id="6ca42-177">However, on a quote, you can use a master price list.</span></span> <span data-ttu-id="6ca42-178">Druga mogućnost je da kopirate glavni cenovnik i uredite ga tako da kreirate prilagođeni cenovnik koji se primenjuje samo na tu ponudu.</span><span class="sxs-lookup"><span data-stu-id="6ca42-178">Alternatively, you can copy a master price list and edit it to create a custom price list that applies only to that quote.</span></span> <span data-ttu-id="6ca42-179">Da biste kreirali novi cenovnik koji je specifičan za ponudu, na stranici **Ponuda** izaberite **Kreiraj prilagođene cene**.</span><span class="sxs-lookup"><span data-stu-id="6ca42-179">To create a new price list that is specific to a quote, on the **Quote** page, select **Create custom pricing**.</span></span> <span data-ttu-id="6ca42-180">Cenovniku projekta specifičan za pogodbu možete da pristupite samo iz ponude.</span><span class="sxs-lookup"><span data-stu-id="6ca42-180">You can access the deal-specific project price list only from the quote.</span></span> 

<span data-ttu-id="6ca42-181">Kada kreirate prilagođeni cenovnik projekta, biće kopirane samo komponente projekta cenovnika.</span><span class="sxs-lookup"><span data-stu-id="6ca42-181">When you create a custom project price list, only the project components of the price list are copied.</span></span> <span data-ttu-id="6ca42-182">Drugim rečima, novi cenovnik kreiran kao kopija postojećeg cenovnika projekta koji je priložen uz ponudu i ovaj novi cenovnik imaju samo povezane cene uloga i cene kategorija transakcija.</span><span class="sxs-lookup"><span data-stu-id="6ca42-182">In other words, a new price list created as a copy of the existing project price list that is attached on the quote, and this new price list has only related role prices and transaction category prices.</span></span>
  
## <a name="tracking-costs"></a><span data-ttu-id="6ca42-183">Praćenje troškova</span><span class="sxs-lookup"><span data-stu-id="6ca42-183">Tracking costs</span></span>

<span data-ttu-id="6ca42-184">Project Operations prati troškove korišćenja vremena ljudskih resursa za projekte.</span><span class="sxs-lookup"><span data-stu-id="6ca42-184">Project Operations tracks costs for the use of human resource time on projects.</span></span> <span data-ttu-id="6ca42-185">Takođe prati druge troškove koji su ostvareni u toku projekta, kao što su putni troškovi.</span><span class="sxs-lookup"><span data-stu-id="6ca42-185">It also tracks costs for other expenses that are incurred during the project, such as travel expenses.</span></span>

<span data-ttu-id="6ca42-186">Kao i kod stopa naplate, stope troškova za ljudske resurse se takođe podešavaju korišćenjem cenovnika.</span><span class="sxs-lookup"><span data-stu-id="6ca42-186">Like bill rates, cost rates for human resources are also set up using price lists.</span></span> <span data-ttu-id="6ca42-187">Evo glavnih razlika u ponašanju cenovnika troškova i cenovnika prodaje:</span><span class="sxs-lookup"><span data-stu-id="6ca42-187">Here are the main differences in the behavior of the cost price list and sales price list:</span></span>

- <span data-ttu-id="6ca42-188">Stopa troškova resursa se ne može zameniti za određeni projekat, ugovor ili ponudu.</span><span class="sxs-lookup"><span data-stu-id="6ca42-188">The cost rate of a resource can’t be overridden on a specific project, contract, or quote.</span></span> <span data-ttu-id="6ca42-189">Međutim, stope naplate mogu se zameniti na osnovu pogodbe, ukoliko dođe do izmena specifičnih za prirodu pogodbe.</span><span class="sxs-lookup"><span data-stu-id="6ca42-189">However, bill rates can be overridden on a per-deal basis if changes are made that are specific to the nature of the deal.</span></span> 

- <span data-ttu-id="6ca42-190">Sledeća porudžbina se koristi za rešavanje problema sa cenovnikom troškova:</span><span class="sxs-lookup"><span data-stu-id="6ca42-190">The following order is used to resolve a cost price list:</span></span>

    1. <span data-ttu-id="6ca42-191">Cenovnik troškova koji je priložen organizacionoj jedinici.</span><span class="sxs-lookup"><span data-stu-id="6ca42-191">The cost price list that is attached to the organizational unit.</span></span>
    2. <span data-ttu-id="6ca42-192">Cenovnik troškova koji je priložen Project Operations parametrima.</span><span class="sxs-lookup"><span data-stu-id="6ca42-192">The cost price list that is attached to the Project Operations parameters.</span></span> <span data-ttu-id="6ca42-193">S obzirom na to da se cenovnici troškova u mnogim različitim valutama mogu priložiti uz parametre, završava se podudaranje valute ugovorne organizacione jedinice projekta, ugovora ili ponude sa valutom cenovnika troškova.</span><span class="sxs-lookup"><span data-stu-id="6ca42-193">Because cost price lists in many different currencies can be attached to the parameters, a currency match is completed between the currency of the contracting organizational unit of the project, contract, or quote, and the currency of the cost price list.</span></span>
    3. <span data-ttu-id="6ca42-194">Kada su u pitanju troškovi, metodi formiranja cena „Provizija preko troškova“ i „Po ceni“ ne primenjuju se na cenovnike troškova.</span><span class="sxs-lookup"><span data-stu-id="6ca42-194">For expenses, the at-cost and markup-over-cost pricing methods don’t apply to cost price lists.</span></span> <span data-ttu-id="6ca42-195">Čak i ako se ovi metodi određivanja cena koriste u stavkama cenovnika troškova da bi se podesili troškovi za kategoriju transakcije, sistem ih zanemaruje i ne unosi se podrazumevana cena koštanja.</span><span class="sxs-lookup"><span data-stu-id="6ca42-195">Even if these pricing methods are used on cost price list lines to set up transaction category costs, the system ignores them, and no default cost price is entered.</span></span>