---
title: Uticaj stvarnih vrednosti za interni projekat
description: Ovaj članak pruža informacije o uticaju na tabelu Stvarne vrednosti na različite događaje za interni projekat u usluzi Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: de05714c079fe121ef68e28b1acb82c24bce095e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921365"
---
# <a name="actuals-impact-for-an-internal-project"></a>Uticaj stvarnih vrednosti za interni projekat

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Sledeća tabela navodi stvarne vrednosti različitih tipova transakcija koje se kreiraju na različitim događajima u angažovanju na internom projektu.

| Događaj | Stvarna vrednost troškova | Primer |
|---|---|---|
| Vreme se kreira. | Nije primenjivo | <p>Bob Kozak, iz organizacione jedinice Fabrikam US koja ima stopu cene od 100 američkih dolara (100 USD) na sat, radi na projektu koji nosi ime „Instalacija naoružanja kod firme Adatum“. Ovaj projekat je mapiran na način naplate fiksne cene u predmetu ugovora. Evo primera unosa vremena Boba Kozaka:</p><p>Bob Kozak – 8 sati</p> |
| Vreme je prosleđeno. | Nije primenjivo | Kreira se stavka cene u glavnoj knjizi za stavku vremena. Podrazumevana stopa cene se unosi u stavku knjiženja u glavnoj knjizi. |
| Stavka vremena se opoziva pre nego što je odobrena. | Nije primenjivo | |
| Vreme se odobrava. | Kreira se stvarna vrednost cene. | <p>Nova stvarna vrednost koja je kreirana:</p><ul><li>**Stvarna vrednost cene:** Bob Kozak, 8 sati, 800</li></ul> |
| Odobravanje vremena je otkazano. | <p>Status korekcije originalne stvarne vrednosti troška se ažurira u **Korigovano**.</p><p>Kreirana je stvarna vrednost troška korekcije koja ima status **Nekorigovano**.</p> | <p>Postojeća stvarna vrednost koja se ažurira:</p><ul><li>**Stvarna vrednost cene**: Bob Kozak, 8 sati, 800 USD, *Korigovano*</li></ul><p>Nova stvarna vrednost koja je kreirana za vraćanje prethodnog finansijskog uticaja:</p><ul><li>**Stvarna vrednost cene**: Bob Kozak (8 sati), (800 USD), *Nekorigovano*</li></ul> |
| Stavka vremena se opoziva nakon što je odobrena. | <p>Status korekcije originalne stvarne vrednosti troška se ažurira u **Korigovano**.</p><p>Kreirana je stvarna vrednost troška korekcije koja ima status **Nekorigovano**.</p> | <p>Postojeća stvarna vrednost koja se ažurira:</p><ul><li>**Stvarna vrednost cene**: Bob Kozak, 8 sati, 800 USD, *Korigovano*</li></ul><p>Nova stvarna vrednost koja je kreirana za vraćanje prethodnog finansijskog uticaja:</p><ul><li>**Stvarna vrednost cene**: Bob Kozak (8 sati), (800 USD), *Nekorigovano*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
