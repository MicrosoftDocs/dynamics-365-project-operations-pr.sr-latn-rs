---
title: Ažuriranje atributa dodatnih komponenti tako da uključuju nove dimenzije za određivanje cena
description: Ova tema pruža informacije o ažuriranju atributa dodatnih komponenti za dimenzije određivanja cena.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 603b0e9a10dc2fe23c9fa0fa7065bc3f500dc540
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147085"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Ažuriranje atributa dodatnih komponenti tako da uključuju nove dimenzije za određivanje cena

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> Ako ne koristite Project Service Automation (PSA) funkcije za davanja ponuda i ugovaranje, možete preskočiti ovu temu.

Ova tema pretpostavlja da ste dovršili procedure u temama, [Kreiranje prilagođenih polja i entiteta](create-custom-fields-entities.md), [Dodavanje prilagođenih polja u podešavanje cena i entitete transakcije](field-references.md) i [Podešavanje prilagođenih polja kao dimenzija za određivanje cena](set-up-pricing-dimensions.md). Ako niste dovršili te procedure, vratite se i dovršite ih, a zatim se vratite na ovu temu.

Kada se na stranici **Stavka ponude** kreira detalj stavke ponude za stavku ponude za projekat, sistem kreira dve stavke procene u pozadini, jednu stavku za troškovni deo procene i jednu za prodajnu stranu. Ovo je isto za predmete ugovora o projektu.

Kada promenite količinu ili polje na strani troškova, ta promena se prenosi na stranu prodaje. Ovo je moguće zbog sledećih dodatnih komponenti koje moraju biti ponovo registrovane posle promene dimenzija za određivanje cena.

- PreOperationContractLineDetailUpdate - Ispravke **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate - Ispravke **msdyn_quotelinetransaction**.

Sledeći koraci vas vode kroz proces registracije dodatnih komponenti.

1. Otvorite **PluginRegistrationTool** i povežite se sa instancom na mreži.
2. Kliknite na **Pretraga** i potražite dodatnu komponentu za ažuriranje.

 ![Snimak ekrana stabla za pretragu](media/PRT-1.png)

3. Nakon što pronađete dodatnu komponentu, izaberite je, a zatim kliknite na **Izaberi u glavnom obrascu**.

4. Izaberite korak dodatne komponente za ažuriranje, kliknite desnim tasterom miša, a zatim izaberite **Ažuriraj**.

 ![Snimak ekrana dodatne komponente za ažuriranje](media/PRT-2.png)
 
5. U prozoru za ažuriranje kliknite na tri tačke (**...**) u atributima filtriranja.

 ![Snimak ekrana sa informacijama za konfigurisanje ažuriranja postojećeg koraka](media/PRT-3.png)
 
6. Izaberite polja za potvrdu atributa za određivanje cena.

 ![Snimak ekrana koji prikazuje izbor u polju za potvrdu za atribute određivanja cena](media/PRT-4.png)

7. Kliknite na **U redu** da zatvorite stranicu, a zatim izaberite **Ažuriraj korak**.

 ![Snimak ekrana koji prikazuje dugme „Ažuriraj korak“](media/PRT-5.png)
 
8. Ponovite ovaj postupak za drugu dodatnu komponentu, **PreOperationQuoteLineDetail - Ispravka za msdyn_quotelinetransaction**.

9. Zatvorite alatku za registrovanje dodatne komponente.

