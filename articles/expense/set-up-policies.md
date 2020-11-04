---
title: Definisanje smernica troškova
description: Možete da definišete smernice troškova koje vaši radnici moraju slediti prilikom unošenja i podnošenja izveštaja o troškovima i putnih zahteva.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 30b3a0e1547ca7043b1433da2b4ebf02f2b473a1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083650"
---
# <a name="define-expense-policies"></a><span data-ttu-id="44d96-103">Definisanje smernica troškova</span><span class="sxs-lookup"><span data-stu-id="44d96-103">Define expense policies</span></span>

<span data-ttu-id="44d96-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="44d96-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="44d96-105">Možete da definišete smernice koje vaši radnici moraju slediti prilikom unošenja i podnošenja izveštaja o troškovima i putnih zahteva.</span><span class="sxs-lookup"><span data-stu-id="44d96-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="44d96-106">Sprovođenje smernica troškova može vam pomoći da efikasno upravljate troškovima.</span><span class="sxs-lookup"><span data-stu-id="44d96-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="44d96-107">Na primer, možete da postavite smernicu za hotelske troškove u NJujorku, koja navodi da trošak po noćenju ne može premašiti 250 USD.</span><span class="sxs-lookup"><span data-stu-id="44d96-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="44d96-108">Ako radnik podnese izveštaj o trošku ili zahtev za putovanje kada cena sobe prelazi ovaj iznos, sistem će obavestiti</span><span class="sxs-lookup"><span data-stu-id="44d96-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="44d96-109">radnika da je prekoračen iznos smernice za trošak.</span><span class="sxs-lookup"><span data-stu-id="44d96-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="44d96-110">Možete da konfigurišete poruku koju će radnik dobiti kada</span><span class="sxs-lookup"><span data-stu-id="44d96-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="44d96-111">definišete smernicu.</span><span class="sxs-lookup"><span data-stu-id="44d96-111">define the policy.</span></span>      
        
<span data-ttu-id="44d96-112">Možete da definišete tri tipa smernica:</span><span class="sxs-lookup"><span data-stu-id="44d96-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="44d96-113">**Upozorenje** : Omogućava radniku da podnese izveštaj o trošku ili zahtev za putovanje, ali će trošak biti označen za sve davaoce odobrenja i</span><span class="sxs-lookup"><span data-stu-id="44d96-113">**Warning** : Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="44d96-114">za kasnije izveštavanje.</span><span class="sxs-lookup"><span data-stu-id="44d96-114">for later reporting.</span></span>        

- <span data-ttu-id="44d96-115">**Greška** : Zahteva od radnika da revidira troškove kako bi se pridržavao smernica pre podnošenja izveštaja o troškovima ili zahteva za putovanje.</span><span class="sxs-lookup"><span data-stu-id="44d96-115">**Error** : Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="44d96-116">**Opravdanje** : Zahteva od radnika ili menadžera da unese obrazloženje za prekoračenje iznosa polise pre podnošenja izveštaja o troškovima ili zahteva za putovanje.</span><span class="sxs-lookup"><span data-stu-id="44d96-116">**Justification** : Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="44d96-117">Saveti za smernice</span><span class="sxs-lookup"><span data-stu-id="44d96-117">Policy tips</span></span>
<span data-ttu-id="44d96-118">Evo nekoliko predloga koji vam mogu pomoći pri kreiranju novih smernica za upravljanje troškovima:</span><span class="sxs-lookup"><span data-stu-id="44d96-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="44d96-119">Smernice važe na datum, što znači da smernice neće stupiti na snagu ako su kreirane sa datumom posle datuma nastanka troškova.</span><span class="sxs-lookup"><span data-stu-id="44d96-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="44d96-120">Na primer, danas kreirate novu politiku za primenu maksimalnih troškova obroka od 50 USD.</span><span class="sxs-lookup"><span data-stu-id="44d96-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="44d96-121">Svi postojeći troškovi koji su uneti od juče neće biti provereni u skladu sa ovom politikom.</span><span class="sxs-lookup"><span data-stu-id="44d96-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="44d96-122">Prilikom kreiranja smernica za kategoriju troškova koja se može podeliti, razmislite o dodavanju uslova za vrstu linije troškova.</span><span class="sxs-lookup"><span data-stu-id="44d96-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="44d96-123">Neke smernice, poput zahteva za priznanicom, možda neće imati smisla za detaljne linije.</span><span class="sxs-lookup"><span data-stu-id="44d96-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="44d96-124">U ovoj situaciji, smernice se primenjuju samo na liniju zaglavlja ili liniju koja nije stavljena u stavke.</span><span class="sxs-lookup"><span data-stu-id="44d96-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="44d96-125">Smernice za upravljanje troškovima podrazumevano se vrednuju prema izvornom entitetu.</span><span class="sxs-lookup"><span data-stu-id="44d96-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="44d96-126">U slučaju interkompanijskih scenarija, možete da podesite da se smernice vrednuju prema odredišnom entitetu (entitetu zaduživanja).</span><span class="sxs-lookup"><span data-stu-id="44d96-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="44d96-127">Da biste pokrenuli smernice prema odredišnom entitetu, uključite funkciju **Procenite smernice troškova u odnosu na zaduživanja pravnog lica** u radnom prostoru **Upravljanje funkcijama**.</span><span class="sxs-lookup"><span data-stu-id="44d96-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="44d96-128">Kada se procenjuju smernice</span><span class="sxs-lookup"><span data-stu-id="44d96-128">When to evaluate policies</span></span>

<span data-ttu-id="44d96-129">U parametrima upravljanja troškovima možete izabrati da procenite politike upravljanja troškovima kada se linija sačuva ili kada se podnese izveštaj o troškovima.</span><span class="sxs-lookup"><span data-stu-id="44d96-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="44d96-130">Ako odlučite da procenite kada je linija sačuvana, korisnici će imati raniji uvid u ono što treba da urade da bi odjednom kompletirali svoj izveštaj o troškovima.</span><span class="sxs-lookup"><span data-stu-id="44d96-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="44d96-131">U suprotnom, možete odložiti procenu smernica i uštedeti vreme potvrđivanjem na kraju, tokom predaje u radni tok.</span><span class="sxs-lookup"><span data-stu-id="44d96-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>
