---
title: Dodavanje novih obrazaca prilagođenih entiteta (Project Service Automation 2. x)
description: Ova tema pruža informacije o dodavanju prilagođenih obrazaca entiteta za mogućnosti za poslovanje, ponude, porudžbine ili fakture u aplikaciji Dynamics 365 Project Service Automation 2.x.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: e59e343887ef59ee28bee13346a0c9bf3ad7df27346e2a4f3f02a1e5c08c060f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995238"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Dodavanje novih obrazaca prilagođenih entiteta (Project Service Automation 2. x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>Polje Tip 

Dynamics 365 Project Service Automation se oslanja na polje **Tip** (**msdyn\_ordertype**) entiteta Mogućnost za poslovanje, Ponuda, Porudžbine i Faktura da bi napravila razlika između verzija ovih entiteta **zasnovanih na poslu** i onih **zasnovanih na stavci** i **usluzi**. PSA upravlja verzijama ovih entiteta zasnovanih na poslu. Veliki deo poslovne logike na klijentskoj strani i na strani servera rešenja zavisi od polja **Tip**. Zbog toga je važno da se ovo polje pokrene sa tačnom vrednošću prilikom kreiranja entiteta. Netačna vrednost može prouzrokovati nepravilna ponašanja, a neka poslovna logika neće ispravno raditi.

## <a name="automatic-form-switching"></a>Automatsko prebacivanje obrazaca

Da bi se izbegla potencijalna oštećenja podataka i neočekivano ponašanje koji su posledica nepravilnog pokretanja i uređivanja zapisa entiteta prodaje, PSA sada uključuje logiku za automatsko prebacivanje obrazaca u unapred definisane obrasce. Ova logika preusmerava korisnike na pravi obrazac za rad sa verzijom zasnovanom na poslu ili bilo koji drugi tip entiteta mogućnosti za poslovanje, ponude, porudžbine ili fakture. Kada korisnik otvori verziju entiteta Mogućnost za poslovanje, Ponuda, Porudžbine ili Faktura, koja je zasnovanu na poslu, obrazac se prebacuje u **Informacije o projektu**.

Logika automatskog prebacivanja obrasca oslanja se na mapiranje između vrednosti **formId** i polja **msdyn\_ordertype**. Svi unapred definisani obrasci su dodati tom mapiranju. Međutim, prilagođeni obrasci moraju se ručno dodati da bi se naznačilo kojom verzijom entiteta bi trebalo da upravljaju. Ovo je zasnovano na polju **msdyn\_ordertype**. Ako se prebacivanje obrasca ne nalazi na mapiranju, logika će se prebaciti na unapred definisani obrazac, na osnovu vrednosti sačuvane u polju **msdyn\_ordertype** entiteta.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Dodavanje prilagođenih obrazaca i uključivanje logike promene obrasca

Sledeći primer prikazuje kako se dodaje prilagođeni obrazac, **Moje informacije o projektu**, tako da funkcioniše sa mogućnostima za poslovanje zasnovanim na poslu. Isti proces se koristi za dodavanje prilagođenih obrazaca kako bi funkcionisale sa ponudama, porudžbinama i fakturama.

Sledite ove korake da biste kreirali prilagođenu verziju obrasca **Informacije o projektu**.

1. U entitetu Mogućnost za poslovanje otvorite obrazac **Informacije o projektu** i sačuvajte kopiju pod imenom **Moje informacije o projektu**.
2. Otvorite novi obrazac, a zatim u svojstvima proverite da li se tu nalaze skripte za pokretanje obrasca iz obrasca **Informacije o projektu**. 

    > [!IMPORTANT]
    > Nemojte uklanjati skripte. U suprotnom, neki podaci mogu biti nepravilno pokrenuti.

3. Proverite da se polje **Tip** (**msdyn\_ordertype**) nalazi u obrascu. 

    > [!IMPORTANT]
    > Nemojte uklanjati ovo polje. U suprotnom, skripte za pokretanja neće uspeti.

4. Pronađite vrednost **formId** novog obrasca. Ovaj korak možete da obavite na dva načina:

    - Izvezite obrazac **Moje informacije o projektu** kao deo nekompletnog rešenja, a zatim potražite vrednost **formId** u datoteci customization.xml u izvezenom rešenju.
    - Otvorite obrazac **Moje informacije o projektu** u uređivaču obrazaca, a zatim potražite univerzalni jedinstveni identifikator (GUID) pored parametra **fromId** u URL adresi, kao što je prikazano na sledećoj ilustraciji.

    ![Vrednost formId novog obrasca u URL adresi.](media/how-to-add-custom-forms-in-v2.0.png)

5. Kreirajte mapiranje **msdyn\_ordertype** za vrednost **formId** uređivanjem veb-resursa msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js. Uklonite kôd iz resursa i zamenite ga sledećim kodom.

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

6. Sačuvajte, a zatim objavite prilagođavanja.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]