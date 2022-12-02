---
title: Šta je novo ili promenjeno u izdanju 43 ispravke Project Service Automation verzije 3
description: U ovom članku navedene su funkcije i ispravke koje su dostupne u izdanju 43 ispravke usluge Microsoft Dynamics 365 Project Service Automation verzije 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/04/2022
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
ms.openlocfilehash: b12cfda08f1ea1fc441782003130be445a437f7c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915339"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-43-v3"></a>Šta je novo ili promenjeno u izdanju 43 ispravke Project Service Automation verzije 3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da najavimo najnoviju ispravku za aplikaciju Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Kompatibilna je sa sistemom Dynamics 365 9.x. Da biste se ažurirali na ovo izdanje, posetite stranicu centra administracije za Dynamics 365 mrežna rešenja i instalirajte ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).

U ovom članku date su funkcije koje su nove ili su promenjene u rešenju Project Service Automation u verziji 3, izdanje ispravke 43. Broj izrade ove verzije je V3.10.74.200 i uglavnom je dostupna putem samostalnog ažuriranja u maju 2022. godine.

## <a name="update-release-43"></a>Izdanje ispravke 43

### <a name="bug-fixes"></a>Ispravke grešaka

Popravljeni su sledeći problemi.


**Vreme i trošak**

- Prilikom uvoza stavki vremena iz rezervacija ili dodeljivanja resursa, referenca na povezani resurs koji se može rezervisati se ne održava.
- Kada se matrica koordinatne mreže za unos vremena proširi na ceo ekran, kretanje kroz matricu koordinatne mreže pomoću tabulatora ne funkcioniše.
- Prilikom prosleđivanja stavke vremena koju je kreirao drugi korisnik, polje **Prosledio** se nepravilno popunjava korisnikom koji je kreirao vremenski list.
