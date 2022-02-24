---
title: Predviđanja i budžeti projekata
description: Microsoft Dynamics 365 Finance obezbeđuje predviđanja projekata i budžete projekata radi upravljanja i kontrole vašim projektima.
author: Yowelle
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f99c00effbb0678f1f55e5068a7128cbfb86f5ce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083693"
---
# <a name="project-forecasts-and-budgets"></a>Predviđanja i budžeti projekata

[!include [banner](../includes/banner.md)]

Postoje dva načina da upravljate i kontrolišete svoje projekte: predviđanja projekata i budžeti projekata. 

Koristite predviđanje projekata ako vaša organizacija ima operativnu perspektivu i ako se fokusira na prihode i troškove koji potiču od određenih transakcija. Koristite budžetiranje projekata ako se vaša organizacija više fokusira na finansijske iznose. 

I predviđanja projekata i budžeti projekata koriste modele predviđanja za zadržavanje predviđenih iznosa transakcija. 

Svaka metoda ima svoje prednosti. Trebalo bi da razmotrite sledeće tačke pre nego što izaberete metodu za svoju organizaciju.

|   Način dodele       |           Predviđanje projekata            |        Budžetiranje projekata                           |
|---------------------------|------------------------------------------|----------------------------------------------------|
| **Dodela perioda**     | Ne možete eksplicitno dodeliti transakcije tokom fiskalnog perioda. Umesto toga, predviđanje i kontrola predviđanja zasnivaju se na životnom veku projekta. Budući da se predviđanja zasnivaju na određenom datumu, morate odrediti period od datuma. | Možete dodeliti transakcije tokom čitavog projekta ili fiskalnog perioda. Ako dodeljujete tokom perioda, neiskorišćene iznose možete preneti na sledeći fiskalni period. |
| **Pregled transakcija**  | Možete pregledati transakcije u obrascima za predviđanja, gde vidite predviđanja za celu kompaniju i za sve projekte, bez obzira na hijerarhiju. Da biste se fokusirali na određeni projekat, morate filtrirati podatke.                                       | Možete pregledati budžetirane transakcije za jednu hijerarhiju projekta. Stoga možete pregledati detalje transakcija za nadređeni projekat ili njegove potprojekte.                 |
| **Promenljive transakcije** | Kada unosite predviđene transakcije, možete koristiti svaki postojeći atribut za transakciju stvarnih vrednosti. Ovo omogućava veće detalje u predviđanju. Na primer, možete uneti detalje o količinama, radnicima, stavkama ili svojstvima linija.         | Kada unesete detalje o budžetu, možete da koristite samo iznose, kategorije i aktivnosti.                    |
| **Bezbednost**              | Predviđanje se zasniva na transakcijama koje unesete u obrasce za predviđanje i ne uključuje mehanizam kontrole procesa. Svaki radnik koji ima dozvolu za obrazac za predviđanje može da revidira informacije bez odobrenja.                                        | Budžetiranje koristi sistem tokova posla, koji omogućava upravljanje promenama i omogućava vam da vodite istoriju revizija.         |
| **Tipovi stavki**           | Stavke transakcija predviđanja zasnivaju se na broju jedinica, kao i na troškovima i cenama prodajnih jedinica.  | Detalji budžeta zasnivaju se na iznosima, koji se dele između troškova i prihoda.                                          |
| **Modeli predviđanja**       | Budući da svako predviđanje mora biti povezano sa modelom, možete kreirati više modela predviđanja i takođe postaviti podmodele.           | Projektno budžetiranje ograničava modele predviđanja koji se koriste za budžetiranje. Manje modela prognoziranja može pomoći povećanju doslednosti u projekcijama.                           |
| **Prekoračenja troškova**         | Možete samo dozvoliti ili zabraniti unos transakcija koje će prouzrokovati prekoračenje troškova.   | Budžetiranje projekata pruža dodatne mogućnosti kontrole za korisnike. Možete dozvoliti upozorenja i prekoračenja.                    |
| **Kontrola**               | Kontrola predviđanja se obavlja korišćenjem smanjenja predviđanja. Iznosi stvarnih vrednosti se oduzimaju od predviđenih stanja transakcija bez ikakvog kontrolnog traga. To može otežati praćenje mesta na kojima su obavljene transakcije stvarnih vrednosti.                   | U kontroli budžeta projekta, iznosi stvarnih vrednosti se oduzimaju od iznosa u preostalom budžetu. Ovo omogućava jasniji kontrolni trag.                                   |

## <a name="project-forecasts"></a>Predviđanja projekata
Kada koristite predviđanje projekata, možete unositi predviđene transakcije u obrasce za svaku vrstu transakcije. Svaki atribut koji je dostupan za stvarnu transakciju može se koristiti za predviđenu transakciju – na primer, profitabilnost linije, atributi linija, radnici ili opisi. Takođe možete predvideti koliko dugo nakon nastanka troška ćete fakturisati klijentu. 

Transakcije predviđanja projekata zasnivaju se na jedinicama i iznosima. 

Svako predviđanje projekta morate povezati sa modelom predviđanja. Kada unesete predviđenu transakciju, automatski se predlaže model predviđanja. Model predviđanja deluje kao kontejner za predviđene transakcije. 

Modele predviđanja možete odrediti kao podmodele za model. Ovo vam omogućava predviđanje po regionu, vremenskom periodu ili odeljenju. Možete da kopirate predviđene transakcije u model da biste kreirali novi model, a možete i da prenesete transakcije u glavnu knjigu. Budući da postoji relacija jedan-prema-jedan između predviđanja i modela, svaki model predviđanja čini zasebni budžet za projekat. 

Modeli predviđanja mogu koristiti smanjenje predviđanja kao kontrolni mehanizam za projekte. U smanjenju predviđanja, transakcije stvarnih vrednosti smanjuju predviđeno stanje transakcija. Međutim, s obzirom da se smanjenje predviđanja primenjuje na najviši projekat u hijerarhiji, to pruža ograničen pogled na promene u predviđanju. Na primer, ako je radnik povezan sa potprojektom, stvarne transakcije za radnika se knjiže u nadređeni projekat. To može otežati praćenje promena, jer ne možete lako odrediti koja je transakcija u kojem potprojektu dovela do smanjenja na predviđeni iznos. Stoga je dobra ideja da kreirate kopiju modela predviđanja za smanjenje predviđanja koja će se koristiti. Tada možete da koristite izveštaje da biste videli ono što je prvobitno predviđeno. 

Možete da revidirate, kopirate, izbrišete ili prenesete predviđanja projekata u budžet glavne knjige. Međutim, ne postoji kontrola procesa. Svaki radnik koji ima dozvolu za obrazac za predviđanje može da revidira informacije bez recenzije.

-   **Revidiraj** – Možete revidirati predviđenu transakciju u istim obrascima u kojima su napravljeni originalni unosi.
-   **Kopiraj ili izbriši** – Kada iskopirate predviđene transakcije, kopirate linije transakcija jednog modela predviđanja u drugi model predviđanja. Kada izbrišete predviđanje, brišete predviđene transakcije iz modela predviđanja. Da biste ograničili predviđene transakcije koje se kopiraju ili brišu, izaberite određene vrste transakcija i datume. Ovo vam omogućava kopiranje ili brisanje samo određenih delova predviđanja.
-   **Transfer** – Kada prenosite predviđanje projekta u budžet glavne knjige, prenosite predviđene transakcije modela predviđanja u budžet glavne knjige. Možete da izmenite sve prethodno prenesene transakcije u budžet glavne knjige na koje prenosite predviđanje projekta.

## <a name="project-budgets"></a>Budžeti projekata
Budžetiranje projekata je jednostavniji metod od predviđanja, iako se integriše sa modelima predviđanja. Koristi jedan obrazac za unos originalnih detalja i revizija budžeta i omogućava projekcije koje se zasnivaju samo na iznosu, kategoriji ili aktivnosti. 

U budžetiranju projekata, svi originalni budžeti i revizije moraju se poslati na odobravanje toku posla projekta. Tokovi posla vam daju povećanu kontrolu nad procesom i kreiraju zapis istorije promena. 

Budžetiranje projekata podseća na budžetiranje glavne knjige, ali je brže i jednostavnije za postavljanje. Mnoge opcije u budžetiranju glavne knjige, kao što su sekvence brojeva ili valuta, ne moraju se posebno postavljati za projekte.

Budžeti projekata automatski su povezani sa dva modela predviđanja, jednim za izvorni budžet i jednim za preostali budžet. Stoga izveštaji koji se zasnivaju na modelima predviđanja mogu da koriste podatke o budžetu. Kada se primeni budžet projekta, sistem kreira predviđene transakcije na osnovu povezanih modela, koji se koriste u svrhe izveštavanja i kontrole.

## <a name="forecast-models"></a>Modeli predviđanja
Modeli predviđanja imaju hijerarhiju sa jednim slojem. To znači da jedno predviđanje projekta mora biti povezano sa jednim modelom predviđanja.

Ako koristite predviđanje projekata, možete prepoznati modele kao podmodele. Možete kreirati predviđanja po odeljenju, vremenskom periodu ili regionu. Na primer, možete da napravite model predviđanja za godinu dana, a zatim da kreirate podmodele predviđanja za severoistočni, jugoistočni, severozapadni i jugozapadni region, koje vam podnose regionalni rukovodioci. Odabirom različitih opcija u dostupnim izveštajima, možete da pregledate informacije prema ukupnom predviđanju ili prema podmodelu.



