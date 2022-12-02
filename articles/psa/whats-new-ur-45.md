---
title: Šta je novo ili promenjeno u izdanju 45 ispravke Project Service Automation verzije 3
description: U ovom članku navedene su funkcije i ispravke koje su dostupne u izdanju 45 ispravke usluge Microsoft Dynamics 365 Project Service Automation verzije 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169186"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Šta je novo ili promenjeno u izdanju 45 ispravke Project Service Automation verzije 3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da najavimo najnoviju ispravku za aplikaciju Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Kompatibilna je sa sistemom Dynamics 365 9.x. Da biste se ažurirali na ovo izdanje, posetite stranicu centra administracije za Dynamics 365 mrežna rešenja i instalirajte ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).

U ovom članku date su funkcije koje su nove ili su promenjene u rešenju Project Service Automation u verziji 3, izdanje ispravke 45. Ova verzija ima broj verzije 3.10.76.168 i opšte je dostupna putem samostalnog ažuriranja u julu 2022.

## <a name="update-release-45"></a>Izdanje ispravke 45

### <a name="bug-fixes"></a>Ispravke grešaka

Popravljeni su sledeći problemi.

**Prodaja**

- Korisnici ne mogu uspešno da kreiraju fakture nakon što pokušaju da kreiraju fakturu bez nenaplaćene prodaje, ako takođe prikazuju istu instancu stranice i ne osvežavaju je.

**Vreme i trošak**

- Kada su savremena odobrenja omogućena i opozvano odobrenje projekta je odobreno, faza zapisa se nepravilno ažurira u **Zahtev za opoziv je odobren**.
- Kada su savremena odobrenja omogućena i tokovi u oblaku su neaktivni, proces odobrenja nije uspešan, a korisnici koji prosleđuju ili odobravaju nisu obavešteni.
