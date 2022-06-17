---
title: Šta je novo u martu 2022. – Project Operations za scenarije zasnovane na resursima/bez zaliha
description: Ovaj članak pruža informacije o kvalitetnim ispravkama koje su dostupne u izdanju projektnih operacija u martu 2022.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910923"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Šta je novo u martu 2022. – Project Operations za scenarije zasnovane na resursima/bez zaliha

*Odnosi se na: Project Operations za scenarije zasnovane na resursima / bez zaliha*

Ovaj članak se odnosi na sledeće komponente i verzije korporacije Microsoft Dynamics 365 Project Operations:

- Operacije projekta u verziji Dataverse okruženja 4.30.0.99
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzija 10.0.25

## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

Dnevnice su sada podržane u novom i redizajniranom modernom radnom prostoru troškova. Kompanije koje koriste dnevnice mogu da omoguće ovoj funkciji da korisnicima pruži jednostavan način za prosleđivanje i nadoknadu troškova dnevnice. Više informacija potražite u članku [Troškovi za dnevnice](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja mapa dvostrukog upisivanja za Project Operations

Sledeća lista prikazuje mape sa dvostrukim pisanjem koje su izmenjene ili dodate u izdanje "Operacije projekta" iz marta 2022.

| **Mapa entiteta** | **Ažurirana verzija** | **komentara** |
| --- | --- | --- |
| Project Operations integration project vendor invoice line export entity msdyn\_ projectvendorinvoicelines | 1.0.0.3 | Mapiranja ažurirana tako da se poravnaju sa entitetom reda fakture dobavljača u programu Dataverse. <br>Ne aktivirajte verziju mapiranja 1.0.0.4. Biće spreman za upotrebu u kombinaciji sa Finance okruženjem verzije 10.0.26 u sledećem mesečnom ažuriranju. |

Uvek pokrenite najnoviju verziju mape u okruženju i omogućite sve povezane mape tabela dok ažurirate rešenje za projektne operacije Dataverse i verziju finansijskog rešenja. Neke funkcije i mogućnosti možda neće ispravno funkcionisati ako najnovija verzija mape nije aktivirana. Aktivnu verziju mape možete videti u koloni **Verzija** na stranici **Dvostruko upisivanje**. Da biste aktivirali novu verziju mape, izaberite **Verzije tabele mape**, izaberite najnoviju verziju, a zatim sačuvajte izabranu verziju. Ako ste prilagodili mapu tabele bez okvira, ponovo primenite promene. Za još informacija pogledajte [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem prilikom početka mape, sledite uputstva [u problemu sa kolonama tabele koje nedostaju u odeljku mape](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rešavanje problema sa dvostrukim upisivanja.

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-on-dataverse"></a>Project Operations u usluzi Dataverse

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Vreme i trošak | 2388011 | Prikažite komentare odbijanja prosleđenim stavkama vremena tokom masovnog odobravanja. |
| Planiranje i praćenje projekta | 2495294 | Detalji projekta ne smeju da se uređuju na stranici **sa detaljima zadatka**. |
| Naplata i određivanje cena | 2499605 | Prekretnice ugovora koje su nastale od prekretnica navoda netačno su označene samo za čitanje. |
| Planiranje i praćenje projekta | 2506050 | Skup operacija ostaje na čekanju jedan sat ako nema promene za čuvanje. Skup je zatim lažno označen kao "Neuspešno **·**", dok bi trebalo odmah da bude dovršen. |
| Naplata i određivanje cena | 2507401 | Podrazumevane jedinice ugovora se nepravilno unose u projekte zbog neispravnog keširanja. |
| Naplata i određivanje cena | 2541660 | **Provera valjanosti kreiranja ulaznih porudžbina** u dvostrukom upisivanju treba da bude samo za porudžbine zasnovane na projektu. |
| Naplata i određivanje cena | 2552745 | Porez se ne deli između kupaca koji su podesili pravila podele naplate. |
| Naplata i određivanje cena | 2558859 | Poboljšane poruke o greškama prilikom podešavanje dimenzija cena. |
| Naplata i određivanje cena | 2558933 | **Uvoz iz procene projekta** ne uspe **kada se msdyn\_** projekat doda kao dimenzija cena. |
| Naplata i određivanje cena | 2559101 | Brisanje parametara projekta nije blokirano i dovodi do problema. |
| Upravljanje mogućnostima za poslovanje | 2570390 | Dodatna komponenta za dvostruko pisanje primorava tip naloga na navodnicima, porudžbinama i prilikama da bude "Kupac **·**", čak i kada taj tip naloga nije ispravan. |
| Naplata i određivanje cena | 2586097 | Razdeljeni troškovi fakturisanih se ne obrću kada se projekat ukloni iz reda ugovora o projektu. |
| Naplata i određivanje cena | 2589619 | Porez na materijal za upis se širi na neželjene aktuele prodaje i fakturu. |
| Upravljanje mogućnostima za poslovanje | 2594015 | Nije moguće zatvoriti citat kao što je osvojeno za kupce koji imaju Net60 **uslove** plaćanja. |
| Planiranje i praćenje projekta | 2595841 | U projektu za Web korisnici dobijaju poruku o grešci o msdyn **actualstart-u \_ koji nedostaje** kada kreiraju novi zahtev za resurs. |
| Vreme i trošak | 2602511 | Polje **"Odbijeno** " za stavke vremena prikazuje **sistem** umesto imenovanog korisnika kao odbijača. |
| Vreme i trošak | 2602528 | Osoba koja vrši odobravanje projekta može da odobri vreme na projektima u kojima nisu navedeni kao osoba koja vrši odobravanje. |
| Naplata i određivanje cena | 2608550 | Korektivna faktura se može potvrditi čak i ako nema promena u originalu. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Upravljanje projektima i računovodstvo na Dynamics 365 Finance

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Upravljanje projektima i računovodstvo | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Postoji nepodudaranje između finansijskih i projektnih operacija u dozvoljenoj dužini polja **ID kategorije**. |
| Upravljanje projektima i računovodstvo | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Projekti fiksne cene se ne mogu eliminisati kada je polje **Fakturisanje konta podešeno** **na "Dobit i** gubitak", a koristi **se princip dovršenog** procenta. |
| Upravljanje projektima i računovodstvo | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Neispravna podrazumevana grupa poreza na promet se unosi iz podešavanja projekta u redove troškova u nalogu integracije operacija projekta. |
| Upravljanje projektima i računovodstvo | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Dimenzije zaglavlja predloga fakture projekta ne možete da uređujete u integrisanom raspoređivanju sa operacijama projekta. |
| Upravljanje projektima i računovodstvo | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Fakture međukompanijskih dobavljača ne smeju biti integrisane sa Dataverse. |
| Upravljanje projektima i računovodstvo | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Došlo je do nepodudaranja valute salda kupca i valute za izveštavanje. |
| Upravljanje projektima i računovodstvo | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Projektnu fakturu možete proknjižiti čak i ako je kupac na čekanju za sve fakture. |
| Upravljanje projektima i računovodstvo | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Dugme **"Izbriši** sve redove" nedostaje u predlozima faktura projekta koji imaju prikaze **"Zaglavlje** " **i "Redovi** ". |
| Upravljanje projektima i računovodstvo | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Kada knjižite fakturu dobavljača, dolazi do sledeće greške: "Računovodstveni datum fakture mora biti u istoj računovodstvenoj godini kao povezana izlazna porudžbina. Pokrenite proces na kraju godine izlazne porudžbine ili promenite datum u tekuću računovodstvenu godinu." |
| Putovanje i trošak | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Posvećeni troškovi za projekat nisu objavljeni nakon što se oslobodi trošak koji je počinio putni put. |
| Putovanje i trošak | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Do sledeće greške dolazi kada prosledite izveštaj o troškovima: "Praćenje steka: Preduzeće ne postoji." |
| Putovanje i trošak | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | Podrazumevani **ID projekta se** ne unosi u izveštaje o troškovima kada je u **projektu izabrana aktivnost "** Zahtevaj aktivnost za parametar naloga". |
| Putovanje i trošak | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | Dugme **"Proknjiži troškove** " ne funkcioniše ispravno u operacijama projekta za scenarije resursa/nedovršavanje. |
| Putovanje i trošak | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Postoji problem sa stopom po **kilometru za izveštaj** o troškovima kilometraže koji uključuje putnike. |
| Putovanje i trošak | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Stope kilometraže troškova za zaposlene nisu pravilno sabirane kada se koriste dve različite vrste vozila u **kategoriji troškova tiraža stope** kilometraže. |
| Putovanje i trošak | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Pronalaženje polja "Projekat **"** u redu trebovanja putovanja ne vraća tačnu listu projekata. |
| Putovanje i trošak | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Kilometraža u pregledu** pokazuje upozorenje na izveštaje o troškovima. |
| Putovanje i trošak | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Usluga priznavanja optičkog prepoznavanja znakova (OCR) ne funkcioniše zbog problema sa URL adresom OCR usluge troškova. |
| Putovanje i trošak | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Kada je **funkcija "Mogućnost artikla periodičnih troškova"** omogućena, iznosi u redovima stavke u izveštajima o troškovima menjaju iznose svaki **put kada se otvori stranica "** Artikalište". |
| Putovanje i trošak | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Izveštaj o troškovima ne možete da izbrišete kada prelazna lista ima više osoba koje vrše odobravanje. |

## <a name="removed-and-deprecated-features"></a>Uklonjene i neodobrene funkcije

Uklonjene [ili zastarele funkcije u članku "Operacije](removed-depreciated-features-project.md) projekta" opisuju funkcije koje su uklonjene ili zastarele za Dynamics 365 Project Operations.

- Uklonjena funkcija više nije dostupna u proizvodu.
- Zastarela funkcija nije u aktivnom razvoju i može biti uklonjena u budućoj ispravci.

Najava amortizacije će se pojaviti u funkcijama " [Uklonjeno" ili "Zastarelo" u članku "Operacije](removed-depreciated-features-project.md) projekta" 12 meseci pre nego što bilo koja funkcija bude uklonjena iz proizvoda.

Za prekid promena koje utiču samo na vreme kompilacije, ali su binarno kompatibilne sa sandbox i proizvodnim okruženjem, vreme amortizacije će biti manje od 12 meseci. Ove promene obično su funkcionalne ispravke koje se moraju izvršiti na kompajleru.
