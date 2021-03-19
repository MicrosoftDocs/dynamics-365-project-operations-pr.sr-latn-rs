---
title: Korigovane fakture
description: Ova tema pruža informacije o korigovanim fakturama.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 734dc01e15339a31ac21f92bb3fb20d634a075ad
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287840"
---
# <a name="corrected-invoices"></a>Korigovane fakture

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Potvrđene fakture se mogu uređivati. Kada uredite potvrđnu fakturu, kreira se radna verzija korigovane fakture. Pošto je pretpostavka da želite da stornirate sve transakcije i količine iz originalne fakture, ova korigovana faktura uključuje sve transakcije iz originalne fakture, a sve količine na njoj su nula (0).

Kada neke transakcije ne zahtevaju korekciju, možete ih ukloniti iz radne verzije korigovane fakture. Da biste stornirali ili opozvali samo delimičnu količinu, možete urediti polje Količina u detaljima stavke. Ako otvorite detalj stavke fakture, možete videti količinu originalne fakture. Zatim možete da uredite količinu trenutne fakture tako da bude manja ili veća od količine originalne fakture.

Kada potvrdite korigovanu fakturu, stornira se originalna stvarna vrednosti naplaćene prodaje i kreira se nova stvarna vrednost naplaćene prodaje. Ako je količina smanjena, razlika će dovesti do toga da se kreira i nova stvarna vrednost nenaplaćene prodaje. Na primer, ako je originalna naplaćena prodaja bila za osam sati, a detalj stavke korigovane fakture ima manju količinu od šest sati, stornira se prvobitna naplaćena stavka prodaje i kreiraju se dve nove stvarne vrednosti:

- Stvarna vrednosti naplaćene prodaje za šest sati.
- Stvarna vrednosti nenaplaćene prodaje za preostala dva sata. Ova transakcija može biti naplaćena kasnije ili označena kao nenaplativa, u zavisnosti od pregovora sa klijentom.


[!INCLUDE[footer-include](../includes/footer-banner.md)]