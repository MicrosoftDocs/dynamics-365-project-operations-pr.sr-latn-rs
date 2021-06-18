---
title: Izmena prodajnih cenovnika za projekat
description: Ova tema pruža informacije o kreiranju prilagođenih prodajnih cenovnika.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: db2ff6acaad6ab4cbcc98d3d5b06b36ed23b758f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995098"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="cc3e6-103">Izmena prodajnih cenovnika za projekat</span><span class="sxs-lookup"><span data-stu-id="cc3e6-103">Override project sales price lists</span></span>

<span data-ttu-id="cc3e6-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="cc3e6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="cc3e6-105">Cenovnici projekata specifični za klijenta</span><span class="sxs-lookup"><span data-stu-id="cc3e6-105">Customer-specific project price lists</span></span>

<span data-ttu-id="cc3e6-106">Ugovori o cenama specifični za klijenta mogu se postaviti kao cenovnici projekata u zapisu poslovnog kontakta u usluzi Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="cc3e6-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="cc3e6-107">Da biste postavili cenovnik projekata specifičan za klijenta, u oblasti **Prodaja**, dođite do zapisa o poslovnom kontaktu.</span><span class="sxs-lookup"><span data-stu-id="cc3e6-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="cc3e6-108">Otvorite stranicu liste **Poslovni kontakti**.</span><span class="sxs-lookup"><span data-stu-id="cc3e6-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="cc3e6-109">Pronađite i dvaput kliknite na zapis klijenta da biste otvorili stranicu sa detaljima o **poslovnom kontaktu**.</span><span class="sxs-lookup"><span data-stu-id="cc3e6-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="cc3e6-110">Na kartici **Cenovnici projekta** izaberite **+ Novi cenovnik projekta**.</span><span class="sxs-lookup"><span data-stu-id="cc3e6-110">On the **Project Price lists** tab, select **+ New Project Price List**.</span></span>
4. <span data-ttu-id="cc3e6-111">Na stranici **Novi cenovnik projekta**, iz padajuće liste izaberite cenovnik.</span><span class="sxs-lookup"><span data-stu-id="cc3e6-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="cc3e6-112">Uključeni su samo cenovnici kojima je kontekst postavljen na **Prodaja** i čija valuta se podudara sa valutom poslovnog kontakta.</span><span class="sxs-lookup"><span data-stu-id="cc3e6-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="cc3e6-113">Imenujte povezivanje, a zatim izaberite **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="cc3e6-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="cc3e6-114">Kreiraće se cenovnik projekta specifičan za klijenta.</span><span class="sxs-lookup"><span data-stu-id="cc3e6-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="cc3e6-115">Ovaj cenovnik će se koristiti za podrazumevane cene za projekat u ponudama ili ugovorima za projekat kreiranim za ovog klijenta kada datum kreiranja ponude ili ugovora za projekat spada u datum efektivnosti cenovnika.</span><span class="sxs-lookup"><span data-stu-id="cc3e6-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="cc3e6-116">Prilagođeno određivanje cena u ponudama za projekat</span><span class="sxs-lookup"><span data-stu-id="cc3e6-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="cc3e6-117">U ponudama za projekat, možete imati cene projekata koje počinju sa podrazumevanim standardnim cenovnikom koji dobija podrazumevane vrednosti od klijenta ili iz parametara projekta.</span><span class="sxs-lookup"><span data-stu-id="cc3e6-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="cc3e6-118">Kada vam je potrebno prilagođeno određivanje cena za posao u vezi sa projektom za određenu ponudu, to možete dobiti iz entiteta povezanog sa cenovnicima projekata.</span><span class="sxs-lookup"><span data-stu-id="cc3e6-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="cc3e6-119">Dovršite sledeće korake da biste postavili cene projekata specifične za ponudu.</span><span class="sxs-lookup"><span data-stu-id="cc3e6-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="cc3e6-120">Otvorite ponudu za projekat i izaberite karticu **Cenovnici projekta**.</span><span class="sxs-lookup"><span data-stu-id="cc3e6-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="cc3e6-121">U podformi izaberite **Kreiraj prilagođene cene**.</span><span class="sxs-lookup"><span data-stu-id="cc3e6-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="cc3e6-122">Svi cenovnici projekta koji su priloženi uz ponudu kopiraju se u nove cenovnike.</span><span class="sxs-lookup"><span data-stu-id="cc3e6-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="cc3e6-123">Nazivi novih cenovnika odražavaju naziv ponude sa obeležjem datuma i vremena kada su ovi cenovnici kreirani.</span><span class="sxs-lookup"><span data-stu-id="cc3e6-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="cc3e6-124">Možete da koristite svaki od tih cenovnika i ažurirate cene rada (cena uloge) i cene troškova (cena kategorije).</span><span class="sxs-lookup"><span data-stu-id="cc3e6-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="cc3e6-125">Ove cene će se primenjivati samo na ovu ponudu za projekat.</span><span class="sxs-lookup"><span data-stu-id="cc3e6-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="cc3e6-126">Cenovnici u ugovoru za projekat</span><span class="sxs-lookup"><span data-stu-id="cc3e6-126">Price lists on a project contract</span></span>

<span data-ttu-id="cc3e6-127">U ugovoru za projekat, određivanje cena za projekat se uvek podrazumeva iz prilagođenog cenovnika sa nazivom ugovora i obeležjem datuma i vremena kreiranja koji se dodaje nazivu.</span><span class="sxs-lookup"><span data-stu-id="cc3e6-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="cc3e6-128">To je tačno da li je ugovor kreiran kada je ponuda dobijena ili je ugovor kreiran ispočetka.</span><span class="sxs-lookup"><span data-stu-id="cc3e6-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="cc3e6-129">Ako je potrebno, možete ukloniti ovo povezivanje sa prilagođenim cenovnikom i umesto toga pridružiti standardni cenovnik ugovoru o projektu.</span><span class="sxs-lookup"><span data-stu-id="cc3e6-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="cc3e6-130">Kada standardni cenovnik pridružite cenovnicima projekta u ponudi ili ugovoru, sve promene cena u cenovniku uticaće na sve ponude i ugovore koji koriste taj cenovnik.</span><span class="sxs-lookup"><span data-stu-id="cc3e6-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]