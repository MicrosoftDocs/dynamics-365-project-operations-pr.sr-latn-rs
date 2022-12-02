---
title: Migracija potpuno fakturisanih kontrolnih tačaka fakturisanja tokom presecanja
description: Ovaj članak objašnjava kako da premestite kontrolne tačke naplate fiksne cene koje su fakturisane klijentu za otvorene projektne ugovore pre datuma objavljivanja.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 05cd71f9860b5698e3a26bc72660b0b2044206c8
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028719"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Migracija potpuno fakturisanih kontrolnih tačaka fakturisanja tokom presecanja

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

## <a name="scenario"></a>Scenario

Contoso se objavljuje sa rešenjem Microsoft Dynamics 365 Project Operations za scenarije resursa/bez zaliha. U sklopu aktivnosti presecanja, tim za implementaciju mora da migrira otvorene projektne ugovore iz starog sistema. Neki od projektnih ugovora uključuju predmete ugovora koji koriste način naplate po fiksnoj ceni i koji su već delimično fakturisani krajnjem klijentu. Tim za implementaciju mora da migrira ove kontrolne tačke za naplatu kao **Proknjižena faktura klijentu**, jer moraju biti uključene u ukupnu vrednost ugovora u svrhe priznavanja prihoda. Međutim, to ne sme uticati na salda klijenta u Dugovanjima i Glavnoj knjizi.

## <a name="solution"></a>Rešenje

### <a name="prerequisites"></a>Preduslovi

- Mora biti instaliran Dynamics 365 Finance 10.0.24 ili noviji.
- Okruženje u kojem će koraci migracije biti dovršeni mora biti u režimu održavanja. Druge aktivnosti ne bi trebalo da se obavljaju dok se kontrolne tačke migriraju.
- Koraci migracije moraju se pratiti tačno onako kako je ovde opisano i mogu se koristiti samo za aktivnost potpunog presecanja. Microsoft ne podržava nijednu drugu upotrebu ove mogućnosti.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Kreiranje verzije preseka mape dvostrukog upisivanja kontrolnih tačaka predmeta ugovora u integraciji usluge Project Operations 

1. Uverite se da je ciljno mapiranje entiteta **Kontrolne tačke za integraciju predmeta ugovora za Project Operations** je ažurirano. 

    1. U Finansijama, idite na **Upravljanje podacima** \> **Entiteti podataka** i izaberite entitet **Kontrolne tačke predmeta ugovora za integraciju rešenja Project Operations**. 
    2. Izaberite **Izmena mapiranja cilja**. 
    3. Na stranici **Priprema mape za cilj** izaberite **Generiši mapiranje**, a zatim potvrdite da želite da generišete mapiranje.

2. Zaustavite i osvežite **Project Operations kontrolne tačke predmeta ugovora o integraciji** (**msdyn\_contractlinescheduleofvalues**) mapu dvostrukog upisivanja. 

    1. Idite na **Upravljanje podacima** \> **Dvostruko upisivanje**, izaberite mapu i otvorite njene detalje. 
    2. Izaberite **Zaustavi** i sačekajte dok sistem ne zaustavi mapu. 
    3. Izaberite **Osveži tabele**.

3. Dodajte mapiranje za status transakcije.

    1. Izaberite **Dodaj mapiranje**.
    2. Na novom redu, u koloni **Aplikacije za finansije i operacije**, izaberite polje **TRANSSTATUS \[TRANSSTATUS\]**.
    3. U koloni **Microsoft Dataverse**, izaberite **msdyn\_invoicestatus \[Status fakture\]**.
    4. U koloni **Tip mape**, izaberite strelicu udesno (**\>**).
    5. U dijalogu koji se pojavu, u polju **Smer sinhronizacije** izaberite **Dataverse u aplikacije za finansije i operacije**.
    6. Izaberite **Dodaj transformaciju**.
    7. U polju **Transformacija tipa** izaberite **ValueMap**.
    8. Izaberite **Dodaj mapiranje vrednosti**.
    9. U levo polje unesite **4**. U desno polje unesite **192350001**. 
    10. Izaberite **Sačuvaj**, a zatim zatvorite dijaloge.

4. Izaberite **Sačuvaj kao** da biste sačuvali verziju mape dvostrukog upisivanja. 
5. U oknu **Dodavanje tabele**, u polju **Objavljivač** izaberite **Podrazumevani izdavač**.
6. U polje **Verzija** unesite verziju.
7. U polje **Opis** unesite napomenu o ovoj verziji preseka mape. 
8. Izaberite **Sačuvaj**.
9. Pokrenite mapu.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Migriranje fakturisanih kontrolnih tačaka u Dataverse okruženje

1. U Project Operations Dataverse okruženju, kreirajte kontrolne tačke koje imaju status fakture **Spremno za fakturisanje**. U ovom trenutku, nemojte migrirati nijednu kontrolnu tačku koja nije fakturisana.

    > [!NOTE]
    > Pre nego što migrirate kontrolne tačke za naplatu, uverite se da su finansijski aspekti koji su povezani sa predmetom ugovora za projekat postavljene na očekivani način. Finansijski aspekti se ne mogu uređivati nakon završetka migracije.

2. Nakon što se sve kontrolne tačke migriraju, zaustavite sledeće mape sa dvostrukim upisivanjem:

    - Kontrolne tačke predmeta ugovora integracije usluge Project Operations (msdyn\_contractlinescheduleofvalues)
    - Project Operations stvarne vrednosti integracije (msdyn\_actuals)
    - Predlog fakture za projekat V2 (fakture)

    Da biste zaustavili mape, pratite ove korake:

    1. U Finansijama, idite na **Upravljanje podacima** \> **Dvostruko upisivanje**, izaberite mapu i otvorite njene detalje.
    2. Izaberite **Zaustavi** i sačekajte dok sistem ne zaustavi mapu.

3. U Project Operations Dataverse okruženju, kreirajte i potvrdite profakture za kontrolne tačke za naplatu. 

    1. Na mapi lokacije idite na ugovore za projekat, izaberite ugovore, a zatim izaberite **Kreiraj fakture**.
    2. Nakon kreiranja faktura, otvorite ih iz menija **Fakture** na mapi lokacije, a zatim izaberite **Potvrdi**.

    Ovaj korak kreira potrebne zapise u Dataverse okruženju. Međutim, to ne utiče na finansije i potraživanja, jer su prethodno navedene mape za dvostruko upisivanje zaustavljene.

4. Nakon što su sve profakture potvrđene, vratite sve mape sa dvostrukim upisivanjem u početno stanje.

    1. Ažurirajte verziju za **Project Operations kontrolne tačke predmeta ugovora o integraciji** (**msdyn\_contractlinescheduleofvalues**) mapu dvostrukog upisivanja na originalnu. 
    2. Izaberite mapu sa dvostrukim upisivanjem na listi mapa, izaberite **Verzija mape tabele**, a zatim izaberite originalnu verziju mape tabele.
    3. Izaberite **Sačuvaj**.
    4. Ponovo pokrenite sledeće mape za dvostruko upisivanje:

        - Kontrolne tačke predmeta ugovora integracije usluge Project Operations (msdyn\_contractlinescheduleofvalues)
        - Project Operations stvarne vrednosti integracije (msdyn\_actuals)
        - Predlog fakture za projekat V2 (fakture)

Kontrolne tačke su sada migrirane, a sistem je spreman za sledeće korake u aktivnosti presecanja.
