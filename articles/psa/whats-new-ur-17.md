---
title: Šta je novo ili promenjeno u izdanju 17 ispravke Project Service Automation verzije 3
description: U ovoj temi date su funkcije i ispravke koje su dostupne u izdanju 17 ispravke za Project Service Automation verzije 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 12df166e1bd1b5f0e11d79dc24122fb1ed7e6e6c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280820"
---
# <a name="project-service-automation-update-release-17-v3"></a>Project Service Automation izdanje ispravke 17, u verziji 3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti.  Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x. Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

U ovoj temi date su funkcije i ispravke koje su nove ili su promenjene u rešenju PSA u verziji 3, izdanje ispravke 17. Ova verzija ima broj verzije V3.10.6.34 i opšte je dostupna putem samo-ispravke u martu 2020. godine.


## <a name="update-release-17"></a>Izdanje ispravke 17

### <a name="bug-fixes"></a>Ispravke grešaka

**Opšti problemi**

- Ispravljeno: ažurirajte Project Service Automation za sprovođenje licenci za članove tima (Čvorište resursa za projekat će uključiti 3.x metapodatke plana usluge za članove tima)
 
**Vreme i trošak**

- Ispravljeno: nemogućnost promene procene troškova iz cene različite od nule u nulu (0). Promena se ignoriše.

**Upravljanje projektima**

- Ispravljeno: dodata je provera nultih vrednosti u ime pozicije člana tima.
- Ispravljeno: polje **msdyn_userresourceid** polje u entitetu **msdyn_resourceassignment** nije odobreno.
- Ispravljeno: nadogradnja sa 2.x na 3.x sada upravlja praznim konturama angažovanja u dodelama zadataka.

**Sales**

- Ispravljeno: **Invoice.PreValidateInvoiceUpdate** sada pravilno upravlja scenarijem ponovnog dodeljivanja vlasništva zapisa.
- Ispravljeno: kada je klasa transakcije **Vreme**, **UnitGroup** ne može da se uređuje ni za jedan entitet, uključujući **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** i **ContractLineDetails**. Međutim, **Jedinica** ne može da se uređuje samo za **JournalLine** i **InvoiceLineDetails**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]