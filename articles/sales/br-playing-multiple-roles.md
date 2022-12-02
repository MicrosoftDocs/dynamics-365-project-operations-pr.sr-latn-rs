---
title: Procena prodaje i troškove za projekat kada resurs koji možete sa rezervišete ispunjava više uloga u projektu
description: Ovaj članak objašnjava kako da koristite dimenzije određivanja cena za podršku procenama cena i troškova za resurs koji ispunjava više uloga u projektu.
author: rumant
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9bb59537aaa75d9003925bec37642a2fa7c9ca22
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923481"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a>Procena prodaje i troškove za projekat kada resurs koji možete sa rezervišete ispunjava više uloga u projektu 

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/nepostojanju zaliha, jednostavna primena – od pogodbe do profakture, Project Operations za scenarije zasnovane na zalihama/proizvodnji_ 

Kompanije zasnovane na projektima često imaju potrebu da jedan resurs ispunjava više uloga u projektu. Svaka uloga može imati drugu cenu i trošak. To znači da bi vreme trajanja istog resursa na projektu moglo da dobije različitu finansijsku procenu, u zavisnosti od naplate i stopa troškova za svaku ulogu. Možete konfigurisati vrednosti u zapisu člana tima za imenovani resurs sa različitim zamenama za svaki od zadataka kojima je dodeljen član tima.

Sledeći primer vas vodi kroz to kako jednostavna zamena vrednosti omogućava resursu da ima više uloga u projektu sa različitim troškovima i stopama naplate.

## <a name="create-tasks"></a>Kreiranje zadataka
Da biste kreirali zadatke, morate da dodate zadatke, kao i rezimirane zadatke, nakon kojih je potrebno dodeliti zadatak pre nego što dodate trajanje zadatka. 

### <a name="add-tasks-and-summary-tasks"></a>Dodavanje zadataka i rezimiranih zadataka
Da biste dodali zadatak, obavite sledeće korake.

1. Idite na **Projekti** i otvorite projekat kome želite da dodate zadatke.
2. Izaberite **Dodaj novi zadatak**. Imenujte zadatak, a zatim pritisnite **Enter**.
3. Unesite drugi naziv zadatka i pritisnite **Enter**. Ponavljajte ovo sve dok ne budete imali potpunu listu zadataka.
3. Za uvlačenje zadataka u okviru zadataka **Rezime**, izaberite tri vertikalne tačke po nazivu zadatka, a zatim izaberite **Napravite podzadatak**. 

  > [!TIP]
  > Da biste izabrali više zadataka, izaberite zadatak, pritisnite i držite taster **Ctrl**, a zatim izaberite drugi zadatak.
  >
  > Takođe možete odabrati **Promoviši podzadatak** za premeštanje zadataka ispod zadataka **Rezime**.

### <a name="assign-tasks"></a>Dodela zadataka

Dovršite sledeće korake da biste dodali zadatke.

1. U koloni **Dodeljeno osobi** za zadatak, izaberite ikonu osobe.
2. Odaberite člana tima sa liste ili unesite tekst da biste potražili ime.

### <a name="add-task-duration-and-columns"></a>Dodavanje trajanja zadatka i kolona

Često je najlakše započeti izgradnju vašeg projekta sa trajanjem. Dovršite sledeće korake da biste dodali trajanje zadatka.

1. U koloni **Trajanje** za zadatak, unesite broj dana za koji mislite da će biti potrebno za izvršenje zadatka. Ako želite da koristite drugu vremensku jedinicu, unesite broj plus reč **sati**, **nedelje** ili **meseci**.
2. Ako želite da se vaš zadatak pojavi kao kontrolna tačka u obliku dijamanta u prikazu **Vremenska osa**, u koloni **Trajanje**, unesite **0 dana**.
3. Pritisnite taster **Enter** da biste otišli do polje **Trajanje** sledećeg zadatka i nastavili sa unošenjem trajanja.

  > [!NOTE]
  > Ne možete da unesete trajanje za rezimirane zadatke.

Možete da dodate kolone u svoj projekat da biste pružili više detalja. Da biste to uradili, izaberite **Dodaj kolonu**. 

Za još informacija, pogledajte članak [Kreiranje projekta](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a>Podešavanje uloge i organizacione jedinice za generičkog člana projektnog tima
Dovršite sledeće korake da biste podesili ulogu i organizacionu jedinicu za generičkog člana tima.

1. Na stranici **Zadaci**, izaberite red **Zadatak** za **Zadataka A**. 
2. U **Dodeljeno osobi**, izaberite **Dodajte generički resurs**. Ovo otvara stranicu **Brzo kreiranja člana tima**.
3. Na stranici **Brzo kreiranje člana tima**, navedite atribute generičkog člana tima koji može da izvrši ovaj zadatak.
4. Izaberite odgovarajuću ulogu i organizacionu jedinicu, a zatim izaberite **Sačuvaj i zatvori**. Generički član tima se kreira i dodeljuje ovom zadatku. 
5. Ponovite korake 1–4 za **Zadatak B**. Međutim, **Zadatak B** mora da ima drugu ulogu i organizacionu jedinicu dodeljenu generičkom članu tima od **Zadatka A**. 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a>Podešavanje uloge i organizacione jedinice za projektni zadatak
Dovršite sledeće korake da biste podesili ulogu i organizacionu jedinicu za zadatak.

1. Nakon što kreirate **Zadatak A**, izaberite zadatak, a zatim izaberite ikonu **i** da biste otvorili okno **Detalji zadatka**. 
2. Na oknu **Detalji zadatka**, pomerite se na dno i izaberite **Prikaži detalje** da biste otvorili stranicu **Detalji zadatka**.
3. Na stranici **Detalji zadatka**, u opciji **Uloga** i **Organizaciona jedinica**, dodajte vrednosti koje su potrebne za izvršenje ovog zadatka za resurs. 

  > [!NOTE]
  > Ako dovršite ovaj scenario koristeći demo podatke za Project Operations, izaberite **Potencijalni klijent za konsultacije** za ulogu, a **Fabrikam US** kao organizacionu jedinicu.

4. Izaberite **Zadatak B**, a zatim izaberite zadatak.
5. Izaberite ikonu **i** da biste otvorili okno **Detalji o zadatku**. 
6. Na oknu **Detalji zadatka**, pomerite se na dno i izaberite **Prikaži detalje** da biste otvorili stranicu **Detalji zadatka**.
7. Na stranici **Detalji zadatka**, u opciji **Uloga** i **Organizaciona jedinica**, dodajte vrednosti koje su potrebne da bi resurs obavio ovaj zadatak. Vrednosti u stavkama **Uloga** i **Organizaciona jedinica** za **Zadatak B** moraju da se razlikuju od onih za **Zadatak A**. 

  > [!NOTE]
  > Ako dovršite ovaj scenario koristeći demo podatke za Project Operations, izaberite **Mrežni tehničar** za ulogu, a **Fabrikam US** kao organizacionu jedinicu.

8. Sačuvajte i zatvorite stranicu **Detalji zadatka**. 

## <a name="team-member-and-estimates-behavior"></a>Član tima i ponašanje procena 
Da biste razumeli ponašanje na mreži **Član tima** i procenama, izvršite sledeće korake.

1. Na mreži **Član tima**, izaberite dva generička člana tima, a zatim izaberite **Generiši zahteve**. Tako ćete generisati zahteve za resursima. 
2. Izaberite red člana tima za **Vođa konsultanata**, a zatim izaberite **Rezerviši**. Tabla rasporeda otvara se listom resursa. Izaberite resurs, a zatim izaberite **Rezerviši** da biste rezervisali resurs prema tom zahtevu.
3. Izaberite red člana tima za **Mrežni tehničar**, a zatim izaberite **Rezerviši**. Tabla rasporeda otvara se listom resursa. Izaberite isti resurs kao iznad, a zatim izaberite **Rezerviši** da biste rezervisali resurs prema tom zahtevu.

### <a name="team-member-grid"></a>Mreža člana tima 

Na mreži **Član tima**, dva generička zapisa člana tima se brišu i zamenjuju samo jednim resursom. Postoji jedan skup vrednosti za taj resurs, koji su podrazumevani skup vrednosti za **Ulogu** i **Organizacionu jedinicu**.

Kada proširite red za taj zapis člana tima, na zapisu člana tima možete videti određene zadatke za oba zadatka. Svaki red zadatka ima vrednosti specifične za zadatak za **ulogu** i **organizacionu jedinicu**. 

### <a name="estimates-grid"></a>Mreža procena 

Na mreži **Procene**, oba zadatka za isti resurs imaju različite cene. Cena dodele resursa **Zadatku A** određuje se korišćenjem vrednosti atributa **Uloga** za **Potencijalni klijent za konsultacije**. Cena dodele istog resursa **Zadatku B** određuje se korišćenjem vrednosti atributa **Uloga** za **tehničara mreže**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]