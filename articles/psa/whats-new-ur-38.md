---
title: Šta je novo ili promenjeno u ažuriranju automatizacije usluge projekta Izdanje 38, V3
description: Ovaj tema navodi funkcije i ispravke koje su dostupne u Microsoft Dynamics 365 Project Service Automation izdanju Update Release 38, V3.
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
ms.openlocfilehash: 1e5175b12c9e06962888bf09c8e07119b9505dda
ms.sourcegitcommit: 2aba2082d50b20b596ee86735045644cd647c2b0
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 12/08/2021
ms.locfileid: "7901517"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Šta je novo ili promenjeno u ažuriranju automatizacije usluge projekta Izdanje 38, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da najavimo najnoviju ispravku za aplikaciju Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Kompatibilna je sa sistemom Dynamics 365 9.x. Da biste se ažurirali na ovo izdanje, posetite stranicu centra administracije za Dynamics 365 mrežna rešenja i instalirajte ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).

Ovaj tema navodi funkcije i ispravke koje su nove ili promenjene za ispravku za automatizaciju usluge projekta Release 38, V3. Ova verzija ima broj verzije V3.10.59.117 i generalno je dostupna putem samostalnog ažuriranja u decembru 2021.

## <a name="update-release-38"></a>Izdanje ispravke 38

### <a name="bug-fixes"></a>Ispravke grešaka

Popravljeni su sledeći problemi.

**Vreme i trošak**

- Do izuzetka dolazi kada dužina evidencije skupa odobravanja premašuje 100.000 zapisa.
- Korisnici ne mogu da pristupe koordinatnoj **mreži za unos vremena sa** **glavne stranice** stavke vremena.
- Dijalog **"Uvoz** vremenske stavke" ne prikazuje tekst kada nijedna stavka nije podobna za uvoz.
- Korisnici mogu da kreiraju skupove odobravanja u **kojima je polje** "Ciljni status" postavljeno na **"Nepoznato".**

**Upravljanje projektima**

- Konture nisu ispravno prikazane u dodelama resursa za UTC(+09:30) i UTC(+10:00) kada počne letnje/zimsko računanje vremena.
- Polje **"Dodatna** kolona" za strukture radne analize skriveno je u nekim lokalnim standardima.
- Izbor datuma za kontrolu kalendara u **koordinatnoj mreži** projektnog zadatka nije ispravno lokalizovan za kineski.

**Prodaja**

- **Performanse** ugovora **i vrednosti stvarnih** troškova projekta se ne podudaraju kada resursi koji se mogu rezervisati i koji imaju različite jedinice ugovora i valute prosleđuju stavke vremena.
- Prilagođeni tok posla za automatsko potvrđivanje faktura ne uspeva kada se fakture uvezu kao kompletno rešenje. Prikazana je sledeća poruka: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException Message: Nevažeći status fakture".
- Kada je Root izabran kao opcija rezimacije, a projekat ima procene iz mešavine klasa **transakcija** (npr. kombinacija vremena, troškova i procena materijala), sistem rezimira u klasama transakcija kao red pojedinačne naknade.
- U slučajevima kada se red troška dodaje pre nego što je red ugovora povezan sa projektom, tačne cene se ne unose kao podrazumevana vrednost **u polje Ažuriraj** cenu.
- Negativni iznosi prodaje nisu dozvoljeni u **entitetima** projekta i **zadataka**.
