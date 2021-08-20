---
title: Šta je novo u maju 2021. – jednostavna primena usluge Project Operations
description: Ova tema pruža informacije o ispravkama kvaliteta dostupnim u jednostavnoj primeni izdanja Project Operations za maj 2021. godine.
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 14ff7f1f7374ffe885c511fd693cda5b7023c5beb53adb45042ddda1e932c93d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005993"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a>Šta je novo u maju 2021. – jednostavna primena usluge Project Operations

_Odnosi se na: Jednostavna primena – od pogodbe do profakture_

Ova tema se odnosi na sledeće komponente i verzije usluge Dynamics 365 Project Operations:

   - Project Operations u Dataverse okruženju verzije 4.10.0.186.

## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

Sledeće funkcije su uključene u ovom izdanju:

- [Režimi zakazivanja](../../project-management/scheduling-modes.md): Menadžeri projekata sada mogu da definišu da li projektom treba upravljati korišćenjem režima zakazivanja fiksnog trajanja, fiksnog rada ili fiksnih jedinica.

## <a name="quality-updates"></a>Ispravke kvaliteta

| **Oblast funkcija** | **Referentni broj** | **Ispravka kvaliteta** |
| --- | --- | --- |
| Naplata i određivanje cena | 2224568 | Dodata je logika za omogućavanje prilagođavanja koja uključuju pozivanje dodatne komponente za potvrdu fakture. |
| Naplata i određivanje cena | 2101098 | Poboljšana logika podrazumevanih polja za predračun. U ova polja spadaju **Adresa fakturisanja**, **Ime fakturisanja** i **Uslovi plaćanja**. Polja su sada podrazumevana iz odgovarajućeg zapisa klijenta ugovora o projektu. |
| Naplata i određivanje cena | 2021413 | Ažurirana su polja **Stvarna cena** i **Prodaja** na entitetu **Zadatak** da uključi vrednosti prodaje iz nenaplaćenih i naplaćenih troškova na zadacima. |
| Naplata i određivanje cena | 2182110 | Prilikom kopiranja ugovora o projektu, ID predmeta ugovora se ponovo generiše u ugovoru o odredišnom projektu kako bi se osiguralo da je jedinstven. |
| Upravljanje mogućnostima za poslovanje | 2186741 | Dodate su validacije kako bi se osiguralo da polje **Poreklo** i tip transakcije ne mogu da se ažuriraju na postojećim detaljima stavke ponude. |
| Upravljanje mogućnostima za poslovanje | 2191353 | Kreiranje kontrolnih tačaka se ne sme omogućiti na predmetu ugovora za vreme i materijal. |
| Upravljanje mogućnostima za poslovanje | 2216956 | Rešeni su problemi sa **ažuriranjem cena**. |
| Planiranje i praćenje | 2182979 | Poboljšana je funkcija kopiranja projekta kako bi se osiguralo kopiranje stavki procene troškova iz originalnog projekta. |
| Planiranje i praćenje | 2184144 | Poboljšana je funkcija kopiranja projekta kako bi se osiguralo da se naziv položaja resursa kopira iz originalnog projekta. |
| Planiranje i praćenje | 2184799 | Pooštrena je kontrola pri kopiranju projekta kako bi se osiguralo da se procenjeni datum početka ne može promeniti dok je kopiranje u toku. |
| Planiranje i praćenje | 2185134 | Tokom kopiranja projekta, predviđeni datum početka odredišnog projekta postavlja se na današnji datum. |
| Planiranje i praćenje | 2196373 | Uverite se da se zapisi menadžera projekta i članova tima ne dupliraju u projektnom timu kada se projekat kopira. |
| Planiranje i praćenje | 2211833 | Zadaci resursa se kopiraju iz izvornog projektnog zadatka u odredišni projekat. |
| Planiranje i praćenje | 2186541 | Rešeni su problemi u mreži **Procene** pri grupisanju po **resursima**. |
| Planiranje i praćenje | 2166906 | Kategorija transakcije iz zadatka mora se kopirati u entitet **Dodeljivanje resursa**. |
| Upravljanje resursima | 2125362 | Rešeni su problemi sa kreiranjem generičkog člana tima pomoću metode raspodele zasnovane na satima. |
| Vreme i trošak | 2113603 | Rešen je problem sa uklanjanjem atributa povezan sa prilagođavanjem sa stranice **Stavka vremena**. Sistem sada proverava da li atribut postoji na stranici pre nego što pristupi atributu pomoću skripte. |
| Vreme i trošak | 2204377 | Kopirani vremenski rasporedi moraju se automatski prikazati kada izaberete **Kopiranje sedmice**. |
| Vreme i trošak | 2209059 | Polje **Status** može da se uređuje za Dynamics 365 Field Service stavke vremena. |
