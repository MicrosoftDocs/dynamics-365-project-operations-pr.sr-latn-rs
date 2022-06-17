---
title: Procene projekata i integracija stvarnih podataka
description: Ovaj članak pruža informacije o integraciji dvostrukog pisanja operacija projekta za procene projekta i stvarne vrednosti.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 43c868b051bf141cfc3211669c0a44333b4b2c65
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914603"
---
# <a name="project-estimates-and-actuals-integration"></a>Procene projekata i integracija stvarnih podataka

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ovaj članak pruža informacije o integraciji dvostrukog pisanja operacija projekta za procene projekta i stvarne vrednosti.

## <a name="project-estimates"></a>Procene za projekat

Projektni rad, troškovi i materijalne procene se kreiraju i održavaju u Microsoft Dataverse aplikacijama za finansije i operacije u knjigovodstvene svrhe. Operacije kreiranja, ažuriranja i brisanja nisu podržane pomoću aplikacija "Finansije i operacije".

Kreiranje procena zahteva važeću računovodstvenu konfiguraciju za projekat. Projekti koji su povezani sa predmetima ugovora moraju imati važeći profil troškova i prihoda projekta definisanih u pravilima profila troškova i prihoda projekta. Za više informacija pogledajte [Konfigurišite računovodstvo za projekte koje treba naplatiti](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Procene radne snage

Procene radne snage kreira menadžer projekta ili menadžer resursa koji takođe dodeljuje generički ili imenovani resurs projektnom zadatku. Zapisi o dodeli resursa mogu se pregledati na kartici **Dodeljivanje resursa** na stranici **Detalji projekta** u Dataverse. Zapisi dodeljivanja resursa Dataverse u zapisima predviđanja za kreiranje časova u aplikacijama **za finansije i operacije pomoću entiteta integracije projektnih operacija za procenu sata (msdyn\_ resourceassignments)**.

   ![Integracija procena radne snage.](./Media/DW4LaborEstimates.png)

Dvostruko upisivanje sinhronizuje zapise o dodeli resursa sa pripremnom tabelom (**ProjCDSEstimateHoursImport**), a zatim koristi poslovnu logiku za kreiranje i ažuriranje zapisa prognoze sati (**ProjForecastEmpl**).

Knjigovođa projekta pregleda zapise sa prognoziranim časovima kreirane u aplikacijama za finansije i operacije tako što ide **na upravljanje projektima i računovodstvo** > **Svih** > **projekata Plan** > **Hour predviđanja**.

## <a name="expense-estimates"></a>Procene troškova

Procene troškova kreira menadžer projekta na kartici **Procene troškova** na stranici **Detalji projekta** u Dataverse. Zapisi o proceni troškova čuvaju se u entitetu **Red za procenu** u Dataverse. Ovi zapisi procene imaju klasu transakcija, "Troškovi" **i** sinhronizuju se sa zapisima predviđanja troškova u aplikacijama **za finansije i operacije koristeći entitet integracije operacija projekta za procenu troškova (msdyn\_ estimatelines)**.

   ![Integracija procena troškova.](./Media/DW4ExpenseEstimates.png)

Dvostruko upisivanje sinhronizuje zapise o proceni troškova sa pripremnom tabelom, **ProjCDSEstimateExpenseImport**, a zatim koristi poslovnu logiku za kreiranje i ažuriranje zapisa prognoze troškova (**ProjForecastCost**). U linijama za procenu odvojeno se čuvaju podaci o proceni prodaje i proceni troškova. Poslovna logika u aplikacijama za finansije i operacije popunjava jedan zapis predviđanja troškova koristeći ovaj detalj u pripremnoj tabeli.

Knjigovođa projekta može da pregleda zapise predviđanja troškova u aplikacijama za finansije i operacije tako što će preći **na upravljanje projektima i računovodstvo** > **Svih projekata** > **Planirajte** > **prognoze troškova**.

## <a name="material-estimates"></a>Procene materijala

Procene materijala kreira menadžer projekta na kartici **Procene materijala** na stranici **Detalji projekta** u Dataverse. Zapisi o proceni materijala čuvaju se u entitetu **Red za procenu** u Dataverse. Ovi zapisi procene imaju klasu transakcija, "Materijal" **i** sinhronizuju se sa zapisima predviđanja artikla u aplikacijama za finansije i operacije **koristeći tabelu integracije projekta za procenu materijala (msdyn\_ estimatelines)**.

   ![Integracija procena materijala.](./Media/DW4MaterialEstimates.png)

Dvostruko upisivanje sinhronizuje zapise o proceni materijala sa pripremnom tabelom, **ProjForecastSalesImpor**, a zatim koristi poslovnu logiku za kreiranje i ažuriranje zapisa prognoze stavki (**ForecastSales**). U linijama za procenu odvojeno se čuvaju podaci o proceni prodaje i proceni troškova. Poslovna logika u aplikacijama "Finansije" i "Operacije" popunjava jedan zapis predviđanja artikla koristeći ovaj detalj u pripremnoj tabeli.

Knjigovođa projekta može da pregleda zapise predviđanja artikla u aplikacijama za finansije i operacije tako što će preći **na upravljanje projektima i računovodstvo** > **Svih projekata** > **Planirati** > **predviđanja artikla**.

## <a name="project-actuals"></a>Stvarni podaci o projektu

Stvarni podaci o projektu kreiraju se u Dataverse, na osnovu vremena, troškova, materijala i obračunske aktivnosti. Svi operativni atributi ovih transakcija, uključujući količinu, cenu koštanja, prodajnu cenu i projekat, obuhvaćeni su ovim Dataverse entitetom. Više informacija pogledajte [Stvarni podaci](../actuals/actuals-overview.md). Stvarni zapisi se sinhronizuju sa aplikacijama "Finansije" i "Operacije" koristeći dvostruku mapu tabele "Integracija projektnih **operacija" (msdyn\_ actuals)** za nizvodno knjigovodstvo.

   ![Integracija stvarnih podataka.](./Media/DW4Actuals.png)

Mapa tabele **Stvarni podaci o Project Operations integraciji** sinhronizuje sve zapise iz entiteta **Stvarni podaci** u Dataverse, sa atributom **Preskoči sinhronizaciju (samo za internu upotrebu)** podešen na **Netačno**. Ova vrednost atributa je postavljena u Dataverse automatski kada se zapis kreira. Primeri gde je ovaj atribut postavljen na **Tačno** su:

  - Stvarni troškovi projekta za međukompanijske transakcije. Za više informacija pogledajte [Kreiranje interkompanijskih transakcija](../project-accounting/create-intercompany-transactions.md). Ovi zapisi se preskaču zato što sistem ponovo kreira trošak projekta stvarni u aplikacijama "Finansije" i "Operacije" kada se proknjiži faktura međukompanijskog dobavljača.
  - Negativni nefakturisani zapisi o prodaji kreirani kada se potvrdi faktura. Ovi zapisi se preskaču zato što podstanar projekta u aplikacijama "Finansije" i "Operacije" ne obrće neželjeni zapis prodaje u fakturisanju, već menja status u potpuno fakturisan.

Mapa tabela sa dvostrukim upisivanjem sinhronizuje stvarne zapise sa pripremnom tabelom, **ProjCDSActualsImport**. Ovi zapisi se obrađuju periodičnim procesom **Uvoz iz pripremne tabele** prilikom kreiranja stavki u glavnoj knjizi Project Operations integracije i redova predloga faktura projekta. Za više informacija pogledajte [Dnevnik integracije u usluzi Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse takođe beleži veze između stvarnih transakcija projekata u entitetu **Transakciona veza**. Za više informacija pogledajte [Povežite stvarne podatke sa originalnim zapisima](../actuals/linkingactuals.md). Veze između stvarnih transakcija se sinhronizuju i sa aplikacijama "Finansije" i "Operacije" koristeći mapu tabele za dvostruko pisanje, **entitet integracije za odnosi (msdyn\_ transactionconnections)**. Ovi zapisi se koriste u periodičnom procesu **Uvoz iz pripremne tabele** prilikom kreiranja stavki u glavnoj knjizi Project Operations integracije i redova predloga faktura projekta.

Objavljivanje dnevnika Project Operations integracije i predloga fakture projekta pokreće ažuriranje u odgovarajućim zapisima u tabeli inscenacije, **ProjCDSActualsImport**. Sistem beleži i evidentira sledeće računovodstvene atribute za stvarne transakcije:

- Iznos računovodstvene valute
- Kurs valute
- Broj vaučera
- Iznos poreza na promet

Mapa tabela **Project Operations stvarne vrednosti integracije** ažurira odgovarajuće stvarne zapise u Dataverse ovim informacijama.
