---
title: Zatvaranje ponude – jednostavno
description: Ova tema pruža informacije o zatvaranju ponude u usluzi Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75345fed57dcbdb84f2a82587c7d0c152530c72b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994153"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="70014-103">Zatvaranje ponude – jednostavno</span><span class="sxs-lookup"><span data-stu-id="70014-103">Close a quote - lite</span></span>

<span data-ttu-id="70014-104">_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="70014-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="70014-105">Ponuda za projekat može da se zatvori kao ostvarena ili neostvarena.</span><span class="sxs-lookup"><span data-stu-id="70014-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="70014-106">Radna verzija ponude može da se zatvori jer Microsoft Dynamics 365 Project Operations ne podržava operacije Aktiviraj i Revidiraj za ponude.</span><span class="sxs-lookup"><span data-stu-id="70014-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="70014-107">Zatvaranje ponude kao ostvarene</span><span class="sxs-lookup"><span data-stu-id="70014-107">Close a quote as Won</span></span>

<span data-ttu-id="70014-108">Kada zatvorite ponudu za projekat kao Dobijenu, status se podešava na Zatvoreno, a razlog statusa je Dobijeno.</span><span class="sxs-lookup"><span data-stu-id="70014-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="70014-109">Zatvaranje ponude je postavlja ponudu za projekat u status samo za čitanje i kreira radnu verziju ugovora za projekat koja sadrži sve informacije iz ponude.</span><span class="sxs-lookup"><span data-stu-id="70014-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="70014-110">Budući da zatvorena ponuda ne može ponovo da se otvori, dijalog za potvrdu će potvrditi vaše promene.</span><span class="sxs-lookup"><span data-stu-id="70014-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="70014-111">Ako priložite ponudu uz mogućnost za poslovanje, sve ostale ponude za projekat u mogućnosti za poslovanje automatski se zatvaraju kao neostvarene.</span><span class="sxs-lookup"><span data-stu-id="70014-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="70014-112">Finansijski uticaj zatvaranja ponude kao ostvarene</span><span class="sxs-lookup"><span data-stu-id="70014-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="70014-113">Ako postoje stvarni podaci o vremenu na projektu, dok je on još uvek priložen uz radnu verziju ponude, evidentiraju se samo troškovi vremena ili troškovi.</span><span class="sxs-lookup"><span data-stu-id="70014-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="70014-114">Nakon što se ponuda zatvori kao ostvarena, aplikacija će refaktorisati troškove storniranjem starijih stvarnih troškova i ponovnim kreiranjem novih stvarnih troškova.</span><span class="sxs-lookup"><span data-stu-id="70014-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="70014-115">Aplikacija će obraditi ove stvarne troškove na osnovu metode naplate povezanog predmeta ugovora o projektu.</span><span class="sxs-lookup"><span data-stu-id="70014-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="70014-116">Ako se stvarni podaci o troškovima odnose na predmet ugovora za vreme i materijal, odgovarajuće nenaplaćene stvarne prodajne vrednosti kreiraju se kada se ponuda zatvori i kreira projektni ugovor.</span><span class="sxs-lookup"><span data-stu-id="70014-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="70014-117">Ako se stvarni podaci o troškovima odnose na predmet ugovora sa fiksnom cenom, aplikacija će zaustaviti ponovnu obradu stvarnih troškova koji se zasnivaju na pravilima deljene naplate za klijente ugovora o projektu.</span><span class="sxs-lookup"><span data-stu-id="70014-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="70014-118">Zatvaranje ponude kao neostvarene:</span><span class="sxs-lookup"><span data-stu-id="70014-118">Closing a quote as lost:</span></span>

<span data-ttu-id="70014-119">Kada zatvorite ponudu za projekat kao Neostvarenu, status se podešava na Zatvoreno, a razlog statusa je Neostvareno.</span><span class="sxs-lookup"><span data-stu-id="70014-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="70014-120">Zatvaranje ponude postavlja ponudu za projekat u režim samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="70014-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="70014-121">Budući da zatvorenu ponudu ne možete ponovo otvoriti, pre nego što zatvorite ponudu, dijalog za potvrdu će potvrditi vaše promene.</span><span class="sxs-lookup"><span data-stu-id="70014-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="70014-122">Ako se ponuda projekta koja je zatvorena kao Neostvarena odnosi na projekat u bilo kom redu, taj projekat je takođe označen kao Zatvoren.</span><span class="sxs-lookup"><span data-stu-id="70014-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="70014-123">Sve rezervacije resursa od tog dana nadalje otkazuju se.</span><span class="sxs-lookup"><span data-stu-id="70014-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="70014-124">U usluzi Project Operations, zatvaranje ponude kao ostvarene ili neostvarene neće uticati na status mogućnosti za poslovanje, koja će ostati otvorena sve dok se ručno ne zatvori.</span><span class="sxs-lookup"><span data-stu-id="70014-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]