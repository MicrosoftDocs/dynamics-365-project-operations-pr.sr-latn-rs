---
title: Konfigurisanje upravljanja troškovima
description: Ovaj članak opisuje razmatranja i odluke koje morate doneti tokom procesa planiranja pre nego što konfigurišete upravljanje troškovima u usluzi Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db3529597c662a326730cf6a0b855ae865f0dce5
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960354"
---
# <a name="configure-expense-management"></a>Konfigurisanje upravljanja troškovima

Ova tema opisuje razmatranja i odluke koje morate doneti tokom procesa planiranja pre nego što konfigurišete upravljanje troškovima. U upravljanju troškovima možete da čuvate informacije o načinima plaćanja, putnim zahtevima, izveštajima o troškovima, smernicama itd.

Budući da se mnoge odluke koje donosite kada planirate konfiguraciju za upravljanje troškovima zasnivaju na hijerarhiji i finansijskoj strukturi vaše organizacije, morate pogledati dokumente za planiranje za ta područja.

## <a name="intercompany-expenses"></a>Međukompanijski troškovi

Kada omogućite međukompanijske troškove, dozvoljavate pravnim licima i zaposlenima da prave troškove u ime drugog pravnog lica i prikupljaju uplate od pravnog lica zaposlenog u vašoj organizaciji. Na primer, zaposleni u pravnom licu A završava projekat za pravno lice B, a projekat obuhvata putne troškove. Ako su omogućeni međukompanijski troškovi, zaposleni tada može podneti izveštaj o troškovima koji će trošak knjižiti pravnom licu B, a trošak tada mora platiti pravno lice A. Ako vaša organizacija nema više pravnih lica, ne morate da omogućite međukompanijske troškove.

**Odluka:** Da li želite da omogućite međukompanijske troškove?

## <a name="financial-management"></a>Finansijski menadžment

Upravljanje troškovima je usko integrisano sa finansijskim upravljanjem vaše organizacije. Veliki deo vaše konfiguracije za upravljanje troškovima zasnivaće se na odlukama koje ste doneli o finansijama organizacije. Sledeći odeljci opisuju različita područja koja zahtevaju planiranje i donošenje odluka, na osnovu finansijskih odluka vaše organizacije i smernica vašeg rukovodećeg tima.

### <a name="per-diems"></a>Dnevnice

Morate definisati dnevnice za zaposlene koje pruža vaša organizacija. Budući da se dnevnice obično koriste za pokrivanje troškova kao što su obroci, smeštaj i drugi slučajni troškovi, možete kreirati pravila za dnevnice koje vaša organizacija nudi. Iznosi dnevnica mogu se zasnivati na dobu godine, lokaciji putovanja ili oboje. Kada definišete pravilo za dnevnicu, možete da odredite da se procenat dnevnice zadržava ako radnik dobije besplatne obroke ili usluge. Takođe možete da definišete nivoe dnevnica da biste odredili minimalni i maksimalni broj sati za koji dnevnica može da se primenjuje na putovanje radnika.

**Odluke:**

- Podrazumevana pravila za dnevnice za prvi i poslednji dan:

    - Koji je minimalan broj sati koje zaposleni može tražiti jedan dan, a da i dalje dobije dnevnicu?
    - Da li postoji smanjenje količine koja se nudi za obroke prvog i poslednjeg dana? Ako postoji smanjenje, koliki je procenat smanjenja?
    - Da li postoji smanjenje količine koja se nudi za hotel prvog i poslednjeg dana? Ako postoji smanjenje, koliki je procenat smanjenja?
    - Da li postoji smanjenje količine koja se nudi za druge troškove do kojih dođe prvog i poslednjeg dana? Ako postoji smanjenje, koliki je procenat smanjenja?

- Podrazumevana pravila za dnevnice:

    - Da li postoji procentualno smanjenje dnevnice za svaki obrok ako je, na primer, obrok besplatan? Ako postoji smanjenje, koliki je procenat smanjenja za svaki obrok?
    - Da li se smanjenje obroka izračunava dnevno, po putovanju ili po broju obroka dnevno?
    - Da li iznose dnevnica treba redovno zaokruživati ili zaokruživati nagore?
    - Da li se dnevnice obračunavaju na 24-časovni period ili na kalendarski dan?

- Pravila za dnevnice zasnovana na lokaciji:

    - Da li se dnevnice razlikuju u zavisnosti od lokacije? Koje su lokacije uključene?
    - Ako se dnevnice razlikuju u zavisnosti od lokacije, za svaku lokaciju, koliki procenat se predviđa za sledeće vrste troškova:

        - Obroci
        - Hotel
        - Ostali troškovi

### <a name="expense-management-journals-and-accounts"></a>Dnevnici i računi za upravljanje troškovima

Upravljanje troškovima zahteva upotrebu više dnevnika i računa. Morate da odlučite, na primer, da li se isti račun koristi za akontacije i sporove o kreditnim karticama.

**Odluke:**

- U kojem se dnevniku za knjiženje objavljuju odobreni izveštaji o troškovima?
- Koji račun se koristi za akontacije?
- Da li treba odmah knjižiti akontacije?

### <a name="payment-methods"></a>Načini plaćanja

Kada dozvoljavate zaposlenima da prave troškove u ime vašeg preduzeća, morate da definišete načine plaćanja koje zaposleni smeju da koriste. Na primer, zaposlenima možete dozvoliti da koriste gotovinu ili korporativnu kreditnu karticu. Takođe možete dozvoliti zaposlenima da koriste lične kreditne kartice, a zatim zaposlenima nadoknaditi novac. Morate doneti sledeće odluke za svaki način plaćanja koji dozvoljavate.

**Odluke:**

- Koji su načini plaćanja dozvoljeni?
- Ko je vlasnik troškova plaćanja?
- Da li postoji tip računa za prebijanje dugovanja? Ako postoji tip računa za prebijanje dugovanja, šta je to?
- Ako postoji tip računa za prebijanje dugovanja, koji je to račun?
- Ako je način plaćanja kreditna kartica, da li bi način plaćanja trebalo koristiti samo kod uvezenih transakcija?

### <a name="expense-categories-and-shared-categories"></a>Kategorije troškova i deljene kategorije

Kada zaposleni kreiraju izveštaj o troškovima, svaki trošak koji evidentiraju mora biti povezan sa kategorijom troškova. Kategorije troškova su izvedene iz deljenih kategorija koje se mogu deliti između pravnih lica u vašoj organizaciji. Ove kategorije se takođe mogu deliti u upravljanju projektima i računovodstvu, u zavisnosti od načina na koji je vaša organizacija definisana. Na osnovu definicije vaše organizacije i smernica tima za primenu, morate da odredite da li će se kategorije koje se koriste u upravljanju troškovima koristiti samo u upravljanju troškovima ili treba da se dele između upravljanja projektima i računovodstva i upravljanja troškovima. Imajte na umu da se ove kategorije se mogu deliti između upravljanja projektima i troškova ili upravljanja projektima i proizvodnje, ali ne između upravljanja troškovima i proizvodnje. Za svaku kategoriju troškova morate doneti sledeće odluke.

**Odluke:**

- Šta je to kategorija troškova? Primeri uključuju kategorije za letove, hotele ili kilometražu.
- Može li se kategorija troškova takođe koristiti u upravljanju projektima i računovodstvu?
- Šta je to tip troška?
- Koji je podrazumevani način plaćanja za kategoriju troška?
- Moraju li se detaljno deliti troškovi u kategoriji troškova?
- Koji je glavni podrazumevani račun za kategoriju troška?
- Koja je podrazumevana grupa poreza na promet proizvoda za kategoriju troškova?
- Da li su dozvoljeni dodatni načini plaćanja za kategoriju troškova? Ako su dozvoljeni dodatni načini plaćanja, koji su to?
- Postoje li potkategorije u ovoj kategoriji troškova? Ako postoje potkategorije, morate doneti i sledeće odluke:

    - Da li je neka od potkategorija izuzeta od povraćaja poreza?
    - Koja je grupa poreza na promet proizvoda za potkategorije?

Ako se kategorija troškova koristi i u upravljanju projektima i računovodstvu, odgovorite na preostala pitanja. U suprotnom, pređite na sledeći odeljak.

- Koji računi troškova će se koristiti za sledeće troškove?

    - Cena
    - Raspodela zarada
    - Prihodi u toku – vrednost troškova
    - Stavka troškova
    - Prihodi u toku – vrednost troškova – stavka
    - Obračunati gubitak
    - Prihodi u toku – obračunati gubitak

- Koji računi prihoda će se koristiti za sledeće?

    - Fakturisani prihod
    - Obračunati prihod – Vrednost prodaje
    - Prihodi u toku – vrednost prodaje
    - Obračunati prihod – proizvodnja
    - Prihodi u toku – proizvodnja
    - Obračunati prihod – dobitak
    - Prihodi u toku – dobitak
    - Obračunati prihod – pretplata
    - Prihodi u toku – pretplata

### <a name="taxes"></a>Porezi

Za poreze povezane sa troškovima morate utvrditi šta je uključeno ili omogućeno u izveštajima o troškovima.

**Odluke:**

- Da li je porez na promet uključen u iznose troškova?
- Da li treba omogućiti povrat poreza na troškove?

    > [!NOTE]
    > Kada ste planirali glavnu knjigu, ako ste odlučili da primenite američki porez na promet i koristite poreska pravila, ne možete da omogućite povraćaj poreza na troškove. (Da biste primenili američki porez na promet i koristili poreska pravila, postavite opciju **Primeni pravila oporezivanja za porez na promet** na **Da**.)

## <a name="policies"></a>smernice/a

Kreiranjem smernica za izveštavanje o troškovima možete da pomognete svojoj organizaciji da uštedi vreme i novac kada zaposleni naprave troškove u njeno ime. Pravila pomažu da zaposleni ostanu u okviru budžeta, pruže sve potrebne informacije i troše novac samo onako kako im je potrebno. Morate doneti sledeće odluke za svake smernice za izveštavanje o troškovima i svake smernice za odobravanje izveštaja o troškovima koju kreirate.

**Odluke:**

- Kako se zovu smernice?
- Čemu služe smernice o troškovima?
- Ako ste prethodno odlučili da omogućite međukompanijske troškove, na koje kompanije u vašoj organizaciji će se primenjivati ove smernice?
- Kada smernice stupaju na snagu?
- Kada smernice ističu?
- Kakvo je pravilo smernica?
- Kakav je ishod pravila smernica?
