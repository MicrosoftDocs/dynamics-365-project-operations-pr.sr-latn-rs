---
title: Podešavanje resursa projekta
description: Ova tema pruža informacije o podešavanju ili zahtevanju resursa projekta.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7eec8ad5d78019219b2e04ca75eeaa5a3c8a748f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083752"
---
# <a name="set-up-project-resources"></a>Podešavanje resursa projekta

[!include [banner](../includes/banner.md)]

Morate postaviti kalendar i povezati ga sa zaposlenim ili radnikom. Kalendar se koristi za planiranje projekta i radno vreme resursa koji su rezervisani za projekat. Tokom podešavanja kalendara, menadžeri projekata mogu izvršiti nivelisanje resursa kao deo optimizacije resursa. Na osnovu kalendarskog rasporeda, resursi se mogu ograničiti. Kalendar možete podesiti na stranici **Kalendari**.

Kada radnika postavite kao resurs projekta, možete da birate između radnika koji rade u kompaniji za koju postavljate resurse. Alternativno, možete da izaberete radnike iz drugih kompanija u vašoj organizaciji. Ti radnici su poznati kao međukompanijski resursi.

Sledeći postupci objašnjavaju kako da postavite radnika kao resurs projekta u vašoj kompaniji i kako da postavite međukompanijski resurs projekta.

## <a name="set-up-a-worker-as-a-project-resource"></a>Postavite radnika kao resurs projekta

1. Na stranici **Radnici** , na listi **Radnici** , izaberite radnika kojeg dodajete kao resurs projekta i otvorite zapis radnika.
2. U oknu radnji izaberite **Projekat** &gt; **Podešavanje** &gt; **Podešavanje projekta**.
3. Izaberite kalendar, a zatim zatvorite stranicu.

Takođe možete odrediti podrazumevane projekte za resurs kao vrstu prethodnog dodeljivanja. Prethodna dodeljivanja se mogu koristiti kada menadžer resursa ili menadžer projekata unapred zna na kojim projektima će resurs raditi. Prethodna dodeljivanja se takođe mogu zasnivati na zahtevu sponzora projekta ili klijenta. Da biste unapred dodelili projekat, na stranici **Dodela projekata** , na kartici **Projekti** , u listi **Preostali projekti** izaberite odgovarajući projekat.

## <a name="set-up-an-intercompany-resource"></a>Podesite međukompanijski resurs

Kada radnika postavite kao međukompanijski resurs, morate dovršiti podešavanje i u kompaniji zajmodavcu i u kompaniji zajmoprimcu.

### <a name="in-the-lending-company"></a>U kompaniji zajmodavcu

1. U usluzi Finance proverite da li je izabrana kompanija zajmodavac, a zatim dovršite postupak u prethodnom odeljku „Postavljanje radnika kao resursa projekta“.
2. Na stranici **Međukompanijsko računovodstvo** , izaberite **Novo**.
3. U polju **ID pravnog lica** izaberite kompaniju zajmodavca. Popunite preostala polja na odgovarajući način, a zatim izaberite opciju **Sačuvaj**.
4. Na stranici **Cena transfera** , izaberite **Novo**.
5. U polju **Pravno lice zajmoprimac** izaberite odgovarajuću kompaniju.
6. Da biste pozajmljivali kompaniji zajmoprimcu samo one resurse koje ste kreirali na početku ovog odeljka, u polju **Resurs** izaberite ime resursa koji ste kreirali. Da biste učinili sve resurse u kompaniji dostupnim kompaniji zajmoprimcu, ostavite polje **Resurs** prazno.
7. Na stranici **Parametri upravljanja projektom i računovodstvenom** , na kartici **Međukompanijsko** podesite opciju **Omogući međukompanijsko raspoređivanje resursa vremenske rasporede** na **Da**.

### <a name="in-the-borrowing-company"></a>U kompaniji zajmoprimcu

- Na stranici **Lista resursa** , u filter za pretragu unesite ime resursa koji ste kreirali za kompaniju zajmodavca, da biste proverili da li je ime uključeno u listu resursa za kompaniju zajmoprimca.

## <a name="request-project-resources"></a>Zahtevanje resursa projekta
Funkcionalnost za raspoređivanje resursa projekta omogućava da samo menadžeri resursa raspoređuju resurse osoblja na angažovanja ili projekte. Da biste omogućili ovu funkcionalnost, izvršite sledeće zadatke ili proverite da li su završeni:

- Podesite sekvence brojeva.
- Podesite tokove posla upravljanja projektima i računovodstvom.
- Omogućite tokove posla zahteva za resursima.

Nakon završetka prethodnih zadataka, možete izvršiti sledeće zadatke po potrebi:

- Kreirajte zahtev za resursom iz uslovno rezervisanog resursa osoblja.
- Nadgledajte zahteve za resursima.
- Ispunite zahteve za resurse.
- Zatražite resurse osoblja iz SAP.
- Rezervišite resurse za projekat bez zahteva za resursima osoblja.
