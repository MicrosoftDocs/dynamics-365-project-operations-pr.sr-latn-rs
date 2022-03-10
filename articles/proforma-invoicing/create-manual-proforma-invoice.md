---
title: Predračuni
description: Ova tema pruža informacije o predračunima u usluzi Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2050a313fe530065341410d60801b13eb958cb32ae24eb4a0a71ab7ea5061881
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995643"
---
# <a name="proforma-invoices"></a>Predračuni

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Predračun daje menadžerima projekta drugi nivo odobravanja pre nego što kreiraju fakture za klijente. Prvi nivo odobravanja se završava kada se odobre stavke vremena, troškova i materijala koje prosleđuju članovi projektnog tima. Potvrđeni predračuni su dostupni u modulu Računovodstvo projekata u usluzi Project Operations. Računovođe projekata mogu izvršiti dodatna ažuriranja kao što su porez na promet, računovodstvo i izgled fakture.


## <a name="creating-project-invoices"></a>Kreiranje faktura za projekte

Fakture za projekte mogu se kreirati jedna po jedna ili masovno. Možete ih kreirati ručno ili ih možete konfigurisati tako da se generišu pri automatizovanim pokretanjima.

### <a name="manually-create-project-invoices"></a>Ručno kreiranje faktura za projekte 

Na stranici sa listom **Ugovori o projektima** možete posebno da kreirate fakture za projekte za svaki ugovor o projektu ili da kreirate fakture masovno za više ugovora o projektima.

Sledite ovaj korak da biste kreirali fakturu za određeni ugovor o projektu.

- Na stranici liste **Ugovori o projektima** otvorite ugovor o projektu, a zatim izaberite **Kreiraj fakturu**.

    Faktura se generiše za sve transakcije za izabrani ugovor o projektu koji imaju status **Spremno za fakturisanje**. Te transakcije uključuju vreme, troškove, materijale, kontrolne tačke i druge nefakturisane stavke u glavnoj knjizi prodaje.

Sledite ove korake da biste kreirali fakture masovno.

1. Na stranici liste **Ugovori o projektima** izaberite jedan ugovor ili više ugovora o projektima za koje morate kreirati fakturu, a zatim izaberite **Kreiraj fakture za projekte**.

    Poruka upozorenja vas obaveštava da možda postoji kašnjenje pre kreiranja faktura. Ovaj proces se takođe prikazuje.

2. Izaberite **U redu** da biste zatvorili polje poruke.

    Faktura se generiše za sve transakcije za predmet ugovora sa statusom **Spremno za fakturisanje**. Te transakcije uključuju vreme, troškove, materijale, kontrolne tačke i druge nefakturisane stavke u glavnoj knjizi prodaje.

3. Da biste videli generisane fakture, idite na **Prodaja** \> **Naplata** \> **Fakture**. Videćete jednu fakturu za svaki ugovor o projektu.

### <a name="set-up-automated-creation-of-project-invoices"></a>Podešavanje automatizovanog kreiranja faktura za projekte 

Sledite ove korake da biste konfigurisali automatsko pokretanje faktura.

1. Idite do stavke **Podešavanja** \> **Grupni poslovi**.
2. Kreirajte grupni posao i imenujte ga **Kreiranje faktura u usluzi Project Operations**. Ime grupnog posla mora da sadrži termin „Kreiranje faktura“.
3. U polju **Vrsta posla** izaberite **Nijedna**. Podrazumevano se opcije **Dnevna učestalost** i **Je aktivna** podešavaju na **Da**.
4. Izaberite **Pokreni tok posla**. U dijalogu **Pronalaženje zapisa** ćete videti tri toka posla:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Izaberite **ProcessRunCaller**, a zatim **Dodaj**.
6. U sledećem dijalogu izaberite **U redu**. Tok posla **Hibernacija** prati tok posla **Proces**.

    Možete izabrati i **ProcessRunner** u koraku 5. Nakon toga, kada izaberete **U redu**, tok posla **Proces** će biti praćen tokom posla **Hibernacija**.

Tokovi posla **ProcessRunCaller** i **ProcessRunner** kreiraju fakture. **ProcessRunCaller** poziva **ProcessRunner**. **ProcessRunner** je tok posla koji zapravo kreira fakture. On prolazi kroz sve predmete ugovora za koje se moraju kreirati fakture i kreira fakture za te predmete. Da bi odredio predmete ugovora za koje fakture moraju biti kreirane, posao traži datume pokretanja fakture za predmete ugovora. Ako predmeti ugovora koji pripadaju jednom ugovoru imaju isti datum pokretanja fakture, transakcije se kombinuju u jednu fakturu koja ima dve stavke fakture. Ako ne postoje transakcije za koje treba kreirati fakture, posao preskače kreiranje fakture.

Nakon što se **ProcessRunner** pokrene, on poziva **ProcessRunCaller**, obezbeđuje vreme završetka i zatvara se. **ProcessRunCaller** zatim pokreće tajmer koji će biti pokrenut tokom perioda od 24 časa od određenog vremena završetka. Na kraju tajmera **ProcessRunCaller** se zatvara.

Posao grupne obrade za kreiranje faktura je periodični posao. Ako se ova grupna obrada pokreće više puta, kreira se više instanci posla i izazivaju greške. Zbog toga bi trebalo samo jednom da pokrenete grupnu obradu i trebalo bi da je ponovo pokrenete samo ako prestane da radi.

> [!NOTE]
> Grupno fakturisanje se izvodi samo za predmete ugovora o projektu koji su konfigurisani prema rasporedima faktura. Predmet ugovora sa načinom naplate uz fiksnu cenu mora da ima konfigurisane kontrolne tačke. Predmet ugovora za projekat sa načinom naplate vremena i materijala treba da uspostavi raspored faktura na osnovu datuma. Isto se odnosi i na predmet ugovora zasnovan na projektu.      
 
### <a name="edit-a-draft-invoice"></a>Uređivanje radne verzije fakture

Kada kreirate radnu verziju fakture za projekat, na fakturu se prenose sve nenaplaćene transakcije prodaje koje su kreirane kada su stavke vremena, troškova i korišćenja materijala odobrene. Možete izvršiti sledeća podešavanja dok je faktura još uvek fazi radne verzije:

- Izbrišite ili uredite detalje stavke fakture.
- Uredite i prilagodite količinu i vrstu naplate.

Izaberite **Potvrdi** da biste potvrdili fakturu. Radnja potvrde ne može da se opozove. Kada izaberete **Potvrdi**, sistem podešava fakturu kao samo za čitanje i kreira stvarne vrednosti naplaćene prodaje iz svakog detalja stavke fakture za svaku stavku fakture. Ako detalj stavke fakture upućuje na stvarne vrednosti nenaplaćene prodaje, sistem takođe stornira stvarnu vrednost nenaplaćene prodaje. (Bilo koji detalj stavke fakture koji je kreiran iz stavke vremena ili troškova upućuje na stvarnu vrednost nenaplaćene prodaje.) Sistemi za integraciju glavne knjige mogu koristiti ovo storniranje da bi opozvali tekući rad na projektu u računovodstvene svrhe.

### <a name="correct-a-confirmed-invoice"></a>Ispravljanje potvrđene fakture

Potvrđene fakture se mogu uređivati (ispravljati). Kada ispravite potvrđenu fakturu, kreira se nova radna verzija korigovane fakture. Pošto je pretpostavka da želite da stornirate sve transakcije i količine iz originalne fakture, ova korigovana faktura uključuje sve transakcije iz originalne fakture, a sve količine na njoj su 0 (nula).

Ako neke transakcije ne zahtevaju korekciju, možete ih ukloniti iz radne verzije korigovane fakture. Ako želite da stornirate ili opozovete samo delimičnu količinu, polje **Količina** u detaljima stavke možete urediti. Ako otvorite detalj stavke fakture, možete videti količinu originalne fakture. Zatim možete da uredite količinu trenutne fakture tako da bude manja ili veća od količine originalne fakture.

Kada potvrdite korigovanu fakturu, stornira se originalna stvarna vrednosti naplaćene prodaje i kreira se nova stvarna vrednost naplaćene prodaje. Ako je količina smanjena, razlika će dovesti do toga da se kreira i nova stvarna vrednost nenaplaćene prodaje. Na primer, ako je originalna naplaćena prodaja bila za osam sati, a detalj stavke korigovane fakture ima manju količinu od šest sati, stornira se prvobitna naplaćena stavka prodaje i kreiraju se dve nove stvarne vrednosti:

- Stvarna vrednosti naplaćene prodaje za šest sati.
- Stvarna vrednosti nenaplaćene prodaje za preostala dva sata. Ova transakcija može biti naplaćena kasnije ili označena kao nenaplativa, u zavisnosti od pregovora sa klijentom.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
