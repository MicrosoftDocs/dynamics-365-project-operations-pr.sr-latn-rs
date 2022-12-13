---
title: Stavke proizvoda zasnovane na obračunu
description: Ovaj članak pruža informacije o primeni cene koštanja na stavku ponude zasnovane na proizvodu.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a8b3569ff217f6fc62606dae4292be14f9d3358c
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825629"
---
# <a name="costing-product-based-quote-lines"></a>Stavke proizvoda zasnovane na obračunu

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_


Stavke ponude zasnovane na proizvodu u usluzi Dynamics 365 Project Operations takođe imaju polje **Cena koštanja**. Ovo polje se koristi za praćenje cene koštanja proizvoda na stavci ponude i za posledične proračune profitabilnosti.

Kada se stavka ponude zasnovana na proizvodu kreira za kataloški proizvod, podrazumevani troškovi stavke ponude zasnovane na proizvodu dolaze iz polja **Standardna cena** u katalogu proizvoda. Polje standardne cene u katalogu proizvoda podešeno je u osnovnoj valuti organizacije. Podrazumevana jedinična cena u stavci ponude zasnovane na proizvodu pretvara se u prodajnu valutu u ponudi.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Jedinična cena stavke ponude zasnovane na proizvodu

Svrha postojanja jedinične cene u stavci ponude zasnovane na proizvodu je omogućavanje različitih cena za proizvod za svaku prodaju. To nije tipičan scenario, ali dobavljač ponekad može da snizi cenu proizvoda u zavisnosti od klijenta konačne prodaje.

Na primer:

Fabrikam Robotics instalira robotske ruke na proizvodnim trakama kompanije A Datum Corporation. Fabrikam pruža usluge ugradnje, ali robotske ruke su nabavljene od kompanije Trey robotics. Ako instalacija robotske ruke u kompaniji A Datum Corporation otvori novu industrijsku delatnost za robotske ruke kompanije Trey, tada bi kompanija Trey mogla dati poseban popust za ovaj posao kompaniji Fabrikam.

U ovom slučaju, Fabrikam će kreirati stavku ponude zasnovanu na proizvodu za robotske ruke i uneće posebnu cenu po jedinici za ovu ponudu. Ta cena se razlikuje od standardne cene robotske ruke kompanije Trey.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
