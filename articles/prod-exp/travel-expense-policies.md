---
title: Podešavanje smernica troškova
description: Polise troškova koje vaši radnici moraju da prate prilikom ulaska i podnošenja izveštaja o troškovima i putnih zahteva možete podesiti Microsoft Dynamics u 365 Finansija.
author: suvaidya
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3dc5d1768b57baa68f134af318dd9d2d7cdd756
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684751"
---
# <a name="set-up-expense-policies"></a>Podešavanje smernica troškova

Možete da definišete smernice koje vaši radnici moraju slediti prilikom unošenja i podnošenja izveštaja o troškovima i putnih zahteva.         
Sprovođenje smernica troškova može vam pomoći da efikasno upravljate troškovima.         

Na primer, možete da postavite smernicu za hotelske troškove u Njujorku, koja navodi da trošak po noćenju ne može premašiti 250 USD.       
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]