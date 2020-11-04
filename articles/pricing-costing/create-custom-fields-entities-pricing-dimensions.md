---
title: Kreiranje prilagođenih polja i entiteta kao dimenzije za određivanje cena
description: Ova tema pruža informacije o tome kako da kreirate prilagođene skupove opcija ili entitete.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083618"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Kreiranje prilagođenih polja i entiteta kao dimenzije za određivanje cena

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Obavite sledeće korake kada želite da kreirate prilagođeni skup opcija ili entitet.

> [!IMPORTANT]
> Preporučuje se da se sve promene dimenzije prilagođene cene unose u odvojenom rešenju. Ova važna najbolja praksa pruža fleksibilnost u budućnosti za ažuriranje ili uklanjanje promena po potrebi, pomoći će pri ponovnoj upotrebi posla i olakšava prilagođavanje ovih promena drugoj instanci. Nakon što unesete sve potrebne promene, izvezite ovo rešenje kao **Kompletno rešenje** i uvezite ga u druge instance da biste ponovo koristili podešavanje cena.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Kreiranje prilagođenog rešenja za dimenzije za određivanje cena
1. Idite na **Podešavanja** > **Rešenja** , a zatim izaberite **Novo** da biste kreirali novo rešenje. 
2. Imenujte rešenje, **\<your organization name> dimenzije za određivanje cena** , unesite preostale zahtevane informacije, a zatim izaberite **Sačuvaj**.
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Kreiranje prilagođenih polja i skupova opcija u rešenju za dimenzije određivanja cena

Dimenzija određivanja cena može biti skup opcija ili entitet. I jedno i drugo morate da kreirate u rešenju za određivanje cena. Koraci u ovoj proceduri objašnjavaju kako da kreirate dimenzije zasnovane na entitetima i dimenzije zasnovane na skupu opcija.

### <a name="entity-based-dimensions"></a>Dimenzije zasnovane na entitetima

1. Idite na **Podešavanja** > **Rešenja** , a zatim dvaput kliknite na **\<your organization name> dimenzije za određivanje cena**.
2. U levom oknu za navigaciju istraživača rešenja izaberite **Entiteti**.
3. Izaberite **Novo** da biste kreirali novi entitet pod nazivom **Standardna pozicija**. 
4. Unesite preostale potrebne informacije, a zatim izaberite **Sačuvaj**.


### <a name="option-set-based-dimensions"></a>Dimenzije zasnovane na skupu opcija 
Možete kreirati dve dimenzije zasnovane na skupovima opcija. Pomoću polja **Radna lokacija resursa** pratite cenu radne lokacije **Kod kuće** i **Na lokaciji** i koristite **Radno vreme resursa** sa vrednostima **Standardno** i **Prekovremeno** da biste primenili proviziju kada se posao završi.


1. Idite na **Podešavanja** > **Rešenja** , a zatim dvaput kliknite na **\<your organization name> dimenzije za određivanje cena**. 
2. U levom oknu za navigaciju istraživača rešenja izaberite **Skupovi opcija**. 
3. Izaberite **Novo** da biste kreirali novi skup opcija, unesite preostale zahtevane informacije, a zatim izaberite **Sačuvaj**.

## <a name="create-data-for-entity-based-dimensions"></a>Kreiranje podataka za dimenzije zasnovane na entitetima

Možete ručno kreirati podatke za dimenzije zasnovane na entitetima ili korišćenjem Microsoft Excel poziva za uvoz ili usluge. Koristite korake iz ove procedure da biste kreirali dve standardne pozicije, **Inženjer sistema** i **Viši inženjer sistema** iz dimenzije zasnovane na entitetima **Standardna pozicija**. Ako je obim podataka koje želite da kreirate mali, kao u sledećem primeru, možete da koristite standardni obrazac.

1. Izaberite **Napredna pretraga** , izaberite entitet **Standardni naslov** , a zatim izaberite **Rezultati**. Biće prikazani svi redovi u entitetu **Standardna pozicija**.
2. Izaberite **Novo** , a zatim u polje **Ime** unesite „Inženjer sistema“ i izaberite **Sačuvaj**.
3. Zatvorite obrazac. 
4. Ponovite korake 1-3 da biste kreirali još jednu standardnu poziciji „Viši inženjer sistema“.

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Dodajte sve zahtevane entitete i srodne komponente u rešenje za dimenzije određivanja cena
Moraćete da dodate sledeće entitete u rešenje za određivanje cena. Korake u ovoj proceduri koristite da biste napravili neke važne promene šema u rešenju za određivanje cena, tako da entiteti postanu svesni novih dimenzija određivanja cena.

1. Izaberite **Podešavanja** > **Rešenja** , a zatim dvaput kliknite na **\<your organization name> dimenzije za određivanje cena**. 
2. U levom oknu za navigaciju istraživača rešenja izaberite **Dodaj postojeće** > **Entiteti**.
3. U dijalogu **Komponente rešenja** izaberite sledeće entitete:

  - Stvarno
  - Resurs koji može da se rezerviše
  - Stavka procene
  - Detalj stavke fakture
  - Stavka u glavnoj knjizi
  - Detalj predmeta ugovora za projekat
  - Član projektnog tima
  - Detalj stavke ponude
  - Provizija na cenu uloge
  - Cena uloge 
  - Stavka vremena 


> [!NOTE]
> Obavezno uključite sve obrasce i prikaze za svaki od izabranih entiteta.

4. Izaberite **Ne** kada se od vas zatraži da uključite zavisne entitete za prethodno izabrane entitete.

