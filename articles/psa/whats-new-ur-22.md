---
title: Šta je novo ili promenjeno u izdanju 22 ispravke za Project Service Automation u verziji 3
description: U ovoj temi date su funkcije i ispravke koje su dostupne u izdanju 22 ispravke za Project Service Automation u verziji 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 5694aa27afe7618cfca6b27444393634a9686600
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006573"
---
# <a name="project-service-automation-update-release-22-v3"></a>Project Service Automation izdanje ispravke 22, u verziji 3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x. Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).

U ovoj temi date su funkcije koje su nove ili su promenjene u izdanju 22 ispravke za Project Service Automation u verziji 3. Broj izrade ove verzije je V 3.10.33.48 i uglavnom je dostupna putem samostalnog ažuriranja u junu 2020. godine.

## <a name="update-release-22"></a>Izdanje ispravke 22

### <a name="bug-fixes"></a>Ispravke grešaka



**Vreme i trošak**

Popravljeni su sledeći problemi:

- **Stavke vremena** se ne dodaju automatski u raspored stavki vremena nakon uvoza.
- Alatka za biranje datuma na mreži u opciji **Stavke vremena** ne prepoznaje regionalna podešavanja korisnika.

**Upravljanje resursima**

Popravljeni su sledeći problemi:

- U ručnom režimu, promene u skicama **Dodela resursa** se ne prepoznaju pri generisanju stavke **Zahtevi za resursom**.
- **Zahtevi za resursom** ne podržavaju statuse prilagođenih zahteva.

**Upravljanje projektima**

Popravljeni su sledeći problemi:

- Dvostrukim klikom na EstimateGridControl neće se pravilno raščlaniti brojevi u holandskom formatu.
- Dodeljeni sati se ne ažuriraju ispravno kada se dodele menjaju pomoću programskog dodatka za Microsoft Project desktop klijent.
- Mreže za praćenje i procene projekata prikazuju pogrešnu šifru valute prodaje kada je valuta ugovora drugačija od valute klijenta i ako je organizacija konfigurisana za prikazivanje šifara valuta umesto simbola valute.
- Datum završetka člana tima dodaće jedan dan ako je raspored radnog vremena 24 sata dnevno.
- U Rasporedu projekata, dodavanje Kategorije transakcije zadatku ne pokreće automatsko čuvanje.
- Sledeća greška se prikazuje prilikom dodavanja člana tima u predložak projekta: „Zahtevi za resursima ne mogu biti povezani sa predlošcima projekta“. 
- Skripta pravila trake „msdyn.Approval.CanApproveOrReject“ prikazuje grešku vremenskog ograničenja.

**Sales**

Popravljeni su sledeći problemi:

- Poruka o grešci prilikom provere nije prikazana kada je u pretraživanju cenovnika na obrascu/entitetu „Novi cenovnik ponude za projekat“ izabran Cenovnik troškova.
- Zatvaranje dobijene ponude ne prelazi na kreirani ugovor ako je BPF u prilogu ponude u završnoj fazi.
- Storniranje stavke **Nenaplaćena prodaja** je povezano sa prvobitnim troškom kada se opozove unos vremena.
- Nakon odabira dugmeta **Potvrdi**, status fakture se ne menja u **Potvrđeno**, osim ako se faktura osveži.


[!INCLUDE[footer-include](../includes/footer-banner.md)]