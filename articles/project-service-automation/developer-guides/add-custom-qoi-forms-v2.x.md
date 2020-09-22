---
title: Dodavanje novih obrazaca prilagođenih entiteta (Project Service Automation 2. x)
description: Ova tema pruža informacije o dodavanju prilagođenih obrazaca entiteta za mogućnosti za poslovanje, ponude, porudžbine ili fakture u aplikaciji Dynamics 365 Project Service Automation 2.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 9eb9fc5e-4c7d-466c-9362-fdb0faa30506
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
ms.openlocfilehash: 2bd955ad3eb26d31676ac4ad387baccaee913cd2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755077"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="1d618-103">Dodavanje novih obrazaca prilagođenih entiteta (Project Service Automation 2. x)</span><span class="sxs-lookup"><span data-stu-id="1d618-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

## <a name="type-field"></a><span data-ttu-id="1d618-104">Polje Tip</span><span class="sxs-lookup"><span data-stu-id="1d618-104">Type field</span></span> 

<span data-ttu-id="1d618-105">Dynamics 365 Project Service Automation se oslanja na polje **Tip** (**msdyn\_ordertype**) entiteta Mogućnost za poslovanje, Ponuda, Porudžbine i Faktura da bi napravila razlika između verzija ovih entiteta **zasnovanih na poslu** i onih **zasnovanih na stavci** i **usluzi**.</span><span class="sxs-lookup"><span data-stu-id="1d618-105">Dynamics 365 Project Service Automation relies on the **Type** (**msdyn\_ordertype**) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="1d618-106">PSA upravlja verzijama ovih entiteta zasnovanih na poslu.</span><span class="sxs-lookup"><span data-stu-id="1d618-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="1d618-107">Veliki deo poslovne logike na klijentskoj strani i na strani servera rešenja zavisi od polja **Tip**.</span><span class="sxs-lookup"><span data-stu-id="1d618-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="1d618-108">Zbog toga je važno da se ovo polje pokrene sa tačnom vrednošću prilikom kreiranja entiteta.</span><span class="sxs-lookup"><span data-stu-id="1d618-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="1d618-109">Netačna vrednost može prouzrokovati nepravilna ponašanja, a neka poslovna logika neće ispravno raditi.</span><span class="sxs-lookup"><span data-stu-id="1d618-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="1d618-110">Automatsko prebacivanje obrazaca</span><span class="sxs-lookup"><span data-stu-id="1d618-110">Automatic form switching</span></span>

<span data-ttu-id="1d618-111">Da bi se izbegla potencijalna oštećenja podataka i neočekivano ponašanje koji su posledica nepravilnog pokretanja i uređivanja zapisa entiteta prodaje, PSA sada uključuje logiku za automatsko prebacivanje obrazaca u unapred definisane obrasce.</span><span class="sxs-lookup"><span data-stu-id="1d618-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="1d618-112">Ova logika preusmerava korisnike na pravi obrazac za rad sa verzijom zasnovanom na poslu ili bilo koji drugi tip entiteta mogućnosti za poslovanje, ponude, porudžbine ili fakture.</span><span class="sxs-lookup"><span data-stu-id="1d618-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="1d618-113">Kada korisnik otvori verziju entiteta Mogućnost za poslovanje, Ponuda, Porudžbine ili Faktura, koja je zasnovanu na poslu, obrazac se prebacuje u **Informacije o projektu**.</span><span class="sxs-lookup"><span data-stu-id="1d618-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="1d618-114">Logika automatskog prebacivanja obrasca oslanja se na mapiranje između vrednosti **formId** i polja **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="1d618-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="1d618-115">Svi unapred definisani obrasci su dodati tom mapiranju.</span><span class="sxs-lookup"><span data-stu-id="1d618-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="1d618-116">Međutim, prilagođeni obrasci moraju se ručno dodati da bi se naznačilo kojom verzijom entiteta bi trebalo da upravljaju.</span><span class="sxs-lookup"><span data-stu-id="1d618-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="1d618-117">Ovo je zasnovano na polju **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="1d618-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="1d618-118">Ako se prebacivanje obrasca ne nalazi na mapiranju, logika će se prebaciti na unapred definisani obrazac, na osnovu vrednosti sačuvane u polju **msdyn\_ordertype** entiteta.</span><span class="sxs-lookup"><span data-stu-id="1d618-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="1d618-119">Dodavanje prilagođenih obrazaca i uključivanje logike promene obrasca</span><span class="sxs-lookup"><span data-stu-id="1d618-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="1d618-120">Sledeći primer prikazuje kako se dodaje prilagođeni obrazac, **Moje informacije o projektu**, tako da funkcioniše sa mogućnostima za poslovanje zasnovanim na poslu.</span><span class="sxs-lookup"><span data-stu-id="1d618-120">The following example shows how to add a custom form, **My Project Information**, so that it works with work-based opportunities.</span></span> <span data-ttu-id="1d618-121">Isti proces se koristi za dodavanje prilagođenih obrazaca kako bi funkcionisale sa ponudama, porudžbinama i fakturama.</span><span class="sxs-lookup"><span data-stu-id="1d618-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="1d618-122">Sledite ove korake da biste kreirali prilagođenu verziju obrasca **Informacije o projektu**.</span><span class="sxs-lookup"><span data-stu-id="1d618-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="1d618-123">U entitetu Mogućnost za poslovanje otvorite obrazac **Informacije o projektu** i sačuvajte kopiju pod imenom **Moje informacije o projektu**.</span><span class="sxs-lookup"><span data-stu-id="1d618-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="1d618-124">Otvorite novi obrazac, a zatim u svojstvima proverite da li se tu nalaze skripte za pokretanje obrasca iz obrasca **Informacije o projektu**.</span><span class="sxs-lookup"><span data-stu-id="1d618-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="1d618-125">Nemojte uklanjati skripte.</span><span class="sxs-lookup"><span data-stu-id="1d618-125">Don't remove the scripts.</span></span> <span data-ttu-id="1d618-126">U suprotnom, neki podaci mogu biti nepravilno pokrenuti.</span><span class="sxs-lookup"><span data-stu-id="1d618-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="1d618-127">Proverite da se polje **Tip** (**msdyn\_ordertype**) nalazi u obrascu.</span><span class="sxs-lookup"><span data-stu-id="1d618-127">Verify that the **Type** (**msdyn\_ordertype**) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="1d618-128">Nemojte uklanjati ovo polje.</span><span class="sxs-lookup"><span data-stu-id="1d618-128">Don't remove this field.</span></span> <span data-ttu-id="1d618-129">U suprotnom, skripte za pokretanja neće uspeti.</span><span class="sxs-lookup"><span data-stu-id="1d618-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="1d618-130">Pronađite vrednost **formId** novog obrasca.</span><span class="sxs-lookup"><span data-stu-id="1d618-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="1d618-131">Ovaj korak možete da obavite na dva načina:</span><span class="sxs-lookup"><span data-stu-id="1d618-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="1d618-132">Izvezite obrazac **Moje informacije o projektu** kao deo nekompletnog rešenja, a zatim potražite vrednost **formId** u datoteci customization.xml u izvezenom rešenju.</span><span class="sxs-lookup"><span data-stu-id="1d618-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="1d618-133">Otvorite obrazac **Moje informacije o projektu** u uređivaču obrazaca, a zatim potražite univerzalni jedinstveni identifikator (GUID) pored parametra **fromId** u URL adresi, kao što je prikazano na sledećoj ilustraciji.</span><span class="sxs-lookup"><span data-stu-id="1d618-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![Vrednost formId novog obrasca u URL adresi](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="1d618-135">Kreirajte mapiranje **msdyn\_ordertype** za vrednost **formId** uređivanjem veb-resursa msdyn\_/Dokument prodaje/PSSalesDocumentCustomFormIds.js.</span><span class="sxs-lookup"><span data-stu-id="1d618-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="1d618-136">Uklonite kôd iz resursa i zamenite ga sledećim kodom.</span><span class="sxs-lookup"><span data-stu-id="1d618-136">Remove the code from the resource, and replace it with the following code.</span></span>

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. <span data-ttu-id="1d618-137">Sačuvajte, a zatim objavite prilagođavanja.</span><span class="sxs-lookup"><span data-stu-id="1d618-137">Save and then publish the customizations.</span></span>
