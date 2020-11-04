---
title: Zahtevi za putovanje
description: Ova tema pruža informacije o zahtevima za putovanje.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 0261405abb9305d7f6abcde9cb90d9b184868580
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083449"
---
# <a name="travel-requisitions"></a>Zahtevi za putovanje

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Zahtev za putovanje navodi troškove koji će nastati u svrhu putovanja. Zahtev za putovanje se podnosi na uvid i može se koristiti za odobravanje troškova.

Možda ćete morati da predate zahtev za putovanje pre nego što nastane bilo kakav trošak koji se naplaćuje organizaciji. Ovaj uslov se primenjuje, bez obzira na to da li naplaćujete troškove na kreditnoj kartici preduzeća, trošite gotovinu koju ste dobili kao akontaciju ili ćete plaćati troškove iz svog džepa koje će vam organizacija nadoknaditi.

Zahtevi za putovanje i smernice mogu se koristiti za lakše upravljanje troškovima organizacije. Na primer, ako vaša organizacija radi na projektu sa fiksnom cenom koji zahteva putovanje, putni troškovi članova projektnog tima moraju se uklapati u budžet projekta. Zahtevanjem da se putni troškovi odobre pre nego što nastanu, organizacija može da pomogne da projekat ostane u okviru budžeta.

## <a name="configuration"></a>Konfigurisanje 

Zahtevi za putovanje mogu se konfigurisati kao „obavezni“ omogućavanjem parametra „Prethodno odobrenje putovanja je obavezno“ u parametrima upravljanja troškovima. 

## <a name="create-and-submit-a-travel-requisition"></a>Kreiranje i prosleđivanje zahteva za putovanje

1. Idite na **Moji troškovi: Zahtev za putovanje** i izaberite **Novi zahtev za putovanje**.
2. Unesite svrhu i odredište za zahtev.
3. U polje **Opis putovanja** unesite sve dodatne informacije. 
4. Za svaki od očekivanih troškova, poput leta, obroka ili iznajmljivanja automobila, napravite stavku troška. Uključite procenjeni datum, procenjeni iznos i valutu za svaki trošak. 
5. Kada završite sa dodavanjem očekivanih troškova, izaberite **Sačuvaj**.
6. Kada budete spremni da predate zahtev za putovanje, izaberite **Tok posla** > **Prosledi**.

Odobrene zahteve za putovanje možete pregledati u odeljku **Moji troškovi: Zahtev za putovanje**. 

## <a name="view-available-travel-requisitions"></a>Prikaz dostupnih zahteva za putovanje

Sve svoje zahteve za putovanje možete pregledati u odeljku **Moji troškovi: Zahtevi za putovanje**.

## <a name="approve-travel-requisitions"></a>Odobravanje zahteva za putovanje

Izaberite zahtev za putovanje koji želite da odobrite, a zatim izaberite **Tok posla** > **Odobri**.  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a>Pošaljite izveštaj o troškovima koristeći odobreni zahtev za putovanje

1. Napravite novi izveštaj o troškovima i u zaglavlju izveštaja o troškovima i sa liste odobrenih putnih zahteva izaberite **Mapiraj na zahtev za putovanje**.
2. Polje **Iznos zahteva za putovanje** se automatski ažurira u zaglavlju izveštaja o troškovima.
3. Dodajte svaki trošak nastao tokom putovanja. Ako je polje **Unapred ovlašćeno** omogućeno, usklađeni iznos i odobreni iznos za određenu kategoriju troškova će se ažurirati.

> [!NOTE]
> Kada mapirate izveštaj o troškovima u odobreni zahtev za putovanje, iznos transakcije ne može biti veći od odobrenog iznosa. 
