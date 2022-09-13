---
title: Korišćenje API-ja za raspored projekata uz Power Automate
description: Ovaj članak obezbeđuje probni tok koji koristi programske interfejse aplikacija "Project schedule" (API).
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

Ovaj članak opisuje probni tok koji prikazuje kako se kreira kompletan plan projekta pomoću Microsoft Power Automate korišćenja, kreiranja skupa operacija i načina ažuriranja entiteta. Primer prikazuje kako se kreira projekat, član projektnog tima, Skupovi operacija, projektni zadaci i dodele resursa. Ovaj članak takođe sadrži objašnjenja o tome kako da ažurirate entitet i izvršite skup operacija.

Sledi kompletna lista koraka koji su dokumentovani u probnom toku u ovom članku:

1. [Kreiranje okidača PowerApps](#1)
2. [Kreirajte projekat](#2)
3. [Pokretanje promenljive za člana tima](#3)
4. [Kreiranje generičkog člana tima](#4)
5. [Kreiranje skupa operacija](#5)
6. [Kreiranje kofe projekta](#6)
7. [Pokretanje promenljive za status veze](#7)
8. [Pokretanje promenljive za broj zadataka](#8)
9. [Pokretanje promenljive za ID projektnog zadatka](#9)
10. [Uradite dok](#10)
11. [Postavljanje projektnog zadatka](#11)
12. [Kreiranje projektnog zadatka](#12)
13. [Kreiranje dodele resursa](#13)
14. [Smanjenje promenljive](#14)
15. [Preimenovanje projektnog zadatka](#15)
16. [Pokretanje skupa operacija](#16)

## <a name="assumptions"></a>Pretpostavke

Ovaj članak pretpostavlja da imate osnovno znanje Dataverse o platformi, tokovima oblaka i programskom interfejsu aplikacije Project Schedule (API). Više informacija potražite u odeljku [Reference u](#references) ovom članku.

## <a name="create-a-flow"></a>Napravi tok

### <a name="select-an-environment"></a>Izbor okruženja

Možete da kreirate Power Automate tok u svom okruženju.

1. Idite na <https://flow.microsoft.com> lokaciju i koristite administratorske akreditive za prijavljivanje.
2. U gornjem desnom uglu izaberite stavku **Okruženja**.
3. Sa liste izaberite okruženje u kojem je Dynamics 365 Project Operations instalirano.

### <a name="create-a-solution"></a>Kreiranje rešenja

Sledite ove korake da biste kreirali tok [svestan rešenja](/power-automate/overview-solution-flows). Kreiranjem toka svesnog rešenja možete lakše da izvezete tok da biste ga kasnije koristili.

1. U oknu za navigaciju izaberite stavku **Rešenja**.
2. Na stranici **Rešenja** izaberite **novo rešenje**.
3. U dijalogu **Novo rešenje** postavite potrebna polja, a zatim izaberite stavku **Kreiraj**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a> 1. korak: Kreiranje okidača PowerApps

1. Na stranici **Rešenja** izaberite rešenje koje ste kreirali, a zatim izaberite stavku **Novo**.
2. U levom oknu izaberite opciju **Cloud flows** \> **Automation** \> **Cloud flow** \> **Instant.**
3. U polje Ime **toka** unesite Schedule **API Demo Flow**.
4. U listi Odaberite **kako da pokrenete ovu listu toka** izaberite **Power Apps**. Kada kreirate okidač Power Apps, logika je na vama kao autoru. U ovom članku parametre unosa ostavite prazne u svrhe testiranja.
5. Izaberite **Kreiraj**.

## <a name="step-2-create-a-project"></a><a id="2"></a>2. korak: Kreiranje projekta

Sledite ove korake da biste kreirali uzorak projekta.

1. U toku koji ste kreirali izaberite **novi korak**.

    ![Dodavanje novog koraka.](media/newstep.png)

2. U dijalogu **Izbor operacije**, u polje za pretragu unesite izvršavanje nepovezane **radnje**. Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.

    ![Izbor operacije.](media/chooseactiontab.png)

3. U novom koraku izaberite elipsu (**...), a zatim izaberite** stavku **Preimenuj**.

![Preisići korak.](media/renamestep.png)

4. Preimenujte korak **Kreiranje projekta**.
5. U polju **Ime radnje** izaberite **msdyn\_ CreateProjectV1**.
6. U okviru **polja msdyn\_ tema** izaberite Dodaj **dinamički sadržaj**.
7. Na kartici **Izraz**, u polje funkcije unesite ime **projekta - utcNow()**.
8. Izaberite **U redu**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a> 3. korak: Pokretanje promenljive za člana tima

1. U toku izaberite novi **korak**.
2. U dijalogu **Izbor operacije**, u polje za pretragu unesite promenljivu **pokretanja**. Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.
3. U novom koraku izaberite elipsu (**...), a zatim izaberite** stavku **Preimenuj**.
4. Preimenujte **korak člana Init tima**.
5. U polje **Ime** unesite **TeamMemberAction**.
6. U polju Vrsta izaberite **nisku** **.**
7. U polje **Vrednost** unesite **msdyn\_ CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a> 4. korak: Kreiranje generičkog člana tima

1. U toku izaberite novi **korak**.
2. U dijalogu **Izbor operacije**, u polje za pretragu unesite izvršavanje nepovezane **radnje**. Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.
3. U novom koraku izaberite elipsu (**...), a zatim izaberite** stavku **Preimenuj**.
4. Preimenujte korak **Kreiranje člana tima**.
5. Za polje **Ime radnje** izaberite **TeamMemberAction u** dijalogu Dinamički **sadržaj**.
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

    - **\@\@ odata.type** – Ime entiteta. Na primer, unesite **"Microsoft.Dynamics.CRM.msdyn\_ projectteam"**.
    - **msdyn\_ projectteamid** – Primarni ključ ID projektnog tima. Vrednost je globalno jedinstveni identifikator (GUID) izraz.   ID se generiše sa kartice izraza.

    - **msdyn\_ project\@ odata.bind** – ID projekta. Vrednost će biti dinamički sadržaj koji potiče od odgovora koraka "Kreiraj projekat". Uverite se da ste uneli punu putanju i dodali dinamički sadržaj između zagrada. Potrebni su znaci navoda. Na primer, unesite **"/msdyn\_ projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_** ime – Ime člana tima. Na primer, unesite **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a> 5. korak: Kreiranje skupa operacija

1. U toku izaberite novi **korak**.
2. U dijalogu **Izbor operacije**, u polje za pretragu unesite izvršavanje nepovezane **radnje**. Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.
3. U novom koraku izaberite elipsu (**...), a zatim izaberite** stavku **Preimenuj**.
4. Preimenujte korak **Kreiranje skupa operacija**.
5. U polju **Ime radnje** izaberite msdyn **\_ CreateOperationSetV1 prilagođenu** Dataverse radnju.
6. U polje **Opis** unesite **ScheduleAPIDemoOperationSet**.
7. U polje **Projekat** unesite **/msdyn projekte\_(**.
8. U dijalogu **Dinamički** sadržaj izaberite **msdyn\_ CreateProjectV1Response Project ID**.
9. U polje **Projekat** unesite **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a> 6. korak: Kreiranje kofe projekta

1. U toku izaberite novi **korak**.
2. U dijalogu Izbor operacije **, u polje za pretragu unesite** dodavanje novog reda **.** Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.
3. U novom koraku izaberite elipsu (**...), a zatim izaberite** stavku **Preimenuj**.
4. Preimenujte korak Kreiranje **kofe**.
5. U polju Ime **tabele** izaberite stavku Kofe **projekta**.
6. U polje **Ime** unesite **ScheduleAPIDemoBucket1**.
7. Za polje **Projekat** izaberite **msdyn\_ CreateProjectV1Response ProjectId u** dijalogu Dinamički **sadržaj**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a> 7. korak: Pokretanje promenljive za status veze

1. U toku izaberite novi **korak**.
2. U dijalogu **Izbor operacije**, u polje za pretragu unesite promenljivu **pokretanja**. Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.
3. U novom koraku izaberite elipsu (**...), a zatim izaberite** stavku **Preimenuj**.
4. Preimenujte **korak Init linkstatus**.
5. U polje **Ime** unesite **statistiku veze**.
6. U polju **Vrsta** izaberite ceo **broj**.
7. U polje **Vrednost** unesite **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a> 8. korak: Pokretanje promenljive za broj zadataka

1. U toku izaberite novi **korak**.
2. U dijalogu **Izbor operacije**, u polje za pretragu unesite promenljivu **pokretanja**. Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.
3. U novom koraku izaberite elipsu (**...), a zatim izaberite** stavku **Preimenuj**.
4. Preimenujte **korak Init Broj zadataka**.
5. U polje **Ime** unesite broj **zadataka**.
6. U polju **Vrsta** izaberite ceo **broj**.
7. U polje **Vrednost** unesite **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a> 9. korak: Pokretanje promenljive za ID projektnog zadatka

1. U toku izaberite novi **korak**.
2. U dijalogu **Izbor operacije**, u polje za pretragu unesite promenljivu **pokretanja**. Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.
3. U novom koraku izaberite elipsu (**...), a zatim izaberite** stavku **Preimenuj**.
4. Preimenujte **korak Init ProjectTaskID**.
5. U polje **Ime** unesite broj **zadataka**.
6. U polju Vrsta izaberite **nisku** **.**
7. Za polje **Vrednost** unesite guid **()** u izradu izraza.

## <a name="step-10-do-until"></a><a id="10"></a> 10. korak: Uradite dok

1. U toku izaberite novi **korak**.
2. U dijalogu **Izbor operacije**, u polje za pretragu unesite opciju **uradi do**. Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.
3. Postavite prvu vrednost u uslovnoj izjavi na broj promenljivih **zadataka iz** dijaloga " **Dinamički** sadržaj".
4. Postavite uslov na **manje od jednakog**.
5. Postavite drugu vrednost u uslovnoj izjavi na **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a> 11. korak: Postavljanje projektnog zadatka

1. U toku izaberite novi **korak**.
2. U dijalogu **Izbor operacije**, u polje za pretragu unesite postavljenu **promenljivu**. Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.
3. U novom koraku izaberite elipsu (**...), a zatim izaberite** stavku **Preimenuj**.
4. Preimenujte korak **Skup projektnog zadatka**.
5. U polju **Ime** izaberite **msdyn\_ projecttaskid**.
6. Za polje **Vrednost** unesite guid **()** u izradu izraza.

## <a name="step-12-create-a-project-task"></a><a id="12"></a> 12. korak: Kreiranje projektnog zadatka

Sledite ove korake da biste kreirali projektni zadatak koji ima jedinstveni ID koji pripada trenutnom projektu i kofu projekta koju ste kreirali.

1. U toku izaberite novi **korak**.
2. U dijalogu **Izbor operacije**, u polje za pretragu unesite izvršavanje nepovezane **radnje**. Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.
3. U koraku izaberite elipsu (...), a zatim **izaberite** stavku **Preimenuj**.
4. Preimenujte korak Kreiranje **projektnog zadatka**.
5. U polju **Ime radnje** izaberite **msdyn\_ PssCreateV1**.
6. U polje **Entitet unesite** sledeće informacije o parametrima.

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

    - **\@\@ odata.type** – Ime entiteta. Na primer, unesite **"Microsoft.Dynamics.CRM.msdyn\_ projecttask"**.
    - **msdyn\_ projecttaskid** – Jedinstveni ID zadatka. Vrednost bi trebalo da bude postavljena na dinamičku promenljivu **iz msdyn\_ projecttaskid**.
    - **msdyn\_ project\@ odata.bind** – ID projekta. Vrednost će biti dinamički sadržaj koji potiče od odgovora koraka "Kreiraj projekat". Uverite se da ste uneli punu putanju i dodali dinamički sadržaj između zagrada. Potrebni su znaci navoda. Na primer, unesite **"/msdyn\_ projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_ tema** – Bilo koje ime zadatka.
    - **msdyn\_ projectbucket\@ odata.bind** – Kanta projekta koja sadrži zadatke. Vrednost će biti dinamičan sadržaj koji potiče od odgovora koraka "Kreiraj kofu". Uverite se da ste uneli punu putanju i dodali dinamički sadržaj između zagrada. Potrebni su znaci navoda. Na primer, unesite **"/msdyn\_ projectbuckets(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_ start** – Dinamički sadržaj za datum početka. Na primer, sutra će biti predstavljeno kao **"addDays(utcNow(), 1)"**.
    - **msdyn\_ planiranistart** – Planirani datum početka. Na primer, sutra će biti predstavljeno kao **"addDays(utcNow(), 1)"**.
    - **msdyn\_ scheduleend** – Planirani datum završetka. Izaberite datum u budućnosti. Na primer, navedite **"addDays(utcNow(), 5)"**.
    - **msdyn\_ LinkStatus** – Status veze. Na primer, unesite **"192350000"**.

7. Za polje **OperationSetId** izaberite **msdyn\_ CreateOperationSetV1Response** u dijalogu dinamički **sadržaj**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a> 13. korak: Kreiranje dodeljivanje resursa

1. U toku izaberite novi **korak**.
2. U dijalogu **Izbor operacije**, u polje za pretragu unesite izvršavanje nepovezane **radnje**. Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.
3. U koraku izaberite elipsu (...), a zatim **izaberite** stavku **Preimenuj**.
4. Preimenujte korak **Kreiranje dodele**.
5. U polju **Ime radnje** izaberite **msdyn\_ PssCreateV1**.
6. U polje **Entitet unesite** sledeće informacije o parametrima.

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

7. Za polje **OperationSetId** izaberite **msdyn\_ CreateOperationSetV1Response** u dijalogu dinamički **sadržaj**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a> 14. korak: Smanjenje promenljive

1. U toku izaberite novi **korak**.
2. U dijalogu **Izbor operacije**, u polje za pretragu unesite promenljivu **smanjenja**. Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.
3. U polju **Ime** izaberite broj **zadataka**.
4. U polje **Vrednost** unesite **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a> 15. korak: Preimenovanje projektnog zadatka

1. U toku izaberite novi **korak**.
2. U dijalogu **Izbor operacije**, u polje za pretragu unesite izvršavanje nepovezane **radnje**. Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.
3. U koraku izaberite elipsu (...), a zatim **izaberite** stavku **Preimenuj**.
4. Preimenujte korak Preimenujte **projektni zadatak**.
5. U polju **Ime radnje** izaberite **msdyn\_ PssUpdateV1**.
6. U polje **Entitet unesite** sledeće informacije o parametrima.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Za polje **OperationSetId** izaberite **msdyn\_ CreateOperationSetV1Response** u dijalogu dinamički **sadržaj**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a> 16. korak: Pokretanje skupa operacija

1. U toku izaberite novi **korak**.
2. U dijalogu **Izbor operacije**, u polje za pretragu unesite izvršavanje nepovezane **radnje**. Zatim na kartici **Radnje** izaberite operaciju sa liste rezultata.
3. U koraku izaberite elipsu (...), a zatim **izaberite** stavku **Preimenuj**.
4. Preimenujte korak **Izvrši skup operacija**.
5. U polju **Ime radnje** izaberite **msdyn\_ ExecuteOperationSetV1**.
6. Za polje **OperationSetId** izaberite **msdyn\_ CreateOperationSetV1Response OperationSetId** u **dijalogu Dinamid** sadržaja.

## <a name="references"></a>Reference

- [Pregled načina integrisanja tokova sa Dataverse - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Korišćenje API-ja za raspored projekata za izvođenje operacija sa entitetima raspoređivanja](schedule-api-preview.md)
- [Pregled tokova oblaka - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Pregled tokova svesnih rešenja - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
