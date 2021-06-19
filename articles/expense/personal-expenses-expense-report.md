---
title: Rad sa ličnim troškovima u izveštaju o troškovima
description: Ova tema pruža informacije o načinu rada sa ličnim troškovima koje su ostvarili zaposlen na poslovnim putovanjima.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025701"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="a1267-103">Rad sa ličnim troškovima u izveštaju o troškovima</span><span class="sxs-lookup"><span data-stu-id="a1267-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="a1267-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="a1267-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a1267-105">Tokom poslovnog puta zaposleni može naplatiti lične troškove sa kreditne kartice preduzeća.</span><span class="sxs-lookup"><span data-stu-id="a1267-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="a1267-106">Ako nije definisan postupak za upravljanje ličnim troškovima, postupak odobravanja izveštaja o troškovima može biti prekinut kada zaposleni preda detaljni izveštaj o troškovima.</span><span class="sxs-lookup"><span data-stu-id="a1267-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="a1267-107">Postoje dve metode koje možete koristiti za rad sa ličnim troškovima zaposlenog:</span><span class="sxs-lookup"><span data-stu-id="a1267-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="a1267-108">**Plaća zaposleni**: Vaša organizacija ne plaća lične troškove koji se pojavljuju na računu za kreditnu karticu preduzeća.</span><span class="sxs-lookup"><span data-stu-id="a1267-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="a1267-109">Umesto toga, zaposleni direktno plaća dobavljaču kreditne kartice za troškove.</span><span class="sxs-lookup"><span data-stu-id="a1267-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="a1267-110">**Plaća preduzeće**: Vaša organizacija plaća ceo račun za kreditnu karticu preduzeća, a zatim tereti račun radnika za lične troškove.</span><span class="sxs-lookup"><span data-stu-id="a1267-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="a1267-111">Možete odabrati metod koji vaša organizacija koristi na stranici **Parametri upravljanja troškovima**.</span><span class="sxs-lookup"><span data-stu-id="a1267-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="a1267-112">Omogućite funkciju podeljenih troškova kada polje za lični iznos ima definisanu vrednost</span><span class="sxs-lookup"><span data-stu-id="a1267-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="a1267-113">Funkcija, **Omogućite funkciju podeljenih troškova kada polje za lični iznos ima definisanu vrednost** odnosi se samo na izveštaje o troškovima koji su odobreni korišćenjem toka posla na nivou stavke.</span><span class="sxs-lookup"><span data-stu-id="a1267-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="a1267-114">Izveštaji se odobravaju odlaskom na **Obrada izveštaja o troškovima** > **Izveštaji o troškovima koji su mi dodeljeni** > **Otvori izveštaj o troškovima**.</span><span class="sxs-lookup"><span data-stu-id="a1267-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="a1267-115">Da biste omogućili ovu funkciju, idite na **Radni prostori** > **Upravljanje funkcijama**, izaberite **Omogući funkciju podeljenih troškova kada polje za lični iznos ima definisanu vrednost**, a zatim izaberite **Omogući odmah**.</span><span class="sxs-lookup"><span data-stu-id="a1267-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="a1267-116">Kada je funkcija omogućena, stavke troškova koje koriste ovu funkciju generišu dve stavke kada se izveštaj podnese.</span><span class="sxs-lookup"><span data-stu-id="a1267-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="a1267-117">Dve stavke se generišu tako da davalac odobrenja može da odobri svaki red zasebno.</span><span class="sxs-lookup"><span data-stu-id="a1267-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
