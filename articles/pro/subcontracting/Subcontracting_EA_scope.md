---
title: Podugovaranje u izdanju za radni pristup iz oktobra 2021.
description: Ova tema pruža pregled mogućnosti podugovaranja u aplikaciji Project Operations koje su deo izdanja za rani pristup iz oktobra 2021.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383712"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>Podugovaranje u izdanju za radni pristup iz oktobra 2021.

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Ova tema pruža pregled mogućnosti podugovaranja u aplikaciji Dynamics 365 Project Operations koje su deo izdanja za rani pristup iz oktobra 2021. Ovaj skup funkcija nije spreman za proizvodna ili okruženja uživo, pa će te funkcije ostati u izdanju za rani pristup sve dok se ne objavi kompletan skup funkcija. Preporučujemo da ne koristite skup funkcija podugovaranja za scenarije proizvodnje uživo sve dok se natpis verzije za pregled ne ukloni. 

Sledeća lista daje pregled onoga što je trenutno dostupno u izdanju ranog pristupa za oktobar 2021. godine:

1. Rukovodilac projekta sklapa podugovor sa dobavljačem. Podrazumevano se cenovnici koji su priloženi evidenciji dobavljača koriste za podugovor. Račun dobavljača ima vrstu odnosa **Dobavljač** ili **Dobavljač**.

2. Rukovodilac projekta može da raščlani sve kupovine i stavi ih kao stavke u podugovoru. Stavke podugovora mogu da budu vezane za vreme, troškove ili proizvode. Klasa transakcije koja je izabrana za predmet podugovora određuje čemu ta stavka služi.

3. Menadžer poslovnog kontakta dobavljača i rukovodilac projekta mogu da ponavljaju podugovor. Cene mogu da se prilagode u cenovnicima za kupovinu koji su priloženi podugovoru.

4. U ovom trenutku ili kasnije u toku procesa, ako se stavka podugovora odnosi na vreme, menadžer poslovnog kontakta dobavljača povezuje kontakte sa svakim predmetom podugovora. Ovo povezivanje pruža informacije rukovodiocu projekta koji radi na podugovoru. Kada je kontakt prodavca povezan sa stavkom podugovora, sistem automatski kreira resurs koji može da se rezerviše od kontakta, ako resurs koji može da se rezerviše već ne postoji.

5. Način naplate na svakoj stavci podugovora može da bude **Fiksna cena** ili **Vreme i materijal**. Za predmete podugovora sa fiksnom cenom podešen je raspored faktura na osnovu kontrolnih tačaka.

Preostali koraci u toku poslovnog procesa za podugovaranje koji su navedeni u pregledu trenutno nisu dostupni. Kako se dodaju nove funkcionalnosti, ova tema će se ažurirati. 

Sledeća ilustracija predstavlja izdanje ranog pristupa za podugovaranje u odnosu na potpunim poslovnim procesom.

![Tok procesa podugovaranja](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>Izdanje za rani pristup predmeta podugovora zasnovanih na količini i predmeta podugovora zasnovanih na poslu
U izdanju za rani pristup iz oktobra 2021, podržani su samo predmeti podugovora zasnovani na količini. To znači da se predmet podugovora može koristiti za kupovinu vremena, troškova ili materijala od prodavca, ali ne i za čitav posao. To takođe znači da se količina koja se kupuje (jedinice vremena, troškovi ili količina materijala) na predmetu podugovora može koristiti za bilo koji projekat u sistemu.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
