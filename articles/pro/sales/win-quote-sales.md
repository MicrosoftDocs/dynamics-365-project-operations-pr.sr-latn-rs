---
title: Zatvaranje ponuda
description: Ova tema pruža informacije o zatvaranju ponude u usluzi Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896208"
---
# <a name="close-quotes"></a><span data-ttu-id="d2856-103">Zatvaranje ponuda</span><span class="sxs-lookup"><span data-stu-id="d2856-103">Close quotes</span></span> 

<span data-ttu-id="d2856-104">_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="d2856-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d2856-105">Ponuda za projekat može da se zatvori kao ostvarena ili neostvarena.</span><span class="sxs-lookup"><span data-stu-id="d2856-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="d2856-106">Budući da operacije Aktiviranje i Revizija nisu podržane u ponudama u usluzi Microsoft Dynamics 365 Project Operations, možete zatvoriti radnu verziju ponude.</span><span class="sxs-lookup"><span data-stu-id="d2856-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="d2856-107">Zatvaranje ponude kao ostvarene</span><span class="sxs-lookup"><span data-stu-id="d2856-107">Close a quote as Won</span></span>

<span data-ttu-id="d2856-108">Zatvaranje ponude za projekat kao ostvarene zatvoriće ponudu sa statusom postavljenim na Zatvoreno i razlogom statusa postavljenim na Ostvareno.</span><span class="sxs-lookup"><span data-stu-id="d2856-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="d2856-109">Zatvaranje ponude je postavlja ponudu za projekat u status samo za čitanje i kreira radnu verziju ugovora za projekat koja sadrži sve informacije iz ponude.</span><span class="sxs-lookup"><span data-stu-id="d2856-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="d2856-110">Postoji dijalog za potvrdu pre nego što se promene izvrše, jer se zatvorena ponuda ne može ponovo otvoriti i promene su nepovratne.</span><span class="sxs-lookup"><span data-stu-id="d2856-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="d2856-111">Ako priložite ponudu uz mogućnost za poslovanje, sve ostale ponude za projekat u mogućnosti za poslovanje automatski se zatvaraju kao neostvarene.</span><span class="sxs-lookup"><span data-stu-id="d2856-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="d2856-112">Finansijski uticaj zatvaranja ponude kao ostvarene</span><span class="sxs-lookup"><span data-stu-id="d2856-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="d2856-113">Ako postoje stvarni podaci za vreme zabeleženo na projektu dok je još uvek priložen uz radnu verziju ponude, beleže se samo troškovi vremena ili rashoda.</span><span class="sxs-lookup"><span data-stu-id="d2856-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="d2856-114">Nakon što se ponuda zatvori kao ostvarena, aplikacija će refaktorisati troškove storniranjem starijih stvarnih troškova i ponovnim kreiranjem novih stvarnih troškova.</span><span class="sxs-lookup"><span data-stu-id="d2856-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="d2856-115">Aplikacija će obraditi ove stvarne troškove na osnovu metode naplate povezanog predmeta ugovora o projektu.</span><span class="sxs-lookup"><span data-stu-id="d2856-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="d2856-116">Ako se stvarni iznosi troškova odnose na predmet ugovora o vremenu i materijalu, sistem će automatski kreirati odgovarajuće nefakturisane stvarne podatke o prodaji kada se ponuda zatvori i kreira projektni ugovor.</span><span class="sxs-lookup"><span data-stu-id="d2856-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="d2856-117">Ako se stvarni podaci o troškovima pozivaju na predmet ugovora sa fiksnom cenom, aplikacija će zaustaviti ponovnu obradu stvarnih troškova na osnovu pravila podeljenog obračuna za klijente po ugovoru o projektu.</span><span class="sxs-lookup"><span data-stu-id="d2856-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="d2856-118">Zatvaranje ponude kao neostvarene:</span><span class="sxs-lookup"><span data-stu-id="d2856-118">Closing a quote as lost:</span></span>

<span data-ttu-id="d2856-119">Zatvaranje ponude za projekat kao neostvarene postaviće status ponude na Zatvoreno a razlog statusa na Neostvareno.</span><span class="sxs-lookup"><span data-stu-id="d2856-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="d2856-120">Zatvaranje ponude postavlja ponudu za projekat u režim samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="d2856-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="d2856-121">Budući da zatvorenu ponudu ne možete ponovo otvoriti, pre nego što zatvorite ponudu, dijalog za potvrdu će potvrditi vaše promene.</span><span class="sxs-lookup"><span data-stu-id="d2856-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="d2856-122">Ako ponuda za projekat koja je zatvorena kao neostvarena ima projekat na koji se poziva bilo koji od njenih predmeta, taj projekat se takođe označava kao zatvoren i sve rezervacije za resurse od tog dana nadalje se otkazuju.</span><span class="sxs-lookup"><span data-stu-id="d2856-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="d2856-123">U usluzi Project Operations, zatvaranje ponude kao ostvarene ili neostvarene neće uticati na status mogućnosti za poslovanje, koja će ostati otvorena sve dok se ručno ne zatvori.</span><span class="sxs-lookup"><span data-stu-id="d2856-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
