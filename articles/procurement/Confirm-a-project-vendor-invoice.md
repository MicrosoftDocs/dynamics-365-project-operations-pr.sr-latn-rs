---
title: Potvrda faktura dobavljača za projekat
description: Ovaj članak objašnjava kako da potvrdite fakturu dobavljača na projektu u rešenju Microsoft Dynamics 365 Project Operations i opisuje finansijski uticaj potvrde fakture dobavljača na projektu.
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
# <a name="confirm-project-vendor-invoices"></a>Potvrda faktura dobavljača za projekat

**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha

Kada je omogućen parametar **Ručna potvrda od strane projektnog menadžera**, fakture dobavljača koje su kreirane u programu Microsoft Dataverse imaju status **Radna verzija**. Fakture dobavljača koje su kreirane na ovaj način moraju biti pregledane i ručno potvrđene. Kada je onemogućen parametar **Ručna potvrda od strane projektnog menadžera**, fakture dobavljača koje su kreirane u programu Dataverse automatski se potvrđuju. Nije potrebna dodatna radnja. 

Nakon što ste verifikovali sve stavke na fakturi dobavljača u rešenju Microsoft Dynamics 365 Project Operations, izaberite **Potvrdi** da biste potvrdili fakturu dobavljača.

Kada na fakturi dobavljača izaberete **Potvrdi**, dolazi do sledećeg ponašanja:

1. Status fakture dobavljača se ažurira na **Potvrđeno**.
1. Potvrđena faktura dobavljača i povezani zapisi postaju samo za čitanje i nije ih moguće uređivati ili brisati.
1. Ako neka stvarna vrednost cene upućuje na stavku na fakturi dobavljača kao deo procesa podudaranja, sve stvarne vrednosti cene koje su povezane sa stavkom na fakturi dobavljača biće stornirane.
1. Nove stvarne vrednosti cene se kreiraju korišćenjem informacija u stavci na fakturi dobavljača.
1. Više ne možete kreirati korektivne naloge, opozive procesa stavki vremena ili otkazati odobrenje prvobitnog vremena, troškova ili materijalnih stvarnih vrednosti koje su stornirane.
1. U sistemu Dynamics 365 Finance, vrednost **Cena projekta** se ažurira korišćenjem dnevnika za integraciju projekta, a konto integracije sa nabavkama se *stornira* nakon knjiženja dnevnika integracije projekta.

> [!NOTE]
> Ako bilo koji red na fakturi dobavljača ima status verifikacije koji nije **Dovršen**, faktura dobavljača ne može biti potvrđena.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
