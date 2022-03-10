---
title: Integracija fakture dobavljača
description: Ova tema pruža informacije o integraciji fakture dobavljača u Project Operations.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 538a2694591f1d0d368ee0ffeed9bdf12cb47420c3d0571f75185fe433f23436
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986508"
---
# <a name="vendor-invoice-integration"></a>Integracija fakture dobavljača

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Nabavka u vezi sa projektom u Dynamics 365 Project Operations može se snimiti odlaskom na **Dugovanja** > **Fakture** > **Fakture dobavljača na čekanju** i korišćenjem dokumenta fakture dobavljača na čekanju. Za više informacija pogledajte [Kupujte neskladišteni materijal koristeći fakturu dobavljača na čekanju](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> Pre nego što upotrebite funkcionalnost opisanu u ovoj temi, pregledajte i primenite potrebne konfiguracije. Za više informacija pogledajte [Omogućite neskladišteni materijal i fakture dobavljača na čekanju](../procurement/configure-materials-nonstocked.md).

U Project Operations, fakture dobavljača u vezi sa projektom objavljuju se koristeći posebna pravila knjiženja:

- Troškovi povezani sa projektom (uključujući nepovratni porez) ne knjiže se odmah na račun troškova projekta u glavnoj knjizi. Umesto toga, trošak se knjiži na **Računu za integraciju nabavki**. Nalog konfigurisan u **Upravljanje projektima i računovodstvo** > **Podešavanje** > **Parametri upravljanja projektom i računovodstveni parametri** na kartici **Project Operations u usluzi Dynamics 365 Customer Engagement**.
- Dvostruko upisivanje sinhronizuje detalje fakture dobavljača sa Microsoft Dataverse koristeći sledeće mape tabela:

     - **Project Operations entitet izvoza fakture prodavca (msdyn_projectvendorinvoices)** : Ova mapa tabele sinhronizuje informacije o zaglavlju fakture dobavljača. Sinhronizuju se samo fakture dobavljača sa najmanje jednim redom koji sadrži ID projekta u Dataverse.
     - **Project Operations entitet izvoza reda fakture prodavca (msdyn_projectvendorinvoicelines)** : Ova mapa tabele sinhronizuje informacije o zaglavlju reda fakture dobavljača. Sinhronizuju se samo redovi koji sadrže ID projekta u Dataverse.

     > [!NOTE]
     > Detalji o fakturi dobavljača u Dataverse se ne mogu uređivati.

Pomoćna knjiga poreza, pomoćna knjiga dobavljača i druga finansijska knjiženja evidentiraju se prema potrebi u Dynamics 365 Finance kada se faktura dobavljača objavi.

![Integracija fakture dobavljača.](media/DW7VendorInvoice.png)

Kada se zapisi upisuju u **Račun dobavljača** entitet u Dataverse, započinje automatizovani postupak odobravanja zapisa. Ako je potrebno, status automatskog postupka odobravanja može se pregledati u Dataverse odlaskom u **Napredna podešavanja** > **Sistem** > **Sistemski poslovi**. Nakon završetka odobrenja, sistem kreira zapisi klase transakcija materijala u entitetu **Stvarni podaci**.

Stvarni podaci povezani sa materijalima se zatim obrađuju pomoću mape tabela dvostrukog pisanja **Project Operations stvarne vrednosti integracije (msdyn_actuals)**. Više informacija potražite u članku [Procene i stvarne vrednosti](resource-dual-write-estimates-actuals.md).

Periodični proces, **Uvoz iz pripreme** kreira stavke u glavnoj knjizi Project Operations integracije koje se odnose na fakturu dobavljača. Račun za prebijanje dugovanja podrazumevano je račun za integraciju nabavke. Kada se objavi dnevnik integracije, saldo računa se briše za transakciju fakture dobavljača i premešta iznos linije na račun troškova projekta. Takođe se kreiraju transakcije pomoćne knjige projekta za dalje fakturisanje i priznavanje prihoda.