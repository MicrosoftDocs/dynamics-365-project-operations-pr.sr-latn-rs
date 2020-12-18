---
title: Pregled internog fakturisanja u okviru preduzeća
description: Ova tema pruža informacije i primere o internom fakturisanju između preduzeća za projekte.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 670b5d15ecf1ef7dcc034064e625814cbe6d54b0
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595543"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="59a04-103">Pregled internog fakturisanja u okviru preduzeća</span><span class="sxs-lookup"><span data-stu-id="59a04-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="59a04-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="59a04-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="59a04-105">Vaša organizacija može imati više odeljenja, podružnica i drugih pravnih lica koja međusobno prenose proizvode i usluge za projekte.</span><span class="sxs-lookup"><span data-stu-id="59a04-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="59a04-106">Pravno lice koje pruža uslugu ili daje proizvod naziva se *pravno lice koje pozajmljuje*.</span><span class="sxs-lookup"><span data-stu-id="59a04-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="59a04-107">Pravno lice koje prima uslugu ili proizvod naziva se *pravno lice koje se zadužuje*.</span><span class="sxs-lookup"><span data-stu-id="59a04-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="59a04-108">Sledeća ilustracija prikazuje tipični scenario kada dva pravna lica, Contoso Robotics USA (pravno lice koje se zadužuje) i Contoso Robotics UK (pravno lice koje pozajmljuje) dele resurse kako bi isporučili projekat klijentu, Adventure works.</span><span class="sxs-lookup"><span data-stu-id="59a04-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="59a04-109">Za ovaj scenario, Contoso Robotics USA po ugovoru treba da isporuči posao preduzeću Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="59a04-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Interno fakturisanje u okviru preduzeća](./media/IntercompanyScenario.png) 

<span data-ttu-id="59a04-111">Dynamics 365 Project Operations koristi sledeći tok za obradu transakcija između preduzeća:</span><span class="sxs-lookup"><span data-stu-id="59a04-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="59a04-112">Resursi pravnog lica koje daje pozajmice evidentiraju transakcije vremena ili troškova između preduzeća prema vremenu i trošku rezervacije u osnovu na projekte pravnog lica koje se zadužuje.</span><span class="sxs-lookup"><span data-stu-id="59a04-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="59a04-113">Troškovi vremena i troškova evidentiraju se u preduzeću koje pozajmljuje korišćenjem jediničnog cenovnika troškova preduzeća koje se zadužuje.</span><span class="sxs-lookup"><span data-stu-id="59a04-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="59a04-114">Nenaplaćene prodajne transakcije između preduzeća evidentiraju se u kompaniji koja pozajmljuje korišćenjem jediničnog cenovnika troškova preduzeća koje se zadužuje.</span><span class="sxs-lookup"><span data-stu-id="59a04-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="59a04-115">Nefakturisani prihod se evidentira u preduzeću koje se zadužuje koristeći cenovnik prodajnih cena po ugovoru o projektu.</span><span class="sxs-lookup"><span data-stu-id="59a04-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="59a04-116">Klijentu možete naplatiti kada se evidentira nefakturisani prihod.</span><span class="sxs-lookup"><span data-stu-id="59a04-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="59a04-117">Klijent ne mora da čeka dok se obrada faktura između preduzeća ne završi.</span><span class="sxs-lookup"><span data-stu-id="59a04-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="59a04-118">Fakture klijenata između preduzeća se kreiraju periodično u preduzeću koje pozajmljuje.</span><span class="sxs-lookup"><span data-stu-id="59a04-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="59a04-119">Fakture se kreiraju ručno ili korišćenjem periodičnog automatizovanog procesa.</span><span class="sxs-lookup"><span data-stu-id="59a04-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="59a04-120">Za svako pravno lice koje se zadužuje možete kreirati pojedinačnu fakturu ili zasebne fakture mogu biti kreirane projektom.</span><span class="sxs-lookup"><span data-stu-id="59a04-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="59a04-121">Kada se faktura klijenta između preduzeća knjiži u pravnom licu koje pozajmljuje, u pravnom licu koje se zadužuje kreira se odgovarajuća faktura dobavljača na čekanju.</span><span class="sxs-lookup"><span data-stu-id="59a04-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="59a04-122">Troškovi na fakturi dobavljača na čekanju evidentiraće se u potknjizi projekta kada se faktura proknjiži.</span><span class="sxs-lookup"><span data-stu-id="59a04-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="59a04-123">Sledeći dijagram ilustruje fakturisanje između preduzeća koje se odnosi na računovodstvene događaje i očekivana knjiženja u glavnu knjigu.</span><span class="sxs-lookup"><span data-stu-id="59a04-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Tok između preduzeća](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="59a04-125">Dodatni resursi</span><span class="sxs-lookup"><span data-stu-id="59a04-125">Additional resources</span></span>

- [<span data-ttu-id="59a04-126">Konfigurisanje internog fakturisanja u okviru preduzeća</span><span class="sxs-lookup"><span data-stu-id="59a04-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="59a04-127">Evidentiranje transakcija u okviru preduzeća</span><span class="sxs-lookup"><span data-stu-id="59a04-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="59a04-128">Kreiranje internih faktura klijenta i dobavljača u okviru preduzeća</span><span class="sxs-lookup"><span data-stu-id="59a04-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)
