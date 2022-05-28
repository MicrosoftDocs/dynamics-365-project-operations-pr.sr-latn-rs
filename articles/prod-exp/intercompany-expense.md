---
title: Interni troškovi u okviru preduzeća
description: Ova tema pruža informacije o načinu korišćenja troškova u okviru preduzeća za dodeljivanje troškova radnika pravnom licu za koje je posao obavljen.
author: suvaidya
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6788a590879bd839ebb9dedc45895dc047cc9f15
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684251"
---
# <a name="intercompany-expenses"></a>Međukompanijski troškovi

Radnik koji je zaposlen u jednom pravnom licu u organizaciji može obavljati posao za drugo pravno lice u istoj organizaciji. Možete da koristite troškove u okviru preduzeća za dodeljivanje troškova radnika pravnom licu za koje je posao obavljen. Pravno lice koje zapošljava radnika naziva se pravno lice koje pozajmljuje. Pravno lice za koje radnik snosi troškove naziva se pravno lice kojem se pozajmljuje. 

Da bi radnik mogao da kreira i preda troškove u okviru preduzeća, morate omogućiti redove troškova u okviru preduzeća. Za pravno lice koje pozajmljuje novac, na stranici **Parametri upravljanja troškovima** izaberite **Omogući redove troškova u okviru preduzeća**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Poresko knjiženje za međukompanijske troškove

[!include [banner](../includes/banner.md)]

Da biste u izveštaju o troškovima mogli da koristite poreske grupe koje su povezane sa pravnim licem koje pozajmljuje novac (izvor) umesto sa pravnim licem koje se zadužuje (odredište), morate da omogućite funkcionalnost u podešavanju poreza na promet u glavnoj knjizi. Kada je parametar **Pravno lice za knjiženje poreza u okviru preduzeća** podešen na **Izvor**, a parametar **Primeni pravila oporezivanja poreza na promet** je podešen na **Ne**, koristi se poreska kombinacija za pravno lice koje pozajmljuje novac. Kada je isti parametar postavljen na **Odredište**, koristiće se poreska kombinacija za pravno lice kojem se pozajmljuje. Za pravna lica u Sjedinjenim Državama, kada je parametar postavljen na **Izvor**, polje **Potraživanje poreza na promet** takođe mora biti konfigurisano na novoj stranici **Grupe za knjiženje glavne knjige**. Računovodstveni mehanizam će koristiti podatke iz ovog polja za računovodstveni unos u vezi sa porezom.   
Ponašanje je dosledno za stavke troškova objavljene sa projektom ili bez njega.  

## <a name="new-expense-expression-builder"></a>Nova izrada izraza za troškove

Nova izrada izraza za troškove rešava probleme sa scenarijima troškova unutar preduzeća koji koriste projekte. Ova funkcija obezbeđuje da, kada kreirate trošak unutar preduzeća, politika troškova bude ispravno potvrđena u odnosu na projekat koji je izabran u stavci troškova i da se izveštaj o troškovima može uspešno podneti.

Da bi funkcija alata za izradu izraza za troškove funkcionisala, mora da bude uključena. Osim toga, treba podesiti politiku troškova koja ima ID projekta.

Ako ste već konfigurisali smernice koje potvrđuju ID projekta na stavci troškova, te smernice moraju da se povuku. Zatim možete da uključite funkciju i ponovo konfigurišete smernice.

Da biste uključili ovu funkciju, sledite ove korake.

1. Idite na stavku **Radni prostori** \> **Upravljanje funkcijama**.
2. Na listi izaberite stavku **Nova izrada izraza za troškove za rešavanje problema sa scenarijima troškova unutar preduzeća koji koriste projekte**. Zatim izaberite **Omogući odmah**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
