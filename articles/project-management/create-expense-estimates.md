---
title: Procene troškova
description: Ova tema pruža informacije o definisanju ili proceni troškova zasnovanih na projektu.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908538"
---
# <a name="expense-estimates"></a><span data-ttu-id="8110d-103">Procene troškova</span><span class="sxs-lookup"><span data-stu-id="8110d-103">Expense estimates</span></span>
<span data-ttu-id="8110d-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="8110d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8110d-105">Zajedno sa definisanjem procena zasnovanih na resursima, Dynamics 365 Project Operations omogućava menadžerima projekata da definišu troškove zasnovane na projektu za svaki projekat.</span><span class="sxs-lookup"><span data-stu-id="8110d-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="8110d-106">Svaka stavka troškova može biti povezana sa određenim projektnim zadatkom ili kategorijom troškova.</span><span class="sxs-lookup"><span data-stu-id="8110d-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="8110d-107">Kategorije troškova se obično definišu na nivou organizacije.</span><span class="sxs-lookup"><span data-stu-id="8110d-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="8110d-108">Određivanje cena za svaku kategoriju troškova obično je definisano u sledećoj hijerarhiji:</span><span class="sxs-lookup"><span data-stu-id="8110d-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="8110d-109">Organizacija</span><span class="sxs-lookup"><span data-stu-id="8110d-109">Organization</span></span>
- <span data-ttu-id="8110d-110">Klijent</span><span class="sxs-lookup"><span data-stu-id="8110d-110">Customer</span></span>
- <span data-ttu-id="8110d-111">Ponuda/ugovor</span><span class="sxs-lookup"><span data-stu-id="8110d-111">Quote/contract</span></span>

<span data-ttu-id="8110d-112">Dovršite sledeće korake za prikaz, dodavanje ili brisanje troškova projekta.</span><span class="sxs-lookup"><span data-stu-id="8110d-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="8110d-113">Idite na **Projekti**, i izaberite projekat na kojem želite da radite.</span><span class="sxs-lookup"><span data-stu-id="8110d-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="8110d-114">Izaberite karticu **Projektne procene** i pogledajte listu troškova projekta.</span><span class="sxs-lookup"><span data-stu-id="8110d-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="8110d-115">Izaberite **Novi trošak** da biste dodali trošak.</span><span class="sxs-lookup"><span data-stu-id="8110d-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="8110d-116">Ili izaberite trošak koji želite da izbrišete, a zatim izaberite **Izbriši trošak**.</span><span class="sxs-lookup"><span data-stu-id="8110d-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="8110d-117">Sledeći atributi su definisani za svaku stavku troškova:</span><span class="sxs-lookup"><span data-stu-id="8110d-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="8110d-118">**Kategorija**: Uobičajena grupisanja korišćena za opisivanje svih troškova nastalih na projektu.</span><span class="sxs-lookup"><span data-stu-id="8110d-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="8110d-119">**Datum početka**: Datum kada se predviđa da će nastati trošak.</span><span class="sxs-lookup"><span data-stu-id="8110d-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="8110d-120">**Količina**: Procenjeni broj stavki troškova za određenu kategoriju.</span><span class="sxs-lookup"><span data-stu-id="8110d-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="8110d-121">**Jedinična cena koštanja**: Jedinična cena koja se koristi za izračunavanje cene troškova.</span><span class="sxs-lookup"><span data-stu-id="8110d-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="8110d-122">**Jedinična prodajna cena**: Jedinična cena koja se koristi za izračunavanje prodajne cene troškova.</span><span class="sxs-lookup"><span data-stu-id="8110d-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>

