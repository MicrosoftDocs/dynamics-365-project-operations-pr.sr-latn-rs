---
title: Konfigurisanje računovodstva za interne projekte
description: Ova tema pruža informacije o tome kako postaviti računovodstvene prakse za interne projekte u usluzi Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9f1cc75b12fec81d726e46f8d970dcfe030f6b29
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287615"
---
# <a name="configure-accounting-for-internal-projects"></a>Konfigurisanje računovodstva za interne projekte

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Interni projekti omogućavaju kompanijama da prate troškove povezane sa aktivnostima koje se ne naplaćuju klijentu. Primeri internih projekata uključuju:

- Razvoj proizvoda, kao što je aplikacija za mobilne uređaje, i praćenje troškova povezanih sa razvojem.
- Upravljanje vremenom i troškovima pretprodaje. Ovaj interni projekat u pretprodaji može se kasnije pretvoriti u naplativi projekat ako se dobije ponuda.

Bilo koji projekat koji nije povezan sa ugovorom u usluzi Dynamics 365 Project Operations tretira se kao interni. Profili troškova i prihoda projekta ne koriste se za određivanje računovodstvenih pravila za projekat. Interni troškovi projekta se uvek knjiže prema principima dobiti i gubitka. Knjigovodstveni računi za knjiženja definisani su na stranici **Podešavanje knjiženja u knjizi**.

- Vremenske transakcije se knjiže zaduživanjem naloga **Trošak** i kreditiranjem naloga **Raspodela zarada**.
- Transakcije troškova se knjiže zaduživanjem naloga **Cena** i kreditiranjem naloga **Račun za prebijanje dugovanja i potraživanja za troškove**.

Nakon što su transakcije knjižene u projekat, ako je projekat povezan sa projektnim ugovorom, sistem poništava sve akumulirane transakcije i kreira nove naplative transakcije. Transakcije koje se naplaćuju prate računovodstvena pravila definisana u odgovarajućem profilu troškova i prihoda projekta.




[!INCLUDE[footer-include](../includes/footer-banner.md)]