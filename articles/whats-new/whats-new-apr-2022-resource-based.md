---
title: Šta je novo u aprilu 2022. – Project Operations za scenarije zasnovane na resursima / bez zaliha
description: Ovaj članak pruža informacije o ispravkama kvaliteta koje su dostupne u izdanju usluge Microsoft Dynamics 365 Project Operations za april 2022. za scenarije zasnovane na resursima/bez zaliha.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 999006b2c2fe2b31d6e47910a3f1a55cab415f0e
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110901"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Šta je novo u aprilu 2022. – Project Operations za scenarije zasnovane na resursima / bez zaliha

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ovaj članak se odnosi na sledeće komponente i verzije usluge Microsoft Dynamics 365 Project Operations:

- Project Operations u Dataverse okruženju verzije 4.41.0.45
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzije 10.0.26

## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

Kategorije nabavke se mogu koristiti u porudžbenicama projekta i fakturama dobavljača na čekanju. Za više informacija, pogledajte članak [Korišćenje kategorija nabavke sa porudžbenicama projekta i fakturama dobavljača na čekanju](../procurement/configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja mapa dvostrukog upisivanja za Project Operations

Sledeća tabela prikazuje mape dvostrukog pisanja koje su izmenjene ili dodate u izdanju Project Operations od marta 2022. godine.

| Mapa entiteta | Ažurirana verzija | komentara |
| -------------- | ------------------- | ------------|
| Project Operations entitet izvoza reda fakture dobavljača entity msdyn\_projectvendorinvoicelines | 1.0.0.4 | Ova mapa podržava korišćenja kategorija nabavke sa porudžbenicama i fakturama dobavljača na čekanju. |

Uvek pokrenite najnoviju verziju mape u svom okruženju i omogućite sve povezane mape tabela dok ažurirate svoje Project Operations Dataverse rešenje i verzija rešenja usluge Finance. Neke funkcije i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija mape. Aktivnu verziju mape možete videti u koloni **Verzija** na stranici **Dvostruko upisivanje**. Da biste aktivirali novu verziju mape, izaberite **Verzije tabele mape**, izaberite najnoviju verziju, a zatim sačuvajte izabranu verziju. Ako ste prilagodili mapu tabele koja je gotova, ponovo primenite. Za još informacija pogledajte [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem kada pokrenete mapu, sledite uputstva u odeljku [Nedostaje izdanje kolona tabele na mapama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rešavanje problema sa dvostrukim upisivanjem.

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-on-dataverse"></a>Project Operations u usluzi Dataverse

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| ------------ | ---------------- | -------------- |
| Vreme i trošak | 2573900 | Funkcija **Moderno odobravanje** podrazumevano mora biti omogućena. |
| Naplata i određivanje cena | 2603313 | Otklonjena je greška u dupliranju zapisa koja je sprečavala da se dodaju redovi ponude i predmeti ugovora koji imaju proizvod. |
| Primena i konfiguracija | 2611368 | Klijenti moraju biti u mogućnosti da dodaju do pet prilagođenih entiteta rešenju pomoću modernog dizajnera aplikacija. |
| Vreme i trošak | 2628285 | Otklonjen je problem koji je uticao na mogućnost postavljanja ispravne kategorije resursa tokom uvoza stavke vremena. |
| Upravljanje mogućnostima za poslovanje| 2628815 | Ažurirajte ograničenje broja znakova opisa detalja reda ponude tako da se podudara sa ograničenjem znakova teme zadatka, tako da uvoz uspe za zadatke u kojima je tema duža od 100 znakova. |
| Vreme i trošak| 2629547 | Polje **Prosledio** odobrenja projekta mora da ukazuje na korisnika koji je prosledio zapis. |
| Vreme i trošak| 2629865 | Polje **Kopiraj kategoriju** na zadacima prilikom kopiranja projekata. |
| Vreme i trošak| 2636463 | Popravljeni su filteri na odobrenjima u modernim obrascima za odobrenje. |
| Planiranje i praćenje projekta | 2648300 | Otklonjen je problem koji sprečava promenu vlasnika projekta. |
| Naplata i određivanje cena | 2563000 | Stavke u glavnoj knjizi za nenaplaćenu prodaju u kojima se valuta razlikuje od valute ugovora ne smeju biti dozvoljene. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Upravljanje projektima i računovodstvo u rešenju Dynamics 365 Finance

Za informacije o ispravkama grešaka koje su uključene u ovu ispravku, prijavite se na Microsoft Dynamics Lifecycle Services (LCS) i pogledajte [članak u bazi znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
