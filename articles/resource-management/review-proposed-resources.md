---
title: Pregled predloženih resursa
description: Ovaj članak pruža informacije o tome kako da predložite projektne resurse.
author: ruhercul
ms.date: 08/18/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3f20dda2b7b384608b8f4b548c18ac21d07fee07
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924861"
---
# <a name="review-proposed-resources"></a>Pregled predloženih resursa

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Menadžeri resursa mogu da predlože resurs menadžeru projekata korišćenjem zahteva za resurs.

Da biste pregledali predložene resurse, sledite ove korake:

1. Iz mreže **Zahtev** ili samog zahteva izaberite **Pronađi resurse**.
2. Na stranici **Pomoćnik za raspored** izaberite resurs, a zatim potvrdite da su svi predloženi sati uključeni u predloženu rezervaciju.
3. U oknu **Kreirajte rezervaciju resursa** podesite polje **Status rezervacije** na **Predloženo**, a zatim izaberite **Rezerviši**.

    > [!NOTE]
    > Ako se **Status rezervacije** postavi na **Predložen**, resurs se ne rezerviše fiksno i ne zamenjuje se generički resurs imenovanim članom tima.

    Dolazi do sledećih izmena statusa:

    - Na stranici **Pomoćnik za zakazivanje** indikatori statusa se ažuriraju kako bi ukazali da je rezervacija predložena, a da resurs nije fiksno rezervisan.
    - U zahtevu za resurs se status menja u **Zahteva pregled**.
    - Na kartici **Tim** u okviru projekta, vrednost generičkog člana tima **Status zahteva** se menja u **Zahteva pregled**.

Menadžer projekta može predlog prihvatiti ili odbaciti.

Kada menadžeri resursa obrađuju zahteve za resurse, mogu koristiti bilo koji od sledećih pristupa:

- Mogu da predlažu više resursa da bi zadovoljili potražnju ako nije dostupan nijedan resurs za ispunjavanje zahtevanih sati. Predloženi sati se zatim dele na više resursa koji mogu da zadovolje zahtevane sate. U ovom scenariju, sati se ne mogu preklapati.
- Mogu da predlažu manje resursa nego što je potrebno. U ovom scenariju, kapacitet predloženog resursa je manji od zahtevanih sati koje je naveo podnosilac zahteva. Kada podnosilac zahteva prihvati predložene resurse, kreira se potreba za neispunjenim resursom da bi se evidentirala preostala potražnja.
- Mogu da rezervišu više resursa da bi zadovoljili potražnju ako nije dostupan nijedan resurs za obavljanje posla.
- Mogu da rezervišu manje resursa nego što je potrebno. U ovom scenariju, broj rezervisanih sati je manji od broja zahtevanih sati. Sistem vas upućuje da predložite resurse umesto rezervacija, tako da podnosilac zahteva može da proveri i prati preostalu potražnju.

## <a name="resource-availability"></a>Dostupnosti resursa

Menadžeri resursa moraju da imaju mogućnost da pregledaju dostupnost resursa i ažuriraju rezervacije. U nekim slučajevima ne postoji formalna potražnja (zahtev za resursima). Međutim, menadžer resursa mora odgovoriti na neplanirani zahtev koji dolazi putem drugih kanala, poput e -pošte, telefonskih poziva ili trenutnih poruka. Menadžeri resursa koriste **tablu rasporeda** za ažuriranje resursa i rezervacija.

Radno vreme resursa koristi se kao osnova za izračunavanje dostupnosti resursa. Rezervacije resursa troše kapacitet resursa.

**Tabela rasporeda** koristi boje i senčenja da bi prikazala rezervacije, dostupnost, prebukiranost i status rezervacija. Podešavanje **Tabela rasporeda** omogućava vam da prikažete legendu.

Ako se strelica usmerena udesno pojavi pored pojedinačnog resursa koji se može rezervisati u **tabeli rasporeda**, resurs se može proširiti i pokazati detalje posla za koji je resurs rezervisan.

Pošto Dynamics 365 Project Operations koristi Universal Resource Scheduling mehanizam, ako ste instalirali i Dynamics 365 Field Service, možete pregledati detalje o rezervacijama resursa za projekte, radnim nalozima i bilo kojim drugim entitetima za koje ste proširili zakazivanje.

Da biste videli dodatne detalje o pojedinačnom resoru, kliknite desnim tasterom miša na resurs da biste otvorili karticu resursa.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
