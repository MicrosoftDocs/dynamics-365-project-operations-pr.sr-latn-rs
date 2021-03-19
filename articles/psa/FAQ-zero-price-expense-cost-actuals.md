---
title: Zašto se cena podrazumevano vraća na nulu na iznosima stvarnih troškova?
description: Rešavanje problema zbog čega se cena podrazumevano vraća na 0 na iznosima stvarnih troškova.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
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
ms.openlocfilehash: 742b0b9c495b4b3ecb4705be3ece5656f0322ca9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285870"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="40036-103">Zašto se cena podrazumevano vraća na nulu za iznose stvarnih troškova?</span><span class="sxs-lookup"><span data-stu-id="40036-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="40036-104">Ova najčešća pitanja se odnose na stvarne troškove u kojima je klasa transakcije podešena na Trošak, a gde je vrsta transakcije Trošak.</span><span class="sxs-lookup"><span data-stu-id="40036-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="40036-105">Rešavanje problema sa stopama troškova u iznosima stvarnih troškova</span><span class="sxs-lookup"><span data-stu-id="40036-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="40036-106">Idite na odnosnu stavku troška i uverite se da u polju stavke troška postoji iznos.</span><span class="sxs-lookup"><span data-stu-id="40036-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="40036-107">Ako izvorna stavka troška nije imala popunjeno polje za iznos, onda ste izolovali problem.</span><span class="sxs-lookup"><span data-stu-id="40036-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="40036-108">Da biste rešili ovaj problem, ponovo kreirajte stavku troška sa važećim iznosom i odobrite ga.</span><span class="sxs-lookup"><span data-stu-id="40036-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]