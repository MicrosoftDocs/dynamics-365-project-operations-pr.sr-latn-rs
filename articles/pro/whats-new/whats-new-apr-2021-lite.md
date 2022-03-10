---
title: Šta je novo u aprilu 2021. – jednostavna primena usluge Project Operations
description: Ova tema pruža informacije o ispravkama kvaliteta dostupnim u jednostavnoj primeni izdanja Project Operations za april 2021. godine.
author: sigitac
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8c85e0230840753bc1d28a46b065bce002446f5d8c62da9666d58bc9d2a68af8
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009413"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>Šta je novo u aprilu 2021. – jednostavna primena usluge Project Operations

_Odnosi se na: Jednostavna primena – od pogodbe do profakture_

Ova tema se odnosi na sledeće komponente i verzije usluge Dynamics 365 Project Operations:

  - Project Operations u Dataverse okruženju verzije 4.9.0.221 

## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

Sledeće funkcije su uključene u ovom izdanju:

- Materijali bez zaliha za projekte. Ključne mogućnosti uključuju:
  - Procena i određivanje cene materijala bez zaliha tokom ciklusa prodaje u projektu. Za više informacija, pogledajte [Podešavanje troškova i stopa prodaje za proizvode iz kataloga – jednostavno](../pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Praćenje upotrebe materijala bez zaliha tokom isporuke projekata. Za više informacija pogledajte [Evidentiranje upotrebe materijala na projektima i projektnim zadacima](../../material/material-usage-log.md).
  - Fakturisanje utrošenih troškova materijala bez zaliha. Za više informacija, pogledajte [Upravljanje zaostalim obračunom – jednostavno](../proforma-invoicing/manage-billing-backlog-sales.md#product-billing-backlog).
  - Novi API-ji u platformi Dynamics 365 Dataverse dozvoljavaju kreiranje, ažuriranje i brisanje operacija pomoću **entiteta planiranja**. Za više informacija, pogledajte [Korišćenje API-ja za raspored za obavljanje operacija sa entitetima planiranja](../../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Ispravke kvaliteta

| **Oblast funkcija** | **Referentni broj** | **Ispravka kvaliteta** |
| --- | --- | --- |
| Naplata i određivanje cena | 2224568 | Dodata je logika za omogućavanje prilagođavanja koja uključuju pozivanje dodatne komponente za potvrdu fakture. |
| Naplata i određivanje cena | 2101098 | Poboljšana logika podrazumevanih polja za predračun: **Adresa fakturisanja**, **Ime fakturisanja** i **Uslovi plaćanja** sada se podrazumevaju iz odgovarajućeg zapisa klijenta ugovora o projektu. |
| Naplata i određivanje cena | 2021413 | Ažurirana su polja **Stvarna cena** i **Prodaja** na entitetu **Zadatak** da uključi vrednosti prodaje iz nenaplaćenih i naplaćenih troškova na zadacima. |
| Naplata i određivanje cena | 2182110 | Prilikom kopiranja ugovora o projektu, ID predmeta ugovora se ponovo generiše u ugovoru o odredišnom projektu kako bi se osiguralo da je jedinstven. |
| Upravljanje mogućnostima za poslovanje | 2186741 | Dodate su validacije kako bi se osiguralo da polje **Poreklo** i **Tip transakcije** ne mogu da se ažuriraju na postojećim detaljima stavke ponude. |
| Upravljanje mogućnostima za poslovanje | 2191353 | Kontrolne tačke se ne smeju kreirati na predmetu ugovora za vreme i materijal. |
| Upravljanje mogućnostima za poslovanje | 2216956 | Rešeni su problemi sa **ažuriranjem cena**. |
| Planiranje i praćenje | 2182979 | Poboljšana je funkcija kopiranja projekta kako bi se osiguralo kopiranje stavki procene troškova iz originalnog projekta. |
| Planiranje i praćenje | 2184144 | Poboljšana je funkcija kopiranja projekta kako bi se osiguralo da se naziv položaja resursa kopira iz originalnog projekta. |
| Planiranje i praćenje | 2184799 | Kopiranje projekta: Pooštrena je kontrola kako bi se osiguralo da se procenjeni datum početka ne može promeniti dok je kopiranje u toku. |
| Planiranje i praćenje | 2185134 | Kopiranje projekta: Predviđeni datum početka odredišnog projekta postavljen je na današnji datum. |
| Planiranje i praćenje | 2196373 | Kopiranje projekta: Uverite se da se zapisi menadžera projekta i člana tima ne dupliraju u projektnom timu. |
| Planiranje i praćenje | 2211833 | Kopiranje projekta: Zadaci resursa se kopiraju iz izvornog projektnog zadatka u odredišni projekat. |
| Planiranje i praćenje | 2186541 | Rešeni su problemi u mreži **Procene** pri grupisanju po resursima. |
| Planiranje i praćenje | 2166906 | Kategorija transakcije iz zadatka mora se kopirati u entitet **Dodeljivanje resursa**. |
| Upravljanje resursima | 2125362 | Rešeni su problemi sa kreiranjem generičkog člana tima pomoću metode raspodele zasnovane na satima. |
| Vreme i trošak | 2113603 | Rešen je problem sa uklanjanjem atributa povezan sa prilagođavanjem sa stranice **Stavka vremena**. Sistem sada proverava da li atribut postoji na stranici pre nego što im pristupi pomoću skripte. |
| Vreme i trošak | 2204377 | Kopirani vremenski rasporedi moraju se automatski prikazati kada izaberete **kopiranje sedmice** tokom unosa vremena. |
| Vreme i trošak | 2209059 | Polje **Status** može da se uređuje za Dynamics 365 Field Service stavke vremena. |