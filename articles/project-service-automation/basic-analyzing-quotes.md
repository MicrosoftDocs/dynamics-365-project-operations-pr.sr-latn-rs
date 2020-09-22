---
title: Analiza ponuda za projekat
description: Ova tema pruža informacije o analizi ponuda za projekat.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 57ac8407-26f5-49dd-97ea-e97642789ff5
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 63c826d27863df62301ec1548fdc94158220c3a2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755107"
---
# <a name="analysis-of-project-quotes"></a>Analiza ponuda za projekat

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation analizira ponude za projekat radi procene profitabilnosti. Takođe analizira koliko je ponuda usaglašena sa očekivanjima klijenta o datumu isporuke ili završetka, kao i sa budžetom.

## <a name="profitability-analysis"></a>Analiza isplativosti

Project Service Automation analizira profitabilnost korišćenjem bruto marže i korigovane bruto marže.

- Bruto marže se izračunavaju pomoću sledeće formule:

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- Korigovana bruto marža se izračunavaju pomoću sledeće formule:

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

Ako se vrednosti bruto marže i korigovane bruto marže značajno razlikuju, veći deo posla u ponudi je klasifikovan kao nenaplativ.

## <a name="analysis-of-customer-expectations"></a>Analiza očekivanja klijenta

Možete analizirati ponude i generisati grafikone za očekivanja klijenata u vezi sa rasporedom i budžetom ako unesete vrednosti za sledeća polja:

- Polje **Zahtevani datum isporuke** u zaglavlju ponude.
- Polje **Budžet klijenta** za svaku stavku ponude (za stavke zasnovane na projektu i stavke zasnovane na proizvodu).

Analiza očekivanja klijenata u vezi sa rasporedom se vrši poređenjem najnovijeg datuma završetka detalja stavke ponude sa zahtevanim datumom isporuke za sve stavke ponude u ponudi.

Analiza očekivanja klijenata u vezi sa budžetom vrši se poređenjem zbira ukupnog budžeta klijenta sa ponuđenim iznosom u svim stavkama ponude.
