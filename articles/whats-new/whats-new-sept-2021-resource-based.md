---
title: Šta je novo u septembru 2021. – Project Operations za resurs/scenarije koji nisu zasnovani na zalihama
description: Ova tema pruža informacije o ažuriranjima kvaliteta dostupnim u izdanju Project Operations za septembar 2021. godine za za scenarije zasnovane na resursima/materijalima koji nisu na zalihama.
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 842ea95892fa4f7a29a778cfd2c33a66e84f676c
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547171"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Šta je novo u septembru 2021. – Project Operations za resurs/scenarije koji nisu zasnovani na zalihama

*Odnosi se na: Project Operations za scenarije zasnovane na resursima / bez zaliha*

Ova tema se odnosi na sledeće komponente i verzije usluge Dynamics 365 Project Operations:

   - Project Operations u Microsoft Dataverse okruženju verzije 4.14.0.99.
   - Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzije 10.0.20.

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja mapa dvostrukog upisivanja za Project Operations

U ovom izdanju nema ispravki za Project Operations mape dvostrukog upisivanja. Za trenutnu listu i verzije Project Operations mapa dvostrukog upisivanja, pogledajte [Verzije Project Operations mapa dvostrukog upisivanja](../environment/resource-dual-write-maps.md).

Uvek pokrenite najnoviju verziju mape u svom okruženju i omogućite sve povezane mape tabela dok ažurirate svoje Project Operations Dataverse rešenje i verzija rešenja usluge Finance. Određene funkcije i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija mape. Aktivnu verziju mape možete videti na stranici **Dvostruko upisivanje** u koloni **Verzija**. Da biste aktivirali novu verziju mape, izaberite **Verzije tabele mape**, izaberite najnoviju verziju, a zatim sačuvajte izabranu verziju. Ako ste prilagodili mapu tabele koja je gotova, ponovo primenite. Za još informacija pogledajte [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem pri pokretanju mape, sledite uputstva u odeljku [Problem sa kolonama tabele na mapama koje nedostaju](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) u vodiču za rešavanje problema pri dvostrukom upisivanju.

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-on-dataverse"></a>Project Operations u usluzi Dataverse

| **Oblast funkcija** | **Referentni broj** | **Ispravka kvaliteta** |
| --- | --- | --- |
| Vreme i trošak | 1811407 | Prilagođena je bezbednosna uloga „Osoba koja odobrava projekat“ za odobrenja unosa troškova. |
| Vreme i trošak | 1811438 | Prilagođena je bezbednosna uloga „Osoba koja odobrava projekat“ za otkazivanje odobrenja stavki vremena. |
| Vreme i trošak | 2370126 | Ažurirane su ikone **Projektni zadatak** i **Uloga** u entitetu **Stavka vremena**. |
| Vreme i trošak | 2379879 | Ispravljena je funkcija **Kopiranje sedmice** u stavci vremena kada koristite Dynamics 365 za telefon. |
| Naplata i određivanje cena | 2371906 | Ukupan iznos predračuna ne sme se menjati u usluzi Project Operations a za primene zasnovane na resursima. |
| Naplata i određivanje cena | 2385802 | Otklonjena je greška koja se javlja sa negativnim stvarnim satima kada se ukupni iznosi projekta osveže. |
| Naplata i određivanje cena | 2389675 | Poboljšano ponašanje potvrde predračuna. Entitet sa dugotrajnim poslovima mora uzeti u obzir aktivnosti potrebne za upisivanje rezultata potvrde za računovodstvo. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Upravljanje projektima i računovodstva u usluzi Dynamics 365 Finance

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Putovanje i trošak | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Iznosi za transakcije dobavljača i poreza na promet koji su knjiženi iz troška koji je nastao transakcijom kreditnom karticom nisu tačni. |
| Putovanje i trošak | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Pogrešne stavke poravnanja se kreiraju kada se generiše dnevnik plaćanja. |
| Putovanje i trošak | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Iznosi za transakcije poreza na promet koji su knjiženi iz troška koji je nastao transakcijom kreditnom karticom nisu tačni. |
| Putovanje i trošak | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Brisanje linije troškova može potrajati. |
| Projektno računovodstvo | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Nakon primene članka baze znanja 4619395, promena redosleda brojeva u **Kontinuirano** nije podržana i kada objavite procenu, dolazi do sledeće greške: „Sistem ne podržava podešavanje „kontinuirano“ za niz brojeva Proj_X“. |
| Projektno računovodstvo | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Objavljivanje fakture dobavljača možda neće uspeti uz sledeću poruku o grešci: „Transakcije na vaučeru nisu u skladu sa bilansom na dan 17.5.2021. (računovodstvena valuta: 0,00 – valuta za izveštavanje: 0,01).“ |
