---
title: Procene resursa
description: Ova tema pruža informacije o tome kako se izračunavaju procene resursa u usluzi Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: f255b2cbf290973ce62fe2c1c121bd1df15a7392
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3928602"
---
# <a name="resource-estimates"></a>Procene resursa

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Procene resursa potiču iz angažovanja u vremenu koje je definisano u strukturnoj analizi posla zajedno sa primenljivim dimenzijama za određivanje cena. Tipično, proračun je **satnica za svaku ulogu x broj sati.** Angažovanje u vremenu za svaki resurs uskladišteno je u zapisu o dodeli resursa. Određivanje cena se skladišti u unapred definisanom cenovniku. Konverzija jedinica primenjuje se na osnovu važećeg cenovnika.

![Procene resursa](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Podrazumevana cena koštanja i valuta troškova

Cene troškova podrazumevano dolaze iz organizacione jedinice.

## <a name="default-bill-rate-and-sales-currency"></a>Podrazumevana stopa naplate i prodajna valuta

Prodajne cene se primenjuju jednom po pogodbi. Hijerarhija prodajnog cenovnika podrazumevano je sledeća:

1. Organizacija
2. Klijent
3. Ponuda/ugovor
