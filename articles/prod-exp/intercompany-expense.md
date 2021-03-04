---
title: Interni troškovi u okviru preduzeća
description: Ova tema pruža informacije o načinu korišćenja troškova u okviru preduzeća za dodeljivanje troškova radnika pravnom licu za koje je posao obavljen.
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
ms.openlocfilehash: 553ddbe622210169db8de4aa506dcf1ea1e9d5ef
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960849"
---
# <a name="intercompany-expenses"></a>Međukompanijski troškovi

Radnik koji je zaposlen u jednom pravnom licu u organizaciji može obavljati posao za drugo pravno lice u istoj organizaciji. Možete da koristite troškove u okviru preduzeća za dodeljivanje troškova radnika pravnom licu za koje je posao obavljen. Pravno lice koje zapošljava radnika naziva se pravno lice koje pozajmljuje. Pravno lice za koje radnik snosi troškove naziva se pravno lice kojem se pozajmljuje. 

Da bi radnik mogao da kreira i preda troškove u okviru preduzeća, morate omogućiti redove troškova u okviru preduzeća. Za pravno lice koje pozajmljuje novac, na stranici **Parametri upravljanja troškovima** izaberite **Omogući redove troškova u okviru preduzeća**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Poresko knjiženje za međukompanijske troškove

[!include [banner](../includes/banner.md)]

Da biste u izveštaju o troškovima mogli da koristite poreske grupe koje su povezane sa pravnim licem koje pozajmljuje novac (izvor) umesto sa pravnim licem koje se zadužuje (odredište), morate da omogućite funkcionalnost u podešavanju poreza na promet u glavnoj knjizi. Kada je parametar **Pravno lice za knjiženje poreza u okviru preduzeća** podešen na **Izvor**, a parametar **Primeni pravila oporezivanja poreza na promet** je podešen na **Ne**, koristi se poreska kombinacija za pravno lice koje pozajmljuje novac. Kada je isti parametar postavljen na **Odredište**, koristiće se poreska kombinacija za pravno lice kojem se pozajmljuje. Za pravna lica u Sjedinjenim Državama, kada je parametar postavljen na **Izvor**, polje **Potraživanje poreza na promet** takođe mora biti konfigurisano na novoj stranici **Grupe za knjiženje glavne knjige**. Računovodstveni mehanizam će koristiti podatke iz ovog polja za računovodstveni unos u vezi sa porezom.   
Ponašanje je dosledno za stavke troškova objavljene sa projektom ili bez njega.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]