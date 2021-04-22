---
title: Konfigurisanje računovodstva za interne projekte
description: Ova tema pruža informacije o tome kako postaviti računovodstvene prakse za interne projekte u usluzi Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 65d05e3a6321dc32aee55c28b3eaa4bd0bae2f86
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/06/2021
ms.locfileid: "5857995"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="25314-103">Konfigurisanje računovodstva za interne projekte</span><span class="sxs-lookup"><span data-stu-id="25314-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="25314-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="25314-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="25314-105">Interni projekti omogućavaju kompanijama da prate troškove povezane sa aktivnostima koje se ne naplaćuju klijentu.</span><span class="sxs-lookup"><span data-stu-id="25314-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="25314-106">Primeri internih projekata uključuju:</span><span class="sxs-lookup"><span data-stu-id="25314-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="25314-107">Razvoj proizvoda, kao što je aplikacija za mobilne uređaje, i praćenje troškova povezanih sa razvojem.</span><span class="sxs-lookup"><span data-stu-id="25314-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="25314-108">Upravljanje vremenom i troškovima pretprodaje.</span><span class="sxs-lookup"><span data-stu-id="25314-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="25314-109">Ovaj interni projekat u pretprodaji može se kasnije pretvoriti u naplativi projekat ako se dobije ponuda.</span><span class="sxs-lookup"><span data-stu-id="25314-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="25314-110">Bilo koji projekat koji nije povezan sa ugovorom u usluzi Dynamics 365 Project Operations tretira se kao interni.</span><span class="sxs-lookup"><span data-stu-id="25314-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="25314-111">Profili troškova i prihoda projekta ne koriste se za određivanje računovodstvenih pravila za projekat.</span><span class="sxs-lookup"><span data-stu-id="25314-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="25314-112">Interni troškovi projekta se uvek knjiže prema principima dobiti i gubitka.</span><span class="sxs-lookup"><span data-stu-id="25314-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="25314-113">Knjigovodstveni računi za knjiženja definisani su na stranici **Podešavanje knjiženja u knjizi**.</span><span class="sxs-lookup"><span data-stu-id="25314-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="25314-114">Vremenske transakcije se knjiže zaduživanjem naloga **Trošak** i kreditiranjem naloga **Raspodela zarada**.</span><span class="sxs-lookup"><span data-stu-id="25314-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="25314-115">Transakcije troškova se knjiže zaduživanjem naloga **Cena** i kreditiranjem naloga **Račun za prebijanje dugovanja i potraživanja za troškove**.</span><span class="sxs-lookup"><span data-stu-id="25314-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>
- <span data-ttu-id="25314-116">Transakcije stavki knjiže se zaduživanjem na računu **Cena** i potraživanjem na računu **Cena – Stavka**.</span><span class="sxs-lookup"><span data-stu-id="25314-116">Item transactions are posted by debiting the **Cost** account and crediting the **Cost - Item** account.</span></span>

<span data-ttu-id="25314-117">Nakon što su transakcije knjižene u projekat, ako je projekat povezan sa projektnim ugovorom, sistem poništava sve akumulirane transakcije i kreira nove naplative transakcije.</span><span class="sxs-lookup"><span data-stu-id="25314-117">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="25314-118">Transakcije koje se naplaćuju prate računovodstvena pravila definisana u odgovarajućem profilu troškova i prihoda projekta.</span><span class="sxs-lookup"><span data-stu-id="25314-118">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
