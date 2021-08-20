---
title: Proizvodi
description: Ova tema pruža informacije o katalogu proizvoda koji možete koristiti za pružanje informacija kupcima o proizvodima i cenama koje nudi vaša organizacija.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 085b7e4d9274f8c8d94d7a84109cfa782acf3dbb9241bfd25ecb8c2f329e1bb8
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986868"
---
# <a name="products"></a>Proizvodi

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Proizvodi su osnova vašeg posla. Katalog proizvoda u usluzi Dynamics 365 Sales Professional je kolekcija proizvoda i informacija o cenama. Olakšajte predstavnicima prodaje da povećaju svoju prodaju brzim kreiranjem kataloga proizvoda.

## <a name="add-a-product"></a>Dodavanje proizvoda

1.  Uverite se da imate ulogu menadžera za Sales Professional ili administrator sistema da biste mogli da dodajete proizvode u usluzi Dynamics 365 Sales Professional.
2.  Na mapi lokacije, u okviru stavke **Instalacija**, izaberite **Proizvodi**.
3.  Izaberite **Dodaj proizvod** i popunite sledeće podatke:

    -  **Ime**
    -  **ID proizvoda**
    -  **Nadređeno**: Izaberite nadređenu porodicu proizvoda za proizvod. Ako kreirate podređeni proizvod u porodici proizvoda, ime nadređene porodice proizvoda se popunjava ovde. Nakon što zapis bude sačuvan, to nije moguće promeniti.
    -  **Važi od**/**Važi do**: Definišite period tokom kog je proizvod važeći tako što ćete izabrati datume **Važi od** i **Važi do**.
    -  **Grupa jedinica**: Izaberite grupu jedinica. Grupa jedinica je kolekcija različitih jedinica kojima je proizvod prodat i definiše kako su pojedinačne stavke grupisane u veće količine. Na primer, ako dodajete semena kao proizvod, možda ste kreirali grupu jedinica koja se zove „Semena“ i definisali njegovu primarnu jedinicu kao „paket“.
    -  **Podrazumevana jedinica**: Izaberite najčešću jedinicu u kojoj će se proizvod prodavati. Jedinice su količine ili mere u kojima prodajete proizvode. Na primer, ako dodajete semena kao proizvod, možete da ih prodajete u paketima, kutijama ili paletama. Svaki od ovih postaje jedinica proizvoda. Ako se semena uglavnom prodaju u paketima, izaberite ga kao jedinicu.
    -  **Podrazumevani cenovnik**: Ako je ovo novi proizvod, ovo polje je samo za čitanje. Pre nego što možete da izaberete podrazumevani cenovnik, morate da dovršite sva zahtevana polja i zatim da sačuvate zapis. Iako podrazumevani cenovnik nije potreban, nakon što sačuvate zapis o proizvodu, bilo bi dobro da podesite podrazumevani cenovnik za svaki proizvod. Zatim, ako zapis klijenta ne sadrži cenovnik, Sales može da koristi podrazumevani cenovnik za generisanje ponuda, porudžbina i faktura.
    -  **Podržani decimalni brojevi:** Unesite ceo broj između 0 i 5. Ako proizvod ne može biti podeljen u delimične količine, unesite 0. Preciznost polja **Količina** u zapisu proizvoda u ponudi, porudžbini ili fakturi se proverava u odnosu na vrednost u ovom polju ako proizvod nema povezan cenovnik.
    -  **Tema**: Povežite ovaj proizvod sa temom. Teme možete koristiti da biste kategorizovali proizvode i filtrirali izveštaje.

4.  Izaberite stavku **Sačuvaj**.
5.  Na kartici **Dodatni detalji**, u odeljku **Stavke cenovnika** izaberite ikonu **Još komandi**, a zatim izaberite **Dodaj novu stavku cenovnika**.
7.  Na kartici **Dodatni detalji** u odeljku **Relacija proizvoda** izaberite ikonu **Još komandi**, a zatim izaberite **Dodaj novu relaciju proizvoda.**
8.  Na obrascu **Nova relacija proizvoda**, unesite sledeće detalje i na komandnoj traci izaberite **Sačuvaj i zatvori**:

    -   **Povezani proizvod**: Izaberite proizvod koji želite da dodate kao povezani proizvod postojećem zapisu o proizvodu na kome radite.
    -   **Tip relacije prodaje**: Izaberite da li želite da dodate proizvod kao proizvod naprednije verzije, srodni proizvod, pribor ili proizvod za zamenu.
    -   **Smer**: Izaberite da li će odnos između proizvoda biti jednosmeran ili dvosmeran. Kada izaberete jednosmeran, proizvod koji izaberete u okviru **Povezani proizvod** biće prikazan kao preporuka za postojeći proizvod, ali ne i obrnuto.

9.  Na obrascu „Proizvod“ izaberite **Sačuvaj**.

## <a name="import-products"></a>Uvoz proizvoda

Možete da koristite predloške za uvoz da biste uneli masovne podatke o proizvodima u Dynamics 365 Sales.

## <a name="revise-a-product"></a>Korigovanje proizvoda

Održavajte zalihu proizvoda ažurnom brzim korigovanjem svojstava za proizvode po potrebi i ponovnim objavljivanjem informacija kako bi vaši agenti prodaje mogli da vide najnovije promene zaliha.

1.  Uverite se da imate jednu od sledećih bezbednosnih uloga ili ekvivalentnih dozvola: administrator sistema, stručnjak za prilagođavanje sistema, menadžer prodaje, potpredsednik službe prodaje, potpredsednik službe marketinga ili izvršni direktor.
2.  Na mapi lokacije, izaberite **Proizvodi**.
3.  Otvorite aktivni proizvod koji želite da promenite i na komandnoj traci izaberite stavku **Koriguj**.
4.  U dijalogu **Potvrdi korekciju**, izaberite **Potvrdi**. Ovo će promeniti status proizvoda na **U Reviziji**.
5.  Kada završite sa unosom izmena, na komandnoj traci izaberite **Objavi**.

    > [!TIP]
    > Da biste vratili izmene i nastavili sa poslednjom aktivnom verzijom proizvoda, izaberite **Vrati**. Ovo menja status proizvoda nazad u **Aktivno**.

## <a name="clone-a-product"></a>Kloniranje proizvoda 

Kada kreirate nov proizvod, uštedite vreme tako što ćete klonirati postojeći. Time se kreira kopija originalnog zapisa sa svim detaljima osim imena i ID oznake.

1.  Uverite se da imate jednu od sledećih bezbednosnih uloga ili ekvivalentnih dozvola: administrator sistema, stručnjak za prilagođavanje sistema, menadžer prodaje, potpredsednik službe prodaje, potpredsednik službe marketinga ili izvršni direktor.
2.  Na mapi lokacije, izaberite **Proizvodi**.
3.  Izaberite zapis proizvoda koji želite da klonirate, a zatim na komandnoj traci izaberite stavku **Kloniraj**. Pojavljuje se dijalog za potvrdu.
4.  Izaberite **Potvrdi**.

Otvara se nov zapis proizvoda sa istim detaljima kao originalni zapis, osim imena i ID oznake.

## <a name="retire-a-product"></a>Obustavljanje proizvoda 

Ako vaša organizacija više ne prodaje proizvode, povucite ih tako da više ne budu dostupni agentima prodaje.

1.  Vodite računa da imate bezbednosnu ulogu administratora sistema ili menadžera za Sales Professional ili ekvivalentne dozvole.
2.  Na mapi lokacije, izaberite **Proizvodi**.
3.  Otvorite aktivni proizvod koji želite da obustavite i na komandnoj traci izaberite stavku **Obustavi**.
4.  U dijalogu **Potvrdi obustavljanje**, izaberite **Potvrdi**.


## <a name="delete-a-product"></a>Brisanje proizvoda

Da biste prekinuli prodaju proizvoda, izbrišite ga.

> [!IMPORTANT]
> Ne možete da povratite izbrisani zapis.

1.  Vodite računa da imate bezbednosnu ulogu administratora sistema ili menadžera za Sales Professional ili ekvivalentne dozvole.
2.  Na mapi lokacije, izaberite **Proizvodi**.
3.  Izaberite zapis proizvoda koji želite da izbrišete, a zatim na komandnoj traci izaberite stavku **Izbriši**.
4.  U okviru dijaloga **Potvrda brisanja**, izaberite stavku **Nastavi**.
 
 ## <a name="quantity-factors-for-products"></a>Količinski faktori proizvoda

Količinski faktori podržavaju prodaju proizvoda zasnovanih na pretplati. Za proizvode zasnovane na pretplati, količina u stavci ponude ili predmetu ugovora o projektu izražena je kao broj korisničkih meseci.

Obično se cena softvera za pretplatu čuva u katalogu kao cena po korisniku mesečno. Međutim, umesto toga možete koristiti opise drugih perioda. Tokom procesa prodaje, cena u stavci ponude je obično cena po korisniku, mesečno, do koje se došlo pregovorima i popustima od strane IT agenta prodaje. Svaka pogodba ima različit broj korisnika i različit broj meseci pretplate. Količina koja se koristi za izračunavanje količine stavke ponude je proizvod broja korisnika i broja meseci pretplate.

Količinski faktori se oslanjaju na atribute proizvoda. Kada konfigurišete određene osobine proizvoda, možete da označite podskup tih svojstava ili sva svojstva kao faktore količine.

Sistem potvrđuje da se kao faktori količine označavaju samo numerička svojstva ili svojstva proizvoda koja imaju numerički tip podataka. Kada se proizvod za koji su konfigurisani faktori količine doda u stavku ponude, polje **Količina** u stavci ponude postaje polje samo za čitanje. Nakon što unesete vrednosti za svojstva proizvoda koja su količinski faktori, izračunava se količina stavke ponude.

Na primer, ako postoje sledeća svojstva: 

- **Br. korisnika**: broj korisnika 
- **Br. meseca**: broj meseci pretplate
- **SKU proizvoda** 

Svojstva **Br. korisnika** i **Br. meseci** se mogu označiti kao faktori količine, uređivanjem svojstava u stavci proizvoda. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]