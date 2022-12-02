---
title: Procena troškova dodeljivanja resursa podizvođačima
description: Ovaj članak sadrži objašnjenja o tome kako Microsoft Dynamics 365 Project Operations izračunava procenu troškova dodele podugovorenih resursa.
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

Dodele zadataka članovima tima podugovorenog projekta se obračunavaju korišćenjem cenovnika **Nabavka** priloženog podugovoru u povezanom zapisu člana tima. Ovo se razlikuje od načina na koji se obračunava cena dodele resursa zaposlenih gde se za dodele zadataka resursa zaposlenih cena određuje koristeći cenovnik **Cena** koji je priložen ugovornoj jedinici projekta. 

Za generičke članove tima projekta koji su podugovoreni, cena za dodele se obračunavaju korišćenjem podešavanja cene zasnovane na ulogama u cenovniku nabavke priloženog podugovoru u povezanom zapisu člana tima. Nabavne cene se takođe mogu posebno podesiti za svaki resurs. Ove cene specifične za resurse biće prioritetne prilikom dodele zadataka određivanja ocena imenovanih članova projektnog tima koji su radnici po ugovoru. 

Prioritet korišćenja cene nabavke specifične za ulogu u odnosu na specifične za resurse podstaknut je podešavanjem prioriteta dimenzije određivanja cena u **Parametri > dimenzije cena zasnovanih na određivanju cena**.

Ova funkcionalnost dinamički izvedenih cena zasnovanih na podešavanju dimenzija za nabavne cene podugovarača je slična načinu na koji se cena i stope naplate izvode za zaposlene sa punim radnim vremenom. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Kreiranje dodela zadataka za dobijanje procena cena resursa podugovarača

Dodele zadataka podugovaračima može se kreirati na dva načina: 
- Korišćenjem kartice **Zadaci**.
- Korišćenjem kartice **Tim**.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Kreiranje dodela resursa pomoću kartice Zadaci
Pomoću liste **Resursi** na kartici **Zadaci** za određeni zadatak možete da kreirate dodelu zadataka za imenovani resurs ili generički resurs. Ako izaberete imenovani resurs iz padajuće liste **Dodeljeni resursi** na zadatku, a ovaj resurs je radnik po ugovoru, imenovani resurs se dodeljuje zadatku, a odgovarajući zapis člana projektnog tima se kreira sa vrstom radnika podešenom na **Radnik po ugovoru** a **Važenje** se postavlja na **Nevažeće**. Kao sledeći korak, moraćete da otvorite zapis člana projektnog tima i izaberete podugovor ili predmet podugovora. Ovo će ažurirati dodelu zadatka tako da ima referencu na podugovor ili predmet podugovora a takođe će ažurirati status člana tima u **Važeće**.

Ako odaberete da kreirate generičkog člana tima sa padajuće liste **Dodeljeni resursi** na zadatku, dijalog **Kreiranje generičkog člana tima** će vam omogućiti da izaberete podugovor i predmet podugovora. Kada se generički resurs dodeli zadatku i kreira odgovarajući zapis člana projektnog tima, primetićete da se zapis člana projektnog tima kreira sa vrstom radnika podešenom na **Radnik po ugovoru**, a **Važenje** se postavlja na **Važeće**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Kreiranje članova projektnog tima pomoću kartice Tim
Pomoću kartice Tim na projektu možete da kreirate generičkog ili imenovanog člana tima. Prilikom kreiranja člana tima možete izabrati podugovor ili predmet podugovora. Nakon kreiranja člana tima, moraćete da dodelite člana tima zadatku koristeći padajuću listu **Dodeljeni resursi** na zadatku. 

## <a name="updating-estimates"></a>Ažuriranje procena
Nakon što dodelite članove projektnog tima zadacima, moraćete da se krećete do kartice **Procene** na projektu i izaberete **Ažuriraj cene** da biste se uverili da se stope cena dodela resursa podugovora ažuriraju na osnovu cenovnika nabavke priloženog podugovoru. Procene se ne generišu za nedodeljene zadatke u rešenju Microsoft Dynamics 365 Project Operations. Kao rezultat toga, moraćete da kreirate dodele zadataka za cenu i da odredite cenu za razne zadatke na projektu. 

> [NAPOMENA!] Članovi projektnog tima koji imaju **Tip radnika** kao **Radnik po ugovoru**, ali nemaju referencu podugovora, označeni su zastavicom kao **Nevažeći** u matrici koordinatne mreže **Članovi projektnog tima**. Ako postoje neki članovi projektnog tima sa ovim statusom, otvorite zapis člana projektnog tima i ručno ažurirajte polja podugovora i predmeta podugovora tako da procena finansijskih troškova tačno odražava trošak podugovarača na kartici **Procene**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
