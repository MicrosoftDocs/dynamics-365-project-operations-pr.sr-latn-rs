---
title: Greška u nepodudaranju valute
description: Ova tema informacije o nepodudaranju valuta do kojih dolazi kada sačuvate određene vrste zapisa.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 52e33ad3728e1a393e8c7e3ca4e0a4b506d0b774
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903762"
---
# <a name="currency-mismatch-error"></a>Greška u nepodudaranju valute 

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Kada sačuvate projekat, ugovor, ponudu ili knjigovodstveni resurs, možete dobiti grešku, **posedovanje valute preduzeća se ne podudara sa valutom ugovaranja jedinice. Izaberite drugo preduzeće ili jedinicu za ugovaranje da biste nastavili**. Do ovoga je došlo zato što postoji nepodudaranje valute između valute ugovaranja za zapis i valute preduzeća u vlasništvu.


## <a name="resolution"></a>Razrešenje

Da biste zaobiљli ovaj problem, uradite sledeжe:
- Proverite valutu ugovorne jedinice za ovaj zapis. Valutu možete videti tako što ćete otvoriti zapis organizacione jedinice i proveriti vrednost na **kartici** "Opšte postavke" u **polju** "Valuta".
- Proverite valutu preduzeća u vlasništvu. Valutu možete videti tako što ćete **u** > **zapisu preduzeća** ići u "Srodne knjige". Dvaput kliknite na zapis knjige koji je povezan sa preduzećem i proverite vrednost na kartici Opšte **postavke** u polju **Obračunska** valuta.

Ako se valuta postavljena u jedinici za ugovaranje i zapis knjige ne podudaraju, korigujte konfiguraciju ili izaberite različite vrednosti prilikom čuvanja zapisa. Sistem zahteva da se ovi zapisi podudaraju da bi se obezbedili ispravni međukompanijski tokovi fakturisanja. Više informacija o međukompanijskim konfiguracijama potražite u [članku Kreiranje međukompanijskih transakcija](../../project-accounting/create-intercompany-transactions.md).

Ako zapis preduzeća nema pridruženi zapis knjige, to ukazuje na to da prilikom podešavanja okruženja nedostaje konfiguracija. Konfiguraciju mora da ispravi administrator sistema. Administrator sistema mora da ode **na konfiguracije sa dva** pisanja i zaustavi i ponovo pokrene **Mapu za dvostruko pisanje sa** početnom sinhronizacijom ove mape i to su preduslovi. Za više informacija pogledajte [Verzije mapa sa dvostrukim upisivanjem za Project Operations](../../environment/resource-dual-write-maps.md).