---
title: Evidencije planiranje projekta
description: Ova tema pruža informacije i uzorke koji će vam pomoći da koristite evidencije za planiranje projekta da biste pratili kvarove koji su povezani sa uslugom zakazivanja projekta i API-jem za planiranje projekta.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1c5632a880fa30d1b863c326b22e3d930c9564dc
ms.sourcegitcommit: 844ec8eacd0fc10d1659b437cc5cbb4480ec9e1e
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 12/01/2021
ms.locfileid: "7877518"
---
# <a name="project-scheduling-logs"></a>Evidencije planiranje projekta

_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_, _Project for the Web_

Microsoft Dynamics 365 Project Operations koristi [Project za Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) kao svoju mašinu za primarno planiranje. Umesto korišćenja standardnih programskih interfejsa (API) Web aplikacije Microsoft Dataverse), operacije projekta koriste nove API-je za planiranje projekta za kreiranje, ažuriranje i brisanje projektnih zadataka, dodeljivanja resursa, zavisnosti od zadataka, kofa projekta i članova projektnih timova. Međutim, kada se operacije kreiranja, ažuriranja ili brisanja programski pokreću na entitetima strukture radne analize (WBS). Da biste pratili ove greške i istoriju operacija, primenjene su dve nove administrativne evidencije: Usluga skupa operacija i planiranje **projekta** **(PSS).** Da biste pristupili ovim evidencijama, idite na stranicu **"Integracija** \> **rasporeda** postavki".

Sledeća ilustracija prikazuje model podataka za evidencije planiranje projekta.

![Model podataka za evidencije planiranje projekta.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Evidencija skupa operacija

Evidencija skupa operacija prati izvršavanje skupa operacija koji se koristi za pokretanje jedne ili više operacija kreiranja, ažuriranja ili brisanja operacija u grupi projekata, projektnih zadataka, dodela resursa, zavisnosti od zadataka, kofa projekta ili članova projektnog tima. Polje **Operacija u** statusu prikazuje ukupan status skupa operacija. Detalji tovara postavljenog za operaciju se zarobe u srodnim zapisima detalja skupa operacija.

### <a name="operation-set"></a>Skup operacija

Sledeća tabela prikazuje polja koja su povezana sa **entitetom skupa** operacija.

| SchemaName            | Opis                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Datum/vreme kada je skup operacija dovršen ili nije uspeo.                                                | CompletedOn            |
| msdyn_correlationid   | ID **vrednosti** ID-a korelacije zahteva.                                                                  | CorrelationId          |
| msdyn_description     | Opis skupa operacija.                                                                        | Opis            |
| msdyn_executedon      | Datum/vreme kada je zapis objavljen.                                                                       | Izvršeno dana            |
| msdyn_operationsetId  | Jedinstveni identifikator instanci entiteta.                                                                   | OperationSet           |
| msdyn_Project         | Projekat koji je povezan sa skupom operacija.                                                            | Project                |
| msdyn_projectid       | ID **vrednosti** projekta zahteva.                                                                      | ProjectId (zastarelo) |
| msdyn_projectName     | Nije primenljivo.                                                                                              | Nije primenjivo         |
| msdyn_PSSErrorLog     | Jedinstveni identifikator evidencije grešaka usluge planiranje projekta koja je povezana sa skupom operacija. | PSS evidencija grešaka          |
| msdyn_PSSErrorLogName | Nije primenljivo.                                                                                              | Nije primenjivo         |
| msdyn_status          | Status skupa operacija.                                                                             | Status                 |
| msdyn_statusName      | Nije primenljivo.                                                                                              | Nije primenjivo         |
| msdyn_useraadid       | ID Azure Active Directory (Azure AD) objekta korisnika kome zahtev pripada.                     | UserAADID              |

### <a name="operation-set-detail"></a>Detalji skupa operacija

Sledeća tabela prikazuje polja koja su povezana sa entitetom **detalja skupa** operacija.

| SchemaName                 | Opis                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Serijski Dataverse polja za zahtev.                                            | CdsPayload            |
| msdyn_entityname           | Ime entiteta za zahtev.                                                     | EntityName            |
| msdyn_httpverb             | Metod zahteva.                                                                         | HTTP glagol (zastarelo) |
| msdyn_httpverbName         | Nije primenljivo.                                                                             | Nije primenjivo        |
| msdyn_operationset         | Jedinstveni identifikator skupa operacija kojem zapis pripada.                      | OperationSet          |
| msdyn_operationsetdetailId | Jedinstveni identifikator instanci entiteta.                                                  | OperationSet detalj   |
| msdyn_operationsetName     | Nije primenljivo.                                                                             | Nije primenjivo        |
| msdyn_operationtype        | Tip operacije skupa detalja.                                             | OperationType         |
| msdyn_operationtypeName    | Nije primenljivo.                                                                             | Nije primenjivo        |
| msdyn_psspayload           | Serijalizovana polja Usluga planiranje projekta za zahtev.                           | PssPayload            |
| msdyn_recordid             | Identifikator zapisa zahteva.                                                       | ID zapisa             |
| msdyn_requestnumber        | Automatski generisani broj koji identifikuje porudžbinu u kojoj su primljeni zahtevi. | Broj zahteva        |

## <a name="project-scheduling-service-error-logs"></a>Evidencije grešaka usluge projektovanja

Usluga za planiranje projekta evidentira greške hvatanja do kojih dolazi kada usluga za planiranje projekta pokuša **operaciju** "Sačuvaj" ili **·** "Otvori". Postoje tri podržana scenarija u kojima se generišu ove evidencije:

- Radnje koje je pokrenuo korisnik kritički ne uspevaju (na primer, nije moguće kreirati dodelu zbog privilegija koje nedostaju).
- Usluga projektovanja ne može programski da kreira, ažurira, izbriše ili izvrši bilo koju drugu kaskadnu operaciju u entitetu.
- Korisnik doživljava greške kada se zapis ne otvori (na primer, kada se otvori projekat ili kada se ažuriraju informacije člana tima).

### <a name="project-scheduling-service-log"></a>Evidencija usluge planiranje projekta

Sledeća tabela prikazuje polja koja su uključena u evidenciju usluge planiranje projekta.

| SchemaName          | Opis                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Stek poziv izuzetka.                                               | Stek poziv     |
| msdyn_correlationid | ID korelacije greške.                                               | CorrelationId  |
| msdyn_errorcode     | Polje koje se koristi za skladištenje Dataverse greške ili HTTP koda greške. | Kod greške     |
| msdyn_HelpLink      | Veza sa dokumentacijom javne pomoći.                                       | Veza za pomoć      |
| msdyn_log           | Evidencija iz usluge planiranje projekta.                                   | Evidencija            |
| msdyn_project       | Projekat koji je povezan sa evidencijom grešaka.                             | Project        |
| msdyn_projectName   | Ime projekta ako će tovar skupa operacija biti istrajan. | Nije primenjivo |
| msdyn_psserrorlogId | Jedinstveni identifikator instanci entiteta.                                     | PSS evidencija grešaka  |
| msdyn_SessionId     | ID sesije projekta.                                                        | ID sesije     |

## <a name="error-log-cleanup"></a>Čišćenje evidencije grešaka

Podrazumevano, i evidencije grešaka usluge planiranje projekta i evidencija operativnog skupa mogu da se očiste svakih 90 dana. Svi zapisi stariji od 90 dana biće izbrisani. Međutim, promenom vrednosti polja msdyn_StateOperationSetAge **na** **stranici "Parametri projekta", administratori mogu da prilagode** opseg čišćenja tako da bude između 1 i 120 dana. Dostupno je nekoliko metoda za promenu ove vrednosti:

- Prilagodite **entitet Parametar** projekta kreiranjem prilagođene stranice i dodavanjem polja **"Starost postavke bajatih** operacija".
- Koristite kôd klijenta [koji koristi WebApi komplet za razvoj softvera (SDK).](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord)
- Koristite SDK kôd usluge koji koristi Xrm SDK **metod ažuriranjaRecord** (Referenca klijenta API) u aplikacijama koje pokreću modeli. Power Apps sadrži opis i podržane parametre za metod **ažuriranjaRecord**.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
