---
title: Uticaj stvarnih vrednosti u pretprodajnoj fazi angažovanja
description: Ovaj članak pruža informacije o uticaju na tabelu Stvarne vrednosti na različite događaje dok je angažovanje u fazi pretprodaje u usluzi Microsoft Dynamics 365 Project Operations.
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
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Uticaj stvarnih vrednosti u pretprodajnoj fazi angažovanja

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Sledeća tabela navodi stvarne vrednosti različitih tipova transakcija koje se kreiraju na različitim događajima tokom faze pretprodaje u angažovanju na projektu.

| Događaj | Stvarna vrednost troškova | Primer |
|---|---|---|
| Vreme se kreira. | Nije primenjivo | <p>Bob Kozak, iz organizacione jedinice Fabrikam US koja ima stopu cene od 100 američkih dolara (100 USD) na sat, radi na projektu koji nosi ime „Instalacija naoružanja kod firme Adatum“. Ovaj projekat je mapiran na način naplate fiksne cene u predmetu ugovora. Evo primera unosa vremena Boba Kozaka:</p><p>Bob Kozak – 8 sati</p> |
| Vreme je prosleđeno. | Nije primenjivo | Kreira se stavka cene u glavnoj knjizi za stavku vremena. Podrazumevana stopa cene se unosi u stavku knjiženja u glavnoj knjizi. |
| Stavka vremena se opoziva pre nego što je odobrena. | Nije primenjivo | |
| Vreme se odobrava. | Kreira se stvarna vrednost cene. | <p>Nova stvarna vrednost koja je kreirana:</p><ul><li>**Stvarna vrednost cene:** Bob Kozak, 8 sati, 800</li></ul> |
| Odobravanje vremena je otkazano. | <p>Status korekcije originalne stvarne vrednosti troška se ažurira u **Korigovano**.</p><p>Kreirana je stvarna vrednost troška korekcije koja ima status **Nekorigovano**.</p> | <p>Postojeća stvarna vrednost koja se ažurira:</p><ul><li>**Stvarna vrednost cene**: Bob Kozak, 8 sati, 800 USD, *Korigovano*</li></ul><p>Nova stvarna vrednost koja je kreirana za vraćanje prethodnog finansijskog uticaja:</p><ul><li>**Stvarna vrednost cene**: Bob Kozak (8 sati), (800 USD), *Nekorigovano*</li></ul> |
| Stavka vremena se opoziva nakon što je odobrena. | <p>Status korekcije originalne stvarne vrednosti troška se ažurira u **Korigovano**.</p><p>Kreirana je stvarna vrednost troška korekcije koja ima status **Nekorigovano**.</p> | <p>Postojeća stvarna vrednost koja se ažurira:</p><ul><li>**Stvarna vrednost cene**: Bob Kozak, 8 sati, 800 USD, *Korigovano*</li></ul><p>Nova stvarna vrednost koja je kreirana za vraćanje prethodnog finansijskog uticaja:</p><ul><li>**Stvarna vrednost cene**: Bob Kozak (8 sati), (800 USD), *Nekorigovano*</li></ul> |
| Ponuda je osvojena i kreira se ugovor. | <p>Status korekcije starih stvarnih vrednosti cene se ažurira u **Korigovano**.</p><p>Stvarne vrednosti cene korekcije se kreiraju koje imaju status korekcije u **Nekorigovano**.</p><p>Nove stvarne vrednosti cene se kreiraju nakon ponovne procene ugovornih pravila.</p> | <p>Postojeća stvarna vrednost koja se ažurira:</p><ul><li>**Stvarna vrednost cene**: Bob Kozak, 8 sati, 800 USD, *Korigovano*</li></ul><p>Nova stvarna vrednost koja je kreirana za vraćanje prethodnog finansijskog uticaja:</p><ul><li>**Stvarna vrednost cene**: Bob Kozak (8 sati), (800 USD), *Nekorigovano*</li></ul><p>Nove stvarne vrednosti koje su kreirane za ponovo evaluirani finansijski uticaj kada se ponuda osvoji i kada se kreira ugovor:</p><ul><li>**Stvarna vrednost cene:** Bob Kozak, 8 sati, 800</li><li>**Stvarna vrednost nenaplaćene prodaje:** Bob Kozak, 8 č, 1.600 USD</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
