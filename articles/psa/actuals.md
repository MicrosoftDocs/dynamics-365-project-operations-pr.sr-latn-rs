---
title: Pregled trenutnog stanja
description: Ova tema pruža informacije o stvarnim vrednostima projekta.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 15c8d26fcf4eb9fda8a4fe4ce085ea3becdc2c76f11525357b75f59e18fd6017
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992493"
---
# <a name="actuals-overview"></a>Pregled trenutnog stanja

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Stvarne vrednosti predstavljaju količinu posla koja je završena za projekat. Stvarne vrednosti projekta mogu da se prate do njegovih izvornih dokumenata. Ti izvorni dokumenti uključuju vreme, troškove i stavke knjiženja u glavnoj knjizi, kao i fakture.

![Kako se stvarne vrednosti projekta prate do izvornih dokumenata.](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>Prosleđivanje stavke vremena

Kod aplikacije PSA, kada se stavka vremena prosledi za projekat koji je mapiran na predmet ugovora o vremenu i materijalima, kreiraju se dve stavke u glavnoj knjizi. Jedna stavka je za troškove, a druga za nefakturisane prodaje. Kada se stavka vremena prosledi za projekat koji je mapiran na predmet ugovora o fiksnoj ceni, kreira se stavka u glavnoj knjizi samo za troškove. 

Logiku za unos podrazumevanih cena možete da pronađete u stavki u glavnoj knjizi. Sve vrednosti polja iz stavke vremena kopiraju se u stavku u glavnoj knjizi. Ova polja uključuju datum transakcije, predmet ugovora na koji je projekat mapiran i valutu koja je rezultat odgovarajućeg cenovnika. 

Polja koja utiču na podrazumevane cene, kao što su **Uloga** i **Organizaciona jedinica** prouzrokuju podrazumevani unos odgovarajuće cene u stavku u glavnoj knjizi. Ako u stavku vremena dodate prilagođeno polje, a želite da se vrednost polja širi na stvarne vrednosti, kreirajte polje u entitetu Stvarne vrednosti i upotrebite preslikavanja polja da biste kopirali polje iz stavke vremena u stvarnu vrednost.

## <a name="submitting-an-expense-entry"></a>Prosleđivanje stavke troška

Kod aplikacije PSA, kada se stavka troška prosledi za projekat koji je mapiran na predmet ugovora o vremenu i materijalima, kreiraju se dve stavke u glavnoj knjizi. Jedna stavka je za troškove, a druga za nefakturisane prodaje. Kada se stavka troška prosledi za projekat koji je mapiran na predmet ugovora o fiksnoj ceni, kreira se stavka u glavnoj knjizi samo za troškove.

Logika za unos podrazumevanih cena za troškove temelji se na kategoriji troškova koja je izabrana na stranici **Stavka troškova**. Datum transakcije, predmet ugovora na koji je projekat mapiran i valuta se koriste za određivanje odgovarajućeg cenovnika. Međutim, za samu cenu, iznos koji je korisnik uneo podrazumevano se podešava direktno na povezanim stavkama troškova u glavnoj knjizi za troškove i prodaju.

U trenutnoj verziji aplikacije PSA, nije dostupna stavka zasnovana na kategoriji podrazumevanih cena po jedinici za stavke troškova.

## <a name="using-entry-journals-to-record-costs"></a>Korišćenje ulaznih glavnih knjiga za evidentiranje troškova

U aplikaciji PSA, ulazne glavne knjige vam omogućavaju da evidentirate troškove ili prihod u klasama materijala, naknade, vremena, troškova ili poreskih transakcija. Glavna knjiga ima zaglavlje, stavke i radnju **Potvrdi**. Evo nekoliko scenarija gde možete da koristite glavnu knjigu:

- Morate zabeležiti stvarne troškove i prodaju materijala na projektu.
- Morate premestiti stvarne vrednosti transakcija iz drugog sistema u PSA.
- Morate da evidentirate troškove ostvarene u drugom sistemu, kao što su troškovi nabavke ili podugovaranja.

> [!IMPORTANT]
> Korišćenje ulaznih glavnih knjiga za kreiranje stvarnih podataka treba da radi samo korisnik koji je u potpunosti svestan računovodstvenog uticaja koji stvarni ljudi imaju na projekat. To je zato što aplikacija ne potvrđuje valjanost tipa stavke u glavnoj knjizi ili srodnu cenu koja se unosi u stavku u glavnoj knjizi. Zbog uticaja ovog tipa glavne knjige, budite oprezni po pitanju kome je omogućen pristup kreiranja ulaznih glavnih knjiga.     


## <a name="recording-actuals-based-on-project-events"></a>Evidentiranje stvarnih vrednosti na osnovu događaja u projektu

PSA beleži finansijske transakcije koje se dešavaju tokom projekta. Ove transakcije se evidentiraju kao **stvarne vrednosti**. Sledeće tabele prikazuju različite vrste stvarnih vrednosti koje se kreiraju, zavisno od toga da li je projekat zasnovan na vremenu i materijalima ili projekat sa fiksnom cenom, da li je u fazi predprodaje ili je interni projekat.

**Resurs pripada istoj organizacionoj jedinici kao i ugovorna jedinica projekta**

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

**Resurs pripada organizacionoj jedinici koja se razlikuje od ugovorne jedinice projekta**

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