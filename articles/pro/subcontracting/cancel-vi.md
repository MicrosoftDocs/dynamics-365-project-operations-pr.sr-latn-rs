---
title: Otkazivanje fakture dobavljača projekta
description: Ova tema objašnjenja o tome kako da otkažete fakturu dobavljača projekta u korporaciji Microsoft Dynamics 365 Project Operations i finansijski uticaj otkazivanja fakture dobavljača projekta.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 87f6bdca30c5779e3d70922e75609ff4cdfca167
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580657"
---
# <a name="cancel-a-project-vendor-invoice"></a>Otkazivanje fakture dobavljača projekta

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
