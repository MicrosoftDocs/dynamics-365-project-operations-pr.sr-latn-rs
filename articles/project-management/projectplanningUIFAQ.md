---
title: Rešavanje problema sa radom u mreži podataka
description: Ova tema pruža informacije o rešavanju problema potrebne za rad u mreži zadataka.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: dedd989cc7c959d9ea97a0abfb13f8f1b2150a56
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286580"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Rešavanje problema sa radom u mreži podataka 

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Ova tema opisuje kako da rešite probleme na koje biste mogli naići tokom rada sa upravljanjem troškovima.

## <a name="enable-cookies"></a>Omogućavanje kolačića

Project Operations zahteva da nezavisni kolačići budu omogućeni kako bi se prikazivala strukturna analiza posla. Kada nezavisni kolačići nisu omogućeni, umesto da vidite zadatke, videćete praznu stranicu kada odaberete karticu **Zadaci** na stranici **Projekat**.

![Prazna kartica kada nezavisni kolačići nisu omogućeni](media/blankschedule.png)


### <a name="workaround"></a>Zaobilazno rešenje
Za pregledače Microsoft Edge ili Google Chrome, sledeći postupci opisuju kako da ažurirate podešavanja pregledača kako biste omogućili nezavisne kolačiće.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Otvorite pregledač Edge.
2. U gornjem desnom uglu izaberite **tri tačke** (...), a zatim izaberite **Podešavanja**.
3. U delu **Kolačići i dozvole za lokacije** izaberite **Kolačići i podaci o lokacijama**.
4. Isključite **Blokiraj kolačiće treće strane**.

#### <a name="google-chrome"></a>Google Chrome

1. Otvorite pregledač Chrome.
2. U gornjem desnom uglu izaberite tri vertikalne tačke, a zatim izaberite **Podešavanja**.
3. U delu **Privatnost i bezbednost** izaberite **Kolačići i drugi podaci o lokacijama**.
4. Izaberite **Dozvoli sve kolačiće**.

> [!IMPORTANT]
> Ako blokirate nezavisne kolačiće, svi kolačići i podaci o lokacijama sa drugih lokacija biće blokirani, čak i ako je lokacija dozvoljena na listi izuzetaka.

## <a name="pex-endpoint"></a>PEX krajnja tačka

Project Operations zahteva da parametar projekta upućuje na PEX krajnju tačku. Ova krajnja tačka je potreban za komunikaciju sa uslugom koja se koristi za prikazivanje strukturne analize posla. Ako parametar nije omogućen, dobićete grešku „Parametar projekta nije važeći“. 

### <a name="workaround"></a>Zaobilazno rešenje
 ![Polje „PEX krajnja tačka“ u parametru projekta](media/projectparameter.png)

1. Dodajte polje **PEX krajnja tačka** na stranicu **Parametri projekta**.
2. Ažurirajte polje sledećom vrednosti: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`
3. Uklonite polje sa stranice **Parametri projekta**.

## <a name="privileges-for-project-for-the-web"></a>Privilegije za projekat za veb

Project Operations se oslanja na eksternu uslugu zakazivanja. Usluga zahteva da korisnik ima nekoliko uloga dodeljenih za čitanje i pisanje u entitete povezane sa strukturnom analizom posla. Ti entiteti uključuju projektne zadatke, dodeljivanje resursa i zavisne elemente zadataka. Ako korisnik ne može da prikaže strukturnu analizu posla kada dođe na karticu **Zadaci**, to je verovatno zato što Project Operations nije omogućen. Korisnik može da dobije grešku za bezbedonosnu ulogu ili grešku povezanu sa uskraćivanjem pristupa.


## <a name="workaround"></a>Zaobilazno rešenje

1. Idite na **Podešavanja > Bezbednost > Korisnici > Korisnici aplikacija**.  

   ![Čitač aplikacije](media/applicationuser.jpg)
   
2. Dvaput kliknite na zapis korisnika aplikacije da biste proverili sledeće:

 - Korisnik ima pristup projektu. Ova verifikacija se obično obavlja tako što se osigurava da korisnik ima bezbednosnu ulogu **Menadžer projekta**.
 - Korisnik aplikacije Microsoft Project postoji i pravilno je konfigurisan.
 
3. Ako ovaj korisnik ne postoji, možete kreirati zapis novog korisnika. Izaberite **Novi korisnici**. Promenite obrazac za unos u **Korisnik aplikacije**, a zatim dodajte **ID aplikacije**.

   ![Detalji o korisniku aplikacije](media/applicationuserdetails.jpg)

4. Proverite da li je korisniku dodeljena ispravna licenca i da li je usluga omogućena u detaljima planova usluge licence.
5. Proverite da li korisnik može da otvori project.microsoft.com.
6. Proverite kroz parametre projekta da li sistem pokazuje na ispravnu krajnju tačku projekta.
7. Proverite da li je kreiran korisnik projektne aplikacije.
8. Primenite sledeće bezbednosne uloge na korisnika:

  - Korisnik usluge Dataverse
  - Project Operations sistem
  - Projektni sistem

## <a name="error-when-updating-the-work-breakdown-structure"></a>Greška pri ažuriranju strukturne analize posla

Kada se obavi jedno ili više ažuriranja strukturne analize posla, promene na kraju ne uspeju i nisu sačuvane. Dolazi do greške u mreži rasporeda uz napomenu da „Nedavna promena koju ste uneli nije mogla biti sačuvana“.

### <a name="workaround"></a>Zaobilazno rešenje

1. Proverite da li je korisniku dodeljena ispravna licenca i da li je usluga omogućena u detaljima planova usluge licence.
2. Proverite da li korisnik može da otvori project.microsoft.com.
3. Proverite da li sistem pokazuje na ispravnu krajnju tačku projekta.
4. Proverite da li je kreiran korisnik projektne aplikacije.
5. Primenite sledeće bezbednosne uloge na korisnika:
  
  - Dataverse korisnik ili osnovni korisnik
  - Project Operations sistem
  - Projektni sistem
  - Project Operations sistem dvostrukog upisivanja (ova uloga je potrebna ako primenjujete resurs/scenario koji nije zasnovan na zalihama usluge Project Operations.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]