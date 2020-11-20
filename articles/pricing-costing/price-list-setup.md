---
title: Podešavanje cenovnika
description: Ova tema pruža informacije o tome kako da podesite cene i cenovnike.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 000c22944b187b6250f2e982d73020028093fde6
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180209"
---
# <a name="set-up-price-lists"></a>Podešavanje cenovnika

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Cenovnici u usluzi Dynamics 365 Project Operations predstavljaju katalog stopa. Stope izražavaju stope cena, prodaje i obračuna. U zavisnosti od toga da li cenovnik izražava stope cena ili prodaje i obračuna, kontekst cenovnika je **Prodaja** ili **Cena**.

Sledeća proširenja su specifična za Project Operations i primenjuju se na cenovnike iz usluge Dynamics 365 Sales.

- **Kontekst**: Ovo polje ima podržane vrednosti **Cena** i **Prodaja**. Nije podržana vrednost **Kupovina**. Postavite kontekst na **Cena** da biste napravili cenovnik troškova ili postavite kontekst na **Prodaja** za prodajni cenovnik. Cenovnik troškova određuje cenu za vrstu troškova na procenama i stvarnim zapisima. Prodajni cenovnici određuju cenu na procenama i stvarnim zapisima nenaplaćenih i naplaćenih tipova prodaje.
- **Jedinica vremena**: Ovo je podrazumevana jedinica vremena za koju se cena postavlja u odgovarajućoj tabeli **Uloga cena** za ovaj cenovnik.
- **Entitet cenovnika**: Ovo skriveno polje služi da Project Operations razlikuje cenovnike koji su specifični za ponudu ili ugovor od onih koji su standardni i globalno primenljivi.

## <a name="price-list-header"></a>Zaglavlje cenovnika

Sledeća tabela uključuje polja sa kartice **Opšti podaci** cenovnika koja su jedinstvena za Project Operations ili imaju značajne promene u ponašanju u odnosu na cenovnik u Prodaji.

| Polje | Lokacija | Opis | Posledični uticaj |
| --- | --- | --- | --- |
| Imenuj | Kartica **Opšti podaci** i obrasci **Brzo kreiranje** | Identitet cenovnika. | Cenovnik je prikazan sa ovom vrednošću na svim stranicama liste i padajućim opcijama.|
| Kontekst | Kartica **Opšti podaci** i obrasci **Brzo kreiranje** | Ovo polje se može postaviti na **Cena** ili **Prodaja**. | Cenovnik podešen na **Trošak** koristi se za traženje cene za procene troškova i stvarne troškove. Cenovnik podešen na **Prodaja** koristi se za traženje cene za procene prodaje i stvarne iznose prodaje. Samo cenovnici kojima je kontekst postavljen na **Prodaja** mogu se priložiti projektnim cenovnicima za klijente, projektnim ponudama i projektnim ugovorima. |
| Datum početka | Kartica **Opšti podaci** i obrasci **Brzo kreiranje** | Datum početka perioda u kome je cenovnik na snazi. | Uz polje **Datum završetka**, ovo polje se koristi da bi se utvrdilo koji cenovnik je primenljiv za određenu procenu ili stvarnu liniju. |
| Datum završetka | Kartica **Opšti podaci** i obrasci **Brzo kreiranje** | Datum završetka perioda u kome je cenovnik na snazi. | Uz polje **Datum početka**, ovo polje se koristi da bi se utvrdilo koji cenovnik je primenljiv za određenu procenu ili stvarnu liniju. |
| Valuta | Kartica **Opšti podaci** i obrasci **Brzo kreiranje** | Ovo polje se koristi za zadavanje podrazumevane valute u svakoj ulozi, kategoriji ili stavci cenovnika u vezi sa ovim cenovnikom. | Na cenovnicima, ulogama, kategorijama ili stavkama cenovnika opcije **Prodaja** ne mogu se kreirati linije ni u jednoj valuti osim u ovoj. Na cenovnicima opcije **Cena** možete kreirati liniju cena uloga u bilo kojoj valuti. Ovde definisana valuta se koristi kao podrazumevana. Korisničko podešavanje koje je povezano sa cenama uloga može zameniti ovu vrednost kako bi se omogućilo podešavanje stope cene rada u bilo kojoj valuti. Stope cene kategorija i cene stavki cenovnika mogu se postaviti samo u valuti koja je ovde definisana. |
| Jedinica vremena | Kartica **Opšti podaci** i obrasci **Brzo kreiranje** | Ovo polje se koristi za zadavanje podrazumevane vremenske jedinice na svakoj liniji uloge u vezi sa ovim cenovnikom. | Ova vrednost polja se koristi samo za podešavanje povezane cene uloge. Na cenovnicima opcije **Cena** i **Prodaja** možete kreirati liniju cena uloga u bilo kojoj jedinici vremena. Ovde definisana jedinica vremena se koristi kao podrazumevana. Korisnički podešene povezane cene uloga mogu zameniti ovu vrednost kako bi se omogućilo podešavanje stope cene rada i obračuna u bilo jedinici vremena. |
| Opis | Kartica **Opšti podaci** i obrasci **Brzo kreiranje** | Ovo tekstualno polje vam omogućava da navedete višelinijski opis cenovnika. | Ovo polje je prikazano u **Vezanim** prikazima na cenovniku u različitim entitetima koji imaju povezane cenovnike. |
