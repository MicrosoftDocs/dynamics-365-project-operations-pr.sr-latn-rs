---
title: Šta je novo ili promenjeno u izdanju 23 ispravke Project Service Automation verzije 3
description: U ovoj temi date su funkcije i ispravke koje su dostupne u izdanju 23 ispravke za Project Service Automation verzije 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: cc918f1516d4751b3f8e70a93d8fc66058201f22
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581623"
---
# <a name="project-service-automation-update-release-23-v3"></a>Project Service Automation izdanje 23 ispravke verzije 3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x. Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).

U ovoj temi date su funkcije i ispravke koje su nove ili promenjene u rešenju Project Service Automation u verziji 3, izdanje ispravke 23. Ova verzija ima broj V3.10.34.30 i opšte je dostupna putem samostalne ispravke objavljene avgusta 2020.

## <a name="update-release-23"></a>Izdanje ispravke 23

### <a name="bug-fixes"></a>Ispravke grešaka

**Vreme i trošak**

Popravljeni su sledeći problemi:
- Rukujte graničnim slučajem u funkciji **Izbriši člana projektnog tima** da biste pružili smislen izuzetak.
- Uvoz zadatka rezultira praznim ekranom za uklanjanje.

**Upravljanje resursima**

Popravljeni su sledeći problemi:

- **Kartica resursa mreže za ukupnu iskorišćenost resursa** prikazuje netačne podatke kada je vremenska skala duža od pet dana.
- Kada klijenti kreiraju resurs koji može da se rezerviše, dodatna komponenta povremeno ne uspeva automatski da doda resurs u Microsoft Office 365 grupu.
- Prikaz **Usaglašenost** netačno prikazuje ručne konture u prikazu **Nedelja** ili **Mesec**.

**Upravljanje projektima**

Popravljeni su sledeći problemi:

- Prekomerni broj entiteta **RetrieveMultiple za podešavanja korisnika** uzrokuju pogoršane performanse za odobravanje projekata i druge operacije.
- Pronalaženje resursa mreže **Planiranje zadataka** ograničeno je na prikazivanje do pet članova tima iz projektnog tima. 
- Pronalaženje resursa mreže **Planiranje zadataka** ne filtrira neaktivne resurse.
- Ručni režim ne radi kako se očekuje u strukturnoj analizi posla na planiranju projekta.
- Mreža **Planiranje zadataka** pokazuje **Neaktivne kategorije transakcija**.
- Mreža **Dodeljivanje resursa** se nepravilno zaokružuje kada zadatak ima više dodela.
- Vrednosti zaokruživanja razlikuju se između planiranih troškova i stvarnih troškova za jedan zadatak.

**Sales**

Popravljeni su sledeći problemi:

- Dupli klik na **Preuzmi sve kategorije transakcija** kreira više linija.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
