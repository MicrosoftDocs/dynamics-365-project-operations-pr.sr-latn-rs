---
title: Pregled sravnjenja resursa
description: Ova tema pruža informacije o tome da li su poravnate rezervacije resursa i dodeljivanja zadacima u projektu.
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
ms.openlocfilehash: 1b60ed9d15f51ff01f27bcc231f5db27513a838f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897468"
---
# <a name="resource-reconciliation-overview"></a>Pregled sravnjenja resursa

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Za članove tima, rezervacije i dodele su labavo povezane. Drugim rečima, resursi mogu imati dodele, ali ne i rezervacije ili mogu imati rezervacije, ali ne i dodele. U idealnom slučaju, rezervacije i dodele treba da se usklade tako da resursi imaju potreban kapacitet da izvrše dodeljene zadatke. Međutim, rezervacije se mogu zasnivati na dostupnosti, a vremenski raspored zadataka može se menjati tokom projekta. Stoga, labava povezanost rezervacija i dodela pruža fleksibilnost.

Kartica **Usaglašenost** na obrascu **Projekat** omogućava menadžerima projekata da usaglase rezervacije članova tima i njihove dodele za projektne timove.

Kartica **Usaglašenost** takođe prikazuje rezervacije i dodele sve do nivoa dodele pojedinačnog zadatka za svakog člana tima. Sati se prikazuju u ćelijama koji predstavljaju vremenske periode, od meseci, pa sve do dana.

Kartica takođe prikazuje ukupni neto iznos projekta, zajedno sa kolonom **Ukupna vrednost**.

Kartica za svaki resurs izračunava razliku između rezervacija člana tima i ukupnog broja dodeljenih zadataka člana tima. U idealnom slučaju, ta razlika bi trebalo da bude 0 (nula). Drugim rečima, ne bi trebalo da postoji razlika između rezervacija i dodela. Razlike su obojene i zasenčene kako bi se skrenula pažnja na dve pojave:

- **Nedostatak rezervacija** - Nedostatak rezervacija nastaje kada resurs ima više dodela nego rezervacija. Budući da ovaj kapacitet nije rezervisan, menadžer projekta može da koriguje tu pojavu proširivanjem rezervacija resursa kako bi pokrio deficit.
- **Prekomerne rezervacije** – Prekomerna rezervacija nastaje kada je resurs rezervisan za projekat, ali nije dodeljen zadacima. Ta pojava može biti prihvatljiva u slučajevima kada je resurs rezervisan za projekat pre dodele zadatka. Međutim, u drugim slučajevima se ne planira dodeljivanje resursa zadacima. U tim slučajevima, menadžer projekta treba da razmotriti otkazivanje rezervacija resursa, tako da se kapacitet može koristiti za drugi projekat.

U nekim slučajevima, kada pregledate vreme na višem nivou od nivoa dana (na primer, na mesečnom nivou), možda ćete videti ukupnu razliku koja je nula za neki resurs (drugim rečima, rezervacije = dodele). Međutim, ako pregledate vreme na nivou nedelje, možda ćete videti da postoje dodele od nula sati i rezervacije od 40 sati u prvoj nedelji, ali dodele od 40 sati i rezervacije od nula sati u drugoj nedelji. Sve u svemu, rezervacije i dodele se usklađuju, ali se razlikuju od jedne do druge nedelje.

Kada pregledate vreme na višim nivoima, ćelije na kartici **Usaglašenost** imaju indikator koji će vas obavestiti da postoje razlike na nižim nivoima. Duplim klikom na ćeliju možete da je povećate kako biste videli razliku. Zatim možete da kliknite desnim tasterom miša da biste je umanjili. Ako odaberete resurs, a zatim koristite kontrolu **Sledeća razlika** na traci sa alatkama mreže, možete preći na sledeću razliku između rezervacija i dodela za taj resurs. Zatim možete da koristite kontrolu **Prethodna razlika** za povratak. Takođe možete isključiti indikator razlike i ponašanje u navigaciji u delu **Podešavanja**.


Ako imate dodele zadataka za resurs, ali nema rezervacija, na stranici **Projekti** na kartici **Usaglašenost** izaberite nedostatak rezervacija, a zatim **Produži rezervaciju**. Pojavljuje se dijalog **Produženje rezervacije** i prikazuje rezervaciju koja je potrebna da se reši problem sa nedostatkom resursa. Takođe pokazuje postojeće rezervacije resursa za sve projekte ili druge entitete koji se mogu zakazivati. Ako izaberete **U redu** da biste kreirali rezervaciju za resurs, bez obzira na dostupnost tog resursa, možete prouzrokovati prekomernu rezervaciju.

Menadžer projekta ili menadžer resursa tada može da koristi tabelu rasporeda kako bi upravljao bilo kojom situacijom u kojoj je resurs prekomerno rezervisan u odnosu na njegov kapacitet.

