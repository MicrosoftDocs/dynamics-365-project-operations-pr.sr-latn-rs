---
title: Stavke troškova
description: Ovaj članak sadrži objašnjenja o tome kako da podelite troškove na stavke pomoću redizajniranog radnog prostora za troškove.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 71bfbe83259804fc0b0355c81d430805da23dd45
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920951"
---
# <a name="expense-itemization"></a>Stavke troškova

[!include [banner](../includes/banner.md)]

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Organizacije često zahtevaju od zaposlenih da obezbede detaljnu analizu troškova nastalih tokom putovanja. Na primer, hotelski izvod može da sadrži nekoliko redova podeljenih po stavkama za cenu sobe, porez, parking i druge razne troškove nastale svakog dana tokom trajanja boravka. Ili troškovi obroka mogu zahtevati da navedete detaljniju analizu za doručak, ručak ili večeru. Bez obzira na potrebe organizacije, svaka kategorija troškova može biti podešena tako da odražava potkategorije ili stavke reda koje čine trošak. Iako je stavka uvek bila podržana u **Upravljanju troškovima**, radni prostor **Redizajniranih troškova** omogućava efikasniju podelu na stavke kada je omogućena funkcija **Mogućnost brze podele periodičnih troškova na stavke**.  

## <a name="enable-quick-itemization"></a>Omogućavanje brze podele na stavke 

Funkciju **Mogućnost brze podele periodičnih troškova na stavke** možete koristiti da biste brzo podelili periodične troškove na stavke, izbegavajući potrebu da svaki put unesete dnevne troškove tokom trajanja boravka. Dovršite sledeće korake da biste omogućili brzu podelu na stavke.

1. Idite na radni prostor **Upravljanje funkcijama** i na listi funkcija pronađite i izaberite **Redizajnirani izveštaji o troškovima**. 
2. Izaberite dugme **Omogući odmah**. 
3. Na listi funkcija pronađite i izaberite stavku **Mogućnost brze podele periodičnih troškova na stavke**.
4. Izaberite dugme **Omogući odmah**. 

## <a name="itemization-grid"></a>Matrica koordinatne mreže za podelu na stavke 

Ako kategorija troškova ima potkategorije ili različite komponente koje čine taj trošak, onda može biti podeljena na stavke. Da biste podelili trošak na stavke, izaberite stavku troška u izveštaju o troškovima, a zatim u oknu **Detalji o troškovima** izaberite **Radnje** > **Podeli na stavke**. Klizač **Podela na stavke** otkriva matricu koordinatne mreže sa poljima. Sledeća tabela daje primer svakog polja u matrici koordinatne mreže i načina prikazivanja polja u izveštaju o troškovima. 

|     Polje          |     Opis                                                                                  |     Primer              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Potkategorija    |     Lista potkategorija konfigurisanih u okviru tipa kategorije troškova **Hotel**.             |     Dnevna cena sobe      |
|     Datum početka     |     Datum kada je stavka troškova prvi put nastala.                                           |     13.09.2021.           |
|     Dnevna cena     |     Iznos nastao za stavku troška.                                                    |     200                  |
|     Količina       |     Broj ponavljanja troška tokom kontinuiranog perioda.                       |     3                    |

![Podelite trošak na stavke.](media/Itemization%20screen%201.png)

Kada sačuvate podelu na stavke, videćete pojedinačni red stavke za količinu navedenu u matrici koordinatne mreže za podelu na stavke. Svaki red počinje na datum koji je naveden u matrici koordinatne mreže.

![Izveštaj o podeljenim stavkama.](media/Itemization%20screen%202.png)

