---
title: Rad sa predmetima ugovora zasnovanim na projektu
description: Ova tema pruža informacije o predmetima ugovora zasnovanim na projektu.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c1c935a998cba8bd42ba2f11c8310d41e72de94adac7c2cb83f4c7224127b10b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990063"
---
# <a name="work-with-projectbased-contract-lines"></a>Rad sa predmetima ugovora zasnovanim na projektu

Predmeti ugovora zasnovani na projektu u usluzi Dynamics 365 Project Operations dizajnirani su tako da drže ugovore o proceni i obračunu za određene komponente projektnog rada na angažmanu. Struktura stavke ugovora zasnovane na projektu proširena je za procene projekata i scenarije naplate sa sledećim konceptima:

- Način naplate
- Mapiranje projekata i zadataka
- Uključene klase transakcija
- Ograničenje koje ne sme da se prekorači
- Podešavanje naplativosti
- Procene korišćenjem detalja o predmeta ugovora
- Klijenti predmeta ugovora

Sledeća polja su uključena u karticu **Opšti podaci** predmeta ugovora zasnovanih na projektu. Ova polja pomažu u postavljanju osnove za detaljnu, celovitu procenu i aranžmane za obračun za rad zasnovan na projektu.

| Polje | Opis | Posledični uticaj |
| --- | --- | --- |
| **Ime** | Naziv predmeta ugovora koji identifikuje diskretnu komponentu ugovora koja se procenjuje. Za projektni ugovor kreiran iz ponude, ova vrednost se kopira iz odgovarajuće vrednosti stavke ponude zasnovane na projektu. | Vrednost ovog polja se kopira u stavku fakture za projekat koja se kreira iz ovog predmeta ugovora kada se kreira faktura. |
| **Način naplate** | Za projektni ugovor kreiran iz ponude, ova vrednost se kopira iz odgovarajućeg polja na stavki ponude. Ovo je skup opcija koji predstavlja dva glavna modela ugovaranja koja podržava usluga Project Operations:</br>- **Fiksna cena**</br>- **Vreme i materijal** | Na osnovu načina naplate navedenog predmeta ugovora, stvarna transakcija će biti obrađena. Ako predmet ugovora na koji se poziva stvarna vrednost ima način naplate vremena i materijala, kreiraju se zapisi stvarnih vrednosti troškova i nenaplaćene prodaje. Ako predmet ugovora na koji se poziva stvarna vrednost ima način obračuna sa fiksnom cenom, kreiraće se samo stvarni trošak. |
| **Project** | Koristite ovo polje za identifikovanje projekta koji će se koristiti za izvođenje radova na ovom angažmanu. | Vrednost u ovom polju se koristi zajedno sa poljima **Uključeni zadaci** i **Uključene klase transakcija** da se razreši referenca na predmet ugovora na stvarnoj vrednosti ili zapisu stavke procene. |
| **Sadrži vreme** | Oznaka označava da li su vremenske transakcije ili troškovi rada na izabranom projektu uključeni u ovaj predmet ugovora. Vrednost **Ne** označava da vremenske transakcije ili troškovi rada neće biti uključeni u ovaj predmet ugovora. Vrednost **Da** ukazuje na to da hoće. | Ova vrednost polja se koristi zajedno sa projektom da se razreši referenca predmeta ugovora na stvarnu vrednost ili zapis stavke procene. |
| **Sadrži trošak** | Oznaka označava da li će cena troškova na izabranom projektu biti uključena u ovaj predmet ugovora. Vrednost **Ne** označava da cena troškova na izabranom projektu neće biti uključena u ovaj predmet ugovora. Vrednost **Da** ukazuje na to da hoće. | Ova vrednost polja se koristi zajedno sa projektom da se razreši referenca predmeta ugovora na stvarnu vrednost ili zapis stavke procene. |
| **Sadrži nadoknadu** | Oznaka označava da li će naknade na izabranom projektu biti uključene u ovaj predmet ugovora. Vrednost **Ne** označava da naknade neće biti uključene u ovaj predmet ugovora. Vrednost **Da** ukazuje na to da hoće. | Ova vrednost polja se koristi zajedno sa projektom da se razreši referenca predmeta ugovora na stvarnu vrednost ili zapis stavke procene. |
| **Ugovoreni iznos** | Na predmetu ugovora sa fiksnom cenom, ovo je dogovorena vrednost koja će se fakturisati klijentu za sve radne komponente povezane sa ovim predmetom ugovora. Na predmetu ugovora za vreme i materijal, ovaj iznos je procenjena vrednost onoga što će se fakturisati klijentu za sve radne komponente povezane sa ovim predmetom ugovora. Za projektni ugovor koji je kreiran iz ponude, ova vrednost se kopira iz odgovarajućeg polja na stavki ponude. Kada predmet ugovora zasnovan na projektu sadrži detalje stavki, ovo polje se zaključava za uređivanje i sažima iz iznosa u detaljima linije ugovora. | Kada predmet ugovora sadrži detalje stavki, ova vrednost se može izmeniti promenom iznosa na detaljima stavki. U predmetu ugovora sa fiksnom cenom, ova vrednost se koristi za generisanje iznosa pre oporezivanja na periodičnim kontrolnim tačkama obračuna. |
| **Procenjeni porez** | Korisnik može da uređuje ovo polje kako bi uneo procenjeni iznos poreza u predmet ugovora. Kada predmet ugovora zasnovan na projektu sadrži detalje stavki, ovo polje se zaključava za uređivanje i sažima iz iznosa poreza u detaljima predmeta ugovora. | Kada predmet ugovora sadrži detalje stavki, ova vrednost se može izmeniti promenom iznosa poreza na detaljima stavki. U predmetu ugovora sa fiksnom cenom, ova vrednost se koristi za generisanje poreza na periodičnim kontrolnim tačkama obračuna. |
| **Ugovoreni iznos sa porezom** | Iznos predmeta ugovora sa porezom. Ovo polje je samo za čitanje i izračunava se kao **Ugovoreni iznos + porez**. | U predmetu ugovora sa fiksnom cenom, ova vrednost se koristi za generisanje periodičnih kontrolnih tačaka obračuna. |
| **Ograničenje koje ne sme da se prekorači** | Korisnik može da uređuje ovo polje i ono je dostupno samo na predmetima ugovora zasnovanim na projektu koji imaju način obračuna za vreme i materijal. | Korisnik može da uređuje ovo polje. Kada se reference na stvarne vrednosti za vreme i trošak odnose na ovaj predmet ugovora za vreme i materijal, iznos na stvarnoj vrednosti se procenjuje prema ograničenju koje ne sme da se premaši na ovom predmetu ugovora nakon obračuna za već potrošene i dodeljene iznose. |
| **Budžet klijenta** | Ovo polje može da se uređuje i kopira se iz odgovarajućeg polja na stavki ponude, ako je ugovor kreiran iz ponude. | Ovo polje se koristi samo za informacije i nema nikakav dalji značaj. |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Pravilo za validaciju za opcije na kartici Opšti podaci za predmete ugovora zasnovane na projektu

Pravilo: Projekat i određena klasa transakcija mogu biti uključeni samo u jednu liniju ugovora zasnovanu na projektu u ugovoru.

| Ugovor | Predmet ugovora | Project | Sadrži vreme | Sadrži trošak | Sadrži naknadu | Važi / Ne važi | Razlog                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C1       | CL1           | P1      | Da          | Da             | Da         | Ne važi       | Krši pravilo. Vreme, troškovi i naknade za projekat P1 uključeni su u oba predmeta ugovora, CL1 i CL2.                                                                                       |
| C1       | CL2           | P1      | Da          | Da             | Da         | Ne važi       | Krši pravilo. Vreme, troškovi i naknade za projekat P1 uključeni su u oba predmeta ugovora, CL1 i CL2.                                                                                       |
| C1       | CL1           | P1      | Da          | No              | Da         | Ne važi       | Krši pravilo. Vreme i naknade za projekat P1 uključeni su u oba predmeta ugovora, CL1 i CL2.                                                                                                   |
| C1       | CL2           | P1      | Da          | Da             | Da         | Ne važi       | Krši pravilo. Vreme i naknade za projekat P1 uključeni su u oba predmeta ugovora, CL1 i CL2.                                                                                                   |
| C1       | CL1           | P1      | Da          | No              | Da         | Važeći           | Vreme i naknade za projekat P1 su uključeni u CL1. Troškovi za projekat P1 uključeni su u CL2. </br>   Nema preklapanja onoga što je uključeno u svaki predmet ugovora i stoga je važeće.  |
| C1       | CL2           | P1      | No           | Da             | No          | Važeći           | Vreme i naknade za projekat P1 su uključeni u CL1. Troškovi za projekat P1 uključeni su u CL2. </br>   Nema preklapanja onoga što je uključeno u svaki predmet ugovora i stoga je važeće.  |
| C1       | CL1           | P1      | Da          | Da             | Da         | Ne važi       | Krši pravilo. Vreme, troškovi i naknade za projekat P1 uključeni su u predmete dva ugovora.                                                                                               |
| CL2      | CL2           | P1      | Da          | Da             | Da         | Ne važi       | Krši pravilo. Vreme, troškovi i naknade za projekat P1 uključeni su u predmete dva ugovora.                                                                                               |


[!INCLUDE[footer-include](../includes/footer-banner.md)]