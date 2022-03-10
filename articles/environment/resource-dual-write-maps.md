---
title: Verzije mape dvostrukog upisivanja za Project Operations
description: Ova tema pruža spisak mapa dvostrukog upisivanja potrebnih za Dynamics 365 Project Operations.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 452f9f16bfbae2d547afb9fcf4fc51595ea49890
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547126"
---
# <a name="project-operations-dual-write-map-versions"></a>Verzije mape dvostrukog upisivanja za Project Operations

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Upotreba Dynamics 365 Project Operations za scenarije sa resursima/materijalima koji nisu na zalihama zahteva skup mapa sa dvostrukim upisivanjem koji će se izvoditi u okruženju. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Mape preduslova: Rešenje orkestracije dvostrukog upisivanja

Sledeće mape su neophodni preduslovi za Project Operations rešenje. Obavezno pokrenite mape navedene u sledećoj tabeli i sve povezane mape tabela u vašem okruženju.

| Mapa tabela | Početna sinhronizacija |
| --- | --- |
| Knjiga (msdyn_ledgers) | Zahteva početnu sinhronizaciju za mapu tabele i sve preduslove. Master za početnu sinhronizaciju su Finance and Operations aplikacije. |
| Pravna lica (cdm_companies) | Nije obavezno. Sistem automatski popunjava ovaj entitet kada su okruženja povezana pomoću dvostrukog upisivanja. |
| Klijenti V3 (poslovni kontakti) | Nije potrebno za rezervisanje. |
| Prodavci V2 (msdyn_vendors) | Nije potrebno za rezervisanje. |

1. Na listi mapa odaberite mapu Glavna knjiga **(msdyn\__ledgers)** sa svim preduslovima i označite polje za potvrdu **Početna sinhronizacija**. U polju **Master za početnu sinhronizaciju**, izaberite **Finance and Operations aplikacije** i za mapu glavne knjige i za sve preduslovne karte. Izaberite **Pokreni**.

![Sinhronizacija mape glavne knjige.](media/DW6.png)

2. Sledite iste korake za sve preostale mape tabela navedene u gornjoj tabeli. Ne birajte polje **Početna sinhronizacija** za pokretanje tih mapa.

## <a name="project-operations-dual-write-maps"></a>Mape dvostrukog upisivanja za Project Operations

Sledeće mape su neophodne za Project Operations rešenje. Navedene su verzije mapa sa dvostrukim upisivanjem, počev od ispravke usluge Project Operations za maj 2021, verzije 4.10.0.186.

| **Mapa entiteta** | **Najnovija verzija** | **Početna sinhronizacija** |
| --- | --- | --- |
| Entitet integracije za odnose transakcija projekta (msdyn\_transactionconnections) | 1.0.0.0 | Nije potrebno za rezervisanje. |
| Zaglavlja projektnih ugovora (nalozi za prodaju) | 1.0.0.1 | Nije potrebno za rezervisanje. |
| Predmeti ugovora projekta (salesorderdetails) | 1.0.0.0 | Nije potrebno za rezervisanje. |
| Izvor finansiranja projekata (msdyn_projectcontractsplitbillingrules) | 1.0.0.2 | Nije potrebno za rezervisanje. |
| Project Operations tabela integracije za procene materijala (msdyn\__estimatelines) | 1.0.0.0 | Nije potrebno za rezervisanje. |
| Predlozi faktura projekta V2 (fakture) | 1.0.0.3 | Nije potrebno za rezervisanje. |
| Project Operations stvarne vrednosti integracije (msdyn_actuals) | 1.0.0.14 | Nije potrebno za rezervisanje. |
| Kontrolne tačke predmeta ugovora za integraciju sa uslugom Project Operations (msdyn_contractlinescheduleofvalues) | 1.0.0.4 | Nije potrebno za rezervisanje. |
| Entitet za integraciju sa uslugom Project Operations za procenu troškova (msdyn_estimatelines) | 1.0.0.2 | Nije potrebno za rezervisanje. |
| Project Operations entitet integracije za procene sati (msdyn_resourceassignments) | 1.0.0.5 | Nije potrebno za rezervisanje. |
| Project Operations entitet izvoza kategorija troškova projekta (msdyn_expensecategories) | 1.0.0.1 | Nije potrebno za rezervisanje. |
| Project Operations entitet izvoza troškova integracije projekta (msdyn_expenses) | 1.0.0.2 | Nije potrebno za rezervisanje. |
| Project Operations entitet izvoza fakture prodavca (msdyn_projectvendorinvoices) | 1.0.0.0 | Nije potrebno za rezervisanje. |
| Project Operations entitet izvoza reda fakture prodavca (msdyn_projectvendorinvoicelines) | 1.0.0.1 | Nije potrebno za rezervisanje. |
| Uloge projektnih resursa za sva preduzeća (bookableresourcecategories) | 1.0.0.1 | Zahteva početnu sinhronizaciju za mapu tabele za sinhronizaciju uloga resursa Menadžera projekta i člana tima koji su popunjeni u Dynamics 365 Dataverse okruženju tokom rezervisanja. Dataverse je glavni izvor za početnu sinhronizaciju. |
| Projektni zadaci (msdyn_projecttasks) | 1.0.0.4 | Nije potrebno za rezervisanje. |
| Kategorije projektnih transakcija (msdyn_transactioncategories) | 1.0.0.0 | Nije potrebno za rezervisanje. |
| Projekti V2 (msdyn_projects) | 1.0.0.2 | Nije potrebno za rezervisanje. |

Dovršite sledeće korake za pokretanje navedenih mapa.

1. Omogućite uloge resursa projekta za **sve kompanije (bookableresourcecategories)** mapu tabele jer ova mapa zahteva početnu sinhronizaciju. U **Master za početnu sinhronizaciju**, izaberite **Common Data Service**. 

 ![Sinhronizacija mape tabele uloga resursa.](media/6ResourceInitialSync.jpg)

 Sačekajte dok status mape ne postane **Aktivno** pre nego što pređete na sledeći korak.

2. Izaberite sve preostale potrebne mape. Možete ih filtrirati na listi mapa sa dvostrukim pisanjem pomoću ključne reči **Projekat** u pretrazi u gornjem desnom uglu. Možete višestruko odabrati sve mape, a zatim pokrenuti. Za više informacija pogledajte [Upravljanje sa više mapa tabela](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps). Obavezno omogućite i pokrenite povezane mape entiteta.

### <a name="project-operations-dual-write-map-versions"></a>Verzije mape dvostrukog upisivanja za Project Operations

Uvek pokrenite najnoviju verziju mape u svom okruženju. Određene funkcije i mogućnosti možda neće raditi ispravno ako postoji bilo koji od sledećih uslova:

- Mapa nije aktivirana.
- Najnovija verzija mape nije aktivirana. 
- Povezane mape tabela nisu aktivirane.

Aktivnu verziju mape možete videti u koloni **Verzija** na stranici **Dvostruko upisivanje**. Možete aktivirati novu verziju mape ako izaberete **Verzije tabele mape**, izaberete najnoviju verziju, a zatim sačuvajte izabranu verziju. Ako ste prilagodili mapu tabele koja je gotova, moraćete ponovo da primenite promene. Za još informacija pogledajte [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).
