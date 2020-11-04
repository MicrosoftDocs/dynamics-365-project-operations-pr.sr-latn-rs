---
title: Obračun troškova za predmete ugovora zasnovane na proizvodima
description: Ova tema pruža informacije o kreiranju
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/20/2020
ms.locfileid: "4083811"
---
# <a name="costing-product-based-contract-lines"></a>Obračun troškova za predmete ugovora zasnovane na proizvodima

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_


Predmeti ugovora zasnovani na proizvodima u programu Dynamics 365 Project Operations uključuju polje **Cena koštanja** , u kome se čuva cena koštanja proizvoda za proračun profitabilnosti na nižem nivou.

Kada se predmet ugovora zasnovan na proizvodu kreira za kataloški proizvod, podrazumevani troškovi predmeta ugovora zasnovanog na proizvodu dolaze iz polja **Standardna cena** u katalogu proizvoda. Polje **Standardna cena** u katalogu proizvoda podešeno je u osnovnoj valuti organizacije. Kada jedinični trošak podrazumeva predmet ugovora, on se pretvara u valutu prodaje na ugovoru.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Jedinična cena predmeta ugovora zasnovanog na proizvodu

Postojanje jedinične cene u predmetu ugovora zasnovanog na proizvodu omogućava različite cene za proizvod za svaku prodaju jedinice. Iako nisu uvek neophodni, postoje određeni scenariji u kojima dobavljač može sniziti troškove proizvoda za klijenta. Razmotrite sledeći scenario:

Fabrikam Robotics instalira robotske ruke na proizvodnim trakama kompanije Adatum Corporation. Fabrikam pruža usluge ugradnje, ali robotske ruke su nabavljene od kompanije Trey Research. Ako instalacija robotske ruke u kompaniji Adatum Corporation otvori novu industrijsku delatnost za robotske ruke kompanije Trey Research, tada bi kompanija Trey Research mogla dati poseban popust za ovaj posao kompaniji Fabrikam. U ovom slučaju, Fabrikam kreira predmet ugovora zasnovan na proizvodu za robotske ruke i unosi jedinični trošak za ovaj ugovor koji se razlikuje od standardnog troška robotskih ruku kompanije Trey Research.
