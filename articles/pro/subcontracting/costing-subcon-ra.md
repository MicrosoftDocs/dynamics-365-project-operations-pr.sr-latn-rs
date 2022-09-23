---
title: Procena troškova dodeljivanja resursa podizvođačima
description: Ovaj članak sadrži objašnjenja o tome kako Microsoft Dynamics 365 Project Operations izračunava procenu troškova dodeljivanja resursa podizvođačima.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9fded1baa63d2defc134994c858dfc6c09f75082
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522673"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Procena troškova dodeljivanja resursa podizvođačima

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Dodeljivanje zadataka članovima projekta podizvođačima košta korišćenjem **cenovnik** nabavke priložen podizvođačem u povezanom zapisu člana tima. Ovo se razlikuje od načina na koji se koštaju dodele resursa zaposlenih gde se dodeljuju dodele resursa **zaposlenih** koristeći cenovnik troška koji je priložen jedinici ugovora projekta. 

Za generičke članove projektnog tima koji su podizvođači, dodele se koštaju korišćenjem podešavanja cene zasnovane na ulozi u cenovniku nabavke priloženom podizvođačem. Nabavne cene se takođe mogu posebno podesiti za svaki resurs. Ove cene specifične za resurse biće prioritet prilikom dodeljivanja zadataka imenovanih članova projektnog tima radnika po ugovoru. 

Prioritet korišćenja nabavne cene specifične za ulogu u odnosu na resurse podstaknut je podešavanjem prioriteta dimenzije **cena u dimenzijama "Parametri> dimenzijama cena zasnovanih na iznosu**.

Ova funkcionalnost dinamički izvedenih cena zasnovanih na podešavanju dimenzija za nabavne cene podizvođača je slična načinu na koji se troškovi i cene računa derogirano za zaposlene sa punim radnim vremenom. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Kreiranje zadataka za dobijanje procene troškova resursa podizvođača

Dodeljivanje zadataka podizvođačima može se kreirati na dva načina: 
- Korišćenje kartice **"Zadaci** ".
- Korišćenje kartice **"Tim** ".

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Kreiranje dodeljivanja resursa pomoću kartice "Zadaci"
Pomoću liste **resursa** na kartici **"** Zadaci" za određeni zadatak možete da kreirate dodelu zadataka za imenovani resurs ili generički resurs. Ako izaberete imenovani resurs iz **padajuće lista Dodeljeni** resursi zadatka, a ovaj resurs je radnik po ugovoru, imenovani resurs se dodeljuje zadatku, a odgovarajući zapis člana projektnog tima se kreira sa vrstom radnika podešenom na "Radnik po **ugovoru"** **i "Validnost"** postavljena na " **Nevažeće"**. Kao sledeći korak, moraćete da otvorite zapis člana projektnog tima i izaberete red podizvođač i podizvođač. Ovo će ažurirati dodelu zadatka tako da ima referencu na red podizvođači i podizvođači, a takođe će ažurirati status člana tima u **Važeće**.

Ako odaberete da kreirate generičkog člana tima **iz padajuće baze dodeljenih** resursa zadatka, **dijalog kreiranja člana generičkog** tima će vam omogućiti da izaberete red podizvođaca i podizvođaca. Kada se generički resurs dodeli zadatku i kreira odgovarajući zapis člana projektnog tima, primetićete da se zapis člana projektnog tima kreira sa vrstom radnika podešenom na " **Radnik po ugovoru"** **i "Validnost" postavljenu** na "Važeće **"**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Kreiranje članova projektnog tima pomoću kartice "Tim"
Pomoću kartice "Tim" na projektu možete da kreirate generički ili imenovani član tima. Prilikom kreiranja člana tima možete izabrati red podizvođače i podizvođače. Nakon kreiranja člana tima, moraćete da dodelite člana tima zadatku koristeći **padajuću** listu Dodeljeni resursi zadatka. 

## <a name="updating-estimates"></a>Ažuriranje procena
Nakon što dodelite članove projektnog tima zadacima, moraćete da **se krećete do kartice "Procene** " na projektu i **izaberete stavku Ažuriraj cene** da biste se uverili da se stope troškova dodeljivača resursa podizvođača ažuriraju na osnovu nabavnog cenovnog spiska priloženog podizvođaču. Procene se ne generišu za nedodeljene zadatke u korporaciji Microsoft Dynamics 365 Project Operations. Kao rezultat toga, moraćete da kreirate dodele zadataka po ceni i da koštate razne zadatke na projektu. 

> [NAPOMENA!] Članovi projektnog tima koji **imaju tip radnika** **kao radnika** po ugovoru, ali nemaju referencu podizvođaca, označeni su **zastavicom kao nevažeći** u **koordinatnoj mreži članova projektnog** tima. Ako postoje članovi projektnog tima sa ovim statusom, otvorite zapis člana projektnog tima i ručno ažurirajte polja reda podizvođača i podizvođača tako da procena finansijskih troškova tačno odražava trošak podizvođača na **kartici "Procene** ". 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
