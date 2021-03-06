---
title: Upravljanje složenim jedinicama, kao što su po korisniku mesečno za stavke ponude zasnovane na proizvodima
description: Ova tema pruža informacije o upravljanju složenim jedinicama za stavke ponude zasnovane na proizvodu.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 741230e69302138cce8f7379f520f7178e1c80af
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965876"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines"></a>Upravljanje složenim jedinicama, kao što su po korisniku mesečno za stavke ponude zasnovane na proizvodima

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Dynamics 365 Project Operations koristi količinske faktore da podrži prodaju proizvoda zasnovanih na pretplati. Za proizvode zasnovane na pretplati, količina stavki ponude ili predmeta ugovora o projektu izražava se kao broj korisnik-meseci.

Obično se cena softvera za pretplatu čuva u katalogu kao cena po korisniku mesečno. Tokom procesa prodaje, cena u stavci ponude je obično cena po korisniku, mesečno, do koje se došlo pregovorima i popustima od strane IT agenta prodaje. Svaka pogodba ima različit broj korisnika i različit broj meseci pretplate. Količina se koristi za izračunavanje stavke ponude je proizvod broja korisnika i broja meseci pretplate.

Da bi podržala ovu vrstu prodaje, usluga Project Operations uvodi koncept faktora količine. Količinski faktori se oslanjaju na atribute proizvoda u sistemu Dynamics 365. Kada konfigurišete određene osobine proizvoda, Project Operations vam omogućava da označite podskup tih svojstava ili sva svojstva kao faktore količine.

Project Operations potvrđuje da se kao faktori količine označavaju samo numerička svojstva ili svojstva proizvoda koja imaju numerički tip podataka. Kada u red ponude dodate proizvod sa faktorima količine, polje **Količina** postaje samo za čitanje. Kada unesete vrednosti za svojstva proizvoda koja su količinski faktori, Project Operations izračunava količinu stavke ponude.

Na primer, Dynamics 365 Sales može imati sledeća svojstva:

- **Br. korisnika**: broj korisnika
- **Br. meseca**: broj meseci pretplate
- **SKU proizvoda**

Možete označiti **Broj korisnika** i **Broj meseci** kao faktore količine, uređivanjem svojstava u stavci proizvoda.

Da biste kreirali faktore količine iz svojstava proizvoda, sledite ove korake:

1. U levom oknu za navigaciju usluge Project Operations idite na **Prodaja** > **Proizvodi**.
2. Otvorite proizvod za koji treba da konfigurišete faktore količine. Uverite se da proizvod ima svojstva koja su već konfigurisana.
3. Na stranici **Informacije o projektu** za Proizvod, izaberite karticu **Faktori količine**.
4. U podformi izaberite **Novi obračun polja**.
5. Unesite naziv faktora količine i izaberite vrednost svojstva koje se mapira u obračun polja.
6. Sačuvajte i zatvorite obrazac. Ponovite ove korake za sva svojstva koja ćete koristiti za izračunavanje količine za stavku ponude zasnovanu na proizvodu.

Kada za proizvod kreirate stavku ponude zasnovane na proizvodu, količina stavke ponude će biti zaključana. Količina će se izračunati kao proizvod vrednosti svojstva koje ste uneli za tu stavku ponude.
