---
title: Promene statusa podugovora
description: Ovaj članak sadrži objašnjenja o prelazima stanja na podizvođač u korporaciji Microsoft Dynamics 365 Project Operations dok se podizvođač kreira, izvršava i zatvara.
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

Ovaj članak sadrži objašnjenja o prelazima stanja na podizvođač u korporaciji Microsoft Dynamics 365 Project Operations. Svaka država je predstavljena kao radna verzija, potvrđena, zatvorena ili otkazana. Sledeća slika predstavlja državne prelaze.

![Model stanja podizvođači](../media/SubconStates.png)  

Sledeća tabela daje opis onoga što svaka država predstavlja u životnom ciklusu podizvođaka u operacijama projekta.

| Stanje | Opis | Dozvoljeni prelazi |
| --- | --- | --- |
| Radna verzija | Ovo predstavlja početno stanje podizvođaka. Pregovori sa dobavljačem su u toku. Redovi i cene podležu izmenama. Podizvođači u ovom stanju mogu da se koriste za procenu i osoblje projektnih zahteva za resurse i materijale. Takođe se može referencizovati na vreme, troškove i upotrebu materijala na projektu. Podizvođači u ovom stanju mogu da se uređuju i brišu. | Potvrđeno |
| Potvrđeno | Ovo predstavlja fazu podizvođače nakon dovršavanja pregovora sa dobavljačem o cenama i predmetima koji se nabavljuju. Međutim, stvarna isporuka materijala i/ili rada po podizvođačima resursa još uvek traje. Podizvođači u ovom stanju mogu da se koriste za procenu i osoblje projektnih zahteva za resurse i materijale. Takođe se može referencizovati na vreme, troškove i upotrebu materijala na projektu. Podizvođači u ovom stanju se ne mogu uređivati ili brisati. Dugme **"Otkaži** " vam omogućava da otkažete potvrđeni podizvođač. Dugme " **Ponovo otvori"** vam omogućava da ponovo otvorite podizvođač da biste ga vratili u status radne **verzije**. Koristite dugme **"** Zatvori" da biste zatvorili potvrđeni podizvođač. | Zatvoreno <br> Otkazana <br> Radna verzija |
| Zatvoreno | Ovo predstavlja fazu podizvođača kada se stvarna isporuka materijala i/ili rada po podizvođačim resursima dovrši. Podizvođači u ovom stanju više ne mogu da se koriste za procenu i osoblje projektnih zahteva za resurse i materijale. Takođe, više se ne može upućivati na vreme, troškove i upotrebu materijala na projektu. Podizvođači u ovom stanju se ne mogu uređivati ili brisati. | Nijedno |
| Otkazana | Ovo predstavlja fazu podizvođača kada stvarna isporuka materijala i/ili rada po resursima podizvođača više nije potrebna. Podizvođači u ovom stanju ne mogu da se koriste za procenu i korišćenje projekta osoblja za resurse i materijale, niti se mogu referencizovati na vreme, troškove i korišćenje materijala na projektu. Podizvođači u ovom stanju se ne mogu uređivati ili brisati. | Nijedno |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
