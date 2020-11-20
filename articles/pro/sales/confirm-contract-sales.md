---
title: Potvrdite ugovor za projekat
description: Ova tema pruža informacije o načinu potvrđivanja ugovora u usluzi Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24da0887c0266d51bddcbbf8efd6f2644b6d0f4f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128300"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="1be06-103">Potvrdite ugovor za projekat</span><span class="sxs-lookup"><span data-stu-id="1be06-103">Confirm a project contract</span></span>

<span data-ttu-id="1be06-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="1be06-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1be06-105">Ugovor za projekat u programu Dynamics 365 Project Operations može biti aktivan sa razlogom **Potvrđeno** ili zatvoren sa razlogom **Izgubljeno**.</span><span class="sxs-lookup"><span data-stu-id="1be06-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed**, or closed with a reason of **Lost**.</span></span> <span data-ttu-id="1be06-106">Kada potvrdite ugovor o projektu, status se ažurira sa **Radna verzija** na **Aktivno**, a razlog statusa je **Potvrđeno**.</span><span class="sxs-lookup"><span data-stu-id="1be06-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="1be06-107">Aktivni ili zatvoreni ugovor ne može se uređivati ili ponovo otvarati.</span><span class="sxs-lookup"><span data-stu-id="1be06-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="1be06-108">Finansijski uticaj potvrđivanja ugovora za projekat</span><span class="sxs-lookup"><span data-stu-id="1be06-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="1be06-109">Nakon što se ugovor za projekat potvrdi, aplikacija će ponovo izračunati troškove storniranjem starijih stvarnih troškova i kreiranjem novih stvarnih troškova.</span><span class="sxs-lookup"><span data-stu-id="1be06-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="1be06-110">Novi stvarni troškovi se zatim obrađuju na osnovu metode naplate povezanog predmeta ugovora o projektu.</span><span class="sxs-lookup"><span data-stu-id="1be06-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="1be06-111">Ako se stvarni troškovi odnose na predmet ugovora o vremenu i materijalu, aplikacija automatski ponovo kreira odgovarajuće nenaplaćene stvarne troškove prodaje.</span><span class="sxs-lookup"><span data-stu-id="1be06-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="1be06-112">Ako se stvarni podaci o troškovima odnose na predmet ugovora sa fiksnom cenom, aplikacija zaustavlja ponovnu obradu stvarnih troškova.</span><span class="sxs-lookup"><span data-stu-id="1be06-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="1be06-113">Ograničenja koja se ne smeju premašiti, podešavanje naplativosti i utvrđivanje cena i troškova na stvarnim podacima procenjuju se, a zatim ažuriraju kao deo procesa potvrde.</span><span class="sxs-lookup"><span data-stu-id="1be06-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="1be06-114">Zatvorite ugovor za projekat kao izgubljen</span><span class="sxs-lookup"><span data-stu-id="1be06-114">Close a project contract as lost</span></span>

<span data-ttu-id="1be06-115">Kada ugovor o projektu zatvorite kao izgubljen, status ugovora se ažurira na **Zatvoreno**, a razlog statusa je **Izgubljeno**.</span><span class="sxs-lookup"><span data-stu-id="1be06-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="1be06-116">Ugovor o projektu postaje samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="1be06-116">The project contract becomes read-only.</span></span> <span data-ttu-id="1be06-117">Dijalog za potvrdu se navodi pre nego što se promene dovrše jer ne možete ponovo otvoriti zatvoreni ugovor o projektu.</span><span class="sxs-lookup"><span data-stu-id="1be06-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="1be06-118">Ako ugovor o projektu koji je zatvoren kao izgubljen upućuje na projekat na svojim stavkama, taj projekat je takođe označen kao zatvoren.</span><span class="sxs-lookup"><span data-stu-id="1be06-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="1be06-119">Sve rezervacije resursa od tog dana nadalje otkazuju se.</span><span class="sxs-lookup"><span data-stu-id="1be06-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="1be06-120">Svi nenaplaćeni stvarni troškovi prodaje na ugovoru za projekt koji već nisu na fakturi biće stornirani.</span><span class="sxs-lookup"><span data-stu-id="1be06-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="1be06-121">U usluzi Dynamics 365 Project Operations, zatvaranje ugovora o projektu kao izgubljenog neće uticati na taj status povezane mogućnosti za poslovanje.</span><span class="sxs-lookup"><span data-stu-id="1be06-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="1be06-122">Mogućnost za poslovanje će ostati otvorena i mora se ručno zatvoriti.</span><span class="sxs-lookup"><span data-stu-id="1be06-122">The opportunity will remain open and must be manually closed.</span></span>
