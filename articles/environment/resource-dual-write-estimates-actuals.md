---
title: Procene projekata i integracija stvarnih podataka
description: Ova tema pruža informacije o Project Operations integraciji dvostrukog upisivanja za procene projekata i stvarne podatke.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d8aa1541a3560db175acead1d000895312b299db
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000048"
---
# <a name="project-estimates-and-actuals-integration"></a>Procene projekata i integracija stvarnih podataka

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ova tema pruža informacije o Project Operations integraciji dvostrukog upisivanja za procene projekata i stvarne podatke.

## <a name="project-estimates"></a>Procene za projekat

Procene rada, troškova i materijala na projektu se kreiraju i održavaju u Microsoft Dataverse i sinhronizovano sa Finance and Operations aplikacijama za računovodstvene svrhe. Stvaranje, ažuriranje i brisanje nisu podržane putem Finance and Operations aplikacija.

Kreiranje procena zahteva važeću računovodstvenu konfiguraciju za projekat. Projekti koji su povezani sa predmetima ugovora moraju imati važeći profil troškova i prihoda projekta definisanih u pravilima profila troškova i prihoda projekta. Za više informacija pogledajte [Konfigurišite računovodstvo za projekte koje treba naplatiti](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Procene radne snage

Procene radne snage kreira menadžer projekta ili menadžer resursa koji takođe dodeljuje generički ili imenovani resurs projektnom zadatku. Zapisi o dodeli resursa mogu se pregledati na kartici **Dodeljivanje resursa** na stranici **Detalji projekta** u Dataverse. Zapisi o dodeli resursa u Dataverse prave zapise o predviđanju sati u Finance and Operations aplikacijama koje koriste **Entitet za Project Operations integraciju za procene sati (msdyn\_resourceassignments)**.

   ![Integracija procena radne snage](./Media/DW4LaborEstimates.png)

Dvostruko upisivanje sinhronizuje zapise o dodeli resursa sa pripremnom tabelom (**ProjCDSEstimateHoursImport**), a zatim koristi poslovnu logiku za kreiranje i ažuriranje zapisa prognoze sati (**ProjForecastEmpl**).

Računovođa projekta pregleda zapise o predviđanju sati napravljene u Finance and Operations aplikacijama odlaskom na **Upravljanje projektima i računovodstvo** > **Svi projekti** > **Plan** > **Prognoze sati**.

## <a name="expense-estimates"></a>Procene troškova

Procene troškova kreira menadžer projekta na kartici **Procene troškova** na stranici **Detalji projekta** u Dataverse. Zapisi o proceni troškova čuvaju se u entitetu **Red za procenu** u Dataverse. Ovi zapisi procene imaju klasu transakcije, **Trošak** i sinhronizuju se sa zapisima predviđanja troškova u Finance and Operations aplikacijama koje koriste **Entitet za Project Operations integraciju za procenu troškova (msdyn\_estimatelines)**.

   ![Integracija procena troškova](./Media/DW4ExpenseEstimates.png)

Dvostruko upisivanje sinhronizuje zapise o proceni troškova sa pripremnom tabelom, **ProjCDSEstimateExpenseImport**, a zatim koristi poslovnu logiku za kreiranje i ažuriranje zapisa prognoze troškova (**ProjForecastCost**). U linijama za procenu odvojeno se čuvaju podaci o proceni prodaje i proceni troškova. Poslovna logika u Finance and Operations aplikacijama popunjava jedan zapis prognoze troškova koristeći ovaj detalj u tabeli za pripremu.

Računovođa projekta može da pregleda zapise o predviđanju troškova u Finance and Operations aplikacijama odlaskom na **Upravljanje projektima i računovodstvo** > **Svi projekti** > **Plan** > **Prognoze troškova**.

## <a name="material-estimates"></a>Procene materijala

Procene materijala kreira menadžer projekta na kartici **Procene materijala** na stranici **Detalji projekta** u Dataverse. Zapisi o proceni materijala čuvaju se u entitetu **Red za procenu** u Dataverse. Ovi zapisi procene imaju klasu transakcije, **Materijal** i sinhronizuju se sa zapisima predviđanja stavki u Finance and Operations aplikacijama koje koriste **Tabelu integracije projekta za procenu materijala (msdyn\_estimatelines)**.

   ![Integracija procena materijala](./Media/DW4MaterialEstimates.png)

Dvostruko upisivanje sinhronizuje zapise o proceni materijala sa pripremnom tabelom, **ProjForecastSalesImpor**, a zatim koristi poslovnu logiku za kreiranje i ažuriranje zapisa prognoze stavki (**ForecastSales**). U linijama za procenu odvojeno se čuvaju podaci o proceni prodaje i proceni troškova. Poslovna logika u Finance and Operations aplikacijama popunjava jedan zapis prognoze stavki koristeći ovaj detalj u tabeli za pripremu.

Računovođa projekta može da pregleda zapise o predviđanju stavki u Finance and Operations aplikacijama odlaskom na **Upravljanje projektima i računovodstvo** > **Svi projekti** > **Plan** > **Prognoze stavki**.

## <a name="project-actuals"></a>Stvarni podaci o projektu

Stvarni podaci o projektu kreiraju se u Dataverse, na osnovu vremena, troškova, materijala i obračunske aktivnosti. Svi operativni atributi ovih transakcija, uključujući količinu, cenu koštanja, prodajnu cenu i projekat, obuhvaćeni su ovim Dataverse entitetom. Više informacija pogledajte [Stvarni podaci](../actuals/actuals-overview.md). Stvarni zapisi se sinhronizuju sa Finance and Operations aplikacijama koje koriste mapu **Stvarni podaci o Project Operations integraciji (msdyn\_actuals)** za nizvodno računovodstvo.

   ![Integracija stvarnih podataka](./Media/DW4Actuals.png)

Mapa tabele **Stvarni podaci o Project Operations integraciji** sinhronizuje sve zapise iz entiteta **Stvarni podaci** u Dataverse, sa atributom **Preskoči sinhronizaciju (samo za internu upotrebu)** podešen na **Netačno**. Ova vrednost atributa je postavljena u Dataverse automatski kada se zapis kreira. Primeri gde je ovaj atribut postavljen na **Tačno** su:

  - Stvarni troškovi projekta za međukompanijske transakcije. Za više informacija pogledajte [Kreiranje interkompanijskih transakcija](../project-accounting/create-intercompany-transactions.md). Ovi zapisi se preskaču jer sistem ponovo stvara stvarne troškove projekta u Finance and Operations aplikacijama kada se knjiži faktura dobavljača među preduzećima.
  - Negativni nefakturisani zapisi o prodaji kreirani kada se potvrdi faktura. Ovi zapisi se preskaču jer pomoćna knjiga projekta u Finance and Operations aplikacijama ne poništava nefakturisane zapise o prodaji prilikom fakturisanja, već menja status u potpuno fakturisane.

Mapa tabela sa dvostrukim upisivanjem sinhronizuje stvarne zapise sa pripremnom tabelom, **ProjCDSActualsImport**. Ovi zapisi se obrađuju periodičnim procesom **Uvoz iz pripremne tabele** prilikom kreiranja stavki u glavnoj knjizi Project Operations integracije i redova predloga faktura projekta. Za više informacija pogledajte [Dnevnik integracije u usluzi Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse takođe beleži veze između stvarnih transakcija projekata u entitetu **Transakciona veza**. Za više informacija pogledajte [Povežite stvarne podatke sa originalnim zapisima](../actuals/linkingactuals.md). Veze između stvarnih transakcija su takođe sinhronizovane sa Finance and Operations aplikacijama koje koriste mapu tabela dvostrukog upisivanja, **Entitet integracije za odnose transakcije projekta (msdyn\_transactionconnections)**. Ovi zapisi se koriste u periodičnom procesu **Uvoz iz pripremne tabele** prilikom kreiranja stavki u glavnoj knjizi Project Operations integracije i redova predloga faktura projekta.

Objavljivanje dnevnika Project Operations integracije i predloga fakture projekta pokreće ažuriranje u odgovarajućim zapisima u tabeli inscenacije, **ProjCDSActualsImport**. Sistem beleži i evidentira sledeće računovodstvene atribute za stvarne transakcije:

- Iznos računovodstvene valute
- Kurs valute
- Broj vaučera
- Iznos poreza na promet

Mapa tabela **Project Operations stvarne vrednosti integracije** ažurira odgovarajuće stvarne zapise u Dataverse ovim informacijama.
