---
title: Kupujte neskladišteni materijal koristeći fakturu dobavljača na čekanju
description: Ova tema objašnjava kako da snimite fakture dobavljača na čekanju.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b5e6632d73c8a211b1f0d568be8e10ef47be77e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993827"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="8f023-103">Kupujte neskladišteni materijal koristeći fakturu dobavljača na čekanju</span><span class="sxs-lookup"><span data-stu-id="8f023-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="8f023-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="8f023-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8f023-105">Kako kompanija nabavlja ne-zalihe materijala za projekat, troškovi se mogu odmah evidentirati u odnosu na projekat.</span><span class="sxs-lookup"><span data-stu-id="8f023-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="8f023-106">Na primer, Contoso Robotics US izvodi projekat obnove opreme i potrebne su softverske licence.</span><span class="sxs-lookup"><span data-stu-id="8f023-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="8f023-107">Ove licence se nabavljaju od nezavisnog dobavljača.</span><span class="sxs-lookup"><span data-stu-id="8f023-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="8f023-108">Koristeći Dynamics 365 Finance, službenik za dugovanja evidentira dokument fakture dobavljača na čekanju i pripisuje troškove licence direktno projektu obnove opreme.</span><span class="sxs-lookup"><span data-stu-id="8f023-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="8f023-109">Pre nego što upotrebite funkcionalnost opisanu u ovoj temi, pregledajte i primenite potrebne konfiguracije.</span><span class="sxs-lookup"><span data-stu-id="8f023-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="8f023-110">Za više informacija pogledajte [Omogućite neskladišteni materijal i fakture dobavljača na čekanju](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="8f023-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="8f023-111">Pošaljite fakturu dobavljača na čekanju u vezi sa projektom</span><span class="sxs-lookup"><span data-stu-id="8f023-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="8f023-112">Fakture dobavljača na čekanju mogu se evidentirati na stranici **Fakture dobavljača na čekanju** (**Dugovanja** > **Fakture** > **Fakture dobavljača na čekanju**).</span><span class="sxs-lookup"><span data-stu-id="8f023-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="8f023-113">Dovršite sledeće korake da biste knjižili fakturu dobavljača na čekanju u vezi sa projektom:</span><span class="sxs-lookup"><span data-stu-id="8f023-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="8f023-114">Idite na **Dugovanja** > **Fakture** i izaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="8f023-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="8f023-115">U polju **Račun fakture** izaberite dobavljača i u polje **Broj** unesite identifikaciju računa dobavljača.</span><span class="sxs-lookup"><span data-stu-id="8f023-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="8f023-116">Dodajte red na fakturu dobavljača i u polje **Broj predmeta** izaberite artikal na zalihama kupljen od dobavljača.</span><span class="sxs-lookup"><span data-stu-id="8f023-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="8f023-117">Redovi faktura dobavljača koji se zasnivaju na kategoriji nabavke ne mogu se evidentirati u projektu.</span><span class="sxs-lookup"><span data-stu-id="8f023-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="8f023-118">Dodajte kupljenu količinu.</span><span class="sxs-lookup"><span data-stu-id="8f023-118">Add the quantity purchased.</span></span> <span data-ttu-id="8f023-119">Sistem će popuniti jediničnu cenu na osnovu konfiguracije cene zaliha na zalihama.</span><span class="sxs-lookup"><span data-stu-id="8f023-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="8f023-120">Potvrdite ukupan iznos i ostale potrebne detalje na liniji.</span><span class="sxs-lookup"><span data-stu-id="8f023-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="8f023-121">Na liniji detalji, na kartici **Projekat** odaberite ID projekta na koji će se snimati ova stavka.</span><span class="sxs-lookup"><span data-stu-id="8f023-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="8f023-122">Po želji odaberite broj aktivnosti i ažurirajte kategoriju projekta i svojstvo linije.</span><span class="sxs-lookup"><span data-stu-id="8f023-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="8f023-123">Pošaljite fakturu dobavljača na čekanju.</span><span class="sxs-lookup"><span data-stu-id="8f023-123">Post pending vendor invoice.</span></span> <span data-ttu-id="8f023-124">Kada je faktura knjižena, sistem beleži:</span><span class="sxs-lookup"><span data-stu-id="8f023-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="8f023-125">Iznos bilansa dobavljača.</span><span class="sxs-lookup"><span data-stu-id="8f023-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="8f023-126">Iznos poreza na promet.</span><span class="sxs-lookup"><span data-stu-id="8f023-126">The sales tax amount.</span></span>
    - <span data-ttu-id="8f023-127">Troškovi projekta evidentiraju se na račun integracije nabavki.</span><span class="sxs-lookup"><span data-stu-id="8f023-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="8f023-128">Stvarna transakcija projekta u Dataverse.</span><span class="sxs-lookup"><span data-stu-id="8f023-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="8f023-129">Ova transakcija se dalje obrađuje pomoću [Project Operations dnevnika integracije](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="8f023-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="8f023-130">Objavljivanjem ovog dnevnika premešta se iznos sa računa integracije nabavki na račun troškova projekta.</span><span class="sxs-lookup"><span data-stu-id="8f023-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
