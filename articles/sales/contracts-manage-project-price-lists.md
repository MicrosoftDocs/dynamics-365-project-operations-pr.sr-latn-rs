---
title: Upravljanje cenovnicima projekata u ugovorima za projekat
description: Ova tema pruža informacije o upravljanju cenovnicima za projekat na ugovorima za projekat.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2cfac6eda64d1d8e578115bba07942a7d786328f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278615"
---
# <a name="manage-project-price-lists-on-project-contracts"></a><span data-ttu-id="8d9c8-103">Upravljanje cenovnicima projekata u ugovorima za projekat</span><span class="sxs-lookup"><span data-stu-id="8d9c8-103">Manage project price lists on project contracts</span></span>

<span data-ttu-id="8d9c8-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="8d9c8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8d9c8-105">Ugovori za projekat u usluzi Dynamics 365 Project Operations osmišljeni su tako da podržavaju više efektivnih prodajnih cenovnika na ugovoru.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-105">Project contracts in Dynamics 365 Project Operations are designed to support multiple date effective sales price lists on a contract.</span></span> <span data-ttu-id="8d9c8-106">U usluzi Project Operations postoji novi pridruženi entitet koji se zove **Cenovnici projekta**.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-106">In Project Operations, there is a new associated entity called **Project Price Lists**.</span></span> <span data-ttu-id="8d9c8-107">Taj entitet ima relaciju „jedan prema više“ sa ugovorom za projekat.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-107">This entity has a one-to-many relationship to a project contract.</span></span>

<span data-ttu-id="8d9c8-108">Cenovnici projekata se koriste za određivanje transakcija vremena i troškova na projektu.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-108">Project price lists are used to price time and expense transactions on a project.</span></span> <span data-ttu-id="8d9c8-109">Kada ugovor ima jedan ili više cenovnika projekata, ovi cenovnici se koriste za određivanje cene za stavke vremena i troškova, kao i za trenutno stanje na projektima koji su povezani sa ugovorom preko predmeta ugovora.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-109">When a contract has one or more project price lists, these price lists are used to price for time and expense estimates and actuals on projects that are associated to the contract through the contract line.</span></span>

<span data-ttu-id="8d9c8-110">Kada u ugovoru za projekat ne postoje cenovnici projekta, videćete poruku upozorenja da ne postoje cenovnici projekta, pa cene za vaše procene, stvarni rad na projektu i troškove neće biti određene.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-110">When there are no project price lists on a project contract, you will see a warning message that there are no project price lists and your estimates, actual project work, and expenses will not be priced.</span></span> <span data-ttu-id="8d9c8-111">Neće biti navedene vrednosti cena prodaje.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-111">There will be no price for sales values.</span></span>

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a><span data-ttu-id="8d9c8-112">Povezivanje ili prekidanje veze cenovnika projekta na ugovoru o projektu</span><span class="sxs-lookup"><span data-stu-id="8d9c8-112">Associate or unassociate a project price list on a project contract</span></span>

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-and-expenses"></a><span data-ttu-id="8d9c8-113">Napravite ili pridružite određeni cenovnik za procenu rada i troškova zasnovanih na projektu</span><span class="sxs-lookup"><span data-stu-id="8d9c8-113">Create or associate a specific price list for estimating project-based work and expenses</span></span>

1. <span data-ttu-id="8d9c8-114">U ugovoru za projekat, izaberite karticu **Cenovnici projekta**.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-114">On the project contract, select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="8d9c8-115">U podformi izaberite **+ Dodaj novi cenovnik projekta**.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-115">In the subgrid, select **+ Add New Project Price List**.</span></span>
3. <span data-ttu-id="8d9c8-116">Na klizaču **Brzo kreiranje**, izaberite cenovnik.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-116">On the **Quick Create** slider, select a price list.</span></span> 

  <span data-ttu-id="8d9c8-117">Padajuća lista prikazuje sve cenovnike kojima je kontekst postavljen na **Prodaja**, pri čemu se valuta na cenovniku podudara sa valutom iz ugovora.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-117">The drop-down list shows all price lists that have the context set to **Sales**, where the currency on the price list matches the currency on the contract.</span></span>
  
4. <span data-ttu-id="8d9c8-118">Unesite opis veze sa cenovnikom projekta, izaberite **Sačuvaj**, a zatim zatvorite klizač **Brzo kreiranje**.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-118">Enter a description for the project price list association, select **Save**, and then close the **Quick Create** slider.</span></span>

   <span data-ttu-id="8d9c8-119">Povezivanje cenovnika projekta je kreirano.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-119">A project price list association is created.</span></span>
   
5. <span data-ttu-id="8d9c8-120">Ponovite korake 1-4 da biste ugovoru za projekat pridružili više od jednog cenovnika projekta.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-120">Repeat steps 1-4 to associate more than one project price list to the project contract.</span></span> <span data-ttu-id="8d9c8-121">Više cenovnika projekta kreirajte samo ako imate različitu efektivnost datuma na svakom povezanom cenovniku projekta.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-121">Only create multiple project price lists if you have different date effectivity on each of the associated project price list.</span></span>

> [!NOTE]
> <span data-ttu-id="8d9c8-122">Project Operations ne podržava preklapanje datumske efektivnosti cenovnika projekta.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-122">Project Operations doesn't support overlapping the date effectivity of the project price lists.</span></span> <span data-ttu-id="8d9c8-123">Ako postoji više cenovnika projekta za transakciju sa datim datumom, cena te transakcije biće podrazumevano postavljena na nulu.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-123">If there are multiple project prices lists for a transaction with a given date, the price on that transaction will be defaulted to zero.</span></span>

### <a name="remove-a-project-price-list-association"></a><span data-ttu-id="8d9c8-124">Uklanjanje veze cenovnika projekta</span><span class="sxs-lookup"><span data-stu-id="8d9c8-124">Remove a project price list association</span></span>

- <span data-ttu-id="8d9c8-125">Izaberite cenovnik projekta, a zatim izaberite **Izbriši cenovnik ugovora za projekat** na podformi.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-125">Select the project price list, and then select **Delete Contract Project Price List** on the subgrid.</span></span> 

  <span data-ttu-id="8d9c8-126">Cenovnik se uklanja iz cenovnika projekta na ugovoru.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-126">The price list is removed from the project price lists on the contract.</span></span> <span data-ttu-id="8d9c8-127">Sam cenovnik neće biti izbrisan.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-127">The price list itself will not be deleted.</span></span> <span data-ttu-id="8d9c8-128">Biće izbrisana samo veza sa ugovorom.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-128">Only the association to the contract will be deleted.</span></span>

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a><span data-ttu-id="8d9c8-129">Podešavanje automatskog postavljanja cenovnika projekta na ugovoru</span><span class="sxs-lookup"><span data-stu-id="8d9c8-129">Set up automatic defaulting of project price lists on a contract</span></span>

<span data-ttu-id="8d9c8-130">Cenovnik projekta se može postaviti kao podrazumevana lista na ugovoru za projekat.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-130">A project price list can be set up as the default list on a project contract.</span></span> <span data-ttu-id="8d9c8-131">Ovo podešavanje može da pomogne da svi ugovori u vašoj organizaciji uvek započinju standardnim cenovnikom za taj cenovni period.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-131">This setup can help ensure that all contracts in your organization always start with a standard price list for that price period.</span></span>

### <a name="set-up-the-organizational-default-for-project-price-lists"></a><span data-ttu-id="8d9c8-132">Podešavanje organizacionog postavljanja za cenovnike projekta</span><span class="sxs-lookup"><span data-stu-id="8d9c8-132">Set up the organizational default for project price lists</span></span>

1. <span data-ttu-id="8d9c8-133">Idite na **Podešavanja** > **Opšti podaci**, a zatim izaberite **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-133">Go to **Settings** > **General**, and then select **Parameters**.</span></span>
2. <span data-ttu-id="8d9c8-134">Na stranici liste **Aktivni parametri**, izaberite i dvaput kliknite na zapis da biste ga otvorili.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-134">In the **Active Parameters** list page, select and double-click the record to open it.</span></span> <span data-ttu-id="8d9c8-135">Dok dvaput kliknete, pazite da ne kliknete na vrednost polja koja je hiperveza.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-135">While double–clicking, make sure that you are not clicking on a field value that is hyperlink.</span></span> 
3. <span data-ttu-id="8d9c8-136">Na stranici **Aktivni parametri**, izaberite karticu **Cenovnik**. Podforma prikazuje listu zadatih cenovnika.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-136">On the **Active Parameters** page, select the **Price List** tab. A subgrid shows a list of default price lists.</span></span> <span data-ttu-id="8d9c8-137">Ovo je lista standardnih troškova i prodajnih cenovnika.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-137">This is a list of standard cost and sales price lists.</span></span> <span data-ttu-id="8d9c8-138">Ako imate cenovnik **prodaje** koji je ovde povezan za svaku valutu u kojoj prodajete, to obezbeđuje da cenovnik prodaje bude podrazumevan za bilo koji ugovor koji kreirate za klijente koji obavljaju transakcije u toj valuti.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-138">Having a **Sales** price list associated here for every currency that you sell in ensures that the sales price list is the default on any contract that you create for customers that transact in this currency.</span></span>

### <a name="set-up-a-customer-specific-project-price-list"></a><span data-ttu-id="8d9c8-139">Podešavanje cenovnika projekta specifičnog za klijenta</span><span class="sxs-lookup"><span data-stu-id="8d9c8-139">Set up a customer-specific project price list</span></span>

<span data-ttu-id="8d9c8-140">Takođe možete da podesite cenovnike projekta specifične za klijenta kada uspostavite glavni ugovor o cenama sa svojim klijentima.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-140">You can also set up customer–specific project price lists when you have negotiated a master pricing agreement with your customers.</span></span>

1. <span data-ttu-id="8d9c8-141">Idite na stavku **Prodaja** > **Klijenti**.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-141">Go to **Sales** > **Customers**.</span></span>
2. <span data-ttu-id="8d9c8-142">Sa liste aktivnih naloga izaberite klijenta za kojeg imate poseban cenovnik.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-142">From the list of active accounts, select the customer for whom have special price list.</span></span>
3. <span data-ttu-id="8d9c8-143">Izaberite zapis klijenta da biste ga otvorili, a zatim izaberite karticu **Cenovnici projekta**. Podforma prikazuje listu cenovnika projekata specifičnih za ovog klijenta.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-143">Select the customer record to open it and then select the **Project Price Lists** tab. A subgrid shows a list of project price lists specific to this customer.</span></span> 
4. <span data-ttu-id="8d9c8-144">Kreirajte novu vezu cenovnika ovde da biste dobili cenovnik projekta specifičan za ovog klijenta.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-144">Create a new price list association here to have project price list specific to this customer.</span></span>

## <a name="custom-pricing-on-a-project-contract"></a><span data-ttu-id="8d9c8-145">Prilagođeno određivanje cena na ugovoru za projekat</span><span class="sxs-lookup"><span data-stu-id="8d9c8-145">Custom pricing on a project contract</span></span>

<span data-ttu-id="8d9c8-146">Kada uspostavite organizacione i podrazumevane cenovnike projekta specifične za vaše klijente, automatski vaši ugovori za projekat će se automatski kreirati sa vezama na cenovnike projekta.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-146">After you have organizational and customer-specific default project price lists, your project contracts will be created with these project price list associations automatically.</span></span> <span data-ttu-id="8d9c8-147">Međutim, cenovnici projekta na ugovoru o projektu se uvek kopiraju sa datumom i nazivom ugovora koji im je dodat.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-147">However, project price lists on a project contract are always copied with the date and contract name appended to them.</span></span> <span data-ttu-id="8d9c8-148">Menadžeri naloga i projekata mogu tada započeti uređivanje cena na ovim primercima.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-148">The account and project managers can then begin making edits to prices on these copies.</span></span> <span data-ttu-id="8d9c8-149">Ove promenjene cene će se primenjivati samo na ovaj ugovor za projekat.</span><span class="sxs-lookup"><span data-stu-id="8d9c8-149">These changed prices will be applicable to this project contract only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]