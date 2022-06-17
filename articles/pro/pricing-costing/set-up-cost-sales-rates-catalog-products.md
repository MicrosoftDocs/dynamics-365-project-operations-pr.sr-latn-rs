---
title: Podešavanje troškova i stopa prodaje za proizvode iz kataloga – jednostavno
description: Ovaj članak pruža informacije o tome kako da podesite trošak i prodajne stope za artikle u katalogu proizvoda.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4689d6929e24ebaa992232f809a7ec60908ee517
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917409"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Podešavanje troškova i stopa prodaje za proizvode iz kataloga – jednostavno

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_


Podešavanje cena za stavke kataloga proizvoda u usluzi Dynamics 365 Project Operations je isto kao i u usluzi Dynamics 365 Sales.

U usluzi Project Operations, proizvodi se ne mogu proceniti ni koristiti u projektima, tako da cene u katalogu proizvoda ne moraju da se podešavaju u cenovnicima projekata za ponude i ugovore.

Koristite polje **Cena proizvoda** ponude, ugovora ili naloga da biste podesili cene u katalogu proizvoda. Ne podešavajte cene u katalogu proizvoda u cenovniku projekta. Cenovnici projekata ekskluzivni su za Project Operations. Poslovna logika specifična za aplikaciju kopira cenovnike iz ponude u ugovor. Rezultat je cenovnik projekta specifičan za ugovor. Operacija kopiranja može odložiti postupak dobijanja ponude ako projektni cenovnik na ponudi postane prevelik. Cenovnici proizvoda se ne kopiraju da bi se kreirali prilagođeni cenovnici po ugovorima. Budući da nije uključeno kopiranje, to ne utiče na performanse procesa ponude.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]