---
title: Šta je novo ili promenjeno u izdanju 31 ispravke Project Service Automation verzije 3
description: U ovoj temi date su funkcije i ispravke koje su dostupne u izdanju 31 ispravke za Project Service Automation verzije 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 2e5fce003c25f9c5911e5a01fb4ec3e19c06c078e00b054472699a522b9cd070
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002168"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Šta je novo ili promenjeno u izdanju 31 ispravke Project Service Automation verzije 3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x. Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).

U ovoj temi date su funkcije koje su nove ili su promenjene u rešenju Project Service Automation u verziji 3, izdanje ispravke 31. Broj izrade ove verzije je V3.10.52.77 i uglavnom je dostupna putem samostalnog ažuriranja u maju 2021. godine.

## <a name="update-release-31"></a>Izdanje ispravke 31

### <a name="bug-fixes"></a>Ispravke grešaka

**Vreme i trošak**

Popravljeni su sledeći problemi:

- Komandna dugmad za kontrolu unosa vremena na stranici **Resurs koji može da se rezerviše** su zbunjivala korisnike.
- Nulti izuzetak reference je generisan u **Project.SetTrackingFields** prilikom odobravanja unosa vremena.

**Upravljanje resursima**

Popravljeni su sledeći problemi:

- **Napravite člana tima** ne prikazuje ispravno podešavanje metapodataka za podešavanje rezervacije za **Podrazumevani status poslate rezervacije**.
- Prilikom nadogradnje sa PSA 1.X to 3.X, proces nadogradnje ne uspeva na **UpgradeResourceRequirements**.


**Prodaja**

Popravljeni su sledeći problemi:

- Stvarni prihod pretvara iznose u valutu projekta u mreži za praćenje.
- Zadana valuta nije jasna prilikom kreiranja redova dnevnika, citata i linija ugovora u scenarijima kada se osnovna valuta organizacije razlikuje od valute projekta.
- Upit **validacije dnevnika ispravki na čekanju** se ne filtrira prema projektu.
- Preostala prodaja se na projektu pogrešno izračunava.
- Ponude zasnovane na kontaktu ne uspevaju kada se kreiraju bez cenovnika.
- Kada odaberete **Potvrdite fakturu**, ne prikazuje se znak obrade.
- Kada odaberete **Kreiraj fakturu**, ne prikazuje se znak obrade.
- Zatvaranje ponude kao izgubljene ne otkazuje rezervacije.







