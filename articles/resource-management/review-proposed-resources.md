---
title: Pregled predloženih resursa
description: Ova tema pruža informacije o tome kako da predložite resurse za projekte.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 212b80a7fde8368eedd7572dd5f9278cc53fae98
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897378"
---
# <a name="review-proposed-resources"></a>Pregled predloženih resursa

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Menadžeri resursa mogu da predlože resurs menadžeru projekata korišćenjem zahteva za resurs.

1. Iz mreže zahteva ili samog zahteva izaberite **Pronađi resurse**.
2. Na stranici **Pomoćnik za zakazivanje** izaberite resurs, a zatim u oknu **Kreiranje rezervacije resursa**, u polju **Status rezervacije**, izaberite **Rezerviši**.

Dolazi do sledećih izmena statusa:

- Na stranici **Pomoćnik za zakazivanje** indikatori statusa se ažuriraju kako bi ukazali da je rezervacija predložena, a da resurs nije fiksno rezervisan.
- U zahtevu za resurs se status menja u **Zahteva pregled**.
- Na kartici **Tim** u okviru projekta, vrednost generičkog člana tima **Status zahteva** se menja u **Zahteva pregled**.

Menadžer projekta može predlog prihvatiti ili odbaciti.

Kada menadžeri resursa obrađuju zahteve za resurse, mogu koristiti bilo koji od sledećih pristupa:

- Mogu da predlažu više resursa da bi zadovoljili potražnju ako nije dostupan nijedan resurs za ispunjavanje zahtevanih sati. Predloženi sati se zatim dele na više resursa koji mogu da zadovolje zahtevane sate. U ovom scenariju, sati se ne mogu preklapati.
- Mogu da predlažu manje resursa nego što je potrebno. U ovom scenariju, kapacitet predloženog resursa je manji od zahtevanih sati koje je naveo podnosilac zahteva. Stoga, kada podnosilac zahteva prihvati predložene resurse, kreira se potreba za neispunjenim resursom da bi se evidentirala preostala potražnja.
- Mogu da rezervišu više resursa da bi zadovoljili potražnju ako nije dostupan nijedan resurs za obavljanje posla.
- Mogu da rezervišu manje resursa nego što je potrebno. U ovom scenariju, broj rezervisanih sati je manji od broja zahtevanih sati. Sistem vas upućuje da predložite resurse umesto rezervacija, tako da podnosilac zahteva može da proveri i prati preostalu potražnju.

## <a name="billable-utilization"></a>Naplativa ukupna iskorišćenost

Resursi mogu imati ciljanu naplativu ukupnu iskorišćenost. Ona je definisana kao atribut podrazumevane uloge resursa ili je podešena u zapisu pojedinačnog resursa koji se može rezervisati. Izračunavanje ukupne iskorišćenosti temelji se na stvarnim satima koje su resursi prijavili korišćenjem odobrenih stavki vremena.

Sledeće formule se koriste za izračunavanje ukupne iskorišćenosti:

- Naplativa ukupna iskorišćenost = naplativi stvarni sati ÷ kapacitet resursa
- Nenaplativa ukupna iskorišćenost = Stvarno vreme sa ID-om vrste naplate = Nenaplativo, dopunsko ili nedostupno ÷ Kapacitet resursa
- Interno = Stvarno vreme bez prodajnog ugovora ÷ Kapacitet resursa
- Kapacitet resursa = Radno vreme resursa – Van kancelarije – Neradni dani

Možete pronaći prikaz **Ukupna iskorišćenost resursa** u oknu **Resursi**.

Svaka ćelija u mreži predstavlja procenat naplative ukupne iskorišćenosti resursa u nekom periodu, kao što je dan, nedelja ili mesec. Sledeće formule se koriste za bojenje ćelija:

- **Zelena:** Naplativa ukupna iskorišćenost \>= ciljna ukupna iskorišćenost resursa
- **Žuta:** ciljna ukupna iskorišćenost – 20 \<= naplativa ukupna iskorišćenost \< ciljna ukupna iskorišćenost
- **Crvena:** naplativa ukupna iskorišćenost \< ciljna ukupna iskorišćenost – 20

Zbog toga što je prikaz **Ukupna iskorišćenost resursa** zasnovana na tabeli rasporeda, za filtriranje rezultata možete koristiti mogućnosti filtriranja tabele rasporeda.

Mreža zahteva da podesite ciljnu ukupnu iskorišćenost za ulogu ili pojedinačni resurs. Da biste to podesili, idite na stavku **Resursi** \> **Uloge resursa**.

Uz to, svakom resursu koji se može rezervisati mora se dodeliti podrazumevana uloga. Idite na **Resursi** \> **Resursi**. Na kartici **Project Service** potvrdite da je definisana uloga resursa i da je polje **Je podrazumevano** za tu ulogu podešeno na **Da**. Ako **Je podrazumevano = Ne**, možete dodati dodatne uloge. Uloga gde **Je podrazumevano = Da** koristi se za procenu ukupne iskorišćenosti resursa u odnosu na ciljnu iskorišćenost za tu ulogu.

Na kartici **Project Service** možete podesiti i pojedinačnu ciljnu ukupnu iskorišćenost za resurs. Kalkulacija ukupne iskorišćenosti zatim koristi tu ciljnu ukupnu iskorišćenost za procenu cilja resursa umesto cilja podrazumevane uloge resursa.

Ukupna iskorišćenost je prikazana za resurs samo ako je taj resurs odobrio naplativo vreme tokom perioda koji je prikazan na mreži.

## <a name="resource-availability"></a>Dostupnosti resursa

Od presudnog je značaja da menadžeri resursa mogu da pregledaju dostupnost resursa i ažuriraju rezervacije. U nekim slučajevima, ne postoji formalna potražnja (zahtev za resurs), ali menadžer resursa mora da odgovori na neplaniranu potražnju koja dolazi preko kanala poput e-pošte, telefonskog poziva ili trenutne poruke. Menadžeri resursa koriste tablu rasporeda za ažuriranje resursa i rezervacija.

Radno vreme resursa koristi se kao osnova za izračunavanje dostupnosti resursa. Rezervacije resursa troše kapacitet resursa.

Tabela rasporeda koristi boje i senčenja da bi prikazala rezervacije, dostupnost i prebukiranost, kao i status rezervacija. Postavka u podešavanjima tabele rasporeda omogućava vam da prikažete legendu.

Ako se strelica usmerena udesno pojavi pored pojedinačnog resursa koji se može rezervisati u tabeli rasporeda, resurs se može proširiti i pokazati detalje posla za koji je resurs rezervisan.

Pošto Dynamics 365 Project Operations koristi Universal Resource Scheduling mehanizam, ako ste instalirali i Dynamics 365 Field Service, možete pregledati detalje o rezervacijama resursa za projekte, radnim nalozima i bilo kojim drugim entitetima za koje ste proširili zakazivanje.

Da biste videli više detalja o pojedinačnom resursu, kliknite desnim tasterom miša na resurs da biste otvorili karticu resursa.

