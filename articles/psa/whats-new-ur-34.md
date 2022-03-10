---
title: Šta je novo ili promenjeno u izdanju 34 ispravke usluge Project Service Automation verzije 3
description: U ovoj temi navedene su funkcije i ispravke koje su dostupne u izdanju 34 ispravke usluge Project Service Automation verzije 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: 528d4f8d108720cb9c912cea1c0d5f37e3716eec
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323298"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Šta je novo ili promenjeno u izdanju 34 ispravke usluge Project Service Automation verzije 3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da najavimo najnoviju ispravku za aplikaciju Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Kompatibilna je sa sistemom Dynamics 365 9.x. Da biste se ažurirali na ovo izdanje, posetite stranicu centra administracije za Dynamics 365 mrežna rešenja i instalirajte ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).

U ovoj temi navedene su funkcije koje su nove ili promenjene u izdanju 34 usluge Project Service Automation verzije 3. Ova verzija ima broj verzije 3.10.55.38 i opšte je dostupna putem samostalnog ažuriranja u julu 2021.

## <a name="update-release-34"></a>Izdanje ispravke 34

### <a name="bug-fixes"></a>Ispravke grešaka
Popravljeni su sledeći problemi.

**Opšte**

- Ažuriranja koja pokreće proizvođač ne aktiviraju novi savremeni tok odobravanja.
- Atributi **Ciljani status** i **Tip radnje** nedostaju na glavnoj stranici **Skup odobrenja**.

**Vreme i trošak**

- Nije moguće odobriti zahtev za opoziv koristeći savremeni tok odobrenja.
- Kopiranje jedne sedmice stavki vremena ne funkcioniše kada kopirate unose koji nisu povezani sa prijavljenim korisnikom.

**Planiranje projekta**

- Konture dodele resursa su oštećene pri uvozu iz programskog dodatka usluge Microsoft Project za računare.

**Upravljanje resursima**

- Kada objavite projekat iz programskog dodatka za uslugu Microsoft Project za računare, datum završetka postojećih zahteva se menja.
- Decimalna preciznost prelazi dva decimalna mesta u dijalogu za potvrdu produženja rezervacije.

**Prodaja**

- Kada ugovoru o projektu dodate stavku zasnovanu na proizvodu sa postojećim proizvodom, prikazuje se izuzetak **ključ nije pronađen u rečniku**.
- Potencijalni klijenti se ne mogu kvalifikovati kada se vrsta naloga mapira iz potencijalnog klijenta u mogućnost za poslovanje.
