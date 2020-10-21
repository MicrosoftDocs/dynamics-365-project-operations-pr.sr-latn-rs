---
title: Članovi projektnog tima
description: Ova tema pruža informacije o načinu rada sa informacijama, atributima i rasporedom članova projektnog tima.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f4941803c657fab55ee2702d9f58d6e333592889
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908537"
---
# <a name="project-team-members"></a>Članovi projektnog tima

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Članovi projektnog tima su učesnici projekta koji završavaju rad na projektu. Cilj mreže članova tima je da pruži spisak imenovanih resursa koji su posvećeni angažovanju i generičkih članova tima koji su čuvari mesta resursa i koji će kasnije biti popunjeni.

Iz mreže članova tima, menadžer projekta i ostali učesnici projekta mogu da vide ko je dodeljen projektu. Takođe mogu pogledati sažetak svojih rezervacija, planiranog angažovanja i pojedinačnih zadataka resursa. Mreža članova tima omogućava menadžerima projekata da definišu zahteve za resursima za generičke članove tima i upravljaju rezervacijama postojećih članova tima.

Sledeća tabela navodi ključne atribute člana projektnog tima.

| Ime polja          | Opis                                                                                                                                                                  |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Način dodele        | Metoda dodele koja se koristi za rezervisanje resursa na projektu.                                                                         |
| Tip naplate             | Izaberite da li je član tima klasifikovan kao naplativ.                                                                                                                                       |
| Resurs koji može da se rezerviše        | Resurs koji je moguće rezervisati izabran da zameni generički resurs.                                                                                                                   |
| Status brisanja            | Status brisanja člana tima za praćenje da li se PSS-u šalje zahtev za brisanje i da li PSS vraća odgovor uspešno i u očekivanom vremenskom roku. |
| Ukupno angažovanje (časovi)     | Zbir angažovanja članova tima na njihovim zadacima.                                                                                                                         |
| Angažovanje na završetku (časovi) | Praćenje angažovanja koje je član tima dovršio za svoje dodele.                                                                                           |
| Preostalo angažovanje (časovi) | Praćenje angažovanja koje član tima još uvek nije završio za svoje dodele.                                                                                    |
| Završetak                   | Datum završetka članstva resursa u timu.                                                                                                                                            |
| Čvrsto rezervisani časovi        | Fiksno rezervisani sati člana tima.                                                                                                                                                                |
| Ime položaja            | Ime koje se koristi za identifikaciju generičkog resursa.                                                                                                                                   |
| Jedinica za određivanje resursa          | Organizaciona jedinica resursa koji obavlja posao.                                                                                                                      |
| Davalac odobrenja za projekat         | Izaberite da li član tima može da odobrava vreme i troškove.                                                                                                                     |
| Zahtevani časovi           | Potrebno radno vreme člana tima prema zahtevu za člana tima.                                                                                                                       |
| Uloga                     | Uloga koju član tima ispunjava u ovom timu.                                                                                                                                |
| Opis položaja     | Unesite opis uloge za ovog člana tima.                                                                                                                             |
| Meko rezervisani časovi        | Uslovno rezervisani sati člana tima.                                                                                                                                                                 |
| Pokreni                    | Datum početka članstva resursa u timu.                                                                                                                                          |

Iz mreže članova tima mogu se preduzeti sledeće radnje:

- **Rezervacija**: Za organizacije koje izvršavaju korišćenje metodologije hibridnih rezervacija, radnja rezervacije će omogućiti korisnicima da rezervišu imenovani resurs na osnovu zahteva koji se generišu od generičkog člana tima
- **Generisanje zahteva**: Ova radnja generiše zahtev.
- **Navođenje obrasca**: Omogućava menadžerima projekata da prilagode konture zahtevanih resursa na detaljnom nivou. Menadžeri projekata mogu se prilagoditi specifičnim potrebama projekta u slučajevima kada podrazumevana distribucija ne odgovara.
- **Prosleđivanje zahteva**: Za organizacije koje koriste centralnu metodologiju rezervacije.
- **Uređivanje**: Atributi člana tima mogu se uređivati, uključujući organizacionu jedinicu, ulogu i naziv položaja.
- **Održavanje rezervacija**: Kada je potrebno ažuriranje rezervacija resursa, održavanje rezervacija omogućava menadžeru projekta da prilagodi:

    - Pokreni
    - Završetak
    - Ukupna dodela angažovanja

- **Novo**: Pored dodavanja resursa direktno iz rasporeda, menadžeri projekta mogu da dodaju nove imenovane ili generičke članove tima iz mreže članova tima.
- **Brisanje**: Odabirom jednog ili više članova tima, menadžer projekta može izbrisati resurse koji više neće učestvovati u projektu. Brisanjem člana tima izbrisaće se i svi pridruženi zadaci resursa i otkazati sve postojeće rezervacije.
