---
title: Sinhronizovanje procena projekta direktno iz usluge Project Service Automation sa uslugom Finance and Operations
description: Ova tema opisuje predloške i osnovne zadatke koji se koriste za sinhronizaciju procene radnih sati i procene troškova projekta direktno iz usluge Microsoft Dynamics 365 Project Service Automation u Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 6696449d80e0915a0c878dbe75cfdf6e268b98ad9f6453bcfc4b424db68021e4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988218"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Sinhronizovanje procena projekta direktno iz usluge Project Service Automation sa uslugom Finance and Operations

[!include[banner](../includes/banner.md)]

Ova tema opisuje predloške i osnovne zadatke koji se koriste za sinhronizaciju procene radnih sati i procene troškova projekta direktno iz usluge Dynamics 365 Project Service Automation u Dynamics 365 Finance.

> [!NOTE]
> - Integracija projektnih zadataka, kategorije transakcija troškova, procene radnih sati, procene troškova i zaključavanje funkcionalnosti dostupni su u verziji 8.0.
> - Integracija stvarnih podataka dostupna je u verziji 8.0.1 ili novijoj.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Tok podataka iz usluge Project Service Automation u Finance

Rešenje za integraciju iz usluge Project Service Automation u Finance koristi funkciju integracije podataka za sinhronizaciju podataka u svim instancama usluga Project Service Automation i Finance. Predlošci za integraciju koji su dostupni sa funkcijom Integracija podataka omogućava tok podataka o procenama radnih sati projekta i procenama troškova projekta između iz usluge Project Service Automation u Finance.

Sledeća ilustracija prikazuje kako se podaci sinhronizuju između usluga Project Service Automation i Finance.

[![Tok podataka za integraciju usluge Project Service Automation sa uslugom Finance.](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Procene radnih sati za projekat

### <a name="template-and-tasks"></a>Predlošci i zadaci

Da biste pristupili dostupnim predlošcima, u Microsoft Power Apps centru administracije izaberite **Projekti**, a zatim u gornjem desnom uglu izaberite **Novi projekat** za izbor javnih predložaka.

Sledeći predložak i osnovni zadaci koji se koriste za sinhronizaciju procena radnih sati projekta iz usluge Project Service Automation u Finance:

- **Naziv predloška u Integraciji podataka:** Procene radnih sati projekta (iz PSA u Fin and Ops)
- **Naziv zadataka u projektu:**

    - Odnosi između transakcija
    - Procene troškova

### <a name="entity-set"></a>Skup entiteta

| Project Service Automation | Finance                                       |
|----------------------------|-----------------------------------------------|
| Projektni zadaci              | Entitet integracije za procene radnih sati projekta |

### <a name="entity-flow"></a>Tok entiteta

Procenama radnih sati projekta se upravlja u usluzi Project Service Automation i oni se sinhronizuju sa uslugom Finance kao predviđanja sati projekta.

### <a name="prerequisites"></a>Preduslovi

Da bi mogla da se izvrši sinhronizacija procena radnih sati projekta, morate sinhronizovati projekte, projektne zadatke i kategorije transakcija troškova projekta.

### <a name="power-query"></a>Power Query

U predlošku za procenu radnog vremena projekta morate da koristite Microsoft Power Query za Excel da biste izvršili ove zadatke:

- Postavite ID podrazumevanog modela predviđanja koji će se koristiti kada integracija kreira nova predviđanja sati.
- U zadatku filtrirajte sve zapise specifične za resurse koji neće uspeti u integraciji predviđanja radnih sati.
- Filtrirajte sve prazne redove kategorija transakcija. Neispunjavanje ovog zadatka može rezultirati netačnim predviđanjima radnih sati.

#### <a name="set-the-default-forecast-model-id"></a>Podesite podrazumevani ID modela predviđanja

Da biste ažurirali podrazumevani ID modela predviđanja u predlošku, kliknite na strelicu **Mapa** za otvaranje mapiranja. Zatim izaberite vezu **Napredni upit i filtriranje**.

- Ako koristite podrazumevani predložak procene radnih sati projekta (iz PSA u Fin and Ops), izaberite **Uslov umetanja** u list **Primenjeni koraci**. U stavci **Funkcija**, zamenite **O\_forecast** nazivom ID-a modela predviđanja koji treba koristiti uz integraciju. Podrazumevani predložak sadrži ID modela predviđanja iz demo podataka.
- Ako kreirate novi obrazac, morate dodati ovu kolonu. U usluzi Power Query izaberite **Dodaj uslovnu kolonu** i unesite naziv za novu kolonu, kao što je **ModelID**. Unesite uslov za kolonu, gde, ako Project zadatak nije bez vrednosti, onda \<enter the forecast model ID\>; u suprotnom je bez vrednosti.

#### <a name="filter-out-resource-specific-records"></a>Filtriranje zapisa specifičnih za resurse

Predložak procena radnih sati projekta (iz PSA u Fin and Ops) ima podrazumevani filter koji uklanja sve zapise specifične za resurse. Ako kreirate sopstveni obrazac, morate dodati ovaj filter. Izaberite vezu **Napredni upit i filtriranje** da filtrirate po koloni **msdyn\_islinetask** tako da budu uvršćeni samo **Netačni** zapisi.

#### <a name="filter-out-empty-transaction-category-rows"></a>Filtrirajte prazne redove kategorija transakcija

Morate dodati filter da biste uklonili sve redove koji imaju prazne kategorije transakcija. Ovaj zadatak je obavezan, bez obzira na to da li koristite podrazumevani predložak ili kreirate sopstveni predložak. Ovaj filter uklanja sve redove rezimea iz usluge Project Service Automation koji mogu prouzrokovati netačna predviđanja radnih sati u usluzi Finance. Izaberite vezu **Napredni upit i filtriranje** da filtrirate prazne zapise u koloni **msdyn\_transactioncategory\_value**.

### <a name="template-mapping-in-data-integration"></a>Mapiranje predložaka u usluzi Data Integration

Sledeća ilustracija prikazuje primer mapiranja zadataka predloška u usluzi Data Integration. Mapiranje prikazuje informacije o terenu koje će se sinhronizovati iz usluge Project Service Automation u Finance.

[![Mapiranje zadataka predložaka u usluzi Data Integration.](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Procene troškova projekta

### <a name="template-and-tasks"></a>Predlošci i zadaci

Sledeći predložak i osnovni zadaci koji se koriste za sinhronizaciju procena troškova iz usluge Project Service Automation u Finance:

- **Naziv predloška u Integraciji podataka:** Procene troškova projekta (iz PSA u Fin and Ops)
- **Naziv zadataka u projektu:**

    - Odnosi između transakcija 
    - Procene troškova

### <a name="entity-set"></a>Skup entiteta

| Project Service Automation | Finance                                                  |
|----------------------------|----------------------------------------------------------|
| Veze transakcija    | Entitet integracije za odnose transakcija projekta |
| Stavke procene             | Entitet integracije za procene troškova projekta         |

### <a name="entity-flow"></a>Tok entiteta

Procenama troškova se upravlja u usluzi Project Service Automation i one se sinhronizuju sa uslugom Finance kao predviđanja troškova projekta.

### <a name="prerequisites"></a>Preduslovi

Da bi mogla da se izvrši sinhronizacija procena troškova projekta, morate sinhronizovati projekte, projektne zadatke i kategorije transakcija troškova projekta.

### <a name="power-query"></a>Power Query

U predlošku za procenu troškova projekta morate da koristite Power Query da biste izvršili sledeće zadatke:

- Filtrirajte da biste uključili samo zapise linija procene troškova.
- Postavite ID podrazumevanog modela predviđanja koji će se koristiti kada integracija kreira nova predviđanja sati.
- Transformišite vrste naplate.
- Transformišite vrste transakcija.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtrirajte da biste uključili samo linije procene troškova

Predložak za procenu troškova projekta (iz PSA u Fin and Ops) ima podrazumevani filter koji uključuje samo linije troškova u integraciji. Ako kreirate sopstveni obrazac, morate dodati ovaj filter. Izaberite zadatak **Odnosi između transakcija**, a zatim kliknite na strelicu **Mapa** da biste otvorili mapiranje. Izaberite vezu **Napredni upit i filtriranje**. Filtrirajte kolonu **msdyn\_transactiontype1** kolona tako da uključuje samo **msdyn\_estimateline**.

#### <a name="set-the-default-forecast-model-id"></a>Podesite podrazumevani ID modela predviđanja

Da biste ažurirali podrazumevani ID modela predviđanja u predlošku, izaberite zadatak **Procene troškova**, a zatim kliknite na strelicu **Mapiraj** da biste otvorili mapiranje. Izaberite vezu **Napredni upit i filtriranje**.

- Ako koristite podrazumevani predložak procene troškova projekta (iz PSA u Fin and Ops), u usluzi Power Query izaberite **Uslov umetanja** u odeljku **Primenjeni koraci**. U stavci **Funkcija**, zamenite **O\_forecast** nazivom ID-a modela predviđanja koji treba koristiti uz integraciju. Podrazumevani predložak sadrži ID modela predviđanja iz demo podataka.
- Ako kreirate novi obrazac, morate dodati ovu kolonu. U usluzi Power Query izaberite **Dodaj uslovnu kolonu** i unesite naziv za novu kolonu, kao što je **ModelID**. Unesite uslov za kolonu, gde, ako ID linije procene nije bez vrednosti, onda \<enter the forecast model ID\>; u suprotnom je bez vrednosti.

#### <a name="transform-the-billing-types"></a>Transformisanje vrsta naplate

Predložak procene troškova projekta (iz PSA u Fin and Ops) uključuje uslovnu kolonu koja se koristi za transformisanje tipova naplate koji su primljeni iz usluge Project Service Automation tokom integracije. Ako kreirate sopstveni obrazac, morate dodati ovu uslovnu kolonu. Izaberite vezu **Napredni upit i filtriranje**, a zatim izaberite **Dodaj uslovnu kolonu**. Unesite ime za novu kolonu, kao što je **BillingType**. Zatim unesite sledeći uslov:

If **msdyn\_billingtype** = 192350000, then **NonChargeable**  
else if **msdyn\_billingtype** = 192350001, then **Chargeable**  
else if **msdyn\_billingtype** = 192350002, then **Complimentary**  
else **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Transformisanje vrsta transakcija

Predložak procene troškova projekta (iz PSA u Fin and Ops) uključuje uslovnu kolonu koja se koristi za transformisanje vrsta transakcija koje su primljene iz usluge Project Service Automation tokom integracije. Ako kreirate sopstveni obrazac, morate dodati ovu uslovnu kolonu. Izaberite vezu **Napredni upit i filtriranje**, a zatim izaberite **Dodaj uslovnu kolonu**. Unesite naziv za novu kolonu, kao što je **TransactionType**. Zatim unesite sledeći uslov:

If **msdyn\_transactiontypecode** = 192350000, then **Cost**  
else if **msdyn\_transactiontypecode** = 192350005, then **Sales**  
else **null**

### <a name="template-mapping-in-data-integration"></a>Mapiranje predložaka u usluzi Data Integration

Sledeće ilustracije prikazuju primere mapiranja zadataka predloška u usluzi Data Integration. Mapiranje prikazuje informacije o terenu koje će se sinhronizovati iz usluge Project Service Automation u Finance.

[![Predložak mapiranja transakcija procene troškova.](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Predložak mapiranja procena troškova.](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]