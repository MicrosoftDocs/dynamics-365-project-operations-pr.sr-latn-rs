---
title: Potvrda fakture dobavljača za projekat
description: Ovaj članak sadrži objašnjenja o tome kako da potvrdite fakturu dobavljača projekta u korporaciji Microsoft Dynamics 365 Project Operations i finansijski uticaj potvrde fakture dobavljača projekta.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4dafbe64e0727957068d68f510202a12871b62aa
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261530"
---
# <a name="confirm-a-project-vendor-invoice"></a>Potvrda fakture dobavljača za projekat

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Nakon što ste verifikovali sve redove na fakturi dobavljača u korporaciji Microsoft, možete Dynamics 365 Project Operations koristiti radnju "Potvrdi" da biste potvrdili fakturu dobavljača.

Kada u fakturi **dobavljača** izaberete opciju "Potvrdi", dešava se sledeće ponašanje:

1. Stanje fakture dobavljača se ažurira u **Potvrđeno**.
2. Potvrđena faktura dobavljača i povezani zapisi postaju samo za čitanje i ne mogu se uređivati ili brisati.
3. Ako neki trošak upućuje na red fakture dobavljača kao deo procesa podudaranja, sve stvarne cene koje su povezane sa referentnim redom fakture dobavljača će biti stornirane.
4. Nove stvarne troškove se kreiraju korišćenjem informacija u redu fakture dobavljača.
5. Nakon potvrde fakture dobavljača, više ne možete kreirati korektivne naloge, opoziv stavki procesa ili otkazati odobravanje originalnog vremena, troškova ili materijalnih stvarnih stavki koje su stornirane.

> [!NOTE]
> Ako bilo koji red u fakturi dobavljača ima status verifikacije koji nije **dovršen**, faktura dobavljača ne može biti potvrđena.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
