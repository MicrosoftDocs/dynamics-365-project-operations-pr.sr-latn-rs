---
title: Izmene cena na određeni datum
description: Ovaj članak objašnjava kako da podesite izmene cena za određene cene u cenovniku.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 41af5176c0809c9621fc0fa946a04492da7d152b
ms.sourcegitcommit: 37293b0b28f072deafc00112ddbbea91c48a7802
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/08/2022
ms.locfileid: "9446009"
---
# <a name="date-effective-price-overrides"></a>Izmene cena na određeni datum 

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

*Izmene cena na određeni datum* obezbeđuju način zamene ili promene određene cene u cenovniku. Na primer, imate standardni cenovnik koji stupa na snagu od 1. januara 2022. do 31. decembra 2022. godine. Ovaj cenovnik ima cene za mnoge uloge. Cena koja je postavljena za ulogu **Tehničara mreže** je 100 američkih dolara (USD) na sat. Kada tehničar mreže evidentira vreme između 1. januara 2022. i 31. decembra 2022. godine, vreme se ceni na 100 USD. Dana 1. oktobra 2022. morate korigovati cenu *samo* za ulogu **Tehničara mreže**, sa 100 USD na sat na 110 USD po satu. Funkcija **Izmene cena na određeni datum** vam omogućava da podesite ovu promenu kao zamenu reda za tu određenu cenu uloge. Zbog toga ne morate da kopirate ceo cenovnik i menjate cenu samo tog jednog reda.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Izmene cena na određeni datum za cene rada

Proces podešavanja izmene cena na određeni datum za vreme rada na projektu sastoji se od dva osnovna koraka.

1. Omogućite funkciju **Izmena cena na određeni datum**.
1. Podesite izmenu cene na određeni datum.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Omogućite funkciju Izmena cena na određeni datum

> [!NOTE]
> Nakon omogućavanja funkcije **Izmene cena na određeni datum**, ne možete je onemogućiti.

Da biste omogućili funkciju **Izmene cena na određeni datum**, pratite ove korake.

1. Idite na **Postavke** \> **Parametri**.
1. Otvori zapis **Parametri**.
1. U oknu Radnja na kartici **Kontrola funkcije**, izaberite **Omogući izmene cena na određeni datum**.
1. U dijalogu za potvrdu izaberite **U redu**.
1. Nakon nekoliko trenutaka osvežite pregledač. Mogućnosti izmene cena na određeni datum bi sada trebalo da budu dostupne. Znaćete da su ove mogućnosti omogućene ako se **Omogući izmene cena na određeni datum** više ne pojavljuje u oknu Radnja.

### <a name="set-up-a-date-effective-price-override"></a>Podesite izmenu cene na određeni datum

Izmene cena na određeni datum možete podesiti na cenovnicima **Cena**, **Prodaja** ili **Nabavka**.

> [!NOTE]
>Ponašanje **Izmena cena na određeni datum** trenutno ima sledeća ograničenja:
>
> - Samo cene za uloge i naznake cena za uloga podržavaju funkciju **Izmene cena na određeni datum** u rešenju Project Operations.
> - Kada kopirate cenovnik korišćenjem radnje **Kopiranje** na stranici **Detalji cenovnika** i kada kreirate cenovnik projekta od standardnog ili prilagođenog cenovnika tokom kreiranja ugovora, zamene cena koje stupaju na snagu određenog dana se ne **kopiraju** iz izvornog cenovnika.

Da biste podesili zamenu cena koja stupa na snagu određenog datuma za cenu uloge ili proviziju na cenu uloge, pratite ove korake.

1. Otvorite stranicu za cenovnik za koji želite da podesite izmenu cene koja stupa na snagu određenog datuma.
1. Izaberite karticu **Cene uloga**. Na ovoj kartici su navedeni svi zapisi o **Cenama uloga** u cenovniku.
1. Izaberite zapis **Cena uloge** za koji želite da podesite novu izmenu cene koja stupa na snagu određenog datuma, a zatim dvaput dodirnite (ili kliknite dvaput) na **Cena uloge** da biste otvorili stranicu **Detalji o ceni**.
1. Izaberite karticu **Izmene koje stupaju na snagu određenog datuma**. Matrica koordinatne mreže na ovoj kartici navodi sve cene koje stupaju na snagu određenog datuma za izabrani zapis **Cena uloge**.
1. Na traci sa alatkama iznad matrice koordinatne mreže izaberite **Nova izmena cene uloge**. Otvoriće se klizač **Nova izmena cene**.
1. Navedite početni datum stupanja na snagu, jedinicu i novu cenu za izmenu cene. Zatim izaberite **Sačuvaj** i zatvorite obrazac.

> [!NOTE]
> - Izmena cene koja stupa na snagu određenog datuma za cenu uloge ili provizije za cenu uloge primenljiva je na istu kombinaciju vrednosti dimenzija cena koje postoje u nadređenoj **Ceni uloge** ili redu **Provizije na cenu uloga**.
> - Datum koji je izabran u polju **Stupa na snagu od** trebalo bi da bude u okviru datuma stupanja na snagu nadređenog cenovnika. Izmena cene će stupiti na snagu na datum koji je izabran u polju **Stupa na snagu od** i primenjivaće se do kraja krajnjeg datuma nadređenog cenovnika. Ako podesite još jednu izmenu cene koja stupa na snagu određenog datuma za istu cenu uloge, prva izmena cene će stupiti na snagu na datum koji je izabran u polju **Stupa na snagu od** i primenjivaće se do početka druge izmene.

## <a name="examples"></a>Primeri

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>1. primer: Utvrđivanje stupanja na snagu datuma za cenu uloge koja ima izmenu cene uloga

Sledeći primer prikazuje kako se određuje datum stupanja na snagu za određenu cenu uloge za koju su podešene izmene cene uloga.

**Cenovnik A: od 1. januara do 30. juna**

*Cena uloge*

| Cena uloge | Jedinica | Cena | Uticaj na određivanje cene za dolazne transakcije |
|---|---|---|---|
| Mrežni tehničar | Sat | 100 | Ova cena će biti korišćena na bilo kojim transakcijama gde je datum transakcije između 1. januara i 14. marta. |

*Izmena cena uloge*

| Stupa na snagu od | Jedinica | Cena | Uticaj na određivanje cene za dolazne transakcije |
|---|---|---|---|
| mart 15. | Sat | 110 | Ova cena će biti korišćena na bilo kojim transakcijama gde je datum transakcije između 15. marta i 30. marta. |
| April 1 | Sat | 120 | Ova cena će biti korišćena nad bilo kojim transakcijama gde je datum transakcije između 1. aprila i 30. juna. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>2. primer: Utvrđivanje stupanja na snagu datuma za proviziju na cenu uloge koja ima izmenu provizije na cenu uloge

Sledeći primer prikazuje kako se određuje datum stupanja na snagu za određenu proviziju na cenu uloge za koju su podešene izmene provizije na cenu uloga.

**Cenovnik A: od 1. januara do 30. juna**

*Cena uloge*

| Cena uloge | Radno vreme | Jedinica | Cena | Uticaj na određivanje cene za dolazne transakcije |
|---|---|---|---|---|
| Mrežni tehničar | Redovno | Sat | 100 | Ova cena će biti korišćena na bilo kojim transakcijama gde je datum transakcije između 1. januara i 14. marta. |

*Provizija na cenu uloge*

| Organizaciona jedinica | Radno vreme | Provizija u % |
|---|---|---|
| Contoso US | Prekovremeni rad | 10% |

*Izmena provizije na cenu uloge*

| Stupa na snagu od | Cena | Uticaj na određivanje cene za dolazne transakcije |
|---|---|---|
| mart 15. | 20% | Ovaj procenat provizije će biti korišćen na bilo kojim transakcijama gde je datum transakcije između 15. marta i 30. marta. |
| April 1 | 25% | Ova provizija će biti korišćena na bilo kojim transakcijama gde je datum transakcije između 1. aprila i 30. juna. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
