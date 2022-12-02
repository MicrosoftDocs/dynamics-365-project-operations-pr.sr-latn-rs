---
title: Šta je novo ili promenjeno u izdanju 38 ispravke Project Service Automation verzije 3
description: U ovom članku navedene su funkcije i ispravke koje su dostupne u izdanju 38 ispravke usluge Microsoft Dynamics 365 Project Service Automation verzije 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
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
ms.openlocfilehash: ccc08cd0bc365bd4761424a4c0ceac91985e7c89
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915202"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Šta je novo ili promenjeno u izdanju 38 ispravke Project Service Automation verzije 3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da najavimo najnoviju ispravku za aplikaciju Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Kompatibilna je sa sistemom Dynamics 365 9.x. Da biste se ažurirali na ovo izdanje, posetite stranicu centra administracije za Dynamics 365 mrežna rešenja i instalirajte ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).

U ovom članku date su funkcije koje su nove ili su promenjene u rešenju Project Service Automation u verziji 3, izdanje ispravke 38. Ova verzija ima broj verzije V3.10.59.117 i generalno je dostupna putem samostalnog ažuriranja u decembru 2021.

## <a name="update-release-38"></a>Izdanje ispravke 38

### <a name="bug-fixes"></a>Ispravke grešaka

Popravljeni su sledeći problemi.

**Vreme i trošak**

- Do izuzetka dolazi kada dužina evidencije skupa odobrenja premašuje 100.000 zapisa.
- Korisnici ne mogu da pristupe matrici koordinatne mreže **Unos vremena** sa glavne stranice **Unos vremena**.
- Dijalog **Uvoz unosa vremena** ne prikazuje nikakav tekst kada nijedna stavka ne ispunjava uslove za uvoz.
- Korisnici mogu da kreiraju skupove odobrenja u kojima je polja **Status cilja** postavljen na **Nepoznato**.

**Upravljanje projektima**

- Konture nisu ispravno prikazane u dodelama resursa za UTC(+09:30) i UTC(+10:00) kada počne letnje/zimsko računanje vremena.
- Polje **Dodatna kolona** za strukturnu analizu posla skriveno je u nekim lokalnim standardima.
- Alatka za odabir datuma za kontrolu kalendara u matrici koordinatne mreže **Projektni zadatak** nije ispravno lokalizovana za kineski.

**Prodaja**

- Vrednosti za **Performanse ugovora** i **Stvarna vrednost troška na projektu** se ne podudaraju kada resursi koji se mogu rezervisati koji imaju različite jedinice ugovaranja i valute prosleđuju unose vremena.
- Prilagođeni tok posla za automatsko potvrđivanje faktura ne uspeva kada se fakture uvezu kao kompletno rešenje. Prikazana je sledeća poruka: „Microsoft.Xrm.Sdk.InvalidPluginExecutionException poruka: Nevažeći status fakture.“
- Kada je **Osnovno** izabrano kao opcija rezimiranja, a projekat ima procene iz mešavine klasa transakcija (npr. kombinacija vremena, troškova i procena materijala), sistem rezimira u klasama transakcija kao jedan red naknade.
- U slučajevima kada se stavka troška dodaje pre nego što je predmet ugovora povezan sa projektom, tačno određivanje cena se ne unosi kao podrazumevana vrednost u polje **Ažuriraj cenu**.
- Negativni iznosi prodaje nisu dozvoljeni u entitetima **Projekat** i **Zadatak**.
