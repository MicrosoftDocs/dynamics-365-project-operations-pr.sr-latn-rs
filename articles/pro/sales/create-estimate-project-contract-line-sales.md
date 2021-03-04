---
title: Procena stavke ponude zasnovane na projektu – jednostavno
description: Ova tema pruža informacije o procenama predmeta ugovora zasnovanog na projektu.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2d0d8309fcb4300e33ed2f5933259f99ad7e0d6a
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180434"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a>Procena stavke ponude zasnovane na projektu – jednostavno

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

U usluzi Dynamics 365 Project Operations, predmet ugovora zasnovan na projektu sadrži detalje koji pomažu u proceni troškova i potencijalnog prihoda od posla koji se odnosi na isporuku predmeta ugovora.

Da biste procenili predmet ugovora zasnovan na projektu, idite na karticu **Detalji predmeta ugovora** za **Predmet ugovora** zasnovan na projektu.  Postoje dva načina da kreirate procenu direktno na predmetu ugovora zasnovanom na projektu:

   - Kreirajte procenu direktno u predmetu ugovora ručnim dodavanjem detalja predmeta ugovora.
   - Kreirajte projekat i plan projekta, a zatim povežite projekat i zadatke sa predmetom ugovora o projektu. Ovo omogućava proces pomoću kojeg možete da uvezete procenu plana projekta u predmet ugovora na osnovu komponenti uključenih u predmet ugovora.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Kreiranje procene direktno na predmetu ugovora zasnovanom na projektu

1. Idite na predmet ugovora i izaberite karticu **Detalji predmeta ugovora**. Redovi koje kreirate na ovoj kartici sažeti su i prikazani kao **Ugovorena vrednost** za ovaj **Predmet ugovora**. 
2. U podformi **Detalji predmeta ugovora**, izaberite **+ Novi detalj predmeta ugovora**. Otvara se klizač za brzo kreiranje. Sledeća polja su dostupna na obrascu **Detalji predmeta ugovora**:

| Polje | Lokacija | Opis | Posledični uticaj |
| --- | --- | --- | --- |
| **Opis** | **Brzo kreiranje** | Opis konkretne procene. | Ovo polje podrazumeva detalje povezanog predmeta ugovora za troškove koji se automatski kreiraju. |
| **Klasa transakcije** | **Brzo kreiranje** | Ovaj padajući meni je lista klasa transakcija uključenih na kartici **Opšti podaci** predmeta ugovora zasnovanog na projektu. | Ovo polje podrazumeva detalje povezanog predmeta ugovora za troškove koji se automatski kreiraju. |
| **Uloga** | **Brzo kreiranje** | Uloga osobe koja obavlja ovaj posao ili snosi ovaj trošak. | Ovo polje podrazumeva detalje povezanog predmeta ugovora za troškove koji se automatski kreiraju. |
| **Kategorija** | **Brzo kreiranje** | Kategorija posla ili troška. | Ovo polje podrazumeva detalje povezanog predmeta ugovora za troškove koji se automatski kreiraju. |
| **Datum početka** | **Brzo kreiranje** | Datum početka posla. | Ovo polje podrazumeva detalje povezanog predmeta ugovora za troškove koji se automatski kreiraju. |
| **Datum završetka** | **Brzo kreiranje** | Datum završetka posla. | Ovo polje podrazumeva detalje povezanog predmeta ugovora za trošak koji se automatski kreira. |
| **Jedinica za određivanje resursa** | **Brzo kreiranje** | Jedinica za resurse koja snosi ovaj trošak i omogućava resursu da radi na tome. | Ovo polje podrazumeva detalje povezanog predmeta ugovora za troškove koji se automatski kreiraju. Ovo polje se takođe koristi za pronalaženje cene koštanja. |
| **Raspored jedinica** | **Brzo kreiranje** | Grupa jedinica posla ili troška. Jedinice pripadaju rasporedu jedinica ili grupi jedinica. Na primer, *milje* i *kilometri (km)* su jedinice koje pripadaju grupi jedinica koje opisuju udaljenost. | Ovo polje podrazumeva detalje povezanog predmeta ugovora za troškove koji se automatski kreiraju. |
| **Jedinica** | **Brzo kreiranje** | Jedinica posla ili troška. | Ovo polje podrazumeva detalje povezanog predmeta ugovora za troškove koji se automatski kreiraju. |
| **Količina** | **Brzo kreiranje** | Količina posla ili troška. | Ovo polje podrazumeva detalje povezanog predmeta ugovora za troškove koji se automatski kreiraju. |
| **Cena po jedinici** | **Brzo kreiranje** | Stopa naplate uloge koja obavlja posao ili prodajna cena kategorije troška. Ovo polje podrazumeva **Vreme** na osnovu kombinacije uloge i jedinice resursa na cenovniku projekta koji važi na datum početka. Za troškove, ovo polje je podrazumevano iz podešavanja cene za kategoriju transakcija u cenovniku projekta koja važi za datum početka. Ako način određivanja cene za kategoriju transakcija nije **cena po jedinici**, nema podrazumevanih vrednosti i ovo polje ostaje prazno. | Stopa troškova uloge koja obavlja posao ili cena po jedinici kategorije troška. Ovo polje je podrazumevano za **Vreme zasnovano na ulozi** i kombinacija jedinice resursa na stavki cene uloga cenovnika troškova koja je priložena ugovornoj jedinici sa važenjem za datum početka. Za troškove, ovo polje se podrazumevano zasniva na stavki cene kategorije iz cenovnika troškova pridruženog jedinici ugovaranja koja važi na datum početka. Ako način određivanja cene za kategoriju transakcija nije cena po jedinici, nema podrazumevanih vrednosti i ovo polje ostaje prazno. |
| **Procenjeni porez** | **Brzo kreiranje** | Procenjeni porez za ovaj posao ili trošak kao unos od strane korisnika. | Procenjeni porez za ovaj posao ili trošak kao unos od strane korisnika. |
| **Iznos** | **Brzo kreiranje** | Korisnik može da doda ovu vrednost u ovo polje ako su polja **Količina** i **Cena** ostala prazna. Ako su polja **Količina** i **Cena** popunjena, polje **Iznos** je samo za čitanje i izračunava se kao **(Količina \* Jedinična cena) + Porez**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Ažuriranje cena na detaljima predmeta ugovora

Ako promenite cene na cenovniku projekta koji je priložen uz ugovor ili cenovnik troškova ugovorne jedinice, možete da osvežite cene u detaljima pojedinih predmeta ugovora kako bi odražavale promenu. Na stranici **Ugovor**, izaberite **Preračunaj**. Otvara se upozorenje koje vas obaveštava da su cene svih predmeta ugovora na ovom ugovoru resetovane. Izaberite **Da** da biste osvežili cene detalja predmeta ugovora za prodaju i troškove.

## <a name="access-contract-line-details-for-cost"></a>Pristup detaljima predmeta ugovora radi troškova

Na kartici **Detalji predmeta ugovora** izaberite red u mreži da biste prikazali radnje na traci s alatkama podforme. Prva radnja na traci sa alatkama podforme je **Otvori detalje o troškovima**. Da biste videli odgovarajuću stopu troškova i iznos za ovaj detalj predmeta ugovora, izaberite **Otvori detalje troškova**. 

> [!NOTE]
> Promena kompanije za resurse, jedinice za resurse, količine, datuma, uloge ili vrednosti kategorije na detaljima ugovorne linije za **Trošak** takođe menja odgovarajuće vrednosti na detaljima ugovorne linije za **Prodaju**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Valuta na detaljima predmeta ugovora za troškove i prodaju

Detalj predmeta ugovora za **Prodaju** postavlja podrazumevanu valutu iz cenovnika projekta koja važi za datum početka detalja o predmetu ugovora.

Detalj predmeta ugovora za **Trošak** postavlja podrazumevanu valutu iz cenovnika ugovorne jedinice ugovora koja važi za datum početka detalja o predmetu ugovora za **trošak**.

Proračuni isplativosti konvertuju iznose za detalje o predmetu ugovora za **Trošak** i **Prodaju** u osnovnu valutu okruženja za izveštavanje o ukupnim stvarnim i procenjenim maržama na ugovoru.

> [!NOTE]
> Greške u zaokruživanju valuta i promenjene marže mogu se desiti zbog nedostatka efektivnih deviznih kurseva za datum. Koristite ove proračune na projektnim ugovorima samo kao približne vrednosti, a ne za stvarno zakonsko ili drugo izveštavanje koje zahteva veću preciznost zaokruživanja i svest o efektivnosti datuma za devizne kurseve.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]