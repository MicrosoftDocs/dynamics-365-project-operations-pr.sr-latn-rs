---
title: Potvrda faktura dobavljača projekta
description: Ovaj članak sadrži objašnjenja o tome kako da potvrdite fakturu dobavljača projekta u korporaciji Microsoft Dynamics 365 Project Operations i opisuje finansijski uticaj potvrde fakture dobavljača projekta.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475493"
---
# <a name="confirm-project-vendor-invoices"></a>Potvrda faktura dobavljača projekta

**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha

Kada je omogućena **ručna potvrda od strane pm parametra**, fakture dobavljača koje su kreirane u programu imaju Microsoft Dataverse status radne **verzije**. Fakture dobavljača koje su kreirane na ovaj način moraju biti redigovane i ručno potvrđene. Kada je **parametar "Ručno potvrđivanje od** strane premijera" onemogućen, fakture dobavljača koje su kreirane Dataverse automatski se potvrđuju. Nije potrebna dalja akcija. 

Kada verifikišete sve redove u fakturi dobavljača u, kliknite na dugme Dynamics 365 Project Operations Potvrdi da **biste** potvrdili fakturu dobavljača.

Kada u fakturi **dobavljača** izaberete opciju "Potvrdi", dešava se sledeće ponašanje:

1. Status fakture dobavljača se ažurira u **Potvrđeno**.
1. Potvrđena faktura dobavljača i povezani zapisi postaju samo za čitanje i ne mogu se uređivati ili brisati.
1. Ako neki trošak upućuje na red fakture dobavljača kao deo procesa podudaranja, sve stvarne cene koje su povezane sa referentnim redom fakture dobavljača će biti stornirane.
1. Nove stvarne troškove se kreiraju korišćenjem informacija u redu fakture dobavljača.
1. Više ne možete kreirati naloge ispravki, obrađivati opozive vremena ili otkazati odobravanje originalnog vremena, troškova ili materijalnih stvarnih stavki koje su stornirane.
1. U Dynamics 365 Finance, vrednost troška **projekta** se ažurira korišćenjem naloga za integraciju sa projektom, a konto *integracije sa nabavkama se storniran* nakon knjiženja naloga integracije projekta.

> [!NOTE]
> Ako bilo koji red u fakturi dobavljača ima status verifikacije koji nije **dovršen**, faktura dobavljača ne može biti potvrđena.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
