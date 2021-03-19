---
title: Pregled predmeta ugovora zasnovanih na proizvodu – jednostavno
description: Ova tema pruža informacije o predmetima ugovora zasnovanim na proizvodu.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6e9ef33cc9c79f828e85733f4f5a199bce842700
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272675"
---
# <a name="product-based-contract-lines-overview---lite"></a>Pregled predmeta ugovora zasnovanih na proizvodu – jednostavno

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Možete kreirati predmete ugovora zasnovane na proizvodu u aplikaciji Dynamics 365 Project Operations. To mogu da budu ručno kreirane stavke ili stavke iz kataloga proizvoda.

## <a name="product-catalog"></a>Katalog proizvoda

Proizvodi u katalogu proizvoda imaju podrazumevanu jedinicu i grupu jedinica. Ako nekoliko proizvoda deli isti skup atributa, možete da kreirate grupu proizvoda koja takođe ima te atribute. Svi proizvodi iz jedne grupe proizvoda nasljeđuju isti skup atributa.

Na primer, kompanija prodaje licence za pretplatu na razne vrste softvera. Sav softver za pretplatu ima sledeća dva atributa:

- Broj korisnika
- Trajanje pretplate (u mesecima)

Da biste održali ovu vrstu kataloga, kreirajte porodicu proizvoda koja nosi ime **Softver za pretplatu**. Dodajte atribute, **Broj korisnika** i **Trajanje pretplate** porodici proizvoda. Zatim dodajte pojedinačne proizvode u porodicu proizvoda **Softver za pretplatu**.

## <a name="add-product-catalog-items-to-a-project-contract"></a>Dodavanje stavki iz kataloga proizvoda u ugovor

Ugovori projekata imaju odeljke za dve vrste stavki, stavke zasnovane na projektu i stavke zasnovane na proizvodu. Stavke zasnovane na proizvodu uključuju sve proizvode i jedinice u cenovniku proizvoda na ugovoru. Možete da dodate proizvode koji nisu deo cenovnika proizvoda ugovora.

Možete odabrati proizvode iz drugih cenovnika ili direktno iz kataloga proizvoda. Kada izaberete proizvode direktno iz kataloga proizvoda, koristi se podrazumevani cenovnik tog proizvoda za prodajnu cenu proizvoda. Ako podrazumevani cenovnik nije podešen, cena se podešava na 0 (nula).

Ako se predmet ugovora temelji na katalogu proizvoda, možete izmeniti prodajnu cenu direktno u predmetu ugovora. Predmet ugovora sadrži polje **Cene** sa dve vrednosti:

- **Izmena načina određivanja cena**
- **Koristi podrazumevano**

Ako polje **Cene** podesite na **Izmena načina određivanja cena**, podrazumevana cena se ne podešava. Unesite cenu za proizvod u predmetu ugovora. Ako polje postavite na **Koristi podrazumevane vrednosti**, koristi se podrazumevana prodajna cena i polje se ne može uređivati.

Nakon što instalirate Project Operations, podrazumevane prodajne cene se unose u stavke zasnovane na proizvodima u okviru ugovora. Polje **Određivanje cena** se podešava na **Izmeni način određivanja cena** tako da možete da uredite podrazumevanu cenu u predmetima ugovora. Ovo je izmena ponašanja stavki zasnovanih na proizvodima specifična za Project Operations u usluzi Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]