---
title: Procena stavke ponude za projekat
description: Ova tema pruža informacije o načinu kreiranja procene na stavci ponude za projekat.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 84283ac055aea802fadbd6814ea65a6d3dc01d29e1e3c6290ef11f72f6a75692
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003968"
---
# <a name="estimate-a-project-quote-line"></a>Procena stavke ponude za projekat

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Stavka ponude zasnovana na projektu sadrži detalje koji pomažu u proceni troškova i potencijalnog prihoda od posla koji se odnosi na isporuku stavke ponude.

Da biste procenili stavku ponude zasnovanu na projektu, u stavci ponude izaberite karticu **Detalj stavke ponude**. Postoje dva načina da kreirate procenu na stavci ponude zasnovane na projektu:

   - Ručno kreirajte procenu direktno na stavci ponude koristeći detalje stavke ponude. 
   - Kreirajte projekat i plan projekta, a zatim povežite projekat i zadatke na projektu sa stavkom ponude. Biće omogućen postupak uvoza procena iz projektnog plana u stavku ponude na osnovu informacija koje ste obezbedili.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Kreiranje procena direktno u stavci ponude zasnovane na projektu

Da biste kreirali procene direktno na stavci ponude zasnovane na projektu, sledite ove korake:

1. Da biste kreirali procenu u stavci ponude zasnovanoj na projektu, izaberite karticu **Detalj stavke ponude**. Stavka koju kreirate na ovoj kartici rezimiraće navedenu vrednost za ovu stavku ponude. 
2. Da biste kreirali detalje stavke ponude, izaberite **+ Novi detalj stavke ponude** na podformi **Detalji stavke ponude**. Otvoriće se klizač za brzo kreiranje. Sledeća polja na stranici **Stavka ponude**.

| **Polje** | **Lokacija** | **Opis** | **Posledični uticaj** |
| --- | --- | --- | --- |
| Opis | Brzo kreiranje | Opis konkretne procene. | Ova vrednost podrazumeva detalje povezanog detalja stavke ponude za cenu koja se automatski kreira. |
| Klasa transakcije | Brzo kreiranje | Ova padajuća lista pruža klase transakcija koje su uključene u karticu **Opšti podaci** stavke ponude zasnovane na projektu.  | Ova vrednost podrazumeva detalje povezanog detalja stavke ponude za cenu koja se automatski kreira. |
| Izaberite proizvod | Brzo kreiranje | Primenjuje se kada je klasa transakcije **Materijal**. Možete izabrati da navedete da li je ova stavka procene za **Postojeći** (kataloški) proizvod ili za **Ručno dodat** proizvod. | Ova vrednost podrazumeva detalje povezanog detalja stavke ponude za cenu koja se automatski kreira. |
| Proizvod | Brzo kreiranje | ID proizvoda iz kataloga proizvoda. Ovo polje je omogućeno samo kada izaberete **Postojeći** u polju **Izaberite proizvod**. ID se koristi za preuzimanje prodajne cene iz cenovnika projekta u ponudu. | Ova vrednost podrazumeva detalje povezanog detalja stavke ponude za cenu koja se automatski kreira. |
| Ručno dodat proizvod | Brzo kreiranje | Tekstualno polje za upisivanje naziva proizvoda. Ovo polje je omogućeno samo kada izaberete **Ručno dodaj** u polju **Izaberite proizvod**.| Ova vrednost podrazumeva detalje povezanog detalja stavke ponude za cenu koja se automatski kreira. |
| Uloga | Brzo kreiranje | Uloga osobe koja će izvršiti ovaj posao ili snositi ovaj trošak. | Ova vrednost podrazumeva detalje povezanog detalja stavke ponude za cenu koja se automatski kreira. |
| Kategorija | Brzo kreiranje | Kategorija posla ili troška. | Ova vrednost podrazumeva detalje povezanog detalja stavke ponude za cenu koja se automatski kreira. |
| Datum početka | Brzo kreiranje | Datum početka posla. | Ovo polje podrazumeva detalje povezanog detalja stavke ponude za cenu koja se automatski kreira. |
| Datum završetka | Brzo kreiranje | Datum završetka posla. | Ovo polje podrazumeva detalje povezanog detalja stavke ponude za cenu koja se automatski kreira. |
| Preduzeće koje određuje resurse | Brzo kreiranje | Preduzeće koje određuje resurse ili pravno lice koje izaziva ovaj trošak i obezbeđuje resurse za rad na njima. | Ta vrednost podrazumeva detalje povezane stavke ponude za cenu koja se automatski kreira i koristi u preuzimanju cene koštanja. |
| Jedinica za određivanje resursa | Brzo kreiranje | Jedinica za određivanje resursa koja izaziva ovaj trošak i obezbeđuje resurse za rad na njima. | Ova vrednost podrazumeva detalje povezane stavke ponude za cenu koja se automatski kreira i koristi u preuzimanju cene koštanja. |
| Raspored jedinica | Brzo kreiranje | Grupa jedinica rada, proizvoda ili troškova. Jedinice pripadaju rasporedu jedinica ili grupi jedinica. Na primer, milje i kilometri su jedinice koje pripadaju grupi jedinica koja opisuje udaljenost. | Ova vrednost podrazumeva detalje povezanog detalja stavke ponude za cenu koja se automatski kreira. |
| Jedinica | Brzo kreiranje | Jedinica rada, proizvoda ili troškova. | Ova vrednost podrazumeva detalje povezanog detalja stavke ponude za cenu koja se automatski kreira. |
| Količina | Brzo kreiranje | Količina rada, proizvoda ili troškova. | Ova vrednost podrazumeva detalje povezanog detalja stavke ponude za cenu koja se automatski kreira. |
| Jedinična cena | Brzo kreiranje |Stopa naplate uloge koja obavlja posao, cena po jedinici proizvoda ili prodajna cena proizvoda ili kategorije troškova. Podrazumevana vrednost za **vreme** na osnovu kombinacije vrednosti aspekata za određivanje cena stavke cene uloge u cenovniku projekta koja je na snazi na datum početka. Za **troškove**, ovo polje je podrazumevano iz podešavanja cene za kategoriju transakcija u cenovniku projekta koja važi na datum početka. Ako način određivanja cene za kategoriju transakcija nije cena po jedinici, nema podrazumevanih vrednosti i ovo polje ostaje prazno. Za proizvode podrazumevana vrednost ovog polja se zasniva na redu **Stavka cenovnika** u cenovniku projekta koji važi na datum početka.| Stopa troškova uloge koja izvodi posao, cena po jedinici kategorije troškova ili jedinična cena proizvoda. Podrazumevana vrednost za **vreme** je zasnovana na kombinaciji vrednosti aspekata za određivanje cena u redu cene uloga u cenovniku koštanja povezanog sa ugovornom jedinicom i koji je na snazi na datum početka. Za troškove se podrazumevana vrednost zasniva na liniji cena kategorije cenovnika troškova koja je priložena ugovornoj jedinici i koja važi na datum početka. Ako metod određivanja cene za kategoriju transakcija nije cena po jedinici, nema podrazumevanih vrednosti i ovo polje ostaje prazno. Za proizvode, podrazumevana vrednost ovog polja se zasniva na stavci **Stavka cenovnika** cenovnika troškova koja je priložena ugovornoj jedinici i koja važi na datum početka.|
| Procenjeni porez | Brzo kreiranje | Možete ručno da unesete procenjeni porez za ovaj rad ili trošak. | Nema posledičnog uticaja za ovo polje. |
| Iznos | Brzo kreiranje | U ovo polje možete ručno da unesete informacije ako su polja **Količina** i **Cena** ostala prazna. Ako ova polja nisu prazna, ovo polje postaje samo za čitanje i izračunava se kao (Količina \* Jedinična cena) + Porez. | Nema posledičnog uticaja za ovo polje. |

## <a name="update-prices-on-quote-line-details"></a>Ažuriranje cena u detaljima stavke ponude

Ako ste promenili cene na cenovniku projekta koji je priložen uz ponudu ili na cenovniku troškova ugovorne jedinice, možete odabrati **Preračunaj** na stranici **Ponuda**, da osvežite cene u detaljima pojedinačnih stavki ponude kako bi odrazile ovu promenu. Kada izaberete **Preračunaj**, prikazuje se upozorenje koje vas obaveštava da će se resetovati cene na detaljima stavki ponude za sve stavke u ovoj ponudi. Izaberite **Da** kako biste osvežili cene detalja prodaje i detalje troškova stavki ponude.

## <a name="access-quote-line-details-for-cost"></a>Pristupite detaljima stavki ponude za cenu

Da biste pristupili detaljima ponude za cenu, sledite ove korake:

1. Na kartici **Detalji stavke ponude**, izaberite red u mreži da biste omogućili radnje na traci s alatkama podforme. 
2. Izaberite **Otvori detalje cene** da biste videli povezanu stopu troškova i iznos za ovu stavku ponude.

> [!NOTE]
> Promena vrednosti jedinice resursa, količine, datuma, uloge ili kategorije u detaljima stavke ponude za cenu promeniće odgovarajuće vrednosti detalja stavke ponude za prodaju.

## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Valuta detalja stavke ponude za troškove i prodaju

Valuta na detaljima stavke ponude za podrazumevane vrednosti prodaje iz cenovnika projekta koja važi na datum početka detalja stavke ponude.

Valuta na detaljima stavke ponude za podrazumevane cene iz cenovnika jedinice ugovaranja ponude koji važi na datum početka detalja stavke ponude za cenu.

> [!NOTE]
> Proračuni isplativosti pretvaraju iznos na detaljima stavki ponude za cenu i prodaju u osnovnu valutu okruženja kako bi se prijavila ukupna procenjena marža u ponudi. Greške u zaokruživanju valuta i promenjene marže mogu se desiti zbog nedostatka efektivnih deviznih kurseva za datum. Koristite ove proračune samo na ponudama za projekat, jer su to približne vrednosti i nisu stvarno zakonsko ili drugo izveštavanje koje zahteva veću preciznost zaokruživanja i svest o efektivnosti datuma za devizne kurseve.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
