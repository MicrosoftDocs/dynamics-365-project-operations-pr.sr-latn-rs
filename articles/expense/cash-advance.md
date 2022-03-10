---
title: Gotovinski avans
description: Ova tema pruža informacije o akontacijama.
author: suvaidya
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6881fc8251a2d3c7d6af0016780a92358ce63397d09b9a0cde201126cd2912cc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988533"
---
# <a name="cash-advance"></a>Gotovinski avans

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Akontacija omogućava zaposlenima da pozajmljuju novac od svog preduzeća pre nego što nastanu bilo kakvi troškovi. Kada se odobri i plati tražena akontacija, zaposleni može novac iskoristiti za poslovne troškove koji će možda nastati. 

## <a name="create-and-submit-a-cash-advance-request"></a>Kreirajte i predajte zahtev za akontaciju
Da biste kreirali novi gotovinski avans i podneli zahtev za gotovinski avans, uradite sledeće: 

1. U delu **Moji troškovi** izaberite **Gotovinski avansi** > **Novo**. 
2. Na stranici **Novi zahtev za akontaciju**, unesite namenu troškova i odaberite lokaciju na kojoj će nastati troškovi.
3. Unesite traženi iznos i valutu, a zatim izaberite **Sačuvaj**. 
4. Kada budete spremni da predate zahtev za akontaciju, na stranici **Zahtev za akontaciju** izaberite **Tok posla** > **Prosledi**.

## <a name="modify-a-cash-advance-request"></a>Izmena zahteva za akontaciju

Zahtev za akontaciju možete izmeniti ako nije podnet na odobrenje.

1. U delu **Moji troškovi: gotovinski avansi** pronađite i izaberite gotovinski avans koji želite da uredite.
2. Izaberite **Uređuj** i izvršite potrebne promene u zahtevu za akontaciju. 
3. Izaberite stavku **Sačuvaj i zatvori**.


## <a name="view-cash-advance-requests"></a>Prikaz zahteva za akontaciju
Listu svih akontacija koje su u radnoj verziji, prosleđene, u pregledu ili isplaćene možete pregledati u delu **Moji troškovi: Akontacije**. 

## <a name="approve-cash-advance-requests"></a>Odobravanje zahteva za akontaciju

Menadžeri ili korisnici konfigurisani kao davaoci odobrenja u toku posla moći će da odobre akontacije koje su im dostavljene na pregled. 

1. Da biste odobrili akontaciju, u delu **Obrada akontacija** izaberite **Akontacije za moj pregled**.
2. Izaberite akontaciju koju treba da pregledate i izaberite **Odobri**.  

## <a name="pay-cash-advances"></a>Isplata akontacija 
Sledeći postupak obično dovršava računovođa ili korisnik sa računovodstvenim dozvolama.

1. Da biste proknjižili odobrene akontacije, izaberite **Odobrene akontacije**, a zatim izaberite **Plati i prebaci**.  
2. Navedite detalje dnevnika za knjiženje za akontacije, a zatim izaberite **U redu**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Podnesite izveštaj o troškovima u odnosu na isplaćenu akontaciju 

Kada kreirate i podnesete izveštaj o troškovima za gotovinski avans koji ste već dobili, troškovi će se automatski prilagoditi tom avansu. Ako je vaša akontacija veća od utrošenog iznosa, morate vratiti razliku preduzeću koristeći kategoriju troška **Povraćaj gotovine**. Ako je gotovinski avans koji je preduzeće platilo manji od iznosa koji ste potrošili, preduzeće vam mora nadoknaditi bilans. 

### <a name="select-cash-advances-that-apply-to-your-expenses"></a>Izaberite avans u gotovini koji se odnosi na vaše troškove
Pre nego što predate izveštaj o troškovima, možete da izaberete avans u gotovini koji se poklapa sa transakcijama troškova u izveštaju. Da biste koristili ovu funkcionalnost, sledeće dve funkcije moraju biti omogućene iz radnog prostora **Upravljanje funkcijama**:

  - Ponovno osmišljeni izveštaji o troškovima
  - Sposobnost mapiranja gotovinskih avansa u stavke troškova
 
 Kada su ove funkcije omogućene:
 
  - Možete platiti jedan ili više gotovinskih avansa za svaku stavku troška.
  - Dostupno stanje gotovinskog avansa vidljivo je u realnom vremenu kada se sačuva izveštaj o troškovima. Ovo vam omogućava istovremeno obrađivanje transakcija troškova i vraćanje gotovinskih transakcija.
  - Možete izabrati više gotovinskih avansa za jednu transakciju troška.
  - Podaci o sravnjenju gotovinskog avansa dostupni su pomoću upita. 
 
Ako ne koristite ove funkcije, funkcionalnost će ostati ista, sa postojećim gotovinskim avansima automatski se smanjuju nakon podnošenja troškova.

### <a name="example"></a>Primer 
Planirate da putujete iz Sijetla u Njujork na konferenciju. Kreirate zahtev za gotovinski avans za 3000,00 USD na osnovu procenjene cene konferencijske karte, letova, hotela, obroka i taksija. Neće vam biti plaćeno ako menadžer ne odobri ovaj zahtev. Kada vaš menadžer odobri, tražena akontacija u iznosu od 3000 USD se uplaćuje na vaš bankovni račun. Zatim prisustvujete konferenciji. Po završetku putovanja, otkrivate da su ukupni izdaci bili samo 2790 USD. Izaberite **Gotovina** u polju **Način plaćanja** i predajte troškove za 2790,00 USD. Prosleđeni iznos troška automatski se prilagođava akontaciji od 3000 USD koja vam je pozajmljena. Sada dugujete iznos od 210,00 USD (3000,00 – 2790,00) koji možete vratiti kompaniji koristeći kategoriju troškova **Povraćaj gotovine**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
