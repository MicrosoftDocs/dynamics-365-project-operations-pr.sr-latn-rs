---
title: Aplikacija za mobilne uređaje Project Timesheet
description: Ovaj članak pruža informacije o mobilnoj Microsoft Dynamics 365 Project Timesheet aplikaciji. Aplikacija za mobilne uređaje Project Timesheet omogućava korisnicima da predaju i odobre radne listove za projekte na svom mobilnom uređaju.
author: abruer
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 730ed36841d07df60e8a8f343126209f0edcc593
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110992"
---
# <a name="project-timesheet-mobile-application"></a>Aplikacija za mobilne uređaje Project Timesheet

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>+Pregled

Mobilna Microsoft Dynamics 365 Project Timesheet aplikacija omogućava korisnicima da proslede i odobre vremenske listove za projekte na svom mobilnom uređaju (iPhone ili Android). Ova mobilna aplikacija isplivava na površinu funkcionalnosti lista sa vremenskim listom koja se nalazi u oblasti upravljanja projektima i knjigovodstvene Dynamics 365 Finance. On pomaže u poboljšanju produktivnosti i efikasnosti korisnika, a takođe omogućava pravovremeni unos i odobravanje vremenskih listova projekta.

## <a name="download-and-install-the-mobile-app"></a>Preuzmite i instalirajte aplikaciju za mobilne uređaje

Preuzmite i instalirajte aplikaciju za mobilne uređaje Microsoft Dynamics 365 Project Timesheet za Android ili iPhone iz mobilne prodavnice za vaš uređaj.

## <a name="enable-the-app"></a>Omogućavanje aplikacije 

U usluzi Finance, mora da bude omogućena aplikacija za mobilne uređaje Project Timesheet. Da biste omogućili funkcionalnost, idite na **Upravljanje projektom i računovodstveni parametri \> Vremenski raspored** i izaberite parametar **Omogući Microsoft Dynamics 365 Project Timesheet**.

### <a name="resolve-sign-in-issues"></a>Rešavanje problema sa prijavljivanjem

**Problem:** Tokom prijavljivanja u aplikaciju Project Timesheet Mobile, korisnici dobijaju poruku o grešci u kojoj se navodi da "ne mogu da pristupe aplikaciji '2bc50526-cdc3-4e36-a970-c284c34cbd6e' kod tog zakupca".

**Problem:** Tokom prijavljivanja u aplikaciju Project Timesheet Mobile, korisnici dobijaju grešku koja je slična jednom od sledećih primera:

- "AADSTS50020: Korisnički nalog '[korisničko ime]' od dobavljača identiteta 'https://sts.windows.net/[id aplikacije]' ne postoji kod zakupca '[id zakupaca]' i ne može da pristupi aplikaciji '[id aplikacije]' u tom zakupca."
- "Izabrani korisnički nalog ne postoji kod zakupca '[id zakupaca]' i ne može da pristupi aplikaciji '[id aplikacije]' u tom zakupu."

**Objašnjenje:** Ova pitanja su izazvana promenom koja je Azure Active Directory napravljena na (Azure AD) u maju 2022. Pošto ova promena nije napravljena za finansiranje i operacije aplikacija, ona može da utiče na kupce na bilo kojoj verziji platforme ili aplikacije.

**Ispravka:** Svi spoljni korisnici moraju biti pozvani kod stanara preko Azure AD. Više informacija potražite u članku [Pozivanje korisnika sa Azure Active Directory B2B saradnjom](/power-platform/admin/invite-users-azure-active-directory-b2b-collaboration).

## <a name="sign-in-to-the-app"></a>Prijavite se u aplikaciju

1.  Pokrenite aplikaciju na mobilnom uređaju.

2.  Unesite URL adresu za Finance.

3.  Kada se prvi put prijavite, od vas će se zatražiti korisničko ime i lozinka. Unesite akreditive.

4. Bićete prijavljeni u podrazumevano preduzeće.

## <a name="submit-a-project-timesheet"></a>Pošaljite vremenski raspored projekta

U aplikaciji možete da kreirate i pošaljete vremenski raspored projekta. Novi vremenski raspored možete zasnivati na informacijama iz prethodnog vremenskog rasporeda, sačuvanim linijama ili projektnim zadacima. Ako ste određeni kao delegat, možete uneti i list sa vremenom za drugog radnika. Da biste kreirali list sa vremenom kao delegat, izaberite dugme " **Meni",** a zatim izaberite ime resursa.

Stranica vremenskog rasporeda stvoriće novi vremenski raspored za period vremenskog rasporeda na osnovu trenutnog datuma. Prikazaće se radna nedelja. Ako period vremenskog rasporeda pokriva više nedelja, na karticama radne nedelje možete odabrati drugu radnu nedelju.
Ako postoji vremenski list za trenutni datum, on će biti prikazan. Ako treba da napravite novi vremenski raspored u drugom periodu vremenskog rasporeda, izaberite **Meni** a zatim izaberite **Novi vremenski raspored**.

Informacije o projektu možete uneti klikom na radnju **Dodaj vreme** ili na radnju **Kopiraj vreme iz**. Radnja **Kopiraj vreme iz** će kopirati informacije o projektnoj liniji, ali ne i sate. Meni **Kopiraj vreme iz** uključuje sledeće opcije:

- **Kopiraj iz postojećeg vremenskog rasporeda** – Kopirajte redove vremenskog rasporeda iz postojećeg vremenskog rasporeda.

- **Kopiraj iz omiljenog** – Kreirajte nove redove vremenskog rasporeda koristeći postavke vremenskog rasporeda koje ste izabrali kao omiljene.

- **Kopiraj iz zadatka** – Napravite nove redove vremenskog rasporeda iz dodeljenih projekata.

Informacije o projektu koje se prikazuju zavise od mobilnih parametara koje ste definisali na stranici **Upravljanje projektom i računovodstveni parametri**.

U polju **Pravno lice**, izaberite pravno lice za koje ste izvršili posao na projektu. Polje **Pravno lice** je dostupno samo ako je za vaše pravno lice omogućena podrška za međukompanijski vremenski raspored.

Izaberite klijenta koji je povezan sa projektom za vremenski raspored. Za početno izdanje stavke Android po klijentu nije podržano, jer prvo morate da izaberete projekat. Ako ste prvo izabrali projekat, polje **Klijent** se popunjava automatski.

U polju **Projekat** izaberite projekat za koji unosite vreme. Polje **Klijent** se popunjava automatski.

Pronalaženja klijenata i projekata omogućava pretraživanje kako klijenata, tako i projekata.

Po potrebi, izaberite informacije u poljima **Kategorija**, **Aktivnost**, **Svojstvo linije**, **Grupa poreza na promet** i **Grupa poreza na promet stavki**. Ta polja se mogu zameniti.

Polje **Svojstvo linije** će biti postavljeno na podrazumevanu vrednost, na osnovu parametara upravljanja projektom i računovodstva. Kada su parametri projekat/kategorija i kategorija/resurs omogućeni, vrednost **Svojstvo linije** će biti postavljena na podrazumevanu vrednost koju ste definisali za ovu proveru valjanosti. Kada projekat/kategorija i parametri kategorije/resursa nisu omogućeni, **vrednost svojstva "Red"** **će biti podrazumevana u skladu sa poljem Omogući podrazumevano svojstvo** reda na **stranici "Upravljanje projektima i računovodstvenim** parametrima". Vrednost **Svojstvo linije** se može izmeniti.

Izaberite dan za dodavanje vremena. Unesite broj sati tokom kojih ste radili svakog dana.

Da biste dodali komentare o časovima koje unosite, kliknite na **dugme "Dodaj** komentare", a zatim unesite komentare za internu korisnici, korisnici ili oboje.
Menadžeri projekta mogu da vide interne komentare. Komentari klijenata su uključeni u fakture.

Da biste liniju sačuvali kao omiljenu, označite polje za potvrdu, a zatim kliknite na **Sačuvaj kao omiljeno**.

Finansijska dimenzija i podrška za priloge nisu obezbeđeni u mobilnoj aplikaciji.

Nastavite da dodajete projektne linije po potrebi kako biste popunili vremenski raspored.

Kliknite na **Prosledi** da biste poslali vremenski raspored toku posla odobravanja.

## <a name="review-timesheets"></a>Pregledajte vremenske rasporede

Lista listova sa vremenom koja treba da se rediguje dostupna je u meniju. Ova opcija je dostupna samo ako ste označeni kao osoba koja vrši odobravanje toka posla. Podržani su i zaglavlje i odobrenje linije. Odobrenje nivoa linije nudi mogućnost obeležavanja jedne ili više linija za odobrenje. Nakon pregleda informacija o vremenskom rasporedu, kliknite na **Odobri**, **Delegat** ili **Povratak** da biste nastavili tok posla.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
