---
title: Ugovori zasnovani na avansima i avansnim uplatama – jednostavno
description: Ova tema pruža informacije o ugovornim modelima i napretku zasnovanim na odbitku u usluzi Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 912b235af5e561349fdfb481e5f5b7c5514669c3
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180884"
---
# <a name="advances-and-retainer-based-contracts---lite"></a>Ugovori zasnovani na avansima i avansnim uplatama – jednostavno


_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Dynamics 365 Project Operations podržava ugovore zasnovane na odbitku. Ugovor zasnovan na odbitku je dogovoreni skup jednako raspoređenih uplata koje će se klijentu fakturisati tokom trajanja projekta. Ova vrsta ugovora se obično koristi za modele obračuna na osnovu vremena i materijala ili potrošnje, gde postoji potreba da se klijentu pruži predvidljiva faktura i raspored plaćanja. Stvarni iznosi prihoda prikupljeni za svaki period usklađuju se sa uplatom primljenom od klijenta na početku perioda. U skladu sa konceptom modela obračuna vremena i materijala, vrednosti prihoda nastale u svakom periodu mogu se razlikovati u zavisnosti od nastalih troškova. Ako je ostvareni prihod veći od iznosa primljenog na početku perioda, kompanija za isporuku projekata bi mogla:

- Da klijentu fakturiše samo višak 
- Da odloži sravnjenje prihoda sa sledećim periodom fakturisanja i napravi jedan završni račun na kraju projekta za sve preostale prihode za koje nema sravnjenja

Glavna razlika između modela ugovaranja zasnovanog na odbitku i modela ugovora sa fiksnom cenom u usluzi Project Operations jeste to što u modelu ugovora sa fiksnom cenom iznos fakture nije povezan ili vezan za nastale troškove. Fakturisanje sledi pristup zasnovan na kontrolnim tačkama koji je usklađen sa troškovima nastalim u tom periodu. U ugovoru koji se zasniva na odbitku, prihod koji se može fakturisati evidentira se na osnovu načina naplate na predmetu ugovora. Kada je način naplate vreme i materijal, fakturisani prihod vezan je za troškove nastale u bilo kom datom periodu i može se razlikovati od perioda do perioda. Međutim, klijentu se fakturiše samo iznos na periodičnom odbitku. Sistem koristi drugu fakturu na kraju perioda za sravnjenje prihoda koji se fakturiše i koji je evidentiran tokom tog perioda u odnosu na iznos za koji je klijentu fakturisan na početku perioda.

Prednost ove metode jeste to što troškovi klijenta postaju predvidljivi u rasporedu odbitaka, za razliku od uobičajenog modela vremena i materijala. Organizacija koja dostavlja projekat takođe ima prostora da pokrije rizik storniranja troškova nastalih usled bilo kakvog povećanja obima koji im model fiksne cene ne bi dozvolio.

Pored periodičnog rasporeda zasnovanog na odbicima, Project Operations može zabeležiti jednokratni avans od klijenta i sravniti ga sa različitim komponentama troškova projekta.

Odbitak u usluzi Project Operations nije dostupan za upotrebu dok se klijentu ne fakturiše. To pokazuju sledeća polja na podformi za avanse i odbitke.

| Polje | Opis | Posledični uticaj |
| --- | --- | --- |
| Dostupan iznos | Iznos koji je dostupan za upotrebu na zapisu odbitka ili avansa. | Dok se avans ili odbitak ne fakturiše, nije dostupan za upotrebu, što znači da će raspoloživi iznos biti nula. |
| Iskorišćen iznos | Iznos koji se već koristi na odbitku ili avansu. | Avans ili odbitak mogu se delimično sravniti na fakturi sa stvarnim troškovima koji će imati deo koji će biti označen kao već korišćen ili potrošen. Preostali iznos avansa ili odbitka dostupan je za sravnjenje na budućoj fakturi sa stvarnim troškovima. |