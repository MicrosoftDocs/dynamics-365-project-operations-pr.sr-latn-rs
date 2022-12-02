---
title: Otkazivanje fakture dobavljača za projekat
description: Ovaj članak objašnjava kako da otkažete fakturu dobavljača na projektu u rešenju Microsoft Dynamics 365 Project Operations i finansijski uticaj otkazivanja fakture dobavljača na projektu.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 79d00a91f9ab2d66eab2f80349d6f1fba1934f94
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261108"
---
# <a name="cancel-a-project-vendor-invoice"></a>Otkazivanje fakture dobavljača za projekat

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Nakon potvrde fakture dobavljača, ne možete je uređivati ili brisati. Ako je došlo do greške u fakturi dobavljača koja je potvrđena, možete koristiti radnju „Otkaži“ da biste stornirali uticaj fakture dobavljača i kreirali novu fakturu dobavljača.

Kada na fakturi dobavljača izaberete **Otkaži**, dolazi do sledećeg ponašanja:

1. Status fakture dobavljača se ažurira na **Otkazano**.
2. Otkazana faktura dobavljača i povezani zapisi postaju samo za čitanje i nije ih moguće uređivati ili brisati.
3. Sve stvarne vrednosti cene koje su kreirane na osnovu redova na fakturi dobavljača kao deo potvrde fakture dobavljača se storniraju.
4. Ako su neke stvarne vrednosti cene bile povezane sa redovima na fakturi dobavljača kao deo procesa podudaranja, potvrda prvobitne fakture dobavljača ih je stornirala. Tokom otkazivanja fakture dobavljača, te stvarne vrednosti cene se ponovo kreiraju. Poreklo ukazuju na stavke vremena, troškova ili korišćenja materijala.
5. Nakon otkazivanja fakture dobavljača, opet možete kreirati korektivne naloge, opozive stavki vremena obrade i otkazati odobrenje prvobitnog vremena, troškova ili materijalnih stvarnih vrednosti.

> [!NOTE]
> Samo potvrđene fakture prodavaca za projekat mogu da budu otkazane. Fakture dobavljača u drugim statusima se ne mogu otkazati.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
