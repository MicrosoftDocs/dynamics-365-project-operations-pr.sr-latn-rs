---
title: Skupovi odobrenja
description: Ova tema pruža informacije o skupu odobrenja, zahtevima i podskupovima tih operacija.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116888"
---
# <a name="approval-sets"></a><span data-ttu-id="a19b3-103">Skupovi odobrenja</span><span class="sxs-lookup"><span data-stu-id="a19b3-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a19b3-104">Skupovi odobrenja grupišu zahteve za odobrenje zajedno u manje podskupove operacija.</span><span class="sxs-lookup"><span data-stu-id="a19b3-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="a19b3-105">Ovo grupisanje omogućava obradu odobrenja u redosledu po projektu i omogućava ponovne pokušaje i sekvenciranja.</span><span class="sxs-lookup"><span data-stu-id="a19b3-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="a19b3-106">Grupisanje poboljšava pouzdanost i sledljivost obrade odobrenja za velike količine odobrenja.</span><span class="sxs-lookup"><span data-stu-id="a19b3-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="a19b3-107">Skupovi odobrenja ukazuju na celokupni status obrade njihovih povezanih zapisa.</span><span class="sxs-lookup"><span data-stu-id="a19b3-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="a19b3-108">Kada se zapis o odobrenju obrađuje pomoću skupa odobrenja, zapis se premešta sa **Prosleđeno** na **Odobreno** i raskida se njegova veza sa skupom odobrenja.</span><span class="sxs-lookup"><span data-stu-id="a19b3-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="a19b3-109">Ako zapis ne uspe kada se podnese na odobrenje, ostaće u statusu **Prosleđeno**, a skup odobrenja se označava kao neuspešan.</span><span class="sxs-lookup"><span data-stu-id="a19b3-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="a19b3-110">Skup odobrenja evidentira poruku o grešci neuspeha.</span><span class="sxs-lookup"><span data-stu-id="a19b3-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="a19b3-111">Obrada odobrenja i skupova odobrenja</span><span class="sxs-lookup"><span data-stu-id="a19b3-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="a19b3-112">Odobrenja koja su u redu za obradu vidljiva su u prikazu **Odobrenja obrade**.</span><span class="sxs-lookup"><span data-stu-id="a19b3-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="a19b3-113">Sistem pokušava da obradi sve stavke više puta asinhrono, uključujući ponovni pokušaj odobrenja ako prethodni pokušaji nisu uspeli.</span><span class="sxs-lookup"><span data-stu-id="a19b3-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="a19b3-114">Polje **Trajanje skupa odobrenja** evidentira broj pokušaja obrade skupa pre nego što se označi kao neuspešan.</span><span class="sxs-lookup"><span data-stu-id="a19b3-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="a19b3-115">Neuspela odobrenja i skupovi odobrenja</span><span class="sxs-lookup"><span data-stu-id="a19b3-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="a19b3-116">Prikaz **Neuspela odobrenja** navodi sva odobrenja koja zahtevaju intervenciju korisnika.</span><span class="sxs-lookup"><span data-stu-id="a19b3-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="a19b3-117">Otvorite povezane evidencije skupova odobrenja da biste identifikovali uzrok neuspeha.</span><span class="sxs-lookup"><span data-stu-id="a19b3-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="a19b3-118">Izbor **Pokušaj ponovo** povećava trajni broj skupova odobrenja, vraća skup odobrenja natrag u status **Obrada** i pokušava da obradi preostale zapise.</span><span class="sxs-lookup"><span data-stu-id="a19b3-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="a19b3-119">Konfigurisanje skupova odobrenja</span><span class="sxs-lookup"><span data-stu-id="a19b3-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="a19b3-120">Omogućavanje funkcije skupova odobrenja</span><span class="sxs-lookup"><span data-stu-id="a19b3-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="a19b3-121">Da biste omogućili funkciju Skupovi odobrenja, uverite se da trenutno nema odobrenja koja se obrađuju.</span><span class="sxs-lookup"><span data-stu-id="a19b3-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="a19b3-122">Idite na stranicu **Parametri projekta** i izaberite **Kontrola funkcija** > **Omogućavanje modernih odobrenja**.</span><span class="sxs-lookup"><span data-stu-id="a19b3-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="a19b3-123">Isključivanje funkcije skupova odobrenja</span><span class="sxs-lookup"><span data-stu-id="a19b3-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="a19b3-124">Da biste isključili funkciju Skupovi odobrenja, uverite se da trenutno nema odobrenja koja se obrađuju.</span><span class="sxs-lookup"><span data-stu-id="a19b3-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="a19b3-125">Idite na stranicu **Parametri projekta** i izaberite **Kontrola funkcija** > **Onemogućavanje modernih odobrenja**.</span><span class="sxs-lookup"><span data-stu-id="a19b3-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="a19b3-126">Konfigurisanje asinhrone granične vrednosti</span><span class="sxs-lookup"><span data-stu-id="a19b3-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="a19b3-127">Kada se kreiraju skupovi odobrenja, obrada se premešta u pozadinu kada izabrani broj zapisa za odobrenje pređe naznačenu graničnu vrednost.</span><span class="sxs-lookup"><span data-stu-id="a19b3-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="a19b3-128">Koristite polje **Asinhrona granična vrednost** da konfigurišete kada obradu odobrenja treba izvoditi sinhrono ili asinhrono.</span><span class="sxs-lookup"><span data-stu-id="a19b3-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="a19b3-129">Važeće vrednosti su:</span><span class="sxs-lookup"><span data-stu-id="a19b3-129">Valid values are:</span></span>

  - <span data-ttu-id="a19b3-130">Nula: Svi zahtevi treba da se obrađuju asinhrono.</span><span class="sxs-lookup"><span data-stu-id="a19b3-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="a19b3-131">Brojevi veći od nule: Odobrenja se obrađuju asinhrono samo kada prijavljeni broj odobrenja premaši ovu vrednost.</span><span class="sxs-lookup"><span data-stu-id="a19b3-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
