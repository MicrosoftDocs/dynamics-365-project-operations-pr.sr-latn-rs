---
title: Pregled troškova
description: Ova tema pruža informacije o funkcionalnosti troškova u usluzi Project Operations.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 6da831fef5dba060b8019d7689645405c7ebdbed
ms.sourcegitcommit: 0874b3d89e1dc0e65a51cedb82bf8f80831ca0bb
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/06/2020
ms.locfileid: "3967383"
---
# <a name="expense-home-page"></a><span data-ttu-id="ff6a0-103">Početna stranica troškova</span><span class="sxs-lookup"><span data-stu-id="ff6a0-103">Expense home page</span></span>

<span data-ttu-id="ff6a0-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="ff6a0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="ff6a0-105">Dynamics 365 Project Operations podržava mogućnost obrade troškova.</span><span class="sxs-lookup"><span data-stu-id="ff6a0-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="ff6a0-106">Obrada troškova se odvija sa projektima ili bez njih korišćenjem prilagodljivog toka posla smernica, kategorija transakcija i odobrenja.</span><span class="sxs-lookup"><span data-stu-id="ff6a0-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="ff6a0-107">U usluzi Project Operations postoje dva podržana modela primene za troškove:</span><span class="sxs-lookup"><span data-stu-id="ff6a0-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="ff6a0-108">**Potpuno**: Potpuna primena je dostupna za **Project Operations za scenarije zasnovane na resursima / bez zaliha** ili **Project Operations za scenarije zasnovane na nalogu za proizvodnju**.</span><span class="sxs-lookup"><span data-stu-id="ff6a0-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order based scenarios**.</span></span>
- <span data-ttu-id="ff6a0-109">**Osnovno**: Osnovna primena je dostupna za **Project Operations za scenarije zasnovane na resursima / bez zaliha** i **Jednostavna primena – od pogodbe do profakture**.</span><span class="sxs-lookup"><span data-stu-id="ff6a0-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="ff6a0-110">Pun</span><span class="sxs-lookup"><span data-stu-id="ff6a0-110">Full</span></span> 
<span data-ttu-id="ff6a0-111">Potpuna primena troškova obezbeđuje potpuno sprovođenje smernica, što obuhvata mogućnost kreiranja smernica, kao što su:</span><span class="sxs-lookup"><span data-stu-id="ff6a0-111">Full Expense deployment provides a complete policy enforcement which includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="ff6a0-112">Ograničenja kategorija troškova</span><span class="sxs-lookup"><span data-stu-id="ff6a0-112">Expense category limits</span></span>
  - <span data-ttu-id="ff6a0-113">Putovanje</span><span class="sxs-lookup"><span data-stu-id="ff6a0-113">Travel</span></span>
  - <span data-ttu-id="ff6a0-114">Dnevnica</span><span class="sxs-lookup"><span data-stu-id="ff6a0-114">Per diem</span></span>
  - <span data-ttu-id="ff6a0-115">Uvozi kreditnih kartica</span><span class="sxs-lookup"><span data-stu-id="ff6a0-115">Credit card imports</span></span>
  - <span data-ttu-id="ff6a0-116">Optičko prepoznavanje znakova priznanice</span><span class="sxs-lookup"><span data-stu-id="ff6a0-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="ff6a0-117">Osnovno</span><span class="sxs-lookup"><span data-stu-id="ff6a0-117">Basic</span></span> 
<span data-ttu-id="ff6a0-118">Scenarij primene osnovnih troškova vam omogućava samo evidentiranje osnovnih troškova u odnosu na projekat.</span><span class="sxs-lookup"><span data-stu-id="ff6a0-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="ff6a0-119">Za više informacija, pogledajte [Unos troškova (jednostavno)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="ff6a0-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="ff6a0-120">Odredite svoju primenu troškova</span><span class="sxs-lookup"><span data-stu-id="ff6a0-120">Determine your Expense deployment</span></span>
<span data-ttu-id="ff6a0-121">Da biste utvrdili da li pokrećete primenu upravljanja osnovnim troškovima, proverite da li se URL adresa završava sa **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="ff6a0-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 
