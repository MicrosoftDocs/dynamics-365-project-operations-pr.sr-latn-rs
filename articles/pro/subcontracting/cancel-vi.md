---
title: Otkazivanje fakture dobavljača za projekat
description: Ovaj članak sadrži objašnjenja o tome kako da otkažete fakturu dobavljača projekta u korporaciji Microsoft Dynamics 365 Project Operations i finansijski uticaj otkazivanja fakture dobavljača projekta.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7ddaadc0f6e336a8ba67bb4ad8000f7e894f3eb0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911567"
---
# <a name="cancel-a-project-vendor-invoice"></a>Otkazivanje fakture dobavljača za projekat

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Nakon potvrde fakture dobavljača, ona se ne može uređivati ili brisati. Ako je došlo do greške u fakturi dobavljača koja je potvrđena, možete koristiti radnju "Otkaži" da biste stornličili uticaj fakture dobavljača i kreirali novu fakturu dobavljača.

Kada u fakturi **dobavljača** izaberete opciju "Otkaži", dešava se sledeće ponašanje:

1. Stanje fakture dobavljača se ažurira u **Otkazano**.
2. Otkazana faktura dobavljača i povezani zapisi postaju samo za čitanje i ne mogu se uređivati ili brisati.
3. Sve stvarne cene koje su kreirane na osnovu redova fakture dobavljača kao deo potvrde fakture dobavljača su stornirane.
4. Ako su neki stvarni troškovi bili povezani sa redovima fakture dobavljača kao deo procesa podudaranja, originalna potvrda fakture dobavljača ih je stornnula. Tokom otkazivanja fakture dobavljača, ti troškovi se ponovo kreiraju. Poreklo ukazuju na stavke vremena, troškova ili korišćenja materijala.
5. Nakon otkazivanja fakture dobavljača, možete ponovo kreirati korektivne naloge, obraditi opozive stavki vremena i otkazati odobravanje originalnog vremena, troškova ili materijalnih stvarnih stavki.

> [!NOTE]
> Samo potvrđene fakture dobavljača projekta mogu biti otkazane. Fakture dobavljača u drugim državama se ne mogu otkazati.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
