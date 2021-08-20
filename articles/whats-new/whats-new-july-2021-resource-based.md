---
title: Šta je novo u julu 2021. – Project Operations za scenarije zasnovane na resursima / bez zaliha
description: Ova tema pruža informacije o ispravkama kvaliteta dostupnim u izdanju za jul 2021. usluge Project Operations za scenarije zasnovane na resursima / bez zaliha.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 69507427521466335df9cbbaba79db1cfc7be91386b8b2ded5b1c384555946ee
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008063"
---
# <a name="whats-new-july-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Šta je novo u julu 2021. – Project Operations za scenarije zasnovane na resursima / bez zaliha

*Odnosi se na: Project Operations za scenarije zasnovane na resursima / bez zaliha*

Ova tema se odnosi na sledeće komponente i verzije usluge Dynamics 365 Project Operations:

   - Project Operations u Microsoft Dataverse okruženju verzije 4.12.0.148 ili 4.12.0.152.
   - Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzije 10.0.20.

## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

Sledeće funkcije su uključene u ovom izdanju:

- Mogućnost administratora da pregledaju PSS evidencije i evidencije podešavanja operacija iz menija za podešavanje. Evidencije se čuvaju 90 dana.

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja mapa dvostrukog upisivanja za Project Operations

U ovom izdanju nema ispravki za Project Operations mape dvostrukog upisivanja.

Za trenutnu listu i verzije Project Operations mapa dvostrukog upisivanja, pogledajte [Verzije Project Operations mapa dvostrukog upisivanja](../environment/resource-dual-write-maps.md).

Uvek pokrenite najnoviju verziju mape u svom okruženju i omogućite sve povezane mape tabela dok ažurirate svoje Project Operations Dataverse rešenje i verzija rešenja usluge Finance. Određene funkcije i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija mape. Aktivnu verziju mape možete videti na stranici **Dvostruko upisivanje** u koloni **Verzija**. Aktivirajte novu verziju mape izborom **Verzije mape tabela**, odabirom najnovije verzije, a zatim čuvanjem izabrane verzije. Ako ste prilagodili mapu tabele koja je gotova, ponovo primenite. Za još informacija pogledajte [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem pri pokretanju mape, sledite uputstva u odeljku [Problem nedostajućih kolona tabele na mapama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) u Vodiču za rešavanje problema sa dvostrukim upisivanjem.

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-on-dataverse"></a>Project Operations u usluzi Dataverse

| **Oblast funkcija**              | **Referentni broj** | **Ispravka kvaliteta**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Naplata i određivanje cena           | 2224046              | Polje **Klasa transakcije** se može uređivati na kartici **Detalji stavke ponude**, ali je zaključano ako radite sa stranice **Detalji stavke ponude**.                                                                     |
| Naplata i određivanje cena           | 2224400              | Radnja **Zatvori ponudu kao ostvarenu** ne uspeva kada ponuda nema kontrolne tačke datuma.                                                                                                                                    |
| Naplata i određivanje cena           | 2234089              | Kada ručno unesete opis proizvoda, on se briše nakon što unesete količinu za procenu materijala.                                                                                                                         |
| Naplata i određivanje cena           | 2234100              | Mreža **Podešavanje naplate za zadatak** ne uključuje kolonu **Materijal** i to je vrednost na kartici **Naplata za zadatak** projekta.                                                                                                       |
| Naplata i određivanje cena           | 2277409              | ID proizvoda nije dostupan u detaljima predmeta ugovora za stavku tipa materijala.                                                                                                                                        |
| Naplata i određivanje cena           | 2281728              | Kreiranje predmeta ugovora nepotrebno preispituje stvarne vrednosti uzrokujući značajno povećanje obima podataka, što utiče na performanse.                                                                                |
| Naplata i određivanje cena           | 2298668              | Stavke u glavnoj knjizi povezane sa opozvanim i izbrisanim troškovima se ne uklanjaju.                                                                                                                                     |
| Naplata i određivanje cena           | 2300192              | Kada više korisnika uređuje fakturu, moguće je kreirati novi detalj linije fakture na potvrđenoj fakturi.                                                                                   |
| Naplata i određivanje cena           | 2301569              | Nije moguće ispravljati fakture ako je primenjena akontacija u iznosu od 0 \$.                                                                                                                                        |
| Naplata i određivanje cena           | 2307965              | Dolazi do greške ako se cena kategorije kreira sa vrednostima koje nedostaju.                                                                                                                           |
| Naplata i određivanje cena           | 2326870              | Dolazi do greške u **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete** ako je **producttypecode** bez vrednosti.                                                                            |
| Naplata i određivanje cena           | 2332732              | Dolazi do greške ako se kreira kontrolna tačka predmeta ugovora bez stavke porudžbine.                                                                                                                |
| Planiranje i praćenje projekta | 2181094              | API za planiranje projekata sada podržava PSS evidencije i evidencije podešavanja operacija koje se čuvaju 90 dana.                                                                                                                  |
| Planiranje i praćenje projekta | 2254201              | Oznaka **Režim rasporeda** se ažurira detaljima koji opisuju podrazumevanu logiku.                                                                                                                                      |
| Planiranje i praćenje projekta | 2300252              | Keš odgovora **openProject** se ažurira i uključuje vlasnika tokena u ključu keša, **osnovnu URL adresu** i **URL adresu segmenta** tako da **URL adresa zahteva** uvek može ponovo da se kreira ako se promeni **osnovna URL adresa**. |
| Planiranje i praćenje projekta | 2301312              | **msdyn_membershipstatus** je uklonjen iz prikaza **Član projektnog tima**.                                                                                                                                        |
| Planiranje i praćenje projekta | 2302759              | Proizvodi se nepotrebno preuzimaju na karticama **Dodeljivanje resursa**, **Procene** i **Procene troškova**.                                                                                                        |
| Planiranje i praćenje projekta | 2308050              | **CopyProject** ne uspeva sa greškom „Nije uspelo preuzimanje tokena za razgovor sa udaljenom službom“.                                                                                                                           |
| Planiranje i praćenje projekta | 2322650              | Prikaz **Lista projektnih zadataka** je ažurirana tako da podrazumevano prikazuje datum zadatka.                                                                                                            |
| Planiranje i praćenje projekta | 2327266              | **CopyProject** generiše grešku „Ključ nije pronađen u rečniku“ prilikom kopiranja procena.                                                                                                      |
| Planiranje i praćenje projekta | 2328123              | **CopyProject** generiše grešku „Nije uspelo preuzimanje tokena za razgovor sa udaljenom službom“.                                                                                                                          |
| Planiranje i praćenje projekta | 2336258              | **CopyProject** pogrešno kopira nazive pozicija resursa.                                                                                                                                                 |
| Naplata i određivanje cena           | 2224476              | Polje **Resurs koji može da se rezerviše** nema podrazumevanu vrednost prijavljenog korisnika na stranici **Upotreba materijala**.                                                                                                            |
| Upravljanje resursima           | 2277249              | Dolazi do greške kada se ažurira zahtev za resursom koji nije zasnovan na projektu.                                                                                                            |
| Upravljanje resursima           | 2323869              | Ukupna iskorišćenost resursa ne prepoznaje pravilno filtrirane resurse.                                                                                                                                             |
| Vreme i trošak              | 2176538              | Netačni operatori filtera primenjuju se na kontroli **Stavka vremena**.                                                                                                                                                   |
| Vreme i trošak              | 2177462              | Brisanje stavke vremena u mreži ne ažurira statuse dugmadi **Pošalji**, **Opozovi**, **Izbriši** i **Izmeni stavku** na očekivan način.                                                                                        |
| Vreme i trošak              | 2299985              | **TimeEntriesImportFromResourceAssignment** ne održava vreme početka/završetka iz kontura zadatka.                                                                                                  |
| Vreme i trošak              | 2318426              | Nakon prosleđivanja stavke vremena, zaključana polja i dalje mogu da se uređuju.                                                                                                                                   |
| Vreme i trošak              | 2323749              | Dolazi do greške kada se trošak kreira na kartici **Povezano** resursa koji može da se rezerviše.                                                                                                      |
| Vreme i trošak              | 2327678              | Kada kreirate stavku vremena sa kartice **Povezano** resursa koji može da se rezerviše, nadređeni resurs se ne prosleđuje kontroli stavke vremena.                                                                            |
| Opšte                       | 2296857              | Praćenje napredovanja za dugotrajne poslove.                                                                                                                                                                        |
| Opšte                       | 2253682              | Project Operations rešenje sa dvostrukim upisivanjem ne bi trebalo instalirati kada je jezgro dvostrukog upisivanja instalirano u okruženju bez rešenja orkestracije dvostrukog upisivanja.                                                |
| Opšte                       | 2316420              | Obezbeđenje Project Service jezgra ne uspeva ako se promeni poslovna jedinica korisnika aplikacije.                                                                                                                     |
| Opšte                       | 2376405              | Rešen je problem sa ažuriranjem koje pokreće proizvođač (ažuriranje kvaliteta je dostupno u verziji 4.12.0.152)                                                                                                                     |
### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Upravljanje projektima i računovodstvo u usluzi Dynamics 365 Finance

| Oblast funkcija                      | Referentni broj | Ispravka kvaliteta                                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Upravljanje projektima i računovodstvo | 4620267          | Nije moguće personalizovati obrasce za dodavanje polja **Svrha** na stranice **Transakcija objavljena u projektu**, **Kreiranje predloga fakture** i **Predlog fakture**.                                                                                                                                                                                         |
| Upravljanje projektima i računovodstvo | 4613449          | Kada izaberete ID ugovora za projekat u usluzi Finance, Project Operations integrisano okruženje otvara stranicu da kreira novi zapis umesto stranice za već kreirane projektne ugovore.                                                                                                                                           |
| Upravljanje projektima i računovodstvo | 4614445          | U primeni Project Operations integrisanog scenarija ne možete uređivati polje **Grupa poreza na promet stavke** na predlogu fakture koji se uvozi iz pripreme. Grupu poreza na promet stavki treba uređivati za otvorene predloge faktura svih vrsta transakcija, uključujući nalog, radno vreme, troškove, naknade i stavke. |
| Upravljanje projektima i računovodstvo |                  | Nije moguće objaviti predlog fakture koji je rezultat negativne korekcije transakcije vremena.                                                                                                                                                                                                                                              |
| Upravljanje projektima i računovodstvo |                  | Stavke predloga fakture se dupliraju zbog više periodičnih procesa **Uvoz iz pripreme** koji se pokreću istovremeno.                                                                                                                                                                                                                |

