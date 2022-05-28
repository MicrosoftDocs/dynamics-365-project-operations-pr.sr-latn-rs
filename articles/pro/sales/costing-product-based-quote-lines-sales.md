---
title: Stavke proizvoda zasnovane na obračunu
description: Ova tema pruža informacije o primeni cene koštanja na stavku ponude zasnovane na proizvodu.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 33cfd42a61b368dc2d2d7f18bfaccf3a221a38fe
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598324"
---
# <a name="costing-product-based-quote-lines"></a>Stavke proizvoda zasnovane na obračunu

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_


Stavke ponude zasnovane na proizvodu u usluzi Dynamics 365 Project Operations takođe imaju polje **Cena koštanja**. Ovo polje se koristi za praćenje cene koštanja proizvoda na stavci ponude i za posledične proračune profitabilnosti.

Kada se stavka ponude zasnovana na proizvodu kreira za kataloški proizvod, podrazumevani troškovi stavke ponude zasnovane na proizvodu dolaze iz polja **Standardna cena** u katalogu proizvoda. Polje standardne cene u katalogu proizvoda podešeno je u osnovnoj valuti organizacije. Podrazumevana jedinična cena u stavci ponude zasnovane na proizvodu pretvara se u prodajnu valutu u ponudi.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Jedinična cena stavke ponude zasnovane na proizvodu

Svrha postojanja jedinične cene u stavci ponude zasnovane na proizvodu je omogućavanje različitih cena za proizvod za svaku prodaju. To nije tipičan scenario, ali dobavljač ponekad može da snizi cenu proizvoda u zavisnosti od klijenta konačne prodaje.

Na primer:

Fabrikam Robotics instalira robotske ruke na proizvodnim trakama kompanije A Datum Corporation. Fabrikam pruža usluge ugradnje, ali robotske ruke su nabavljene od kompanije Trey robotics. Ako instalacija robotske ruke u kompaniji A Datum Corporation otvori novu industrijsku delatnost za robotske ruke kompanije Trey, tada bi kompanija Trey mogla dati poseban popust za ovaj posao kompaniji Fabrikam.

U ovom slučaju, Fabrikam će kreirati stavku ponude zasnovanu na proizvodu za robotske ruke i uneće posebnu cenu po jedinici za ovu ponudu. Ta cena se razlikuje od standardne cene robotske ruke kompanije Trey.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]