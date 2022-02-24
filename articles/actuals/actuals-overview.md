---
title: Trenutno stanje
description: Ova tema pruža informacije o tome kako se radi sa stvarnim podacima u usluzi Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 304c51a4e502ad6ecec1fd821e98d6604ddd59ba
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852561"
---
# <a name="actuals"></a>Trenutno stanje 

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Trenutno stanje predstavlja pregledani i odobreni finansijski i vremenski raspored projekta. Kreira se kao rezultat odobravanja vremena, troškova, stavki upotrebe materijala, stavki dnevnika i faktura.

## <a name="journal-lines-and-time-submission"></a>Stavke u glavnoj knjizi i vreme predaje

Za više informacija o stavci vremena, pogledajte [Pregled unosa vremena](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Vreme i materijali

Kada je stavka vremena koja je prosleđena povezana sa projektom koji je mapiran u predmet ugovora o vremenu i materijalima, sistem kreira dve stavke u glavnoj knjizi, jednu za troškove i jednu za nenaplaćenu prodaju.

### <a name="fixed-price"></a>Fiksna cena

Kada se prosleđena stavka vremena poveže sa projektom koji se mapiran na predmet ugovora sa fiksnom cenom, sistem kreira jednu stavku u glavnoj knjizi za troškove.

### <a name="default-pricing"></a>Podrazumevano određivanje cena

Logika za kreiranje podrazumevanih cena se nalazi u stavci u glavnoj knjizi. Vrednosti polja iz stavke vremena kopiraju se u stavku u glavnoj knjizi. Ove vrednosti uključuju datum transakcije, predmet ugovora na koji je projekat mapiran i valutu koja je rezultat odgovarajućeg cenovnika.

Polja koja utiču na podrazumevane cene, kao što su **Uloga** i **Jedinica za određivanje resursa**, koriste se za utvrđivanje odgovarajuće cene u stavki u glavnoj knjizi. Na stavku vremena možete dodati prilagođeno polje. Ako želite da se vrednost polja širi na trenutno stanje, kreirajte polje u tabelama **Trenutno stanje** i **Stavka u glavnoj knjizi**. Koristite prilagođeni kôd za širenje izabrane vrednosti polja iz stavku vremena u trenutno stanje putem stavke u glavnoj knjizi koristeći poreklo transakcija. Za više informacija o poreklu transakcija i vezama, pogledajte [Povezivanje trenutnog stanja sa originalnim zapisima](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-basic-expense-submission"></a>Prosleđivanje stavki u glavnoj knjizi i osnovnih troškova

Za više informacija o stavci troška, pogledajte [Pregled troškova](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Vreme i materijali

Kada se stavka osnovnog troška koja je prosleđena poveže sa projektom koji je mapiran u predmet ugovora o vremenu i materijalima, sistem kreira dve stavke u glavnoj knjizi, jednu za troškove i jednu za nenaplaćenu prodaju.

### <a name="fixed-price"></a>Fiksna cena

Kada se prosleđena stavka troška poveže sa projektom koji se mapira na predmet ugovora o fiksnoj ceni, sistem kreira jednu stavku u glavnoj knjizi za troškove.

### <a name="default-pricing"></a>Podrazumevano određivanje cena

Logika unošenja zadatih cena za troškove zasniva se na kategoriji troškova. Datum transakcije, predmet ugovora na koji je projekat mapiran i valuta se koriste za određivanje odgovarajućeg cenovnika. Polja koja utiču na podrazumevane cene, kao što su **Kategorija transakcije** i **Jedinica**, koriste se za utvrđivanje odgovarajuće cene u stavki u glavnoj knjizi. Međutim, to funkcioniše samo kada je metoda određivanja cena u cenovniku **Cena po jedinici**. Ako je metoda određivanja cena **Po ceni** ili **Provizija preko troškova**, cena koja se unosi kada se kreira stavka troškova koristi se kao trošak, a cena stavke u glavnoj knjizi prodaje izračunava se na osnovu metode određivanja cena. 

Na stavku troškova možete dodati prilagođeno polje. Ako želite da se vrednost polja širi na trenutno stanje, kreirajte polje u tabelama **Trenutno stanje** i **Stavka u glavnoj knjizi**. Koristite prilagođeni kôd za širenje izabrane vrednosti polja iz stavku vremena u trenutno stanje putem stavke u glavnoj knjizi koristeći poreklo transakcija. Za više informacija o poreklu transakcija i vezama, pogledajte [Povezivanje trenutnog stanja sa originalnim zapisima](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-material-usage-log-submission"></a>Stavke u glavnoj knjizi i prosleđivanje evidencije upotrebe materijala

Za više informacija o stavci troškova, pogledajte [Dnevnik upotrebe materijala](../material/material-usage-log.md).

### <a name="time-and-materials"></a>Vreme i materijali

Kada se prosleđena stavka evidencije upotrebe materijala poveže sa projektom koji se mapira u predmet ugovora o vremenu i materijalima, sistem kreira dve stavke u glavnoj knjizi, jednu za troškove i jednu za nefakturisanu prodaju.

### <a name="fixed-price"></a>Fiksna cena

Kada se prosleđena stavka evidencije upotrebe materijala poveže sa projektom koji se mapira na predmet ugovora o fiksnoj ceni, sistem kreira jednu stavku u glavnoj knjizi za troškove.

### <a name="default-pricing"></a>Podrazumevano određivanje cena

Logika unošenja zadatih cena materijala zasniva se na kombinaciji proizvoda i jedinice. Datum transakcije, predmet ugovora na koji je projekat mapiran i valuta se koriste za određivanje odgovarajućeg cenovnika. Polja koja utiču na podrazumevane cene, kao što su **ID proizvoda** i **Jedinica**, koriste se za utvrđivanje odgovarajuće cene u stavki u glavnoj knjizi. Međutim, ovo važi samo za kataloške proizvode. Za proizvode koji se dodaju ručno, cena koja se unosi kada se kreira stavka evidencije upotrebe materijala koristi se za troškove i prodajnu cenu u stavkama u glavnoj knjizi. 

Na stavku **Evidencija upotrebe materijala** možete dodati prilagođeno polje. Ako želite da se vrednost polja širi na trenutno stanje, kreirajte polje u tabelama **Trenutno stanje** i **Stavka u glavnoj knjizi**. Koristite prilagođeni kôd za širenje izabrane vrednosti polja iz stavku vremena u trenutno stanje putem stavke u glavnoj knjizi koristeći poreklo transakcija. Za više informacija o poreklu transakcija i vezama, pogledajte [Povezivanje trenutnog stanja sa originalnim zapisima](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="use-entry-journals-to-record-costs"></a>Korišćenje dnevnika za knjiženje za evidentiranje troškova

Možete da koristite dnevnike za knjiženje da evidentirate troškove ili prihod u klasama materijala, naknade, vremena, troškova ili poreskih transakcija. Dnevnici se mogu koristiti u sledeće svrhe:

- Premestite stvarne vrednosti transakcija iz drugog sistema u Microsoft Dynamics 365 Project Operations.
- Evidentirajte troškove koji su se dogodili u drugom sistemu. Ovi troškovi mogu uključivati troškove nabavke ili podugovaranja.

> [!IMPORTANT]
> Aplikacija ne potvrđuje tip stavke u glavnoj knjizi ili povezano određivanje cena koje se unosi u stavku u glavnoj knjizi. Stoga samo korisnik koji je potpuno svestan računovodstvenog uticaja koji stvarne vrednosti imaju na projekat treba da koristi dnevnike za knjiženje za kreiranje stvarnih podataka. Zbog uticaja ovog tipa dnevnika, pažljivo birajte ko ima pristup kreiranju dnevnika za knjiženje.

## <a name="record-actuals-based-on-project-events"></a>Evidentiranje stvarnih vrednosti na osnovu događaja u projektu

Project Operations beleži finansijske transakcije koje se dešavaju tokom projekta. Ove transakcije se evidentiraju kao stvarne vrednosti. Sledeće tabele prikazuju različite vrste stvarnih vrednosti koje se kreiraju, zavisno od toga da li je projekat zasnovan na vremenu i materijalima ili projekat sa fiksnom cenom, da li je u fazi predprodaje ili je interni projekat.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>Resurs pripada istoj organizacionoj jedinici kao i ugovorna jedinica projekta

<table>
<thead>
<tr>
<th rowspan="3">Događaj</th>
<th colspan="4">Projekat koji se može naplatiti ili prodati</th>
<th rowspan="3">Projekat u fazi predprodaje</th>
<th rowspan="3">Interni projekat</th>
</tr>
<tr>
<th colspan="2">Vreme i materijali</th>
<th colspan="2">Fiksna cena</th>
</tr>
<tr>
<th>Stvarne vrednosti</th>
<th>Valuta transakcije</th>
<th>Fiksna cena</th>
<th>Valuta transakcije</th>
</tr>
</thead>
<tbody>
<tr>
<td>Stavka vremena je kreirana.</td>
<td colspan="6">Nema aktivnosti u entitetu Stvarne vrednosti</td>
</tr>
<tr>
<td>Stavka vremena je prosleđena.</td>
<td colspan="6">Nema aktivnosti u entitetu Stvarne vrednosti</td>
</tr>
<tr>
<td rowspan="2">Vreme je odobreno, a tokom odobravanja ne može da se promeni ili poveća broj sati za naplatu.</td>
<td>Stvarna vrednost troškova</td>
<td>Ugovorna valuta jedinice</td>
<td rowspan="2">Stvarna vrednost troškova</td>
<td rowspan="2">Ugovorna valuta jedinice
<td rowspan="2">Stvarna vrednost troškova</td>
<td rowspan="2">Stvarna vrednost troškova</td>
</tr>
<tr>
<td>Nenaplaćene stvarne vrednosti prodaje – Naplativo</td>
<td>Ugovorna valuta za projekat</td>
</tr>
<tr>
<td rowspan="3">Vreme je odobreno, a tokom odobravanja dolazi do smanjenja broj sati za naplatu.</td>
<td>Stvarna vrednost troškova</td>
<td>Ugovorna valuta jedinice</td>
<td rowspan="3">Stvarna vrednost troškova</td>
<td rowspan="3">Ugovorna valuta jedinice</td>
<td rowspan="3">Stvarna vrednost troškova</td>
<td rowspan="3">Stvarna vrednost troškova</td>
</tr>
<tr>
<td>Nenaplaćene stvarne vrednosti prodaje – naplativo za novu količinu</td>
<td>Ugovorna valuta za projekat</td>
</tr>
<tr>
<td>Nenaplaćene stvarne vrednosti prodaje – ne može da se naplati za razliku</td>
<td>Ugovorna valuta za projekat</td>
</tr>
<tr>
<td rowspan="2">Faktura je odobrena, a ne može da se promeni ili poveća broj sati za naplatu.</td>
<td>Storniranje nenaplaćene prodaje</td>
<td>Ugovorna valuta za projekat</td>
<td rowspan="2">Naplaćena prodaja za kontrolnu tačku</td>
<td rowspan="2">Ugovorna valuta za projekat</td>
<td rowspan="2">Nije primenjivo</td>
<td rowspan="2">Nije primenjivo</td>
</tr>
<tr>
<td>Naplaćena prodaja</td>
<td>Ugovorna valuta za projekat</td>
</tr>
<tr>
<td rowspan="3">Faktura je odobrena i dolazi do smanjenja broja sati za naplatu.</td>
<td>Storniranje nenaplaćene prodaje</td>
<td>Ugovorna valuta za projekat</td>
<td rowspan="3">Nije primenjivo</td>
<td rowspan="3">Nije primenjivo</td>
<td rowspan="3">Nije primenjivo</td>
<td rowspan="3">Nije primenjivo</td>
</tr>
<tr>
<td>Naplaćena prodaja – naplativo za novu količinu</td>
<td>Ugovorna valuta za projekat</td>
</tr>
<tr>
<td>Naplaćena prodaja – ne može da se naplati za razliku</td>
<td>Ugovorna valuta za projekat</td>
</tr>
<tr>
<td rowspan="2">Faktura se ispravlja da bi se povećala naplativa količina.</td>
<td>Naplaćena prodaja – Storniranje</td>
<td>Ugovorna valuta za projekat</td>
<td rowspan="5">
<ul>
<li>Storniranje naplaćene prodaje za kontrolnu tačku</li>
<li>Promena statusa kontrolne tačke sa <strong>Fakturirano</strong> na <strong>Spremno za fakturisanje</strong></li>
</ul>
</td>
<td rowspan="5">Ugovorna valuta za projekat</td>
<td rowspan="5">Nije primenjivo</td>
<td rowspan="5">Nije primenjivo</td>
</tr>
<tr>
<td>Naplaćena prodaja</td>
<td>Ugovorna valuta za projekat</td>
</tr>
<tr>
<td rowspan="3">Faktura se ispravlja da bi se smanjila naplativa količina.</td>
<td>Naplaćena prodaja – Storniranje</td>
<td>Ugovorna valuta za projekat</td>
</tr>
<tr>
<td>Naplaćena prodaja za novu količinu</td>
<td>Ugovorna valuta za projekat</td>
</tr>
<tr>
<td>Nenaplaćena prodaja – može da se naplati za razliku</td>
<td>Ugovorna valuta za projekat</td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>Resurs pripada organizacionoj jedinici koja se razlikuje od ugovorne jedinice projekta

<table>
<thead>
<tr>
<th rowspan="3">Događaj</th>
<th colspan="4">Projekat koji se može naplatiti ili prodati</th>
<th rowspan="3">Projekat u fazi predprodaje</th>
<th rowspan="3">Interni projekat</th>
</tr>
<tr>
<th colspan="2">Vreme i materijali</th>
<th colspan="2">Fiksna cena</th>
</tr>
<tr>
<th>Stvarne vrednosti</th>
<th>Valuta transakcije</th>
<th>Fiksna cena</th>
<th>Valuta transakcije</th>
</tr>
</thead>
<tbody>
<tr>
<td>Stavka vremena je kreirana.</td>
<td colspan="6">Nema aktivnosti u entitetu Stvarne vrednosti</td>
</tr>
<tr>
<td>Stavka vremena je prosleđena.</td>
<td colspan="6">Nema aktivnosti u entitetu Stvarne vrednosti</td>
</tr>
<tr>
<td rowspan="4">Vreme je odobreno, a tokom odobravanja ne može da se promeni ili poveća broj sati za naplatu.</td>
<td>Stvarna vrednost troškova</td>
<td>Ugovorna valuta jedinice</td>
<td rowspan="4">Stvarna vrednost troškova</td>
<td rowspan="4">Ugovorna valuta jedinice</td>
<td rowspan="4">Stvarna vrednost troškova</td>
<td rowspan="4">Stvarna vrednost troškova</td>
</tr>
<tr>
<td>Nenaplaćene stvarne vrednosti prodaje – Naplativo</td>
<td>Ugovorna valuta za projekat</td>
</tr>
<tr>
<td>Troškovi jedinice za obezbeđivanje resursa</td>
<td>Valuta jedinice za obezbeđivanje resursa</td>
</tr>
<tr>
<td>Prodaja između organizacija</td>
<td>Ugovorna valuta jedinice</td>
</tr>
<tr>
<td rowspan="5">Vreme je odobreno, a tokom odobravanja dolazi do smanjenja broj sati za naplatu.</td>
<td>Stvarna vrednost troškova</td>
<td>Ugovorna valuta jedinice</td>
<td rowspan="5">Stvarna vrednost troškova</td>
<td rowspan="5">Ugovorna valuta jedinice</td>
<td rowspan="5">Stvarna vrednost troškova</td>
<td rowspan="5">Stvarna vrednost troškova</td>
</tr>
<tr>
<td>Troškovi jedinice za obezbeđivanje resursa</td>
<td>Valuta jedinice za obezbeđivanje resursa</td>
</tr>
<tr>
<td>Prodaja između organizacija</td>
<td>Ugovorna valuta jedinice</td>
</tr>
<tr>
<td>Nenaplaćene stvarne vrednosti prodaje – naplativo za novu količinu</td>
<td>Ugovorna valuta za projekat</td>
</tr>
<tr>
<td>Nenaplaćene stvarne vrednosti prodaje – ne može da se naplati za razliku</td>
<td>Ugovorna valuta za projekat</td>
</tr>
<tr>
<td rowspan="2">Faktura je odobrena, a ne može da se promeni ili poveća broj sati za naplatu.</td>
<td>Storniranje nenaplaćene prodaje</td>
<td>Ugovorna valuta za projekat</td>
<td rowspan="2">Naplaćena prodaja za kontrolnu tačku</td>
<td rowspan="2">Ugovorna valuta za projekat</td>
<td rowspan="2">Nije primenjivo</td>
<td rowspan="2">Nije primenjivo</td>
</tr>
<tr>
<td>Naplaćena prodaja</td>
<td>Ugovorna valuta za projekat</td>
</tr>
<tr>
<td rowspan="3">Faktura je odobrena i dolazi do smanjenja broja sati za naplatu.</td>
<td>Storniranje nenaplaćene prodaje</td>
<td>Ugovorna valuta za projekat</td>
<td rowspan="3">Nije primenjivo</td>
<td rowspan="3">Nije primenjivo</td>
<td rowspan="3">Nije primenjivo</td>
<td rowspan="3">Nije primenjivo</td>
</tr>
<tr>
<td>Naplaćena prodaja – naplativo za novu količinu</td>
<td>Ugovorna valuta za projekat</td>
</tr>
<tr>
<td>Naplaćena prodaja – ne može da se naplati za razliku</td>
<td>Ugovorna valuta za projekat</td>
</tr>
<tr>
<td rowspan="2">Faktura se ispravlja da bi se povećala naplativa količina.</td>
<td>Naplaćena prodaja – Storniranje</td>
<td>Ugovorna valuta za projekat</td>
<td rowspan="5">
<ul>
<li>Storniranje naplaćene prodaje za kontrolnu tačku</li>
<li>Promena statusa kontrolne tačke sa <strong>Fakturirano</strong> na <strong>Spremno za fakturisanje</strong></li>
</ul>
</td>
<td rowspan="5">Ugovorna valuta za projekat</td>
<td rowspan="5">Nije primenjivo</td>
<td rowspan="5">Nije primenjivo</td>
</tr>
<tr>
<td>Naplaćena prodaja</td>
<td>Ugovorna valuta za projekat</td>
</tr>
<tr>
<td rowspan="3">Faktura se ispravlja da bi se smanjila naplativa količina.</td>
<td>Naplaćena prodaja – Storniranje</td>
<td>Ugovorna valuta za projekat</td>
</tr>
<tr>
<td>Naplaćena prodaja za novu količinu</td>
<td>Ugovorna valuta za projekat</td>
</tr>
<tr>
<td>Nenaplaćena prodaja – može da se naplati za razliku</td>
<td>Ugovorna valuta za projekat</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
