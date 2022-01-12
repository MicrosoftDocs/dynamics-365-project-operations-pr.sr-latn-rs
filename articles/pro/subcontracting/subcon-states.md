---
title: Državni prelazi na podizvođačima
description: Ova tema objašnjava stanje prelazi na podizvođaи u korporaciji Microsoft dok Dynamics 365 Project Operations se podizvoрaи kreira, izvršava i zatvara.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d67f4a3cd834c25462304c2d75c824427fcbd034
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903756"
---
# <a name="state-transitions-on-a-subcontract"></a>Državni prelazi na podizvođačima 

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Ova tema objašnjava stanje prelaza na podizvođačima u korporaciji Microsoft Dynamics 365 Project Operations. Svaka država je predstavljena kao radna verzija, potvrđena, zatvorena ili otkazana. Sledeća slika predstavlja državne prelaze.

![Model stanja podizvođači](../media/SubconStates.png)  

Sledeća tabela daje opis onoga što svaka država predstavlja u životnom ciklusu podizvođaka u operacijama projekta.

| Stanje | Opis | Dozvoljeni prelazi |
| --- | --- | --- |
| Radna verzija | Ovo predstavlja početno stanje podizvođaka. Pregovori sa dobavljačem su u toku. Redovi i cene podležu izmenama. Podizvođači u ovom stanju mogu da se koriste za procenu i osoblje projektnih zahteva za resurse i materijale. Takođe se može referencizovati na vreme, troškove i upotrebu materijala na projektu. Podizvođači u ovom stanju mogu da se uređuju i brišu. | Potvrđeno |
| Potvrđeno | Ovo predstavlja fazu podizvođače nakon dovršavanja pregovora sa dobavljačem o cenama i predmetima koji se nabavljuju. Međutim, stvarna isporuka materijala i/ili rada po podizvođačima resursa još uvek traje. Podizvođači u ovom stanju mogu da se koriste za procenu i osoblje projektnih zahteva za resurse i materijale. Takođe se može referencizovati na vreme, troškove i upotrebu materijala na projektu. Podizvođači u ovom stanju se ne mogu uređivati ili brisati. Dugme **·** "Otkaži" vam omogućava da otkažete potvrđeni podizvođač. Dugme **"Ponovo** otvori" vam omogućava da ponovo otvorite podizvođač da biste ga vratili u status radne **verzije**. Koristite **dugme** "Zatvori" da biste zatvorili potvrđeni podizvođač. | Zatvoreno <br> Otkazana <br> Radna verzija |
| Zatvoreno | Ovo predstavlja fazu podizvođača kada se stvarna isporuka materijala i/ili rada po podizvođačim resursima dovrši. Podizvođači u ovom stanju više ne mogu da se koriste za procenu i osoblje projektnih zahteva za resurse i materijale. Takođe, više se ne može upućivati na vreme, troškove i upotrebu materijala na projektu. Podizvođači u ovom stanju se ne mogu uređivati ili brisati. | Nijedno |
| Otkazana | Ovo predstavlja fazu podizvođača kada stvarna isporuka materijala i/ili rada po resursima podizvođača više nije potrebna. Podizvođači u ovom stanju ne mogu da se koriste za procenu i korišćenje projekta osoblja za resurse i materijale, niti se mogu referencizovati na vreme, troškove i korišćenje materijala na projektu. Podizvođači u ovom stanju se ne mogu uređivati ili brisati. | Nijedno |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
