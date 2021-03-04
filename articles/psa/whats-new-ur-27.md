---
title: Šta je novo ili promenjeno u izdanju ispravke 27 usluge Project Service Automation verzije 3
description: U ovoj temi su navedene funkcije i ispravke koje su dostupne u izdanju ispravke 27 za Project Service Automation verzije 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 6b9da3ec54ec10408774945d26db9e702c858d05
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146680"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Šta je novo ili promenjeno u izdanju ispravke 27 usluge Project Service Automation verzije 3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x. Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

U ovoj temi su navedene funkcije i ispravke koje su nove ili promenjene u izdanju ispravke 27 za Project Service Automation verzije 3. Ova verzija ima broj verzije V3.10.45.98 i opšte je dostupna putem samo-ispravke u januaru 2021. godine.

## <a name="update-release-27"></a>Izdanje ispravke 27

### <a name="bug-fixes"></a>Ispravke grešaka

**Opšti problemi**

Popravljeni su sledeći problemi:

- Evidencija koju generišu programski dodaci u usluzi Project Service Automation nije podešena na automatsko brisanje.
- Automatska nadogradnja ne uspeva jer rešenje Project Service Automation sadrži zastareli NavBarArea bez vrednosti i element naslova.

**Vreme i trošak**

Popravljeni su sledeći problemi:

- Mreža **Unos vremena** prikazuje netačne podatke za ponašanje datuma **Nezavisno od vremenske zone**.
- Mreža **Unos vremena** kreira netačno vreme za ponašanje datuma **Nezavisno od vremenske zone**.
- Pronalaženje zadataka nije ograničeno na izabrani projekat na stranici **Izmena unosa vremena**.
- Odobrenje vremena za stavke vremena koje se ne odnose na projekat je blokirano jer sistem traži odobravaoca projekta.
- Ispravni unosi za stvarne vrednosti prikazuju poruku o grešci za netačan unos.
- Kada zadatak sadrži nultu vrednost za stvarne troškove i ukupni troškovi projekta se osvežavaju, javlja se sledeća greška: „Dati ključ nije prisutan u rečniku“.
- U određenim slučajevima, filteri **Grupiši prema** na kartici **Procena projekta** ne prikazuju procene troškova.
- Interval **Letnje računanje vremena** nije tačan za unose vremena.

**Upravljanje projektima**

Popravljeni su sledeći problemi:

- Poboljšanja keširanja, što poboljšava performanse povezane sa učitavanjem stranice **Projekat**.
- Zastarelo poslovno pravilo koje sprečava izvršenje projektnih zadataka.
- Konture programskog dodataka za Microsoft Project ne poštuju kalendar programskog dodataka što rezultira netačnim zahtevima za resurse.
- Kreiranje projekata iz šablona netačno podešava datume dodeljivanja resursa i sprečava mogućnost generisanja zahteva za resurse.
- Korisnik ne može da pristupi opcijama **Kategorija**, **Opis** i **Status** pomoću tastature.
- Stvarne prodajne vrednosti projekta ne uključuju prodajne vrednosti naknada i materijala.
- Objedinjavanje stvarne prodaje i stvarnih troškova dešava se pogrešno sa različitim deviznim kursevima.
- Opis u delu **Podrazumevani predložak radnog sata** je obmanjujući.
- Uvlačenjem zadatka se ne uklanja stavka **Kategorija** u korisničkom interfejsu dok se ne osveži.
- Nije dozvoljeno nepostojanje validacije kako bi se osiguralo premeštanje projekta posle datuma završetka.

**Sales**

Popravljeni su sledeći problemi:

- Izuzetak nulte reference se generiše u stavci ponude za projekat jer je opcija **Uvoz iz procene projekta** vidljiva kada projekat nije izabran.
- Sledeća greška se javlja prilikom zatvaranja ponude kao **Dobijeno**: „Referenca objekta nije podešena na instancu objekta“.
- Status prilagođavanja nije podešen tokom stvarnog storniranja dok se raskida veza projekta od predmeta ugovora.
- Kada su instalirani Dynamics 365 Field Service i Project Service Automation, opcije **Zaključaj cene** i **Koristi trenutne cene** se ne prikazuju istovremeno na stranici **Faktura**.
- Za japanski jezik postoji nedosledan prevod sa drugim stranicama zasnovanim na kalendaru.
- Opcije **Aktiviraj** i **Deaktiviraj** su uklonjene iz entiteta **Veza cenovnika** u usluzi Project Service Automation.


[!INCLUDE[footer-include](../includes/footer-banner.md)]