---
title: Upravljanje zaostalim obračunima
description: Ova tema pruža informacije o tome kako da prikažete i radite sa zaostalim naplatama u usluzi Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9837af0d3c0b2476edab35a53092cf95a44e5244
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600021"
---
# <a name="manage-billing-backlog"></a>Upravljanje zaostalim obračunima

**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha

Dynamics 365 Project Operations ima namenske prikaze koji pomažu u upravljanju zaostalim naplatama. Da biste upravljali zaostalim naplatama, izaberite veze u oblasti **Prodaja** u odeljku **Naplate**. 

Dostupni su sledeći prikazi:

- Avansi i akontacije
- Dostupni avansi i akontacije
- Kontrolne tačke fiksne cene
- Neizvršavanje naplate vremena i materijala

## <a name="retainers-and-advances"></a>Avansi i akontacije

Prikaz **Obustave i akontacije** navodi obustave i akontacije u svim ugovorima za projekte u sistemu. Kada se akontacija ili avans fakturiše, iznos avansa postaje dostupan za upotrebu.

## <a name="available-retainers-and-advances"></a>Dostupni avansi i akontacije

Prikaz **Dostupne obustave i akontacije** navodi sve dostupne obustave i akontacije u svim ugovorima za projekte u sistemu. Kada se akontacija ili avans fakturiše, iznos avansa postaje dostupan za upotrebu i dodaje se na listu. Kada se u potpunosti iskoristi iznos obustave ili akontacije, stavka se uklanja sa liste.

## <a name="fixed-price-milestones"></a>Kontrolne tačke fiksne cene

Prikaz **Kontrolne tačke sa fiksnom cenom** navodi sve kontrolne tačke sa fiksnom cenom u svim predmetima ugovora o projektu. Iz ovog prikaza, jedna ili više kontrolnih tačaka mogu se označiti kao **Spremno za fakturisanje** ili **Nije spremno za fakturisanje**. Označavanje kontrolne tačke kao **Spremno za fakturisanje** omogućava njeno stavljanje na radnu verziju fakture.

Kada predmeti ugovora za više klijenata imaju metodu obračuna sa fiksnom cenom, kreira se kontrolna tačka za svakog klijenta na predmetu ugovora. Kontrolna tačka se može kreirati, a zatim podeliti u pojedinačne zapise kontrolnih tačaka specifične za klijenta. Ova podela je interna i u skladu je sa podelom procenta naplate koja je definisana za svakog klijenta u predmetu ugovora. U prikazu **Kontrolne tačke sa fiksnom cenom** videćete pojedinačne kontrolne tačke specifične za klijenta. Svaki od ovih zapisa kontrolnih tačaka može se označiti kao **Spremno za fakturisanje** nezavisno od ovog prikaza. Kada se jedna ili više povezanih podeljenih kontrolnih tačaka označi kao **Spremno za fakturisanje**, status zaglavlja se ažurira sa **U toku** na **Nije započeto**. Kada se fakturišu sve podeljene kontrolne tačke, status kontrolne tačke zaglavlja se ažurira na **Završeno**.

Kontrolna tačka u radnoj verziji fakture prikazana je u ovom prikazu sa statusom naplate **Kreirana je faktura za klijenta**. Kada se potvrdi radna verzija fakture, status naplate u zapisu se menja na **Faktura za klijenta je objavljena**. 

> [!NOTE] 
> Ne ažurirajte ovu vrednost statusa pomoću prilagođenog koda. Project Operations ne funkcioniše ispravno kada se ove vrednosti statusa ažuriraju sa prilagođenim kodom.

## <a name="time-and-material-billing-backlog"></a>Neizvršavanje naplate vremena i materijala

Prikaz **Neizvršavanje naplate vremena i materijala** navodi sve stvarne vrednosti nenaplaćene prodaje u svim ugovorima za projekte u sistemu koji nisu fakturisani. Jedan ili više nenaplaćenih stvarnih iznosa prodaje možete označiti kao **Spremno za fakturisanje** ili **Nije spremno za fakturisanje** iz ovog prikaza. Označavanje nenaplaćenog stvarnog iznosa prodaje kao **Spremno za fakturisanje** omogućava stavljanje fakture u radnu verziju.

Stvarne vrednosti nenaplaćene prodaje sa statusom **Neprekoračenje** čija vrednost je **Nije uspelo** ne može da se označi kao **Spremno za fakturisanje**. Ako stvarne stvari treba označiti kao **Spremno za fakturisanje**, resetujte status na ostale stvarne vrednosti na predmetu ugovora koje su preuzete, a zatim ponovo procenite status **Ne sme da se prekorači**.

Ako predmeti ugovora za više klijenata imaju način naplate vremena i materijala, kada se odobre vreme i troškovi, za svakog klijenta na predmetu ugovora se kreira jedna stvarna vrednost nenaplaćene prodaje, prema podeli procenta naplate definisanoj za svakog od klijenata. U prikazu **Neizvršavanje naplate vremena i materijala** videćete ove pojedinačne stvarne vrednosti nenaplaćene prodaje specifične za klijenta. Svaki od ovih zapisa nenaplaćenih stvarnih troškova prodaje može se označiti kao **Spremno za fakturisanje** nezavisno od ovog prikaza.

Stvarna vrednost nenaplaćene prodaje koja se nalazi u radnoj verziji fakture prikazuje se u ovom prikazu sa statusom naplate **Kreirana faktura za klijenta**. Kada se potvrdi radna verzija fakture, status naplate na ovom zapisu ažurira se na **Faktura za klijenta je proknjižena**. 

> [!NOTE] 
> Ne ažurirajte ovu vrednost statusa pomoću prilagođenog koda. Project Operations ne funkcioniše ispravno kada se ove vrednosti statusa ažuriraju sa prilagođenim kodom.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
