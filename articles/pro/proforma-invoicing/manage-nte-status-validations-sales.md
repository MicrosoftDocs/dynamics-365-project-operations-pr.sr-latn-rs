---
title: Upravljanje statusom i potvrdama koje ne smete premašiti
description: Ovaj članak pruža informacije o ograničenjima koja se ne prekoračuju u usluzi Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d10a88305339a84b36d8606631ea9761806098a1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932773"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Upravljanje statusom i potvrdama koje ne smete premašiti 

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

## <a name="not-to-exceed-on-approvals"></a>Odobrenja koja se ne smeju premašiti

Kada se prosledi stavka vremena, troškova ili upotrebe materijala, kreira se zapis odobrenja. Ako je odobrenje naplativo i mapira se na predmet ugovora za vreme i materijal, sistem izvršava proveru stavki koje ne smeju premašiti na sledećim nivoima:

  - Provera da li je postavljeno ograničenje za klijenta na predmetu ugovora za projekat
  - Provera da li je postavljeno ograničenje za predmet ugovora
  - Provera da li je postavljeno ograničenje za klijenta
  - Provera da li je postavljeno ograničenje za ugovor

Provere na svakom nivou uključuju osiguravanje da iznos prodajne vrednosti na ovom odobrenju neće prekršiti ograničenje premašivanja na tom nivou nakon obračunavanja iznosa zaostalih računa koji je već evidentiran, kao ni iznos koji je do danas fakturisan na tom nivou.

Ako provera prođe, odobrenje dobija status potvrde **Uspeh**.

Ako provera ne uspe, odobrenje dobija status potvrde **Neuspešno**. Detalji provere valjanosti neprekoračenja obavestiće korisnika na kom nivou provera valjanosti nije uspela.

Kada se prosleđena stavka vremena, troškova ili upotrebe materijala smatra nenaplativom, status potvrde koji se ne sme premašiti postavlja se na **Nije primenljivo** sa detaljima validacije jednakim sa **Nije primenljivo**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Neprekoračenje stvarnih vrednosti nenaplaćene prodaje

Kada se odobri unos vremena, troškova ili upotrebe materijala, kreiraju se zapisi stvarnih troškova i nefakturisane prodaje. Ako je stvarna vrednost nenaplaćene prodaje koja se kreira naplativa i mapira se na predmet ugovora za vreme i materijal, aplikacija obavlja proveru stavki koje ne smeju premašiti na sledećim nivoima:

  - Provera da li je postavljeno ograničenje za klijenta na predmetu ugovora za projekat
  - Provera da li je postavljeno ograničenje za predmet ugovora
  - Provera da li je postavljeno ograničenje za klijenta
  - Provera da li je postavljeno ograničenje za ugovor

Provere na svakom nivou obezbeđuju da iznos vrednosti prodaje na ovoj stvarnoj vrednosti neće prekršiti ograničenje premašivanja na tom nivou nakon obračunavanja iznosa zaostalih naplata koji je već evidentiran, kao ni iznos koji je do danas fakturisan na tom nivou.

Ako provera prođe, stvarna vrednost nenaplaćene prodaje dobija status koji ne sme premašiti **Dodeljeno**.

Ako provera ne uspe, stvarna vrednost nenaplaćene prodaje dobija status koji ne sme premašiti **Neuspešno**. Detalji provere valjanosti obaveštavaju korisnika na kom nivou provera valjanosti nije uspela.

Kada se nenaplaćena prodaja smatra nenaplativom ili besplatnom, ako na bilo kojem od četiri nivoa ne postoji ograničenje premašivanja ili ako je stvarna vrednost koja se kreira trošak, avans, jedinica za resurse ili prodaja između organizacija, polja **Status neprekoračenja** i **Detalj provere valjanosti neprekoračenja** moraju biti podešena na **Nije primenljivo**.

## <a name="reset-the-not-to-exceed-status"></a>Resetovanje statusa neprekoračenja

Možete izvršiti grupno resetovanje statusa neprekoračenja. Menadžeri projekata mogu da prilagode validaciju koja ne sme da se premaši da bi dali prednost fakturisanju jednog određenog dela posla, vremena, troškova ili upotrebe materijala nad drugima koji su već preuzeti iz raspoloživog iznosa koji ne sme da se premaši.

Nakon resetovanja statusa neprekoračenja na stvarnim vrednostima nenaplaćene prodaje, dodeljeni iznos se smanjuje. Menadžer projekta može da izabere drugi deo posla, vremena, troškova ili unosa upotrebe materijala koji prethodno nije uspeo da izvrši validaciju i ponovo proceni. Sa smanjenjem dodeljenog iznosa, ovi stvarni podaci sada prolaze validaciju što pomaže menadžeru projekta da izvrši veći uticaj i kontrolu nad transakcijama koje mogu da se fakturišu za taj period.

Da biste resetovali status neprekoračenja, izaberite jednu ili više stvarnih vrednosti iz prikaza **Neizvršavanje naplate vremena i materijala** ili **Stvarne vrednosti**, a zatim izaberite **Resetovanje statusa neprekoračenja**.

Status neprekoračenja se resetuje na **Nije procenjeno** na svim relevantnim izabranim stvarnim vrednostima. Stvarne vrednosti čiji se status neprekoračenja resetuje su stvarne vrednosti nenaplaćene prodaje, nisu u radnoj verziji fakture i označene su kao naplative. Sve ostale izabrane stvarne vrednosti se ignorišu.

## <a name="reevaluate-not-to-exceed-status"></a>Ponovna procena statusa neprekoračenja

Možete izvršiti grupnu ponovnu procenu statusa neprekoračenja. Ponovna procena statusa neprekoračenja je korisna u sledećim slučajevima:

  - Došlo je do ponovnog pregovaranja sa klijentom o ograničenjima koja se ne smeju premašiti i potrebno je ponoviti procenu stvarnih vrednosti.
  - Menadžer projekta želi da fino podesi fakturisanje neisplaćenih zaostalih prodaja davanjem prioriteta jednom delu posla u odnosu na drugi.

Da biste ponovo procenili status neprekoračenja, izaberite jednu ili više stvarnih vrednosti iz prikaza **Neizvršavanje naplate vremena i materijala** ili **Stvarne vrednosti**, a zatim izaberite **Ponovna procena statusa neprekoračenja**.

Sve relevantne izabrane stvarne vrednosti sa ograničenjem neprekoračenja biće procenjene u odnosu na podešavanje ograničavanja neprekoračenja. Stvarne vrednosti koje su relevantne za ponovnu procenu statusa neprekoračenja su stvarne vrednosti nenaplaćene prodaje koje nisu fakturisane, nisu u radnoj verziji fakture i označene su kao naplative. Sve ostale izabrane stvarne vrednosti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
