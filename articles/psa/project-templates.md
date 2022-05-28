---
title: Predlošci projekata
description: Ova tema pruža informacije o tome kako koristiti predloške projekta za brzo podešavanje projekta.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: aff6fc5bb855fe1e9007933fdc1a88eb020da0ad
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586039"
---
# <a name="project-templates"></a>Predlošci projekata 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Predložak projekta je unapred definisan okvir koji vam pomaže da brzo i lako pokrenete projekat. Možete da koristite unapred definisani predložak za kreiranje novog projekta jednim klikom. Što se tiče projekata, morate definisati preduslove za predloške projekata. Morate definisati kalendar projekta za svaki predložak projekta, a uloge i cenovnici moraju biti unapred definisani u organizaciji kako bi komponente predloška imale korisne podatke.

Predložak projekta sastoji se od tri komponente: raspored, procene projekta i članovi projektnog tima.

## <a name="schedule"></a>Raspored

Raspored u predlošku projekta ima isti skup elemenata kao i raspored u projektu. Možete da kreirate hijerarhiju zadatka, povezujete uloge sa zadacima, definišete raspored atributa i podešavate zavisne elemente. Raspored u predlošku projekta takođe podržava režime zadataka za svaki zadatak. Stoga podržava i sistem za zakazivanje. Morate povezati kalendar projekta sa projektom. Kada kreirate radni raspored, nema razlike između predloška projekta i projekta.

## <a name="project-estimates"></a>Procene za projekat

Procene projekta u obrascu projekta funkcionišu na isti način kao procene projekta u projektu. Međutim, cene troškova i prodajne cene se preuzimaju iz podrazumevanih cenovnika troškova i prodajnih cenovnika koje su definisani u parametrima.

## <a name="creating-a-project-from-a-template"></a>Kreiranje projekta iz predloška
 
Postoji nekoliko načina za kreiranje projekta iz predloška projekta:

- Kada kreirate projekat iz ponude, možete odabrati predložak projekta u dijalogu za **brzo kreiranje projekta**.

> ![Dijalog za brzo kreiranje projekta.](media/project-11.png)

- Kada kreirate projekat odabirom opcije **Novi projekat**, stranica **Projekat** se pojavljuje pre nego što se zapis sačuva. U polju **Izbor predloška** izaberite jedan od unapred definisanih predložaka projekata u organizaciji.
- Upotrebite **Kreiranje projekta iz predloška** na stranici **Entitet predloška**.

## <a name="copying-components-of-template-to-project"></a>Kopiranje komponenti predloška u projekat

Kada kopirate komponente predloška projekta u projekat, može se dogoditi nekoliko zamena, zavisno od podešavanja u projektu.

### <a name="copying-the-schedule"></a>Kopiranje rasporeda

Kada kopirate raspored iz predloška projekta, ako projekat ima drugačiji kalendar projekta nego predložak, radno vreme iz kalendara projekta se primenjuje na raspored zadataka. Na ovaj način se raspored prilagođava kako bi odgovarao kalendaru koji podržava projekat. Slično, prvi zadatak u rasporedu počinje na datum početka projekta, a ostatak rasporeda hijerarhije se ažurira na osnovu trajanja i zavisnih elemenata navedenih u predlošku. 

### <a name="copying-project-estimates"></a>Kopiranje procena projekta 

Kada kopirate više stavki procene projekata, cenovnici se ažuriraju. U cenovniku troškova, ove ispravke su zasnovane na jedinici koja je vlasnik projekta. U cenovniku prodaje zasnovane su na klijentu. Kada su u pitanju projekti koji su povezani sa entitetom prodaje, troškovi po jedinici i prodajne cene se utvrđuju na osnovu ovih cenovnika.

### <a name="copying-a-project-team"></a>Kopiranje projektnog tima

Kada kopirate projektni tim iz predloška projekta u projekat, kopiraju se generički resursi, zajedno sa veštinama i stručnošću definisanim u predlošku. Dodele generičkih resursa takođe se održavaju kao u predlošku projekta. Imenovani resursi nisu podržani u predlošcima projekata.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
