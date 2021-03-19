---
title: Ažuriranje atributa dodatnih komponenti sa novim aspektima za određivanje cena
description: Ova tema pruža informacije o tome kako da ažurirate atribute dodatnih komponenti za dimenzije određivanja cena.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7999c003a0cf670d586ebf4445901e106fbee39f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274700"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="45e83-103">Ažurirajte atribute dodatnih komponenti sa novim aspektima za određivanje cena</span><span class="sxs-lookup"><span data-stu-id="45e83-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="45e83-104">Ova tema pruža informacije o tome kako da ažurirate atribute dodatnih komponenti za dimenzije određivanja cena.</span><span class="sxs-lookup"><span data-stu-id="45e83-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="45e83-105">Ova tema je primenljiva samo na funkcije ponude i ugovora u usluzi Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="45e83-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="45e83-106">Preduslovi</span><span class="sxs-lookup"><span data-stu-id="45e83-106">Prerequisites</span></span>
<span data-ttu-id="45e83-107">Pre nego što dovršite korake u ovoj temi, morate dovršiti procedure u sledećim temama:</span><span class="sxs-lookup"><span data-stu-id="45e83-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="45e83-108">Kreiranje prilagođenih polja i entiteta</span><span class="sxs-lookup"><span data-stu-id="45e83-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="45e83-109">Dodavanje prilagođenih polja u podešavanje cena i entitete transakcije </span><span class="sxs-lookup"><span data-stu-id="45e83-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="45e83-110">[Podešavanje prilagođenih polja kao dimenzija za određivanje cena](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="45e83-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="45e83-111">Ako niste dovršili te procedure, dovršite ih, a zatim se vratite na ovu temu.</span><span class="sxs-lookup"><span data-stu-id="45e83-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="45e83-112">Registrovanje dodatne komponente</span><span class="sxs-lookup"><span data-stu-id="45e83-112">Register a plug-in</span></span>
<span data-ttu-id="45e83-113">Kada kreirate detalj stavke ponude na stranici **Stavka ponude** za stavku ponude projekta, sistem kreira dve stavke procene.</span><span class="sxs-lookup"><span data-stu-id="45e83-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="45e83-114">Jedna stavka je za troškovnu stranu procene, a druga stavka za prodajnu stranu.</span><span class="sxs-lookup"><span data-stu-id="45e83-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="45e83-115">Ovo je isto za predmete ugovora o projektu.</span><span class="sxs-lookup"><span data-stu-id="45e83-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="45e83-116">Kada promenite količinu ili polje na strani troškova, ta promena se vrši i na strani prodaje.</span><span class="sxs-lookup"><span data-stu-id="45e83-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="45e83-117">To je moguće jer dodatne komponente PreOperation na Quotelinedetail i stavkama detalja za contractline povezuju određene atribute na troškovnoj strani sa prodajnom stranom transakcije.</span><span class="sxs-lookup"><span data-stu-id="45e83-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="45e83-118">Ako su vam potrebne izmene vrednosti dimenzija formiranja cena na prodajnoj strani da bi se izvršile i na troškovnoj strani, sledeće dodatne komponente moraju da se ponovo registruju nakon unošenja promena u dimenziju formiranja cene.</span><span class="sxs-lookup"><span data-stu-id="45e83-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="45e83-119">Ovo su dodatne komponente za ažuriranje i ponovnu registraciju:</span><span class="sxs-lookup"><span data-stu-id="45e83-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="45e83-120">PreOperationContractLineDetailUpdate – **Update msdyn_orderlinetransaction**</span><span class="sxs-lookup"><span data-stu-id="45e83-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="45e83-121">PreOperationQuoteLineDetailUpdate – **Updates msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="45e83-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="45e83-122">Dovršite sledeće korake da biste ažurirali i ponovo registrovali dodatne komponente.</span><span class="sxs-lookup"><span data-stu-id="45e83-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="45e83-123">Otvorite **PluginRegistrationTool** i povežite se sa svojim Project Operations Dataverse okruženjem.</span><span class="sxs-lookup"><span data-stu-id="45e83-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="45e83-124">Izaberite **Pretraga** i otkucajte prvih nekoliko slova dodatne komponente koji treba da se ažurira.</span><span class="sxs-lookup"><span data-stu-id="45e83-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="45e83-125">Nakon što pronađete dodatnu komponentu, izaberite je, a zatim izaberite **Izaberi u glavnom obrascu**.</span><span class="sxs-lookup"><span data-stu-id="45e83-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="45e83-126">Izaberite korak **Ažuriraj msdyn_orderlinetransaction**, kliknite desnim tasterom i izaberite **Ažuriraj**.</span><span class="sxs-lookup"><span data-stu-id="45e83-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="45e83-127">Na stranici sa dijalogom **Ažuriraj** , izaberite tri tačke (**...**) u atributima filtriranja.</span><span class="sxs-lookup"><span data-stu-id="45e83-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="45e83-128">Otvara se prozor filtriranja atributa i navodi spisak svih atributa u entitetu i dimenzijama formiranja cena.</span><span class="sxs-lookup"><span data-stu-id="45e83-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="45e83-129">Izaberite polja za potvrdu za atribute dimenzije formiranja cena.</span><span class="sxs-lookup"><span data-stu-id="45e83-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="45e83-130">Izaberite **U redu** da zatvorite stranicu, a zatim izaberite **Ažuriraj korak**.</span><span class="sxs-lookup"><span data-stu-id="45e83-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="45e83-131">Ponovite korake od 2-7 za drugu dodatnu komponentu, **PreOperationQuoteLineDetail**.</span><span class="sxs-lookup"><span data-stu-id="45e83-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="45e83-132">Za ovu dodatnu komponentu, morate da ažurirate korak **Update of msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="45e83-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="45e83-133">Zatvorite **PluginRegistrationTool**.</span><span class="sxs-lookup"><span data-stu-id="45e83-133">Close **PluginRegistrationTool**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]