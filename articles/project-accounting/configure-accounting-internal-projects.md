---
title: Konfigurisanje računovodstva za interne projekte
description: Ova tema pruža informacije o tome kako postaviti računovodstvene prakse za interne projekte u usluzi Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 504e7481cb2aee6310cb4ace2d0791d1c7fe360d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083514"
---
# <a name="configure-accounting-for-internal-projects"></a>Konfigurisanje računovodstva za interne projekte

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Interni projekti omogućavaju kompanijama da prate troškove povezane sa aktivnostima koje se ne naplaćuju klijentu. Primeri internih projekata uključuju:

- Razvoj proizvoda, kao što je aplikacija za mobilne uređaje, i praćenje troškova povezanih sa razvojem.
- Upravljanje vremenom i troškovima pretprodaje. Ovaj interni projekat u pretprodaji može se kasnije pretvoriti u naplativi projekat ako se dobije ponuda.

Bilo koji projekat koji nije povezan sa ugovorom u proizvodu Dynamics 365 Project Operations se tretira kao interni. Profili troškova i prihoda projekta ne koriste se za određivanje računovodstvenih pravila za projekat. Interni troškovi projekta se uvek knjiže prema principima dobiti i gubitka. Knjigovodstveni računi za knjiženja definisani su na stranici **Podešavanje knjiženja u knjizi**.

- Vremenske transakcije se knjiže zaduživanjem naloga **Trošak** i kreditiranjem naloga **Raspodela zarada**.
- Transakcije troškova se knjiže zaduživanjem naloga **Cena** i kreditiranjem naloga **Račun za prebijanje dugovanja i potraživanja za troškove**.

Nakon što su transakcije knjižene u projekat, ako je projekat povezan sa projektnim ugovorom, sistem poništava sve akumulirane transakcije i kreira nove naplative transakcije. Transakcije koje se naplaćuju prate računovodstvena pravila definisana u odgovarajućem profilu troškova i prihoda projekta.


