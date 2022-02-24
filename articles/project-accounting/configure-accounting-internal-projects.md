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
ms.openlocfilehash: 65d05e3a6321dc32aee55c28b3eaa4bd0bae2f86
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/06/2021
ms.locfileid: "5857995"
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
