---
title: Nadogradnja matične stranice
description: Ova tema pokazuje gde možete pronaći važne informacije o novim i izmenjenim funkcijama u aplikaciji Dynamics 365 Project Service Automation i postupak nadogradnje na najnoviju verziju.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: fa25d069de8098c0e8788c9ebb8aa3426eec5db9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121775"
---
# <a name="upgrade-home-page"></a>Nadogradnja matične stranice

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>Nadogradnja sa aplikacije PSA verzije 2.x ili 1.x na verziju 3.x

### <a name="new-instances"></a>Nove instance

Od 17. maja 2019. godine, kada se izabere Project Service Automation tokom obezbeđivanja nove instance, podrazumevano se instalira verzija 3.x.

### <a name="existing-instances"></a>Postojeće instance

Predhodno su klijenti koji imaju instancu aplikacije PSA verzije 2.x, a morali su da je nadograde na verziju 3.x, koja predstavlja PSA verziju zasnovanu na objedinjenom interfejsu klijenta, morali da se obrate Microsoft podršci i dostave detalje o instanci kako bi podrška mogla da omogući instancu za nadogradnju na verziju 3.x. Od 1. marta 2020. će kupci koji imaju instancu PSA verzije 2.x, a moraju da je nadograde na verziju 3.x, moći da nadograde svoje instance direktno sa portala za administraciju, a da ne moraju da se obrate Microsoft podršci.  

> [!NOTE]
> PSA verzije 3.x uključuje značajne promene. Razvijen je u okviru objedinjenog interfejsa kako bi pružio poboljšano korisničko iskustvo. Redizajnirana aplikacija omogućava dosledan i jedinstven korisnički interfejs i sledi principe prilagodljivog dizajna za optimalni pregled na bilo kojoj veličini ekrana ili uređaju. Došlo je i do drugih promena u celoj aplikaciji. Neke od oblasti koje su izmenjene uključuju određivanje cena, rezervisanje i dodeljivanje resursa, vremena i troškova, kao i odobrenja.

Pre nego što započnete postupak nadogradnje, preporučujemo vam da obavite sledeće zadatke:

- Proverite da li su Dynamics 365 Field Service i Project Service Automation instalirani na identifikovanoj instanci. Ako su oba rešenja instalirana, trebalo bi da planirate nadogradnju oba pre nego što nastavite sa redovnom upotrebom instance.
- Pažljivo pregledajte sledeće teme. Ako ste svesni promena između verzija i razumete ih, to će vam pomoći u procesu nadogradnje. Ove teme pružaju informacije o glavnim promenama u aplikaciji PSA, uz razmatranje nadogradnje i preporuke za planiranje nadogradnje na verziju 3.x.

    - [Šta je novo ili promenjeno u aplikaciji Project Service Automation verzije 3](whats-new-changed-v3.md)
    - [Činjenice koje treba uzeti u obzir prilikom nadogradnje - Project Service Automation verzije 2.x ili 1.x na verziju 3.x](upgrade-v3.md)

- Nadogradite instancu sandbox okruženja da biste procenili promene u implementaciji pre nadogradnje proizvodne instance.

Nakon što pregledate prethodno spomenute teme i spremni ste za nadogradnju na PSA verzije 3.x ili verziju zasnovanu na objedinjenom interfejsu klijenta, prosledite zahtev Microsoft podršci kako bi nadogradnja postala dostupna u centru administracije. U zahtevu navedite detalje instance.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>Starije verzije aplikacije PSA (PSA verzije 2.x) u novoj instanci

Od 17. maja 2019. godine, sve nove instance će kao podrazumevanog klijenta imati objedinjeni interfejs klijenta. Kako bismo obezbedili usklađenost sa ovom promenom, podrazumevano ćemo obezbediti PSA verzije 3.x i Field Service verzije 8.x jer su ove verzije dizajnirane da funkcionišu sa klijentom UCI (objedinjeni interfejs klijenta).

Od 1. marta 2020. klijenti sistema Dynamics PSA više neće moći da stvaraju nova okruženja sa starijim PSA verzijama, na primer PSA verzije 2.x ili starije. Svako novo okruženje će biti PSA verzije 3.x.

> [!NOTE]
> Da biste dobili najbolje iskustvo prilikom korišćena starije verzije Field Service i PSA aplikacija, idite na stranicu **Podešavanja sistema** i za polje **Korišćenje samo novog objedinjenog interfejsa (preporučeno)** izaberite **Ne** jer ove verzije nisu dizajnirane da budu ispravno učitane u objedinjeni interfejs klijenta. Nakon što isključite objedinjeni interfejs klijenta, ove verzije usluga Field Service i PSA možete otvoriti i pokrenuti pomoću starog veb-klijenta. 