---
title: Podešavanje troškova i stopa prodaje za proizvode iz kataloga – jednostavno
description: Ova tema pruža informacije o tome kako da postavite stope cena i prodaje za stavke iz kataloga proizvoda.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176718"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Podešavanje troškova i stopa prodaje za proizvode iz kataloga – jednostavno

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_


Postavljanje cena za stavke kataloga proizvoda u programu Dynamics 365 Project Operations je isto kao u programu Dynamics 365 Sales.

Budući da se proizvodi ne mogu proceniti ili koristiti na projektima u usluzi Project Operations, nema potrebe za postavljanjem cena kataloga proizvoda na cenovnike projekata za ponude i ugovore.

Cene kataloga proizvoda treba postaviti u polju **Cena proizvoda** ponude, ugovora ili naloga. Ne postavljajte cene kataloga proizvoda u cenovnike projekata za ove entitete. Cenovnici projekata ekskluzivni su za Project Operations. Postoji specifična poslovna logika koja kopira cenovnike iz ponude u ugovor. Rezultat je cenovnik projekta specifičan za ugovor. Operacija kopiranja može odložiti postupak dobijanja ponude ako projektni cenovnik na ponudi postane prevelik. Cenovnici proizvoda se ne kopiraju da bi se kreirali prilagođeni cenovnici po ugovorima. To znači da cenovnici proizvoda ne utiču na performanse procesa osvajanja ponuda.
