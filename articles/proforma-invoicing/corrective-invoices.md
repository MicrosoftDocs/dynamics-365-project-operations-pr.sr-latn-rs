---
title: Korigovane fakture
description: Ova tema pruža informacije o korigovanim fakturama.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: e14da1c07d5b697de6caf1b9041c30581ecff102
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898098"
---
# <a name="corrected-invoices"></a>Korigovane fakture

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Potvrđene fakture se mogu uređivati. Kada uredite potvrđnu fakturu, kreira se radna verzija korigovane fakture. Pošto je pretpostavka da želite da stornirate sve transakcije i količine iz originalne fakture, ova korigovana faktura uključuje sve transakcije iz originalne fakture, a sve količine na njoj su nula (0).

Kada neke transakcije ne zahtevaju korekciju, možete ih ukloniti iz radne verzije korigovane fakture. Da biste stornirali ili opozvali samo delimičnu količinu, možete urediti polje Količina u detaljima stavke. Ako otvorite detalj stavke fakture, možete videti količinu originalne fakture. Zatim možete da uredite količinu trenutne fakture tako da bude manja ili veća od količine originalne fakture.

Kada potvrdite korigovanu fakturu, stornira se originalna stvarna vrednosti naplaćene prodaje i kreira se nova stvarna vrednost naplaćene prodaje. Ako je količina smanjena, razlika će dovesti do toga da se kreira i nova stvarna vrednost nenaplaćene prodaje. Na primer, ako je originalna naplaćena prodaja bila za osam sati, a detalj stavke korigovane fakture ima manju količinu od šest sati, stornira se prvobitna naplaćena stavka prodaje i kreiraju se dve nove stvarne vrednosti:

- Stvarna vrednosti naplaćene prodaje za šest sati.
- Stvarna vrednosti nenaplaćene prodaje za preostala dva sata. Ova transakcija može biti naplaćena kasnije ili označena kao nenaplativa, u zavisnosti od pregovora sa klijentom.
