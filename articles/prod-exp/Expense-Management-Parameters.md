---
title: Parametri upravljanja troškovima
description: Sledeći parametri kontrolišu ponašanje u upravljanju troškovima.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 41d78726f6d0aa6b5e647dbb359824950cb6ca72
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993747"
---
# <a name="expense-management-parameters"></a>Parametri upravljanja troškovima


Sledeći parametri kontrolišu opšte ponašanje u upravljanju troškovima.

### <a name="general"></a>Opšte postavke

| **Polje**                                                | **Opis**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Standardna stopa pređenih kilometara**                             | Unesite stopu naknade za troškove pređenih kilometara. Stopa se množi sa kilometražom koja se unosi za trošak da bi se izračunao iznos koji se nadoknađuje za putni trošak.                       |
|**Lični troškovi koje plaća**                             | Izaberite ko je odgovoran za plaćanje bilo kog iznosa transakcije na kreditnoj kartici koji je kategorisan kao lični.                                                                                                     |
|**Prikažite celokupan izveštaj o troškovima vraćanja**               | Izaberite ovu opciju da biste prikazali sve troškove za izveštaj o troškovima kada se pregledaju detalji originalnog dokumenta za određeni vaučer koji je generisan prilikom knjiženja izveštaja o troškovima.              |
|**Prethodna autorizacija putovanja je obavezna**                 | Izaberite ovu opciju da biste zahtevali da se zahtev za putovanje prosledi i odobri pre nego što zaposleni bude mogao da podnese izveštaj o troškovima.                                                                    |
|**Dozvolite uređivanje distribucija pre knjiženja**            | Izaberite da li se distribucije izveštaja o troškovima mogu uređivati pre knjiženja.                                                                                                                 |
|**Procenite smernice za upravljanje troškovima**                     | Izaberite kada će se troškovi procenjivati da biste utvrdili da li su prekršene smernice za troškove. Kršenje smernica za troškove se može proveriti kada se stavka troška unese i sačuva ili kada se trošak podnese na odobrenje. Pravila smernica za priznanice koje su obavezne proveriće se kada se sačuva stavka troška.                   |
|**Omogućite stavke međukompanijskih troškova**                         | Izaberite da li se dozvoljava unos troškova za druga pravna lica u izveštaj o troškovima.                                                                                                          |
|**Dozvolite uređivanje kursa valuta za troškove kreditne kartice** | Izaberite ovu opciju da biste korisniku dozvolili da uređuje kurs valute za uvezene troškove kreditne kartice.                                                                        |
|**Polja hijerarhije na više nivoa za prikaz**                  | Izaberite koja se polja davaoca odobrenja prikazuju kada je tip dodeljivanja toka posla za izveštaj o troškovima postavljen kao hijerarhija, a izbor Hijerarhija je postavljen tako da koristi hijerarhiju odobrenja, odobrenje troškova na više nivoa. Kada se za radni tok koristi hijerarhija odobrenja na više nivoa, izabrana polja će biti prikazana u izveštaju o troškovima i mogu se uređivati. |
|**Unesite broj kreditne kartice zaposlenog (ažuriranje iz jula 2017)**     | Izaberite da li se može uneti i sačuvati broj od 15 ili 16 znakova u polju **ID kartice** na stranici **Kreditne kartice** za zaposlenog.                                                                          |

### <a name="financial"></a>Finansije

| **Polje**                                                            | **Opis**     |
|----------------------------------------------------------------------|------------------------------------|
|**Naziv dnevnog dnevnika za knjiženje u glavnu knjigu**                                         | Izaberite naziv dnevnika za knjiženje u glavnu knjigu u koji se knjiže odobreni izveštaji o troškovima.            |
|**Omogući povraćaj poreza iz troškova**                                  | Izaberite ovu opciju da biste omogućili povraćaj poreza na troškove za prihvatljive troškove. Ova opcija se ne može omogućiti ako su omogućena američka pravila o porezu na promet i porezu na upotrebu.      |
|**Knjiži akontacije odmah**                                     | Izaberite ovu opciju da biste knjižili odobrenu akontaciju kada se postupak plaćanja i transfera završi. Ako ova opcija nije izabrana, proces plaćanja i prenosa generiše neproknjiženi opšti dnevnik. |
|**Tačan datum obračuna tokom knjiženja**                             | Izaberite ovu opciju da biste ažurirali datum obračuna kada su troškovi proknjiženi, ako je tekući period na čekanju ili je zatvoren. Datum obračuna biće postavljen na sledeći otvoreni period.   |
|**Dozvoli grupisanje transakcija na osnovu računa za prebijanje dugovanja i potraživanja navedenog u načinu plaćanja**      | Izaberite ovu opciju da biste sumirali transakcije troškova za izveštaj o troškovima, na osnovu računa za prebijanje dugovanja i potraživanja koji je naveden u načinu plaćanja troškova.   
|**Porez je uključen**                                                   | Izaberite ovu opciju da biste podrazumevano uključili porez na promet u iznos troškova.             |
|**Oslobodi opterećenja prilikom zatvaranja zahteva za putovanje**            | Izaberite ovu opciju da biste oslobodili opterećena sredstva kada se odobreni zahtev za putovanje zatvori.                                                                                   |
|**Dozvoli predaju zahteva za putovanje pri prekoračenju budžeta za budžetski registar i budžet projekta** | Izaberite ovu opciju da biste zaposlenima omogućili da podnesu zahteve za putovanje na odobrenje koji premašuju ili dozvoljeni budžet koji je postavljen u budžetskom registru ili dozvoljeni budžet za projekat.            |
|**Dozvoli predaju izveštaja o troškovima pri prekoračenju budžeta za budžetski registar i budžet projekta**    | Izaberite ovu opciju da biste zaposlenima omogućili da podnesu izveštaje o troškovima na odobrenje koji premašuju ili dozvoljeni budžet koji je postavljen u budžetskom registru ili dozvoljeni budžet za projekat.                |
|**Dozvoli odobrenje izveštaja o troškovima samo pri prekoračenju budžeta za budžetski registar**                | Izaberite ovu opciju da dozvolite davaocima odobrenja da odobre izveštaje o troškovima koji premašuju dozvoljeni budžet postavljen u registru budžeta.                                                                       |

### <a name="per-diem"></a>Dnevnica

| **Polje**                             | **Opis**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Minimalni broj sati za dnevnicu**           | Unesite podrazumevani minimalni broj sati koje zaposleni mora da radi u jednom danu da bi imao pravo na dnevnicu za putne troškove.  Ova vrednost se koristi kao podrazumevana vrednost samo za polje Minimalni broj sati za nivo dnevnica.                                                                                      |
|**Procenat za obroke**                          | Unesite podrazumevani procenat dnevnice za obroke koji se koristi prvog i poslednjeg dana putnih troškova kada je polje **Izračunajte smanjenje obroka za** postavljeno na bilo **Tip obroka dnevno** ili **Broj obroka dnevno**. Radni dan prvog i poslednjeg dana može biti kraći od uobičajenog radnog dana. Stoga bi se iznos dnevnice tih dana mogao razlikovati od standardnog iznosa. Ako je procenat postavljen na 0 (nula), odbici za prvi i poslednji dan biće 0,00. |
|**Procenat za hotel**                        | Unesite podrazumevani procenat dnevnice za hotele koji se koristi prvog i poslednjeg dana putnih troškova. Radni dan prvog i poslednjeg dana može biti kraći od uobičajenog radnog dana. Stoga bi se iznos dnevnice tih dana mogao razlikovati od standardnog iznosa. Ako je procenat postavljen na 0 (nula), odbici za prvi i poslednji dan biće 0,00.                                              |
|**Ostali procenti**                        | Unesite podrazumevani procenat dnevnice za razne troškove koji se koristi prvog i poslednjeg dana putnih troškova. Radni dan prvog i poslednjeg dana može biti kraći od uobičajenog radnog dana. Stoga bi se iznos dnevnice tih dana mogao razlikovati od standardnog iznosa. Ako je procenat postavljen na 0 (nula), odbici za prvi i poslednji dan biće 0,00.                                                                                                     |
|**Smanjenje procenta za doručak** | Unesite iznos za koji se umanjuje dnevnica za doručak. Na primer, ako zaposleni dobije besplatan doručak, možda treba da smanjite iznos dnevnice za 10 procenata.                               |
|**Smanjenje procenta za ručak**    | Unesite iznos za koji se umanjuje dnevnica za ručak. Na primer, ako zaposleni dobije besplatan ručak, možda treba da smanjite iznos dnevnice za 15 procenata.                                       |
|**Smanjenje procenta za večeru**   | Unesite iznos za koji se umanjuje dnevnica za večeru. Na primer, ako zaposleni dobije besplatnu večeru, možda treba da smanjite iznos dnevnice za 25 procenata.                                     |
|**Izračunajte smanjenje obroka za**         | Izaberite kako sistem treba da izračuna dnevnu redukciju obroka tako što ćete izabrati da li se smanjenje zasniva na vrsti obroka po putovanju, po danu ili na osnovu broja obroka koji je dozvoljen dnevno.|
|**Zaokruživanje dnevnica**                  | Izaberite vrstu zaokruživanja koja se koristi za dnevnice. Ako izaberete normalno zaokruživanje, svi troškovi dnevnica koji imaju iznos od 0,50 zaokružuju se na 1,00, a svi troškovi dnevnica koji imaju iznos manji od 0,50 zaokružuju se na 0,00.                                                                                              |
|**Osnovni obračun dnevnice na**         | Izaberite da li se iznos dnevnice zasniva na kalendarskom danu ili periodu od 24 sata.       |

### <a name="fax-cover-pages"></a>Naslovne stranice faksa

| **Polje**                      | **Opis**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Uputstva**                   | Unesite uputstva koja zaposleni moraju slediti kada kreiraju naslovnu stranicu za faks koji se koristi za slanje računa koji se odnose na izveštaj o troškovima. Kliknite na dugme **Prevodi** da biste uneli tekst specifičan za jezik koji će se prikazivati, na osnovu korisničkog jezika. |
|**ID korisnika (informacije o bar kodu)** | Izaberite ovu opciju da biste čuvali jedinstveni identifikator zaposlenog u bar kodu koji se koristi na naslovnoj stranici faksa.                 |
|**Bar kôd**                      | Izaberite bar kôd koji se koristi na naslovnoj stranici faksa. U upravljanju troškovima podržani su bar kodovi 39 i 128.               |

### <a name="anti-corruption"></a>Borba protiv korupcije

|                 <strong>Polje</strong>                 |                                                                                                                                                                                            <strong>Opis</strong>                                                                                                                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <strong>Prikaz atestiranja o borbi protiv korupcije</strong>  | Izaberite ovu opciju da biste prikazali tekst o borbi protiv korupcije kada se kreira novi izveštaj o troškovima. Tada se mogu omogućiti određene kategorije troškova koje će zahtevati da se u izveštaju o troškovima izabere potvrda o borbi protiv korupcije. Na primer, kategorija poklona koja se odnosi na trošak državnog službenika može zahtevati da zaposleni potvrdi da trošak ispunjava smernice preduzeća koje se odnose na državne službenike. |
| <strong>Poruka o borbi protiv korupcije za podnosioca</strong> |                                                                                             Unesite tekst koji će biti prikazan zaposlenom prilikom kreiranja novog izveštaja o troškovima. Kliknite na dugme <strong>Prevodi</strong> da biste uneli tekst specifičan za jezik koji će se prikazivati, na osnovu korisničkog jezika.                                                                                             |
| <strong>Poruka o borbi protiv korupcije za davaoca odobrenja</strong>  |                                                                                             Unesite tekst koji će biti prikazan davaocu odobrenja prilikom kreiranja novog izveštaja o troškovima. Kliknite na dugme <strong>Prevodi</strong> da biste uneli tekst specifičan za jezik koji će se prikazivati, na osnovu korisničkog jezika.                                                                                             |



[!INCLUDE[footer-include](../includes/footer-banner.md)]