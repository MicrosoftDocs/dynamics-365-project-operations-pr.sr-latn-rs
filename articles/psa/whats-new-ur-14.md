---
title: Šta je novo ili promenjeno u izdanju 14 ispravke Project Service Automation verzije 3
description: U ovoj temi date su informacije o tome šta je novo u izdanju ispravke 14 za Project Service Automation u verziji 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: e19c8ffe7d92ab7ec9eb46aff8f944c62b0bb4bc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281000"
---
# <a name="project-service-automation-update-release-14-v3"></a>Project Service Automation izdanje ispravke 14, u verziji 3

[!include [banner](../includes/psa-now-project-operations.md)]

Sa zadovoljstvo najavljujemo najnoviju ispravku za aplikaciju Dynamics 365 Project Service Automation (PSA). Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x. Da biste ažurirali ovo izdanje, posetite centar za administraciju za Dynamics 365 online i idite do stranice sa rešenjima kako biste instalirali ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

U ovoj temi date su funkcije koje su nove ili su promenjene u rešenju PSA u verziji 3, izdanje ispravke 14. Ova verzija ima broj verzije V3.10.4.21 i dostupna je prema sledećem planu:

- **Opšta dostupnost (samo-ispravka):** januar 2020. godine
- **Auto-ispravka:** februar 2020. godine

## <a name="update-release-14"></a>Izdanje ispravke 14

### <a name="enhancements"></a>Poboljšanja

- Sales

     - Vrednosti iz prilagođenih polja iz **Detalji stavke ponude** se kopiraju u **Detalji predmeta ugovora za projekat** kada se ponuda ispravi na **Zatvorena kao dobijena**.
     - Potvrđeni projekti mogu imati status **Zatvorena kao izgubljena**.

- Upravljanje resursima

     - Kada produžavate rezervacije, od korisnika će biti zatraženo da u dijalogu za potvrdu rezimiraju rezultate rezervacija i navedu vezu do opcije „Održavanje rezervacija“.


### <a name="bug-fixes"></a>Ispravke grešaka

- Vreme i trošak

     - Ispravljeno: poboljšano korisničko iskustvo kada korisnik nije izabrao nijednu stavku koju treba ispraviti.

- Upravljanje resursima

     - Ispravljeno: rezervacija resursa više puta prekoračuje ime resursa koji je moguće rezervisati.

- Sales

     - Ispravljeno: ukupna prodajna cena se ne izračunava sve dok korisnik ne unese i cenu koštanja za procene troškova za projekat.
     - Ispravljeno: zatvaranje ponude kao **Osvojena** ne uspeva ako ugovorni projekat nije u statusu **Radna verzija**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]