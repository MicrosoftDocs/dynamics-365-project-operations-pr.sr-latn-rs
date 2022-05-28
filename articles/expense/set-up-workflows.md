---
title: Podesite tokove posla za upravljanje troškovima
description: Možete da podesite proces toka posla koji se koristi za pregled i odobravanje putnih i troškovnih dokumenata.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: da015904aebfb4cfe046407bbf7bc7fe5a0a0faa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581209"
---
# <a name="set-up-workflows-for-expense-management"></a>Podesite tokove posla za upravljanje troškovima

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Možete da podesite proces toka posla za pregled i odobravanje putnih i troškovnih dokumenata. Možete da definišete tokove posla za izveštaje o troškovima, putne zahteve i zahteve za gotovinskim avansom.

Tok posla predstavlja poslovni proces i definiše kako dokument prolazi kroz sistem. Tok posla takođe pokazuje ko mora da izvrši zadatak ili odobri dokument. Postoji nekoliko prednosti korišćenja sistema toka posla u vašoj organizaciji:

- **Dosledni procesi** : Možete da definišete postupak odobravanja za određene dokumente, kao što su zahtevi za kupovinu i izveštaji o troškovima. Korišćenje sistema toka posla pomaže u obezbeđivanju obrade i odobravanja dokumenata na dosledan i efikasan način.
- **Vidljivost procesa** : Možete pratiti status, istoriju i pokazatelje učinka određene instance toka posla. Ovo vam pomaže da utvrdite da li treba izvršiti promene u toku posla kako biste poboljšali efikasnost.
- **Centralizovana radna lista** : Korisnici mogu da vide centralizovanu listu poslova da bi videli zadatke toka posla i odobrenja koja su im dodeljena. 

## <a name="workflow-types"></a>Tipovi toka posla

Sledeća tabela navodi tipove tokova posla u kojima možete da kreirate **Upravljanje troškovima**.


|              <strong>Tip</strong>              |                   <strong>Koristite ovaj tip za</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>Automatsko odobravanje izveštaja o troškovima</strong> |            Kreirajte tokove odobrenja za izveštaje o troškovima.             |
|  <strong>Automatsko objavljivanje izveštaja o troškovima</strong>   |        Kreirajte tokove automatskog objavljivanja za izveštaje o troškovima.        |
|       <strong>Stavka troška</strong>        |     Kreirajte tokove odobrenja za stavke u izveštajima o troškovima.      |
| <strong>Automatsko objavljivanje stavke troška</strong> | Kreirajte tokove automatskog objavljivanja za stavke u izveštajima o troškovima. |
|       <strong>Zahtev za putovanjem</strong>       |          Kreirajte tokove posla odobrenja za putne zahteve.           |
|      <strong>Zahtev za gotovinski avans</strong>      |         Kreirajte tokove odobrenja za zahteve za gotovinskim avansom.          |
|        <strong>Povraćaj PDV-a</strong>        | Kreirajte tokove odobrenja za povraćaj poreza na dodatu vrednost (PDV).  |


[!INCLUDE[footer-include](../includes/footer-banner.md)]