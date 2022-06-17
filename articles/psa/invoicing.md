---
title: Fakturisanje u aplikaciji Project Service Automation
description: Ovaj članak pruža informacije o fakturisanju.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: fa036dda6514449b04e1416bde2cd9c21fc558b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926839"
---
# <a name="invoicing-in-project-service-automation"></a>Fakturisanje u aplikaciji Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Fakturisanje u sistemu Dynamics 365 Project Service Automation je korisno jer daje menadžerima projekata drugi nivo odobravanja pre nego što kreiraju fakture za klijente. Prvi nivo odobravanja se završi kada se odobre stavke vremena i troškova koje prosleđuju članovi projektnog tima.

PSA nije dizajniran da generiše fakture u okruženju klijenta iz sledećih razloga:

- Ne sadrži poreske informacije.
- Ne može da konvertuje druge valute u valutu fakturisanja koristeći ispravno konfigurisane kurseve valuta.
- Ne može ispravno da formatira fakture kako bi mogle da se štampaju.

Umesto toga, možete da koristite finansijski ili računovodstveni sistem da biste kreirali fakture u okruženju klijenta koje koriste informacije iz predloga za fakture koji se generišu u aplikaciji PSA.

## <a name="creating-project-invoices-in-psa"></a>Kreiranje faktura za projekte u aplikaciji PSA

Fakture za projekte mogu se kreirati jedna po jedna ili masovno. Možete ih kreirati ručno ili ih možete konfigurisati tako da se generišu pri automatizovanim pokretanjima.

### <a name="manually-create-project-invoices-in-psa"></a>Ručno kreiranje faktura za projekte u aplikaciji PSA

Na stranici sa listom **Ugovori o projektima** možete posebno da kreirate fakture za projekte za svaki ugovor o projektu ili da kreirate fakture masovno za više ugovora o projektima.

Sledite ovaj korak da biste kreirali fakturu za određeni ugovor o projektu.

- Na stranici liste **Ugovori o projektima** otvorite ugovor o projektu, a zatim izaberite **Kreiraj fakturu**.

    ![Kreiranje faktura za projekat za određeni ugovor o projektu.](media/CreateProjectInvoicesOneByOne.png)

    Faktura se generiše za sve transakcije za izabrani ugovor o projektu koji imaju status **Spremno za fakturisanje**. Ove transakcije uključuju vreme, troškove, kontrolne tačke i predmete ugovora zasnovane na proizvodu.

Sledite ove korake da biste kreirali fakture masovno.

1. Na stranici liste **Ugovori o projektima** izaberite jedan ugovor ili više ugovora o projektima za koje morate kreirati fakturu, a zatim izaberite **Kreiraj fakture za projekte**.

    ![Masovno kreiranje faktura za projekte.](media/CreateProjectInvoicesBulk.png)

    Poruka upozorenja vas obaveštava da možda postoji kašnjenje pre kreiranja faktura. Ovaj proces se takođe prikazuje.

2. Izaberite **U redu** da biste zatvorili polje poruke.

    Faktura se generiše za sve transakcije za predmet ugovora sa statusom **Spremno za fakturisanje**. Ove transakcije uključuju vreme, troškove, kontrolne tačke i predmete ugovora zasnovane na proizvodu.

3. Da biste videli generisane fakture, idite na **Prodaja** \> **Naplata** \> **Fakture**. Videćete jednu fakturu za svaki ugovor o projektu.

### <a name="set-up-automated-creation-of-project-invoices-in-psa"></a>Podešavanje automatizovanog kreiranja faktura za projekte u aplikaciji PSA

Sledite ove korake da biste konfigurisali automatsko pokretanje faktura u aplikaciji PSA.

1. Idite na **Project Service** \> **Podešavanja** \> **Grupni poslovi**.
2. Kreirajte grupni posao i imenujte ga **PSA kreiranje faktura**. Ime grupnog posla mora da sadrži termin „Kreiranje faktura“.
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
> Paketno fakturisanje u Project Service Automation pokreće se samo za predmete projektnih ugovora koji su konfigurisani rasporedima faktura. Predmet ugovora sa načinom naplate uz fiksnu cenu mora da ima konfigurisane kontrolne tačke. Predmet ugovora za projekat sa načinom naplate vremena i materijala treba da uspostavi raspored faktura na osnovu datuma. Informacije o podešavanju frekvencija fakturisanja u kontekstu projekta koji se zasniva na redu ponude, navedene su u redovima članka, [ponuda i ponuda](basic-quote-lines.md#invoice-schedule). Isto se odnosi i na predmet ugovora zasnovan na projektu.      
 
### <a name="edit-a-draft-psa-invoice"></a>Uređivanje radne verzije PSA fakture

Kada kreirate radnu verziju fakture za projekat, sve nenaplaćene prodajne transakcije, koje su kreirane kada su stavke vremena i troškova odobrene, prenose se na fakturu. Možete izvršiti sledeća podešavanja dok je faktura još uvek fazi radne verzije:

- Izbrišite ili uredite detalje stavke fakture.
- Uredite i prilagodite količinu i vrstu naplate.
- U fakturu direktno dodajte vreme, trošak i naknade kao transakcije. Ovu funkciju možete koristiti ako je stavka fakture mapirana u predmet ugovora koji dozvoljava ove klase transakcija.

Izaberite **Potvrdi** da biste potvrdili fakturu. Radnja potvrde ne može da se opozove. Kada izaberete **Potvrdi**, sistem podešava fakturu kao samo za čitanje i kreira stvarne vrednosti naplaćene prodaje iz svakog detalja stavke fakture za svaku stavku fakture. Ako detalj stavke fakture upućuje na stvarne vrednosti nenaplaćene prodaje, sistem takođe stornira stvarnu vrednost nenaplaćene prodaje. (Bilo koji detalj stavke fakture koji je kreiran iz stavke vremena ili troškova upućuje na stvarnu vrednost nenaplaćene prodaje.) Sistemi za integraciju glavne knjige mogu koristiti ovo storniranje da bi opozvali tekući rad na projektu u računovodstvene svrhe.

### <a name="correct-a-confirmed-psa-invoice"></a>Ispravljanje potvrđene PSA fakture

Potvrđene PSA fakture se mogu uređivati (ispravljati). Kada ispravite potvrđenu fakturu, kreira se nova radna verzija korigovane fakture. Pošto je pretpostavka da želite da stornirate sve transakcije i količine iz originalne fakture, ova korigovana faktura uključuje sve transakcije iz originalne fakture, a sve količine na njoj su 0 (nula).

Ako neke transakcije ne zahtevaju korekciju, možete ih ukloniti iz radne verzije korigovane fakture. Ako želite da stornirate ili opozovete samo delimičnu količinu, polje **Količina** u detaljima stavke možete urediti. Ako otvorite detalj stavke fakture, možete videti količinu originalne fakture. Zatim možete da uredite količinu trenutne fakture tako da bude manja ili veća od količine originalne fakture.

Kada potvrdite korigovanu fakturu, stornira se originalna stvarna vrednosti naplaćene prodaje i kreira se nova stvarna vrednost naplaćene prodaje. Ako je količina smanjena, razlika će dovesti do toga da se kreira i nova stvarna vrednost nenaplaćene prodaje. Na primer, ako je originalna naplaćena prodaja bila za osam sati, a detalj stavke korigovane fakture ima manju količinu od šest sati, PSA stornira prvobitnu naplaćenu stavku prodaje i kreira dve nove stvarne vrednosti:

- Stvarna vrednosti naplaćene prodaje za šest sati.
- Stvarna vrednosti nenaplaćene prodaje za preostala dva sata. Ova transakcija može biti naplaćena kasnije ili označena kao nenaplativa, u zavisnosti od pregovora sa klijentom.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
