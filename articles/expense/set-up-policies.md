---
title: Definisanje smernica troškova
description: Možete da definišete smernice troškova koje vaši radnici moraju slediti prilikom unošenja i podnošenja izveštaja o troškovima i putnih zahteva.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 30b3a0e1547ca7043b1433da2b4ebf02f2b473a1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083650"
---
# <a name="define-expense-policies"></a>Definisanje smernica troškova

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Možete da definišete smernice koje vaši radnici moraju slediti prilikom unošenja i podnošenja izveštaja o troškovima i putnih zahteva.         
Sprovođenje smernica troškova može vam pomoći da efikasno upravljate troškovima.         

Na primer, možete da postavite smernicu za hotelske troškove u NJujorku, koja navodi da trošak po noćenju ne može premašiti 250 USD.       
Ako radnik podnese izveštaj o trošku ili zahtev za putovanje kada cena sobe prelazi ovaj iznos, sistem će obavestiti         
radnika da je prekoračen iznos smernice za trošak. Možete da konfigurišete poruku koju će radnik dobiti kada        
definišete smernicu.      
        
Možete da definišete tri tipa smernica:         
        
- **Upozorenje** : Omogućava radniku da podnese izveštaj o trošku ili zahtev za putovanje, ali će trošak biti označen za sve davaoce odobrenja i         
  za kasnije izveštavanje.        

- **Greška** : Zahteva od radnika da revidira troškove kako bi se pridržavao smernica pre podnošenja izveštaja o troškovima ili zahteva za putovanje.        
 
 - **Opravdanje** : Zahteva od radnika ili menadžera da unese obrazloženje za prekoračenje iznosa polise pre podnošenja izveštaja o troškovima ili zahteva za putovanje.        

## <a name="policy-tips"></a>Saveti za smernice
Evo nekoliko predloga koji vam mogu pomoći pri kreiranju novih smernica za upravljanje troškovima: 

- Smernice važe na datum, što znači da smernice neće stupiti na snagu ako su kreirane sa datumom posle datuma nastanka troškova. Na primer, danas kreirate novu politiku za primenu maksimalnih troškova obroka od 50 USD. Svi postojeći troškovi koji su uneti od juče neće biti provereni u skladu sa ovom politikom.
- Prilikom kreiranja smernica za kategoriju troškova koja se može podeliti, razmislite o dodavanju uslova za vrstu linije troškova. Neke smernice, poput zahteva za priznanicom, možda neće imati smisla za detaljne linije. U ovoj situaciji, smernice se primenjuju samo na liniju zaglavlja ili liniju koja nije stavljena u stavke. 
- Smernice za upravljanje troškovima podrazumevano se vrednuju prema izvornom entitetu. U slučaju interkompanijskih scenarija, možete da podesite da se smernice vrednuju prema odredišnom entitetu (entitetu zaduživanja). Da biste pokrenuli smernice prema odredišnom entitetu, uključite funkciju **Procenite smernice troškova u odnosu na zaduživanja pravnog lica** u radnom prostoru **Upravljanje funkcijama**.

## <a name="when-to-evaluate-policies"></a>Kada se procenjuju smernice

U parametrima upravljanja troškovima možete izabrati da procenite politike upravljanja troškovima kada se linija sačuva ili kada se podnese izveštaj o troškovima. Ako odlučite da procenite kada je linija sačuvana, korisnici će imati raniji uvid u ono što treba da urade da bi odjednom kompletirali svoj izveštaj o troškovima. U suprotnom, možete odložiti procenu smernica i uštedeti vreme potvrđivanjem na kraju, tokom predaje u radni tok.
