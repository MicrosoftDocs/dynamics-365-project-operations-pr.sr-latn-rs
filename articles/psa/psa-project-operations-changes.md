---
title: Promene funkcija od aplikacije Project Service Automation do usluge Project Operations
description: Ovaj članak pruža pregled promena funkcija iz usluge Project Service Automation u Dynamics 365 Project Operations.
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
ms.openlocfilehash: a9c69fc4296d30763f3994a4955e64ab258ceb4f
ms.sourcegitcommit: 675e9f3615e701c5f998de3a5ea3e25df11ae107
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459944"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Promene funkcija od aplikacije Project Service Automation do usluge Project Operations

Nadogradnja sa usluge Dynamics 365 Project Service Automation na Dynamics 365 Project Operations jednostavnu primenu biće isporučena u tri faze. Ovaj članak pruža informacije o velikim promenama koje možete očekivati kada se nadogradnja dovrši.

| Isporuka nadogradnje | Faza 1 <br>(januar 2022.) | Faza 2 <br>(novembar 2022.) | Faza 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Nema zavisnosti na strukturnoj analizi posla (SAP) za projekte. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| SAP je uključen u trenutno podržana ograničenja za Project Operations. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| SAP izvan trenutno podržanih ograničenja za Project Operations, uključujući podršku za Project Desktop Client. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Upravljanje projektima

Najznačajnije promene u korisničkom iskustvu biće u oblasti planiranja projekta. Project Operations usvaja novo moderno iskustvo za upravljanje strukturnom analizom posla (SAP) tako što koristi mogućnosti zakazivanja koje pruža [Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Razlike u iskustvu zakazivanja

Sledeća tabela rezimira razlike u zakazivanju između usluga Project Service Automation i Project Operations.

|  Zakazivanje     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Predlošci projekata – mogućnost definisanja i primene predložaka projekta prilikom kreiranja projekta  |  &nbsp;    | :heavy_check_mark: |
| Integracija strukturne analize posla (SAP) sa klijentom za računare   |    &nbsp;  | :heavy_check_mark: |
| Ograničenja – nemojte početi pre, nemojte završiti nakon  | :heavy_check_mark: |   &nbsp;  |
| Kontrolne tačke – zadaci sa nultim trajanjem   | :heavy_check_mark:  |  &nbsp;  |
| Zadaci zasnovani na resursima poštovaće dostupnost dodeljenih resursa   | :heavy_check_mark: |  &nbsp;    |
| Vremensko uređivanje – uređujte planove i radite na dnevnoj osnovi   |   &nbsp;  | :heavy_check_mark: |
| Automatsko/ručno zakazivanje – koristite mehanizam za zakazivanje projekta da biste automatski ili ručno zakazali zadatke |  &nbsp; | :heavy_check_mark:  |
| Uređivanje velikih projekata direktno u korisničkom interfejsu: ne postoji ograničenje po pitanju veličine planova koji se mogu uređivati  | Ograničenje od 500 zadataka  | :heavy_check_mark:       |
| Procenat dovršenog – označite tok zadatka   | :heavy_check_mark:  |  &nbsp;  |
| [Režimi rasporeda projekta](../project-management/scheduling-modes.md) – definišite projekat kao fiksne jedinice, fiksno angažovanje ili fiksno trajanje | :heavy_check_mark: | &nbsp; |
| Vremenska osa – napravite i prilagodite prikaz vremenske ose da biste vizuelizovali detalje rasporeda i komunicirali sa zainteresovanim stranama. | :heavy_check_mark:  | &nbsp; |
| Zadaci zasnovani na angažovanju – podrške mehanizma za zakazivanje za zakazivanja zadatka kao zasnovanog na angažovanju  | :heavy_check_mark:  | &nbsp; |
| Dijalog **Informacije o zadatku** – čuvajte detalje o zadatku koristeći dijalog | :heavy_check_mark:  |  &nbsp;  |
| Prevucite i otpustite – izaberite više zadataka i izmenite njihove položaju u SAP-u | :heavy_check_mark: | &nbsp;  |
| Fleksibilni trajni prikazi – definišite detaljnije prikaze atributa zadatka   | :heavy_check_mark:  | &nbsp; |
| Sortiranje i filtriranje SAP-a  | :heavy_check_mark:  | &nbsp; |
| Prikaz tabli za isporuku projekta bez „vodopada“  | :heavy_check_mark:   | &nbsp; |
| Prikaz vremenske ose – interaktivni Gantov grafikon koji se koristi za vizuelizaciju i uređivanje SAP-a   | :heavy_check_mark:  | &nbsp; |
| Tasterske prečice – koristite tasterske prečice za uobičajene operacije, kao što su uvlačenje pasusa ili umetanje  | :heavy_check_mark:  |  &nbsp; |
| Opoziv u više nivoa – obavite „šta-ako“ analizu da biste u potpunosti razumeli uticaj promena tako što ćete stornirati i ponovo primeniti čitav skup operacija | :heavy_check_mark: | &nbsp; |
| Isecite/Kopirajte/Nalepite – sarađujte na razvoju rasporeda kopiranjem i lepljenjem detalja o rasporedu između aplikacija  | :heavy_check_mark: | &nbsp; |
| Kontrolne liste zadataka – dodajte do 20 stavki kontrolne liste zadatku   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Planiranje projekta

Stranica **Projekat** u usluzi Project Operations ima značajan broj razlika u poređenju sa stranicom **Projekat** u usluzi Project Service Automation.

Sledeće radnje su uklonjene sa stranice **Projekti** u sklopu nadogradnje faze 1:

  - **Otvori u programu MS Project**
  - **Kreiraj predložak**
  - **Raskini vezu sa programom MS Project**

Stranica **Projekat** u usluzi Project Operations sadrži sledeće nove kartice.

- **Procena materijala**
- **Podešavanje naplate za zadatak**

Kartica **Status** je uklonjena i polje **Status** se sada nalazi na kartici **Rezime** sa režimom zakazivanja projekta.

   ![Ažuriranja stranice „Projekat“.](media/projectform.png)

Kartica **Raspored** je preimenovana u karticu **Zadatak** i sadrži novo iskustvo planiranja projekta sa uslugom Project for the Web.

   ![Nova kartica zadataka projekta.](media/tasktab.png)

## <a name="scheduling-modes"></a>Režimi planiranja

Project Operations je uveo novu funkciju, [Režimi zakazivanja](../project-management/scheduling-modes.md). Svi postojeći Project Service Automation projekti podrazumevano će imati **Fiksno trajanje** u usluzi Project Operations. Međutim, podrazumevanim vrednostima za nove projekte možete upravljati odlaskom u **Postavke** > **Parametri** > **Parametar** > **Režim rasporeda**.

   ![Postavke parametara projekta za režim rasporeda.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Ograničenja u planiranju projekta

Project Operations se oslanja na Project for the Web za sve operacije planiranja projekta. Project for the Web upravlja strukturnom analizom posla koristeći ograničenja u sledećoj tabeli.

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

## <a name="project-planning-extensibility-and-development"></a>Mogućnost proširenja i razvoja planiranja projekta

Nakon nadogradnje na Project Operations, morate koristiti API-je za planiranje projekta da biste izvršili operacije kreiranja, ažuriranja i brisanja na sledećim entitetima:

|   Naziv entiteta           |   Logičko ime entiteta       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projektni zadatak            | msdyn_projecttask           |
| Zavisnost projektnog zadatka | msdyn_projecttaskdependency |
| Dodela resursa     | msdyn_resourceassignment    |
| Kontejner projekta          | msdyn_projectbucket         |
| Član projektnog tima     | msdyn_projectteam           |

Ako trenutno imate prilagođavanja koja obuhvataju ove entitete, pogledajte članak [Korišćenje API-ja za planiranje projekta za obavljanje operacija sa entitetima planiranja](../project-management/schedule-api-preview.md) gde ćete pronaći smernice za primenu.

## <a name="data-model-changes"></a>Promene u modelu podataka

U sklopu faze 1 nadogradnje, postoje promene u modelu podataka. Ove promene su pre svega promene polja u postojećim entitetima. U fazi 1, entiteti **msydn_project** i **msdyn_projectteam** su refaktorizacija prilagođavanja. 

> [!IMPORTANT]
> Ovaj odeljak će se ažurirati sa dodatnim entitetima dok se buduće faze nadogradnje budu dovršavale.

Sledeća polja su zamenjena novim poljima.

|   Entity          |   Staro logičko ime   |   Novo logičko ime    |
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
| msdyn_project     | msdyn_actualfeesales                         | Prikazuje agregirani iznos stvarne naknade prodaje u projektu. Za korišćenje samo u usluzi Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialcost                     | Prikazuje agregirane stvarne materijalne troškove u projektu. Za korišćenje samo u usluzi Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialsales                    | Prikazuje agregirani iznos stvarne prodaje materijala u projektu. Za korišćenje samo u usluzi Project Service Automation. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Predmet ugovora povezan sa ovim projektom. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Ovo je interno sistemsko polje koje se koristi za **kopiranje projekta** povezanog sa identifikatorom korelacije. Za korišćenje samo u usluzi Project Service Automation. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Ovo je interno sistemsko polje koje se koristi za **kopiranje projekta** povezanog sa identifikatorom sesije. Za korišćenje samo u usluzi Project Service Automation. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Poslednja sinhronizacija xRM tokena za globalnu reviziju iz usluge planiranja projekta. |
| msdyn_project     | msdyn_msprojectdocument                      | Microsoft Project dokument koji pripada projektu. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Zbir planiranih materijalnih troškova u projektu. Za korišćenje samo u usluzi Project Service Automation. |
| msdyn_project     | msdyn_plannedmaterialsales                   | Zbir planirane prodaje materijala u projektu. Za korišćenje samo u usluzi Project Service Automation. |
| msdyn_project     | msdyn_program                                | Program sa kojim je ovaj projekat povezan. |
| msdyn_project     | msdyn_quotelineproject                       | Stavka ponude povezana sa ovim projektom. |
| msdyn_project     | msdyn_replaylogheader                        | Zaglavlje za ponovnu reprodukciju evidencije. |
| msdyn_project     | msdyn_schedulemode                           | Podrazumevani režim rasporeda koji se koristi za sve zadatke u projektu.  |
| msdyn_project     | msdyn_taskearlieststart                      | Najraniji datum početka bilo kog zadatka u projektu.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Član projektnog tima sa kojeg je kopiran ovaj član projektnog tima. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Označava da li treba da se kreira zahtev za resurs za nedavno kreiranog generičkog člana tima.  |
| msdyn_projectteam | msdyn_deletestatus                           | Status brisanja člana tima za praćenje da li se usluzi planiranja projekta šalje zahtev za brisanje i da li ona uspešno vraća odgovor i u očekivanom vremenskom roku. |
| msdyn_projectteam | msdyn_effortcompleted                        | Prati angažovanje koje je član tima dovršio za svoje dodele. |
| msdyn_projectteam | msdyn_effortremaining                        | Prati angažovanje koje član tima treba da završi za svoje dodele. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Period čekanja od vremena kada član tima šalje zahtev za brisanje usluzi planiranja projekta dok član tima zaista ne bude izbrisan u usluzi Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Vremenska oznaka za evidentiranje kada se zahtev za brisanje člana tima pošalje u uslugu planiranja projekta. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Pokazuje člana projektnog tima sa kojeg je kopiran ovaj član projektnog tima.  |

## <a name="project-templates"></a>Predlošci projekata

Project Operations ne obezbeđuje podršku za šablone projekta. Međutim, veći deo osnovne funkcionalnosti možete da replicirate korišćenjem [Project Copy API-ja](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Podrška za programski dodatak za računare

Podrška za Microsoft Project programski dodatak za računare neće biti dostupna tokom prve 2 faze nadogradnje. U fazi 3, klijenti koji imaju projekte veće od trenutno podržanih ograničenja usluge Project for the Web moći će da koriste programski dodatak za računare.

## <a name="editing-resource-assignment-contours"></a>Uređivanje kontura dodeljivanja resursa

Mogućnost uređivanja kontura dodele resursa biće dostupna kada faza 2 nadogradnje bude dostupna.

## <a name="billing-and-pricing"></a>Naplata i određivanje cena

Sledeće nove funkcije su dodate u usluzi Project Operations. Ove funkcije su po prirodi dodatne i ne utiču na Project Service Automation model podataka.

- [Evidentiranje korišćenja materijala na projektima i projektnim zadacima](../material/material-usage-log.md)
- [Upravljanje podugovorima](../pro/subcontracting/managing-subcontracts-overview.md)
- [Avansi i ugovori zasnovani na avansnim uplatama](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Statusom i provere ugovora koje ne smete premašiti](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Naplata zasnovana na zadatku](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Zastarele komponente

Sledeće tabele dokumentuju sva zastarela polja koja su premeštena u rešenje sa zastarelim komponentama nakon nadogradnje. Više informacija i vezu ka rešenju potražite u članku [Dynamics 365 Project Service Automation 3x u Project Operations 4x zastarele komponente](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

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
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
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
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
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

