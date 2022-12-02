---
title: Potvrda fakture dobavljača za projekat
description: Ovaj članak objašnjava kako da potvrdite fakturu dobavljača na projektu u rešenju Microsoft Dynamics 365 Project Operations i finansijski uticaj potvrde fakture dobavljača na projektu.
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

Nakon što ste verifikovali sve stavke na fakturi dobavljača u rešenju Microsoft Dynamics 365 Project Operations, možete da koristite radnju Potvrdi da biste potvrdili fakturu dobavljača.

Kada na fakturi dobavljača izaberete **Potvrdi**, dolazi do sledećeg ponašanja:

1. Status fakture dobavljača se ažurira na **Potvrđeno**.
2. Potvrđena faktura dobavljača i povezani zapisi postaju samo za čitanje i nije ih moguće uređivati ili brisati.
3. Ako neka stvarna vrednost cene upućuje na stavku na fakturi dobavljača kao deo procesa podudaranja, sve stvarne vrednosti cene koje su povezane sa stavkom na fakturi dobavljača biće stornirane.
4. Nove stvarne vrednosti cene se kreiraju korišćenjem informacija u stavci na fakturi dobavljača.
5. Nakon potvrde fakture dobavljača, više ne možete kreirati korektivne naloge, opozive stavki vremena obrade ili otkazati odobrenje prvobitnog vremena, troškova ili materijalnih stvarnih vrednosti koje su stornirane.

> [!NOTE]
> Ako bilo koji red na fakturi dobavljača ima status verifikacije koji nije **Dovršen**, faktura dobavljača ne može biti potvrđena.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
