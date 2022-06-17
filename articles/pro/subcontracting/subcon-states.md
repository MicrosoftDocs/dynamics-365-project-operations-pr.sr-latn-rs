---
title: Promene statusa podugovora
description: Ovaj članak sadrži objašnjenja o prelazima stanja na podizvođač u korporaciji Microsoft Dynamics 365 Project Operations dok se podizvođač kreira, izvršava i zatvara.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b41e3d44a17c51778dd850c7d4a48351a5d44554
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919755"
---
# <a name="state-transitions-on-a-subcontract"></a>Promene statusa podugovora 

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

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
