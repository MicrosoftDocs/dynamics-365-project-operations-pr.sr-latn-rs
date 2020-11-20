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
ms.openlocfilehash: ea04178d4327ccd701ab431f172463a13a55154e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132395"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="38701-103">Konfigurisanje računovodstva za interne projekte</span><span class="sxs-lookup"><span data-stu-id="38701-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="38701-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="38701-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="38701-105">Interni projekti omogućavaju kompanijama da prate troškove povezane sa aktivnostima koje se ne naplaćuju klijentu.</span><span class="sxs-lookup"><span data-stu-id="38701-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="38701-106">Primeri internih projekata uključuju:</span><span class="sxs-lookup"><span data-stu-id="38701-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="38701-107">Razvoj proizvoda, kao što je aplikacija za mobilne uređaje, i praćenje troškova povezanih sa razvojem.</span><span class="sxs-lookup"><span data-stu-id="38701-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="38701-108">Upravljanje vremenom i troškovima pretprodaje.</span><span class="sxs-lookup"><span data-stu-id="38701-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="38701-109">Ovaj interni projekat u pretprodaji može se kasnije pretvoriti u naplativi projekat ako se dobije ponuda.</span><span class="sxs-lookup"><span data-stu-id="38701-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="38701-110">Bilo koji projekat koji nije povezan sa ugovorom u proizvodu Dynamics 365 Project Operations se tretira kao interni.</span><span class="sxs-lookup"><span data-stu-id="38701-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="38701-111">Profili troškova i prihoda projekta ne koriste se za određivanje računovodstvenih pravila za projekat.</span><span class="sxs-lookup"><span data-stu-id="38701-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="38701-112">Interni troškovi projekta se uvek knjiže prema principima dobiti i gubitka.</span><span class="sxs-lookup"><span data-stu-id="38701-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="38701-113">Knjigovodstveni računi za knjiženja definisani su na stranici **Podešavanje knjiženja u knjizi**.</span><span class="sxs-lookup"><span data-stu-id="38701-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="38701-114">Vremenske transakcije se knjiže zaduživanjem naloga **Trošak** i kreditiranjem naloga **Raspodela zarada**.</span><span class="sxs-lookup"><span data-stu-id="38701-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="38701-115">Transakcije troškova se knjiže zaduživanjem naloga **Cena** i kreditiranjem naloga **Račun za prebijanje dugovanja i potraživanja za troškove**.</span><span class="sxs-lookup"><span data-stu-id="38701-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>

<span data-ttu-id="38701-116">Nakon što su transakcije knjižene u projekat, ako je projekat povezan sa projektnim ugovorom, sistem poništava sve akumulirane transakcije i kreira nove naplative transakcije.</span><span class="sxs-lookup"><span data-stu-id="38701-116">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="38701-117">Transakcije koje se naplaćuju prate računovodstvena pravila definisana u odgovarajućem profilu troškova i prihoda projekta.</span><span class="sxs-lookup"><span data-stu-id="38701-117">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>


