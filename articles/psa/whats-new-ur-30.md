---
title: Šta je novo ili promenjeno u izdanju 30 ispravke Project Service Automation verzije 3
description: U ovoj temi date su funkcije i ispravke koje su dostupne u izdanju 30 ispravke za Project Service Automation verzije 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 07ca20425d05d1d638d9b2b8c3425562e39dd6627916794d1ad8441f00658459
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987003"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Šta je novo ili promenjeno u izdanju 30 ispravke Project Service Automation verzije 3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x. Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution.md).

U ovoj temi date su funkcije koje su nove ili su promenjene u rešenju Project Service Automation u verziji 3, izdanje ispravke 30. Broj izrade ove verzije je V3.10.51.61 i uglavnom je dostupna putem samostalnog ažuriranja u aprilu 2021. godine.

## <a name="update-release-30"></a>Izdanje ispravke 30

### <a name="bug-fixes"></a>Ispravke grešaka

**Vreme i trošak**

Popravljeni su sledeći problemi:

- Dolazi do greške kada kreirate i sačuvate stavku vremena na stranici **Brzo kreiranje** ako je polje **Uloga** uklonjeno.
- Filter za stavku vremena primenjuje pogrešan operator filtera.
- Kopirani vremenski listovi se ne prikazuju automatski kada izaberete **Kopiranje sedmice** na kontroli stavke vremena.

**Upravljanje resursima**

Popravljeni su sledeći problemi:

- Kada produžite rezervaciju, status rezervacije dodeljen fiksnoj rezervaciji je netačan. Produženjem rezervacije poštuje se status rezervacije definisan kao **Dodeljeno** u metapodacima podešavanja rezervacije.
- Kada nije naveden važeći status rezervacije, poruka o grešci nije pravilno lokalizovana.

**Upravljanje projektima**

Popravljeni su sledeći problemi:

- Projekti se ne mogu kreirati u jednoj valuti, a da uključuju povezane zadatke u drugoj valuti.

**Prodaja**

Popravljeni su sledeći problemi:

- Kada se kopira cenovnik, cene se ne ažuriraju.
- Zatvaranje ponude kao ostvarene ne uspeva kada detalj cene ima vrednost za poreklo.
- Na entitetu **Projektni zadatak**, **Procenjena cena** se preimenuje u **Planirana cena (osnovna)**.
- Izuzetak nulte reference se generiše kada se fakture kreiraju ili izbrišu.
