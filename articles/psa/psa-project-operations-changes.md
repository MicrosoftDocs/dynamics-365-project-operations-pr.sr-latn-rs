---
title: Promene funkcija od aplikacije Project Service Automation do usluge Project Operations
description: Ovaj članak pruža pregled promena funkcija iz automatizacije usluge projekta u Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 8a6030faf777051ea1003679589af4bdf97322ab
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925367"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Promene funkcija od aplikacije Project Service Automation do usluge Project Operations

Nadogradnja sa Dynamics 365 Project Service Automation na Dynamics 365 Project Operations Lite biće isporučena u tri faze. Ovaj članak pruža informacije o velikim promenama koje možete očekivati kada se nadogradnja dovrši.

| Nadogradnja isporuke | Faza 1 <br>(januar 2022. godine) | Faza 2 <br>(Aprilski talas 2022) | Faza 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Nema zavisnosti od strukture analize rada (WBS) za projekte. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS je uključen u trenutno podržana ograničenja projektnih operacija. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| WBS izvan trenutno podržanih ograničenja projektnih operacija, uključujući podršku za klijenta radne površine projekta. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Upravljanje projektima

Najznačajnije promene u korisničkom iskustvu biće u oblasti planiranja projekta. Project Operations usvaja novo moderno iskustvo za upravljanje strukturom analize rada (WBS) tako što koristi mogućnosti [zakazivanja koje obezbeđuje Projekat za Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Razlike u iskustvu sa planiranjem

Sledeća tabela rezimira razlike u planiranjeu između automatizacije projektnih usluga i operacija projekta.

|  Zakazivanje     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Predlošci projekata - mogućnost definisanja i primene predložaka projekta prilikom kreiranja projekta  |  &nbsp;    | :heavy_check_mark: |
| Integracija strukture projektnog rada (WBS) sa klijentom radne površine   |    &nbsp;  | :heavy_check_mark: |
| Ograničenja - Počnite ne ranije nego, završite ne kasnije od  | :heavy_check_mark: |   &nbsp;  |
| Prekretnice - zadaci sa nultim trajanjem   | :heavy_check_mark:  |  &nbsp;  |
| Zadaci vođeni resursima će poštovati dostupnost dodeljenih resursa   | :heavy_check_mark: |  &nbsp;    |
| Uređivanje u fazi vremena - Uređivanje planova i rad na dnevnoj bazi   |   &nbsp;  | :heavy_check_mark: |
| Automatsko/ručno planiranje - Koristite mašinu za planiranje projekta da biste automatski ili ručno isplanirali zadatke |  &nbsp; | :heavy_check_mark:  |
| Uređivanje velikih projekata direktno u korisničkom interfejsu: ne postoji ograničenje veličine planova koji se mogu uređivati  | Ograničenje zadatka od 500  | :heavy_check_mark:       |
| Procenat dovršenog - označi tok zadatka   | :heavy_check_mark:  |  &nbsp;  |
| [Režimi projektnog](../project-management/scheduling-modes.md) rasporeda - Definisanje projekta kao fiksnih jedinica, fiksni napor ili fiksno trajanje | :heavy_check_mark: | &nbsp; |
| Vremenska osa - Napravite i prilagodite prikaz vremenske ose da biste vizuelizovali detalje rasporeda i komunicirali sa zainteresovanim stranama. | :heavy_check_mark:  | &nbsp; |
| Zadaci vođeni naporom - Zakazivanje podrške motora za zakazivanje zadatka kao napora vođenog  | :heavy_check_mark:  | &nbsp; |
| **Dijalog sa informacijama** o zadatku - čuvanje detalja zadatka pomoću dijaloga | :heavy_check_mark:  |  &nbsp;  |
| Prevucite i otpustite - zadaci sa više izbora i izmenite njihov položaj u WBS-u | :heavy_check_mark: | &nbsp;  |
| Fleksibilni uporni prikazi - Definisanje granuliranih prikaza atributa zadatka   | :heavy_check_mark:  | &nbsp; |
| Sortiranje i filtriranje WBS-a  | :heavy_check_mark:  | &nbsp; |
| Prikaz tabli za isporuku projekta bez vodopada  | :heavy_check_mark:   | &nbsp; |
| Prikaz vremenske ose - Interaktivni Gantov grafikon koji se koristi za vizuelizaciju i uređivanje WBS-a   | :heavy_check_mark:  | &nbsp; |
| Tasterske prečice - korišćenje tasterskih prečica za uobičajene operacije, kao što su uvlačenje pasusa ili umetanje  | :heavy_check_mark:  |  &nbsp; |
| Opoziv na više nivoa - Izvrši analizu "šta-ako" da biste u potpunosti razumeli uticaj promena tako što ćete storinom i ponovo primeniti čitav skup operacija | :heavy_check_mark: | &nbsp; |
| Iseci/kopiraj/nalepiti - Sarađujte po planu tako što ćete kopirati i nalepiti detalje rasporeda između aplikacija  | :heavy_check_mark: | &nbsp; |
| Kontrolne liste zadataka - dodavanje do 20 stavki kontrolne liste zadatku   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Planiranje projekta

Stranica **"Projekat** " u oblasti "Operacije projekta" ima značajan broj razlika u poređenju sa stranicom **"Projekat"** u oblasti Automatizacije projektnih usluga.

Sledeće radnje su uklonjene sa stranice **"** Projekti" u sklopu nadogradnje faze 1:

  - **Otvori u programu MS Project**
  - **Kreiraj predložak**
  - **Raskini vezu sa programom MS Project**

Stranica **"Projekat** " u operacijama projekta sadrži sledeće nove kartice.

- **Procena materijala**
- **Podešavanje naplate za zadatak**

Kartica **"** Status" je uklonjena i polje **Status** se sada nalazi **na** kartici "Rezime" sa režimom zakazivanja projekta.

   ![Ispravke stranice projekta.](media/projectform.png)

Kartica **"Raspored**" je preimenovana u **karticu** "Zadatak" i sadrži novo iskustvo planiranja projekta sa projektom za Web.

   ![Kartica "Novi projektni zadaci".](media/tasktab.png)

## <a name="scheduling-modes"></a>Režimi planiranja

Operacije projekta su predstavile novu funkciju, [režime zakazivanja](../project-management/scheduling-modes.md). Svi postojeći projekti automatizacije projektnih usluga podrazumevano će biti fiksno **trajanje u** operacijama projekta. Međutim, podrazumevanim vrednostima za nove projekte može se upravljati odlaskom u režim **rasporeda** > **parametara "Parametri postavki** > **·** > **"**.

   ![Postavke parametara projekta za režim "Raspored".](media/projectparameter.png)

## <a name="project-planning-limits"></a>Ograničenja planiranja projekta

Operacije projekta se oslanja na Projekat za Web za sve operacije zakazivanja projekta. Projekat za Web upravlja strukturom radne analize koristeći ograničenja u sledećoj tabeli.

| **Polje**                                          | **Ograničenje**             |
|----------------------------------------------------|-----------------------|
| Maksimalni ukupni broj zadataka za projekat                  | 500                   |
| Maksimalno ukupno trajanje za projekat               | 3650 dana (10 godina)  |
| Maksimalni ukupni broj resursa za projekat              | 300                   |
| Maksimalan ukupni broj veza (samo narednih) za projekat | 600                   |
| Maksimalni ukupni broj prilagođenih polja za projekat          | 10                    |
| Maksimalni nivo hijerarhije                            | 10 nivoa             |
| Maksimalan broj veza (narednih + prethodnih)            | 20                    |
| Maksimalno trajanje zadatka lista                      | 1250 dana             |
| Maksimalno trajanje zadatka rezimea                 | 3650 dana (10 godina)  |
| Maksimalan broj resursa dodeljenih zadatku               | 20 resursa          |
| Podržani opseg datuma za zadatak                    | 1.1.2000. – 12.31.2149. |
| Stavke liste za proveru                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Projektno planiranje ekstenzije i razvoja

Nakon nadogradnje na operacije projekta, morate koristiti API-je za planiranje projekta da biste izvršili operacije kreiranja, ažuriranja i brisanja na sledećim entitetima:

|   Naziv entiteta           |   Logičko ime entiteta       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projektni zadatak            | msdyn_projecttask           |
| Zavisnost projektnog zadatka | msdyn_projecttaskdependency |
| Dodela resursa     | msdyn_resourceassignment    |
| Kontejner projekta          | msdyn_projectbucket         |
| Član projektnog tima     | msdyn_projectteam           |

Ako trenutno imate prilagođavanja koja uključuju ove entitete, pogledajte članak Korišćenje [API-ja sa planom projekta za izvršavanje operacija sa entitetima za](../project-management/schedule-api-preview.md) planiranje za smernice za implementaciju.

## <a name="data-model-changes"></a>Promene modela podataka

U sklopu Faze nadogradnje 1, postoje promene u modelu podataka. Ove promene su pre svega promene polja u postojećim entitetima. U fazi 1, entiteti, **msydn_project** i **msdyn_projectteam** su reaktorizacija prilagođavanja. 

> [!IMPORTANT]
> Ovaj odeljak će se ažurirati sa dodatnim entitetima dok se buduće faze nadogradnje budu dovršale.

Sledeća polja su zamenjena novim poljima.

|   Entity          |   Staro logično ime   |   Novo logičko ime    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Dodata su sledeća polja.

|   Entity          |   Logičko ime                               |   Opis |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Prikazuje zbir stvarne prodaje naknada na projektu. Samo za korišćenje u funkciji Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialcost                     | Prikazuje zbir stvarnih troškova materijala na projektu. Samo za korišćenje u funkciji Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialsales                    | Prikazuje zbir stvarne prodaje materijala na projektu. Samo za korišćenje u funkciji Project Service Automation. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Red ugovora povezan sa ovim projektom. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Ovo je interno sistemsko polje koje se koristi za kopiranje **projekta** povezanog sa identifikatorom korelacije. Samo za korišćenje u funkciji Project Service Automation. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Ovo je interno sistemsko polje koje se koristi za **kopiranje** projekta povezanog sa identifikatorom sesije. Samo za korišćenje u funkciji Project Service Automation. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Poslednja sinhronizacija XRM globalnog simbola revizije iz usluge projektovanja. |
| msdyn_project     | msdyn_msprojectdocument                      | Microsoft Project dokument koji pripada projektu. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Zbir planiranih troškova materijala na projektu. Samo za korišćenje u funkciji Project Service Automation. |
| msdyn_project     | msdyn_plannedmaterialsales                   | Agregat planirane prodaje materijala na projektu. Samo za korišćenje u funkciji Project Service Automation. |
| msdyn_project     | msdyn_program                                | Program sa kojim je ovaj projekat povezan. |
| msdyn_project     | msdyn_quotelineproject                       | Red ponude povezan sa ovim projektom. |
| msdyn_project     | msdyn_replaylogheader                        | Zaglavlje evidencija ponovne reprodukcije. |
| msdyn_project     | msdyn_schedulemode                           | Podrazumevani režim zakazivanja koji se koristi za sve zadatke na projektu.  |
| msdyn_project     | msdyn_taskearlieststart                      | Najraniji datum početka bilo kog zadatka u projektu.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Član projektnog tima iz kojeg je kopiran ovaj član projektnog tima. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Označava da li treba kreirati zahtev resursa za novokreiranog generičkog člana tima.  |
| msdyn_projectteam | msdyn_deletestatus                           | Status brisanja člana tima za praćenje da li postoji zahtev za brisanje poslat usluzi "Planiranje projekta" i da li uspešno šalje odgovor u očekivanom vremenskom prozoru. |
| msdyn_projectteam | msdyn_effortcompleted                        | Prati napore koje je član tima postigao na svojim zadacima. |
| msdyn_projectteam | msdyn_effortremaining                        | Prati napore koje tek treba da završi član tima na svojim zadacima. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Period čekanja od vremena kada član tima šalje zahtev za brisanje usluzi za planiranje projekta dok član tima zaista ne bude izbrisan na Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Vreme koje treba zapisati kada član tima izbriše zahtev za brisanje šalje se usluzi za planiranje projekta. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Pokazuje člana projektnog tima sa kojeg je kopiran ovaj član projektnog tima.  |

## <a name="project-templates"></a>Predlošci projekata

Operacije projekta ne pružaju podršku predlošcima projekata. Međutim, veći deo osnovne funkcionalnosti možete da kopirate korišćenjem API-ja [za kopiranje projekta](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Podrška za programski dodatak na radnoj površini

Podrška za programski dodatak Microsoft Project Desktop neće biti dostupna u prve 2 faze nadogradnje. U fazi 3, klijenti koji imaju projekte veće od trenutno podržanih ograničenja projekta za Web moći će da koriste programski dodatak na radnoj površini.

## <a name="editing-resource-assignment-contours"></a>Uređivanje kontura dodeljivanje resursa

Mogućnost uređivanja kontura dodeljivanja resursa biće dostupna kada faza 2 nadogradnje bude dostupna.

## <a name="billing-and-pricing"></a>Naplata i određivanje cena

Sledeće nove funkcije su dodate u operacije projekta. Ove funkcije su aditiv u prirodi i ne utiču na model podataka za automatizaciju usluge projekta.

- [Snimanje korišćenja materijala na projektima i projektne zadatke](../material/material-usage-log.md)
- [Upravljanje podizvođačima](../pro/subcontracting/managing-subcontracts-overview.md)
- [Avansi i ugovori zasnovani na avansnim uplatama](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Status i provere valjanosti ugovora koji se ne premašuju](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Naplata zasnovana na zadatku](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Neodobrene komponente

Sledeće tabele dokumentuju sva neodobrena polja koja su premeštena u rešenje za zastarele komponente nakon nadogradnje. Više informacija i vezu ka rešenju potražite u članku [Dynamics 365 Project Service Automation 3x sa operacijama projekta 4x neodobrenim komponentama](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>invoicedetail

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_cenovnik                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_agregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

