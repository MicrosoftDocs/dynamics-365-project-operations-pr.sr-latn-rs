---
title: Razvijte predloške projekata pomoću opcije za kopiranje projekata
description: Ovaj članak pruža informacije o kreiranju predložaka projekta pomoću prilagođene radnje projekta Kopiranje.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 47c1023bbc4c21e3571bffbf3670bf0f7854f81d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923849"
---
# <a name="develop-project-templates-with-copy-project"></a>Razvijte predloške projekata pomoću opcije za kopiranje projekata

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Dynamics 365 Project Operations podržava mogućnost kopiranja projekta i vraćanja bilo kojih zadataka generičkim resursima koji predstavljaju ulogu. Klijenti mogu da koriste ovu funkcionalnost za izradu osnovnih predložaka projekata.

Kada odaberete **Kopiraj projekat**, status ciljnog projekta se ažurira. Koristite **Razlog statusa** da bi se utvrdilo kada je akcija kopiranja završena. Izbor **Kopiraj projekat** takođe ažurira datum početka projekta na trenutni datum početka ako nije otkriven ciljni datum u ciljnom entitetu projekta.

## <a name="copy-project-custom-action"></a>Prilagođena radnja kopiranja projekta

### <a name="name"></a>Imenuj 

msdyn\_ CopyProjectV3

### <a name="input-parameters"></a>Ulazni parametri

Postoje tri ulazna parametra:

- **ReplaceNamedResources** ili **ClearTeamsAndAssignments** – Postavite samo jednu od opcija. Ne postavljaj oba.

    - **\{"ReplaceNamedResources":true\}** – Podrazumevano ponašanje za projektne operacije. Svi imenovani resursi se zamenjuju generičkim resursima.
    - **\{"ClearTeamsAndAssignments":true\}** – Podrazumevano ponašanje za Projekat za Web. Svi zadaci i članovi tima su uklonjeni.

- **SourceProject** – Referenca entiteta izvornog projekta iz kojeg treba kopirati. Ovaj parametar ne može biti bez vrednosti.
- **Cilj** – Referenca entiteta ciljnog projekta u koji treba kopirati. Ovaj parametar ne može biti bez vrednosti.

Sledeća tabela obezbeđuje rezime tri parametra.

| Parametar                | Tip             | Vrednost                 |
|--------------------------|------------------|-----------------------|
| ZameniNamedResources    | Boolean          | **Tačno ili** netačno **·** |
| ClearTeamsAndAssignments | Boolean          | **Tačno ili** netačno **·** |
| SourceProject            | Referentni entitet | Izvorni projekat    |
| Cilj                   | Referentni entitet | Ciljni projekat    |

Više podrazumevanih vrednosti radnji potražite u članku [Korišćenje Radnji sa Web API-ja](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Provere valjanosti

Sledeće provere valjanosti su završene.

1. Null proverava i preuzima izvorne i ciljne projekte kako bi potvrdio postojanje oba projekta u organizaciji.
2. Sistem proverava da li je ciljni projekat važeći za kopiranje verifikacijom sledećih uslova:

    - Ne postoji prethodna aktivnost na projektu (uključujući izbor kartice " **Zadaci** ") i projekat je novokreiran.
    - Ne postoji prethodna kopija, nije zahtevan uvoz na ovom projektu, a projekat nema status "Neuspešno **·**".

3. Operacija se ne poziva pomoću HTTP-a.

## <a name="specify-fields-to-copy"></a>Navedite polja za kopiranje

Kada je akcija pozvana, **Kopiraj projekat** pogledaće prikaz projekta **Kopirajte kolone projekta** da bi se utvrdilo koja polja treba kopirati kada se projekat kopira.

### <a name="example"></a>Primer

Sledeći primer prikazuje kako se naziva copyProjectV3 **prilagođena** radnja sa skupom **parametara RemoveNamedResources**.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
