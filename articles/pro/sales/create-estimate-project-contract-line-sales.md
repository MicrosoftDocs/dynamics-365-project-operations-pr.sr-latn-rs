---
title: Procena stavke ponude zasnovane na projektu – jednostavno
description: Ovaj članak pruža informacije o procenama predmeta ugovora zasnovanog na projektu.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8b4379cc5822d08b55623f0f3d4d49791af90927
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914419"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a>Procena stavke ponude zasnovane na projektu – jednostavno

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

U usluzi Dynamics 365 Project Operations, predmet ugovora zasnovan na projektu sadrži detalje koji pomažu u proceni troškova i potencijalnog prihoda od posla koji se odnosi na isporuku predmeta ugovora.

Da biste procenili predmet ugovora zasnovan na projektu, idite na karticu **Detalji predmeta ugovora** za **Predmet ugovora** zasnovan na projektu.  Postoje dva načina da kreirate procenu direktno na predmetu ugovora zasnovanom na projektu:

   - Kreirajte procenu direktno u predmetu ugovora ručnim dodavanjem detalja predmeta ugovora.
   - Kreirajte projekat i plan projekta, a zatim povežite projekat i zadatke sa predmetom ugovora o projektu. Ovo omogućava proces pomoću kojeg možete da uvezete procenu plana projekta u predmet ugovora na osnovu komponenti uključenih u predmet ugovora.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Kreiranje procene direktno na predmetu ugovora zasnovanom na projektu

Da biste kreirali procenu direktno na predmetu ugovora zasnovanom na projektu, sledite ove korake:

1. Idite na predmet ugovora i izaberite karticu **Detalji predmeta ugovora**. Redovi koje kreirate na ovoj kartici sažeti su i prikazani kao **Ugovorena vrednost** za ovaj **Predmet ugovora**. 
2. U podformi **Detalji predmeta ugovora**, izaberite **Novi detalj predmeta ugovora**. Otvara se klizač za brzo kreiranje. Sledeća polja su dostupna na stranici **Detalji predmeta ugovora**.

| Polje | Lokacija | Opis | Posledični uticaj |
| --- | --- | --- | --- |
| **Opis** | **Brzo kreiranje** | Opis konkretne procene. | Ova vrednost podrazumeva detalje povezanog predmeta ugovora za cenu koja se automatski kreira. |
| **Klasa transakcije** | **Brzo kreiranje** | Ovo je lista klasa transakcija uključenih na kartici **Opšti podaci** predmeta ugovora zasnovanog na projektu. | Ova vrednost podrazumeva detalje povezanog predmeta ugovora za cenu koja se automatski kreira. |
| **Izaberite proizvod** | **Brzo kreiranje** | Primenjuje se kada je klasa transakcije **Materijal**. Možete da navedete da li je ova stavka procene za **Postojeći** (kataloški) proizvod ili za **Ručno dodat** proizvod. | Ova vrednost podrazumeva detalje povezanog predmeta ugovora za cenu koja se automatski kreira. |
| **Proizvod** | **Brzo kreiranje** | ID proizvoda iz kataloga proizvoda. Ovo polje je omogućeno samo kada izaberete **Postojeći proizvod** u polju **Izaberite proizvod**. ID se koristi za preuzimanje prodajne cene iz cenovnika projekta u ugovor. | Ova vrednost podrazumeva detalje povezanog predmeta ugovora za cenu koja se automatski kreira. |
| **Ručno dodat proizvod** | **Brzo kreiranje** | Tekstualno polje za upisivanje naziva proizvoda. Ovo polje je omogućeno samo kada izaberete **Ručno dodaj** u polju **Izaberite proizvod**.| Ova vrednost podrazumeva detalje povezanog predmeta ugovora za cenu koja se automatski kreira. |
| **Uloga** | **Brzo kreiranje** | Uloga osobe koja obavlja ovaj posao ili snosi ovaj trošak. | Ova vrednost podrazumeva detalje povezanog predmeta ugovora za cenu koja se automatski kreira.|
| **Kategorija** | **Brzo kreiranje** | Kategorija posla ili troška. |Ova vrednost podrazumeva detalje povezanog predmeta ugovora za cenu koja se automatski kreira.|
| **Datum početka** | **Brzo kreiranje** | Datum početka posla. | Ova vrednost podrazumeva detalje povezanog predmeta ugovora za cenu koja se automatski kreira. |
| **Datum završetka** | **Brzo kreiranje** | Datum završetka posla. | Ova vrednost podrazumeva detalje povezanog predmeta ugovora za cenu koja se automatski kreira. |
| **Jedinica za određivanje resursa** | **Brzo kreiranje** | Jedinica za određivanje resursa koja izaziva ovaj trošak i obezbeđuje resurse za rad na njima. |Ova vrednost podrazumeva detalje povezanog predmeta ugovora za cenu koja se automatski kreira i koristi u preuzimanju cene koštanja. |
| **Raspored jedinica** | **Brzo kreiranje** | Grupa jedinica rada, proizvoda ili troškova. Jedinice pripadaju rasporedu jedinica ili grupi jedinica. Na primer, *milje* i *kilometri (km)* su jedinice koje pripadaju grupi jedinica koje opisuju udaljenost. | Ova vrednost podrazumeva detalje povezanog predmeta ugovora za cenu koja se automatski kreira. |
| **Jedinica** | **Brzo kreiranje** | Jedinica rada, proizvoda ili troškova. | Ova vrednost podrazumeva detalje povezanog predmeta ugovora za cenu koja se automatski kreira. |
| **Količina** | **Brzo kreiranje** | Količina rada, proizvoda ili troškova. | Ova vrednost podrazumeva detalje povezanog predmeta ugovora za cenu koja se automatski kreira. |
| **Cena po jedinici** | **Brzo kreiranje** | Stopa naplate uloge koja obavlja posao, cena po jedinici proizvoda ili prodajna cena proizvoda ili kategorije troškova. Ovo polje je podrazumevano za **vreme** na osnovu kombinacije vrednosti aspekata za određivanje cena u redu cene uloga u cenovniku projekta koja je na snazi za datum početka. Za **troškove**, ovo polje je podrazumevano iz podešavanja cene za kategoriju transakcija u cenovniku projekta koja važi za datum početka. Ako način određivanja cene za kategoriju transakcija nije **cena po jedinici**, nema podrazumevanih vrednosti i ovo polje ostaje prazno. Za proizvode podrazumevana vrednost ovog polja se zasniva na redu **Stavka cenovnika** u cenovniku projekta koji važi na datum početka.| Stopa troškova uloge koja izvodi posao, ili cena po jedinici kategorije troškova ili jedinična cena proizvoda. Ovo polje je podrazumevano za **vreme** na osnovu kombinacije vrednosti aspekata za određivanje cena u redu cene uloga u cenovniku koštanja povezanog sa ugovornom jedinicom koja je na snazi za datum početka. Za troškove, ovo polje se podrazumevano zasniva na stavki cene kategorije iz cenovnika troškova pridruženog jedinici ugovaranja koja važi na datum početka. Ako način određivanja cene za kategoriju transakcija nije cena po jedinici, nema podrazumevanih vrednosti i ovo polje ostaje prazno. Za proizvode, podrazumevana vrednost ovog polja se zasniva na stavci **Stavka cenovnika** cenovnika troškova koja je priložena ugovornoj jedinici i koja važi na datum početka.|
| **Procenjeni porez** | **Brzo kreiranje** | Procenjeni porez za ovaj rad ili trošak. | Procenjeni porez za ovaj rad ili trošak. |
| **Iznos** | **Brzo kreiranje** | U ovo polje možete dodati vrednost ako polja **Količina** i **Cena** ostanu prazna. Ako su polja **Količina** i **Cena** popunjena, polje **Iznos** je samo za čitanje i izračunava se kao **(Količina \* Jedinična cena) + Porez**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Ažuriranje cena na detaljima predmeta ugovora

Ako promenite cene na cenovniku projekta koji je priložen uz ugovor ili cenovnik troškova ugovorne jedinice, možete da osvežite cene u detaljima pojedinih predmeta ugovora kako bi odražavale promenu. Na stranici **Ugovor**, izaberite **Preračunaj**. Pojavljuje se upozorenje koje vas obaveštava da su cene za sve predmete ugovora na ovom ugovoru resetovane. Izaberite **Da** da biste osvežili cene detalja predmeta ugovora za prodaju i troškove.

## <a name="access-contract-line-details-for-cost"></a>Pristup detaljima predmeta ugovora radi troškova

Na kartici **Detalji predmeta ugovora** izaberite red u mreži da biste prikazali radnje na traci s alatkama podforme. Prva radnja na traci sa alatkama podforme je **Otvori detalje o troškovima**. Da biste videli odgovarajuću stopu troškova i iznos za ovaj detalj predmeta ugovora, izaberite **Otvori detalje troškova**. 

> [!NOTE]
> Promena kompanije za resurse, jedinice za resurse, količine, datuma, uloge ili vrednosti kategorije na detaljima ugovorne linije za **Trošak** takođe menja odgovarajuće vrednosti na detaljima ugovorne linije za **Prodaju**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Valuta na detaljima predmeta ugovora za troškove i prodaju

Detalj predmeta ugovora za **Prodaju** postavlja podrazumevanu valutu iz cenovnika projekta koja važi za datum početka detalja o predmetu ugovora.

Detalj predmeta ugovora za **Trošak** postavlja podrazumevanu valutu iz cenovnika ugovorne jedinice ugovora koja važi za datum početka detalja o predmetu ugovora za **trošak**.

Proračuni isplativosti konvertuju iznose za detalje o predmetu ugovora za **Trošak** i **Prodaju** u osnovnu valutu okruženja za izveštavanje o ukupnim stvarnim i procenjenim maržama na ugovoru.

> [!NOTE]
> Greške u zaokruživanju valuta i promenjene marže mogu se desiti zbog nedostatka efektivnih deviznih kurseva za datum. Koristite ove proračune samo na ugovorima za projekat, jer su to približne vrednosti i nisu stvarno zakonsko ili drugo izveštavanje koje zahteva veću preciznost zaokruživanja i svest o efektivnosti datuma za devizne kurseve.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
