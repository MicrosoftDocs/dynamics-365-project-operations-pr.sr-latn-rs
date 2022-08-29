---
title: Ključni koncepti u podugovaranju
description: Ovaj članak sadrži objašnjenja o nekim ključnim konceptima koji se primenjuju na podizvođač u korporaciji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e75f2cf9c1092604e43e5cb60dda0e2a1b7dcd64
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262187"
---
# <a name="key-concepts-in-subcontracting"></a>Ključni koncepti u podugovaranju


_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Članak sadrži objašnjenja o nekim ključnim konceptima kojih bi trebalo da budete svesni pre nego što počnete da koristite funkcionalnost podizvođanja u korporaciji Microsoft Dynamics 365 Project Operations.

## <a name="contracting-unit-on-the-subcontract"></a>Ugovorna jedinica podugovora

Ugovorna jedinica predstavlja odeljenje ili praksu koja je vlasnik isporuke konačnog projekta. Ugovorna jedinica je takođe odeljenje koje stupa u ugovorni odnos sa dobavljačem.

## <a name="purchase-currency"></a>Kupovna valuta

U usluzi Project Operations, kupovna valuta je valuta u kojoj je napravljen podugovor. To je takođe valuta u kojoj se evidentiraju troškovi podizvođača na projektu. Kupovna valuta može se razlikovati od valute projekta, a valuta projekta se može razlikovati od prodajne valute.

## <a name="billing-methods-on-subcontract-lines"></a>Metode naplate na stavkama podugovora

Za projekte obično postoje modeli ugovaranja sa fiksnom naknadom i prema potrošnji. Usluga Project Operations podržava ove metode naplate u kontekstu prodaje i kupovine. Za kupovinu, metode naplate funkcionišu na sledeći način:

- **Vreme i materijal** – Kada linija stavka podugovora koristi metod naplate **Vreme i materijal**, trošak vremena se evidentira u projektu jer podizvođači rade na tom projektu i evidentiraju vreme. Ove transakcije troškova od podizvođača se zatim uparuju sa stavkama na fakturama dobavljača. U ovom modelu, rukovodioci projekata koji koriste Project Operations mogu da upare i provere stavke faktura dobavljača sa vremenom podizvođača koje je evidentirano i odobreno. Nakon što je završetka verifikacije, prethodni stvarni troškovi koji su evidentirani nakon odobrenja se poništavaju, a novi stvarni troškovi zasnovani na fakturi dobavljača kreiraju se na projektu.
- **Fiksna cena** – U ovom modelu ugovaranja sa fiksnim naknadama, fakture dobavljača su zasnovane na fiksnim ključnim tačkama. Međutim, resursi podizvođača takođe mogu prijaviti vreme. Zatim vreme pregleda i odobrava rukovodilac projekta. Nakon odobravanja, usluga Project Operations kreira privremene stvarne troškove za projekat. Nakon što dobavljač pošalje fakturu za ključnu tačku, rukovodilac projekta može da uporedi prethodno evidentirane stvarne troškove sa ključnom tačkom. Kada se provera završi, stvarni troškovi se poništavaju i evidentiraju se troškovi zasnovani na ključnim tačkama.

## <a name="project-price-lists-on-subcontracts"></a>Cenovnici projekata za podugovore

Cenovnici projekata su cenovnici koji se koriste za podešavanje otkupnih cena za vreme, troškove i druge komponente vezane za projekat. Može postojati više cenovnika, od kojih svaki može da ima sopstveni podugovor sa datumom stupanja na snagu u usluzi Project Operations. Usluga Project Operations ne podržava preklapanje datuma stupanja na snagu na cenovnicima projekata za podugovor.

## <a name="transaction-classes-on-subcontracts"></a>Klase transakcija na podugovorima

Projektne operacije podržavaju četiri vrste klasa transakcija:

- Vreme
- Trošak
- Materijal
- Naknada

Troškovi kupovine mogu da se procene i nastanu samo u klasama transakcija **Vreme**, **Troškovi** i **Materijal**. **Nadoknada** je klasa transakcija samo za prihod i nije dostupna u sadržaju kupovine.

## <a name="purchase-pricing-dimensions"></a>Dimenzije za cene kupovine

Dimenzije cena vam omogućavaju da odlučite koji se atributi koriste za podešavanje kupovne cene i određivanje podrazumevanih vrednosti pri vremenskim transakcijama. Povezano sa cenama, usluga Project Operations podržava samo skupove fiksnih dimenzija za podešavanje kupovne cene i određivanje podrazumevanih vrednosti. Atributi su za podešavanje kupovne cene i određivanje podrazumevanih vrednosti na stavkama podugovora i vremenskim transakcijama su **Uloga** i **Resurs koji može da se rezerviše**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
