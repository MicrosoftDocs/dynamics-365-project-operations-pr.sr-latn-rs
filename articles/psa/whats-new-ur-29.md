---
title: Šta je novo ili promenjeno u izdanju 29 ispravke Project Service Automation verzije 3
description: Ovaj članak navodi funkcije i ispravke koje su dostupne u okviru ispravke za automatizaciju usluge projekta Release 29, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 733bbad53933b2de62222e78e3c5c919543c59e9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915386"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Šta je novo ili promenjeno u izdanju 29 ispravke Project Service Automation verzije 3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x. Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).

Ovaj članak navodi funkcije i ispravke koje su nove ili promenjene za V3 za automatizaciju projektne usluge, izdanje za ažuriranje 29. Ova verzija ima broj verzije V3.10.47.7 i generalno je dostupna putem samostalnog ažuriranja u februaru 2021.

## <a name="update-release-29"></a>Izdanje ispravke 29

### <a name="bug-fixes"></a>Ispravke grešaka

**Vreme i trošak**

Popravljeni su sledeći problemi:

- Korisnici ne mogu da vide radno vreme zabeleženo neradnim danima u mreži za unos vremena.
- Odobreni unosi troškova mogu se uređivati na mreži.

**Upravljanje projektima**

Popravljeni su sledeći problemi:

- Nedostaje logika validacije da bi se osiguralo da sati angažovanja za dodelu resursa ne mogu biti negativni.
- Prilagođena radnja, **AssignResourcesForTask** ažurira sva polja, a ne samo promenjena.
- Kada kopirate projekat u okruženju sa dodatnim komponentama ili tokovima posla koji su registrovani u događaju **CreateProject**, atribut **msdyn_bulkgenerationstatus** se ne ažurira ako je **CopyWBSToProject** neuspešan.
- Kada proširite kalendar projekta, radni dani se ne sortiraju u rastućem redosledu, što dovodi do neuspeha ažuriranja nekih projektnih zadataka.
- Promena menadžera projekta na postojećem projektu pokreće podrazumevanu logiku organizacione jedinice.

**Prodaja**

Popravljeni su sledeći problemi:

- Kartica **Izvršenje ugovora** na stranici **Ugovor** bez upozorenja ne uspeva tokom inicijalizacije kada nema linija ugovora.
