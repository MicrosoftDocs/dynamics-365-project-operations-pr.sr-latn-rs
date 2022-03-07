---
title: Rešavanje problema sa radom u mreži podataka
description: Ova tema pruža informacije o rešavanju problema potrebne za rad u mreži zadataka.
author: ruhercul
ms.date: 09/22/2021
ms.topic: article
ms.product: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 67136229d84a09886fffe9677b10f671aea3c393
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547216"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Rešavanje problema sa radom u mreži podataka 


_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, jednostavnu implementaciju – pogodbu o predračunima, Project for the Web_

Mreža zadataka koju koristi Dynamics 365 Project Operations je hostovani iframe u okviru usluge Microsoft Dataverse. Kao rezultat ove upotrebe, potrebno je ispuniti posebne zahteve kako bi se osiguralo da potvrda identiteta i autorizacija pravilno funkcionišu. Ova tema opisuje uobičajena pitanja koja mogu da utiču na sposobnost prikazivanja mreže ili upravljanje zadacima u strukturnoj analizi posla (SAP).

Uobičajeni problemi obuhvataju:

- Kartica **Zadatak** na mreži zadataka je prazna.
- Prilikom otvaranja projekta, projekat se ne učitava i korisnički interfejs (UI) je zaglavljen na okretnom dugmetu.
- Administracija privilegija za **Project for the Web**.
- Promene se ne čuvaju kada kreirate, ažurirate ili izbrišete zadatak.

## <a name="issue-the-task-tab-is-empty"></a>Problem: Kartica „Zadatak“ je prazna

### <a name="mitigation-1-enable-cookies"></a>Ublažavanje 1: Omogućite kolačiće

Usluga Project Operations zahteva da kolačići trećih strana budu omogućeni za prikazivanje strukturne analize posla. Kada nezavisni kolačići nisu omogućeni, umesto da vidite zadatke, videćete praznu stranicu kada odaberete karticu **Zadaci** na stranici **Projekat**.

Za pregledače Microsoft Edge ili Google Chrome, sledeći postupci opisuju kako da ažurirate podešavanja pregledača kako biste omogućili nezavisne kolačiće.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Otvorite pregledač Edge.
2. U gornjem desnom uglu izaberite **tri tačke** (...), a zatim izaberite **Podešavanja**.
3. U delu **Kolačići i dozvole za lokacije** izaberite **Kolačići i podaci o lokacijama**.
4. Isključite **Blokiraj kolačiće treće strane**.
5. Osvežite pregledač. 

#### <a name="google-chrome"></a>Google Chrome

1. Otvorite pregledač Chrome.
2. U gornjem desnom uglu izaberite tri vertikalne tačke, a zatim izaberite **Podešavanja**.
3. U delu **Privatnost i bezbednost** izaberite **Kolačići i drugi podaci o lokacijama**.
4. Izaberite **Dozvoli sve kolačiće**.
5. Osvežite pregledač. 

> [!NOTE]
> Ako blokirate nezavisne kolačiće, svi kolačići i podaci o lokacijama sa drugih lokacija biće blokirani, čak i ako je lokacija dozvoljena na listi izuzetaka.

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>Ublažavanje 2: Potvrdite da je krajnja tačka PEX ispravno konfigurisana

Project Operations zahteva da parametar projekta upućuje na PEX krajnju tačku. Ova krajnja tačka je potrebna za komunikaciju sa uslugom koja se koristi za prikazivanje strukturne analize posla. Ako parametar nije omogućen, dobićete grešku „Parametar projekta nije važeći“. Da biste ažurirali krajnju tačku PEX, dovršite sledeće korake.

1. Dodajte polje **PEX krajnja tačka** na stranicu **Parametri projekta**.
2. Identifikujte tip proizvoda koji koristite. Ova vrednost se koristi kada je PEX krajnja tačka podešena. Nakon preuzimanja, tip proizvoda je već definisan u PEX krajnjoj tački. Zadržite tu vrednost.
3. Ažurirajte polje sledećom vrednošću: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2` U sledećoj tabeli navedeni su parametri vrste koje treba koristiti na osnovu vrste proizvoda.

      | **Tip proizvoda**                     | **Tip parametra** |
      |--------------------------------------|--------------------|
      | Project for the Web za podrazumevanu organizaciju   | tip=0             |
      | Project for the Web za organizaciju sa CDS nazivom | tip=1             |
      | Project Operations                   | tip=2             |

4. Uklonite polje sa stranice **Parametri projekta**.

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>Problem: Projekat se ne učitava i korisnički interfejs je zaglavljen na okretnom dugmetu

Za potrebe potvrde identiteta, iskačući prozori moraju da budu omogućeni da bi se mreža zadataka učitala. Ako iskačući prozori nisu omogućeni, ekran će se zaglaviti na okretnom dugmetu za učitavanje. Sledeća slika prikazuje URL adresu sa blokiranom iskačućom oznakom u traci adrese, što dovodi do toga da se okretno dugme zaglavi pokušavajući da učita stranicu. 

   ![Zaglavljeno okretno dugme i blokiranje iskačućih prozora.](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>Ublažavanje 1: Omogućite iskačuće prozore

Kada se vaš projekat zaglavi na okretnom dugmetu, može se desiti da iskačući prozori nisu omogućeni.

#### <a name="microsoft-edge"></a>Microsoft Edge

Postoje dva načina da omogućite iskačuće prozore u pregledaču Edge.

1. U pregledaču Edge izaberite obaveštenje u gornjem desnom uglu pregledača.
2. Izaberite **Uvek dozvoli iskačuće prozore i preusmeravanja sa** specifičnog Dataverse okruženja.
 
     ![Prozor za blokirane iskačuće prozore.](media/enablepopups.png)

Pored toga, možete takođe obavite jedan od sledećih koraka:

1. Otvorite pregledač Edge.
2. U gornjem desnom uglu izaberite **tri tačke** (...), a zatim izaberite **Podešavanja** > **Dozvole za lokaciju** > **Iskačući prozori i preusmeravanja**.
3. Isključite opciju **Iskačući prozori i preusmeravanja** za blokiranje iskačućih prozora ili je uključite da biste omogućili iskačuće prozore na svom uređaju.
4. Nakon što omogućite iskačuće prozore, osvežite pregledač. 

#### <a name="google-chrome"></a>Google Chrome
1. Otvorite pregledač Chrome.
2. Idite na stranicu na kojoj su iskačući prozori blokirani.
3. Na traci adrese izaberite **Iskačući prozor je blokiran**.
4. Izaberite vezu za iskačući prozor koji želite da vidite.
5. Nakon što omogućite iskačuće prozore, osvežite pregledač. 

> [!NOTE]
> Da biste uvek videli iskačuće prozore za tu lokaciju, izaberite opciju **Uvek dozvoli iskačuće prozore i preusmeravanja sa [lokacija]**, a zatim izaberite **Gotovo**.

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>Problem 3: Administracija privilegija za Project for the Web

Project Operations se oslanja na eksternu uslugu zakazivanja. Usluga zahteva da korisnik ima nekoliko dodeljenih uloga koje mu omogućavaju čitanje i pisanje za entitete povezane sa SAP-om. Ti entiteti uključuju projektne zadatke, dodeljivanje resursa i zavisne elemente zadataka. Ako korisnik ne može ne može da prikaže SAP prilikom navigacije do kartice **Zadaci**, to je verovatno zato što **Projekat** za **Project Operations** nije omogućen. Korisnik može da dobije grešku za bezbedonosnu ulogu ili grešku povezanu sa uskraćivanjem pristupa.

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>Ublažavanje 1: Potvrdite bezbednosne uloge korisnika aplikacije i krajnjeg korisnika

1. Idite na **Podešavanja** > **Bezbednost** > **Korisnici** > **Korisnici aplikacija**.  

   ![Čitač aplikacije.](media/applicationuser.jpg)
   
2. Dvaput kliknite na zapis o korisnicima aplikacije da biste potvrdili:

     - Korisnik ima pristup projektu. To možete učiniti ako proverite da li korisnik ima bezbednosnu ulogu **Vođa projekata**.
     - Korisnik aplikacije Microsoft Project postoji i pravilno je konfigurisan.
 
3. Ako ovaj korisnik ne postoji, kreirajte novi korisnički zapis. 
4. Izaberite opciju **Novi Korisnici**, promenite obrazac za prijavu u **Korisnik aplikacije**, a zatim dodajte **ID aplikacije**.

   ![Detalji o korisniku aplikacije.](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>Problem 4: Promene se ne čuvaju kada kreirate, ažurirate ili izbrišete zadatak

Kada izvršite jedno ili više ažuriranja u SAP-u, promene su neuspešne i ne čuvaju se. Došlo je do greške u mreži rasporeda uz poruku „Nedavna promena koju ste uneli nije mogla da se sačuva“.

### <a name="mitigation-1-validate-the-license-assignment"></a>Ublažavanje 1: Potvrdite prenos licence

1. Proverite da li je korisniku dodeljena ispravna licenca i da li je usluga omogućena u detaljima planova usluge licence.  
2. Proverite da li korisnik može da otvori **project.microsoft.com**.
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>Ublažavanje 2: Konfiguracija potvrde korisnika aplikacije „Project“
1. Proverite da li je kreiran korisnik aplikacije „Project“.
2. Primenite sledeće bezbednosne uloge na korisnika:
  
  - Dataverse korisnik ili osnovni korisnik
  - Project Operations sistem
  - Projektni sistem
  - Sistem dvostrukog upisivanja za Project Operations. Ova uloga je neophodna za resurs/scenarije primene koji nisu zasnovani na zalihama za Project Operations.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
