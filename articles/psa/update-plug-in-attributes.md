---
title: Ažuriranje atributa dodatnih komponenti tako da uključuju nove dimenzije za određivanje cena
description: Ovaj članak pruža informacije o ažuriranju atributa dodatne komponente za dimenzije cena.
author: Rumant
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 459aefb510cc9a9ec55a86ca7e362db98ccabb70
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913223"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Ažuriranje atributa dodatnih komponenti tako da uključuju nove dimenzije za određivanje cena

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> Ako ne koristite funkcije za automatizaciju usluge projekta (PSA) za citiranje i ugovaranje, možete da preskočite ovaj članak.

Ovaj članak pretpostavlja da ste dovršili procedure u člancima, [kreirali prilagođena polja i entitete,](create-custom-fields-entities.md) dodali prilagođena polja [u podešavanje cena i transakcione entitete i](field-references.md) podesili prilagođena polja [kao dimenzije cena](set-up-pricing-dimensions.md). Ako niste završili te procedure, vratite se i dovršite ih, a zatim se vratite na ovaj članak.

Kada se na stranici **Stavka ponude** kreira detalj stavke ponude za stavku ponude za projekat, sistem kreira dve stavke procene u pozadini, jednu stavku za troškovni deo procene i jednu za prodajnu stranu. Ovo je isto za predmete ugovora o projektu.

Kada promenite količinu ili polje na strani troškova, ta promena se prenosi na stranu prodaje. Ovo je moguće zbog sledećih dodatnih komponenti koje moraju biti ponovo registrovane posle promene dimenzija za određivanje cena.

- PreOperationContractLineDetailUpdate - Ispravke **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate - Ispravke **msdyn_quotelinetransaction**.

Sledeći koraci vas vode kroz proces registracije dodatnih komponenti.

1. Otvorite **PluginRegistrationTool** i povežite se sa instancom na mreži.
2. Kliknite na **Pretraga** i potražite dodatnu komponentu za ažuriranje.

 ![Snimak ekrana stabla za pretragu.](media/PRT-1.png)

3. Nakon što pronađete dodatnu komponentu, izaberite je, a zatim kliknite na **Izaberi u glavnom obrascu**.

4. Izaberite korak dodatne komponente za ažuriranje, kliknite desnim tasterom miša, a zatim izaberite **Ažuriraj**.

 ![Snimak ekrana dodatne komponente za ažuriranje.](media/PRT-2.png)
 
5. U prozoru za ažuriranje kliknite na tri tačke (**...**) u atributima filtriranja.

 ![Snimak ekrana sa informacijama za konfigurisanje ažuriranja postojećeg koraka.](media/PRT-3.png)
 
6. Izaberite polja za potvrdu atributa za određivanje cena.

 ![Snimak ekrana koji prikazuje izbor u polju za potvrdu za atribute određivanja cena.](media/PRT-4.png)

7. Kliknite na **U redu** da zatvorite stranicu, a zatim izaberite **Ažuriraj korak**.

 ![Snimak ekrana koji prikazuje dugme „Ažuriraj korak“.](media/PRT-5.png)
 
8. Ponovite ovaj postupak za drugu dodatnu komponentu, **PreOperationQuoteLineDetail - Ispravka za msdyn_quotelinetransaction**.

9. Zatvorite alatku za registrovanje dodatne komponente.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
