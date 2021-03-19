---
title: Sinhronizujte kategorije troškova projekta između usluga Finance and Operations i Project Service Automation
description: Ova tema opisuje predloške i osnovne zadatke koji se koriste za sinhronizaciju kategorija zadataka projekta između usluga Microsoft Dynamics 365 Finance i Dynamics 365 Project Service Automation.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 4abb7fe6554825b97df4cc04ee1b02d731cb4af9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289656"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Sinhronizujte kategorije troškova projekta između usluga Finance and Operations i Project Service Automation

[!include[banner](../includes/banner.md)]

Ova tema opisuje predloške i osnovne zadatke koji se koriste za sinhronizaciju kategorija zadataka projekta između usluga Dynamics 365 Finance i Dynamics 365 Project Service Automation.

> [!NOTE]
> - Integracija projektnih zadataka, kategorije transakcija troškova, procene sati, procene troškova i zaključavanje funkcionalnosti dostupni su u verziji 8.0.
> - Integracija stvarnih podataka dostupna je u verziji 8.0.1 ili novijoj.
> - Ako koristite Enterprise Edition 7.3.0, kada instalirate KB 4132657 i KB 4132660, moći ćete da koristite predloške za integrisanje projektnih zadataka, kategorije transakcija troškova, procene sati, procene troškova i stvarnih podataka, kao i da konfigurišite zaključavanje funkcionalnosti. Ako morate da resetujete računovodstvene distribucije, preporučujemo da instalirate i KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Tok podataka za Project Service Automation i Finance

Rešenje za integraciju usluga Project Service Automation i Finance koristi funkciju integracije podataka za sinhronizaciju podataka u svim instancama usluga Project Service Automation i Finance. Predlošci za integraciju koji su dostupni sa funkcijom Integracija podataka omogućava tok podataka o kategorijama projektnih zadataka između usluga Finance i Project Service Automation.

Ako se kategorije troškova projekta savladaju u usluzi Finance, tok integracije je prvi iz usluge Finance u Project Service Automation. ID-ovi integracije kategorija troškova projekta se zatim ažuriraju sinhronizacijom iz usluge Project Service Automation u Finance.

Ako se kategorije troškova projekta savladaju u usluzi Project Service Automation, tok integracije je prvi iz usluge Project Service Automation u Finance. Kategorije projekata moraju već biti konfigurisane u usluzi Finance pre sinhronizacije iz usluge Project Service Automation. Zatim sinhronizujte iz usluge Finance nazad u Project Service Automation, a zatim ponovo iz usluge Project Service Automation u Finance. Na ovaj način garantujete da će se kategorije povezati i da se neće napraviti duplikati.

> [!NOTE]
> Kategorije troškova projekta obično se savladavaju u usluzi Finance. Međutim, ako nije takav slučaj ili ako su kategorije troškova već kreirane u usluzi Project Service Automation, prvo morate sinhronizovati pomoću predloška kategorija transakcija troškova (iz PSA u Fin and Ops). Zatim sinhronizujte pomoću predloška kategorija transakcija troškova projekta (iz Fin and Ops u PSA). Zatim bi trebalo da još jednom pokrenete sinhronizaciju iz usluge Project Service Automation u Finance.
>
> Ako prvo izvršite sinhronizaciju iz usluge Project Service Automation, u usluzi Finance moraju biti ispunjeni sledeći zahtevi:
>
> - Deljena kategorija koja se podudara sa kategorijom projekta koja je postavljena u usluzi Project Service Automation mora postojati i mora biti omogućena i za **Projekat** i za **Trošak**.
> - Za svako pravno lice u usluzi Finance sa kojim se mora integrisati, moraju postojati sledeće kategorije projekata:
>
>     - **Kategorija projekta** postoji. 
>     - **Koristi u trošku** je omogućeno.
>     - **Aktivno u dnevniku** je omogućeno.
>     - **Tip transakcije** je podešen na **Trošak**.

Sledeća ilustracija prikazuje kako se podaci sinhronizuju između usluga Project Service Automation i Finance.

[![Tok podataka za integraciju usluge Project Service Automation sa uslugom Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Sinhronizacija kategorije troškova projekta iz usluge Finance u Project Service Automation

### <a name="template-and-task"></a>Predložak i zadatak

Da biste pristupili predlošku, u Microsoft Power Apps centru administracije izaberite **Projekti**, a zatim u gornjem desnom uglu izaberite **Novi projekat** za odabir javnih obrazaca.

Sledeći predložak i osnovni zadatak koji se koriste za sinhronizaciju kategorija troškova projekta iz usluge Finance u Project Service Automation:

- **Naziv predloška u usluzi Data Integration:** Kategorije transakcija troškova projekta (iz Fin and Ops u PSA)
- **Naziv zadatka u projektu:** Sinhronizujte kategorije sa PSA

### <a name="entity-set"></a>Skup entiteta

| Finance                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Entitet integracije za kategorije | Kategorije transakcija     |

### <a name="entity-flow"></a>Tok entiteta

Kategorijama projektnih zadataka se upravlja u usluzi Finance i oni se sinhronizuju sa uslugom Project Service Automation kao kategorija transakcija.

### <a name="power-query"></a>Power Query

Kada se sinhronizujete sa uslugom Project Service Automation, morate da koristite Microsoft Power Query za Excel da biste postavili vrstu naplate za kategoriju transakcija. Predložak kategorija transakcija troškova projekta (iz Fin and Ops u PSA) pružaju podrazumevanu kolonu i mapiranje. Ako kreirate sopstveni predložak, morate dodati uslovnu kolonu u Power Query. Pratite ove korake.

1. Kliknite na strelicu da biste otvorili mapiranje zadatka kategorija projektnih troškova u predlošku kategorija transakcija troškova projekta (iz Fin and Ops u PSA).
2. Kliknite na vezu **Napredni upit i filtriranje** da biste otvorili Power Query.
2. Izaberite **Dodaj uslovnu kolonu**.
3. Unesite ime za novu kolonu, kao što je **BillingType**.
4. Unesite sledeći uslov: **if CATEGORYID not equal to null then 19235001, Otherwise null**.
5. Kliknite na **U redu** na koloni.
6. Obavezno mapirajte ovu novu kolonu na stranicu za mapiranje.

Sledeća ilustracija prikazuje primer mapiranja zadataka predloška u usluzi Data Integration. Mapiranje prikazuje informacije o polju koje će se sinhronizovati iz usluge Finance u Project Service Automation.

[![Mapiranje kategorije troškova projekta sa Project Service Automation predloškom](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Sinhronizacija kategorije troškova projekta iz usluge Project Service Automation u Finance

### <a name="template-and-task"></a>Predložak i zadatak

Sledeći predložak i osnovni zadatak koji se koriste za sinhronizaciju kategorija troškova projekta iz usluge Project Service Automation u Finance:

- **Naziv predloška u usluzi Data Integration:** Kategorije transakcija troškova projekta (iz PSA u Fin and Ops)
- **Naziv zadatka u projektu:** Sinhronizujte kategorije sa Fin Ops

### <a name="entity-set"></a>Skup entiteta

| Project Service Automation | Finance                           |
|----------------------------|-----------------------------------|
| Kategorije transakcija     | Entitet integracije za kategorije |

### <a name="entity-flow"></a>Tok entiteta

Kategorijama projektnih zadataka se upravlja u usluzi Finance i oni se sinhronizuju sa uslugom Project Service Automation kao kategorija transakcija. Povratna sinhronizacija u Finance ažurira kategoriju projekta u usluzi Finance sa ID-om integracije iz usluge Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Mapiranje predložaka u usluzi Data Integration

Sledeća ilustracija prikazuje primer mapiranja zadataka predloška u usluzi Data Integration.

> [!NOTE]
> Mapiranje prikazuje informacije o terenu koje će se sinhronizovati iz usluge Project Service Automation u Finance.

[![Mapiranje usluge Project Service Automation sa Finance predloškom](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]