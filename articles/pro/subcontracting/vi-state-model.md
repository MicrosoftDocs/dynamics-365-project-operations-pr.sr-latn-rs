---
title: Državni prelazi na fakturi dobavljača
description: Ova tema objašnjava državne prelaze u fakturi dobavljača u korporaciji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7efb52621ee325d5025dfad0b45218d1fe20a063
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584705"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Državni prelazi na fakturi dobavljača

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Ova tema objašnjava državne prelaze u fakturi dobavljača u korporaciji Microsoft Dynamics 365 Project Operations. Koriste se sledeće države: "Radna **verzija",** "U **pregledu", "** Potvrđeno **",** **"Na čekanju**" i "Otkazano **"**.

Sledeće ilustracije prikazuju državne tranzicije.

![Model tranzicije stanja podizvođaja.](../media/VI_State_Model.jpg)

Sledeća tabela sadrži objašnjenja o tome šta svaka država predstavlja u životnom ciklusu fakture dobavljača u operacijama projekta.

| Stanje | Opis | Dozvoljeni prelazi |
| --- | --- | --- |
| Radna verzija | Ovo stanje je početno stanje fakture dobavljača. Redovi i cene podležu izmenama. Faktura dobavljača u ovom stanju se može uređivati i brisati. | U toku je |
| Pregleda se | Ovo stanje predstavlja stanje obrade fakture dobavljača. Najmanje jedan red fakture dobavljača ima status verifikacije u **toku**. | Potvrđeno, na čekanju |
| Potvrđeno | Ovo stanje predstavlja fazu fakture dobavljača u kojoj je zatvaranje kreiralo stvarne troškove za svaki red fakture dobavljača. Sve povezane stvarne troškove koje su se podudarale sa redovima fakture dobavljača su stornirane i zamenjene stvarnim troškovima iz tih redova fakture dobavljača. Faktura dobavljača u ovom stanju ne može da se uređuje ili briše. Dugme "Otkaži" možete **koristiti** da biste otkazali potvrđenu fakturu dobavljača. Radnja "Otkaži" poništava uticaj radnje "Potvrdi". | Otkazana |
| Na čekanju | <p>Ovo stanje predstavlja fazu fakture dobavljača u kojoj faktura dobavljača ne može da se premesti zbog problema sa fakturom ili statusom dobavljača. Faktura dobavljača u ovom stanju ne može biti potvrđena, otkazana, uređena ili izbrisana.</p><p>Radnju "Ponovo otvori" možete koristiti za premeštanje fakture dobavljača u radno **ili** in **review** stanje. Ako najmanje jedan red u fakturi dobavljača ima status provere "U **toku**" ili "**Dovršeno**", faktura dobavljača će biti ponovo otvorena u stanju **"U pregledu**". Ako svi redovi u fakturi dobavljača imaju status provere statusa "Nije započeto **", faktura** dobavljača će biti ponovo otvorena u radnoj **verziji stanja**.</p> | Radna verzija, u recenziji |
| Otkazana | Ovo stanje predstavlja fazu podizvođača u kojoj stvarna isporuka materijala i/ili rad pomoću resursa podizvođača više nije potreban. Podizvođači u ovoj državi ne mogu da se koriste za procenu i korišćenje projekta osoblja za resurse i materijale, a takođe se ne mogu pominjati na vreme, troškove i korišćenje materijala na projektu. Podizvođači u ovom stanju ne mogu da se uređuju ili brišu. | Nijedno |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]