---
title: Cena za predmete ugovora zasnovane na proizvodu – jednostavno
description: Ova tema pruža informacije o kreiranju
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3def4c330dc9aadbf5ff806ef7682fbfd1072e4b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599287"
---
# <a name="cost-product-based-contract-lines---lite"></a>Cena za predmete ugovora zasnovane na proizvodu – jednostavno

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_


Predmeti ugovora zasnovanih na proizvodima u usluzi Dynamics 365 Project Operations uključuju polje **Cena koštanja** u kome se čuva cena koštanja proizvoda za proračune profitabilnosti distribucije.

Kada se za proizvod iz kataloga kreira predmet ugovora zasnovan na proizvodu, troškovi u redu se podrazumevano podešavaju iz polja **Standardni troškovi** u katalogu proizvoda. Polje **Standardna cena** u katalogu proizvoda podešeno je u osnovnoj valuti organizacije. Kada jedinični trošak podrazumeva predmet ugovora, on se pretvara u valutu prodaje na ugovoru.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Jedinična cena predmeta ugovora zasnovanog na proizvodu

Postojanje jedinične cene u predmetu ugovora zasnovanog na proizvodu omogućava različite cene za proizvod za svaku prodaju jedinice. Iako nisu uvek neophodni, postoje određeni scenariji u kojima dobavljač može sniziti troškove proizvoda za klijenta. Razmotrite sledeći scenario:

Fabrikam Robotics instalira robotske ruke na proizvodnim trakama kompanije Adatum Corporation. Fabrikam pruža usluge ugradnje, ali ruke robota su iz kompanije Trey Research. Ako instalacija robotske ruke u kompaniji Adatum Corporation otvori novu industrijsku delatnost za robotske ruke kompanije Trey Research, tada bi kompanija Trey Research mogla dati poseban popust za ovaj posao kompaniji Fabrikam. U ovom slučaju, Fabrikam kreira predmet ugovora zasnovan na proizvodu za ruke robota. Za ovaj ugovor se unosi cena po jedinici. Cena se razlikuje od cene za ruke robota kompanije Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]