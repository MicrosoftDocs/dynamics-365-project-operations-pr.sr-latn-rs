---
title: Podešavanje smernica troškova
description: Možete da podesite smernice troškova koje vaši radnici moraju slediti prilikom unošenja i podnošenja izveštaja o troškovima i putnih zahteva u usluzi Microsoft Dynamics 365 Finance.
author: suvaidya
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa4f628a918e6e099a723ed05994f63d6ad847f5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005763"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="25034-103">Podešavanje smernica troškova</span><span class="sxs-lookup"><span data-stu-id="25034-103">Set up expense policies</span></span>

<span data-ttu-id="25034-104">Možete da definišete smernice koje vaši radnici moraju slediti prilikom unošenja i podnošenja izveštaja o troškovima i putnih zahteva.</span><span class="sxs-lookup"><span data-stu-id="25034-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="25034-105">Sprovođenje smernica troškova može vam pomoći da efikasno upravljate troškovima.</span><span class="sxs-lookup"><span data-stu-id="25034-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="25034-106">Na primer, možete da postavite smernicu za hotelske troškove u Njujorku, koja navodi da trošak po noćenju ne može premašiti 250 USD.</span><span class="sxs-lookup"><span data-stu-id="25034-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="25034-107">Ako radnik podnese izveštaj o trošku ili zahtev za putovanje kada cena sobe prelazi ovaj iznos, sistem će o tome obavestiti</span><span class="sxs-lookup"><span data-stu-id="25034-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="25034-108">radnika da je prekoračen iznos smernice za trošak.</span><span class="sxs-lookup"><span data-stu-id="25034-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="25034-109">Možete da konfigurišete poruku koju će radnik dobiti kada</span><span class="sxs-lookup"><span data-stu-id="25034-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="25034-110">definišete smernicu.</span><span class="sxs-lookup"><span data-stu-id="25034-110">define the policy.</span></span>      
        
<span data-ttu-id="25034-111">Možete da definišete tri tipa smernica:</span><span class="sxs-lookup"><span data-stu-id="25034-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="25034-112">Upozorenje – Omogućava radniku da podnese izveštaj o trošku ili zahtev za putovanje, ali će trošak biti označen za sve davaoce odobrenja i</span><span class="sxs-lookup"><span data-stu-id="25034-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="25034-113">za kasnije izveštavanje.</span><span class="sxs-lookup"><span data-stu-id="25034-113">for later reporting.</span></span>        

- <span data-ttu-id="25034-114">Greška – Zahteva od radnika da revidira troškove kako bi se pridržavao smernica pre podnošenja izveštaja o troškovima ili zahteva za putovanje.</span><span class="sxs-lookup"><span data-stu-id="25034-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="25034-115">Opravdanje – Zahteva od radnika ili menadžera da unese obrazloženje za prekoračenje iznosa polise pre podnošenja izveštaja o troškovima ili zahteva za putovanje.</span><span class="sxs-lookup"><span data-stu-id="25034-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="25034-116">Saveti za smernice</span><span class="sxs-lookup"><span data-stu-id="25034-116">Policy tips</span></span>
<span data-ttu-id="25034-117">Evo nekoliko predloga koji vam mogu pomoći pri kreiranju novih smernica za upravljanje troškovima.</span><span class="sxs-lookup"><span data-stu-id="25034-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="25034-118">Smernice važe na datum i neće stupiti na snagu ako su kreirane sa datumom posle datuma nastanka troškova.</span><span class="sxs-lookup"><span data-stu-id="25034-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="25034-119">Na primer, ako danas kreirate nove smernice za primenu maksimalnog troška obroka od 50 USD, svi postojeći troškovi uneti od juče neće biti provereni u skladu sa ovim smernicama.</span><span class="sxs-lookup"><span data-stu-id="25034-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="25034-120">Prilikom kreiranja smernica za kategoriju troškova koja se može podeliti, razmislite o dodavanju uslova za vrstu linije troškova.</span><span class="sxs-lookup"><span data-stu-id="25034-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="25034-121">Neke smernice, poput zahteva za priznanicu, možda neće imati smisla za razvrstane stavke i treba ih primeniti samo na zaglavlje ili nerazvrstane stavke.</span><span class="sxs-lookup"><span data-stu-id="25034-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="25034-122">Smernice za upravljanje troškovima podrazumevano se vrednuju prema izvornom entitetu.</span><span class="sxs-lookup"><span data-stu-id="25034-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="25034-123">U slučaju interkompanijskih scenarija, možete da podesite da se smernice vrednuju prema odredišnom entitetu (entitetu zaduživanja).</span><span class="sxs-lookup"><span data-stu-id="25034-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="25034-124">Da biste pokrenuli smernice prema odredišnom entitetu, uključite funkciju „Procenite smernice troškova u odnosu na zaduživanja pravnog lica“ u radnom prostoru **Upravljanje funkcijama**.</span><span class="sxs-lookup"><span data-stu-id="25034-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="25034-125">Kada se procenjuju smernice</span><span class="sxs-lookup"><span data-stu-id="25034-125">When to evaluate policies</span></span>

<span data-ttu-id="25034-126">U parametrima upravljanja troškovima postoji opcija da procenite politike upravljanja troškovima kada se linija sačuva ili kada se podnese izveštaj o troškovima.</span><span class="sxs-lookup"><span data-stu-id="25034-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="25034-127">Ako odlučite da procenite kada je linija sačuvana, korisnici će imati raniji uvid u ono što treba da urade da bi odjednom kompletirali svoj izveštaj o troškovima.</span><span class="sxs-lookup"><span data-stu-id="25034-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="25034-128">U suprotnom, možete odložiti procenu smernica i uštedeti vreme ako se potvrđivanje obavlja na kraju, tokom predaje u radni tok.</span><span class="sxs-lookup"><span data-stu-id="25034-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]