---
title: Promene statusa na fakturi dobavljača
description: Ovaj članak sadrži objašnjenja o prelazima statusa na fakturi dobavljača u rešenju Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e25e4d63d4c9098112a7f40abe60c7184018d582
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261061"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Promene statusa na fakturi dobavljača

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Ovaj članak sadrži objašnjenja o prelazima statusa na fakturi dobavljača u rešenju Microsoft Dynamics 365 Project Operations. Koriste se sledeći statusi: **Radna verzija**, **U pregledu**, **Potvrđeno**, **Obustavljeno** i **Otkazano**.

Sledeće ilustracije prikazuju prelaze statusa.

![Model prelaska statusa podugovora.](../media/VI_State_Model.jpg)

Sledeća tabela sadrži objašnjenja o tome šta svaki status predstavlja u životnom ciklusu fakture dobavljača u Project Operations.

| Stanje | Opis | Dozvoljeni prelasci |
| --- | --- | --- |
| Radna verzija | Ovaj status je početni status fakture dobavljača. Redovi i cene podležu izmenama. Faktura dobavljača sa ovim statusom može se uređivati i izbrisati. | U obradi |
| Pregleda se | Ovaj status predstavlja status obrade fakture dobavljača. Najmanje jedan red fakture dobavljača ima status verifikacije **U toku**. | Potvrđeno, obustavljeno |
| Potvrđeno | Ovaj status predstavlja fazu fakture dobavljača u kojoj je aplikacija kreirala stvarne vrednosti cene za svaki red na fakturi dobavljača. Sve povezane stvarne vrednosti cena koje su se podudarale sa redovima na fakturi dobavljača su stornirane i zamenjene stvarnim vrednostima cena iz tih redova na fakturi dobavljača. Fakture dobavljača sa ovim statusom ne mogu se uređivati ili izbrisati. Možete koristiti dugme **Otkaži** da biste otkazali potvrđenu fakturu dobavljača. Radnja otkazivanja stornira uticaj radnje Potvrdi. | Otkazana |
| Na čekanju | <p>Ovaj status predstavlja fazu fakture dobavljača u kojoj faktura dobavljača ne može da se premesti zbog problema sa fakturom ili statusom dobavljača. Faktura dobavljača u ovom statusu ne može da se potvrdi, otkaže, uredi ili izbriše.</p><p>Možete da koristite radnju Ponovo otvori da biste premestili fakturu dobavljača u status **Radna verzija** ili **U pregledu**. Ako najmanje jedan red na fakturi dobavljača ima status provere **U toku** ili **Dovršeno**, faktura dobavljača će biti ponovo otvorena u statusu **U pregledu**. Ako svi redovi na fakturi dobavljača imaju status provere **Nije započeto**, faktura dobavljača će biti ponovo otvorena u statusu **Radna verzija**.</p> | Radna verzija, U pregledu |
| Otkazana | Ovaj status predstavlja fazu podugovora u kojoj stvarna isporuka materijala i/ili rad pomoću resursa podugovora više nije potrebna. Podugovor u ovom status ne može da se koristi za procenu i zahteve za osoblja na projektu za resurse i materijale, a takođe ne može da upućuje na vreme, troškove i korišćenje materijala na projektu. Podugovor sa ovim statusom ne može se uređivati ili izbrisati. | Nijedno |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
