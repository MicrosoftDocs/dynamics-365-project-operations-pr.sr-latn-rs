---
title: Uklonjene ili neodobrene funkcije u Dynamics 365 Project Operations
description: Ovaj tema opisuje funkcije koje su uklonjene ili koje su planirane za uklanjanje iz programa Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61bb84b94274762636eb8532f09634db1109e969
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601587"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Uklonjene ili neodobrene funkcije u Dynamics 365 Project Operations

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture, kao i Project Operations za scenarije zasnovane na zalihama/proizvodnji_

Ovaj tema opisuje funkcije koje su uklonjene ili koje su planirane za uklanjanje iz programa Dynamics 365 Project Operations.

- *Uklonjena* funkcija više nije dostupna u proizvodu.
- *Zastarela* funkcija nije u aktivnom razvoju i možda će biti uklonjena u budućoj ispravci.

Svrha ove liste je da vam pomogne da razmislite o ovim uklanjanjima i zastarevanjima za sopstveno planiranje.

> [!NOTE]
> Detaljne informacije o objektima u aplikacijama "Finansije i operacije" možete pronaći u tehničkim [**referentnim izveštajima**](/dynamics/s-e/global/axtechrefrep_61). Možete da uporedite različite verzije ovih izveštaja da biste saznali više o objektima koji su promenjeni ili uklonjeni u svakoj verziji aplikacija "Finansije i operacije".

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Funkcije uklonjene ili zastarele u izdanju Projektne operacije marta 2022.

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Parametar upravljanja projektima i računovodstva "Uvek kreiraj transakciju korekcije"

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za zastarevanje/uklanjanje** | Transakcije korekcije su potrebne u svrhe nadgledanja. Nakon amortizacije, ovaj parametar će biti sakriven. Sistem će uvek kreirati transakcije korekcije, kao što trenutno čini kada je parametar podešen na "Da **"**. |
| **Zamenjeno drugom funkcijom?** | No |
| **Pogođena područja proizvoda** | ID aplikacije |
| **Opcija primene** | Projektne operacije za proizvodne/snabdevene scenarije |
| **Status** | Deprecated: Do 1. marta 2023. sakrićemo parametar i promeniti ponašanje sistema tako da se uvek kreiraju transakcije prilagođavanja. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Upravljanje projektima i računovodstvo "Koristi datum korekcije kao novi datum projekta" parametar

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za zastarevanje/uklanjanje** | Ovaj parametar je prvobitno korišćen da bi se dozvolila podešavanja kada fiskalni period zatvorena. Međutim, to više nije potrebno jer se računovodstveni datum transakcije može promeniti u prvi datum otvorenog perioda, ako je konfigurisan. Datum projekta ne sme biti promenjen jer predstavlja datum kada je došlo do transakcije. |
| **Zamenjeno drugom funkcijom?** | No |
| **Pogođena područja proizvoda** | ID aplikacije |
| **Opcija primene** | Projektne operacije za proizvodne/snabdevene scenarije |
| **Status** | Deprecated: Do 1. marta 2023. sakrićemo parametar i promeniti ponašanje sistema tako da se datum projekta nikada ne menja na korekcijama. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Tok posla zahteva za resurse u operacijama projekta za snabdevene scenarije/scenarije zasnovane na proizvodnji

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za zastarevanje/uklanjanje** | Neodobreno zbog slabog korišćenja i ograničenja obima transakcija. |
| **Zamenjeno drugom funkcijom?** | No |
| **Pogođena područja proizvoda** | ID aplikacije |
| **Opcija primene** | Projektne operacije za proizvodne/snabdevene scenarije |
| **Status** | Neodobreno: Do 1. marta 2023. onemogućićemo opciju zahtevanja resursa za projekat pomoću toka posla. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Stranica predloga fakture projekta bez prikaza zaglavlja i redova

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za zastarevanje/uklanjanje** | Neodobreno zbog poboljšanja stranice koja je uvedena zajedno sa **predlogom fakture za projekat i obrascima naloga faktura sa ključem funkcije prikaza zaglavlja** i redova. |
| **Zamenjeno drugom funkcijom?** | Da |
| **Pogođena područja proizvoda** | ID aplikacije |
| **Opcija primene** | Projektne operacije za scenarije proizvodnje/zaliha; Projektne operacije za scenarije koji nisu snabdeveni |
| **Status** | Neodobreno: Do 1. marta 2023. isključićemo prethodnu (zastarelu) stranicu i podrazumevano uključiti **predlog fakture za korišćenje projekta i obrasce naloga** faktura sa ključem za prikaz zaglavlja i redova. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Funkcije uklonjene ili zastarele u izdanju Projektne operacije decembra 2021.

### <a name="collaboration-workspaces"></a>Radni prostori za saradnju

[Kreiranje radnog prostora za saradnju ili veza sa vezom (Projekat)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za zastarevanje/uklanjanje** | Neodobreno zbog slabe upotrebe. Klijenti koji koriste projektne operacije za scenarije koji nisu snabdeveni mogu da iskoriste [saradnju sa Office grupama](../project-management/collaboration-groups.md). |
| **Zamenjeno drugom funkcijom?** | No |
| **Pogođena područja proizvoda** | ID aplikacije  |
| **Opcija primene** | Projektne operacije za proizvodne/snabdevene scenarije |
| **Status** | Deprecated: Do 1. decembra 2022. planiramo da više ne podržavamo radni prostor saradnje. |
