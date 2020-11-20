---
title: Gotovinski avans
description: Ova tema pruža informacije o akontacijama.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c5839fbdab58903555936324139b76f4c94b6c35
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122766"
---
# <a name="cash-advance"></a>Gotovinski avans

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Akontacija omogućava zaposlenima da pozajmljuju novac od svog preduzeća pre nego što nastanu bilo kakvi troškovi. Kada se odobri i plati tražena akontacija, zaposleni može novac iskoristiti za poslovne troškove koji će možda nastati. 

## <a name="create-and-submit-a-cash-advance-request"></a>Kreirajte i predajte zahtev za akontaciju

1. U delu **Moji troškovi** izaberite **Akontacije** > **Nova** da biste kreirali novu akontaciju. 
2. Na stranici **Novi zahtev za akontaciju**, unesite namenu troškova i odaberite lokaciju na kojoj će nastati troškovi.
3. Unesite traženi iznos i valutu, a zatim izaberite **Sačuvaj**. 
4. Kada budete spremni da predate zahtev za akontaciju, na stranici **Zahtev za akontaciju** izaberite **Tok posla** > **Prosledi**.

## <a name="modify-a-cash-advance-request"></a>Izmena zahteva za akontaciju

Zahtev za akontaciju možete izmeniti ako nije podnet na odobrenje.

1. U delu **Moji troškovi: Akontacije** pronađite i izaberite akontaciju koju želite da uredite.
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

Kada kreirate i predate izveštaj o troškovima za akontaciju koju ste već dobili, troškovi će se automatski prilagoditi toj akontaciji. Ako je vaša akontacija veća od utrošenog iznosa, morate vratiti razliku preduzeću koristeći kategoriju troška **Povraćaj gotovine**. Ako je akontacija koju je preduzeće isplatilo manja od iznosa koji ste potrošili, preduzeće vam mora nadoknaditi razliku. 

### <a name="example"></a>Primer
Planirate da putujete na konferenciju iz Sijetla u Njujork. Kreirate zahtev za akontaciju za iznos od 3000 USD jer ste procenili da troškovi kotizacije, letova, hotela, obroka i taksija iznose približno toliko. Nećete biti isplaćeni ukoliko vaš menadžer ne odobri ovaj zahtev. Kada vaš menadžer odobri, tražena akontacija u iznosu od 3000 USD se uplaćuje na vaš bankovni račun. Zatim prisustvujete konferenciji. Po završetku putovanja, otkrivate da su ukupni izdaci bili samo 2790 USD. Izaberite **Gotovina** u polju **Način plaćanja** i prosledite vaš trošak na 2790 USD. Prosleđeni iznos troška automatski se prilagođava akontaciji od 3000 USD koja vam je pozajmljena. Sada preduzeću dugujete preduzeću 210 USD (3000 – 2790), koji preduzeću možete vratiti koristeći kategoriju troška **Povraćaj gotovine**. 
