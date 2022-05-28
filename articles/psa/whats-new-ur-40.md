---
title: Šta je novo ili promenjeno u ažuriranju automatizacije usluge projekta Izdanje 40, V3
description: Ovaj tema navodi funkcije i ispravke koje su dostupne u izdanju Microsoft Dynamics 365 Project Service Automation Update Release 40, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 25f375ce648eb7d233f6433739832caee351830d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588661"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Šta je novo ili promenjeno u ažuriranju automatizacije usluge projekta Izdanje 40, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da najavimo najnoviju ispravku za aplikaciju Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Kompatibilna je sa sistemom Dynamics 365 9.x. Da biste se ažurirali na ovo izdanje, posetite stranicu centra administracije za Dynamics 365 mrežna rešenja i instalirajte ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).

Ovaj tema navodi funkcije i ispravke koje su nove ili promenjene za ispravku za automatizaciju usluge projekta Release 40, V3. Ova verzija ima broj verzije V3.10.61.61 i generalno je dostupna putem samostalnog ažuriranja u februaru 2022.

## <a name="update-release-40"></a>Izdanje ispravke 40

### <a name="features"></a>Funkcije
Prva faza nadogradnje sa Automatizacije projektnih usluga na projektne operacije - Lite biće objavljena u februaru 2022. godine svim kupcima. Da biste proverili da li ispunjava uslove, pogledajte [nadogradnju sa automatizacije projektne usluge na projektne operacije](upgrade-project-operations-non-stocked.md). Ako se aplikacija ne pojavi u vašoj instanci u Power Platform Centru za administraciju, obratite se podršci i zatražite da let bude omogućen za vaša okruženja. Vaš zahtev mora da sadrži listu ID-a okruženja gde je potrebno omogućiti let.

### <a name="bug-fixes"></a>Ispravke grešaka

Popravljeni su sledeći problemi.

**Vreme i trošak**
- Stavka note nedostaje kada je stavka vremena odbijena ili otkazana. 

**Prodaja**

- Kada ažurirate troškove ili procene prodaje korišćenjem dodatnih komponenti za izlazak iz kutije, neispravno vam je dozvoljeno da šaljete JSON tovare koji nisu važeći izvan korisničkog interfejsa.
- Kada ažurirate redove ponude pomoću brzog prikaza, dozvoljeno vam je da aktivirate ponude.
