---
title: Šta je novo ili promenjeno u Project Service Automation izdanju ispravke 19 u verziji 3
description: Ovaj članak navodi funkcije i ispravke koje su dostupne u izdanju za ažuriranje automatizacije usluge projekta Release 19, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: a17275220eec726107e8ce5f82bdf5cdd403033e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915523"
---
# <a name="project-service-automation-update-release-19-v3"></a>Project Service Automation izdanje ispravke 19, u verziji 3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x. Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).

Ovaj članak navodi funkcije i ispravke koje su nove ili promenjene za PSA V3, Izdanje za ažuriranje 19. Broj izrade ove verzije je V3.10.30.41 i uglavnom je dostupna putem samostalnog ažuriranja u maju 2020. godine.

## <a name="update-release-19"></a>Izdanje ispravke 19

### <a name="bug-fixes"></a>Ispravke grešaka

**Vreme i trošak**

Popravljeni su sledeći problemi: 

- Greške nastale prilikom uvoza u stavki vremena se ne pojavljuju ispravno.
- Mreža stavke vremena ne podržava ponašanje polja **Samo datum**.
- Resursi projekta ne mogu da kreiraju trošak sa projektom.

**Upravljanje projektima**

Popravljeni su sledeći problemi: 

-  Drugostepeni podređeni zadatak uzrokuje pogrešnu procenu zalaganja tokom izračunavanja završetka (EAC).

**Sales**

Popravljeni su sledeći problemi: 

- Radnja **Ponovno izračunavanje** ne funkcioniše sa detaljima o troškovima predmeta ugovora ili detaljima stavke ponude.
- **Ažuriranje cena** nedostaje za procene troškova.
-  Klijenti ne mogu da izaberu prilagođene razloge statusa ugovora sa stranice **Projektni ugovor**.
- Klijenti imaju smanjene performanse kada kreiraju prilagođeni cenovnik iz ponude.
- Klijenti doživljavaju nedoslednost sa podrazumevanim vrednostima za **jedinicu** na stranicama **Detalji stavke ponude** i **Detalji predmeta ugovora**.
- Dodavanje stavki iz kategorije nenaplativih transakcija u naplativi predmet ugovora neće se poštovati tip obračuna **Nije naplativo** kategorije transakcije.
- Klijenti ne mogu da koriste novododate uloge i kategoriju na prethodno kreiranim ugovorima.
- Klijenti imaju smanjene performanse Nepotrebnog umanjenja u PreValidateProjectTeamMemberUpdate.cs
- Uloge koje su podešene kao nenaplative na listi **Kategorije resursa** trebaju biti dodate na karticu **Naplative uloge** kao **Nenaplative** na predmetu ugovora za projekat.
- Klijenti mogu imati smanjene performanse prilikom kreiranja projekta jer **GetBookableResourceIdFromUser** pribavlja sve kolone resursa koji mogu da se rezervišu umesto samo primarni ID.
- Entitetu **Tip transakcije** nedostaje dodatna komponenta za prethodnu validaciju da spreči korisnike da unose **Jedinice** i **UnitGroups** koje nisu važeće za tipove transakcija.
- Korak **Ukloni** ne radi za uvoz stavke vremena.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
