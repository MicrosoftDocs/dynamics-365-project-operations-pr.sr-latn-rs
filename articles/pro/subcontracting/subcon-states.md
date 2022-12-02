---
title: Promene statusa podugovora
description: Ovaj članak objašnjava prelate statusa na podugovoru u usluzi Microsoft Dynamics 365 Project Operations dok se podugovor kreira, izvršava i zatvara.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2804fc30f8dade42dc1093e5fc0f01fa1db22ca3
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522952"
---
# <a name="state-transitions-on-a-subcontract"></a>Promene statusa podugovora 

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Ovaj članak sadrži objašnjenja o prelazima statusa na podugovoru u rešenju Microsoft Dynamics 365 Project Operations. Svaki status je predstavljen kao radna verzija, potvrđeno, zatvoreno ili otkazano. Sledeća slika predstavlja prelaze statusa.

![Model statusa podugovora](../media/SubconStates.png)  

Sledeća tabela sadrži opis šta svaki status predstavlja u životnom ciklusu podugovora u usluzi Project Operations.

| Stanje | Opis | Dozvoljeni prelasci |
| --- | --- | --- |
| Radna verzija | Ovo predstavlja početni status podugovora. Pregovori sa dobavljačem su u toku. Redovi i cene podležu izmenama. Podugovor u ovom status može da se koristi za procenu i zahteve za osobljem na projektu za resurse i materijale. Takođe može biti referenca za vreme, trošak i korišćenje materijala na projektu. Podugovor sa ovim statusom ne može se uređivati i izbrisati. | Potvrđeno |
| Potvrđeno | Ovo predstavlja fazu podugovora nakon dovršavanja pregovora sa dobavljačem o određivanju cenama i artiklima koji se nabavljaju. Međutim, stvarna isporuka materijala i/ili rada prema podugovorenim resursima još uvek traje. Podugovor u ovom status može da se koristi za procenu i zahteve za osobljem na projektu za resurse i materijale. Takođe može biti referenca za vreme, trošak i korišćenje materijala na projektu. Podugovor sa ovim statusom ne može se uređivati ili izbrisati. Dugme **Otkaži** vam omogućava da otkažete potvrđeni podugovor. Dugme **Ponovo otvori** vam omogućava da ponovo otvorite podugovor da biste ga vratili u status **Radna verzija** . Koristite dugme **Zatvori** da biste zatvorili potvrđeni podugovor. | Zatvoreno <br> Otkazana <br> Radna verzija |
| Zatvoreno | Ovao predstavlja fazu podugovora kada je stvarna isporuka materijala i/ili rad pomoću resursa podugovora dovršena. Podugovor u ovom status ne može više da se koristi za procenu i zahteve za osobljem na projektu za resurse i materijale. Takođe, više ne može biti referenca za vreme, trošak i korišćenje materijala na projektu. Podugovor sa ovim statusom ne može se uređivati ili izbrisati. | Nijedno |
| Otkazana | Ovao predstavlja fazu podugovora kada je stvarna isporuka materijala i/ili rad pomoću resursa podugovora više nisu potrebni. Podugovor u ovom status ne može da se koristi za procenu i zahteve za osoblja na projektu za resurse i materijale niti može da upućuje na korišćenje vremena, troškova i materijala na projektu. Podugovor sa ovim statusom ne može se uređivati ili izbrisati. | Nijedno |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
