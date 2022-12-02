---
title: Greška nepodudaranja valute
description: Ovaj članak pruža informacije o rešavanju problema o grešci nepodudaranja valute do koje dolazi prilikom čuvanja određenih vrsta zapisa.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5b0973a340dec8e68f326803d75bea9803e19791
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914741"
---
# <a name="currency-mismatch-error"></a>Greška nepodudaranja valute 

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Kada sačuvate projekat, ugovor, ponudu ili resurs koji je moguće rezervisati, možda ćete primiti grešku: **Valuta preduzeća-vlasnika ne podudara se sa valutom jedinice ugovaranja. Izaberite drugo preduzeće-vlasnika ili jedinicu ugovaranja za nastavak ugovora za projekat**. Do ovoga je došlo zato što postoji nepodudaranje valute između valute jedinice ugovaranja za zapis i valute preduzeća-vlasnika.


## <a name="resolution"></a>Razrešenje

Da biste zaobilazno rešili ovaj problem, uradite sledeće:
- Proverite valutu ugovorne jedinice za ovaj zapis. Valutu možete videti tako što ćete otvoriti zapis organizacione jedinice i proveriti vrednost na kartici **Opšti podaci** u polju **Valuta**.
- Proverite valutu preduzeća-vlasnika. Valutu možete videti tako što ćete otići do **Srodno** > **Knjige** u zapisu preduzeća. Dvaput kliknite na zapis knjige koji je povezan sa preduzećem i proverite vrednost na kartici **Opšti podaci** u polju **Računovodstvena valuta**.

Ako se valuta postavljena u jedinici za ugovaranje i zapis knjige ne podudaraju, korigujte konfiguraciju ili izaberite druge vrednosti prilikom čuvanja zapisa. Sistem zahteva da se ovi zapisi podudaraju da bi se obezbedili ispravni međukompanijski tokovi fakturisanja. Više informacija o međukompanijskim konfiguracijama potražite u članku [Kreiranje međukompanijskih transakcija](../../project-accounting/create-intercompany-transactions.md).

Ako zapis preduzeća nema pridruženi zapis knjige, to ukazuje da prilikom instaliranja okruženja nedostaje konfiguracija. Konfiguraciju mora da ispravi administrator sistema. Administrator sistema mora da ode na **Konfiguracije dvostrukog upisivanja** i zaustavi i ponovo pokrene **Mapu za dvostruko upisivanje u knjigu** sa početnom sinhronizacijom ove mape i njenim preduslovima. Za više informacija pogledajte [Verzije mapa sa dvostrukim upisivanjem za Project Operations](../../environment/resource-dual-write-maps.md).
