---
title: Odredite troškove za projekat i procenjene prihode
description: Kako da odredite troškove projekta i procene prihoda u aplikaciji Project Service
author: ruhercul
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 5d1bdde3c376a74952d54a1e7fade1f48e675d2f
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580243"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>Odredite troškove za projekat i procenjene prihode 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Procene projekta finansijski prikaz za rad koji je procenjen i zakazan u strukturnoj analizi posla za projekat. Prikaz procena vas obaveštava o uticaju planiranog posla na troškove i prihod. Prikaz procena obezbeđuje alatku za prikaz informacija za određeni broj unapred definisanih aspekata koji će vas najbolje obavestiti o finansijskom uticaju projekta.  
  
## <a name="cost-and-sales-value-of-the-project"></a>Troškovi i prodajna vrednost projekta  
Cenovnici [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] definišu cene i naplate za uloge koje projekti koriste. Na osnovu uloga povezanih sa zadacima u strukturiranoj analizi posla, možete utvrditi uticaj posla na troškove i prihod.  
  
## <a name="cost-price-defaulting"></a>Određivanje podrazumevane cene koštanja  
Svaki projekat pripada organizaciji (naznačenoj u **Vlasnička jedinica** u projektu). Cenovnik povezan sa vlasničkom organizacionom jedinicom određuje cenu koštanja jedinice. [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] utvrđuje cene koštanja za uloge pretraživanjem kombinacije uloge, jedinice i organizacione jedinice na cenovnik troškova da biste dobili ispravne cene koštanja za datum efektive u stavkama procene.  
  
Ako kombinacija uloge, jedinice i organizacione jedinice ne rezultuje cenom koštanja iz cenovnika vlasničke jedinice, jedinica se zanemaruje u korist kombinacije uloge i organizacione jedinice. Ako postoji cena koštanja, ovaj cena se konvertuje u jedinicu koju odaberete u stavki procene.  
  
Ako kombinacija uloge i organizacione jedinicu ne dovede do cene koštanja, organizaciona jedinica se zanemaruje u korist kombinacije uloge i jedinice i cena postaje podrazumevana nakon primene bilo kakve konverzije, ako je potrebna.  
  
 Ako nema cene za ulogu, cena koštanja će podrazumevano prikazivati 0,00 na stavci procene.  
  
 Svi iznosi troškova na stavkama procene troškova za projekat su u valuti vlasničke organizacione jedinice.  
  
## <a name="sales-price-defaulting"></a>Podrazumevana prodajna cena  
Cenovnik prodaje je zasnovan na entitetu prodaje kome je projekat priložen. Cenovnik prodaje povezan sa ponudom ili ugovorom određuje jedinicu cene za prodaju. Ako ponuda ili ugovor imaju prilagođeni cenovnik, to je podrazumevani cenovnik prodaje za procene projekta. Ako nema povezivanja sa entitetima prodaje, onda će podrazumevani cenovnik prodaje konfigurisan u postavkama parametara biti podrazumevani cenovnik prodaje za projekat. Svaka stavka procene ima povezanu organizacionu jedinicu resursa koja ukazuje na organizacionu jedinicu iz koje će biti rezervisani resursi za dovršavanje zadataka. Prodajna cena za povezane uloge se određuje pretraživanjem kombinacije uloge, jedinice i organizacione jedinice resursa u cenovniku troškova da biste dobili ispravnu prodajnu cenu za datum efektive u stavkama procene.  
  
Ako kombinacija uloge, jedinice i organizacione jedinice resursa ne dovede do prodajne cene iz cenovnika prodaje, sistem će zanemariti jedinicu i potražite kombinaciju uloge i organizacione jedinice resursa. Ako se prodajna cena pronađe, ona se konvertuje u jedinicu koju odaberete u stavki procene za prodaju.  
  
Ako sistem ne pronađe cenu za ulogu, prodajna cena će podrazumevano prikazivati 0,00 na stavci procene.  
  
Prikaz procena ima prikaz mreže koji prikazuje ravnomernu mrežu stavki procene sa jedinicom, ukupnom cenom i prodajnom cenom.  
  
## <a name="time-phased-view-of-project-estimates"></a>Prikaz procena za projekat u vremenu  
U prikazu procena za projekat u vremenu, podaci o procenama iz prikaza koordinatne mreže se podrazumevano okreću po ulozi i prikazuje se širenje podataka o proceni na vremenskoj osi u odabranoj skali vremena.  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>Dodela procene truda na osnovu režima zadatka  
U prikazu u vremenu, ukupan procenjeni trud za zadatak je distribuiran dodeljivanjem određenog broja sati truda časova po jedinici vremena odabrane skale vremena. U funkciji project service, režim zadatka određuje način dodeljivanja truda tokom trajanja zadatka. Dve vrste dodele su ravnomerna dodela i dodela na osnovu radnog vremena. 
  
## <a name="work-hours-based-allocation"></a>Dodela na osnovu radnog vremena  
Režim automatskog zakazivanja zadataka nalaže da se, za broj resursa procenjenih u zadatku, procenjuje da su oni iskorišćeni puno radno vreme po danu. Ovo se primenjuje i kada se dodeljuje trud podelom po trajanju zadataka u prikazu u vremenu. Na primer, na vremenskoj skali „Dan“, za zadatak za koji je procenjeno da će ga dovršiti jedan resurs, trud dodeljen po danu neće premašiti radno vreme po danu definisano u kalendaru projekta. Stoga, dodela truda uvek osigurava da bude procenjeno da se resursi koriste pun dan.  
  
## <a name="even-distribution"></a>Ravnomerna distribucija  
Režim ručnog zakazivanja zadatka ne poštuje radne časove, kalendar projekta niti broj resursa koji su definisani u zadatku. Raspored zadatka je zasnovan na unosu korisnika. Za takve zadatke, dodela truda po jedinici vremenskog perioda odabrane vremenske skale nema ograničavajuće faktore. Ukupan trud u zadatku se jednako deli i dodeljuje za svaku jedinicu vremenskog perioda na odabranoj skali vremena.  
  
Režim zadataka definisan u zadatku na ovaj način određuje distribuciju ili dodelu truda po jedinici vremenskog perioda u procenama u vremenu.  
  
## <a name="grouping-and-time-phasing-options"></a>Opcije grupisanja i prikazivanja u vremenu  
Ovaj prikaz vam pomaže da razumete distribuciju truda, cene i procene prodaje na osnovu dana, sedmice, meseca ili godine. Opcija „Grupiši po“ omogućava usmeravanje podataka procena na dva druga aspekta: kategoriju i resurs. U prikazu mreže i prikazu u vremenu možete izabrati polja koja se prikazuju. Ukupni iznosi za svaki blok vremena se prikazuju na dnu, pokazujući ukupan procenjeni trud, cenu i prodaju za dan, nedelju, mesec ili godinu.  
  
Podrazumevana cena koštanja i prodajna cena stupaju na snagu određenog datuma. Kada se stope za ulogu promene, to će biti transparentnije u prikazu u vremenu prilikom prikaza podataka procene usmerenih na „Resurs“ i prikaza po sedmicama.  
  
## <a name="expense-estimates"></a>Procene troškova  
Svi troškovi koji će nastati u toku projekta koji nisu direktno u vezi sa radom koji će se obavljati se mogu zabeležiti u procenama projekta u prikazu mreže. Pomoću opcije **Dodaj procenu troškova** u prikazu mreže možete to da postignete. Možete zabeležiti procene troškova za određeni zadatak ili za ceo projekat. U ovim redovima možete odabrati kategorije troškova i odabrati okvirni datum kada se očekuje da će troškovi nastati. Ako povezani troškovnik i cenovnik prodaje ima podrazumevane cene ili procente marže definisane u kategorijama troškova, on će biti podrazumevano prikazan u stavci procene po povezivanju.  
  
### <a name="see-also"></a>Takođe pogledajte  
 [Vodič za menadžera projekta](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
