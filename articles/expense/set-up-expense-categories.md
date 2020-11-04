---
title: Podešavanje kategorija troškova
description: Ova tema pruža informacije o tome kako da postavite kategorije troškova i deljene kategorije za izveštaje o troškovima.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083470"
---
# <a name="set-up-expense-categories"></a>Podešavanje kategorija troškova

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Kada zaposleni kreiraju izveštaje o troškovima, svaki trošak koji evidentiraju mora biti povezan sa kategorijom troškova. Kategorije troškova su izvedene iz deljenih kategorija koje se mogu deliti između pravnih lica u vašoj organizaciji. U zavisnosti od toga kako je vaša organizacija definisana, ove kategorije troškova mogu se deliti i u drugim oblastima. Na osnovu definicije vaše organizacije i smernica tima za primenu, morate da odredite da li će se kategorije koje se koriste u upravljanju troškovima koristiti samo u upravljanju troškovima ili treba da se dele u drugim oblastima.

> [!NOTE]
> Ove kategorije se mogu deliti između upravljanja projektima i računovodstva i upravljanja troškovima ili između upravljanja projektima i računovodstva i proizvodnje. Međutim, oni ne mogu da se dele između troškova upravljanja i proizvodnje.

Pre nego što započnete postupak podešavanja, za svaku kategoriju troškova moraju se doneti sledeće odluke:

- Šta je to kategorija troškova? Primeri uključuju kategorije za letove, hotele ili kilometražu.
- Može li se kategorija troškova takođe koristiti u upravljanju projektima i računovodstvu? Ako može, morate doneti i sledeće odluke:

    - Koji računi troškova će se koristiti za sledeće troškove?

        - Cena
        - Raspodela zarada
        - Prihodi u toku – vrednost troškova
        - Stavka troškova
        - Prihodi u toku – vrednost troškova – stavka
        - Obračunati gubitak
        - Prihodi u toku – obračunati gubitak

    - Koji računi prihoda će se koristiti za sledeće izvore prihoda?

        - Fakturisani prihod
        - Obračunati prihod – Vrednost prodaje
        - Prihodi u toku – vrednost prodaje
        - Obračunati prihod – proizvodnja
        - Prihodi u toku – proizvodnja
        - Obračunati prihod – dobitak
        - Prihodi u toku – dobitak
        - Obračunati prihod – pretplata
        - Prihodi u toku – pretplata

- Šta je to tip troška?
- Koji je podrazumevani način plaćanja za kategoriju troška?
- Moraju li se detaljno deliti troškovi u kategoriji troškova?
- Koji je glavni podrazumevani račun za kategoriju troška?
- Koja je podrazumevana grupa poreza na promet proizvoda za kategoriju troškova?
- Da li su dozvoljeni dodatni načini plaćanja za kategoriju troškova? Ako jesu, koji su to?
- Postoje li potkategorije u ovoj kategoriji troškova? Ako postoje potkategorije, morate doneti i sledeće odluke:

    - Da li je neka od potkategorija izuzeta od povraćaja poreza?
    - Koja je grupa poreza na promet proizvoda za potkategorije?
