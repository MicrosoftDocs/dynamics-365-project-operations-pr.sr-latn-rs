---
title: Predračuni za projekat
description: Ovaj članak pruža informacije o proforma projektne fakture u projektne operacije.
author: rumant
ms.date: 04/06/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8f028ec12aa3144a2c1bf13f6f8ce90c9de48519
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934567"
---
# <a name="proforma-project-invoices"></a>Predračuni za projekat

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Predračun za projekat daje menadžerima projekta drugi nivo odobravanja pre nego što kreiraju fakture za klijente. Prvi nivo odobravanja se završava kada se odobre stavke vremena, troškova i materijala koje prosleđuju članovi projektnog tima.

Jednostavna primena usluge Dynamics 365 Project Operations nije dizajnirana da generiše fakture prema klijentima. Sledeća lista pokazuje zašto se fakture ne mogu generisati:

- Ne sadrži poreske informacije.
- Nije moguće konvertovati druge valute u valutu za fakturisanje.
- Nije moguće pravilno formatirati fakture za štampanje.

Umesto toga, možete da koristite finansijski ili računovodstveni sistem da biste kreirali fakture prema klijentima koje koriste informacije u generisanim predlozima za fakture.

## <a name="creating-project-invoices"></a>Kreiranje faktura za projekte

Fakture za projekte mogu se kreirati jedna po jedna ili masovno. Možete ih kreirati ručno ili ih možete konfigurisati tako da se generišu pri automatizovanim pokretanjima.

### <a name="manually-create-project-invoices"></a>Ručno kreiranje faktura za projekte 

Na stranici sa listom **Ugovori o projektima** možete posebno da kreirate fakture za projekte za svaki ugovor o projektu ili da kreirate fakture masovno za više ugovora o projektima.

   - Da biste kreirali fakturu za specifičan ugovor o projektu, na stranici liste **Ugovori o projektima** otvorite jedan ugovor o projektu, a zatim izaberite **Kreiraj fakturu**.

   Faktura se generiše za sve transakcije za izabrani ugovor o projektu koji imaju status **Spremno za fakturisanje**. Te transakcije uključuju vreme, troškove, materijale, kontrolne tačke, predmete ugovora zasnovane na proizvodima i druge stavke nenaplaćene prodaje u glavnoj knjizi prodaje koje su možda potvrđene.

Kako se grupno kreiraju fakture:

1. Na stranici liste **Ugovori o projektima** izaberite jedan ili više ugovora o projektu za koje morate kreirati fakturu, a zatim izaberite **Kreiraj fakture za projekte**.
2. Poruka upozorenja vas obaveštava da možda postoji kašnjenje pre kreiranja faktura. Ovaj proces se takođe prikazuje. Izaberite **U redu** da biste zatvorili polje poruke.

   Faktura se generiše za sve transakcije za predmet ugovora sa statusom **Spremno za fakturisanje**. Te transakcije uključuju vreme, troškove, materijale, kontrolne tačke, predmete ugovora zasnovane na proizvodima i druge stavke nenaplaćene prodaje u glavnoj knjizi prodaje koje su možda potvrđene.

3. Prikažite fakture koje su generisane tako što ćete otići na **Prodaja** \> **Naplata** \> **Fakture**. Videćete jednu fakturu za svaki ugovor o projektu.

### <a name="set-up-automated-creation-of-project-invoices"></a>Podešavanje automatizovanog kreiranja faktura za projekte 

Sledite ove korake da biste konfigurisali automatsko pokretanje faktura.

1. Idite do stavke **Podešavanja** \> **Grupni poslovi**.
2. Kreirajte grupni posao i imenujte ga **Kreiranje faktura u usluzi Project Operations**. Ime grupnog posla mora da sadrži termin „Kreiranje faktura“.
3. U polju **Vrsta posla** izaberite **Nijedna**. Podrazumevano se opcije **Dnevna učestalost** i **Je aktivna** podešavaju na **Da**.
4. Izaberite **Pokreni tok posla**. U dijalogu **Zapis za pronalaženje** ćete videti sledeće tokove posla:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Izaberite **ProcessRunCaller**, a zatim **Dodaj**.
6. U sledećem dijalogu izaberite **U redu**. Tok posla **Hibernacija** prati tok posla **Proces**.

    Možete izabrati i **ProcessRunner** u koraku 5. Nakon toga, kada izaberete **U redu**, tok posla **Proces** će biti praćen tokom posla **Hibernacija**.

Tokovi posla **ProcessRunCaller** i **ProcessRunner** kreiraju fakture. **ProcessRunCaller** poziva **ProcessRunner**. **ProcessRunner** je tok posla koji kreira fakture. Taj tok posla prolazi kroz sve predmete ugovora za koje se fakture moraju kreirati i kreira fakture. Da bi odredio predmete ugovora za koje fakture moraju biti kreirane, tok posla traži datume pokretanja fakturisanja za predmete ugovora. Ako predmeti ugovora koji pripadaju jednom ugovoru imaju isti datum pokretanja fakture, transakcije se kombinuju u jednu fakturu koja ima dve stavke fakture. Ako ne postoje transakcije za koje treba kreirati fakture, neće se kreirati nijedna faktura.

Nakon što se **ProcessRunner** pokrene, on poziva **ProcessRunCaller**, obezbeđuje vreme završetka i zatvara se. **ProcessRunCaller** zatim pokreće tajmer koji će biti pokrenut tokom perioda od 24 časa od određenog vremena završetka. Na kraju tajmera **ProcessRunCaller** se zatvara.

Posao grupne obrade za kreiranje faktura je periodični posao. Ako se ova grupna obrada pokreće više puta, kreira se više instanci posla i to može da izazove greške. Da bi se taj problem rešio, pokrenite grupnu obradu samo jednom i ponovo ga pokrenite samo ako prestane da radi.

> [!NOTE]
> Grupno fakturisanje se izvodi samo za predmete ugovora o projektu koji su konfigurisani prema rasporedima faktura. Predmet ugovora sa načinom naplate uz fiksnu cenu mora da ima konfigurisane kontrolne tačke. Predmet ugovora za projekat sa načinom naplate vremena i materijala treba da uspostavi raspored faktura na osnovu datuma. Isto se odnosi i na predmet ugovora zasnovan na projektu.      
 
### <a name="edit-a-draft-invoice"></a>Uređivanje radne verzije fakture

Kada kreirate radnu verziju fakture za projekat, sve nenaplaćene prodajne transakcije, koje su kreirane kada su stavke vremena i troškova odobrene, prenose se na fakturu. Možete izvršiti sledeća podešavanja dok je faktura još uvek fazi radne verzije:

- Izbrišite ili uredite detalje stavke fakture.
- Uredite i prilagodite količinu i vrstu naplate.
- U fakturu direktno dodajte vreme, trošak, materijal i naknade kao transakcije. Ovu funkciju možete koristiti ako je stavka fakture mapirana u predmet ugovora koji dozvoljava ove klase transakcija.

Izaberite **Potvrdi** da biste potvrdili fakturu. Ova radnja je jednosmerna. Kada izaberete **Potvrdi**, faktura postaje samo za čitanje i kreira stvarne vrednosti naplaćene prodaje iz svakog detalja stavke fakture za svaku stavku fakture. Ako detalj stavke fakture upućuje na stvarne vrednosti nenaplaćene prodaje, sistem takođe stornira stvarnu vrednost nenaplaćene prodaje. Bilo koji detalj stavke fakture koji je kreiran na osnovu stavke vremena, troškova ili upotrebe materijala odnosiće se na stvarnu vrednost nenaplaćene prodaje. Sistemi za integraciju glavne knjige mogu koristiti ovo storniranje da bi opozvali posao u toku na projektu (WIP) u računovodstvene svrhe.

### <a name="correct-a-confirmed-invoice"></a>Ispravljanje potvrđene fakture

Potvrđene fakture se mogu uređivati. Kada ispravite potvrđenu fakturu, kreira se nova radna verzija korigovane fakture. Pošto je pretpostavka da želite da stornirate sve transakcije i količine iz originalne fakture, ova korigovana faktura uključuje sve transakcije iz originalne fakture, a sve količine na njoj su nula.

Ako postoje transakcije koje ne zahtevaju korekciju, možete ih ukloniti iz radne verzije korigovane fakture. Ako želite da stornirate ili opozovete samo delimičnu količinu, polje **Količina** u detaljima stavke možete urediti. Ako otvorite detalj stavke fakture, možete videti količinu originalne fakture. Zatim možete da uredite količinu trenutne fakture tako da bude manja ili veća od količine originalne fakture.

Kada potvrdite korigovanu fakturu, stornira se originalna stvarna vrednosti naplaćene prodaje i kreira se nova stvarna vrednost naplaćene prodaje. Ako je količina smanjena, razlika će dovesti do toga da se kreira nova stvarna vrednost nenaplaćene prodaje. Na primer, ako je originalna naplaćena prodaja bila za osam sati, a detalj stavke korigovane fakture ima manju količinu od šest sati, stornira se prvobitna naplaćena stavka prodaje i kreiraju se dve nove stvarne vrednosti:

- Stvarna vrednosti naplaćene prodaje za šest sati.
- Stvarna vrednosti nenaplaćene prodaje za preostala dva sata. Ova transakcija može biti naplaćena kasnije ili označena kao nenaplativa, u zavisnosti od pregovora sa klijentom.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
