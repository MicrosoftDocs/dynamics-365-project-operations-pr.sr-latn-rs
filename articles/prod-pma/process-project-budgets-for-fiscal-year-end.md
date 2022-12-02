---
title: Prenos budžeta projekata na kraj fiskalne godine
description: Ovaj članak daje informacije o tome kako preneti preostale iznose budžeta u buduće godine i stvoriti detalje budžetskog registra.
author: Yowelle
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 5b4e768cb78d6a6cb76b3c338fd76363d5290ebd
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684061"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Prenos budžeta projekata na kraj fiskalne godine

[!include [banner](../includes/banner.md)]

Kada radite na višegodišnjem projektu, možda ćete imati preostali budžet na kraju fiskalne godine. Preostale iznose budžeta možete preneti u buduću godinu i stvoriti detalje registra budžeta za iznose na povezanim računima glavne knjige. Pre nego što prenesete preostale iznose, pregledajte i analizirajte preostale iznose budžeta.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Pregledajte i analizirajte preostale iznose budžeta

Dovršite sledeće korake da biste pregledali iznose budžeta na kraju godine za projekte, ali ne i da biste ih preneli dalje.

1. Idite na **Upravljanje projektima i računovodstvo** > **Periodično** > **Budžeti** > **Prenesi budžete**. 
2. Na stranici **Proces prenosa budžeta projekta**, na kartici **Opcije za kraj godine**, potvrdite da opcija **Prenesite preostale iznose budžeta projekta** nije omogućena.
3. Na kartici **Parametri** u polju **Godina budžeta projekta** odaberite fiskalnu godinu za koju želite da vidite preostali iznos budžeta. 
4. U polju **Početna fiskalna godina** odaberite fiskalnu godinu za koju želite da vidite preostali iznos budžeta. 
5. U polju **Iz modela prognoze** izaberite **Preostali budžet**. 
6. Da biste uključili projekte koji ispunjavaju izabrane kriterijume i nemaju preostali budžet, izaberite **Pokaži preostalu nulu**.  
7. Na kartici **Izaberite budžete** izaberite **Preuzmite sve budžete** da biste učitali sve budžete koji odgovaraju odabranim kriterijumima, a zatim izaberite **Obradi**. 
8. Da biste dizajnirali upit baze podataka koji učitava određeni skup budžeta u okno, izaberite **Preuzimanje izabranih budžeta**.

Za više informacija o određenoj liniji u oknu odaberite liniju, a zatim izaberite **Prikaži detalje o budžetu** ili **Prikaži naloge**.

## <a name="carry-forward-remaining-budget-amounts"></a>Prenesite preostale iznose budžeta 

Kada obrađujete preostale iznose budžeta, možete da kreirate transakcije u glavnoj knjizi za iznose koje prenosite dalje. Da biste kreirali transakcije glavne knjige, izvršite korake u odeljku [Prenesite budžetske iznose i kreirajte transakcije iz glavne knjige](#carry-forward). 

> [!NOTE]
> Iznosi budžeta koji se prenose, prebacuju se na model predviđanja koji je izabran na stranici **Modeli predviđanja** kao model prognoze prenosa.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Prenesite budžetske iznose i kreirajte transakcije iz glavne knjige

1.  Izaberite **Upravljanje projektima i računovodstvo** > **Periodično** > **Budžeti** > **Prenesi budžete**. 
2. Na stranici **Proces prenosa budžeta projekta** izaberite **Kraj godine**, a zatim omogućite **Prenesite preostale iznose budžeta projekta** i **Kreirajte unose u registru budžeta u glavnoj knjizi**. 
3. Na kartici **Parametri**, u grupi polja **Parametri projekta** izaberite sledeće:

   - **Godina budžeta projekta**: Odaberite početak fiskalne godine za koju želite da vidite preostale iznose budžeta. 
   - **Profit i gubitak**: Kreirajte transakcije dobiti i gubitka u glavnoj knjizi. 
   -  **WIP**: Kreirajte transakcije u toku (WIP) u glavnoj knjizi.
   -  **Zarada**: Kreirajte transakcije raspodele zarada u glavnoj knjizi. 

5. U grupi polja **Glavna knjiga** navedite sledeće informacije: 

   - U polju **Početna fiskalna godina** odaberite fiskalnu godinu na koju želite da prenesete preostale iznose budžeta za projekte. Podrazumevana vrednost je godinu dana nakon vrednosti u polju **Godina budžeta projekta**.
   -  U polju **Period prenosa** odaberite period za koji želite da kreirate detalje budžetskog registra u glavnoj knjizi. Ovo je obično prvi period početne fiskalne godine.

6. U grupi polja **Kopiranje iz/u** navedite sledeće informacije:

   - U polju **Iz modela prognoze** izaberite model predviđanja budžeta projekta povezan sa preostalim iznosima budžeta koje želite da prenesete za projekte. 
   - U polju **Ka modelu budžeta knjige** izaberite model budžeta knjige projekta povezan sa preostalim iznosima budžeta koje želite da prenesete u glavnu knjigu. 
   -  Izaberite **Prenesite valutu prodaje** da biste koristili valutu prodaje projekta za transakcije glavne knjige koje se kreiraju kada prenesete iznose budžeta za projekte. Kada opcija nije izabrana, transakcije koriste računovodstvenu valutu. 
   -  Izaberite **Pokaži preostalu nulu** da biste uključili projekte koji nemaju preostali iznos budžeta, ali ispunjavaju ostale kriterijume koje odaberete u projektima prikazanim u donjem oknu.

7. Na kartici **Izaberite budžete** izaberite **Preuzmite sve budžete** da biste učitali sve budžete koji odgovaraju odabranim kriterijumima. Ako želite da dizajnirate upit baze podataka koji učitava određeni skup budžeta projekata u okno, izaberite **Preuzimanje izabranih budžeta**.
8. Za svaki projekat koji želite da obradite odaberite opciju na početku reda za projekat.

    > [!TIP]
    > Da biste izabrali sve ili većinu projekata, izaberite potvrdni znak u gornjem levom uglu. Da biste isključili obradu bilo kog projekta, uklonite oznaku za taj projekat.

9. Da biste prebacili preostale iznose budžeta za izabrane projekte na izabranu fiskalnu godinu i kreirali detalje budžetskog registra u glavnoj knjizi, izaberite **Obradi**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Prenesite budžetske iznose bez kreiranja transakcija iz glavne knjige

1. Idite na **Upravljanje projektima i računovodstvo** > **Periodično** > **Budžeti** > **Prenesi budžete**.
2. Na stranici **Proces prenosa budžeta projekta**, u polju **Opcije za kraj godine**, izaberite **Prenesite preostale iznose budžeta projekta**.
3. U grupi **Parametri** u polju **Godina budžeta projekta** odaberite fiskalnu godinu za koju želite da vidite preostale iznose budžeta.
4. U grupi **Kopiranje iz/u** navedite sledeće informacije:

   - U polju **Iz modela prognoze** izaberite model predviđanja budžeta projekta koji je povezan sa preostalim iznosima budžeta koje želite da prenesete za projekte. 
   - Izaberite **Pokaži preostalu nulu** da biste uključili projekte koji nemaju preostali budžet, ali ispunjavaju druge izabrane kriterijume.
   - U grupi **Izaberite budžete** izaberite **Preuzmite sve budžete** da biste učitali sve budžete koji odgovaraju odabranim kriterijumima. Da biste dizajnirali upit baze podataka koji učitava određeni skup budžeta projekata u okno, izaberite **Preuzimanje izabranih budžeta**.

5. Za svaki projekat koji želite da obradite odaberite opciju na početku reda za projekat. 
6. Izaberite **Obradi** da biste preneli preostale iznose budžeta za odabrane projekte na izabranu fiskalnu godinu.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
