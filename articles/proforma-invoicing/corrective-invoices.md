---
title: Korigovane fakture
description: Ova tema pruža informacije o korigovanim fakturama.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 1ebfec053a59bbadd261d4333f6737cf16292e81
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122405"
---
# <a name="corrected-invoices"></a><span data-ttu-id="63137-103">Korigovane fakture</span><span class="sxs-lookup"><span data-stu-id="63137-103">Corrected invoices</span></span>

<span data-ttu-id="63137-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="63137-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="63137-105">Potvrđene fakture se mogu uređivati.</span><span class="sxs-lookup"><span data-stu-id="63137-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="63137-106">Kada uredite potvrđnu fakturu, kreira se radna verzija korigovane fakture.</span><span class="sxs-lookup"><span data-stu-id="63137-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="63137-107">Pošto je pretpostavka da želite da stornirate sve transakcije i količine iz originalne fakture, ova korigovana faktura uključuje sve transakcije iz originalne fakture, a sve količine na njoj su nula (0).</span><span class="sxs-lookup"><span data-stu-id="63137-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="63137-108">Kada neke transakcije ne zahtevaju korekciju, možete ih ukloniti iz radne verzije korigovane fakture.</span><span class="sxs-lookup"><span data-stu-id="63137-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="63137-109">Da biste stornirali ili opozvali samo delimičnu količinu, možete urediti polje Količina u detaljima stavke.</span><span class="sxs-lookup"><span data-stu-id="63137-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="63137-110">Ako otvorite detalj stavke fakture, možete videti količinu originalne fakture.</span><span class="sxs-lookup"><span data-stu-id="63137-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="63137-111">Zatim možete da uredite količinu trenutne fakture tako da bude manja ili veća od količine originalne fakture.</span><span class="sxs-lookup"><span data-stu-id="63137-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="63137-112">Kada potvrdite korigovanu fakturu, stornira se originalna stvarna vrednosti naplaćene prodaje i kreira se nova stvarna vrednost naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="63137-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="63137-113">Ako je količina smanjena, razlika će dovesti do toga da se kreira i nova stvarna vrednost nenaplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="63137-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="63137-114">Na primer, ako je originalna naplaćena prodaja bila za osam sati, a detalj stavke korigovane fakture ima manju količinu od šest sati, stornira se prvobitna naplaćena stavka prodaje i kreiraju se dve nove stvarne vrednosti:</span><span class="sxs-lookup"><span data-stu-id="63137-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="63137-115">Stvarna vrednosti naplaćene prodaje za šest sati.</span><span class="sxs-lookup"><span data-stu-id="63137-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="63137-116">Stvarna vrednosti nenaplaćene prodaje za preostala dva sata.</span><span class="sxs-lookup"><span data-stu-id="63137-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="63137-117">Ova transakcija može biti naplaćena kasnije ili označena kao nenaplativa, u zavisnosti od pregovora sa klijentom.</span><span class="sxs-lookup"><span data-stu-id="63137-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
