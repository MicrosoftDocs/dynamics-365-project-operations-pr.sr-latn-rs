---
title: Kreiranje prilagođenih polja i entiteta
description: Ova tema objašnjava kako se kreiraju skupovi opcija i entiteti u rešenju platforme Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755231"
---
# <a name="create-custom-fields-and-entities"></a>Kreiranje prilagođenih polja i entiteta 

Obavite sledeće korake kada želite da kreirate prilagođeni skup opcija ili entitet na Power Apps platformi.  
Procedure u ovoj temi bi trebalo da budu završene korišćenjem veb interfejsa aplikacije Project Service Automation (PSA).

> [!IMPORTANT]
> Preporučuje se da se sve promene dimenzije prilagođene cene unose u odvojenom rešenju. Ova važna najbolja praksa pruža fleksibilnost u budućnosti za ažuriranje ili uklanjanje promena po potrebi, pomoći će pri ponovnoj upotrebi posla i olakšava prilagođavanje ovih promena drugoj instanci. Nakon što unesete sve potrebne promene, izvezite ovo rešenje kao **Kompletno rešenje** i uvezite ga u druge instance da biste ponovo koristili podešavanje cena.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Kreiranje prilagođenog rešenja za dimenzije za određivanje cena
1. U aplikaciji PSA, kliknite na **Podešavanja** > **Rešenja**, a zatim kliknite na **Novo** da biste kreirali novo rešenje. 
2. Imenujte rešenje, **\<ime organizacije > dimenzije za određivanje cena**, unesite preostale zahtevane informacije, a zatim kliknite na **Sačuvaj**.

> ![Kreiranje prilagođenog rešenja za dimenzije za određivanje cena](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Kreiranje prilagođenih polja i skupova opcija u rešenju za dimenzije određivanja cena

Dimenzija određivanja cena može biti skup opcija ili entitet. I jedno i drugo morate da kreirate u rešenju za određivanje cena. Koraci u ovoj proceduri objašnjavaju kako da kreirate dimenzije zasnovane na entitetima i dimenzije zasnovane na skupu opcija.

### <a name="entity-based-dimensions"></a>Dimenzije zasnovane na entitetima

1. U aplikaciji PSA kliknite na **Podešavanja** > **Rešenja**, a zatim dvaput na **\<ime organizacije > dimenzije određivanja cena**.
2. U levom oknu za navigaciju istraživača rešenja izaberite **Entiteti**.
3. Kliknite na **Novi** da biste kreirali novi entitet pod nazivom **Standardna pozicija**. Unesite preostale potrebne informacije, a zatim kliknite na **Sačuvaj**.

> ![Definicija standardnog entiteta naziva](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Dimenzije zasnovane na skupu opcija 
Možete kreirati dve dimenzije zasnovane na skupovima opcija. Pomoću polja **Radna lokacija resursa** pratite cenu radne lokacije **Kod kuće** i **Na lokaciji** i koristite **Radno vreme resursa** sa vrednostima **Standardno** i **Prekovremeno** da biste primenili proviziju kada se posao završi.


1. U aplikaciji PSA kliknite na **Podešavanja** > **Rešenja**, a zatim dvaput na **\<ime organizacije > dimenzije određivanja cena**. 
2. U levom oknu za navigaciju istraživača rešenja izaberite **Skupovi opcija**. 
3. Kliknite na **Novo** da biste kreirali novi skup opcija, unesite preostale zahtevane informacije, a zatim kliknite na **Sačuvaj**.

> ![Dimenzija određivanja cena zasnovana na skupu opcija pod nazivom Radna lokacija resursa ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Dimenzija određivanja cena zasnovana na skupu opcija pod nazivom Radno vreme resursa ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Kreiranje podataka za dimenzije zasnovane na entitetima

Možete ručno kreirati podatke za dimenzije zasnovane na entitetima ili korišćenjem Microsoft Excel poziva za uvoz ili usluge. Koristite korake iz ove procedure da biste kreirali dve standardne pozicije, **Inženjer sistema** i **Viši inženjer sistema** iz dimenzije zasnovane na entitetima **Standardna pozicija**. Ako je obim podataka koje želite da kreirate mali, kao u sledećem primeru, možete da koristite standardni obrazac.

1. U aplikaciji PSA, kliknite na **Napredna pretraga**. Izaberite entitet **Standardna pozicija**, a zatim kliknite na **Rezultati**. Biće prikazani svi redovi u entitetu **Standardna pozicija**.
2. Kliknite na dugme **Novo**. U polje **Naziv** unesite „Inženjer sistema“, a zatim kliknite na **Sačuvaj**.
3. Zatvorite obrazac. 
4. Ponovite korake 1-3 da biste kreirali još jednu standardnu poziciji „Viši inženjer sistema“.

> ![Probni podaci za entitet Standardna pozicija ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a>Dodajte sve zahtevane PSA entitete i srodne komponente u rešenje za dimenzije određivanja cena
Moraćete da dodate sledeće Project Service entitete u rešenje za određivanje cena. Korake u ovoj proceduri koristite da biste napravili neke važne promene šema u rešenju za određivanje cena, tako da entiteti postanu svesni novih dimenzija određivanja cena.

1. U aplikaciji PSA kliknite na **Podešavanja** > **Rešenja**, a zatim dvaput na **\<ime organizacije > dimenzije određivanja cena**. 
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

> ![Dodavanje postojećih entiteta u rešenje za dimenzije određivanja cena](media/Existing-entities-to-PD-solution.png)

> ![Izaberite komponente rešenja](media/Dimension-Components.png)

> [!NOTE]
> Obavezno uključite sve obrasce i prikaze za svaki od izabranih entiteta.

4. Kliknite na **Ne** kada se od vas zatraži da uključite zavisne entitete za goreizabrane entitete.

> ![Nemojte da uključujete sve povezane komponente](media/Do-not-include-required.png)


