---
title: Evidentiranje upotrebe materijala na projektima i projektnim zadacima
description: Ova tema pruža informacije o tome kako da evidentirate upotrebu materijala prema projektima i projektnim zadacima.
author: rumant
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4d8757049953fab0ad8bf6ee1a1d695fcb6df75b1be52641ad4af3b3137d7a0a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999288"
---
# <a name="record-material-usage-on-projects-and-project-tasks"></a>Evidentiranje upotrebe materijala na projektima i projektnim zadacima

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Dok projektni tim radi na zadacima na projektu, troše se ili koriste materijali. Evidencija upotrebe materijala pruža način za evidentiranje ove upotrebe tako da ga menadžer projekta može odobriti i na kraju fakturisati klijentu. 

Da biste evidentirali upotrebu materijala iz kataloga ili za upis i predali ih davaocu odobrenja, sledite ove korake: 

1. U oknu za navigaciju izaberite **Upotreba materijala**, a zatim izaberite **Nova**.
2. Na stranici **Nova upotreba materijala**, unesite potrebne informacije o upotrebi materijala, a zatim izaberite **Sačuvaj**.

Sledeća tabela pruža informacije o poljima na stranici **Evidencija upotrebe materijala**. 

| **Polje** | **Opis** | **Posledični uticaj** |
| --- | --- | --- |
| Opis | Opis specifične upotrebe materijala. | Nema posledičnog uticaja za ovo polje. |
| Datum | Datum kada se očekuje da će se materijal koristiti. | Nema posledičnog uticaja za ovo polje. |
| Project | Spisak aktivnih projekata. | Izbor projekta za evidenciju upotrebe materijala utiče na polje **Zadatak** tako da prikaže samo one zadatke koji su na projektu. |
| Zadatak | Spisak zadataka za projekat, uključujući sažetke i zadatke čvora lista. | Odabir zadatka za evidenciju upotrebe materijala utiče na trenutno stanje cene materijala i trenutno stanje prodaje materijala za zadatak. Ako to polje ostane prazno, cena upotrebe i prodaja odgovarajućeg materijala se prati i rezimira samo na nivou projekta. |
| Izaberite proizvod | Navedite da li je ova upotreba materijala za **Postojeći** (kataloški) proizvod ili za **Ručno dodat** proizvod. | Ovo polje određuje vrstu proizvoda. |
| Proizvod | ID proizvoda iz kataloga proizvoda. Kada izaberete ID proizvoda, vrednost u polju **Izaberite proizvod** se automatski ažurira na **Postojeći proizvod**. ID se koristi za preuzimanje cene i prodajnih cena iz cenovnika. | Nema posledičnog uticaja za ovo polje. |
| Opis ručno dodatog proizvoda | Tekstualno polje za upisivanje naziva proizvoda. Ovo polje je dostupno kada izaberete **Ručno dodat** proizvod u polje **Izaberite proizvod**.| Nema posledičnog uticaja za ovo polje. |
| Resurs koji može da se rezerviše| Resurs koji je koristio ovaj materijal na projektu. Podrazumevana vrednost za ovo polje je resurs prijavljenog korisnika koji može da se rezerviše, ali se može promeniti tako da beleži upotrebu u ime ostalih članova projektnog tima. | Nema posledičnog uticaja za ovo polje. |
| Grupa jedinica | Podrazumevana vrednost u ovom polju dolazi iz grupe jedinica koja je postavljena kao podrazumevana u kataloškom proizvodu. Ovo polje možete ažurirati da biste izabrali drugu grupu jedinica. | Nema posledičnog uticaja za ovo polje. |
| Jedinica | Vrednost u ovom polju je podrazumevana jedinica izabranog proizvoda. Ovo polje možete ažurirati da biste izabrali drugu jedinicu. | Promena jedinice rezultira drugačijom podrazumevanom cenom i troškom jedinice. |
| Količina | Količina proizvoda koja je upotrebljena na projektu ili projektnom zadatku. | Nema posledičnog uticaja za ovo polje. |
| Cena po jedinici | Jedinična cena izabranog proizvoda i kombinacija jedinica kako su postavljene u važećem cenovniku troškova. | Cena jedinice se uvek prikazuje u valuti cene projekta. Ako u cenovniku nema jedinične cene za kombinaciju proizvoda i jedinice, jedinična cena će podrazumevano iznositi 0,00. |
| Ukupna cena | Iznos troškova koji se izračunava kao količina \* jedinični trošak.| Iznos cene se uvek prikazuje u valuti cene projekta. |


## <a name="submit-material-usage-for-review-and-approval"></a>Pošaljite upotrebu materijala na pregled i odobrenje 
Kada zabeležite svu upotrebu materijala i spremni ste da ga odobrite, informacije o upotrebi morate da pošaljete na pregled.

1. Idite na **Evidenciju upotrebe materijala** i izaberite jedan ili više unosa. Ili izaberite sve zapise o upotrebi materijala pomoću polja za potvrdu na zaglavlju.
2. Izaberite **Prosledi**. Sistem obrađuje odabrane stavke, a zatim kreira zahteve za odobrenje upotrebe materijala.

## <a name="recall-a-material-usage-log"></a>Opoziv evidencije upotrebe materijala

Kada je potrebno, možete opozvati prosleđenu upotrebu materijala. Vreme potrebno za opoziv stavke upotrebe materijala zavisi od faze odobrenja.  Ako davalac odobrenja još nije odobrio stavku, opoziv se može izvršiti odmah. Međutim, ako je stavka već odobrena, od davaoca odobrenja se traži da odobri opoziv i poništi transakcije.

1. Idite na **Upotreba materijala**, pa na listi evidencija upotrebe materijala izaberite upotrebu materijala za opoziv.
2. Izaberite **Opozovi**. Ako stavka upotrebe materijala još uvek nije odobrena, sistem je odmah opoziva. Ako je stavka materijala već odobrena, kreira se zahtev za opoziv da bi se obavestio davalac odobrenja da želite da opozovete upotrebu materijala. Davalac odobrenja će zatim potvrditi da se storniranje može izvršiti i stavka će biti vraćena.

## <a name="delete-a-material-usage-log"></a>Brisanje evidencije upotrebe materijala

Možete izbrisati evidenciju upotrebe materijala koja nije poslata. Da biste izbrisali evidenciju upotrebe materijala koja je već poslata, prvo je morate opozvati.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
