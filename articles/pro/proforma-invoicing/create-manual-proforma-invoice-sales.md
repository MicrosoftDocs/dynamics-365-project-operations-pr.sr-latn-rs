---
title: Kreiranje ručnog predračuna – jednostavno
description: Ova tema pruža informacije o kreiranju ručnog predračuna u usluzi Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a924de6efc377e28a20e038e7deac04616b95aa
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764520"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="1650a-103">Kreiranje ručnog predračuna – jednostavno</span><span class="sxs-lookup"><span data-stu-id="1650a-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="1650a-104">_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="1650a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1650a-105">U usluzi Dynamics 365 Project Operations, profakture se po potrebi mogu kreirati ručno.</span><span class="sxs-lookup"><span data-stu-id="1650a-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="1650a-106">Možete ručno da kreirate predračun sa stranice lista **Ugovori o projektu** ili sa stranice sa detaljima **Ugovor o projektu**.</span><span class="sxs-lookup"><span data-stu-id="1650a-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="1650a-107">Stranica liste ugovora za projekat</span><span class="sxs-lookup"><span data-stu-id="1650a-107">Project Contracts list page</span></span>

<span data-ttu-id="1650a-108">Sa stranice liste **Ugovori o projektu** odaberite jedan ili više projektnih ugovora i kreirajte fakture za sve izabrane zapise.</span><span class="sxs-lookup"><span data-stu-id="1650a-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="1650a-109">Sistem proverava koji od izabranih projektnih ugovora ima zaostatak **Spremno za fakturisanje** datiran pre današnjeg datuma.</span><span class="sxs-lookup"><span data-stu-id="1650a-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="1650a-110">Od tih ugovora sistem kreira radne verzije predračuna.</span><span class="sxs-lookup"><span data-stu-id="1650a-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="1650a-111">Ako projektni ugovor ima više klijenata, može se kreirati jedna faktura po klijentu i više faktura po ugovoru o projektu.</span><span class="sxs-lookup"><span data-stu-id="1650a-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="1650a-112">Sve kreirane fakture projekta su dostupne na stranici **Faktura** u odeljku **Naplata** oblasti **Prodaja**.</span><span class="sxs-lookup"><span data-stu-id="1650a-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="1650a-113">Stranica sa detaljima ugovora za projekat</span><span class="sxs-lookup"><span data-stu-id="1650a-113">Project Contract details page</span></span>

<span data-ttu-id="1650a-114">Profaktura se takođe može kreirati na stranici sa detaljima **Ugovor o projektu**.</span><span class="sxs-lookup"><span data-stu-id="1650a-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="1650a-115">Sistem proverava da li projektni ugovor ima zaostatak **Spremno za fakturisanje** datiran pre današnjeg datuma.</span><span class="sxs-lookup"><span data-stu-id="1650a-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="1650a-116">Od ovih ugovora sistem kreira radne verzije predračuna na osnovu broja klijenata u svakom predmetu ugovora.</span><span class="sxs-lookup"><span data-stu-id="1650a-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="1650a-117">Kada se kreira jedan predračun, otvara se stranica **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="1650a-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="1650a-118">Ako se kreira više faktura za taj ugovor o projektu, otvara se stranica lista **Fakture** sa prikazom svih kreiranih faktura.</span><span class="sxs-lookup"><span data-stu-id="1650a-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>
