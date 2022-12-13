---
title: Koncepti jedinstveni za ponude zasnovane na projektu
description: Ovaj članak pruža informacije o ponudama projekata u korporaciji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824345"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Koncepti jedinstveni za ponude zasnovane na projektu

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Pre nego što počnete da koristite ponude za projekat u korporaciji Microsoft Dynamics 365 Project Operations, trebalo bi da budete svesni sledećih ključnih koncepata.

## <a name="owning-company"></a>Preduzeće-vlasnik

Kompanija u vlasništvu predstavlja pravno lice koje je vlasnik isporuke projekta. Kupac u ponudi bi trebalo da bude važeći kupac u tom pravnom licu u aplikacijama za finansije i operacije. Valuta preduzeća u vlasništvu i valuta ugovorne jedinice koja je izabrana u ponudi zasnovanoj na projektu moraju da se podudaraju.

## <a name="contracting-unit"></a>Jedinica ugovaranja

Ugovorna jedinica predstavlja odeljenje ili praksu u čijem je vlasništvu isporuka projekta. Možete podesiti troškove resursa za svaku jedinicu ugovaranja. Kada navedete troškove resursa za resurs u jedinici za ugovaranje, možete podesiti različite stope troškova za resurse od kojih se jedinica ugovaranja pozajmljuje ili za druge divizije ili prakse u preduzeću. Ove cene troškova se nazivaju transferne cene, zaduživanje resursa ili cene razmene. Kada podesite troškove pozajmljivanja resursa iz drugih odeljenja, možete podesiti stope troškova u valuti odeljenja zajmova.

## <a name="cost-currency"></a>Valuta cene

Valuta troška u projektnim operacijama je valuta u kojoj se izveštavaju troškovi. Ova valuta potiče iz valute koja je priložena polju Jedinica **za ugovaranje** u ponudi, ugovoru i projektu. Troškovi u odnosu na projekat mogu se zapisati u bilo kojoj valuti. Međutim, postoji konverzija valute iz valute u koju su zabeleženi troškovi valute projekta.

S obzirom na to da Dataverse kursevi valuta na platformi ne mogu biti datum-efektivni, ukupni iznosi na ekranu za trošak mogu se vremenom promeniti ako ažurirate kurseve valuta. Međutim, troškovi koji su zapisani u bazi podataka ostaju nepromenjeni, jer su iznosi uskladišteni u valuti u kojoj su nastali.

## <a name="sales-currency"></a>Valuta prodaje

Valuta prodaje u operacijama projekta je valuta u kojoj su zapisani i prikazani procenjeni i stvarni iznosi prodaje. To je takođe valuta u kojoj je kupac fakturisan za dogovor. Za ponudu projekta, podrazumevana valuta prodaje se postavlja iz zapisa kupca ili konta i može se promeniti prilikom kreiranja ponude. Međutim, valuta prodaje ne može da se promeni nakon što se ponuda sačuva. Podrazumevani cenovnici proizvoda i projekta se postavljaju na osnovu valute prodaje ponude.

Za razliku od troškova, vrednosti prodaje se mogu zapisati **samo** u prodajnoj valuti.

## <a name="billing-method"></a>Način naplate

Projekti obično imaju fiksnu naknadu i modele ugovaranja zasnovane na potrošnji. U projektne operacije, model ugovaranja projekta je predstavljen načinom naplate. Način naplate ima dve vrednosti: vreme i materijal i fiksnu cenu.

- **Vreme i materijal** – Model ugovaranja zasnovan na potrošnji gde svaki trošak koji na nastaja ima podršku odgovarajućeg prihoda. Kako procenite ili napravite više troškova, odgovarajuća procenjena i stvarna prodaja će se takođe povećati. Možete odrediti ograničenja koja se ne smeju premašiti za stavke ponude koje imaju ovaj način obračuna. Na taj način možete da povećate stvarni prihod. Na procenjene prihode ne utiču ograničenja koja se ne prekorašuju.
- **Fiksna**  cena– Model ugovaranja fiksne naknade gde su vrednosti prodaje nezavisne od nastalih troškova. Vrednost prodaje je fiksna i ne menja se kako procenite ili napravite više troškova.

## <a name="project-price-lists"></a>Cenovnici projekta

Cenovnici projekta su cenovnici koji se koriste za unos podrazumevanih cena, a ne cene troškova, za vreme, troškove i druge komponente vezane za projekat. Može biti više cenovnika, a svaka lista može imati svoju efektivnost datuma za svaku ponudu za projekat. Operacije projekta ne podržavaju efekat preklapanja datuma za cenovnike projekta.

## <a name="product-price-lists"></a>Cenovnici proizvoda

Cenovnici proizvoda su cenovnici koji se koriste za unos podrazumevanih cena, a ne cena troškova, za redove zasnovane na proizvodu u ponudi. Postoji samo jedan cenovnik proizvoda po ponudi.

## <a name="transaction-classes"></a>Klase transakcije

Projektne operacije podržavaju četiri vrste klasa transakcija:

- Vreme
- Trošak
- Materijal
- Naknada

Vrednosti troška i prodaje mogu se proceniti i naneti na **vreme**, troškove **i** klase **transakcija** materijala. **Naknada** je klasa transakcije samo za prihode.

## <a name="work-entities-and-billing-entities"></a>Radni entiteti i entiteti obračuna

Projekti i zadaci su entiteti koji predstavljaju rad. Redovi ponude i redovi ugovora su entiteti koji predstavljaju naplatu. Različite radne entitete možete povezati sa opcijama fakturisanja tako što ćete ih povezati sa redovima ponude ili redovima ugovora.

## <a name="multi-customer-deals"></a>Pogodbe sa više klijenata

Do poslova sa više kupaca dolazi kada postoji više kupaca po fakturi. Evo nekih tipičnih primera:

- **Originalna preduzeća proizvođača opreme (OEM) i**  njihovi partneri – Partneri i prodavci prodaju proizvod koji uključuje usluge sa dodatnom vrednošću. Tokom dogovora sa kupcem, OEM obično nudi finansiranje dela projekta.
- **Projekti u javnom**  sektoru– Više odeljenja lokalne samouprave pristaje na finansiranje projekta i fakturiše se prema prethodno dogovorenoj podeli. Na primer, školski okrug i gradska uprava ili odeljenje lokalne uprave dogovore se da finansiraju izgradnju bazena.

## <a name="invoice-schedules"></a>Rasporedi za fakturisanje

Rasporedi faktura su specifični za svaki red ponude i opcionalni su. Rasporedi faktura se kreiraju na osnovu određenih datuma početka i završetka i učestalosti fakture. Koriste se tokom faze ugovora, kada je konfigurisan proces automatskog kreiranja fakture. Tokom faze ponude, rasporedi faktura su opcionalni. Ako su kreirane tokom faze ponude, kopiraju se u ugovor o projektu koji je kreiran prilikom izbora ponude za projekat.

## <a name="differences-from-dynamics-365-sales-quotes"></a>Razlike u odnosu na Dynamics 365 ponude za prodaju

Ponude za operacije projekta su izgrađene na Dynamics 365 ponudama za prodaju. Međutim, postoje neke važne razlike u funkcionalnosti kojih bi trebalo da budete svesni:

- Ponude za operacije projekta imaju dve različite vrste redova: jednu za projekte i drugu za proizvode.
- Ponude za operacije projekta imaju svoje elemente stranice i korisničkog interfejsa (korisnički interfejs), poslovna pravila, poslovnu logiku u dodatnim komponentama i skripte na strani klijenta koje ih čine različitim od ponuda za prodaju.
- U prozoru "Prodaja" možete priložiti više porudžbina jednoj ponudi za prodaju. U projektne operacije možete priložiti samo jedan ugovor o projektu ponudi za projekat.
- Kada osvojite ponudu za prodaju, povezana prilika može ostati otvorena. Kada vam odobre ponudu za projekat, biće zatvorena povezana mogućnost za poslovanje.
- Ponuda za prodaju ne uključuje neka polja i koncepte koje uključuje ponuda za projekat. U polja spadaju **Ugovorna jedinica**, **Menadžer za poslovne kontakte** i **Ime kontakta za fakturisanje**.
- Ponude za prodaju i ponude za projekat su identifikovane skup opcija vrsta zasnovana na **projektu** . Za ponudu za prodaju, vrednost ovog polja je zasnovana na **artiklu**. Za ponudu projekta, vrednost je zasnovana **na radu**.

Zbog ovih razlika, ne preporučujemo da međusobno koristite ponude za prodaju i ponude za operacije projekta.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
