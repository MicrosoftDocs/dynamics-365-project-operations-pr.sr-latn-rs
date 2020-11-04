---
title: Međukompanijski troškovi
description: Radnik koji je zaposlen u jednom pravnom licu u organizaciji može obavljati posao za drugo pravno lice u istoj organizaciji. U ovoj situaciji možete da koristite funkciju troškova u okviru preduzeća za dodeljivanje troškova radnika pravnom licu za koje je posao izveden.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083731"
---
# <a name="intercompany-expenses"></a>Međukompanijski troškovi

[!include [banner](../includes/banner.md)]

Radnik koji je zaposlen u jednom pravnom licu u organizaciji može obavljati posao za drugo pravno lice u istoj organizaciji. U ovoj situaciji možete da koristite funkciju troškova u okviru preduzeća za dodeljivanje troškova radnika pravnom licu za koje je posao izveden. Pravno lice koje zapošljava radnika naziva se pravno lice koje pozajmljuje. Pravno lice za koje radnik snosi troškove naziva se pravno lice kojem se pozajmljuje. 

Pre nego što radnik može kreirati i podneti troškove za rad koji se obavlja za drugo pravno lice, u pravnom licu koje pozajmljuje, na stranici **Parametri upravljanja troškovima** izaberite **Omogućite stavke troškova u okviru preduzeća**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Poresko knjiženje za međukompanijske troškove

[!include [banner](../includes/banner.md)]

Ako u izveštaju o troškovima želite da koristite poreske grupe koje su povezane sa pravnim licem koje pozajmljuje (izvorno pravno lice) umesto sa pravnim licem kojem se pozajmljuje (odredišno pravno lice), moraćete to da konfigurišete u podešavanju poreza na promet u glavnoj knjizi. Kada je parametar glavne knjige **Pravno lice za poresko knjiženje u okviru preduzeća** podešen na **Izvor** i opcija **Primeni pravila oporezivanja za porez na promet** podešena na **Ne** , koristiće se kombinacija poreza za pravno lice koje pozajmljuje. Kada je isti parametar postavljen na **Odredište** , koristiće se poreska kombinacija za pravno lice kojem se pozajmljuje. Za pravna lica u Sjedinjenim Državama, kada je parametar postavljen na **Izvor** , polje **Potraživanje poreza na promet** takođe mora biti konfigurisano na novoj stranici **Grupe za knjiženje glavne knjige**. Računovodstveni mehanizam će koristiti podatke iz ovog polja za računovodstveno knjiženje u vezi sa porezom.   
Ponašanje je dosledno za stavke troškova objavljene sa projektom ili bez njega.  
