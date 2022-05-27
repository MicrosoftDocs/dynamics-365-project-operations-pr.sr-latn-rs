---
title: Stvarni uticaj na angažovanje fiksne cene
description: Ova tema pruža informacije o uticaju na tabelu "Stvarne stvari" na različite događaje tokom životnog ciklusa angažovanja fiksne cene u korporaciji Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 222e7c5eefd7c619e4d7389cdaff2f96176ff275
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579245"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Stvarni uticaj na angažovanje fiksne cene

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Sledeća tabela navodi stvarne vrste transakcija koje se kreiraju na različitim događajima u angažovanju fiksne cene.

| Događaj | Stvarna vrednost troškova | Stvarna vrednost nenaplaćene prodaje | Fakturisana prodaja stvarna | Primer |
|---|---|---|---|---|
| Vreme je stvoreno. | Nije primenjivo | Nije primenjivo | Nije primenjivo | <p>Bob Kozak, iz američke organizacione jedinice Fabrikam koja ima stopu troškova od 100 američkih dolara (100 USD) na sat, radi na projektu koji nosi ime "Instalacija naoružanja na Adatumu". Ovaj projekat je mapiran na način naplate fiksne cene u redu ugovora. Evo uzorka vremena od Boba Kozaka:</p><p>Bob Kozak - 8 sati</p> |
| Vreme se podnosi. | Nije primenjivo | Nije primenjivo | Nije primenjivo | Za stavku vremena kreira se red naloga troškova. Podrazumevana stopa troška se unosi u stavku naloga. |
| Stavka vremena je opozvana pre nego što je odobrena. | Nije primenjivo | Nije primenjivo | Nije primenjivo | |
| Vreme je odobreno. | Kreira se stvarni trošak. | Nije primenjivo | Nije primenjivo | <p>Nova stvarna koja je kreirana:</p><ul><li>**Trošak aktuelan:** Bob Kozak, 8 hr, USD 800</li></ul> |
| Odobravanje vremena je otkazano. | <p>Status korekcije originalnog troška se ažurira u "Korigovano **"**.</p><p>Kreiran je stvarni trošak storniranja koji ima status korekcije **"Neodustivo"**.</p> | Nije primenjivo | Nije primenjivo | <p>Postojeći stvarni koji se ažurira:</p><ul><li>**Trošak aktuelan:** Bob Kozack, 8 hr, USD 800, *Korigovano*</li></ul><p>Nova stvarna koja je kreirana da bi se preokrenuo prethodni finansijski uticaj:</p><ul><li>**Trošak aktuelan:** Bob Kozack, (8 hr), (USD 800), *Neuništiv*</li></ul> |
| Stavka vremena je opozvana nakon što je odobrena. | <p>Status korekcije originalnog troška se ažurira u "Korigovano **"**.</p><p>Kreiran je stvarni trošak storniranja koji ima status korekcije **"Neodustivo"**.</p> | Nije primenjivo | Nije primenjivo | <p>Postojeći stvarni koji se ažurira:</p><ul><li>**Trošak aktuelan:** Bob Kozack, 8 hr, USD 800, *Korigovano*</li></ul><p>Nova stvarna koja je kreirana da bi se preokrenuo prethodni finansijski uticaj:</p><ul><li>**Trošak aktuelan:** Bob Kozack, (8 hr), (USD 800), *Neuništiv*</li></ul> |
| Ugovor je potvrđen. | <p>Status korekcije starih stvarnih troškova se ažurira u "Korigovano **"**.</p><p>Kreiraju se stvarni troškovi storniranja koji imaju status korekcije **"Neodustivo"**.</p><p>Novi troškovi se kreiraju nakon ponovnog revalorizacije ugovornih pravila.</p> | Nije primenjivo | Nije primenjivo | <p>Postojeći stvarni koji se ažurira:</p><ul><li>**Trošak aktuelan:** Bob Kozack, 8 hr, USD 800, *Korigovano*</li></ul><p>Nova stvarna koja je kreirana da bi se preokrenuo prethodni finansijski uticaj:</p><ul><li>**Trošak aktuelan:** Bob Kozack, (8 hr), (USD 800), *Neuništiv*</li></ul><p>Nova stvarna koja je kreirana za revalorizovani finansijski uticaj:</p><ul><li>**Trošak aktuelan:** Bob Kozak, 8 hr, USD 800</li></ul> |
| Faktura je kreirana. | Nije primenjivo | Nije primenjivo | Nije primenjivo | |
| Faktura je potvrрena prekretnicom. | Nije primenjivo | Nije primenjivo | Kreiraju se nove stvarne prodaje zasnovane na prekretnici. | <p>Postojeći stvarni koji ostaje nepromenjen:</p><ul><li>**Trošak aktuelan:** Bob Kozak, 8 hr, USD 800</li></ul><p>Nova stvarna koja je kreirana za zapisivanje naloženih vrednosti prodaje:</p><ul><li>**Prodaja na naplati stvarna:** Prekretnica, USD 5,000</li></ul> |
| Faktura je ispravljena da bi se pripisala prekretnica. | Nije primenjivo | Nije primenjivo | Kreiraju se aktueli fakturisane prodaje. | <p>Postojeći stvarni koji ostaje nepromenjen:</p><ul><li>**Trošak aktuelan:** Bob Kozak, 8 hr, 800 USD</li></ul><p>Postojeći stvarni koji se ažurira:</p><ul><li>**Prodaja na naplati stvarna:** Prekretnica, USD 5,000, *Korigovano*</li></ul><p>Nova stvarna koja je kreirana da bi se stornlele prethodne fakturisane vrednosti prodaje:</p><ul><li>**Prodaja na naplati stvarna:** Prekretnica, (5.000 USD), *Neodustavljivo*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
