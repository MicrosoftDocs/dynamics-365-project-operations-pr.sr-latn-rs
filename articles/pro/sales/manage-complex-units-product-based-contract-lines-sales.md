---
title: Upravljanje složenim jedinicama za predmete ugovora zasnovane na proizvodima – jednostavno
description: Ova tema pruža informacije o podršci prodaji proizvoda zasnovanih na pretplati.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6bd4e11bf96d9f7d77c77fe081fde02b421c3139915150480a8d1a4d812887f6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003383"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Upravljanje složenim jedinicama za predmete ugovora zasnovane na proizvodima – jednostavno

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Dynamics 365 Project Operations koristi količinske faktore da podrži prodaju proizvoda zasnovanih na pretplati. Za proizvode zasnovane na pretplati, količina ugovoru ili predmetu ugovora o projektu izražena je kao broj korisničkih meseci.

Cena softvera za pretplatu se čuva u katalogu kao cena po korisniku mesečno. Tokom procesa prodaje, cena u predmetu ugovora je obično cena po korisniku mesečno, do koje se došlo pregovorima i popustima od strane agenta prodaje. Svaka pogodba ima različit broj korisnika i različit broj meseci pretplate. Količina koja se koristi za izračunavanje iznosa predmeta ugovora je proizvod broja korisnika i broja meseci pretplate.

Da bi podržao ovu vrstu prodaje, Project Operations podržava koncept *faktora količine*. Količinski faktori se oslanjaju na atribute proizvoda. Kada konfigurišete određene osobine proizvoda, možete da označite podskup tih svojstava ili sva svojstva kao faktore količine.

Project Operations potvrđuje da se kao faktori količine označavaju samo numerička svojstva ili svojstva proizvoda koja imaju numerički tip podataka. Kada se proizvod sa konfigurisanim faktorima količine doda predmetu ugovora, polje **Količina** postaje samo za čitanje. Kada unesete vrednosti za svojstva proizvoda koja su količinski faktori, Project Operations izračunava količinu predmeta ugovora.

Na primer, Dynamics 365 Sales može imati sledeća svojstva:

- **Br. korisnika**: broj korisnika.
- **Br. meseci**: broj meseci pretplate.
- **SKU proizvoda**: Jedinica za čuvanje zaliha (SKU) za proizvod.

Svojstva **Br. korisnika** i **Br. meseci** se mogu označiti kao faktori količine, uređivanjem svojstava u stavci proizvoda.

Da biste kreirali faktore količine iz svojstava proizvoda, obavite sledeće korake.

1. U usluzi **Project Operations** izaberite **Prodaja-proizvodi**.
2. Otvorite proizvod za koji treba da podesite faktore količine. Uverite se da proizvod ima svojstva koja su već podešena.
3. Na stranici **Informacije o projektu** izaberite karticu **Faktori količine**.
4. U podformi izaberite **Novi obračun polja**.
5. Unesite naziv **faktora količine** i izaberite vrednost svojstva koje se mapira u obračun polja.
6. Sačuvajte i zatvorite obrazac.
7. Ponovite korake 2–6 za sva svojstva koja će zajedno činiti količinu za predmet ugovora zasnovan na proizvodu.

Kada se postave faktori količine, kada korisnik kreira predmet ugovora za ovaj proizvod, količina predmeta ugovora se zaključava. Količina se zatim izračunava kao proizvod vrednosti svojstva za taj predmet ugovora.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]