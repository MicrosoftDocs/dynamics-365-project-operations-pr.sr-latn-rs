---
title: Zašto se cena podrazumevano vraća na nulu na iznosima stvarnih troškova?
description: Rešavanje problema zbog čega se cena podrazumevano vraća na 0 na iznosima stvarnih troškova.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9f4ff8a96250d675faeda3246c2d0a6c5bd83286
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083601"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>Zašto se cena podrazumevano vraća na nulu na iznosima stvarnih troškova?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ova najčešća pitanja se odnose na stvarne troškove u kojima je klasa transakcije podešena na Trošak, a gde je vrsta transakcije Trošak.

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Rešavanje problema sa stopama troškova u iznosima stvarnih troškova

Idite na odnosnu stavku troška i uverite se da u polju stavke troška postoji iznos. Ako izvorna stavka troška nije imala popunjeno polje za iznos, onda ste izolovali problem.
 
Da biste rešili ovaj problem, ponovo kreirajte stavku troška sa važećim iznosom i odobrite ga.
