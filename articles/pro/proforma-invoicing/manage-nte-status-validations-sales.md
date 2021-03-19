---
title: Upravljanje statusom i potvrdama koje ne smete premašiti
description: Ova tema pruža informacije o ograničenjima koja se ne prekoračuju u usluzi Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c5c491d4014ffc2568d7df72b542761ec9b1a90b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274049"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Upravljanje statusom i potvrdama koje ne smete premašiti 

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

## <a name="not-to-exceed-on-approvals"></a>Odobrenja koja se ne smeju premašiti

Kada se podnese stavka vremena ili troška, kreira se zapis o odobrenju. Ako je odobrenje naplativo i mapira se na predmet ugovora za vreme i materijal, sistem izvršava proveru stavki koje ne smeju premašiti na sledećim nivoima:

  - Provera da li je postavljeno ograničenje za klijenta na predmetu ugovora za projekat
  - Provera da li je postavljeno ograničenje za predmet ugovora
  - Provera da li je postavljeno ograničenje za klijenta
  - Provera da li je postavljeno ograničenje za ugovor

Provere na svakom nivou uključuju osiguravanje da iznos prodajne vrednosti na ovom odobrenju neće prekršiti ograničenje premašivanja na tom nivou nakon obračunavanja iznosa zaostalih računa koji je već evidentiran, kao ni iznos koji je do danas fakturisan na tom nivou.

Ako provera prođe, odobrenje dobija status potvrde **Uspeh**.

Ako provera ne uspe, odobrenje dobija status potvrde **Neuspešno**. Detalji provere valjanosti neprekoračenja obavestiće korisnika na kom nivou provera valjanosti nije uspela.

Kada se podneti unos vremena ili troškova smatra nenaplativim, status provere valjanosti neprekoračenja se postavlja na **Nije primenljivo** sa detaljima provere valjanosti jednakim **Nije primenljivo**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Neprekoračenje stvarnih vrednosti nenaplaćene prodaje

Kada se odobri stavka vremena ili troška, kreiraju se zapisi o stvarnim vrednostima troškovima i nenaplaćene prodaje. Ako je stvarna vrednost nenaplaćene prodaje koja se kreira naplativa i mapira se na predmet ugovora za vreme i materijal, aplikacija obavlja proveru stavki koje ne smeju premašiti na sledećim nivoima:

  - Provera da li je postavljeno ograničenje za klijenta na predmetu ugovora za projekat
  - Provera da li je postavljeno ograničenje za predmet ugovora
  - Provera da li je postavljeno ograničenje za klijenta
  - Provera da li je postavljeno ograničenje za ugovor

Provere na svakom nivou obezbeđuju da iznos vrednosti prodaje na ovoj stvarnoj vrednosti neće prekršiti ograničenje premašivanja na tom nivou nakon obračunavanja iznosa zaostalih naplata koji je već evidentiran, kao ni iznos koji je do danas fakturisan na tom nivou.

Ako provera prođe, stvarna vrednost nenaplaćene prodaje dobija status koji ne sme premašiti **Dodeljeno**.

Ako provera ne uspe, stvarna vrednost nenaplaćene prodaje dobija status koji ne sme premašiti **Neuspešno**. Detalji provere valjanosti obaveštavaju korisnika na kom nivou provera valjanosti nije uspela.

Kada se nenaplaćena prodaja smatra nenaplativom ili besplatnom, ako na bilo kojem od četiri nivoa ne postoji ograničenje premašivanja ili ako je stvarna vrednost koja se kreira trošak, avans, jedinica za resurse ili prodaja između organizacija, polja **Status neprekoračenja** i **Detalj provere valjanosti neprekoračenja** moraju biti podešena na **Nije primenljivo**.

## <a name="reset-the-not-to-exceed-status"></a>Resetovanje statusa neprekoračenja

Možete izvršiti grupno resetovanje statusa neprekoračenja. Ovo omogućava menadžerima projekata da prilagode proveru valjanosti neprekoračenja da bi dali prednost fakturisanju jednog određenog dela posla, vremena ili troškova u odnosu na druge koji su već preuzeti iz raspoloživog iznosa koji ne sme da premaši.

Nakon resetovanja statusa neprekoračenja na stvarnim vrednostima nenaplaćene prodaje, dodeljeni iznos se smanjuje. Menadžer projekta može da izabere drugo delo, vreme ili troškove koji prethodno nisu prošli proveru valjanosti neprekoračenja i da ih ponovo proceni. Sa smanjenjem angažovanog iznosa, ove stvarne vrednosti će sada će proći proveru valjanosti. To pomaže menadžeru projekta da izvrši veći uticaj i kontrolu nad transakcijama za taj period koje mogu da se fakturišu.

Da biste resetovali status neprekoračenja, izaberite jednu ili više stvarnih vrednosti iz prikaza **Neizvršavanje naplate vremena i materijala** ili **Stvarne vrednosti**, a zatim izaberite **Resetovanje statusa neprekoračenja**.

Status neprekoračenja se resetuje na **Nije procenjeno** na svim relevantnim izabranim stvarnim vrednostima. Stvarne vrednosti čiji se status neprekoračenja resetuje su stvarne vrednosti nenaplaćene prodaje, nisu u radnoj verziji fakture i označene su kao naplative. Sve ostale izabrane stvarne vrednosti se ignorišu.

## <a name="reevaluate-not-to-exceed-status"></a>Ponovna procena statusa neprekoračenja

Možete izvršiti grupnu ponovnu procenu statusa neprekoračenja. Ponovna procena statusa neprekoračenja je korisna u sledećim slučajevima:

  - Došlo je do ponovnog pregovaranja sa klijentom o ograničenjima koja se ne smeju premašiti i potrebno je ponoviti procenu stvarnih vrednosti.
  - Menadžer projekta želi da fino podesi fakturisanje neisplaćenih zaostalih prodaja davanjem prioriteta jednom delu posla u odnosu na drugi.

Da biste ponovo procenili status neprekoračenja, izaberite jednu ili više stvarnih vrednosti iz prikaza **Neizvršavanje naplate vremena i materijala** ili **Stvarne vrednosti**, a zatim izaberite **Ponovna procena statusa neprekoračenja**.

Sve relevantne izabrane stvarne vrednosti sa ograničenjem neprekoračenja biće procenjene u odnosu na podešavanje ograničavanja neprekoračenja. Stvarne vrednosti koje su relevantne za ponovnu procenu statusa neprekoračenja su stvarne vrednosti nenaplaćene prodaje koje nisu fakturisane, nisu u radnoj verziji fakture i označene su kao naplative. Sve ostale izabrane stvarne vrednosti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]