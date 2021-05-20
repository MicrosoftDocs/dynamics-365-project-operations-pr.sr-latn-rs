---
title: Razvijte predloške projekata pomoću opcije za kopiranje projekata
description: Ova tema pruža informacije o tome kako kreirati predloške projekata pomoću prilagođene radnje Kopiranje projekta.
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cc17df0c73b276048f7c4b04bd9dc6644e828dc0
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949831"
---
# <a name="develop-project-templates-with-copy-project"></a>Razvijte predloške projekata pomoću opcije za kopiranje projekata

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations podržava mogućnost kopiranja projekta i vraćanja bilo kojih zadataka generičkim resursima koji predstavljaju ulogu. Klijenti mogu da koriste ovu funkcionalnost za izradu osnovnih predložaka projekata.

Kada odaberete **Kopiraj projekat**, status ciljnog projekta se ažurira. Koristite **Razlog statusa** da bi se utvrdilo kada je akcija kopiranja završena. Izbor **Kopiraj projekat** takođe ažurira datum početka projekta na trenutni datum početka ako nije otkriven ciljni datum u ciljnom entitetu projekta.

## <a name="copy-project-custom-action"></a>Prilagođena radnja kopiranja projekta 

### <a name="name"></a>Imenuj 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Ulazni parametri
Postoje tri ulazna parametra:

| Parametar          | Tip   | Vrednosti                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** ili **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Referentni entitet | Izvorni projekat |
| Cilj             | Referentni entitet | Ciljni projekat |


- **{"clearTeamsAndAssignments":true}**: Podrazumevano ponašanje za Project za veb i ukloniće sve zadatke i članove tima.
- **{"removeNamedResources":true}** Podrazumevano ponašanje za Project Operations i vratiće zadatke na generičke resurse.

Za više podrazumevanih vrednosti radnji pogledajte [Koristite veb API radnje](/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Navedite polja za kopiranje 
Kada je akcija pozvana, **Kopiraj projekat** pogledaće prikaz projekta **Kopirajte kolone projekta** da bi se utvrdilo koja polja treba kopirati kada se projekat kopira.


### <a name="example"></a>Primer
Sledeći primer pokazuje kako da pozovete prilagođenu radnju **CopyProject** pomoću skupa parametara **removeNamedResources**.
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

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
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```


[!INCLUDE[footer-include](../includes/footer-banner.md)]