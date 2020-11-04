---
title: Podešavanje smernica troškova
description: Možete da podesite smernice troškova koje vaši radnici moraju slediti prilikom unošenja i podnošenja izveštaja o troškovima i putnih zahteva u usluzi Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f74f6906cc1137b9645a830360a546432dc5207f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083727"
---
# <a name="set-up-expense-policies"></a>Podešavanje smernica troškova

[!include [banner](../includes/banner.md)]

Možete da definišete smernice koje vaši radnici moraju slediti prilikom unošenja i podnošenja izveštaja o troškovima i putnih zahteva.         
Sprovođenje smernica troškova može vam pomoći da efikasno upravljate troškovima.         

Na primer, možete da postavite smernicu za hotelske troškove u NJujorku, koja navodi da trošak po noćenju ne može premašiti 250 USD.       
Ako radnik podnese izveštaj o trošku ili zahtev za putovanje kada cena sobe prelazi ovaj iznos, sistem će o tome obavestiti        
radnika da je prekoračen iznos smernice za trošak. Možete da konfigurišete poruku koju će radnik dobiti kada        
definišete smernicu.      
        
Možete da definišete tri tipa smernica:         
        
- Upozorenje – Omogućava radniku da podnese izveštaj o trošku ili zahtev za putovanje, ali će trošak biti označen za sve davaoce odobrenja i        
  za kasnije izveštavanje.        

- Greška – Zahteva od radnika da revidira troškove kako bi se pridržavao smernica pre podnošenja izveštaja o troškovima ili zahteva za putovanje.       
 
 - Opravdanje – Zahteva od radnika ili menadžera da unese obrazloženje za prekoračenje iznosa polise pre podnošenja izveštaja o troškovima ili zahteva za putovanje.        

## <a name="policy-tips"></a>Saveti za smernice
Evo nekoliko predloga koji vam mogu pomoći pri kreiranju novih smernica za upravljanje troškovima. 
* Smernice važe na datum i neće stupiti na snagu ako su kreirane sa datumom posle datuma nastanka troškova. Na primer, ako danas kreirate nove smernice za primenu maksimalnog troška obroka od 50 USD, svi postojeći troškovi uneti od juče neće biti provereni u skladu sa ovim smernicama.
* Prilikom kreiranja smernica za kategoriju troškova koja se može podeliti, razmislite o dodavanju uslova za vrstu linije troškova. Neke smernice, poput zahteva za priznanicu, možda neće imati smisla za razvrstane stavke i treba ih primeniti samo na zaglavlje ili nerazvrstane stavke. 
* Smernice za upravljanje troškovima podrazumevano se vrednuju prema izvornom entitetu. U slučaju interkompanijskih scenarija, možete da podesite da se smernice vrednuju prema odredišnom entitetu (entitetu zaduživanja). Da biste pokrenuli smernice prema odredišnom entitetu, uključite funkciju „Procenite smernice troškova u odnosu na zaduživanja pravnog lica“ u radnom prostoru **Upravljanje funkcijama**.

## <a name="when-to-evaluate-policies"></a>Kada se procenjuju smernice

U parametrima upravljanja troškovima postoji opcija da procenite politike upravljanja troškovima kada se linija sačuva ili kada se podnese izveštaj o troškovima. Ako odlučite da procenite kada je linija sačuvana, korisnici će imati raniji uvid u ono što treba da urade da bi odjednom kompletirali svoj izveštaj o troškovima. U suprotnom, možete odložiti procenu smernica i uštedeti vreme ako se potvrđivanje obavlja na kraju, tokom predaje u radni tok.
