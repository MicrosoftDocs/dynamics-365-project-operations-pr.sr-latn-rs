---
title: Šta je novo u junu 2022. – Project Operations jednostavna primena
description: Ovaj članak pruža informacije o kvalitetnim ispravkama koje su dostupne u izdanju Microsoft Dynamics 365 Project Operations lite primene u junu 2022.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 2d773603abef7ab45d4d1c298e5553e57893294d
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959655"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Šta je novo u junu 2022. – Project Operations jednostavna primena

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Ovaj članak se odnosi na sledeće komponente i verzije korporacije Microsoft Dynamics 365 Project Operations:

- Operacije projekta u verziji Dataverse okruženja 4.43.0.77

## <a name="quality-updates"></a>Ispravke kvaliteta

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Podizvođača | 2708885 | Otklonjena je poruka o grešci koja se pojavljuje kada korisnik kreira zapis zaglavlja rezervacije resursa koji se može rezervisati, a u kome nije popunjen resurs koji se može rezervisati. |
| Planiranje i praćenje projekta | 2629441 | Ispravljena je logika okidača toka posla da bi se sprečila beskonačna petlja kada se ažuriraju projektni zadaci. |
| Vreme i trošak | 2641209 | Uvoz vremenske stavke iz dodela/rezervacija mora zadržati referencu resursa koja se može rezervisati. |
| Planiranje i praćenje projekta | 2651148 | Zaglavlje projektnog dokumenta mora biti čuvano.|
| Planiranje i praćenje projekta | 2653145 | Dodate provere valjanosti da biste se uverili da nije moguće kreirati zapis projekta koji u imenu ima nevažeće znakove. |
| Vreme i trošak | 2654710 | Ispravljeno je filtriranje na stranici **"Odobrenja** ". |
| Naplata i određivanje cena | 2667805 | Dodate provere valjanosti koje pomažu u sprečavanju kreiranja rezultata fakturisane prodaje ako podrška neželjenim stvarnim prodajama ne postoji. |
| Naplata i određivanje cena | 2668378 | Dodate provere valjanosti koje sprečavaju da se doda prilagođena dimenzija određivanja cena, osim ako se ne popune logičko ime i ime polja. |
| Vreme i trošak | 2700428 | Poboljšana logika odobravanja kako bi se osiguralo da drugi skupovi odobravanja za projekat mogu da se obrade čak i ako je jedan od skupova odobravanja zaglavljen u sistemskim poslovima. |
