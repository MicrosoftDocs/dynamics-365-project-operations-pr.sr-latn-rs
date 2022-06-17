---
title: Analiza ponuda za projekat
description: Ovaj članak pruža informacije o analizi ponuda za projekat.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 9db924c16c5eca17e7962ff1d88b09e581347fa5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919295"
---
# <a name="analysis-of-project-quotes"></a>Analiza ponuda za projekat

[!include [banner](../includes/psa-now-project-operations.md)]

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
