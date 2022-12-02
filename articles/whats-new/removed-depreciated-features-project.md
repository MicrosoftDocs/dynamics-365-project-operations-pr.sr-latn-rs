---
title: Uklonjene ili zastarele funkcije u usluzi Dynamics 365 Project Operations
description: Ovaj članak opisuje funkcije koje su uklonjene ili su planirane za uklanjanje iz usluge Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f0fbaed028db11d8fb1551d304a40543faf35b0d
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028346"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Uklonjene ili zastarele funkcije u usluzi Dynamics 365 Project Operations

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture, kao i Project Operations za scenarije zasnovane na zalihama/proizvodnji_

Ovaj članak opisuje funkcije koje su uklonjene ili su planirane za uklanjanje iz usluge Dynamics 365 Project Operations.

- *Uklonjena* funkcija više nije dostupna u proizvodu.
- *Zastarela* funkcija nije u aktivnom razvoju i možda će biti uklonjena u budućoj ispravci.

Svrha ove liste je da vam pomogne da razmislite o ovim uklanjanjima i zastarevanjima za sopstveno planiranje.

> [!NOTE]
> Detaljne informacije o objektima u aplikacijama za finansije i operacije možete pronaći u [**Tehničkim referentnim izveštajima**](/dynamics/s-e/global/axtechrefrep_61). Možete da uporedite različite verzije ovih izveštaja da biste saznali više o objektima koji su promenjeni ili uklonjeni u svakoj verziji aplikacija za finansije i operacije.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Funkcije koje su uklonjene ili zastarele u izdanju za mart 2022. usluge Project Operations

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Parametar upravljanja projektima i računovodstva „Uvek kreiraj transakciju korekcije“

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za zastarevanje/uklanjanje** | Transakcije korekcije su potrebne u svrhe nadgledanja. Nakon zastarevanja, ovaj parametar će biti sakriven. Sistem će uvek kreirati transakcije korekcije, kao što trenutno čini kada je parametar podešen na **Da**. |
| **Zamenjeno drugom funkcijom?** | No |
| **Pogođena područja proizvoda** | ID aplikacije |
| **Opcija primene** | Project Operations za scenarije proizvodnje/na zalihama |
| **Status** | Zastarelo: Do 1. marta 2023. sakrićemo parametar i promeniti ponašanje sistema tako da se transakcije korekcije uvek kreiraju. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Parametar upravljanja projektima i računovodstva „Koristi datum korekcije kao novi datum projekta“

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za zastarevanje/uklanjanje** | Ovaj parametar je prvobitno korišćen da bi se dozvolile korekcije kada je fiskalni period zatvoren. Međutim, to više nije potrebno jer se računovodstveni datum transakcije može promeniti u prvi datum otvorenog perioda, ako je konfigurisan. Datum projekta ne sme biti promenjen jer predstavlja datum kada je došlo do transakcije. |
| **Zamenjeno drugom funkcijom?** | No |
| **Pogođena područja proizvoda** | ID aplikacije |
| **Opcija primene** | Project Operations za scenarije proizvodnje/na zalihama |
| **Status** | Zastarelo: Do 1. marta 2023. sakrićemo parametar i promeniti ponašanje sistema tako da se datum projekta nikad ne menja tokom korekcija. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Tok posla zahteva za resursom u usluzi Project Operations za scenarije zasnovane na zalihama/proizvodnji

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za zastarevanje/uklanjanje** | Zastarelo zbog slabog korišćenja i ograničenja obima transakcija. |
| **Zamenjeno drugom funkcijom?** | No |
| **Pogođena područja proizvoda** | ID aplikacije |
| **Opcija primene** | Project Operations za scenarije proizvodnje/na zalihama |
| **Status** | Zastarelo: Do 1. marta 2023. onemogućićemo opciju zahtevanja resursa za projekat koristeći tok posla. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Stranica predloga fakture projekta bez prikaza zaglavlja i redova

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za zastarevanje/uklanjanje** | Zastarelo zbog poboljšanja stranice koja su uvedena zajedno sa ključem funkcije **Koristi predlog fakture za projekat i obrasce dnevnika faktura sa prikazom zaglavlja i redova**. |
| **Zamenjeno drugom funkcijom?** | Da |
| **Pogođena područja proizvoda** | ID aplikacije |
| **Opcija primene** | Project Operations za scenarije proizvodnje/na zalihama; Project Operations za scenarije resursa/bez zaliha |
| **Status** | Zastarelo: Do 1. marta 2023. isključićemo prethodnu (zastarelu) stranicu i podrazumevano uključiti ključ funkcije **Koristi predlog fakture za projekat i obrasce dnevnika faktura sa prikazom zaglavlja i redova**. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Funkcije koje su uklonjene ili zastarele u izdanju za decembar 2021. usluge Project Operations

### <a name="collaboration-workspaces"></a>Radni prostori za saradnju

[Kreiranje ili povezivanje radnog prostora za saradnju (Projekat)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za zastarevanje/uklanjanje** | Zastarelo zbog slabe upotrebe. Klijenti koji koriste Project Operations za scenarije sa resursima/bez zaliha mogu da iskoriste [Saradnju sa Office grupama](../project-management/collaboration-groups.md). |
| **Zamenjeno drugom funkcijom?** | No |
| **Pogođena područja proizvoda** | ID aplikacije  |
| **Opcija primene** | Project Operations za scenarije proizvodnje/na zalihama |
| **Status** | Zastarelo: Do 1. decembra 2022. planiramo da više ne podržavamo radne prostore za saradnju. |
