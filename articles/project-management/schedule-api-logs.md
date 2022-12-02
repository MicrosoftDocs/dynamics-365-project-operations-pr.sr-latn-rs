---
title: Evidencije rasporeda projekata
description: Ovaj članak pruža informacije i uzorke koji će vam pomoći da koristite evidencije za planiranje projekta da biste pratili kvarove koji su povezani sa uslugom planiranja projekta i API-jem za planiranje projekta.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c57419642e90e4def01f2cd2474c9e82dc162b86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923712"
---
# <a name="project-scheduling-logs"></a>Evidencije rasporeda projekata

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, jednostavnu primenu – pogodbu o predračunima_, _Project for the Web_

Microsoft Dynamics 365 Project Operations koristi [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) kao primarni mehanizam planiranja. Umesto korišćenja standardnih Microsoft Dataverse interfejsa za programiranje veb aplikacija (API-ja), Project Operations koriste nove API-je za planiranje projekta za kreiranje, ažuriranje i brisanje projektnih zadataka, dodela resursa, zavisnosti zadataka, kontejnere projekata i članova projektnih timova. Međutim, kada se operacije kreiranja, ažuriranja ili brisanja programski izvršavaju na entitetima strukturne analize posla (SAP), može doći do grešaka. Da bi se pratile ove greške i istoriju operacija, primenjene su dve nove administrativne evidencije: **Skup operacija** i **Usluge planiranja projekta (PSS)**. Da biste pristupili ovim evidencijama, idite na **Postavke** \> **Integracija rasporeda**.

Sledeća ilustracija prikazuje model podataka za evidencije planiranja projekta.

![Model podataka za evidencije planiranja projekta.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Evidencija skupa operacija

Evidencija skupa operacija prati izvršavanje skupa operacija koji se koristi za pokretanje jedne ili više operacija kreiranja, ažuriranja ili brisanja operacija u grupi projekata, projektnih zadataka, dodela resursa, zavisnosti zadataka, kontejnera projekata ili članova projektnog tima. Polje **Operacija u statusu** prikazuje opšti status skupa operacija. Detalji korisnih podataka skupa operacija se beleže u povezanim zapisima detalja skupa operacija.

### <a name="operation-set"></a>Skup operacija

Sledeća tabela prikazuje polja koja su povezana sa entitetom **Skup operacija**.

| Naziv šeme            | Opis                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Datum i vreme kada je skup operacija završen ili nije uspeo.                                                | CompletedOn            |
| msdyn_correlationid   | Vrednost za **correlationId** zahteva.                                                                  | CorrelationId          |
| msdyn_description     | Opis skupa operacija.                                                                        | Opis            |
| msdyn_executedon      | Datum i vreme izvršavanja zapisa.                                                                       | Datum izvršavanja            |
| msdyn_operationsetId  | Jedinstveni identifikator instanci entiteta.                                                                   | OperationSet           |
| msdyn_Project         | Projekat koji se odnosi na skup operacija.                                                            | Project                |
| msdyn_projectid       | Vrednost za **projectId** zahteva.                                                                      | ProjectId (zastarelo) |
| msdyn_projectName     | Nije primenljivo.                                                                                              | Nije primenjivo         |
| msdyn_PSSErrorLog     | Jedinstveni identifikator evidencije grešaka usluge planiranja projekta koja je povezana sa skupom operacija. | PSS evidencija grešaka          |
| msdyn_PSSErrorLogName | Nije primenljivo.                                                                                              | Nije primenjivo         |
| msdyn_status          | Status skupa operacija.                                                                             | Status                 |
| msdyn_statusName      | Nije primenljivo.                                                                                              | Nije primenjivo         |
| msdyn_useraadid       | ID Azure Active Directory (Azure AD) objekta korisnika kome zahtev pripada.                     | UserAADID              |

### <a name="operation-set-detail"></a>Detalj skupa operacija

Sledeća tabela prikazuje polja koja su povezana sa entitetom **Detalj skupa operacija**.

| Naziv šeme                 | Opis                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Serijalizovana Dataverse polja za zahtev.                                            | CdsPayload            |
| msdyn_entityname           | Naziv entiteta za zahtev.                                                     | EntityName            |
| msdyn_httpverb             | Metod zahteva.                                                                         | HTTP glagol (zastarelo) |
| msdyn_httpverbName         | Nije primenljivo.                                                                             | Nije primenjivo        |
| msdyn_operationset         | Jedinstveni identifikator skupa operacija kojem zapis pripada.                      | OperationSet          |
| msdyn_operationsetdetailId | Jedinstveni identifikator instanci entiteta.                                                  | OperationSet detalj   |
| msdyn_operationsetName     | Nije primenljivo.                                                                             | Nije primenjivo        |
| msdyn_operationtype        | Tip operacije detalja skupa operacija.                                             | OperationType         |
| msdyn_operationtypeName    | Nije primenljivo.                                                                             | Nije primenjivo        |
| msdyn_psspayload           | Serijalizovana polja usluge planiranja projekta za zahtev.                           | PssPayload            |
| msdyn_recordid             | Identifikator zapisa zahteva.                                                       | ID zapisa             |
| msdyn_requestnumber        | Automatski generisani broj koji identifikuje redosled primanja zahteva. | Broj zahteva        |

## <a name="project-scheduling-service-error-logs"></a>Evidencije grešaka usluge planiranja projekta

Evidencije grešaka usluge planiranja projekta evidentira greške do kojih dolazi kada usluga planiranja projekta pokuša operaciju **Sačuvaj** ili **Otvori**. Postoje tri podržana scenarija u kojima se generišu ove evidencije:

- Radnje koje je pokrenuo korisnik kritički ne uspevaju (na primer, nije moguće kreirati dodelu zbog privilegija koje nedostaju).
- Usluga planiranja projekta ne može programski da kreira, ažurira, izbriše ili izvrši bilo koju drugu kaskadnu operaciju u entitetu.
- Korisnik doživljava greške kada se zapis ne otvori (na primer, kada se projekat otvori ili kada se ažuriraju informacije o članu tima).

### <a name="project-scheduling-service-log"></a>Evidencija usluge planiranja projekta

Sledeća tabela prikazuje polja koja su obuhvaćena evidencijom usluge planiranja projekta.

| Naziv šeme          | Opis                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Stek poziv izuzetka.                                               | Stek poziv     |
| msdyn_correlationid | ID korelacije greške.                                               | CorrelationId  |
| msdyn_errorcode     | Polje koje se koristi za skladištenje Dataverse koda greške ili HTTP koda greške. | Kod greške     |
| msdyn_HelpLink      | Veza do javne dokumentacije za pomoć.                                       | Veza za pomoć      |
| msdyn_log           | Evidencija iz usluge planiranja projekta.                                   | Evidencija            |
| msdyn_project       | Projekat koji je povezan sa odeljkom evidencijom grešaka.                             | Project        |
| msdyn_projectName   | Naziv projekta ako će korisni podaci skupa operacija biti zadržani. | Nije primenjivo |
| msdyn_psserrorlogId | Jedinstveni identifikator instanci entiteta.                                     | PSS evidencija grešaka  |
| msdyn_SessionId     | ID sesije projekta.                                                        | ID sesije     |

## <a name="error-log-cleanup"></a>Čišćenje evidencije grešaka

Podrazumevano, i evidencije grešaka usluge planiranja projekta i evidencija skupa operacija mogu da se brišu svakih 90 dana. Svi zapisi stariji od 90 dana biće obrisani. Međutim, promenom vrednosti polja **msdyn_StateOperationSetAge** na stranici **Parametri projekta**, administratori mogu da prilagode opseg čišćenja tako da bude između 1 i 120 dana. Dostupno je nekoliko metoda za promenu ove vrednosti:

- Prilagodite entitet **Parametar projekta** kreiranjem prilagođene stranice i dodavanjem polja **Starost zastarelog skupa operacija**.
- Koristite kôd klijenta koji koristi [WebApi komplet za razvoj softvera (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Koristite SDK kôd usluge koji koristi metod Xrm SDK **updateRecord** (referenca API-ja klijenta) u aplikacijama zasnovanim na modelu. Power Apps obuhvata opis i podržane parametre za metod **updateRecord**.

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
