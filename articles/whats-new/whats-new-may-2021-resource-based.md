---
title: Šta je novo u maju 2021. – Project Operations za scenarije zasnovane na resursima / bez zaliha
description: Ovaj članak pruža informacije o kvalitetnim ispravkama dostupnim u maju 2021.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 425b0eb78b5f03d4b0da9a792d6e33fc96adf060
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930427"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Šta je novo u maju 2021. – Project Operations za scenarije zasnovane na resursima / bez zaliha

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ovaj članak se odnosi na sledeće Dynamics 365 Project Operations komponente i verzije:

- Project Operations u Dynamics 365 Dataverse okruženju verzije 4.10.0.186
- Upravljanje projektima i računovodstvo u okruženjima aplikacija za finansije i operacije verzija 10.0.18

## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

Sledeće funkcije su uključene u ovom izdanju:

- [Režimi zakazivanja](../project-management/scheduling-modes.md): Menadžeri projekata mogu definisati da li projektom treba da se upravlja korišćenjem režima zakazivanja fiksnog trajanja, fiksnog rada ili fiksnih jedinica.
- [Podešavanje kilometraže pomoću nivoa kilometraže](../expense/set-up-mileage.md): Ažurirajte nivoe kilometraže za izveštaje o troškovima zaposlenih.

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja mapa dvostrukog upisivanja za Project Operations

Sledeća lista prikazuje mape dvostrukog upisivanja koje su izmenjene ili dodate u izdanju Project Operations od maja 2021. godine.

| Mapa entiteta | Ažurirana verzija | Komentari |
| --- | --- | --- |
| Izvor finansiranja projekata (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | Sinhronizacija uslova plaćanja za klijenta prema ugovoru o projektu. |
| Predlog fakture za projekat V2 (fakture) | 1.0.0.3 | Sinhronizacija uslova plaćanja prema predračunu. |
| Project Operations entitet izvoza reda fakture prodavca (msdyn\__projectvendorinvoicelines) | 1.0.0.1 | Ispravke kvaliteta |
| Projects V2 (msdyn\_projects) | 1.0.0.2 | Ispravke kvaliteta |

Uvek pokrenite najnoviju verziju mape u okruženju i omogućite sve povezane mape tabela dok ažurirate rešenje za projektne Dataverse operacije i verziju rešenja za finansije i operacije. Određene funkcije i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija mape. Aktivnu verziju mape možete videti u koloni **Verzija** na stranici **Dvostruko upisivanje**. Da biste aktivirali novu verziju mape, izaberite **Verzije tabele mape**, izaberite najnoviju verziju, a zatim sačuvajte izabranu verziju. Ako ste prilagodili mapu tabele koja je gotova, ponovo primenite. Za još informacija pogledajte [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem sa pokretanjem mape, sledite uputstva u odeljku [Nedostaje izdanje kolona tabele na mapama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rešavanje problema sa dvostrukim upisivanjem.

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-on-dataverse"></a>Project Operations u usluzi Dataverse

| **Oblast funkcija** | **Referentni broj** | **Ispravka kvaliteta** |
| --- | --- | --- |
| Naplata i određivanje cena | 2227635 | Podrazumevane vrednosti u poljima **Grupa jedinica** i **Jedinica** se preuzimaju iz proizvoda u mreži **Procene materijala**. |
| Naplata i određivanje cena | 2234127 | Polje **ID zadatka** se sada pravilno integriše u stvarne vrednosti Dataverse projekta kada se proknjiži faktura dobavljača. |
| Naplata i određivanje cena | 2235564 | Čuvanjem stavke u glavnoj knjizi obezbeđuje se da valuta prikazana u stavka knjiženja u glavnoj knjizi podudara sa podrazumevanom valutom stavke nakon čuvanja. |
| Naplata i određivanje cena | 2246671 | Ako se transakcija ne naplati tokom fakturisanja, poništava se originalni nefakturisani zapis prodaje i kreira se novi nefakturisani zapis prodaje kao nenaplativ. |
| Naplata i određivanje cena | 2264042 | Važeća korekcija fakture ne sme biti blokirana ako postoji detalj korekcije fakture koji nije važeći u okruženju. |
| Naplata i određivanje cena | 2146367 | Mapiranje dvostrukog upisivanja zaglavlja fakture za projekat prošireno je tako da uključuje uslove plaćanja. |
| Upravljanje mogućnostima za poslovanje | 2086888 | Nemojte dodavati uloge i kategorije koje su deaktivirane pre kopiranja ponude u uloge i kategorije novokopirane ponude koje se naplaćuju. |
| Upravljanje mogućnostima za poslovanje | 2234376 | Polja samo za čitanje su zatamnjena u mreži **Procene materijala**. |
| Upravljanje mogućnostima za poslovanje | 2238337 | Ponuda zasnovana na kontaktu može se sačuvati čak i ako nije povezana sa cenovnikom projekta. |
| Upravljanje mogućnostima za poslovanje | 2239810 | Zatvaranje ponude kao izgubljene takođe zatvara pridruženi projekat i otkazuje sve rezervacije. |
| Planiranje i praćenje projekta | 2099559 | Dodate su dodatne provere ispravnosti sistema pre nego što se otvori mreža **Projektni zadaci**. |
| Planiranje i praćenje projekta | 2178987 | Ispravljena je privremena greška koja se javlja prilikom izbora stavke **Sledeća faza** na stranici **Projekat**. |
| Upravljanje resursima | 2224817 | Funkcionalnost za proširenje vrednosti rezervacija uzima podrazumevane vrednosti iz tačnog statusa rezervacije. |
| Stavka vremena | 2202476 | Stranica **Stavka vremena** sada koristi kontrolu mreže reakcije i rešava probleme kao što je neusklađenost mreže. |
| Stavka vremena | 2223377 | Stavka vremena se skriva iz odeljka **Povezano** na stranici **Resurs koji može da se rezerviše** kako bi se izbegla zabuna sa upotrebljivošću. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Upravljanje projektima i računovodstvo u Dynamics 365 Finance

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Upravljanje projektima i računovodstvo | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Project Operations za scenarije zasnovane na resursima: Ne možete konvertovati ponudu kao ostvarenu zbog greške integracije. |
| Upravljanje projektima i računovodstvo | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations: Dolazi do greške kada pokušate da pridružite predmet ugovora ID-u projekta zbog provere da li se predmeti ugovora i tipovi transakcija preklapaju. |
| Upravljanje projektima i računovodstvo | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** podešava adresu fakture izvora finansiranja od drugog klijenta. |
| Putovanje i trošak | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | Može da dođe do greške u knjiženju u vezi sa podešavanjem kilometraže. |
| Putovanje i trošak | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | Funkcionalnost **Podeliti na lični** ne funkcioniše za transakcije troškova u stranoj valuti. |
| Putovanje i trošak | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | Vrednosti padajućeg menija kategorije troškova prikazuju pogrešne kategorije za delegate bez obzira na to da li su oni resurs. |
| Putovanje i trošak | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | Ne možete sačuvati izveštaj o troškovima kompanije zbog greške u **validaciji resursa/kategorije**. |
| Putovanje i trošak | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | Pogrešno izračunavanje kilometraže u knjiženju izveštaja o troškovima ima podeljene linije. |
| Putovanje i trošak | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | Ne možete da proknjižite izveštaj o troškovima unutar preduzeća ako je uračunat porez na promet i ako je vrsta računa prebačena na način plaćanja **Radnik**. |
| Putovanje i trošak | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Poništavanje entiteta podataka **TrvRequisitionLine** i jedinstveni indeks su povezani. |
| Putovanje i trošak | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Izveštaj o troškovima podržava kreiranje i ažuriranje stavki izvornog dokumenta. |
| Putovanje i trošak | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Prikazuje se pogrešan nalog za knjiženje u potknjizi u scenariju unutar preduzeća ako se porez na promet knjiži u pravnom licu na odredištu. |
| Putovanje i trošak | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations: Procena troškova se ne briše iz usluge Finance kada se briše iz platforme Dataverse. |
| Putovanje i trošak | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Kada je kategorija troškova kategorija koja nije projekat, finansijski aspekti izabrani na stranici **Troškovi** se ne kopiraju u izveštaj o troškovima. |
