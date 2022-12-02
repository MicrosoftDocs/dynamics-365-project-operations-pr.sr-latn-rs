---
title: Podešavanje stopa cena i prodaje za troškove
description: Ovaj članak pruža informacije o tome kako da postavite stope cena i prodaje za kategorije transakcija i troškova.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c503230348750af246f6ee7a4af1176d7bf22ba4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911889"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a>Podešavanje stopa cena i prodaje za troškove

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Možete podesiti troškove i prodajne cene za kategorije transakcija u usluzi Dynamics 365 Project Operations. Budući da su cene troškova i prodajne cene dizajnirani za troškove, svaka kategorija transakcije koja ih uključuje takođe mora biti postavljena kao kategorija troškova. Ova postavka osigurava tačnost posledične funkcionalnosti. Troškovi i prodajne cene za kategorije transakcija mogu se navesti samo u jednoj valuti, koja mora biti valuta u zaglavlju cenovnika.

Da biste postavili troškove i stope prodaje za kategorije transakcija, izvršite sledeće korake. 

1. Idite na **Prodaja** > **Klijenti** > **Cenovnici**.
2. Izaberite **Novo** da biste kreirali novi cenovnik. 
3. Na kartici **Cene kategorija**, u meniju podforme izaberite **Nova cena kategorije**. 
4. Na stranici **Brzo kreiranje**, unesite kategoriju transakcije i jedinicu za koju kreirate novu cenu.

Sledeća tabela navodi polja na kartici **Opšti podaci** i stranici **Brzo kreiranje** linije cena kategorije za ulogu koju treba imati na umu dok kreirate cene kategorija na prodajnom ili cenovniku koštanja:

| Polje | Lokacija | Opis | Posledični uticaj |
| --- | --- | --- | --- |
| Kategorija transakcije | Kartica **Opšti podaci** i stranice **Brzo kreiranje** | Izaberite kategoriju transakcije za koju kreirate prodajnu ili troškovnu cenu. | Kategorija transakcije na dolaznoj proceni ili trenutnom stanju za troškove će se podudarati sa ovom linijom kako bi se zadala stopa cene ili prodaje kategorije transakcije. |
| Raspored jedinica | Kartica **Opšti podaci** i stranice **Brzo kreiranje** | Raspored jedinica je podrazumevan prema rasporedu jedinica kategorije transakcije. | Nema posledičnog uticaja iz ovog polja. |
| Jedinica | Kartica **Opšti podaci** i stranice **Brzo kreiranje** | Izaberite jedinicu za koju se stope podešavaju. | Jedinica na dolaznoj proceni ili stvarna cena upoređuje se sa jedinicom na ovoj liniji da bi se podrazumevala stopa na proceni troškova ili stvarnoj ceni. |
| Način određivanja cena | Kartica **Opšti podaci** i stranice **Brzo kreiranje** | Moguće vrednosti polja **Metod određivanja cena** su **Cena po jedinici**, **Po ceni**, i **Provizija preko troškova**. | Tokom podešavanja cena, odabir **Cena po jedinici** zaključava polje **Procenat** na liniji cena kategorije. Ako je izabrano **Po ceni**, polja **Cena** i **Procenat** su zaključana na prodajnom cenovniku. Izbor **Provizija preko troškova** zaključava polje **Cena** na prodajnom cenovniku. Na dolaznom stvarnom redu za troškove, metoda određivanja cena **Po ceni** ili **Provizija preko troškova** rezultira time da se odgovarajućoj nefakturisanoj prodajnoj liniji dodeli cena koja je jednaka ceni na stvarnom trošku ili se izračunava kao provizija iznad cene. |
| Cena | Kartica **Opšti podaci** i stranice **Brzo kreiranje** | Postavite stopu po jedinici za kategoriju transakcije i kombinaciju jedinica. Na primer, stopa pređenih kilometara je 10 USD po milji i 8 USD po kilometru. | Stopa kilometraže će biti stopa koja podrazumeva jediničnu cenu ili trošak dolazne procene ili stvarne linije za klasu transakcije troška.|
| Procenat | Kartica **Opšti podaci** i stranice **Brzo kreiranje** | Postavite procenat preko troškova za kategoriju transakcije i kombinaciju jedinica. Na primer, stopa prodaje avionskih karata treba da bude viša za 10 procenata u odnosu na troškove nastalih avionskih troškova. | Ovaj procenat preko troškova je primenjiv na prodajni cenovnik kada je izabrani metod određivanja cena **Provizija preko troškova**. |
| Valuta | Kartica **Opšti podaci** i stranice **Brzo kreiranje** | Ova vrednost podrazumevano potiče iz valute u zaglavlju cenovnika. Za određivanje cena kategorija transakcija, valutu nije moguće zameniti. | Ova valuta je podrazumevana za cenu po jedinici dolazne stvarne prodaje za klasu transakcije troškova za cenu i prodaju. |

## <a name="pricing-methods-for-expenses"></a>Metode određivanja cena za troškove

Kada postavljate cene kategorija koje su relevantne samo u kontekstu određivanja troškova, možete koristiti jedan od sledeća tri načina određivanja cena:

- **Cena po jedinici**
- **Po ceni**
- **Provizija preko troškova**

### <a name="price-per-unit"></a>Cena po jedinici
Kada je ovaj metod određivanja cena odabran na liniji cena kategorije koja je povezana sa prodajnim cenovnikom, cena podrazumeva kombinaciju kategorije i jedinice i u proceni i u stvarnoj vrednosti. Procena se odnosi na linije za procenu troškova za troškove projekta, detalje linije citata i detalje linije ugovora za troškove.

### <a name="at-cost"></a>Po ceni
Kada je ovaj metod određivanja cena odabran na liniji cena kategorije koja je povezana sa prodajnim cenovnikom, cena podrazumeva kombinaciju kategorije i jedinice samo za stvarnu vrednost troškova. Na primer, nenaplaćeni stvarni iznosi prodaje za klasu transakcije troškova. Jedinična cena određuje se na nenaplaćenom stvarnom iznosu prodaje od jedinične cene na stvarnom trošku za taj trošak. Neplaćanje cena na osnovu troškova ne vrši se na osnovu procene troškova za troškove ili detalja o liniji ponude i ugovorne linije za troškove.

### <a name="markup-over-cost"></a>Provizija preko troškova
Kada je ovaj metod određivanja cena odabran na liniji cena kategorije koja je povezana sa prodajnim cenovnikom, cena podrazumeva kombinaciju kategorije i jedinice samo za stvarnu vrednost troškova. Na primer, nenaplaćeni stvarni iznosi prodaje za klasu transakcije troškova. Ova jedinična cena postavlja se na nenaplaćenom stvarnom iznosu prodaje na izračunatu vrednost iz jedinične cene na stvarnom trošku za taj trošak nakon primene definisanog procenta provizije. Neplaćanje cena na osnovu troškova ne vrši se na osnovu procene troškova za troškove ili detalja o liniji ponude i ugovorne linije za troškove.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
