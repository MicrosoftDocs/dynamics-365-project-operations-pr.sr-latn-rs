---
title: Potrebe za uslovnim rezervisanjem
description: Ova tema pruža informacije o tome kako da rezervišete resurse prema potrebama za uslovnim rezervisanjem.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bc58c805bfe1a3087600b8d4a6be2d1bcdd18188
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997933"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="e37a9-103">Potrebe za uslovnim rezervisanjem</span><span class="sxs-lookup"><span data-stu-id="e37a9-103">Soft-book requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e37a9-104">Potreba za resursom može se fiksno rezervisati.</span><span class="sxs-lookup"><span data-stu-id="e37a9-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="e37a9-105">Fiksna rezervacija kreira predlog koji troši kapacitet resursa.</span><span class="sxs-lookup"><span data-stu-id="e37a9-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="e37a9-106">Predlog se zatim vraća podnosiocu zahteva na odobrenje.</span><span class="sxs-lookup"><span data-stu-id="e37a9-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="e37a9-107">Uslovno rezervisanje privremeno dodaje resurs u projektni tim i ima drugačiji status u tabeli rasporeda, ali ne troši kapacitet resursa.</span><span class="sxs-lookup"><span data-stu-id="e37a9-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="e37a9-108">Da biste uslovno rezervisali resurs iz tabele rasporeda, podesite polje **Status rezervacije** na **Uslovna**.</span><span class="sxs-lookup"><span data-stu-id="e37a9-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![Status rezervacije je podešen na Uslovna](media/Resource-Management-image77.png)

<span data-ttu-id="e37a9-110">Kada kartica **Tim** ima prikaz **Imenovani članovi tima**, resurs se pojavljuje tamo.</span><span class="sxs-lookup"><span data-stu-id="e37a9-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="e37a9-111">Uslovno rezervisani sati se evidentiraju u koloni **Uslovno rezervisani sati**.</span><span class="sxs-lookup"><span data-stu-id="e37a9-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Uslovno rezervisani sati u prikazu Imenovani članovi tima](media/Resource-Management-image78.png)

<span data-ttu-id="e37a9-113">Uslovno rezervisani članovi tima mogu biti dodeljeni zadacima.</span><span class="sxs-lookup"><span data-stu-id="e37a9-113">Soft-booked team members can be assigned to tasks.</span></span>

![Uslovno rezervisan član tima je dodeljen zadatku](media/Resource-Management-image79.png)

<span data-ttu-id="e37a9-115">Na kartici **Usaglašenost** nisu prikazane rezervacije uslovno rezervisanog resursa jer kartica **Usaglašenost** uzima u obzir samo fiksne rezervacije.</span><span class="sxs-lookup"><span data-stu-id="e37a9-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Uslovno rezervisan resurs bez rezervacija na kartici Usaglašenost](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="e37a9-117">Ne možete uslovno da rezervišete resurs iz potrebe koja je generisana od generičkog člana tima.</span><span class="sxs-lookup"><span data-stu-id="e37a9-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="e37a9-118">Na tabeli rasporeda upotrebljava se drugačija boja za uslovne rezervacije resursa.</span><span class="sxs-lookup"><span data-stu-id="e37a9-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Uslovne rezervacije u tabeli rasporeda](media/Resource-Management-image81.png)

<span data-ttu-id="e37a9-120">Da biste uslovnu rezervaciju pretvorili u fiksnu, u tabeli rasporeda kliknite desnim tasterom miša na uslovna rezervacija, a zatim izaberite **Promeni status** \> **Fiksna rezervacija** \> **Fiksna**.</span><span class="sxs-lookup"><span data-stu-id="e37a9-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![Promena statusa rezervacije u Fiksna](media/Resource-Management-image82.png)

<span data-ttu-id="e37a9-122">Rezervacija je promenjena i status se menja u tabeli rasporeda.</span><span class="sxs-lookup"><span data-stu-id="e37a9-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="e37a9-123">Pošto je status rezervacije sada **Fiksna**, resurs je prikazan kao rezervisan, a njegov kapacitet i dostupnost su prilagođeni.</span><span class="sxs-lookup"><span data-stu-id="e37a9-123">Because the booking status is now **Hard**, the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="e37a9-124">Možete upotrebiti isti metod da otkažete fiksnu rezervaciju ili uslovnu rezervaciju u tabeli rasporeda.</span><span class="sxs-lookup"><span data-stu-id="e37a9-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="e37a9-125">Da biste pretvorili resurs koji je uslovno rezervisan u fiksno rezervisan na kartici projekta **Tim**, izaberite resurs, a zatim izaberite **Potvrdi**.</span><span class="sxs-lookup"><span data-stu-id="e37a9-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Komanda za potvrdu](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]