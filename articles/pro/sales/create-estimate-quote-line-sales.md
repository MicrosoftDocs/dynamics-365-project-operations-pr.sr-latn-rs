---
title: Procena stavke ponude zasnovane na projektu
description: Ova tema pruža informacije o tome kako da kreirate procenu na stavci ponude zasnovane na projektu.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a8e2b56b4a97ce184fc36145fffe63db8772bdef8bb89f9b60ddaf43db0c1ba4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997308"
---
# <a name="estimating-a-project-based-quote-line"></a>Procena stavke ponude zasnovane na projektu

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Stavka ponude zasnovana na projektu sadrži detalje koji pomažu u proceni troškova i potencijalnog prihoda od posla koji se odnosi na isporuku stavke ponude.

Da biste procenili stavku ponude zasnovanu na projektu, u stavci ponude zasnovane na projektu izaberite karticu **Detalj stavke ponude**. Postoje dva načina za kreiranje procene stavke ponude zasnovane na projektu:

- Ručno kreirajte procenu direktno na stavci ponude koristeći detalje stavke ponude. 
- Kreirajte projekat i plan projekta, a zatim povežite projekat i zadatke na projektu sa stavkom ponude. Biće omogućen postupak uvoza procena iz projektnog plana u stavku ponude na osnovu informacija koje ste obezbedili.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Kreiranje procena direktno u stavci ponude zasnovane na projektu

Da biste kreirali procenu u stavci ponude zasnovanoj na projektu, izaberite karticu **Detalj stavke ponude**. Stavka koju kreirate na ovoj kartici rezimiraće navedenu vrednost za ovu stavku ponude. 

Da biste kreirali detalje stavke ponude, izaberite **+ Novi detalj stavke ponude** na podformi **Detalji stavke ponude**. Otvoriće se klizač za brzo kreiranje. Sledeća tabela daje detalje o poljima na stranici **Detalj stavke ponude** i kako vrednosti utiču na funkcionalnost.

| **Polje** | **Lokacija** | **Opis** | **Posledični uticaj** |
| --- | --- | --- | --- |
| Opis | Brzo kreiranje | Opis konkretne procene. | Ova vrednost podrazumeva detalje povezanog detalja stavke ponude za cenu koja se automatski kreira. |
| Klasa transakcije | Brzo kreiranje | Ova padajuća lista pruža klase transakcija koje su uključene na kartici **Opšti podaci** stavke ponude zasnovane na projektu.  | Ova vrednost podrazumeva detalje povezanog detalja stavke ponude za cenu koja se automatski kreira. |
| Izaberite proizvod | Brzo kreiranje | Primenjuje se kada je klasa transakcije **Materijal**. Možete izabrati da navedete da li je ova stavka procene za **Postojeći** (kataloški) proizvod ili za **Ručno dodat** proizvod. | Ova vrednost podrazumeva detalje povezanog detalja stavke ponude za cenu koja se automatski kreira. |
| Proizvod | Brzo kreiranje | ID proizvoda iz kataloga proizvoda. Ovo polje je omogućeno samo ako izaberete **Postojeći** u polje **Izaberite proizvod**. ID se koristi za preuzimanje prodajne cene iz cenovnika projekta u ponudu. | Ova vrednost podrazumeva detalje povezanog detalja stavke ponude za cenu koja se automatski kreira. |
| Ručno dodat proizvod | Brzo kreiranje | Tekstualno polje za upisivanje naziva proizvoda. Ovo polje je omogućeno samo ako izaberete **Ručno dodaj** u polju **Izaberite proizvod**.| Ova vrednost podrazumeva detalje povezanog detalja stavke ponude za cenu koja se automatski kreira. |
| Uloga | Brzo kreiranje | Uloga osobe koja će izvršiti ovaj posao ili snositi ovaj trošak. | Ova vrednost podrazumeva detalje povezanog detalja stavke ponude za cenu koja se automatski kreira. |
| Kategorija | Brzo kreiranje | Kategorija posla ili troška. | Ova vrednost podrazumeva detalje povezanog detalja stavke ponude za cenu koja se automatski kreira. |
| Datum početka | Brzo kreiranje | Datum početka posla. | Ovo polje podrazumeva detalje povezanog detalja stavke ponude za cenu koja se automatski kreira. |
| Datum završetka | Brzo kreiranje | Datum završetka posla. | Ovo polje podrazumeva detalje povezanog detalja stavke ponude za cenu koja se automatski kreira. |
| Jedinica za određivanje resursa | Brzo kreiranje | Jedinica za resurse koja će izazvati ovaj trošak i obezbediće resurse za rad na njima. | Ova vrednost podrazumeva detalje povezane stavke ponude za cenu koja se automatski kreira i koristi u preuzimanju cene koštanja. |
| Raspored jedinica | Brzo kreiranje | Grupa jedinica rada, proizvoda ili troškova. Jedinice pripadaju rasporedu jedinica ili grupi jedinica. Na primer, milje i kilometri su jedinice koje pripadaju grupi jedinica koja opisuje udaljenost. | Ova vrednost podrazumeva detalje povezanog detalja stavke ponude za cenu koja se automatski kreira. |
| Jedinica | Brzo kreiranje | Jedinica rada, proizvoda ili troškova. | Ova vrednost podrazumeva detalje povezanog detalja stavke ponude za cenu koja se automatski kreira. |
| Količina | Brzo kreiranje | Količina rada, proizvoda ili troškova. | Ova vrednost podrazumeva detalje povezanog detalja stavke ponude za cenu koja se automatski kreira. |
| Jedinična cena | Brzo kreiranje |Stopa naplate uloge koja obavlja posao, cena po jedinici proizvoda ili prodajna cena proizvoda ili kategorije troškova. Za ovo polje se podrazumeva **vreme** na osnovu kombinacije vrednosti aspekata za određivanje cena u redu cene uloga u cenovniku projekta koji važi na datum početka. Za **troškove**, ovo polje je podrazumevano iz podešavanja cene za kategoriju transakcija u cenovniku projekta koja važi na datum početka. Ako način određivanja cene za kategoriju transakcija nije cena po jedinici, nema podrazumevanih vrednosti i ovo polje ostaje prazno. Za proizvode podrazumevana vrednost se zasniva na redu **Stavka cenovnika** u cenovniku projekta koji važi na datum početka.| Stopa troškova uloge koja izvodi posao, cena po jedinici kategorije troškova ili jedinična cena proizvoda. Za ovo polje se podrazumeva **vreme** na osnovu kombinacije vrednosti aspekata za određivanje cena u redu cene uloga u cenovniku projekta koji važi na datum početka. Za **troškove**, ovo polje je podrazumevano iz podešavanja cene za kategoriju transakcija u cenovniku projekta koja važi na datum početka. Ako način određivanja cene za kategoriju transakcija nije cena po jedinici, nema podrazumevanih vrednosti i ovo polje ostaje prazno. Za proizvode podrazumevana vrednost se zasniva na redu **Stavka cenovnika** u cenovniku projekta koji važi na datum početka.|
| Procenjeni porez | Brzo kreiranje | Možete ručno da unesete procenjeni porez za ovaj rad ili trošak. | Nema posledičnog uticaja za ovo polje. |
| Iznos | Brzo kreiranje | U ovo polje možete ručno da unesete informacije ako su polja **Količina** i **Cena** ostala prazna. Ako ova polja nisu prazna, ovo polje postaje samo za čitanje i izračunava se kao (Količina \* Jedinična cena) + Porez. | Nema posledičnog uticaja za ovo polje. |


## <a name="update-prices-on-quote-line-details"></a>Ažuriranje cena u detaljima stavke ponude

Ako ste promenili cene na cenovniku projekta koji je priložen uz ponudu ili na cenovniku troškova ugovorne jedinice, možete izabrati **Preračunaj** na stranici **Ponuda** kako biste osvežili cene na pojedinačnim detaljima stavki ponude kako bi odražavali ovu promenu. Kada izaberete **Preračunaj**, prikazuje se upozorenje koje vas obaveštava da će se resetovati cene na detaljima stavki ponude za sve stavke u ovoj ponudi. Izaberite **Da** kako biste osvežili cene detalja prodaje i detalje troškova stavki ponude.

## <a name="access-quote-line-details-for-cost"></a>Pristupite detaljima stavki ponude za cenu

Na kartici **Detalji stavke ponude** izaberite red u mreži da biste omogućili neke radnje na traci s alatkama podforme. Prva radnja na traci alata podforme kada se izabere detalj stavke ponude je **Otvori detalje cene**. Izaberite **Otvori detalje cene** da biste videli povezanu stopu troškova i iznos za ovu stavku ponude.

> [!NOTE]
> Promena vrednosti jedinice resursa, količine, datuma, uloge ili kategorije u detaljima stavke ponude za cenu promeniće odgovarajuće vrednosti detalja stavke ponude za prodaju.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Valuta detalja stavke ponude za troškove i prodaju

Valuta detalja stavke ponude za podrazumevane vrednosti prodaje iz cenovnika projekta koji važi na datum početka detalja stavke ponude.

Valuta detalja stavke ponude za podrazumevane vrednosti cene iz cenovnika ugovorne jedinice ponude koji važi na datum početka detalja stavke ponude cene.

Proračuni isplativosti pretvaraju iznos na detaljima stavki ponude za cenu i prodaju u osnovnu valutu okruženja kako bi se prijavila ukupna procenjena marža u ponudi.

> [!NAPOMENA
> > Greške u zaokruživanju valuta i promenjene marže mogu se desiti zbog nedostatka efektivnih deviznih kurseva za datum. Koristite ove proračune samo na ugovorima za projekat, jer su to približne vrednosti i nisu stvarno zakonsko ili drugo izveštavanje koje zahteva veću preciznost zaokruživanja i svest o efektivnosti datuma za devizne kurseve.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
