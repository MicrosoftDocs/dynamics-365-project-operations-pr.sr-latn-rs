---
title: Kako prilagođavate tok poslovnog procesa za faze projekta?
description: Pregled načina prilagođavanja toka poslovnog procesa za faze projekta.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2dccc33088cd9e49e7ffe609f9d9754ef33a5dba
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083766"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="8460f-103">Kako prilagođavate tok poslovnog procesa za faze projekta?</span><span class="sxs-lookup"><span data-stu-id="8460f-103">How do I customize the Project Stages business process flow?</span></span>
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="8460f-104">Postoji poznato ograničenje u ranijim verzijama aplikacije Project Service da imena faza u toku poslovnog procesa za faze projekta moraju biti potpuno ista sa očekivanim engleskim imenima ( **Quote** , **Plan** , **Close** ).</span><span class="sxs-lookup"><span data-stu-id="8460f-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names ( **Quote** , **Plan** , **Close** ).</span></span> <span data-ttu-id="8460f-105">U suprotnom, poslovna logika, koja se oslanja na englesko ime faze, ne radi kako je očekivano.</span><span class="sxs-lookup"><span data-stu-id="8460f-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="8460f-106">Zato ne vidite da su poznate radnje, kao što su **Prebaci proces** ili **Uredi proces** dostupne u obrascu projekta, a prilagođavanje toka poslovnog procesa se ne podstiče.</span><span class="sxs-lookup"><span data-stu-id="8460f-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="8460f-107">Ovo ograničenje je otklonjeno u verziji 2.4.5.48 i novijim.</span><span class="sxs-lookup"><span data-stu-id="8460f-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="8460f-108">U ovom članku data su predložena zaobilazna rešenja ukoliko morate da prilagodite podrazumevani tok poslovnog procesa za starije verzije.</span><span class="sxs-lookup"><span data-stu-id="8460f-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="8460f-109">Poslovna logika zahteva potpuno podudaranje sa engleskim imenima faze</span><span class="sxs-lookup"><span data-stu-id="8460f-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="8460f-110">Tok poslovnog procesa za faze projekta sadrži poslovnu logiku koja upravlja sledećim ponašanjima u aplikaciji:</span><span class="sxs-lookup"><span data-stu-id="8460f-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="8460f-111">Kada je projekat povezan sa ponudom, kôd postavlja tok poslovnog procesa na fazu **Quote**.</span><span class="sxs-lookup"><span data-stu-id="8460f-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="8460f-112">Kada je projekat povezan sa kontaktom, kôd postavlja tok poslovnog procesa na fazu **Plan**.</span><span class="sxs-lookup"><span data-stu-id="8460f-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="8460f-113">Kada je tok poslovnog procesa napredovao do faze **Close** , zapis projekat se deaktivira.</span><span class="sxs-lookup"><span data-stu-id="8460f-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="8460f-114">Kada je projekat deaktiviran, obrazac projekta i strukturna analiza posla (SAP) su podešeni na samo za čitanje, rezervacije imenovanog resursa se ukidaju i svi povezani cenovnici se deaktiviraju.</span><span class="sxs-lookup"><span data-stu-id="8460f-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="8460f-115">Ova poslovna logika se oslanja imena na engleskom jeziku za faze projekta.</span><span class="sxs-lookup"><span data-stu-id="8460f-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="8460f-116">Ova zavisnost od imena na engleskom jeziku predstavlja glavni razlog zašto se ne podstiče prilagođavanje toka poslovnog procesa za faze projekta, kao i zašto ne vidite uobičajene radnje toka poslovnog procesa kao što su **Prebaci proces** ili **Uredi proces** u entitetu Projekat.</span><span class="sxs-lookup"><span data-stu-id="8460f-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="8460f-117">Šta se događa ako se imena faza ne podudaraju sa imenima na engleskom?</span><span class="sxs-lookup"><span data-stu-id="8460f-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="8460f-118">U aplikaciji Project Service, verzija 1.x na platformi 8.2, kada se imena faza u toku poslovnog procesa ne podudaraju tačno sa engleskim imenima za faze, preskače se poslovna logika koja podešava pravi fazu za ponude ili ugovore ili koja zatvara projekat.</span><span class="sxs-lookup"><span data-stu-id="8460f-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="8460f-119">Neće se prikazivati poruke o grešci.</span><span class="sxs-lookup"><span data-stu-id="8460f-119">No error messages are displayed.</span></span> <span data-ttu-id="8460f-120">Zbog toga deluje da možete da prilagodite tok poslovnog procesa za faze projekta.</span><span class="sxs-lookup"><span data-stu-id="8460f-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="8460f-121">Međutim, nećete videti da ijedan automatski proces funkcioniše za ponude, ugovore i zatvaranje projekta.</span><span class="sxs-lookup"><span data-stu-id="8460f-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="8460f-122">U aplikaciji Project Service, verzija 2.4.4.30 ili ranija na platformi 9.0, došlo je do značajne arhitektonske promene tokova poslovnih procesa, što je zahtevalo ponovno pisanje poslovne logike toka poslovnog procesa.</span><span class="sxs-lookup"><span data-stu-id="8460f-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="8460f-123">Kao posledica toga, ako se imena faze procesa ne podudaraju sa očekivanim imenima na engleskom jeziku, primićete poruku o grešci.</span><span class="sxs-lookup"><span data-stu-id="8460f-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="8460f-124">Stoga, ako želite da prilagodite tok poslovnog procesa za faze projekta za entitet projekta, možete samo da dodate potpuno nove faze u podrazumevani tok poslovnog procesa za entitet projekta zadržavajući faze **Ponuda** , **Plan** i **Zatvori** nepromenjene.</span><span class="sxs-lookup"><span data-stu-id="8460f-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote** , **Plan** , and **Close** stages as-is.</span></span> <span data-ttu-id="8460f-125">Ovo ograničenje osigurava da ne dobijate greške od poslovne logike koja očekuje imena na engleskom jeziku u toku poslovnog procesa.</span><span class="sxs-lookup"><span data-stu-id="8460f-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="8460f-126">U verziji 2.4.5.48 ili novijoj, poslovna logika opisana u ovom članku je uklonjena iz podrazumevanog toka poslovnog procesa za entitet projekta.</span><span class="sxs-lookup"><span data-stu-id="8460f-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="8460f-127">Nadogradnja na tu verziju ili kasniju će vam omogućiti da prilagodite ili zamenite podrazumevani tok poslovnog procesa sopstvenim.</span><span class="sxs-lookup"><span data-stu-id="8460f-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="8460f-128">Zaobilazna rešenja za ranije verzije</span><span class="sxs-lookup"><span data-stu-id="8460f-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="8460f-129">Ako nadogradnja ne predstavlja opciju, možete da prilagodite tok poslovnog procesa za faze projekta za entitet projekta na jedan od ova dva načina:</span><span class="sxs-lookup"><span data-stu-id="8460f-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="8460f-130">Dodajte dodatne faze podrazumevanoj konfiguraciji istovremeno zadržavajući engleska imena faza za opcije **Quote** , **Plan** i **Close**.</span><span class="sxs-lookup"><span data-stu-id="8460f-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote** , **Plan** , and **Close**.</span></span>


![Snimak ekrana za dodavanje faza podrazumevanoj konfiguraciji](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="8460f-132">Kreirajte sopstveni tok poslovnog procesa i neka on bude vaš primarni tok poslovnog procesa za entitet projekta, što vam omogućava da imate bilo koja imena faze po želji.</span><span class="sxs-lookup"><span data-stu-id="8460f-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="8460f-133">Međutim, ako želite da koristite iste standardne faze projekta **Quote** , **Plan** i **Close** , potrebno je da izvršite još neka prilagođavanja koja se pokreću na osnovu vaših prilagođenih imena za faze.</span><span class="sxs-lookup"><span data-stu-id="8460f-133">However, if you want to use the same standard project stages **Quote** , **Plan** , and **Close** , you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="8460f-134">Složenija logika se nalazi u zatvaranju projekta, koju i dalje možete da pokrećete prostim deaktiviranjem zapisa projekta.</span><span class="sxs-lookup"><span data-stu-id="8460f-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![BPF prilagođavanje](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="8460f-136">Dodatna razmatranja za aplikaciju Project Service, verzija 2.4.4.30 ili ranije na platformi 9.0</span><span class="sxs-lookup"><span data-stu-id="8460f-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="8460f-137">U aplikaciji Project Service 2.4.4.30 ili ranijoj na platformi 9.0, sa prilagođenim tokom poslovnog procesa, polje **Ime faze** u entitetu Projekat kojeg koristi grafikon **Projekata prema fazi** i prikaz liste projekta se neće ispravljati, jer su povezani sa tokom poslovnog procesa za podrazumevane faze projekta.</span><span class="sxs-lookup"><span data-stu-id="8460f-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="8460f-138">Ovaj problem možete da rešite sa sledećim koracima:</span><span class="sxs-lookup"><span data-stu-id="8460f-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="8460f-139">Dodajte prilagođeno polje da biste pribeležili trenutnu fazu toka poslovnog procesa koja se ažurira kako korisnik prilazi kroz prilagođeni tok poslovnog procesa.</span><span class="sxs-lookup"><span data-stu-id="8460f-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="8460f-140">Izmenite grafikon **Projekat prema fazi** kako biste radili sa prilagođenim poljem umesto sa podrazumevanom konfiguracijom.</span><span class="sxs-lookup"><span data-stu-id="8460f-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="8460f-141">Koraci za kreiranje sopstvenog toka poslovnog procesa za entitet projekta</span><span class="sxs-lookup"><span data-stu-id="8460f-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="8460f-142">Postupite na sledeći način da biste kreirali sopstveni tok poslovnog procesa za entitet projekta:</span><span class="sxs-lookup"><span data-stu-id="8460f-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="8460f-143">Idite na stavku **Podešavanja** > **Centar za procese**.</span><span class="sxs-lookup"><span data-stu-id="8460f-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="8460f-144">Nemojte da kopirate tok poslovnog projekta za faze projekta jer to kopira i poslovnu logiku aplikacije Project Service.</span><span class="sxs-lookup"><span data-stu-id="8460f-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![Kreiraj proces](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="8460f-146">Koristite dizajner procesa za kreiranje željenih imena za faze.</span><span class="sxs-lookup"><span data-stu-id="8460f-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="8460f-147">Ako želite istu funkcionalnost kao podrazumevane faze za stavke **Quote** , **Plan** i **Close** , moraćete da je kreirate na osnovu imena za faze prilagođenog toka poslovnog procesa.</span><span class="sxs-lookup"><span data-stu-id="8460f-147">If you want the same functionality as the default stages for **Quote** , **Plan** , and **Close** , you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![Snimak ekrana dizajnera procesa koji se koristi za prilagođavanje BPF](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="8460f-149">U dizajneru procesa, kliknite na stavku **Redosled toka procesa** kako bi prilagođeni tok poslovnog procesa postao primarni tok poslovnog procesa za entitet projekta njegovim premeštanjem iznad toka poslovnog procesa za faze projekta na vrh liste.</span><span class="sxs-lookup"><span data-stu-id="8460f-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="8460f-150">Snimak ekrana korišćenja Redosleda toka procesa</span><span class="sxs-lookup"><span data-stu-id="8460f-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="8460f-151">Sledeći koraci se primenjuju na aplikaciju Project Service 2.4.4.30 ili raniju na platformi 9.0</span><span class="sxs-lookup"><span data-stu-id="8460f-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="8460f-152">Dodajte novo prilagođeno polje u entitet projekta da biste pribeležili prilagođene faze u svom prilagođenom toku poslovnog procesa.</span><span class="sxs-lookup"><span data-stu-id="8460f-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="8460f-153">Potrebno je da dodate poslovnu logiku (dodatnu komponentu/tok posla) da biste ispravili ovo polje kada se ispravlja faza u prilagođenom toku poslovnog procesa.</span><span class="sxs-lookup"><span data-stu-id="8460f-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![Snimak ekrana za prilagođavanje entiteta Projekat](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="8460f-155">Izmenite grafikon **Projekat prema fazi** da biste koristili novo prilagođeno polje za faze.</span><span class="sxs-lookup"><span data-stu-id="8460f-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![Snimak ekrana korišćenja grafikona Projekat prema fazi](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="8460f-157">Izmenite sve prikaze za entitet Projekat da biste obuhvatili novo prilagođeno polje za faze.</span><span class="sxs-lookup"><span data-stu-id="8460f-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![Snimak ekrana izmene prikaza u entitetu Projekat](media/FAQ-Customize-BPF-8-720.png)

