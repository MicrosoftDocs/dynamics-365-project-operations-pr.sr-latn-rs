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
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="eec43-103">Razvijte predloške projekata pomoću opcije za kopiranje projekata</span><span class="sxs-lookup"><span data-stu-id="eec43-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="eec43-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="eec43-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="eec43-105">Dynamics 365 Project Operations podržava mogućnost kopiranja projekta i vraćanja bilo kojih zadataka generičkim resursima koji predstavljaju ulogu.</span><span class="sxs-lookup"><span data-stu-id="eec43-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="eec43-106">Klijenti mogu da koriste ovu funkcionalnost za izradu osnovnih predložaka projekata.</span><span class="sxs-lookup"><span data-stu-id="eec43-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="eec43-107">Kada odaberete **Kopiraj projekat**, status ciljnog projekta se ažurira.</span><span class="sxs-lookup"><span data-stu-id="eec43-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="eec43-108">Koristite **Razlog statusa** da bi se utvrdilo kada je akcija kopiranja završena.</span><span class="sxs-lookup"><span data-stu-id="eec43-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="eec43-109">Izbor **Kopiraj projekat** takođe ažurira datum početka projekta na trenutni datum početka ako nije otkriven ciljni datum u ciljnom entitetu projekta.</span><span class="sxs-lookup"><span data-stu-id="eec43-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="eec43-110">Prilagođena radnja kopiranja projekta</span><span class="sxs-lookup"><span data-stu-id="eec43-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="eec43-111">Imenuj</span><span class="sxs-lookup"><span data-stu-id="eec43-111">Name</span></span> 

<span data-ttu-id="eec43-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="eec43-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="eec43-113">Ulazni parametri</span><span class="sxs-lookup"><span data-stu-id="eec43-113">Input parameters</span></span>
<span data-ttu-id="eec43-114">Postoje tri ulazna parametra:</span><span class="sxs-lookup"><span data-stu-id="eec43-114">There are three input parameters:</span></span>

| <span data-ttu-id="eec43-115">Parametar</span><span class="sxs-lookup"><span data-stu-id="eec43-115">Parameter</span></span>          | <span data-ttu-id="eec43-116">Tip</span><span class="sxs-lookup"><span data-stu-id="eec43-116">Type</span></span>   | <span data-ttu-id="eec43-117">Vrednosti</span><span class="sxs-lookup"><span data-stu-id="eec43-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="eec43-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="eec43-118">ProjectCopyOption</span></span>  | <span data-ttu-id="eec43-119">String</span><span class="sxs-lookup"><span data-stu-id="eec43-119">String</span></span> | <span data-ttu-id="eec43-120">**{"removeNamedResources":true}** ili **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="eec43-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="eec43-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="eec43-121">SourceProject</span></span>      | <span data-ttu-id="eec43-122">Referentni entitet</span><span class="sxs-lookup"><span data-stu-id="eec43-122">Entity Reference</span></span> | <span data-ttu-id="eec43-123">Izvorni projekat</span><span class="sxs-lookup"><span data-stu-id="eec43-123">Source Project</span></span> |
| <span data-ttu-id="eec43-124">Cilj</span><span class="sxs-lookup"><span data-stu-id="eec43-124">Target</span></span>             | <span data-ttu-id="eec43-125">Referentni entitet</span><span class="sxs-lookup"><span data-stu-id="eec43-125">Entity Reference</span></span> | <span data-ttu-id="eec43-126">Ciljni projekat</span><span class="sxs-lookup"><span data-stu-id="eec43-126">Target Project</span></span> |


- <span data-ttu-id="eec43-127">**{"clearTeamsAndAssignments":true}**: Podrazumevano ponašanje za Project za veb i ukloniće sve zadatke i članove tima.</span><span class="sxs-lookup"><span data-stu-id="eec43-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="eec43-128">**{"removeNamedResources":true}** Podrazumevano ponašanje za Project Operations i vratiće zadatke na generičke resurse.</span><span class="sxs-lookup"><span data-stu-id="eec43-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="eec43-129">Za više podrazumevanih vrednosti radnji pogledajte [Koristite veb API radnje](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="eec43-129">For more defaults on actions, see [Use Web API actions](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="eec43-130">Navedite polja za kopiranje</span><span class="sxs-lookup"><span data-stu-id="eec43-130">Specify fields to copy</span></span> 
<span data-ttu-id="eec43-131">Kada je akcija pozvana, **Kopiraj projekat** pogledaće prikaz projekta **Kopirajte kolone projekta** da bi se utvrdilo koja polja treba kopirati kada se projekat kopira.</span><span class="sxs-lookup"><span data-stu-id="eec43-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="eec43-132">Primer</span><span class="sxs-lookup"><span data-stu-id="eec43-132">Example</span></span>
<span data-ttu-id="eec43-133">Sledeći primer pokazuje kako da pozovete prilagođenu radnju **CopyProject** pomoću skupa parametara **removeNamedResources**.</span><span class="sxs-lookup"><span data-stu-id="eec43-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
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