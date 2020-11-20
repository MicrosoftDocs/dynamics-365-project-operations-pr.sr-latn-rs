---
title: Podešavanje rasporeda avansa – jednostavno
description: Ova tema pruža informacije o tome kako da podesite raspored avansa u usluzi Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e0312b89d9969f140146b6aaaa9bdcfde702c0b
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181289"
---
# <a name="set-up-a-retainer-schedule---lite"></a>Podešavanje rasporeda avansa – jednostavno

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Rasporedi avansa se podešavaju na stranici **Ugovor za projekat** u usluzi Dynamics 365 Project Operations.

1. Na stranici **Ugovor o projektu**, na kartici **Akontacije i avansi**, izaberite **Podesi raspored avansa**.
2. Na stranici dijaloga koja se otvori, prikazana su polja navedena u sledećoj tabeli. Tabela daje ideju o tome kako unete vrednosti utiču na raspored avansa koji će se kreirati.

| Polje | Opis | Posledični uticaj |
| --- | --- | --- |
| Klijent ugovora za projekat | Klijent na ugovoru kome će se fakturisati za ovu akontaciju ili avans. | Ako imate više klijenata na ugovoru i ako treba da fakturišete svakom od njih za određenu akontaciju ili avansni iznos, ručno napravite po jednu fakturu za svakog klijenta. |
| Početak rasporeda avansa | Unesite datum početka rasporeda avansa. | Ovaj datum ne mora da bude datum kada je kreiran prvi avans ili akontacija. Na datum kreiranja prvog avansa ili akontacije takođe utiče učestalost fakturisanja. |
| Završetak rasporeda avansa | Unesite datum završetka rasporeda avansa. | Ovaj datum ne mora da bude datum kada je kreiran poslednji avans ili akontacija. Na datum kreiranja poslednjeg avansa ili akontacije takođe utiče učestalost fakturisanja. |
| Broj avansa za kreiranje | Kada unesete broj avansa koje treba kreirati, sistem koristi datum početka i učestalost za kreiranje broja u ovom polju. | Kada se ovo polje ručno ažurira, sistem zanemaruje vrednost u polju **Kraj rasporeda avansa** i umesto toga kreira određeni broj avansa ili akontacija. |
| Učestalost fakturisanja | Koliko često će aplikacija kreirati avanse i akontacije. | Ova vrednost direktno utiče na broj avansa i akontacija i datume kreiranja. |
| Ukupan iznos | Ukupan iznos je iznos koji se deli na pojedinačni avans ili avansno plaćanje koje će se kreirati. | Nema posledičnog uticaja za ovo polje. |
