---
title: Podesite troškove i stope prodaje za proizvode iz kataloga
description: Ova tema pruža informacije o tome kako da postavite stope cena i prodaje za stavke iz kataloga proizvoda.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083647"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a>Podesite troškove i stope prodaje za proizvode iz kataloga

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_


Postavljanje cena za stavke kataloga proizvoda u programu Dynamics 365 Project Operations je isto kao u programu Dynamics 365 Sales.

Budući da se proizvodi ne mogu proceniti ili koristiti na projektima u usluzi Project Operations, nema potrebe za postavljanjem cena kataloga proizvoda na cenovnike projekata za ponude i ugovore.

Cene kataloga proizvoda treba postaviti u polju **Cena proizvoda** ponude, ugovora ili naloga. Ne postavljajte cene kataloga proizvoda u cenovnike projekata za ove entitete. Cenovnici projekata ekskluzivni su za Project Operations. Postoji specifična poslovna logika koja kopira cenovnike iz ponude u ugovor. Rezultat je cenovnik projekta specifičan za ugovor. Operacija kopiranja može odložiti postupak dobijanja ponude ako projektni cenovnik na ponudi postane prevelik. Cenovnici proizvoda se ne kopiraju da bi se kreirali prilagođeni cenovnici po ugovorima. To znači da cenovnici proizvoda ne utiču na performanse procesa osvajanja ponuda.
