---
title: Šta je novo u junu 2022. – Project Operations jednostavna primena
description: Ovaj članak pruža informacije o ispravkama kvaliteta koje su dostupne u izdanju za jun 2022. usluge Microsoft Dynamics 365 Project Operations jednostavna primena.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8313288ecf7ff1350cd82c62d3d0c291d8a3ded4
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031210"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Šta je novo u junu 2022. – Project Operations jednostavna primena

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Ovaj članak se odnosi na sledeće komponente i verzije usluge Microsoft Dynamics 365 Project Operations:

- Project Operations u Dataverse okruženju verzije 4.43.0.77 ili 4.43.0.119

## <a name="quality-updates"></a>Ispravke kvaliteta

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Podugovaranje | 2708885 | Otklonjena je poruka o grešci koja se pojavljuje kada korisnik kreira zapis zaglavlja rezervacije resursa koji može da se rezerviše, a u kome nije popunjen resurs koji se može rezervisati. |
| Planiranje i praćenje projekta | 2629441 | Ispravljena je logika okidača toka posla da bi se sprečila beskonačna petlja kada se ažuriraju projektni zadaci. |
| Vreme i trošak | 2641209 | Uvozi stavki vremena iz dodela/rezervacija mora zadržati referencu na resurs koji se može rezervisati. |
| Planiranje i praćenje projekta | 2651148 | Zaglavlje projektnog dokumenta mora biti zaštićeno.|
| Planiranje i praćenje projekta | 2653145 | Dodate su provere ispravnosti da se osiguralo da nije moguće kreirati zapis projekta koji u nazivu ima nevažeće znakove. |
| Vreme i trošak | 2654710 | Ispravljeno je filtriranje na stranici **Odobrenja**. |
| Naplata i određivanje cena | 2667805 | Dodate su provere ispravnosti kojima se sprečava kreiranje stvarnih vrednosti naplaćene prodaje ako podrška stvarnih vrednosti nenaplaćene prodaje ne postoji. |
| Naplata i određivanje cena | 2668378 | Dodate su provere ispravnosti koje sprečavaju da se doda prilagođena dimenzija određivanja cena, osim ako se ne popune logičko ime i naziv polja. |
| Vreme i trošak | 2700428 | Poboljšana je logika odobrenja kako bi se osiguralo da drugi skupovi odobrenja za projekat mogu da se obrade čak i ako je jedan od skupova odobrenja zaglavljen u sistemskim poslovima. |
