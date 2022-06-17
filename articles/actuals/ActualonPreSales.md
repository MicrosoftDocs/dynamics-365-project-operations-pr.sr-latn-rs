---
title: Stvarni uticaj u pred-prodajnoj fazi angažovanja
description: Ovaj članak pruža informacije o uticaju na tabelu "Stvarne stvari" na različitim događajima dok je engagment u fazi pre prodaje u korporaciji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d03d6ac2154806189d0d9d0b232bb317f51071ba
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922377"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Stvarni uticaj u pred-prodajnoj fazi angažovanja

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Sledeća tabela navodi stvarne vrste transakcija koje se kreiraju na različitim događajima tokom faze pre prodaje projektnog angažovanja.

| Događaj | Stvarna vrednost troškova | Primer |
|---|---|---|
| Vreme je stvoreno. | Nije primenjivo | <p>Bob Kozak, iz američke organizacione jedinice Fabrikam koja ima stopu troškova od 100 američkih dolara (100 USD) na sat, radi na projektu koji nosi ime "Instalacija naoružanja na Adatumu". Ovaj projekat je mapiran na način naplate fiksne cene u redu ugovora. Evo uzorka vremena od Boba Kozaka:</p><p>Bob Kozak - 8 sati</p> |
| Vreme se podnosi. | Nije primenjivo | Za stavku vremena kreira se red naloga troškova. Podrazumevana stopa troška se unosi u stavku naloga. |
| Stavka vremena je opozvana pre nego što je odobrena. | Nije primenjivo | |
| Vreme je odobreno. | Kreira se stvarni trošak. | <p>Nova stvarna koja je kreirana:</p><ul><li>**Trošak aktuelan:** Bob Kozak, 8 hr, USD 800</li></ul> |
| Odobravanje vremena je otkazano. | <p>Status korekcije originalnog troška se ažurira u "Korigovano **"**.</p><p>Kreiran je stvarni trošak storniranja koji ima status korekcije **"Neodustivo"**.</p> | <p>Postojeći stvarni koji se ažurira:</p><ul><li>**Trošak aktuelan:** Bob Kozack, 8 hr, USD 800, *Korigovano*</li></ul><p>Nova stvarna koja je kreirana da bi se preokrenuo prethodni finansijski uticaj:</p><ul><li>**Trošak aktuelan:** Bob Kozack, (8 hr), (USD 800), *Neuništiv*</li></ul> |
| Stavka vremena je opozvana nakon što je odobrena. | <p>Status korekcije originalnog troška se ažurira u "Korigovano **"**.</p><p>Kreiran je stvarni trošak storniranja koji ima status korekcije **"Neodustivo"**.</p> | <p>Postojeći stvarni koji se ažurira:</p><ul><li>**Trošak aktuelan:** Bob Kozack, 8 hr, USD 800, *Korigovano*</li></ul><p>Nova stvarna koja je kreirana da bi se preokrenuo prethodni finansijski uticaj:</p><ul><li>**Trošak aktuelan:** Bob Kozack, (8 hr), (USD 800), *Neuništiv*</li></ul> |
| Ponuda se osvaja i kreira se ugovor. | <p>Status korekcije starih stvarnih troškova se ažurira u "Korigovano **"**.</p><p>Kreiraju se stvarni troškovi storniranja koji imaju status korekcije **"Neodustivo"**.</p><p>Novi troškovi se kreiraju nakon ponovnog revalorizacije ugovornih pravila.</p> | <p>Postojeći stvarni koji se ažurira:</p><ul><li>**Trošak aktuelan:** Bob Kozack, 8 hr, USD 800, *Korigovano*</li></ul><p>Nova stvarna koja je kreirana da bi se preokrenuo prethodni finansijski uticaj:</p><ul><li>**Trošak aktuelan:** Bob Kozack, (8 hr), (USD 800), *Neuništiv*</li></ul><p>Nove stvarne stvari koje su kreirane za revalorizovani finansijski uticaj kada se ponuda osvoji i kada se kreira ugovor:</p><ul><li>**Trošak aktuelan:** Bob Kozak, 8 hr, USD 800</li><li>**Neželjena prodaja stvarna:** Bob Kozack, 8 hr, USD 1,600</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
