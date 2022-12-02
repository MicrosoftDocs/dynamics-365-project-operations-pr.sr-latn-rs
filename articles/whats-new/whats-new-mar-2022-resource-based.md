---
title: Šta je novo u martu 2022. – Project Operations za scenarije zasnovane na resursima/bez zaliha
description: Ovaj članak pruža informacije o ispravkama kvaliteta koje su dostupne u izdanju usluge Project Operations za mart 2022. za scenarije zasnovane na resursima/bez zaliha.
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

Ovaj članak se odnosi na sledeće komponente i verzije usluge Microsoft Dynamics 365 Project Operations:

- Project Operations u Dataverse okruženju verzije 4.30.0.99
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzije 10.0.25

## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

Dnevnice su sada podržane u novom i redizajniranom modernom radnom prostoru za troškove. Kompanije koje koriste dnevnice mogu da omoguće ovoj funkciji da korisnicima pruži jednostavan način za slanje i nadoknadu troškova dnevnice. Za više informacija pogledajte [Troškovi za dnevnice](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja mapa dvostrukog upisivanja za Project Operations

Sledeća lista prikazuje mape dvostrukog pisanja koje su izmenjene ili dodate u izdanju Project Operations od marta 2022. godine.

| **Mapa entiteta** | **Ažurirana verzija** | **komentara** |
| --- | --- | --- |
| Project Operations entitet izvoza reda fakture dobavljača entity msdyn\_projectvendorinvoicelines | 1.0.0.3 | Mapiranja su ažurirana tako da budu usklađena sa entitetom reda na fakturi dobavljača u programu Dataverse. <br>Ne aktivirajte verziju mapiranja 1.0.0.4. Biće spremno za upotrebu u kombinaciji sa okruženjem za finansije u verziji 10.0.26 u sledećem mesečnom ažuriranju. |

Uvek pokrenite najnoviju verziju mape u svom okruženju i omogućite sve povezane mape tabela dok ažurirate svoje Project Operations Dataverse rešenje i verzija rešenja usluge Finance. Neke funkcije i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija mape. Aktivnu verziju mape možete videti u koloni **Verzija** na stranici **Dvostruko upisivanje**. Da biste aktivirali novu verziju mape, izaberite **Verzije tabele mape**, izaberite najnoviju verziju, a zatim sačuvajte izabranu verziju. Ako ste prilagodili mapu tabele koja je gotova, ponovo primenite. Za još informacija pogledajte [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem kada pokrenete mapu, sledite uputstva u odeljku [Nedostaje izdanje kolona tabele na mapama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rešavanje problema sa dvostrukim upisivanjem.

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-on-dataverse"></a>Project Operations u usluzi Dataverse

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Vreme i trošak | 2388011 | Prikažite komentare odbijanja osobama koje prosleđuju stavke vremena tokom masovnog odobravanja. |
| Planiranje i praćenje projekta | 2495294 | Detalji projekta ne smeju da se uređuju na stranici **Detalji zadatka**. |
| Naplata i određivanje cena | 2499605 | Kontrolne tačke ugovora koje su keširane na osnovu kontrolnih tačaka ponude netačno su označene samo za čitanje. |
| Planiranje i praćenje projekta | 2506050 | Skup operacija ostaje na čekanju jedan sat ako nema promene za čuvanje. Skup se zatim lažno označava kao **Neuspešno**, dok bi trebalo odmah da bude dovršen. |
| Naplata i određivanje cena | 2507401 | Podrazumevane jedinice ugovora se nepravilno unose u projekte zbog pogrešnog keširanja. |
| Naplata i određivanje cena | 2541660 | **Provera valjanosti kreiranja ulaznih porudžbina** u dvostrukom upisivanju treba da bude samo za porudžbine zasnovane na projektu. |
| Naplata i određivanje cena | 2552745 | Porez se ne deli između klijenata koji su podesili pravila za podelu obračuna. |
| Naplata i određivanje cena | 2558859 | Poboljšane poruke o greškama prilikom podešavanja dimenzija za određivanje cena. |
| Naplata i određivanje cena | 2558933 | **Uvoz iz procena za projekat** ne uspeva kada se **msdyn\_project** doda kao dimenzija za određivanje cena. |
| Naplata i određivanje cena | 2559101 | Brisanje parametara projekta nije blokirano i dovodi do problema. |
| Upravljanje mogućnostima za poslovanje | 2570390 | Dodatna komponenta za dvostruko upisivanje primorava da tip naloga na ponudama, porudžbinama i mogućnostima za poslovanje bude **Klijent**, čak i kada taj tip naloga nije ispravan. |
| Naplata i određivanje cena | 2586097 | Stvarne vrednosti podeljenih naplaćenih troškova se ne storniraju kada se projekat ukloni iz predmeta ugovora za projekat. |
| Naplata i određivanje cena | 2589619 | Porez na ručno uneti materijal se propagira na stvarne vrednosti nenaplaćene prodaje i fakturu. |
| Upravljanje mogućnostima za poslovanje | 2594015 | Nije moguće zatvoriti ponudu kao osvojenu za klijente koji imaju **Net60** uslove plaćanja. |
| Planiranje i praćenje projekta | 2595841 | U rešenju Project for the Web, korisnici dobijaju poruku o grešci da nedostaje **msdyn\_actualstart** kada kreiraju novi zahtev za resursom. |
| Vreme i trošak | 2602511 | Polje **Odbio** za stavke vremena prikazuje **Sistem** umesto imenovanog korisnika kao osobe koja je odbila. |
| Vreme i trošak | 2602528 | Osoba koja vrši odobravanje projekta može da odobri vreme na projektima u kojima nije navedena kao osoba koja vrši odobravanje. |
| Naplata i određivanje cena | 2608550 | Korektivna faktura se može potvrditi čak i ako nema promena u originalnoj. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Upravljanje projektima i računovodstvo u rešenju Dynamics 365 Finance

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Upravljanje projektima i računovodstvo | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Postoji nepodudaranje između usluga Finance i Project Operations u dozvoljenoj dužini polja **ID kategorije**. |
| Upravljanje projektima i računovodstvo | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Projekti sa fiksnom cenom se ne mogu ukloniti kada je polje **O fakturisanju poslovnog kontakta** podešeno na **Dobit i gubitak**, a koristi se princip **Dovršenog procenta**. |
| Upravljanje projektima i računovodstvo | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Neispravna podrazumevana grupa poreza na promet se unosi iz podešavanja projekta u redove troškova u dnevniku integracije za Project Operations. |
| Upravljanje projektima i računovodstvo | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Dimenzije zaglavlja predloga fakture za projekat ne možete da uređujete u integrisanoj primeni sa uslugom Project Operations. |
| Upravljanje projektima i računovodstvo | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Fakture dobavljača između preduzeća ne smeju biti integrisane sa uslugom Dataverse. |
| Upravljanje projektima i računovodstvo | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Došlo je do nepodudaranja valute salda klijenta i valute za izveštavanje. |
| Upravljanje projektima i računovodstvo | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Projektnu fakturu možete proknjižiti čak i ako je klijent na čekanju za sve fakture. |
| Upravljanje projektima i računovodstvo | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Dugme **Izbriši sve redove** nedostaje u predlozima faktura za projekat koji imaju prikaze **Zaglavlje** i **Redovi**. |
| Upravljanje projektima i računovodstvo | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Kada knjižite fakturu dobavljača, dolazi do sledeće greške: „Računovodstveni datum fakture mora biti u istoj računovodstvenoj godini kao povezana izlazna porudžbina. Pokrenite proces za porudžbenicu na kraju godine ili promenite datum u tekuću računovodstvenu godinu.“ |
| Putovanje i trošak | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Preduzeti troškovi za projekat se ne oslobađaju nakon otpuštanja dodeljenog troška zahteva za putovanje. |
| Putovanje i trošak | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Do sledeće greške dolazi kada prosledite izveštaj o troškovima: „Praćenje steka: Kompanija ne postoji.“ |
| Putovanje i trošak | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | Podrazumevani **ID projekta** se ne unosi u izveštaje o troškovima kada je u projektu izabran parametar **Zahtevaj aktivnost za dnevnik**. |
| Putovanje i trošak | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | Dugme **Proknjiži troškove** ne funkcioniše ispravno u rešenju Project Operations za scenarije resursa/bez zaliha. |
| Putovanje i trošak | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Postoji problem sa **Stopom po kilometru** za izveštaj o troškovima kilometraže koji uključuje putnike. |
| Putovanje i trošak | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Stope za troškove kilometraže za zaposlene se ne sabiraju pravilno kada se koriste dve različite vrste vozila u kategoriji troškova **Slojevi stope za kilometražu**. |
| Putovanje i trošak | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Pronalaženje polja **Projekat** u redu trebovanja za putovanje ne vraća ispravnu listu projekata. |
| Putovanje i trošak | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Kilometraža je u pregledu** pokazuje upozorenje na izveštajima o troškovima. |
| Putovanje i trošak | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Usluga optičkog prepoznavanja znakova (OCR) na priznanicama ne funkcioniše zbog problema sa URL adresom usluge OCR za troškove. |
| Putovanje i trošak | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Kada je omogućena funkcija **Mogućnost brze podele periodičnih troškova**, iznosi u redovima sa podelom u izveštajima o troškovima menjaju iznose svaki put kada se otvori stranica **Podeli**. |
| Putovanje i trošak | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Izveštaj o troškovima ne možete da izbrišete kada prelazna lista ima više osoba koje vrše odobravanje. |

## <a name="removed-and-deprecated-features"></a>Uklonjene i zastarele funkcije

Članak [Uklonjene ili zastarele funkcije u rešenju Project Operations](removed-depreciated-features-project.md) opisuje funkcije koje su uklonjene ili zastarele za rešenje Dynamics 365 Project Operations.

- Uklonjena funkcija više nije dostupna u proizvodu.
- Zastarela funkcija nije u aktivnom razvoju i možda će biti uklonjena u budućoj ispravci.

Najava zastarevanja će se pojaviti u članku [Uklonjene ili zastarele funkcije u rešenju Project Operations](removed-depreciated-features-project.md) 12 meseci pre nego što bilo koja funkcija bude uklonjena iz proizvoda.

Za presudne promena koje utiču samo na vreme kompilacije, ali su binarno kompatibilne sa Sandbox i proizvodnim okruženjima, vreme zastarevanja će biti manje od 12 meseci. Ove promene obično su funkcionalne ispravke koje se moraju izvršiti na kompajleru.
