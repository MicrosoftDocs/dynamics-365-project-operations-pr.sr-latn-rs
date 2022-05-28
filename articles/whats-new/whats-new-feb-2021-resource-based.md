---
title: Šta je novo u februaru 2021. – Project Operations za scenarije zasnovane na resursima/bez zaliha
description: Ova tema pruža informacije o ispravkama kvaliteta dostupnim u izdanju usluge Project Operations za februar 2021. za scenarije zasnovane na resursima/bez zaliha.
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: cb6ab1337652d18a30fba56560ffe50f78dd4eb4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589029"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Šta je novo u februaru 2021. – Project Operations za scenarije zasnovane na resursima/bez zaliha

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ova tema se odnosi na sledeće komponente i verzije usluge Dynamics 365 Project Operations:

- Project Operations u Dataverse okruženju 4.7.0.95
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzija 10.0.16 

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-on-dataverse"></a>Project Operations u usluzi Dataverse

| **Oblast funkcija** | **Referentni broj** | **Ispravka kvaliteta** |
| --- | --- | --- |
| **Naplata i određivanje cena** | 2053736 | Detalji stavke fakture sada su dostupni ako odete na **Faktura** > **Srodne informacije**. |
| **Naplata i određivanje cena** | 2122613 | Radnje **Aktiviraj** i **Deaktiviraj** su uklonjene iz entiteta veze **cenovnika**. |
| **Naplata i određivanje cena** | 2128606 | Rešen je problem sa **ullReferenceException** u dodatnoj komponenti **GetEstimatesForProject**. |
| **Primena i konfiguracija** | 2139346 | Rešen je problem sa uvozom neupravljanog rešenja **Dynamics365ProjectOperationsDualWrite**. |
| **Primena i konfiguracija** | 2140569 | Projektno rešenje ne sme da se instalira u okruženje Dataverse Teams. |
| **Primena i konfiguracija** | 2086991 | Ograničeno prilagođavanje lokalizacije veb-resursa. |
| **Upravljanje mogućnostima za poslovanje** | 2136794 | Prikažite tačnu poruku o grešci kada procesi **Potvrdi fakturu** ili **Označi fakturu kao plaćenu** ne uspeju. |
| **Upravljanje mogućnostima za poslovanje** | 2139330 | Promena menadžera projekta za projekat ne sme da vrati preduzeće-vlasnika na podrazumevanu vrednost. |
| **Upravljanje mogućnostima za poslovanje** | 2146376 | Ispravljen iznos poreza u stvarnom nenaplativom iznosu se kreira na osnovu potvrde fakture. |
| **Planiranje i praćenje projekta** | 2099879 | Primena Dataverse okruženja mora da kreira podrazumevanu kategoriju transakcija sa statičkim ID-om, a ne da nasumično generiše jedan po okruženju. |
| **Planiranje i praćenje projekta** | 2128577 | Ispravljene su Project Service privilegije korisnika za ažuriranje kategorije transakcije u dodeli resursa. |
| **Planiranje i praćenje projekta** | 2164035 | Rešeni su problemi sa funkcijom **Kopiraj projekat**. |
| **Stavka vremena** | 2129161 | Primenjuju se stroža ograničenja kako bi se osiguralo da korisnici ne mogu promeniti i ažurirati unos vremena koji je poslat ili odobren. |
| **Stavka vremena** | 2103572 | Odobrenje vremena za unose vremena koji se ne odnose na projekat ne sme tražiti ulogu odobravaoca projekta. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Upravljanje projektima i računovodstvo u Dynamics 365 Finance 

Više informacija o upravljanju projektima i računovodstvu u Dynamics 365 Finance [. godini potražite u članku Šta je novi januar 2021](whats-new-jan-2021-resource-based.md).


## <a name="regulatory-updates"></a>Regulatorne ispravke

Više informacija o regulatornim ispravkama za aplikacije za finansije i operacije potražite u članku [Regulatorne ispravke](/dynamics365/finance/localizations/regulatory-updates). Drugi način da saznate više o regulatornim ispravkama je da se prijavite na Lifecycle Services (LCS) i pregledate planirane regulatorne ispravke pomoću alatke za pretragu problema. Pretraga problema vam omogućava pretragu po zemlji, tipu funkcije i izdanju.


[!INCLUDE[footer-include](../includes/footer-banner.md)]