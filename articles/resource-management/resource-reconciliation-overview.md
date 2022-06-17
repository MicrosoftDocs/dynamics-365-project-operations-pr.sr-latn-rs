---
title: Pregled sravnjenja resursa
description: Ovaj članak pruža informacije koje će vam pomoći da obezbedite usklađivanje rezervacija resursa i dodela za projekte.
author: ruhercul
ms.date: 01/08/2021
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: eaad9187f08be810d730f5a8ca6411ecee85bbc4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926333"
---
# <a name="resource-reconciliation-overview"></a>Pregled sravnjenja resursa

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Za članove tima, rezervacije i dodele su labavo povezane. Drugim rečima, resursi mogu imati dodele bez rezervacija ili mogu imati rezervacije bez dodela. U idealnom slučaju, rezervacije i dodele treba da se usklade tako da resursi imaju potreban kapacitet da izvrše dodeljene zadatke. Međutim, rezervacije se mogu zasnivati na dostupnosti, a vremenski raspored zadataka može se menjati tokom projekta. Stoga, labava povezanost rezervacija i dodela pruža fleksibilnost.

Kartica **Usaglašenost** na stranici **Projekti** omogućava menadžerima projekata da usaglase rezervacije članova tima i njihove dodele za projektne timove.

Kartica **Usaglašenost** prikazuje rezervacije i dodele sve do nivoa dodele pojedinačnog zadatka za svakog člana tima. Sati sa prikazuju u ćelijama koje predstavljaju vremenske periode, od meseci, pa sve do dana. Kartica takođe prikazuje ukupni neto iznos projekta, zajedno sa kolonom **Ukupna vrednost**.

Kartica **Usaglašenost** za svaki resurs izračunava razliku između rezervacija člana tima i ukupnog broja dodeljenih zadataka tog člana tima. U idealnom slučaju, ta razlika bi trebalo da bude 0 (nula). Drugim rečima, ne bi trebalo da postoji razlika između rezervacija i dodela. Razlike su obojene i zasenčene kako bi se skrenula pažnja na dve pojave:

- **Nedostatak rezervacija** - Nedostatak rezervacija nastaje kada resurs ima više dodela nego rezervacija. Budući da kapacitet nije rezervisan, menadžer projekta može da koriguje tu pojavu proširivanjem rezervacija resursa kako bi pokrio deficit.
- **Prekomerne rezervacije** – Prekomerna rezervacija nastaje kada je resurs rezervisan za projekat, ali nije dodeljen zadacima. Ta pojava može biti prihvatljiva u slučajevima kada je resurs rezervisan za projekat pre dodele zadatka. Međutim, u drugim slučajevima, kada ne postoji plan za dodeljivanje resursa zadacima, menadžer projekta bi trebalo da razmotri otkazivanje rezervacija resursa. Na taj način se kapacitet može iskoristiti za drugi projekat.

U nekim slučajevima, kada pregledate vreme na višem nivou od nivoa dana (na primer, na mesečnom nivou), možda ćete videti ukupnu razliku koja je nula za neki resurs (drugim rečima, rezervacije su jednake dodelama). Međutim, ako pregledate vreme na nivou nedelje, možda ćete videti da postoje dodele od nula sati i rezervacije od 40 sati u prvoj nedelji, ali dodele od 40 sati i rezervacije od nula sati u drugoj nedelji. Sve u svemu, rezervacije i dodele se usklađuju, ali se razlikuju od jedne do druge nedelje.

Kada pregledate vreme na višim nivoima, ćelije na kartici **Usaglašenost** imaju indikator koji će vas obavestiti da postoje razlike na nižim nivoima. Duplim dodirom ili klikom na ćeliju možete da je povećate kako biste videli razliku. Zatim možete da je izaberete i zadržite (kliknite desnim tasterom miša) da biste je umanjili. Ako odaberete resurs, a zatim koristite kontrolu **Sledeća razlika** na traci sa alatkama mreže, možete preći na sledeću razliku između rezervacija i dodela za taj resurs. Zatim možete da koristite kontrolu **Prethodna razlika** za povratak. Takođe možete isključiti indikator razlike i ponašanje u navigaciji u delu **Podešavanja**.

Ako imate dodele zadataka za resurs, ali nema rezervacija, izaberite nedostatak rezervacija na kartici **Usaglašenost** na stranici **Projekti**, a zatim **Produži rezervaciju**. Dijalog **Produženje rezervacije** koji se pojavljuje prikazuje rezervaciju koja je potrebna da se reši problem sa nedostatkom resursa. Dijalog takođe pokazuje postojeće rezervacije resursa za sve projekte ili druge entitete koji se mogu zakazivati. Ako izaberete **U redu** da biste kreirali rezervaciju za resurs, bez obzira na dostupnost tog resursa, možete prouzrokovati prekomernu rezervaciju.

Rezervacije kreirane putem radnje **Proširi rezervaciju** su povezane sa primarnim projektnim zahtevom. Kada se pokreće proširenje, ne može se utvrditi konkretan zahtev koji se mora proširiti jer resurs može biti povezan sa više zahteva za projekat.

Menadžer projekta ili menadžer resursa tada može da koristi tabelu rasporeda kako bi upravljao bilo kojom situacijom u kojoj je resurs prekomerno rezervisan u odnosu na njegov kapacitet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]