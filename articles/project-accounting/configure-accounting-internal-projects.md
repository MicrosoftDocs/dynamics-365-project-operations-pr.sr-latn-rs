---
title: Konfigurisanje računovodstva za interne projekte
description: Ova tema pruža informacije o tome kako postaviti računovodstvene prakse za interne projekte u usluzi Project Operations.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: be1dcd1b6b18591c99c904e0013d9870c7cafe1077fa6e9634f2e9f495190848
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005543"
---
# <a name="configure-accounting-for-internal-projects"></a>Konfigurisanje računovodstva za interne projekte

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Interni projekti omogućavaju kompanijama da prate troškove povezane sa aktivnostima koje se ne naplaćuju klijentu. Primeri internih projekata uključuju:

- Razvoj proizvoda, kao što je aplikacija za mobilne uređaje, i praćenje troškova povezanih sa razvojem.
- Upravljanje vremenom i troškovima pretprodaje. Ovaj interni projekat u pretprodaji može se kasnije pretvoriti u naplativi projekat ako se dobije ponuda.

Bilo koji projekat koji nije povezan sa ugovorom u usluzi Dynamics 365 Project Operations tretira se kao interni. Profili troškova i prihoda projekta ne koriste se za određivanje računovodstvenih pravila za projekat. Interni troškovi projekta se uvek knjiže prema principima dobiti i gubitka. Knjigovodstveni računi za knjiženja definisani su na stranici **Podešavanje knjiženja u knjizi**.

- Vremenske transakcije se knjiže zaduživanjem naloga **Trošak** i kreditiranjem naloga **Raspodela zarada**.
- Transakcije troškova se knjiže zaduživanjem naloga **Cena** i kreditiranjem naloga **Račun za prebijanje dugovanja i potraživanja za troškove**.
- Transakcije stavki knjiže se zaduživanjem na računu **Cena** i potraživanjem na računu **Cena – Stavka**.

Nakon što su transakcije knjižene u projekat, ako je projekat povezan sa projektnim ugovorom, sistem poništava sve akumulirane transakcije i kreira nove naplative transakcije. Transakcije koje se naplaćuju prate računovodstvena pravila definisana u odgovarajućem profilu troškova i prihoda projekta.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
