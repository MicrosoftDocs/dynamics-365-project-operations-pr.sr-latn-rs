---
title: Upravljanje zaostalima naplatama za projekat
description: Ova tema pruža informacije o raznim prikazima koji se mogu koristiti prilikom upravljanja zaostalim obračunima na projektima.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 27ef2ae90778394d15b979a13215c8f5af483cda0312682e9fc7256b8282b999
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988308"
---
# <a name="manage-project-billing-backlog"></a>Upravljanje zaostalima naplatama za projekat 

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Dynamics 365 Project Operations ima namenske prikaze koji pomažu u upravljanju zaostalim naplatama. Da biste upravljali zaostalim naplatama, izaberite veze u oblasti **Prodaja** u odeljku **Naplate**. 

Dostupni su sledeći prikazi:

- Avansi i akontacije
- Dostupni avansi i akontacije
- Kontrolne tačke fiksne cene
- Neizvršavanje naplate proizvoda
- Neizvršavanje naplate vremena i materijala

## <a name="retainers-and-advances"></a>Avansi i akontacije

Prikaz **Avansi i akontacije** navodi sve avanse i akontacije u svim ugovorima za projekte u sistemu. Kada se akontacija ili avans fakturiše, iznos avansa postaje dostupan za upotrebu.

## <a name="available-retainers-and-advances"></a>Dostupni avansi i akontacije

Prikaz **Dostupni avansi i akontacije** navodi sve dostupne avanse i akontacije u svim ugovorima za projekte u sistemu. Kada se akontacija ili avans fakturiše, iznos avansa postaje dostupan za upotrebu i dodaje se na listu. Kada se u potpunosti iskoristi iznos akontacije ili avansa, stavka se uklanja sa liste.

## <a name="fixed-price-milestones"></a>Kontrolne tačke fiksne cene

Prikaz **Kontrolne tačke sa fiksnom cenom** navodi sve kontrolne tačke sa fiksnom cenom u svim predmetima ugovora o projektu u sistemu. Jednu ili više kontrolnih tačaka možete označiti kao **Spremno za fakturisanje** ili **Nije spremno za fakturisanje** iz ovog prikaza. Označavanje kontrolne tačke kao **Spremno za fakturisanje** omogućava njeno stavljanje na radnu verziju fakture.

Kada predmeti ugovora za više klijenata imaju metodu obračuna sa fiksnom cenom, kreira se kontrolna tačka za svakog klijenta na predmetu ugovora. Kontrolna tačka se može kreirati, a zatim podeliti u pojedinačne zapise kontrolnih tačaka specifične za klijenta. Ova podela je interna i u skladu je sa podelom procenta naplate koja je definisana za svakog klijenta u predmetu ugovora. U prikazu **Kontrolne tačke sa fiksnom cenom** videćete pojedinačne kontrolne tačke specifične za klijenta. Svaki od ovih zapisa kontrolnih tačaka može se označiti kao **Spremno za fakturisanje** nezavisno od ovog prikaza. Kada se podele jedne ili više povezanih kontrolnih tačaka označe kao **Spremno za fakturisanje**, status zaglavlja se menja sa **Nije započeto** na **U toku**. Kada se fakturišu sve podele kontrolnih tačaka, status kontrolne tačke zaglavlja se menja na **Završeno**.

Kontrolna tačka u radnoj verziji fakture prikazana je u ovom prikazu sa statusom naplate **Kreirana je faktura za klijenta**. Kada se potvrdi radna verzija fakture, status naplate u zapisu se menja na **Faktura za klijenta je objavljena**. Ne ažurirajte ovu vrednost statusa pomoću prilagođenog koda. Project Operations ne funkcioniše ispravno kada se ove vrednosti statusa ažuriraju sa prilagođenim kodom.

## <a name="product-billing-backlog"></a>Neizvršavanje naplate proizvoda

Prikaz **Zaostatak u obračunu proizvoda** navodi sve predmete ugovora zasnovane na proizvodima u svim ugovorima za projekte u sistemu. Jedan ili više predmeta ugovora zasnovanih na proizvodu možete označiti kao **Spremno za fakturisanje** ili **Nije spremno za fakturisanje** iz ovog prikaza. Označavanje predmeta ugovora zasnovanog na proizvodu kao **Spremno za fakturisanje** omogućava njegovo stavljanje na radnu verziju fakture.

Predmet ugovora zasnovan na proizvodu koji se nalazi na radnoj verziji fakture prikazuje se u ovom prikazu sa statusom naplate **Faktura kreirana za klijenta**. Kada se potvrdi radna verzija fakture, status naplate na ovom zapisu ažurira se na **Faktura za klijenta je proknjižena**. Ne ažurirajte ovu vrednost statusa pomoću prilagođenog koda. Project Operations ne funkcioniše ispravno kada se ove vrednosti statusa ažuriraju sa prilagođenim kodom.

## <a name="time-and-material-billing-backlog"></a>Neizvršavanje naplate vremena i materijala

Prikaz **Neizvršavanje naplate vremena i materijala** navodi sve stvarne vrednosti nenaplaćene prodaje u svim ugovorima za projekte u sistemu koji nisu fakturisani. Jedan ili više nenaplaćenih stvarnih iznosa prodaje možete označiti kao **Spremno za fakturisanje** ili **Nije spremno za fakturisanje** iz ovog prikaza. Označavanje nenaplaćenog stvarnog iznosa prodaje kao **Spremno za fakturisanje** omogućava stavljanje fakture u radnu verziju.

Stvarne vrednosti nenaplaćene prodaje sa statusom **Neprekoračenje** čija vrednost je **Nije uspelo** ne može da se označi kao **Spremno za fakturisanje**. Ako stvarne vrednosti treba označiti kao **Spremno za fakturisanje**, resetujte status na ostalih stvarnih vrednosti na predmetu ugovora koje su dodeljene. i ponovo procenite status **Neprekoračenje**.

Ako predmeti ugovora za više klijenata imaju način naplate vremena i materijala, kada se odobre vreme i troškovi, za svakog klijenta na predmetu ugovora se kreira jedna stvarna vrednost nenaplaćene prodaje, prema podeli procenta naplate definisanoj za svakog od klijenata. U prikazu **Neizvršavanje naplate vremena i materijala** videćete ove pojedinačne stvarne vrednosti nenaplaćene prodaje specifične za klijenta. Svaki od ovih zapisa nenaplaćenih stvarnih troškova prodaje može se označiti kao **Spremno za fakturisanje** nezavisno od ovog prikaza.

Stvarna vrednost nenaplaćene prodaje koja se nalazi na radnoj verziji fakture prikazuje se u ovom prikazu sa statusom naplate **Faktura kreirana za klijenta**. Kada se potvrdi radna verzija fakture, status naplate na ovom zapisu ažurira se na **Faktura za klijenta je proknjižena**. Ne ažurirajte ovu vrednost statusa pomoću prilagođenog koda. Project Operations ne funkcioniše ispravno kada se ove vrednosti statusa ažuriraju sa prilagođenim kodom.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
