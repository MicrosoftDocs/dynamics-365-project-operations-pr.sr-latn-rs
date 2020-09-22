---
title: Ažuriranje atributa dodatnih komponenti tako da uključuju nove dimenzije za određivanje cena
description: Ova tema pruža informacije o ažuriranju atributa dodatnih komponenti za dimenzije određivanja cena.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: e9b7e752-39c3-4610-8ced-25d9e197b705
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 746b9978f9ae63c05e1031afc31c8134f05ec195
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755203"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="4e3be-103">Ažuriranje atributa dodatnih komponenti tako da uključuju nove dimenzije za određivanje cena</span><span class="sxs-lookup"><span data-stu-id="4e3be-103">Update plug-in attributes to include new pricing dimensions</span></span>

> [!NOTE]
> <span data-ttu-id="4e3be-104">Ako ne koristite Project Service Automation (PSA) funkcije za davanja ponuda i ugovaranje, možete preskočiti ovu temu.</span><span class="sxs-lookup"><span data-stu-id="4e3be-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="4e3be-105">Ova tema pretpostavlja da ste dovršili procedure u temama, [Kreiranje prilagođenih polja i entiteta](create-custom-fields-entities.md), [Dodavanje prilagođenih polja u podešavanje cena i entitete transakcije](field-references.md) i [Podešavanje prilagođenih polja kao dimenzija za određivanje cena](set-up-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="4e3be-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="4e3be-106">Ako niste dovršili te procedure, vratite se i dovršite ih, a zatim se vratite na ovu temu.</span><span class="sxs-lookup"><span data-stu-id="4e3be-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="4e3be-107">Kada se na stranici **Stavka ponude** kreira detalj stavke ponude za stavku ponude za projekat, sistem kreira dve stavke procene u pozadini, jednu stavku za troškovni deo procene i jednu za prodajnu stranu.</span><span class="sxs-lookup"><span data-stu-id="4e3be-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="4e3be-108">Ovo je isto za predmete ugovora o projektu.</span><span class="sxs-lookup"><span data-stu-id="4e3be-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="4e3be-109">Kada promenite količinu ili polje na strani troškova, ta promena se prenosi na stranu prodaje.</span><span class="sxs-lookup"><span data-stu-id="4e3be-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="4e3be-110">Ovo je moguće zbog sledećih dodatnih komponenti koje moraju biti ponovo registrovane posle promene dimenzija za određivanje cena.</span><span class="sxs-lookup"><span data-stu-id="4e3be-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="4e3be-111">PreOperationContractLineDetailUpdate - Ispravke **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="4e3be-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="4e3be-112">PreOperationQuoteLineDetailUpdate - Ispravke **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="4e3be-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="4e3be-113">Sledeći koraci vas vode kroz proces registracije dodatnih komponenti.</span><span class="sxs-lookup"><span data-stu-id="4e3be-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="4e3be-114">Otvorite **PluginRegistrationTool** i povežite se sa instancom na mreži.</span><span class="sxs-lookup"><span data-stu-id="4e3be-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="4e3be-115">Kliknite na **Pretraga** i potražite dodatnu komponentu za ažuriranje.</span><span class="sxs-lookup"><span data-stu-id="4e3be-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Snimak ekrana stabla za pretragu](media/PRT-1.png)

3. <span data-ttu-id="4e3be-117">Nakon što pronađete dodatnu komponentu, izaberite je, a zatim kliknite na **Izaberi u glavnom obrascu**.</span><span class="sxs-lookup"><span data-stu-id="4e3be-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="4e3be-118">Izaberite korak dodatne komponente za ažuriranje, kliknite desnim tasterom miša, a zatim izaberite **Ažuriraj**.</span><span class="sxs-lookup"><span data-stu-id="4e3be-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Snimak ekrana dodatne komponente za ažuriranje](media/PRT-2.png)
 
5. <span data-ttu-id="4e3be-120">U prozoru za ažuriranje kliknite na tri tačke (**...**) u atributima filtriranja.</span><span class="sxs-lookup"><span data-stu-id="4e3be-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![Snimak ekrana sa informacijama za konfigurisanje ažuriranja postojećeg koraka](media/PRT-3.png)
 
6. <span data-ttu-id="4e3be-122">Izaberite polja za potvrdu atributa za određivanje cena.</span><span class="sxs-lookup"><span data-stu-id="4e3be-122">Select the pricing attribute check boxes.</span></span>

 ![Snimak ekrana koji prikazuje izbor u polju za potvrdu za atribute određivanja cena](media/PRT-4.png)

7. <span data-ttu-id="4e3be-124">Kliknite na **U redu** da zatvorite stranicu, a zatim izaberite **Ažuriraj korak**.</span><span class="sxs-lookup"><span data-stu-id="4e3be-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Snimak ekrana koji prikazuje dugme „Ažuriraj korak“](media/PRT-5.png)
 
8. <span data-ttu-id="4e3be-126">Ponovite ovaj postupak za drugu dodatnu komponentu, **PreOperationQuoteLineDetail - Ispravka za msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="4e3be-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="4e3be-127">Zatvorite alatku za registrovanje dodatne komponente.</span><span class="sxs-lookup"><span data-stu-id="4e3be-127">Close the plug-in registration tool.</span></span>

