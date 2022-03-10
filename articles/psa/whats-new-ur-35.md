---
title: Šta je novo ili promenjeno u izdanju 35 ispravke usluge Project Service Automation verzije 3
description: U ovoj temi navedene su funkcije i ispravke koje su dostupne u izdanju 35 ispravke usluge Microsoft Dynamics 365 Project Service Automation verzije 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.openlocfilehash: 53670e2c7f54f8fccf636b2855e190f5f85c6068
ms.sourcegitcommit: 5bb8ca5055deda57e2b1173a2e45c53b15f61d62
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/03/2021
ms.locfileid: "7473282"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Šta je novo ili promenjeno u izdanju 35 ispravke usluge Project Service Automation verzije 3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da najavimo najnoviju ispravku za aplikaciju Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Kompatibilna je sa sistemom Dynamics 365 9.x. Da biste se ažurirali na ovo izdanje, posetite stranicu centra administracije za Dynamics 365 mrežna rešenja i instalirajte ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).

U ovoj temi date su funkcije koje su nove ili su promenjene u rešenju Project Service Automation u verziji 3, izdanje ispravke 35. Ova verzija ima broj verzije 3.10.56.110 i opšte je dostupna putem samostalnog ažuriranja u septembru 2021.

## <a name="update-release-35"></a>Izdanje ispravke 35

### <a name="bug-fixes"></a>Ispravke grešaka

Popravljeni su sledeći problemi.

**Vreme i trošak**

- Osoba koja odobrava projekat dobija grešku vezanu za privilegije čitanja kada odobri stavke troškova pomoću uloge **Osoba koja odobrava projekat**.
- Osoba koja odobrava projekat prima grešku vezanu za privilegije upisivanja na **msdyn_projectapproval** kada otkaže odobreni unos vremena pomoću uloge **Osoba koja odobrava projekat**.
- Kada izaberete **Kopiraj nedelju** u vremenskom unosu u modulu aplikacije Dynamics 365 za telefon – Čvorište resursa za projekat dolazi do sledeće greške: „...\OfficeProductivity_RibbonRules.js.map: HTTP error: status code 404, net::ERR_HTTP_RESPONSE_CODE_FAILURE“.
- Smernice **Pokušaj ponovo** automatski odobravaju unose koji su prethodno odbijeni.
- Podforma **Skupovi odobrenja** prikazuje neprimenljive radnje na traci.
- Ikone nedostaju za **Zadatak projekta** i **Uloga resursa** na entitetu **Stavka vremena**.
- Kada uvozite zadatke resursa, uvezeni unosi vremena nemaju ispravno trajanje za zadatke koji su kreirani kroz zadatke ručnog režima.
- **Izbriši** nedostaje na stranici **Napredna pretraga zapisa stavki vremena**.
- **Sačuvaj** nedostaje na stranici **Informacije o stavci vremena**. Ovaj problem sprečava čuvanje promena kada se stranica zatvori.

**Planiranje projekta**

- Mreže **Dodeljivanje resursa** i **Usklađivanje resursa** ne sortiraju grupisane atribute po abecedi.
- Zadaci se ne mogu kreirati ako je ponašanje datuma prilagođeno na **Samo datum**.

**Upravljanje resursima**

- Ako su instalirani i Dynamics 365 Field Service i Project Service Automation, problemi sa preklapanjem se javljaju kada je **Vezani prikaz zahteva resursa** povezan sa glavnom stranicom.
- Dvostrukim klikom na **Sačuvaj** u dijalogu **Brzo kreiranje člana tima** sprečavate kreiranje zahteva za resursima.

**Prodaja**

- Izuzetak se pojavljuje ako izbrišete zadatak koji je povezan sa ponudom koja ima status **Dobijeno**.