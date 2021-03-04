---
title: Gotovinski avans
description: Ova tema pruža informacije o akontacijama.
author: suvaidya
manager: AnnBe
ms.date: 02/01/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 58864790720824cecad8ce1ff7ff0a335a42cc03
ms.sourcegitcommit: 7aa0b7fb22213d8baa2d69efece9a636d9f62493
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/01/2021
ms.locfileid: "5098901"
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

### <a name="example"></a>Primer
Planirate da putujete iz Sijetla u Njujork na konferenciju. Kreirate zahtev za gotovinski avans za 3000,00 USD na osnovu procenjene cene konferencijske karte, letova, hotela, obroka i taksija. Neće vam biti plaćeno ako menadžer ne odobri ovaj zahtev. Kada vaš menadžer odobri, tražena akontacija u iznosu od 3000 USD se uplaćuje na vaš bankovni račun. Zatim prisustvujete konferenciji. Po završetku putovanja, otkrivate da su ukupni izdaci bili samo 2790 USD. Izaberite **Gotovina** u polju **Način plaćanja** i predajte troškove za 2790,00 USD. Prosleđeni iznos troška automatski se prilagođava akontaciji od 3000 USD koja vam je pozajmljena. Sada dugujete iznos od 210,00 USD (3000,00 – 2790,00) koji možete vratiti kompaniji koristeći kategoriju troškova **Povraćaj gotovine**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]