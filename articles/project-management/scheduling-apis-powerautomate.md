---
title: Korišćenje API-ja za raspored projekata uz Power Automate
description: Ovaj članak obezbeđuje probni tok koji koristi interfejse za programiranje (API-je) za raspored projekta.
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: afec082c680596e8dcb8ec0b350b4bb7853c49ff
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404463"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Korišćenje API-ja za raspored projekata uz Power Automate

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Ovaj članak opisuje probni tok koji prikazuje kako se kreira kompletan plan projekta pomoću usluge Microsoft Power Automate, kako se kreira skup operacija i kako se ažuriraju entiteti. Primer prikazuje kako se kreira projekat, član projektnog tima, skupovi operacija, projektni zadaci i dodele resursa. Ovaj članak takođe objašnjava kako da ažurirate entitet i izvršite skup operacija.

Sledi kompletna lista koraka koji su dokumentovani u probnom toku u ovom članku:

1. [Kreiranje PowerApps okidača](#1)
2. [Kreirajte projekat](#2)
3. [Pokretanje promenljive za člana tima](#3)
4. [Kreiranje generičkog člana tima](#4)
5. [Kreiranje skupa opcija](#5)
6. [Kreiranje kontejnera projekta](#6)
7. [Pokretanje promenljive za status veze](#7)
8. [Pokretanje promenljive za broj zadataka](#8)
9. [Pokretanje promenljive za ID projektnog zadataka](#9)
10. [Uraditi do](#10)
11. [Podešavanje projektnog zadatka](#11)
12. [Kreiranje projektnog zadatka](#12)
13. [Kreiranje dodele resursa](#13)
14. [Smanjenje promenljive](#14)
15. [Preimenovanje projektnog zadatka](#15)
16. [Izvršavanje skupa opcija](#16)

## <a name="assumptions"></a>Pretpostavke

Ovaj članak pretpostavlja da imate osnovno znanje o platformi Dataverse, tokovima u oblaku i interfejsu za programiranje aplikacije (API) za raspored projekta. Za više informacija pogledajte odeljak [Reference](#references) kasnije u ovom članku.

## <a name="create-a-flow"></a>Napravi tok

### <a name="select-an-environment"></a>Izbor okruženja

Ne možete da kreirate Power Automate tok u svom okruženju.

1. Idite na <https://flow.microsoft.com> i koristite akreditive administratora da se prijavite.
2. U gornjem desnom uglu izaberite **Okruženja**.
3. Sa liste izaberite okruženje u kojem je instalirana usluga Dynamics 365 Project Operations.

### <a name="create-a-solution"></a>Kreiranje rešenja

Pratite ove korake da biste kreirali [tok koji prati rešenje](/power-automate/overview-solution-flows). Kreiranjem toka koji prati rešenje možete lakše da izvezete tok da biste ga kasnije koristili.

1. U oknu za navigaciju izaberite **Rešenja**.
2. Na stranici **Rešenja** izaberite **Novo rešenje**.
3. U dijalogu **Novo rešenje**, postavite potrebna polja, pa izaberite **Kreiraj**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>1. korak: Kreiranje PowerApps okidača

1. Na stranici **Rešenja**, izaberite rešenje koje ste kreirali, a zatim izaberite **Novo**.
2. U levom oknu izaberite **Tokovi u oblaku** \> **Automatizacija** \> **Tok u oblaku** \> **Trenutno**.
3. U polje **Naziv toka** unesite **Zakaži API demo tok**.
4. Na listi **Odaberite kako da pokrenete ovaj tok**, izaberite **Power Apps**. Kada kreirate Power Apps okidač, logika je na vama kao autoru. U ovom članku parametre unosa ostavite prazne u svrhe testiranja.
5. Izaberite **Kreiraj**.

## <a name="step-2-create-a-project"></a><a id="2"></a>2. korak: Kreiranje projekta

Sledite ove korake za kreiranje primera projekta.

1. U toku koji ste kreirali izaberite **Novi korak**.

    ![Dodavanje novog koraka.](media/newstep.png)

2. U dijalogu **Izbor operacije**, u polje za pretragu unesite **izvršavanje nepovezane radnje** . Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.

    ![Izbor operacije.](media/chooseactiontab.png)

3. U novom koraku izaberite tri tačke (**...**), a zatim izaberite **Preimenuj**.

![Preimenovanje koraka.](media/renamestep.png)

4. Preimenujte korak **Kreiranje projekta**.
5. U polju **Naziv radnje** izaberite **msdyn\_CreateProjectV1**.
6. U okviru polja **msdyn\_subject** izaberite **Dodavanje dinamičkog sadržaja**.
7. Na kartici **Izraz**, u polje funkcije unesite **Naziv projekta – utcNow()**.
8. Izaberite **U redu**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>3. korak: Pokretanje promenljive za člana tima

1. U toku izaberite **Novi korak**.
2. U dijalogu **Izbor operacije**, u polje za pretragu unesite **iniciranje promenljive** . Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.
3. U novom koraku izaberite tri tačke (**...**), a zatim izaberite **Preimenuj**.
4. Preimenujte korak **Iniciranje člana tima**.
5. U polju **Naziv**, unesite **TeamMemberAction**.
6. U polju **Tip posla** izaberite **Niska**.
7. U polju **Vrednost** unesite **msdyn\_CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>4. korak: Kreiranje generičkog člana tima

1. U toku izaberite **Novi korak**.
2. U dijalogu **Izbor operacije**, u polje za pretragu unesite **izvršavanje nepovezane radnje** . Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.
3. U novom koraku izaberite tri tačke (**...**), a zatim izaberite **Preimenuj**.
4. Preimenujte korak **Kreiranje člana tima**.
5. Za polje **Naziv radnje** izaberite **TeamMemberAction** u dijalogu **Dinamički sadržaj**.
6. U polje **Parametri radnje** unesite sledeće informacije o parametrima.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    Evo objašnjenja parametara:

    - **\@\@odata.type** – Naziv entiteta. Na primer, unesite **"Microsoft.Dynamics.CRM.msdyn\_projectteam"**.
    - **msdyn\_projectteamid** – Primarni ključ ID-a projektnog tima. Vrednost je univerzalni jedinstveni identifikator (GUID) izraz.   ID se generiše sa kartice izraza.

    - **msdyn\_project\@odata.bind** – ID projekta projekta-vlasnika. Vrednost će biti dinamički sadržaj koji potiče od odgovora koraka „Kreiranje projekta“. Uverite se da ste uneli punu putanju i dodali dinamički sadržaj između zagrada. Potrebni su znaci navoda. Na primer, unesite **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_name** – Naziv člana tima. Na primer, unesite **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>5, korak: Kreiranje skupa operacija

1. U toku izaberite **Novi korak**.
2. U dijalogu **Izbor operacije**, u polje za pretragu unesite **izvršavanje nepovezane radnje** . Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.
3. U novom koraku izaberite tri tačke (**...**), a zatim izaberite **Preimenuj**.
4. Preimenujte korak **Kreiranje skupa operacija**.
5. U polju **Naziv radnje** izaberite **msdyn\_CreateOperationSetV1** Dataverse prilagođenu radnju.
6. U polje **Opis** unesite **ScheduleAPIDemoOperationSet**.
7. U polje **Projekat** unesite **/msdyn\_projects(**.
8. U dijalogu **Dinamički sadržaj** izaberite **msdyn\_CreateProjectV1Response ProjectId**.
9. U polje **Projekat** unesite **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>6. korak: Kreiranje kontejnera

1. U toku izaberite **Novi korak**.
2. U dijalogu **Izbor operacije**, u polje za pretragu unesite **dodavanje novog reda** . Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.
3. U novom koraku izaberite tri tačke (**...**), a zatim izaberite **Preimenuj**.
4. Preimenujte korak **Kreiranje kontejnera**.
5. U polju **Naziv tabele**, izaberite **Kontejneri projekta**.
6. U polje **Naziv** unesite **ScheduleAPIDemoBucket1**.
7. Za polje **Projekat** izaberite **msdyn\_CreateProjectV1Response ProjectId** u dijalogu **Dinamički sadržaj**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>7. korak: Pokretanje promenljive za status veze

1. U toku izaberite **Novi korak**.
2. U dijalogu **Izbor operacije**, u polje za pretragu unesite **iniciranje promenljive** . Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.
3. U novom koraku izaberite tri tačke (**...**), a zatim izaberite **Preimenuj**.
4. Preimenujte korak **Iniciranje linkstatus**.
5. U polju **Naziv**, unesite **linkstatus**.
6. U polju **Tip posla** izaberite **Ceo broj**.
7. U polje **Vrednost** unesite **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>8. korak: Pokretanje promenljive za broj zadataka

1. U toku izaberite **Novi korak**.
2. U dijalogu **Izbor operacije**, u polje za pretragu unesite **iniciranje promenljive** . Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.
3. U novom koraku izaberite tri tačke (**...**), a zatim izaberite **Preimenuj**.
4. Preimenujte korak **Iniciranje broja zadataka**.
5. U polju **Naziv**, unesite **broj zadataka**.
6. U polju **Tip posla** izaberite **Ceo broj**.
7. U polje **Vrednost** unesite **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>9. korak: Pokretanje promenljive za ID projektnog zadataka

1. U toku izaberite **Novi korak**.
2. U dijalogu **Izbor operacije**, u polje za pretragu unesite **iniciranje promenljive** . Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.
3. U novom koraku izaberite tri tačke (**...**), a zatim izaberite **Preimenuj**.
4. Preimenujte korak **Iniciranje ProjectTaskID**.
5. U polju **Naziv**, unesite **broj zadataka**.
6. U polju **Tip posla** izaberite **Niska**.
7. Za polje **Vrednost** unesite **guid()** u izradi izraza.

## <a name="step-10-do-until"></a><a id="10"></a>10. korak: Uradite do

1. U toku izaberite **Novi korak**.
2. U dijalogu **Izbor operacije**, u polje za pretragu unesite **uradi do** . Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.
3. Postavite prvu vrednost u uslovnoj izjavi na promenljivu **broj zadataka** iz dijaloga **Dinamički sadržaj**.
4. Postavite uslov na **manje od jednako**.
5. Postavite drugu vrednost u uslovnoj izjavi na **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a>11. korak. Podešavanje projektnog zadatka

1. U toku izaberite **Novi korak**.
2. U dijalogu **Izbor operacije**, u polje za pretragu unesite **podešavanje promenljive** . Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.
3. U novom koraku izaberite tri tačke (**...**), a zatim izaberite **Preimenuj**.
4. Preimenujte korak **Podešavanje projektnog zadatka**.
5. U polju **Naziv** izaberite **msdyn\_projecttaskid**.
6. Za polje **Vrednost** unesite **guid()** u izradi izraza.

## <a name="step-12-create-a-project-task"></a><a id="12"></a>12. korak: Kreiranje projektnog zadatka

Sledite ove korake da biste kreirali projektni zadatak koji ima jedinstveni ID koji pripada trenutnom projektu i kontejner projekta koji ste kreirali.

1. U toku izaberite **Novi korak**.
2. U dijalogu **Izbor operacije**, u polje za pretragu unesite **izvršavanje nepovezane radnje** . Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.
3. U koraku izaberite tri tačke (**...**), a zatim izaberite **Preimenuj**.
4. Preimenujte korak **Kreiranje projektnog zadatka**.
5. U polju **Naziv radnje** izaberite **msdyn\_PssCreateV1**.
6. U polje **Entitet** unesite sledeće informacije o parametrima.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    Evo objašnjenja parametara:

    - **\@\@odata.type** – Naziv entiteta. Na primer, unesite **"Microsoft.Dynamics.CRM.msdyn\_projecttask"**.
    - **msdyn\_projecttaskid** – Jedinstveni ID zadatka. Vrednost bi trebalo da bude postavljena na dinamičku promenljivu iz **msdyn\_projecttaskid**.
    - **msdyn\_project\@odata.bind** – ID projekta projekta-vlasnika. Vrednost će biti dinamički sadržaj koji potiče od odgovora koraka „Kreiranje projekta“. Uverite se da ste uneli punu putanju i dodali dinamički sadržaj između zagrada. Potrebni su znaci navoda. Na primer, unesite **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_subject** – Bilo koji naziv zadatka.
    - **msdyn\_projectbucket\@odata.bind** – Kontejner projekta koji sadrži zadatke. Vrednost će biti dinamički sadržaj koji potiče od odgovora koraka „Kreiranje kontejnera“. Uverite se da ste uneli punu putanju i dodali dinamički sadržaj između zagrada. Potrebni su znaci navoda. Na primer, unesite **"/msdyn\_projectbuckets(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_start** – Dinamički sadržaj za datum početka. Na primer, sutra će biti predstavljeno kao **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduledstart** – Planirani datum početka. Na primer, sutra će biti predstavljeno kao **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduleend** – Planirani datum završetka. Izaberite datum u budućnosti. Na primer, navedite **"addDays(utcNow(), 5)"**.
    - **msdyn\_LinkStatus** – Status veze. Na primer, unesite **"192350000"**.

7. Za polje **OperationSetId** izaberite **msdyn\_CreateOperationSetV1Response** u dijalogu **Dinamički sadržaj**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>Korak 13: Kreiranje dodele resursa

1. U toku izaberite **Novi korak**.
2. U dijalogu **Izbor operacije**, u polje za pretragu unesite **izvršavanje nepovezane radnje** . Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.
3. U koraku izaberite tri tačke (**...**), a zatim izaberite **Preimenuj**.
4. Preimenujte korak **Kreiranje dodele**.
5. U polju **Naziv radnje** izaberite **msdyn\_PssCreateV1**.
6. U polje **Entitet** unesite sledeće informacije o parametrima.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. Za polje **OperationSetId** izaberite **msdyn\_CreateOperationSetV1Response** u dijalogu **Dinamički sadržaj**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>14. korak: Smanjenje promenljive

1. U toku izaberite **Novi korak**.
2. U dijalogu **Izbor operacije**, u polje za pretragu unesite **smanjenje promenljive** . Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.
3. U polju **Naziv** izaberite **broj zadataka**.
4. U polje **Vrednost** unesite **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>15. korak. Preimenovanje projektnog zadatka

1. U toku izaberite **Novi korak**.
2. U dijalogu **Izbor operacije**, u polje za pretragu unesite **izvršavanje nepovezane radnje** . Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.
3. U koraku izaberite tri tačke (**...**), a zatim izaberite **Preimenuj**.
4. Preimenujte korak **Preimenovanje projektnog zadatka**.
5. U polju **Naziv radnje** izaberite **msdyn\_PssUpdateV1**.
6. U polje **Entitet** unesite sledeće informacije o parametrima.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Za polje **OperationSetId** izaberite **msdyn\_CreateOperationSetV1Response** u dijalogu **Dinamički sadržaj**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>16, korak: Izvršavanje skupa operacija

1. U toku izaberite **Novi korak**.
2. U dijalogu **Izbor operacije**, u polje za pretragu unesite **izvršavanje nepovezane radnje** . Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.
3. U koraku izaberite tri tačke (**...**), a zatim izaberite **Preimenuj**.
4. Preimenujte korak **Izvršavanje skupa operacija**.
5. U polju **Naziv radnje** izaberite **msdyn\_ExecuteOperationSetV1**.
6. Za polje **OperationSetId** izaberite **msdyn\_CreateOperationSetV1Response OperationSetId** u dijalogu **Dinamički sadržaj**.

## <a name="references"></a>Reference

- [Pregled načina integracije tokova sa uslugom Dataverse – Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Korišćenje API-ja za raspored projekata za izvođenje operacija sa entitetima raspoređivanja](schedule-api-preview.md)
- [Pregled tokova u oblaku – Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Pregled tokova koji prate rešenja – Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
