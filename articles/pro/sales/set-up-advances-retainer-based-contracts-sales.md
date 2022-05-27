---
title: Avansi i ugovori zasnovani na avansnim uplatama
description: Ova tema pruža informacije o ugovornim modelima i napretku zasnovanim na odbitku u usluzi Project Operations.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: fcee7b818097c10f8f861c4de4898daacef60e4f
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574815"
---
# <a name="advances-and-retainer-based-contracts"></a>Avansi i ugovori zasnovani na avansnim uplatama


_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Dynamics 365 Project Operations podržava ugovore zasnovane na avansnim uplatama. Ugovor zasnovan na odbitku je dogovoreni skup jednako raspoređenih uplata koje će se klijentu fakturisati tokom trajanja projekta. Ova vrsta ugovora se obično koristi za modele obračuna na osnovu vremena i materijala ili potrošnje, gde postoji potreba da se klijentu pruži predvidljiva faktura i raspored plaćanja. Stvarni iznosi prihoda prikupljeni za svaki period usklađuju se sa uplatom primljenom od klijenta na početku perioda. U skladu sa konceptom modela obračuna vremena i materijala, vrednosti prihoda nastale u svakom periodu mogu se razlikovati u zavisnosti od nastalih troškova. Ako je ostvareni prihod veći od iznosa primljenog na početku perioda, kompanija za isporuku projekata bi mogla:

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]