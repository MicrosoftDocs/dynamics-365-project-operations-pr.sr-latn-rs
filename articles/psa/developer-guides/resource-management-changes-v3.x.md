---
title: Promene u upravljanju resursima (Project Service Automation 3.x)
description: Ova tema pruža informacije o promenama u oblasti upravljanja resursima.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 94f9adc67163254486387a1ce59d5d3e8e93c335
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148660"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>Promene u upravljanju resursima (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

Odeljci ove teme pružaju informacije o promenama koje su izvršene u oblasti upravljanja resursima u usluzi Dynamics 365 Project Service Automation verzije 3.x.

## <a name="project-estimates"></a>Procene za projekat

Umesto da se zasniva na entitetu **msdyn\_projecttask** (**Projektni zadatak**), procene projekata se zasnivaju na entitetu **msdyn\_resourceassignment** (**Dodela resursa**). Dodele resursa su postale „izvor istine“ za zakazivanje zadataka i određivanje cena zadataka.

## <a name="line-tasks"></a>Zadaci stavke

U aplikaciji PSA 3.x, zadaci stavke su zastareli. Zadaci sada ukazuju na ceo zadatak umesto na zadatke stavke.

Sledeći primer prikazuje kako se zadatak koji se zove „Probni zadatak“ dodeljuje A i B članovima tima u starijim verzijama aplikacije PSA i aplikaciji PSA 3.x.

- **Pre verzije aplikacije PSA 3.x:**

    - Probni zadatak

        - Probni zadatak – 1. zadatak stavke

            - Dodela članu A

        - Probni zadatak – 2. zadatak stavke

            - Dodela članu B

- **PSA 3.x:**

    - Probni zadatak

        - Dodela članu A
        - Dodela članu B

## <a name="unassigned-assignment"></a>Neodeljeni zadatak

U aplikaciji PSA 3.x, nedodeljeni zadatak je zadatak koji je dodeljen članu tima koji ima nultu vrednost (**NULL**) i resursu sa nultom vrednošću (**NULL**). Nedodeljeni zadaci mogu se pojaviti u nekoliko scenarija:

- Ako je zadatak kreiran, ali još uvek nije dodeljen nijednom članu tima, uvek se kreira nedodeljeni zadatak. 
- Ako se uklone svi dodeljeni korisnici iz zadatka, za taj zadatak se ponovo kreira nedodeljeni zadatak.

## <a name="scheduling-fields-on-the-project-task-entity"></a>Polja za zakazivanje u entitetu Projektni zadatak

Polja u entitetu **msdyn\_projecttask** su zastarela ili premeštena u entitet **msdyn\_resourceassignment** ili se sada navode u entitetu **msdyn\_projectteam** (**Član projektnog tima**).

| Zastarelo polje u entitetu msdyn\_projecttask (projektni zadatak) | Novo polje u entitetu msdyn\_resourceassignment (dodela resursa) | Komentar |
|---|---|---|
| msdyn\_assignedresources | Nijedno | |
| msdyn\_assignedteammembers | Nijedno | |
| msdyn\_numberofresources | Nijedno | |
| msdyn\_scheduledhours | Nijedno | |
| msdyn\_effortcontour | msdyn\_plannedwork | Format strukture podataka JSON (JavaScript Object Notation) koja se čuva u polju je promenjen. |

## <a name="schedule-contour"></a>Zakazivanje skice

Skica rasporeda se čuva u polju **Planirani rad** (**msdyn\_plannedwork**) svakog entiteta **Dodela resursa** (**msdyn\_resourceassignment**).

### <a name="structure"></a>Struktura

Nova struktura skice rasporeda sastoji se od fleksibilnih delića vremena koji su definisani za svaki dan rasporeda. Svaki delić vremena ima sledeća svojstva:

- **Početak** - Početak radnog vremena za dan, prema kalendaru projekta.
- **Kraj** - Kraj radnog vremena za dan, prema kalendaru projekta.
- **Radno vreme** - Broj sati koji su dodeljeni u danu.

**Primer**

Ovaj primer koristi kalendar projekta gde je radni dan od 9:00 do 17:00 u vremenskoj zoni UTC-8.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>Automatsko zakazivanje i ručno zakazivanje

Ako je zadatak automatski zakazan, sati se učitavaju unapred, a trajanje zadatka može biti smanjeno.

**Primer**

Sledeći zadatak je automatski zakazan za 18 sati tokom tri dana (od 3. do 5. decembra 2018. godine).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

Ako je zadatak ručno zakazan, sati su ravnomerno raspoređeni na sve datume.

**Primer**

Sledeći zadatak je ručno zakazan za 18 sati tokom tri dana (od 3. do 5. decembra 2018. godine).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>Jedinica dodele

Jedinica dodele zastarela je u aplikaciji PSA 3.x. Sati angažovanja na zadatku sada su ravnomerno podeljeni, po danu, na sve dodeljene resurse.

**Primer**

U ovom primeru, zadatak je dodeljen na dva resursa i automatski je zakazan za 36 sati tokom tri dana (od 3. do 5. decembra 2018. godine).

- 1. dodela:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- 2. dodela:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>Dimenzije za određivanje cena

U aplikaciji PSA 3.x, polja dimenzija za određivanje cena, specifična za resurse (kao što su **Uloga** i **Organizaciona jedinica**) su uklonjeni iz entiteta **msdyn\_projecttask**. Ova polja se sada mogu preuzeti od odgovarajućeg člana projektnog tima (**msdyn\_projectteam**) za dodelu resursa (**msdyn\_resourceassignment**) kada se generišu procene projekata. Novo polje, **msdyn\_organizationalunit**, je dodato u entitet **msdyn\_projectteam**.

| Zastarelo polje u entitetu msdyn\_projecttask (projektni zadatak) | Polje u entitetu msdyn\_projectteam (član projektnog tima) koje se koristi umesto toga |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>Skiciranja

Polja sa skicama za određivanje cena i procene su zastarela u entitetu **msdyn\_projecttask**. Premeštena su u entitet **msdyn\_resourceassignment**.

| Zastarelo polje u entitetu msdyn\_projecttask (projektni zadatak) | Novo polje u entitetu msdyn\_resourceassignment (dodela resursa) |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

Sledeća polja su dodata u entitet **msdyn\_resourceassignment**:

* msdyn\_plannedcost
* msdyn\_plannedsales

Sledeća polja za planirane, stvarne i preostale troškove i prodaju nepromenjena su u entitetu **msdyn\_projecttask**:

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales


[!INCLUDE[footer-include](../../includes/footer-banner.md)]