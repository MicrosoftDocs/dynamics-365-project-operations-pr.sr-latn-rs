---
title: Uticaj stvarnih vrednosti na angažovanje po fiksnoj ceni
description: Ovaj članak pruža informacije o uticaju na tabelu Stvarne vrednosti na različite događaje tokom životnog ciklusa angažovanja po fiksnoj ceni u usluzi Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 50819d77d56935bfe5438d7d9dae99562bcc0b49
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918145"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Uticaj stvarnih vrednosti na angažovanje po fiksnoj ceni

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Sledeća tabela navodi stvarne vrednosti različitih tipova transakcija koje se kreiraju na različitim događajima u angažovanju po fiksnoj ceni.

| Događaj | Stvarna vrednost troškova | Stvarna vrednost nenaplaćene prodaje | Stvarna vrednost naplaćene prodaje | Primer |
|---|---|---|---|---|
| Vreme se kreira. | Nije primenjivo | Nije primenjivo | Nije primenjivo | <p>Bob Kozak, iz organizacione jedinice Fabrikam US koja ima stopu cene od 100 američkih dolara (100 USD) na sat, radi na projektu koji nosi ime „Instalacija naoružanja kod firme Adatum“. Ovaj projekat je mapiran na način naplate fiksne cene u predmetu ugovora. Evo primera unosa vremena Boba Kozaka:</p><p>Bob Kozak – 8 sati</p> |
| Vreme je prosleđeno. | Nije primenjivo | Nije primenjivo | Nije primenjivo | Kreira se stavka cene u glavnoj knjizi za stavku vremena. Podrazumevana stopa cene se unosi u stavku knjiženja u glavnoj knjizi. |
| Stavka vremena se opoziva pre nego što je odobrena. | Nije primenjivo | Nije primenjivo | Nije primenjivo | |
| Vreme se odobrava. | Kreira se stvarna vrednost cene. | Nije primenjivo | Nije primenjivo | <p>Nova stvarna vrednost koja je kreirana:</p><ul><li>**Stvarna vrednost cene:** Bob Kozak, 8 sati, 800</li></ul> |
| Odobravanje vremena je otkazano. | <p>Status korekcije originalne stvarne vrednosti troška se ažurira u **Korigovano**.</p><p>Kreirana je stvarna vrednost troška korekcije koja ima status **Nekorigovano**.</p> | Nije primenjivo | Nije primenjivo | <p>Postojeća stvarna vrednost koja se ažurira:</p><ul><li>**Stvarna vrednost cene**: Bob Kozak, 8 sati, 800 USD, *Korigovano*</li></ul><p>Nova stvarna vrednost koja je kreirana za vraćanje prethodnog finansijskog uticaja:</p><ul><li>**Stvarna vrednost cene**: Bob Kozak (8 sati), (800 USD), *Nekorigovano*</li></ul> |
| Stavka vremena se opoziva nakon što je odobrena. | <p>Status korekcije originalne stvarne vrednosti troška se ažurira u **Korigovano**.</p><p>Kreirana je stvarna vrednost troška korekcije koja ima status **Nekorigovano**.</p> | Nije primenjivo | Nije primenjivo | <p>Postojeća stvarna vrednost koja se ažurira:</p><ul><li>**Stvarna vrednost cene**: Bob Kozak, 8 sati, 800 USD, *Korigovano*</li></ul><p>Nova stvarna vrednost koja je kreirana za vraćanje prethodnog finansijskog uticaja:</p><ul><li>**Stvarna vrednost cene**: Bob Kozak (8 sati), (800 USD), *Nekorigovano*</li></ul> |
| Ugovor je potvrđen. | <p>Status korekcije starih stvarnih vrednosti cene se ažurira u **Korigovano**.</p><p>Stvarne vrednosti cene korekcije se kreiraju koje imaju status korekcije u **Nekorigovano**.</p><p>Nove stvarne vrednosti cene se kreiraju nakon ponovne procene ugovornih pravila.</p> | Nije primenjivo | Nije primenjivo | <p>Postojeća stvarna vrednost koja se ažurira:</p><ul><li>**Stvarna vrednost cene**: Bob Kozak, 8 sati, 800 USD, *Korigovano*</li></ul><p>Nova stvarna vrednost koja je kreirana za vraćanje prethodnog finansijskog uticaja:</p><ul><li>**Stvarna vrednost cene**: Bob Kozak (8 sati), (800 USD), *Nekorigovano*</li></ul><p>Nova stvarna vrednost koja je kreirana za ponovo procenjeni finansijski uticaj:</p><ul><li>**Stvarna vrednost cene:** Bob Kozak, 8 sati, 800</li></ul> |
| Faktura se kreira. | Nije primenjivo | Nije primenjivo | Nije primenjivo | |
| Faktura je potvrđena kontrolnom tačkom. | Nije primenjivo | Nije primenjivo | Kreiraju se nove stvarne vrednosti naplaćene prodaje zasnovane na kontrolnoj tački. | <p>Postojeća stvarna vrednost koja ostaje nepromenjena:</p><ul><li>**Stvarna vrednost cene:** Bob Kozak, 8 sati, 800</li></ul><p>Nova stvarna vrednost koja je kreirana za evidentiranje vrednosti naplaćene prodaje:</p><ul><li>**Stvarna vrednost naplaćene ponude:** Kontrolna tačka, 5.000 USD</li></ul> |
| Faktura je korigovana da bi se zadužilo za kontrolnu tačku. | Nije primenjivo | Nije primenjivo | Kreiraju se stvarne vrednosti storniranja naplaćene prodaje. | <p>Postojeća stvarna vrednost koja ostaje nepromenjena:</p><ul><li>**Stvarna vrednost cene:** Bob Kozak, 8 sati, 800 USD</li></ul><p>Postojeća stvarna vrednost koja se ažurira:</p><ul><li>**Stvarna vrednost naplaćene ponude**: Kontrolna tačka, 5.000 USD. *Prilagođeno*</li></ul><p>Nova stvarna vrednost koja je kreirana za evidentiranje storniranje prethodne vrednosti naplaćene prodaje:</p><ul><li>**Stvarna vrednost naplaćene ponude**: Kontrolna tačka (5.000 USD),*Neprilagođeno*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
