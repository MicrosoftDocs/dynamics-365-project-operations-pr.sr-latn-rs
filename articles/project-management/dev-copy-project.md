---
title: Razvijte predloške projekata pomoću opcije za kopiranje projekata
description: Ova tema pruža informacije o tome kako kreirati predloške projekata pomoću prilagođene radnje Kopiranje projekta.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb49109e8c199bc4569702ae844a19985534294d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083520"
---
# <a name="develop-project-templates-with-copy-project"></a>Razvijte predloške projekata pomoću opcije za kopiranje projekata

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Dynamics 365 Project Operations podržava mogućnost kopiranja projekta i vraćanja svih zadataka u generičke resurse koji predstavljaju ulogu. Klijenti mogu da koriste ovu funkcionalnost za izradu osnovnih predložaka projekata.

Kada odaberete **Kopiraj projekat** , status ciljnog projekta se ažurira. Koristite **Razlog statusa** da bi se utvrdilo kada je akcija kopiranja završena. Izbor **Kopiraj projekat** takođe ažurira datum početka projekta na trenutni datum početka ako nije otkriven ciljni datum u ciljnom entitetu projekta.

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


- **{"clearTeamsAndAssignments":true}** : Podrazumevano ponašanje za Project za veb i ukloniće sve zadatke i članove tima.
- **{"removeNamedResources":true}** Podrazumevano ponašanje za Project Operations i vratiće zadatke na generičke resurse.

Za više podrazumevanih vrednosti radnji pogledajte [Koristite veb API radnje](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Navedite polja za kopiranje 
Kada je akcija pozvana, **Kopiraj projekat** pogledaće prikaz projekta **Kopirajte kolone projekta** da bi se utvrdilo koja polja treba kopirati kada se projekat kopira.
