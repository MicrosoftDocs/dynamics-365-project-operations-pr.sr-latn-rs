---
title: Kreiranje dodela resursa
description: Ova tema pruža informacije o kreiranju generičkih i imenovanih dodela resursa.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a6f4f12a962cb570e8b83d8ee7a01fc0cc2c6155
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287120"
---
# <a name="create-resource-assignments"></a>Kreiranje dodela resursa

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_


Dodeljivanje resursa je direktno povezivanje člana projektnog tima sa zadatkom čvora lista. Ova tema pruža informacije o različitim načinima za dodeljivanje resursa.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Kreiranje generičkog člana tima preko dodele zadatka


Kada kreirate generičkog člana tima dodeljivanjem zadatka, kreirate rezervisano mesto ili generički resurs. Ovaj generički resurs opisuje karakteristike imenovanog resursa za kojeg doista želite da radi na zadacima. Zatim generišete uslov ili prosleđujete zahtev korišćenjem uslova koji se koristi za pretragu i rezervaciju imenovanog resursa.

1. Na mreži Raspored za zadatak, izaberite ikonu resursa u ćeliji **Resurs**.
2. Unesite ime koje će služiti kao ime čuvara mesta resursa. Na primer, Menadžer programa.
3. Izaberite **Kreiraj**, pa u polju **Brzo kreiranje člana projektnog tima** podesite ulogu za generički resurs.
4. Dodeljujte zadatke po potrebi u ovaj resurs čuvara mesta izborom resursa u **biraču resursa** za zadatak. Resursi su navedeni u okviru opcije **Članovi tima**.
5. Kada završite sa dodeljivanjem generičkog resursa, izaberite generički resurs na kartici **Tim**, a zatim izaberite **Generiši potrebu** da biste kreirali potrebu za resursom za generički resurs.
6. Izaberite stavku **Rezerviši** za generički resurs, a zatim koristite tabelu rasporeda da biste pronašli i rezervisali stvarni resurs. Možete i da prosledite zahtev za ispunjenje od strane menadžera resursa.
7. Kada se generički resurs u potpunosti ispuni (delimično ispunjenje zahteva za resursom neće rezultirati dodeljivanjem resursa) sa imenovanim resursom, generički resurs se uklanja iz tima. Zadaci zadatka za generički resurs dodeljuju se imenovanom resursu koji je ispunio zahtev za resursom generičkog resursa.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Dodela imenovanog resursa sa liste svih resursa koji mogu da se rezervišu

Možete da koristite polje za pretragu u **biraču resursa** da pretražite sve aktivne resurse koji mogu da se rezervišu i dodelite ih zadatku čvora lista. Resursi dodeljeni na ovaj način dodaju se u tim bez ikakvih rezervacija. To je slično dodavanju člana tima i odluci da izaberete **Nijedno** kao metodu dodele. Resurs se prikazuje na karticama **Tim**, **Dodela resursa** i **Usaglašenost** kao resurs samo sa dodelama i sa nedostatkom rezervacije. Rezervišete ih ako želite da koristite njihovu dostupnost.

1. Iz mreže zadataka, sa table ili vremenske ose idite na ćeliju **Dodeljeno**.
2. U polju za pretragu počnite da kucate ime. Prikazuju se rezultati pretrage za ime u **biraču resursa** u okviru opcije **Drugi resursi**.
3. Izaberite resurs koji želite da dodelite zadatku ili izaberite ime resursa u delu **Ostali resursi tima**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]