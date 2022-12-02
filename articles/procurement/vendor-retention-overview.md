---
title: Pregled odlaganja obaveza prema dobavljaču
description: Ovaj članak pruža pregled mogućnosti odlaganja obaveza prema dobavljaču.
author: sigitac
ms.date: 10/01/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 680786f239125905f3b8746cb8318732aa74d9e0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916857"
---
# <a name="vendor-retention-overview"></a>Pregled odlaganja obaveza prema dobavljaču

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Možda će vaša organizacija odložiti deo plaćanja dobavljačima koji rade na projektima za vašu organizaciju. Na primer, pre nego što platite svom dobavljaču, možda biste želeli da se uverite da artikli i usluge koje pružaju ispunjavaju vaša očekivanja.

Kada pregovarate o kupovini projekata sa dobavljačima, možete navesti uslove odlaganja plaćanja dobavljačima koji uključuju procenat ili iznos koji će biti odložen. Kada dobavljač isporuči artikle i usluge, oduzima se određeni procenat zadržavanja ili iznos od vašeg plaćanja dobavljaču. Kada je projekat završen ili dođe u privremenu fazu kako je navedeno u ugovoru sa dobavljačem, oslobađate zadržani iznos i kreirate plaćanje dobavljaču.

## <a name="vendor-retention-example"></a>Primer odlaganja obaveza prema dobavljaču

Sledeći primer prikazuje kako se zadržava procenat iznosa fakture dobavljača na osnovu kompletnog procenta za projekat.

Preduzeće Contoso Robotics USA ugovorilo je sa dobavljačem Fabrikam isporuku 100 sati obuke za projekat obnove opreme. Ukupna vrednost ugovora je 30.000 USD sa ugovorenom otkupnom cenom od 300 USD po satu.

Obuka će se odvijati u tri faze po sledećem rasporedu:

- Faza 1: 50 sati ili 50 procenata projekta
- Faza 2: 30 sati ili ukupno 80 procenata projekta
- Faza 3: 20 sati ili 100 procenata projekta

U sledećoj tabeli navedeni su uslovi odlaganja plaćanja.

| **Procenat isporučenih jedinica** | **Procenat za zadržavanje** | **Procenat za isplatu** |
| --- | --- | --- |
| 50% | 20% | 0% |
| 80% | 10% | 10% |
| 100% | 0% | 100% |

Transakcije rezultiraju sledećim iznosima:

- Faza 1:
  - Iznos za plaćanje je 50 x 300 ili 15.000.
  - Zadržava se 20 procenata iznosa ili 3.000 i biće isplaćeno kasnije.
  - Iznos koji se isplaćuje dobavljaču je 12.000.
- Faza 2:
  - Iznos za plaćanje je 30 x 300 ili 9.000.
  - Zadržava se 10 procenata iznosa ili 900.
  - Isplaćuje se 10 procenata od 3.000 koliko je zadržano u prvoj fazi ili 300.
  - Iznos koji se isplaćuje dobavljaču je 8.400. Ovaj iznos je 9.000 minus 900 zadržanih, plus 300 isplaćenih u fazi 1 zadržavanja.
- Faza 3:
  - Iznos za plaćanje je 20 x 300 ili 6.000.
  - Ništa se ne zadržava.
  - Iznos koji je isplaćen je 3.600. Ovaj iznos se sastoji od 3.000 koje su zadržane u prvoj fazi, minus 300 iz 1. faze isplaćenih u drugoj fazi, plus 900 zadržanih u drugoj fazi.
  - Iznos koji se isplaćuje dobavljaču je 9.600. Ovaj iznos sastoji se od zadržanog iznosa od 3.600 plus 6.000 za završetak 3. faze.

Ukupan iznos isplaćen dobavljaču nakon završetka tri faze je 30.000, što je ukupan iznos narudžbenice (15.000 + 9.000 + 6.000).
