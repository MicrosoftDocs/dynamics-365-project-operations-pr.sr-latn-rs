---
title: Šta je novo u februaru 2022. – Project Operations za scenarije zasnovane na resursima/bez zaliha
description: Ovaj članak pruža informacije o ispravkama kvaliteta koje su dostupne u izdanju usluge Project Operations za februar 2022. za scenarije zasnovane na resursima/bez zaliha.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b036c0a3c39c52cb15277293679ef88906cae2c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933003"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Šta je novo u februaru 2022. – Project Operations za scenarije zasnovane na resursima/bez zaliha

*Odnosi se na: Project Operations za scenarije zasnovane na resursima / bez zaliha*

Ovaj članak se odnosi na sledeće komponente i verzije usluge Microsoft Dynamics 365 Project Operations:

- Project Operations u Dataverse okruženju verzije 4.28.0.120
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzije 10.0.24

## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

- Od ovog izdanja, možete da dodate do 300 članova tima u jedan projekat. Prethodno je ograničenje broja članova tima bilo 150. Za više informacija, pogledajte članak [Ograničenja projekta](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Ažuriranja mape dvostrukog upisivanja za Project Operations

Sledeća lista prikazuje mape dvostrukog pisanja koje su izmenjene ili dodate u izdanju Project Operations od februara 2022. godine.

| Mapa entiteta | Ažurirana verzija | komentara |
| --- | --- | --- |
| Project Operations entitet izvoza troškova integracije projekta (msdyn\_expenses) | 1.0.0.3 | Prošireno za sinhronizaciju projektne aktivnosti sa uslugom Dataverse. |

Za trenutnu listu i verzije Project Operations mapa dvostrukog upisivanja, pogledajte [Verzije Project Operations mapa dvostrukog upisivanja](../environment/resource-dual-write-maps.md).

Uvek pokrenite najnoviju verziju mape u svom okruženju i omogućite sve povezane mape tabela dok ažurirate svoje Project Operations Dataverse rešenje i verzija rešenja usluge Finance. Neke funkcije i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija mape. Aktivnu verziju mape možete videti u koloni **Verzija** na stranici **Dvostruko upisivanje**. Da biste aktivirali novu verziju mape, izaberite **Verzije tabele mape**, izaberite najnoviju verziju, a zatim sačuvajte izabranu verziju. Ako ste prilagodili mapu tabele koja je gotova, ponovo primenite. Za još informacija pogledajte [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem kada pokrenete mapu, sledite uputstva u odeljku [Nedostaje izdanje kolona tabele na mapama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rešavanje problema sa dvostrukim upisivanjem.

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-on-dataverse"></a>Project Operations u usluzi Dataverse

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Naplata i određivanje cena | 2415109 | Podrazumevana vrednost u polju **Uslovi plaćanja za operacije** mora biti zapis klijenta ugovora o projektu i zapis profakture. |
| Naplata i određivanje cena | 2497369 | Korekcija materijala mora pratiti vrednost datuma u parametrima **Korekcija**. |
| Naplata i određivanje cena | 2498697 | Poboljšana je bezbednosna konfiguracija za **Opoziv stavke vremena**. |
| Naplata i određivanje cena | 2513824 | Za scenarije zasnovane na resursima, ID kategorije transakcije ne sme da premaši 28 znakova u rešenju Project Operations. |
| Naplata i određivanje cena | 2517455 | Radnja **Osvežavanje transakcija stavki na fakturi** ne sme biti dozvoljena da bude aktivirana više puta istovremeno za istu fakturu. |
| Naplata i određivanje cena | 2517465 | Radnja **Deaktiviranje detalja o redu na fakturi** je blokirana jer nije podržana. |
| Naplata i određivanje cena | 2556660 | Popravljena je provera stupanja na snagu datuma koja se vrši na cenovniku koji je priložen zapisu parametara projekta. |
| Upravljanje mogućnostima za poslovanje | 2369202 | Ispravljena je poslovna logika koja potvrđuje da cenovnici koji imaju preklapajuće datume stupanja na snagu mogu biti priloženi istom projektnom ugovoru. |
| Upravljanje mogućnostima za poslovanje | 2385965 | Ispravili ste ponašanje na kartici **Klijenti** na stranici **Projektni ugovor** kada izaberete **Sačuvaj i zatvori**. |
| Vreme i trošak | 2538503 | Projektni zadatak mora biti dostupan u entitetu **Stvarne vrednosti projekta** nakon što se proknjiži izveštaj o troškovima. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Upravljanje projektima i računovodstvo u rešenju Dynamics 365 Finance

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Upravljanje projektima i računovodstvo | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Tokom uvoza kreditnih odobrenja dobavljača dolazi do greške. U poruci o grešci piše: „Iznos zadržavanja ne može biti veći od preostalog neto iznosa“. |
| Upravljanje projektima i računovodstvo | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Ako predlog fakture uključuje transakcije naknade sa nultim iznosom koje su stvarne vrednosti nenaplaćene prodaje, do fakturisanja ne može doći. |
| Upravljanje projektima i računovodstvo | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Proknjižena cena nije tačna nakon što se ažurira nabavna cena i kada je omogućeno **Aktiviranje upravljanja promenom**.|
| Upravljanje projektima i računovodstvo | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Procena knjiženja za projekat sa fiksnom cenom koristi netačnu valutu i iznos u vaučeru procene, čak i kada je omogućena funkcija **Omogući valutu ugovora za izračunavanje procene**. |
| Upravljanje projektima i računovodstvo | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_Extension** ne bi trebalo da vrši poziv za omogućavanje praćenja promena bez evidentiranja izuzetaka za entitete koji imaju ključeve konfiguracije koji nisu omogućeni |
| Upravljanje projektima i računovodstvo | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Grupni posao se popravlja kada se proknjiži više naprednih dnevnika i dođe do greške. |
| Putovanje i trošak | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Zbog problema sa poravnanjem koji se odnosi na gotovinske avanse na izveštajima o troškovima, iznos poreza nije pokriven kao deo gotovinskog avansa. |
| Putovanje i trošak | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Informacije o porezu na promet nisu uključene u izveštaj **Troškovi – proknjižene transakcije**. |
| Putovanje i trošak | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | Kršenje smernica za troškove **Potrebne priznanice** netačno prikazuje upozorenje u izveštajima o troškovima. |
| Putovanje i trošak | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Transakcija projekta ne uključuje porez na promet koji se ne može refundirati u ukupnom iznosu prodaje kada je transakcija rezultat troškova kilometraže. |
| Putovanje i trošak | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Kada raščlanjeni red ima porez, ne možete da promenite datum rašlanjenog reda i dolazi do greške u statusu izvornog dokumenta. |

## <a name="removed-and-deprecated-features"></a>Uklonjene i zastarele funkcije

Članak [Uklonjene ili zastarele funkcije u rešenju Project Operations](removed-depreciated-features-project.md) opisuje funkcije koje su uklonjene ili zastarele za rešenje Dynamics 365 Project Operations.

- Uklonjena funkcija više nije dostupna u proizvodu.
- Zastarela funkcija nije u aktivnom razvoju i možda će biti uklonjena u budućoj ispravci.

Najava zastarevanja će se pojaviti u članku [Uklonjene ili zastarele funkcije u rešenju Project Operations](removed-depreciated-features-project.md) 12 meseci pre nego što bilo koja funkcija bude uklonjena iz proizvoda.

Za presudne promena koje utiču samo na vreme kompilacije, ali su binarno kompatibilne sa Sandbox i proizvodnim okruženjima, vreme zastarevanja će biti manje od 12 meseci. Ove promene obično su funkcionalne ispravke koje se moraju izvršiti na kompajleru.
