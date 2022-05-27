---
title: Stvarni uticaj na interni projekat
description: Ovaj tema informacije o uticaju na tabelu "Stvarne stvari" na različitim događajima za interni projekat u korporaciji Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 66a9ac4d2f56ae95313ed6731c3e51926105cff7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579783"
---
# <a name="actuals-impact-for-an-internal-project"></a>Stvarni uticaj na interni projekat

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Sledeća tabela navodi stvarne različite vrste transakcija koje se kreiraju na različitim događajima u internom projektnom angažovanju.

| Događaj | Stvarna vrednost troškova | Primer |
|---|---|---|
| Vreme je stvoreno. | Nije primenjivo | <p>Bob Kozak, iz američke organizacione jedinice Fabrikam koja ima stopu troškova od 100 američkih dolara (100 USD) na sat, radi na projektu koji nosi ime "Instalacija naoružanja na Adatumu". Ovaj projekat je mapiran na način naplate fiksne cene u redu ugovora. Evo uzorka vremena od Boba Kozaka:</p><p>Bob Kozak - 8 sati</p> |
| Vreme se podnosi. | Nije primenjivo | Za stavku vremena kreira se red naloga troškova. Podrazumevana stopa troška se unosi u stavku naloga. |
| Stavka vremena je opozvana pre nego što je odobrena. | Nije primenjivo | |
| Vreme je odobreno. | Kreira se stvarni trošak. | <p>Nova stvarna koja je kreirana:</p><ul><li>**Trošak aktuelan:** Bob Kozak, 8 hr, USD 800</li></ul> |
| Odobravanje vremena je otkazano. | <p>Status korekcije originalnog troška se ažurira u "Korigovano **"**.</p><p>Kreiran je stvarni trošak storniranja koji ima status korekcije **"Neodustivo"**.</p> | <p>Postojeći stvarni koji se ažurira:</p><ul><li>**Trošak aktuelan:** Bob Kozack, 8 hr, USD 800, *Korigovano*</li></ul><p>Nova stvarna koja je kreirana da bi se preokrenuo prethodni finansijski uticaj:</p><ul><li>**Trošak aktuelan:** Bob Kozack, (8 hr), (USD 800), *Neuništiv*</li></ul> |
| Stavka vremena je opozvana nakon što je odobrena. | <p>Status korekcije originalnog troška se ažurira u "Korigovano **"**.</p><p>Kreiran je stvarni trošak storniranja koji ima status korekcije **"Neodustivo"**.</p> | <p>Postojeći stvarni koji se ažurira:</p><ul><li>**Trošak aktuelan:** Bob Kozack, 8 hr, USD 800, *Korigovano*</li></ul><p>Nova stvarna koja je kreirana da bi se preokrenuo prethodni finansijski uticaj:</p><ul><li>**Trošak aktuelan:** Bob Kozack, (8 hr), (USD 800), *Neuništiv*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
