---
title: Premošćava cena koja je efektivna
description: Ovaj članak sadrži objašnjenja o tome kako da podesite premošćivanje cena za određene cene u cenovnik.
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
# <a name="date-effective-price-overrides"></a>Premošćava cena koja je efektivna 

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

*Zamene cena koje su efektivne za* datum obezbeđuju način da se zamene ili promene određene cene u cenovnik. Na primer, imate standardni cenovnik koji stupa na snagu od 1. januara 2022. do 31. decembra 2022. godine. Ovaj cenovnik ima cene za mnoge uloge. Cena koja je postavljena za ulogu Mrežnog **tehničara** je 100 američkih dolara (USD) na sat. Kada mrežni tehničar evidentira vreme između 1. januara 2022. i 31. decembra 2022. godine, vreme se ceni na 100 USD. Dana 1. oktobra 2022. morate koriguti *cenu samo* **za ulogu Mrežnog** tehničara, od 100 USD na sat do 110 USD po satu. Funkcija **"Datum efektivne cene"** vam omogućava da podesite ovu promenu kao zamnoćivanje reda za tu određenu cenu uloge. Zbog toga ne morate da kopirate ceo cenovnik i promenite cenu samo tog jednog reda.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Datum-efektivna cena zamenjuje cene rada

Proces podešavanja datum-efektivne cene zamenjuje radno vreme na projektu koji se sastoji od dva osnovna koraka.

1. Omogući **funkciju efektivne cene za** datum.
1. Podešavanje zamene cene koja stupa na snagu datuma.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Omogućavanje funkcije "Datum efektivne cene"

> [!NOTE]
> Nakon što **je omogućena funkcija "Datum efektivne** cene", ona se ne može onemogućiti.

Da biste omogućili **funkciju "Datum efektivne cene",** sledite ove korake.

1. Idite na **parametre** \> **postavki.**
1. Otvorite zapis **"Parametri** ".
1. U oknu za radnje, na kartici **Kontrola** funkcija izaberite **stavku Omogući datum efektivne cene.**
1. U dijalogu za potvrdu izaberite **U redu**.
1. Nakon nekoliko trenutaka osvežite pregledač. Mogućnosti zamene cena koje su efektivne sada bi trebalo da budu dostupne. Znaćete da su ove mogućnosti omogućene ako se u oknu **za radnje više ne pojavljuje omogućeno** za datum efektivne cene.

### <a name="set-up-a-date-effective-price-override"></a>Podešavanje zamene cene koja stupa na snagu datuma

Cene koje su efektivne po datumu mogu se podesiti na cenovnici **troška** **·**, prodaje **ili** nabavke.

> [!NOTE]
>Ponašanje datuma **efektivne cene trenutno** ima sledeća ograničenja:
>
> - Samo cene uloga i naznake cena uloga podržavaju funkciju "Datum efektivne **cene" u operacijama** projekta.
> - Kada kopirate cenovnik korišćenjem **radnje Kopiranje** na stranici **sa detaljima cenovnka**, a kada kreirate cenovnik projekta od standardnog ili prilagođenog cenovnka tokom kreiranja ugovora, prekaljene cene koje su efektivne datuma **se** ne kopiraju iz izvornog cenovnka.

Da biste podesili poništavanje cene koja stupa na snagu datuma za cenu uloge ili naznake cena uloge, sledite ove korake.

1. Otvorite stranicu za cenovnik za koji želite da podesite zamenu cene koja stupa na snagu datuma.
1. Izaberite karticu **Cene uloga** . Na ovoj kartici su navedeni **svi zapisi** o cenama uloga u cenovnik.
1. Izaberite zapis **cene** uloge za koji želite da podesite novu cenu zamene koja stupa na snagu datuma, a zatim dvaput dodirnite (ili kliknite dvaput na klik) na cenu **uloge da** biste otvorili **stranicu sa detaljima o ceni** uloge.
1. Izaberite karticu **Datum efektivne zamenjuje** . Koordinatna mreža na ovoj kartici navodi sve cene koje stupaju na snagu datuma za izabrani **zapis cene** uloge.
1. Na traci sa alatkama iznad koordinatne mreže izaberite **stavku Zamena nove cene uloge**. Otvoriće **se klizač "Nova cena** uloge".
1. Navedite datum stupanja na snagu, jedinicu i novu cenu za premošćavanje cene. Zatim izaberite **Sačuvaj** i zatvorite obrazac.

> [!NOTE]
> - Zamena cene koja stupa na snagu datuma za cenu uloge ili naznake cene uloge primenljiva je na istu kombinaciju vrednosti dimenzija cena koje postoje u nadređenoj **ceni** **uloge ili redu naznaka cena uloga.**
> - Datum koji je izabran u polju Efektivno od **trebalo bi** da bude u okviru datuma stupanja na snagu nadređenog cenovnka. Zamena cene će stupiti na snagu na datum koji je izabran **u polju Efektvori iz** i primenjivaće se do kraja krajnjeg datuma nadređenog cenovnka. Ako podesite još jednu zamenu cene koja stupa na snagu datuma za istu cenu uloge, prva zamena cene će stupiti na snagu na datum koji je **izabran u polju Efektvori** iz i primenjivaće se do početka drugog premošćavanja.

## <a name="examples"></a>Primeri

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Primer 1: Utvrđivanje efekata datuma za cenu uloge koja ima premošćavanje cene uloga

Sledeći primer prikazuje kako se određuje efekat datuma za određenu cenu uloge za koju su podešene cene uloga.

**Cenovnik A: od 1. januara do 30. juna**

*Cena uloge*

| Cena uloge | Jedinica | Cena | Uticaj na cene za dolazne transakcije |
|---|---|---|---|
| Mrežni tehničar | Sat | 100 | Ova cena će biti korišćena na bilo kojim transakcijama gde je datum transakcije između 1. |

*Zamena cene uloge*

| Efektivno od | Jedinica | Cena | Uticaj na cene za dolazne transakcije |
|---|---|---|---|
| mart 15. | Sat | 110 | Ova cena će biti korišćena za sve transakcije gde je datum transakcije između 15. |
| April 1 | Sat | 120 | Ova cena će biti korišćena za sve transakcije gde je datum transakcije između 1. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Primer 2: Utvrđivanje efekata datuma za naznake cena uloge koje imaju prenaglašavanje cena uloga

Sledeći primer prikazuje kako se određuje efekat datuma za određenu naznaku cene uloga za koju su podešene prenaglašavanja cena uloga.

**Cenovnik A: od 1. januara do 30. juna**

*Cena uloge*

| Cena uloge | Radno vreme | Jedinica | Cena | Uticaj na cene za dolazne transakcije |
|---|---|---|---|---|
| Mrežni tehničar | Redovne | Sat | 100 | Ova cena će biti korišćena na bilo kojim transakcijama gde je datum transakcije između 1. |

*Naznake cene uloga*

| Organizaciona jedinica | Radno vreme | Označi % |
|---|---|---|
| Contoso US | Prekovremeni rad | 10% |

*Zamena naznaka cena uloga*

| Efektivno od | Cena | Uticaj na cene za dolazne transakcije |
|---|---|---|
| mart 15. | 20% | Ovaj procenat naznaka će se koristiti za sve transakcije u kojima je datum transakcije između 15. |
| April 1 | 25% | Ove naznake će se koristiti za sve transakcije u kojima je datum transakcije između 1. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
