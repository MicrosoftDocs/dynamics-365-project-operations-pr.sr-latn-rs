---
title: Kreiranje prilagođenih polja i entiteta kao dimenzije za određivanje cena
description: Ova tema pruža informacije o tome kako da kreirate prilagođene skupove opcija ili entitete.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
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
ms.openlocfilehash: fc5917856b8f28d36dc55593a68eba7823a00b36
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642830"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Kreiranje prilagođenih polja i entiteta kao dimenzije za određivanje cena

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Obavite sledeće korake kada želite da kreirate prilagođeni skup opcija ili entitet za korišćenje kao dimenzije određivanja cena. Za više informacija pogledajte [Pregledu dimenzija određivanja cena](pricing-dimensions-overview.md).  

> [!IMPORTANT]
> Preporučuje se da se sve promene dimenzije prilagođene cene unose u odvojenom rešenju. Ova važna najbolja praksa pruža fleksibilnost u budućnosti za ažuriranje ili uklanjanje promena po potrebi. Ovo će takođe pomoći u ponovnoj upotrebi vašeg posla i olakšati prenos ovih promena na drugu instancu. Nakon što izvršite sve potrebne promene, izvezite ovo rešenje kao **Kompletno rešenje** i uvezite ga u druge instance da biste ponovo koristili podešavanje cena.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Kreiranje prilagođenih polja i skupova opcija u rešenju za dimenzije određivanja cena

Dimenzija određivanja cena može biti skup opcija ili entitet. I jedno i drugo morate da kreirate u rešenju za određivanje cena. Koraci u ovoj proceduri objašnjavaju kako da kreirate dimenzije zasnovane na entitetima i dimenzije zasnovane na skupu opcija.

### <a name="entity-based-dimensions"></a>Dimenzije zasnovane na entitetima
Da biste kreirali dimenzije zasnovane na entitetima, sledite ove korake:

1. Idite na **Podešavanja** > **Rešenja**, a zatim dvaput kliknite na **\<your organization name> dimenzije za određivanje cena**.
2. U levom oknu za navigaciju istraživača rešenja izaberite **Entiteti**.
3. Izaberite **Novo** da biste kreirali novi entitet pod nazivom **Standardna pozicija**. 
4. Unesite preostale potrebne informacije, a zatim izaberite **Sačuvaj**.

> ![Definicija standardnog entiteta naziva](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>Dimenzije zasnovane na skupu opcija 
Možete kreirati dve dimenzije zasnovane na skupovima opcija. 

- Koristite **Mesto rada resursa** da biste pratili cenu za rad na lokaciji **Kuća** i za rad **Na lokaciji**. 
- Koristite **Radno vreme resursa** sa vrednostima **Redovno** i **Prekovremeno** da biste primenili proviziju kada je posao završen.

Sledeći grafikon daje prikaz dimenzije **Mesto rada resursa**. 

> ![Dimenzija određivanja cena zasnovana na skupu opcija pod nazivom Radna lokacija resursa](media/Option-set-PD-called-Resource-Work-Location.png)

Sledeći grafikon daje prikaz dimenzije **Radno vreme resursa**. 

> ![Dimenzija određivanja cena zasnovana na skupu opcija pod nazivom Radno vreme resursa](media/Option-set-PD-called-Resource-Work-Hours.png)

1. Idite na **Podešavanja** > **Rešenja**, a zatim dvaput kliknite na **\<your organization name> dimenzije za određivanje cena**. 
2. U levom oknu za navigaciju istraživača rešenja izaberite **Skupovi opcija**. 
3. Izaberite **Novo** da biste kreirali novi skup opcija, unesite preostale zahtevane informacije, a zatim izaberite **Sačuvaj**.

## <a name="create-data-for-entity-based-dimensions"></a>Kreiranje podataka za dimenzije zasnovane na entitetima

Možete ručno kreirati podatke za dimenzije zasnovane na entitetima ili korišćenjem Microsoft Excel poziva za uvoz ili usluge. Koristite korake iz ove procedure da biste kreirali dve standardne pozicije, **Inženjer sistema** i **Viši inženjer sistema** iz dimenzije zasnovane na entitetima **Standardna pozicija**. Ako je obim podataka koje želite da kreirate mali, kao u sledećem primeru, možete da koristite standardni obrazac.

1. Izaberite **Napredna pretraga**.
2. Izaberite entitet **Standardna pozicija** a, a zatim izaberite **Rezultati**. Biće prikazani svi redovi u entitetu **Standardna pozicija**.
3. Izaberite **Novo**, a zatim u polje **Ime** unesite „Inženjer sistema“ i izaberite **Sačuvaj**.
4. Zatvorite stranicu. 
5. Ponovite korake 1-3 da biste kreirali još jednu standardnu poziciji „Viši inženjer sistema“.

> ![Probni podaci za entitet Standardna pozicija](media/ST-data.png)
