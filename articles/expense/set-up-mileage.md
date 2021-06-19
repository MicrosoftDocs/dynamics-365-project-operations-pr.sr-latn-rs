---
title: Podešavanje kilometraže pomoću nivoa kilometraže
description: Ova tema pruža informacije o kilometraži i nivoima kilometraže.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: a44d32358a9e88824efc5452b2b5493ac8b97c7f
ms.sourcegitcommit: 18f99fbceccadd4b3e75875e1c5bcdd3e59ce206
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/20/2021
ms.locfileid: "6083688"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a>Podešavanje kilometraže pomoću nivoa kilometraže

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Kada se prijavi trošak, a odabrana kategorija rashoda je **Kilometraža**, iznos za tu stavku troškova izračunava se prema iznosu *stopa po kilometraži*. Ovaj iznos se određuje korišćenjem definisanih nivoa kilometraže ili, ako nisu postavljeni nivoi kilometraže, prateći standardnu stopu kilometraže. 

Nivoi kilometraže mogu se podesiti tako što ćete otići na **Upravljanje troškovima** > **Podešavanje** > **Opšti podaci** > **Kategorije troškova** > **Kilometraža** > **Podešavanje kategorije**.

Nakon nadogradnje na verziju 10.0.18, ako vaša organizacija koristi kategoriju troškova kilometraže, razmislite o omogućavanju funkcije kilometraže nakon pregleda promena dizajna u nastavku. 

Novi dizajn nivoa kilometraže utiče na to kako se obrađuje vrednost u polju **Količina**. Pre objavljivanja verzije 10.0.18, vrednost u polju **Količina** se smatrala donjim ograničenjem. Kada je akumulacija prešla tu vrednost, korišćena je odgovarajuća stopa.  Od verzije 10.0.18, vrednost u polju **Količina** se smatra gornjim ograničenjem. Odgovarajuća stopa se koristi kada je akumulirana kilometraža manja od vrednosti u polju **Količina**.  Novi model za kilometražu pomaže u doslednosti među kilometrima i boljoj upotrebljivosti.   

Svi odobreni izveštaji o troškovima biće preračunati tokom knjiženja u skladu sa novim dizajnom.

## <a name="example"></a>Primer
 
### <a name="before-version-10018"></a>Pre verzije 10.0.18
Sa dva nivoa kilometraže, polje **Količina** u svakom nivou predstavlja donje ograničenje kilometraže. Trenutno, prvi nivo ima vrednost nula (0) i stopu od 0,45, a drugi nivo ima vrednost 1000 i stopu od 0,25. Ako akumulirane milje ili kilometri pređu vrednost u polju, koristi se odgovarajuća stopa. Ako ne postoji stavka sa nultom količinom, sistem koristi stopu pređenih kilometara koja je definisana u upravljanju troškovima. 
 
Ako zaposleni podnese izveštaj o trošku od 1500 milja, dve stavke kilometraže u objavljenom izveštaju o troškovima bile bi: 1000 (stopa 0,45) + 500 (stopa 0,25) = 575,00.

### <a name="after-version-10018"></a>Posle verzije 10.0.18
U verziji 10.0.18, polje **Količina** u svakom nivou predstavlja gornje ograničenje nivoa. Trenutno, prvi nivo ima vrednost 999 i stopu od 0,45, a drugi nivo ima vrednost 999.999.999,00 i stopu od 0,25. Ako akumulirane milje ili kilometri pređu vrednost u polju **Količina**, koristi se odgovarajuća stopa. Ako se premaše sva gornja ograničenja, sistem koristi kilometražu koja je definisana u upravljanju troškovima. 
 
Da bi se pravilno izračunao isti scenario, postavljeni nivo mora biti promenjen. Polje **Količina** u prvom nivou ima vrednost 999,00 i vrednost 999.999.999,00 u drugom nivou. Ako zaposleni premaši ukupnu količinu milja ili kilometara u prvom nivou, sistem koristi kilometražu koja je definisana u upravljanju troškovima. 
  
Ako zaposleni podnese izveštaj o trošku od 1500 milja, dve stavke kilometraže u objavljenom izveštaju o troškovima bile bi: 1000 (stopa 0,45) + 500 (stopa 0,25) = 575

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a>Omogućavanje izračunavanja kilometraže za više nivoa pređenih kilometara sa istom funkcijom stope

Funkcija **Izračunavanje kilometraže za više nivoa pređenih kilometara sa istom stopom** poboljšava izračunavanje kilometraže. Dovršite sledeće korake da biste omogućili ovu funkciju.

1. Idite na stavku **Radni prostori** > **Upravljanje funkcijama**. 
2. Na listi pronađite i izaberite **Izračunavanje kilometraže za više nivoa pređenih kilometara sa istom stopom**, a zatim izaberite **Omogući odmah**.

Kada omogućite funkciju, resetujte nivoe kilometraže da pravilno odražavaju vrednost polja **Količina**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
