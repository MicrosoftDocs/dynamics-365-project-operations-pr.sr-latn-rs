---
title: Procena stavke ponude zasnovane na projektu
description: Ova tema pruža informacije o tome kako da kreirate procenu na stavci ponude zasnovane na projektu.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dbd3876e555ee6bc70308ef11a3528a5dd8b6a32
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273569"
---
# <a name="estimating-a-project-based-quote-line"></a>Procena stavke ponude zasnovane na projektu

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Stavka ponude zasnovana na projektu sadrži detalje koji pomažu u proceni troškova i potencijalnog prihoda od posla koji se odnosi na isporuku stavke ponude.

Da biste procenili stavku ponude zasnovanu na projektu, u stavci ponude zasnovane na projektu izaberite karticu **Detalj stavke ponude**. Postoje dva načina za kreiranje procene stavke ponude zasnovane na projektu:

- Ručno kreirajte procenu direktno na stavci ponude koristeći detalje stavke ponude 
- Kreirajte projekat i plan projekta, a zatim povežite projekat i zadatke na projektu sa stavkom ponude. Biće omogućen postupak uvoza procena iz projektnog plana u stavku ponude na osnovu informacija koje ste obezbedili.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Kreiranje procena direktno u stavci ponude zasnovane na projektu

Da biste kreirali procenu u stavci ponude zasnovanoj na projektu, izaberite karticu **Detalj stavke ponude**. Stavka koju kreirate na ovoj kartici rezimiraće navedenu vrednost za ovu stavku ponude. 

Da biste kreirali detalje stavke ponude, izaberite **+ Novi detalj stavke ponude** na podformi **Detalji stavke ponude**. Otvoriće se klizač za brzo kreiranje. Sledeća polja na obrascu **Stavka ponude**:

| **Polje** | **Lokacija** | **Opis** | **Posledični uticaj** |
| --- | --- | --- | --- |
| Opis | Brzo kreiranje | Opis konkretne procene. | Ovo polje podrazumevano sadrži cenu iz povezane stavke ponude za cenu koja se automatski kreira. |
| Klasa transakcije | Brzo kreiranje | Ova padajuća lista pruža klase transakcija koje su uključene u karticu **Opšti podaci** stavke ponude zasnovane na projektu.  | Ovo polje podrazumevano sadrži cenu iz povezane stavke ponude za cenu koja se automatski kreira. |
| Uloga | Brzo kreiranje | Osoba koja će izvršiti ovaj posao ili snositi ovaj trošak. | Ovo polje podrazumevano sadrži cenu iz povezane stavke ponude za cenu koja se automatski kreira. |
| Kategorija | Brzo kreiranje | Kategorija rada ili troška. | Ovo polje podrazumevano sadrži cenu iz povezane stavke ponude za cenu koja se automatski kreira. |
| Datum početka | Brzo kreiranje | Datum početka rada. | Ovo polje podrazumevano sadrži cenu iz povezane stavke ponude za cenu koja se automatski kreira. |
| Datum završetka | Brzo kreiranje | Datum završetka rada. | Ovo polje podrazumevano sadrži cenu iz povezane stavke ponude za cenu koja se automatski kreira. |
| Jedinica za određivanje resursa | Brzo kreiranje | Jedinica za obezbeđenje resursa koja će snositi ovaj trošak i obezbediti resurs za rad na njoj. | Ovo polje podrazumevano sadrži cenu iz povezane stavke ponude za cenu koja se automatski kreira. Ovo polje se takođe koristi za pronalaženje cene koštanja. |
| Raspored jedinica | Brzo kreiranje | Grupa jedinica rada ili troškova. Jedinice pripadaju rasporedu jedinica ili grupi jedinica. Na primer, milje i kilometri su jedinice koje pripadaju grupi jedinica koje opisuju udaljenost. | Ovo polje podrazumevano sadrži cenu iz povezane stavke ponude za cenu koja se automatski kreira. |
| Jedinica | Brzo kreiranje | Jedinica rada ili troškova. | Ovo polje podrazumevano sadrži cenu iz povezane stavke ponude za cenu koja se automatski kreira. |
| Količina | Brzo kreiranje | Količina rada ili troškova | Ovo polje podrazumevano sadrži cenu iz povezane stavke ponude za cenu koja se automatski kreira. |
| Cena po jedinici | Brzo kreiranje | Obračun uloge koja izvodi posao ili prodajna cena kategorije troškova. Ovo polje podrazumeva vreme na osnovu uloge i kombinacije jedinica resursa na cenovniku projekta koji važi na datum početka. Za troškove, ovo polje podrazumevano podešava cenu za kategoriju transakcija u cenovniku projekta koji važi na datum početka. Ako način određivanja cene za kategoriju transakcija nije cena po jedinici, nema podrazumevanih vrednosti i ovo polje ostaje prazno. | Obračun uloge koja izvodi posao ili prodajna cena po jedinici kategorije troškova. Ovo polje podrazumeva vreme na osnovu kombinacije uloge i jedinica resursa po ceni ugovorne jedinice iz cenovnika ponude koji važi na datum početka. Za troškove, ovo polje podrazumeva podešavanje cene za kategoriju transakcija u cenovniku koštanja ugovorne jedinice koja važi na datum početka. Ako način određivanja cene za kategoriju transakcija nije cena po jedinici, nema podrazumevanih vrednosti i ovo polje ostaje prazno. |
| Procenjeni porez | Brzo kreiranje | Možete ručno da unesete procenjeni porez za ovaj rad ili trošak. | Nema posledičnog uticaja ovog polja. |
| Iznos | Brzo kreiranje | U ovo polje možete ručno da unesete informacije ako su polja **Količina** i **Cena** ostala prazna. Ako ova polja nisu prazna, ovo polje postaje samo za čitanje i izračunava se kao (Količina \* Jedinična cena) + Porez. | Nema posledičnog uticaja ovog polja. |

## <a name="update-prices-on-quote-line-details"></a>Ažuriranje cena u detaljima stavke ponude

Ako ste promenili cene na cenovniku projekta koji je priložen uz ponudu ili na cenovniku troškova ugovorne jedinice, možete odabrati **Preračunaj** na stranici **Ponuda**, da osvežite cene u detaljima pojedinačnih stavki ponude kako bi odrazile ovu promenu. Kada izaberete **Preračunaj**, pojavljuje se upozorenje koje vas obaveštava da će se resetovati cene na detaljima stavke ponude za sve stavke ove ponude. Izaberite **Da** kako biste osvežili cene detalja prodaje i detalje troškova stavki ponude.

## <a name="access-quote-line-details-for-cost"></a>Pristupite detaljima stavki ponude za cenu

Na kartici **Detalji stavke ponude** izaberite red u mreži da biste omogućili neke radnje na traci s alatkama podforme. Prva radnja na traci alata podforme kada se izabere detalj stavke ponude je **Otvori detalje cene**. Izaberite **Otvori detalje cene** da biste videli povezanu stopu troškova i iznos za ovu stavku ponude.

> [!NOTE]
> Promena vrednosti jedinice resursa, količine, datuma, uloge ili kategorije u detaljima stavke ponude za cenu promeniće odgovarajuće vrednosti detalja stavke ponude za prodaju.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Valuta detalja stavke ponude za troškove i prodaju

Valuta detalja stavke ponude za podrazumevane vrednosti prodaje iz cenovnika projekta koji važi na datum početka detalja stavke ponude.

Valuta detalja stavke ponude za podrazumevane vrednosti cene iz cenovnika ugovorne jedinice ponude koji važi na datum početka detalja stavke ponude cene.

Proračuni isplativosti pretvaraju iznos na detaljima stavki ponude za cenu i prodaju u osnovnu valutu okruženja kako bi se prijavila ukupna procenjena marža u ponudi.

To bi moglo dovesti do grešaka u zaokruživanju valuta i promene marži zbog nedostatka efektivnih deviznih kurseva koji važe na taj datum. Koristite ove proračune na ponudama za projekte samo kao aproksimacije, a ne stvarno zakonsko ili drugo izveštavanje koje zahteva veću preciznost zaokruživanja i svest o datumu važenja za devizne kurseve.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]