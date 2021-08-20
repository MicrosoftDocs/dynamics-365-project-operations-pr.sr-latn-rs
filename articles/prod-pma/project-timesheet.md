---
title: Aplikacija za mobilne uređaje Project Timesheet
description: Ova tema pruža informacije o aplikaciji za mobilne uređaje Microsoft Dynamics 365 Project Timesheet. Aplikacija za mobilne uređaje Project Timesheet omogućava korisnicima da predaju i odobre radne listove za projekte na svom mobilnom uređaju.
author: abruer
ms.date: 04/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: df6d286b6d5716fb0ea908ed71c2257b4db21ecfd35148fea65dfd96e058ac9a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997218"
---
# <a name="project-timesheet-mobile-application"></a>Aplikacija za mobilne uređaje Project Timesheet

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Pregled

Aplikacija za mobilne uređaje Microsoft Dynamics 365 Project Timesheet omogućava korisnicima da predaju i odobre radne listove za projekte na svom mobilnom uređaju (iPhone ili Android). Ova aplikacija za mobilne uređaje prikazuje funkcionalnost vremenskog rasporeda koja se nalazi u području upravljanja projektima i računovodstva usluge Dynamics 365 Finance, poboljšavajući produktivnost i efikasnost korisnika, kao i omogućavanje pravovremenog unosa i odobravanja vremenskih rasporeda projekata.

## <a name="download-and-install-the-mobile-app"></a>Preuzmite i instalirajte aplikaciju za mobilne uređaje

Preuzmite i instalirajte aplikaciju za mobilne uređaje Microsoft Dynamics 365 Project Timesheet za Android ili iPhone iz mobilne prodavnice za vaš uređaj.

## <a name="enable-the-app"></a>Omogućavanje aplikacije 

U usluzi Finance, mora da bude omogućena aplikacija za mobilne uređaje Project Timesheet. Da biste omogućili funkcionalnost, idite na **Upravljanje projektom i računovodstveni parametri \> Vremenski raspored** i izaberite parametar **Omogući Microsoft Dynamics 365 Project Timesheet**.

## <a name="sign-in-to-the-app"></a>Prijavite se u aplikaciju

1.  Pokrenite aplikaciju na mobilnom uređaju.

2.  Unesite URL adresu za Finance.

3.  Kada se prvi put prijavite, od vas će se zatražiti korisničko ime i lozinka. Unesite akreditive.

4.  Bićete prijavljeni u svoju podrazumevanu kompaniju.

## <a name="submit-a-project-timesheet"></a>Pošaljite vremenski raspored projekta

U aplikaciji možete da kreirate i pošaljete vremenski raspored projekta. Novi vremenski raspored možete zasnivati na informacijama iz prethodnog vremenskog rasporeda, sačuvanim linijama ili projektnim zadacima. Ako ste određeni za delegata, možete da unesete i vremenski raspored za drugog radnika. Da biste kreirali vremenski raspored kao delegat, izaberite **Meni**, a zatim izaberite naziv resursa.

Stranica vremenskog rasporeda stvoriće novi vremenski raspored za period vremenskog rasporeda na osnovu trenutnog datuma. Prikazaće se radna nedelja. Ako period vremenskog rasporeda pokriva više nedelja, na karticama radne nedelje možete odabrati drugu radnu nedelju.
Ako postoji vremenski list za trenutni datum, on će biti prikazan. Ako treba da napravite novi vremenski raspored u drugom periodu vremenskog rasporeda, izaberite **Meni** a zatim izaberite **Novi vremenski raspored**.

Informacije o projektu možete uneti klikom na radnju **Dodaj vreme** ili na radnju **Kopiraj vreme iz**. Radnja **Kopiraj vreme iz** će kopirati informacije o projektnoj liniji, ali ne i sate. Meni **Kopiraj vreme iz** uključuje sledeće opcije:

- **Kopiraj iz postojećeg vremenskog rasporeda** – Kopirajte redove vremenskog rasporeda iz postojećeg vremenskog rasporeda.

- **Kopiraj iz omiljenog** – Kreirajte nove redove vremenskog rasporeda koristeći postavke vremenskog rasporeda koje ste izabrali kao omiljene.

- **Kopiraj iz zadatka** – Napravite nove redove vremenskog rasporeda iz dodeljenih projekata.

Informacije o projektu koje se prikazuju zavise od mobilnih parametara koje ste definisali na stranici **Upravljanje projektom i računovodstveni parametri**.

U polju **Pravno lice**, izaberite pravno lice za koje ste izvršili posao na projektu. Polje **Pravno lice** je dostupno samo ako je za vaše pravno lice omogućena podrška za međukompanijski vremenski raspored.

Izaberite klijenta koji je povezan sa projektom za vremenski raspored. Za početno izdanje na platformi Android, stavka klijenta nije podržana, jer prvo morate da izaberete projekat. Ako ste prvo izabrali projekat, polje **Klijent** se popunjava automatski.

U polju **Projekat**, izaberite projekat za koji unosite vreme. Polje **Klijent** se popunjava automatski.

Pronalaženja klijenata i projekata omogućava pretraživanje kako klijenata, tako i projekata.

Po potrebi, izaberite informacije u poljima **Kategorija**, **Aktivnost**, **Svojstvo linije**, **Grupa poreza na promet** i **Grupa poreza na promet stavki**. Ta polja se mogu zameniti.

Polje **Svojstvo linije** će biti postavljeno na podrazumevanu vrednost, na osnovu parametara upravljanja projektom i računovodstva. Kada su parametri projekat/kategorija i kategorija/resurs omogućeni, vrednost **Svojstvo linije** će biti postavljena na podrazumevanu vrednost koju ste definisali za ovu proveru valjanosti. Kada parametri projekat/kategorija i kategorija/resurs nisu omogućeni, vrednost **Svojstvo linije** će biti podrazumevana prema polju **Omogući podrazumevano svojstvo linije** na stranici **Upravljanje projektom i računovodstveni parametri**. Vrednost **Svojstvo linije** se može izmeniti.

Izaberite dan za dodavanje vremena. Unesite broj sati tokom kojih ste radili svakog dana.

Da biste dodali komentare o satima koje unosite, kliknite na **Dodaj komentare**, a zatim unesite komentare za interne korisnike, korisnike klijenta ili obe grupe.
Menadžeri projekta mogu da vide interne komentare. Komentari klijenata su uključeni u fakture.

Da biste liniju sačuvali kao omiljenu, označite polje za potvrdu, a zatim kliknite na **Sačuvaj kao omiljeno**.

Finansijska dimenzija i podrška za priloge nisu predviđeni u aplikaciji za mobilne uređaje.

Nastavite da dodajete projektne linije po potrebi kako biste popunili vremenski raspored.

Kliknite na **Prosledi** da biste poslali vremenski raspored toku posla odobravanja.

## <a name="review-timesheets"></a>Pregledajte vremenske rasporede

Lista vremenskih rasporeda koje treba pregledati dostupna je u meniju. Ova opcija je dostupna samo ako ste izabrani za davaoca odobrenja toka posla. Podržani su i zaglavlje i odobrenje linije. Odobrenje nivoa linije nudi mogućnost obeležavanja jedne ili više linija za odobrenje. Nakon pregleda informacija o vremenskom rasporedu, kliknite na **Odobri**, **Delegat** ili **Povratak** da biste nastavili tok posla.


[!INCLUDE[footer-include](../includes/footer-banner.md)]