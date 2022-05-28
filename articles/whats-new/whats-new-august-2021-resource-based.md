---
title: Šta je novo u avgustu 2021. – Project Operations za scenarije zasnovane na resursima / bez zaliha
description: Ova tema pruža informacije o ispravkama kvaliteta dostupnim u izdanju za avgust 2021. usluge Project Operations za scenarije zasnovane na resursima / bez zaliha.
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 144a8c0d5ac47ad6fee54850c149a349f1698049
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594181"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Šta je novo u avgustu 2021. – Project Operations za scenarije zasnovane na resursima / bez zaliha

*Odnosi se na: Project Operations za scenarije zasnovane na resursima / bez zaliha*

Ova tema se odnosi na sledeće komponente i verzije usluge Dynamics 365 Project Operations:

   - Project Operations u Microsoft Dataverse okruženju verzije 4.13.0.152.
   - Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzija 10.0.20.

## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

Sledeće funkcije su uključene u ovom izdanju:

- **Skupovi odobrenja**: Skupovi odobrenja grupišu zahteve za odobrenje vremena, troškova ili korišćenje materijala u manje podskupove operacija. Ovo grupisanje omogućava da se odobrenja obrađuju prema određenom redosledu po projektu i omogućava ponovni pokušaj i sekvenciranje. Grupisanje zahteva poboljšava pouzdanost i mogućnost praćenja obrade odobrenja za velike brojeve odobrenja. Za više informacija, pogledajte [Skupovi odobrenja](../approvals/approval-sets.md).

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja mapa dvostrukog upisivanja za Project Operations

U ovom izdanju nema ispravki za Project Operations mape dvostrukog upisivanja.

Za trenutnu listu i verzije Project Operations mapa dvostrukog upisivanja, pogledajte [Verzije Project Operations mapa dvostrukog upisivanja](../environment/resource-dual-write-maps.md).

Uvek pokrenite najnoviju verziju mape u svom okruženju i omogućite sve povezane mape tabela dok ažurirate svoje Project Operations Dataverse rešenje i verzija rešenja usluge Finance. Određene funkcije i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija mape. Aktivnu verziju mape možete videti na stranici **Dvostruko upisivanje** u koloni **Verzija**. Aktivirajte novu verziju mape izborom **Verzije mape tabela**, odabirom najnovije verzije, a zatim čuvanjem izabrane verzije. Ako ste prilagodili mapu tabele koja je gotova, ponovo primenite. Za još informacija pogledajte [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem pri pokretanju mape, sledite uputstva u odeljku [Problem nedostajućih kolona tabele na mapama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) u Vodiču za rešavanje problema sa dvostrukim upisivanjem.

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-on-dataverse"></a>Project Operations u usluzi Dataverse

| **Oblast funkcija** | **Referentni broj** | **Ispravka kvaliteta** |
| --- | --- | --- |
| Naplata i određivanje cena | 2295625 | Naziv kontrolne tačke mora se kopirati iz rasporeda faktura u detalje stavke fakture. |
| Naplata i određivanje cena | 2316323 | Za popust ne treba da postoji mogućnosti uređivanja na predračunu u aplikaciji Project Operations za scenarije zasnovane na resursima. |
| Upravljanje mogućnostima za poslovanje | 2338619 | Poslovna pravila za stavke **Mogućnost za poslovanje** i **Ponuda** moraju se pozivati samo na stranicama. |
| Upravljanje resursima | 2316523 | Korišćenje stavke **Poslati zahtev** iz zahteva resursa koji ima priloženu ulogu ne bi trebalo da prikaže grešku. |
| Upravljanje resursima | 2326885 | Kreiranje zahteva za resursima kroz projekat ne bi trebalo da prikaže grešku. |
| Vreme i trošak | 2335584 | Zastareli tokovi zadataka u unosu vremena. |
| Vreme i trošak | 2336884 | Dugme za unos vremena **Kopiraj sedmicu** mora raditi ne samo za trenutnog korisnika. |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Upravljanje projektima i računovodstvo na Dynamics 365 Finance

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Putovanje i trošak | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Netačni iznosi transakcija prodavca i poreza na promet knjiže se kada se trošak napravi od transakcije kreditnom karticom. |
| Putovanje i trošak | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Pogrešno poravnanje su redovi nastali kada se generiše dnevnik plaćanja. |
| Putovanje i trošak | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Netačni iznosi transakcija poreza na promet knjiže se kada se trošak napravi od transakcije kreditnom karticom. |
| Putovanje i trošak | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Brisanje linije troškova može potrajati. |
| Projektno računovodstvo | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Sistem ne podržava postavljanje kontinuiranog redosleda brojeva kada objavite procenu nakon primene baze znanja 4619395. |
| Projektno računovodstvo | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Knjiženje faktura prodavca možda neće uspeti sa porukom o grešci „Transakcije na vaučeru nemaju bilans od 17.5.2021. (računovodstvena valuta: 0,00 – valuta za izveštavanje: 0,01)“ |
