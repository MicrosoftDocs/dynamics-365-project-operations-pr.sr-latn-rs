---
title: Dodeljivanje generičkih resursa koji se mogu rezervisati zadatku i projektnom timu
description: Ova tema pruža informacije o rezervisanju generičkih resursa za zadatke i timove projekta.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ca0999ae5413d824dd1384fe2262e5226695a5f8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083595"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>Dodeljivanje generičkih resursa koji se mogu rezervisati zadatku i generisanje potreba za resursima 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Pored rezervisanja i dodeljivanja imenovanih ili stvarnih resursa projektu, možete da dodelite generičke resurse projektnim zadacima. Ti resursi mogu da posluže kao čuvari mesta za imenovane resurse dok ne budete spremni da kao angažovane osobe na projektu koristite imenovane resurse. 

1. U aplikaciji Project Service Automation (PSA) otvorite stranicu **Projekat** i na kartici **Raspored** unesite ime uloge generičkog resursa u ćeliju rasporeda **Resurs**. Možete i da kliknete na ikonu **Resurs** u ćeliji da biste otvorili birač resursa, a zatim uneli ime generičkog resursa koji želite da kreirate.

![Kreiranje i dodeljivanje generičkog člana tima](media/RM-how-to-9.png)

Tako ćete otvoriti tablu **Brzo kreiranje člana projektnog tima**. 

2. Unesite ulogu i organizacionu jedinicu generičkog člana tima resursa, a zatim kliknite na **Sačuvaj**.

![Brzo kreiranje generičkog člana tima](media/RM-how-to-10.png)

3. Nakon što ste kreirali novog generičkog člana tima resursa, on će biti dodeljen zadatku. Možete nastaviti da dodeljujete taj generički resurs drugim zadacima u rasporedu zadataka.

![Dodeljivanje postojećeg generičkog člana tima zadacima](media/RM-how-to-11.png)

4. Nakon što ste dodelili generički resurs, možete da generišete potrebu za resursom i da je ispunite direktnim rezervisanjem ili prosleđivanjem zahteva za resurs menadžeru resursa.

![Generisanje zahteva za generičkog člana tima](media/RM-how-to-12.png)

U mreži za članove tima, pored toga što možete da koristite birač resursa kao što je pomenuto gore, moći ćete direktno da dodate generičke resurse. Resursi se dodaju pomoću potreba za resursima koje se zasnivaju na datumu početka/završetka i metodi dodele koja je navedena u tabli **Brzo kreiranje člana projektnog tima**.

Možete videti razliku ako direktno dodate generičkog člana tima, a zatim dodelite još zadataka generičkom resursu od broja sati koje taj resurs može da pokrije. Kliknite na **Generiši zahtev** da biste ponovo generisali zahtev i balansirali zahtevane sate u odnosu na dodeljene zadatke.

Takođe možete da kliknete na vezu **Potreba za resursom** u mreži tima da biste otvorili zahtev i dodali veštine, željene resurse itd.

![Zahtev za resursima](media/RM-how-to-13.png)

