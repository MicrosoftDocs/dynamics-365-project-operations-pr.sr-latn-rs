---
title: Podešavanje troškova i stopa prodaje za proizvode iz kataloga – jednostavno
description: Ova tema pruža informacije o tome kako da postavite stope cena i prodaje za stavke iz kataloga proizvoda.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bfb28e710c7b6da17d94679a72659f81df7a58e376e4bad94b58c36de781b197
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996048"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Podešavanje troškova i stopa prodaje za proizvode iz kataloga – jednostavno

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_


Podešavanje cena za stavke kataloga proizvoda u usluzi Dynamics 365 Project Operations je isto kao i u usluzi Dynamics 365 Sales.

U usluzi Project Operations, proizvodi se ne mogu proceniti ni koristiti u projektima, tako da cene u katalogu proizvoda ne moraju da se podešavaju u cenovnicima projekata za ponude i ugovore.

Koristite polje **Cena proizvoda** ponude, ugovora ili naloga da biste podesili cene u katalogu proizvoda. Ne podešavajte cene u katalogu proizvoda u cenovniku projekta. Cenovnici projekata ekskluzivni su za Project Operations. Poslovna logika specifična za aplikaciju kopira cenovnike iz ponude u ugovor. Rezultat je cenovnik projekta specifičan za ugovor. Operacija kopiranja može odložiti postupak dobijanja ponude ako projektni cenovnik na ponudi postane prevelik. Cenovnici proizvoda se ne kopiraju da bi se kreirali prilagođeni cenovnici po ugovorima. Budući da nije uključeno kopiranje, to ne utiče na performanse procesa ponude.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]