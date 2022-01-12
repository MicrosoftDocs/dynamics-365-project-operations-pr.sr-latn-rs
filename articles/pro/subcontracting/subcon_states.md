---
title: Državni prelazi na podizvođačima u projektnim operacijama
description: Ova tema objašnjava stanje prelaza na podizvođačima u korporaciji Microsoft dok Dynamics 365 Project Operations se podizvođači kreiraju, izvršavaju i zatvaraju.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 4ca658440c7a9b29a927098f24c092d72d9eb0c9
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 12/09/2021
ms.locfileid: "7903078"
---
# <a name="state-transitions-on-a-subcontract-in-project-operations"></a>Državni prelazi na podizvođačima u projektnim operacijama

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
