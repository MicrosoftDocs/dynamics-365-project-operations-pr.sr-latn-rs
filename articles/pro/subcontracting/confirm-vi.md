---
title: Potvrda fakture dobavljača za projekat
description: Ovaj članak sadrži objašnjenja o tome kako da potvrdite fakturu dobavljača projekta u korporaciji Microsoft Dynamics 365 Project Operations i finansijski uticaj potvrde fakture dobavljača projekta.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 092b3cd5981f7d9bb8767c7a2acb2f4952801d06
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932451"
---
# <a name="confirm-a-project-vendor-invoice"></a>Potvrda fakture dobavljača za projekat

[!include [banner](../../includes/dataverse-preview.md)]

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
