---
title: Migracija potpuno fakturisanih prekretnica u naplati kod presecanja
description: Ova tema objašnjava kako da migrirate prekretnice naplate fiksne cene koje su fakturisane kupcu za otvorene ugovore o projektu pre datuma odlaska uživo.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ccdba864a68521024b2c479c12cf5cea616c5bbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576287"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Migracija potpuno fakturisanih prekretnica u naplati kod presecanja

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

## <a name="scenario"></a>Scenario

Contoso ide uživo sa korporacijom Microsoft za Dynamics 365 Project Operations scenarije koji nisu snabdeveni. U sklopu slatkih aktivnosti, tim za implementaciju mora da migrira otvorene projektne ugovore iz starog sistema. Neki od ugovora o projektu uključuju redove ugovora koji koriste način naplate fiksne cene i koji su već delimično fakturisani krajnjem kupcu. Tim za implementaciju mora da migrira ove prekretnice u naplati dok **je faktura kupca proknjižena**, jer moraju biti uključene u ukupnu vrednost ugovora u svrhe priznavanja prihoda. Međutim, to ne sme uticati na salda kupaca u potraživanjima i glavnoj knjizi.

## <a name="solution"></a>Rešenje

### <a name="prerequisites"></a>Preduslovi

- Dynamics 365 Finance 10.0.24 ili noviji mora biti instaliran.
- Okruženje u kojem će koraci migracije biti dovršeni mora biti u režimu održavanja. Druge aktivnosti ne bi trebalo da se obavljaju dok se prekretnice migriraju.
- Koraci migracije moraju biti praćeni tačno onako kako je ovde opisano i mogu se koristiti samo za aktivnost presecanja. Microsoft ne podržava drugu upotrebu ove mogućnosti.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Kreiranje presečene verzije ugovora o integraciji projektnih operacija prekretnice dvostrukog pisanja mape 

1. Uverite se da je ciljno mapiranje entiteta **za integraciju ugovora** o projektnim operacijama akustiиno. 

    1. U oblasti finansija idite u entitete **podataka za** \> **upravljanje podacima** i izaberite entitet prekretnica **u vezi sa ugovorom o integraciji sa operacijama** projekta. 
    2. Izaberite **izmeni mapiranja cilja**. 
    3. Na mapi **koja se priprema za ciljnu** stranicu izaberite **stavku Generiši** mapiranje, a zatim potvrdite da želite da generišete mapiranje.

2. Zaustavite i osvežite mapu **dvostrukog** pisanja ugovora o integraciji sa ugovorom za operacije projekta (**msdyn\_ contractlinescheduleofvalues**). 

    1. Idite na **dual-write** \> **upravljanje podacima**, izaberite mapu i otvorite njene detalje. 
    2. Kliknite **na dugme** "Zaustavi" i sačekajte dok sistem ne zaustavi mapu. 
    3. Izaberite stavku **Osveži tabele**.

3. Dodajte mapiranje za status transakcije.

    1. Izaberite **opciju Dodaj mapiranje**.
    2. U novom redu, u koloni Aplikacije **za finansije i** operacije izaberite **polje TRANSSTATUS \[TRANSSTATUS\]**.
    3. U koloni **Microsoft Dataverse** izaberite **status msdyn\_ invoicestatus \[fakture\]**.
    4. U koloni **Tip mape** izaberite strelicu nadesno (**\>**).
    5. U dijalogu koji se pojavljuje, u polju Smer sinhronizacije **izaberite** u aplikacijama **Dataverse "Finansije" i "Operacije"**.
    6. Izaberite dodaj **transformaciju**.
    7. U polju Vrsta **transformacije** izaberite **mapu vrednosti**.
    8. Izaberite **opciju Dodaj mapiranje vrednosti**.
    9. U levo polje unesite **4**. U desno polje unesite **192350001**. 
    10. Izaberite **stavku** Sačuvaj, a zatim zatvorite dijalog.

4. Kliknite **na dugme Sačuvaj** kao da biste sačuvali verziju mape za dvostruko pisanje. 
5. U oknu **"Dodavanje tabele** ", u polju **Publisher** izaberite stavku Podrazumevani **izdavač**.
6. U polje **Verzija** unesite verziju.
7. U polje **Opis** unesite notu o ovoj presladljivoj verziji mape. 
8. Izaberite **Sačuvaj**.
9. Pokreni mapu.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Migriranje fakturisanih prekretnica u životnu sredinu Dataverse

1. U okruženju Operacija Dataverse projekta kreirajte prekretnice koje imaju status fakture " **Spremno za fakturisanje"**. U ovom trenutku, nemojte migrirati nikakve prekretnice koje nisu fakturisane.

    > [!NOTE]
    > Pre nego što migrirate prekretnice naplate, uverite se da su finansijske dimenzije koje su povezane sa redom ugovora o projektu postavljene na očekivani način. Finansijske dimenzije se ne mogu uređivati nakon završetka migracije.

2. Nakon što se sve prekretnice migriraju, zaustavite sledeće mape sa dvostrukim pisanjem:

    - Prekretnice ugovora o integraciji operacija projekta (msdyn\_ contractlinescheduleofvalues)
    - Project Operations stvarne vrednosti integracije (msdyn\_actuals)
    - Predlog fakture za projekat V2 (fakture)

    Da biste zaustavili mape, sledite ove korake:

    1. U finansijama idite na **dual-write** \> **upravljanje podacima**, izaberite mapu i otvorite njene detalje.
    2. Kliknite **na** dugme "Zaustavi" i sačekajte dok sistem ne zaustavi mapu.

3. U okruženju projektnih Dataverse operacija kreirajte i potvrdite pro-forma fakture za prekretnice naplate. 

    1. Na mapi lokacije idite na ugovore o projektu, izaberite ugovore, a zatim izaberite stavku Kreiraj **fakture**.
    2. Nakon kreiranja faktura, otvorite ih iz menija "Fakture **" na** mapi lokacije, a zatim izaberite stavku **Potvrdi**.

    Ovaj korak kreira potrebne zapise u okruženju Dataverse. Međutim, to ne utiče na finansije i potraživanja na računima, jer su prethodno navedene mape za dvostruko pisanje zaustavljene.

4. Nakon što sve pro-forma fakture budu potvrđene, vratite sve mape sa dvostrukim upisima u početno stanje.

    1. Ažurirajte verziju prekretnice **reda ugovora o integraciji operacija** projekta (**msdyn\_ contractlinescheduleofvalues**) dvostruke mape za pisanje nazad u original. 
    2. Izaberite mapu sa dva pisanja na listi mapa, izaberite verziju **mape** tabele, a zatim izaberite originalnu verziju mape tabele.
    3. Izaberite **Sačuvaj**.
    4. Ponovo pokrenite sledeće mape za dvostruko pisanje:

        - Prekretnice ugovora o integraciji operacija projekta (msdyn\_ contractlinescheduleofvalues)
        - Project Operations stvarne vrednosti integracije (msdyn\_actuals)
        - Predlog fakture za projekat V2 (fakture)

Prekretnice su sada migrirane, a sistem je spreman za sledeće korake u aktivnosti presecanja.
