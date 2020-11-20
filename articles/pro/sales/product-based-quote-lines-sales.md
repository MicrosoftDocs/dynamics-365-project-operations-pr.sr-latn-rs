---
title: Pregled stavki ponude zasnovane na proizvodu – jednostavno
description: Ova tema pruža informacije o radu sa stavkama ponude zasnovanim na proizvodu.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6aa428c486f149308ad078f9d7a80a0be0f0f04
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178205"
---
# <a name="product-based-quote-lines-overview---lite"></a>Pregled stavki ponude zasnovane na proizvodu – jednostavno

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Možete kreirati stavke ponude zasnovane na proizvodu u usluzi Dynamics 365 Project Operations. Stavke ponude zasnovane na proizvodu možete dodati ručno ili to mogu da budu stavke iz kataloga proizvoda.

## <a name="product-catalog"></a>Katalog proizvoda

Svaki proizvod u katalogu proizvoda ima podrazumevanu jedinicu i grupu jedinica. Ako više proizvoda deli isti skup atributa, možete da kreirate grupu proizvoda koja takođe deli te atribute. 

Na primer, kompanija prodaje licence za pretplatu na razne vrste softvera. Sav softver za pretplatu ima sledeća dva atributa:

- Broj korisnika
- Trajanje pretplate, mereno u mesecima

Da biste održavali ovu vrstu kataloga, kreirajte porodicu proizvoda pod imenom **Softver za pretplatu** i dodajte broj korisnika i trajanje pretplate kao atribute. Zatim možete da dodate pojedinačne proizvode u porodicu proizvoda **Softver za pretplatu**.

## <a name="add-product-catalog-items-to-a-project-quote"></a>Dodavanje stavki iz kataloga proizvoda u ponudu za projekat

Stranice **Ponuda za projekat** i **Ugovor za projekat** imaju odeljke za stavke zasnovane na projektu i stavke zasnovane na proizvodu. Za stavke zasnovane na proizvodu, padajuća lista u okviru stavke ponude ili predmeta ugovora za projekat uključuje sve proizvode i jedinice u cenovniku proizvoda. Takođe možete da dodate proizvode koji nisu deo cenovnika proizvoda.

Pored toga, možete odabrati proizvode iz drugih cenovnika ili direktno iz kataloga proizvoda. Kada izaberete proizvode direktno iz kataloga proizvoda, koristi se podrazumevani cenovnik tog proizvoda da biste dobili prodajnu cenu proizvoda. Ako podrazumevani cenovnik nije podešen, cena se podešava na nula (0).

Kada se stavka ponude zasniva na katalogu proizvoda, možete izmeniti prodajnu cenu direktno u stavci ponude. Stavka ponude u polju **Određivanje cene** sa dve dostupne vrednosti:

- **Izmena načina određivanja cena**
- **Koristi podrazumevano**

Ako izaberete **Izmena načina određivanja cena**, podrazumevana cena se ne postavlja. Umesto toga, morate da unesete cenu proizvoda u stavku ponude. Ako izaberete **Koristi podrazumevano**, koristi se podrazumevana prodajna cena i polje se zaključava za uređivanje.

Podrazumevane prodajne cene se unose u stavke zasnovane na proizvodima u okviru ponude. Polje **Određivanje cena** se tada podešava na **Izmeni način određivanja cena** tako da možete da uredite podrazumevanu cenu u stavkama ponude. Ovo je ponašanje specifično za Project Operations pri izmeni stavki zasnovanih na proizvodima u usluzi Dynamics 365 Sales.