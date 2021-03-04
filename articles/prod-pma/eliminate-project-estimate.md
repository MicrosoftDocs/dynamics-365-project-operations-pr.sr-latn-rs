---
title: Eliminisanje procene za projekat
description: Ova tema pruža informacije o eliminisanju procene projekta nakon što je završena.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 8bda8a7357e883b948449b2a19bea476996dde3c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083633"
---
# <a name="eliminate-a-project-estimate"></a>Eliminisanje procene za projekat

[!include [banner](../includes/banner.md)]

Procene projekta pružaju finansijski prikaz za posao koji je procenjen i zakazan za projekat. Da biste radili sa procenama za projekat, morate priložiti projekat projektu za procenu. Projekt procene uvek se zasniva na postojećem projektu, međutim više projekata može se odnositi na jedan projekat procene. Za procenu projekata mogu se priložiti samo projekti sa fiksnom cenom i investicioni projekti, koji moraju pripadati istoj projektnoj grupi kao i projekat procene.

Da bi se eliminisao projekt procene, on mora biti potpun. Sledeći koraci objašnjavaju kako eliminisati procenu.

1. Idite na **Upravljanje projektima i računovodstvo** > **Svi projekti** i otvorite projekat. 
2. Na kartici **Upravljanje** izaberite **Procene** i na stranici **Procena** izaberite stranicu **Eliminisanje**.
3. Na stranici **Eliminišite procenu** na kartici **Opšti podaci** postavite sledeće opcije:

   - **Šifra perioda** : Izaberite šifru perioda da biste izabrali odgovarajuće procene projekata. 
   - **Datum procene** : Izaberite odgovarajući datum procene za eliminisanje.
   - **Eliminišite WIP upozorenja** : Omogućite ovu opciju da biste pružili obaveštenje kada će procena koja je povezana sa radom u toku (WIP) biti uklonjena. Kada ova opcija nije omogućena, uklanjanje se ne može nastaviti ako postoje neprocenjene transakcije. 
   > [!NOTE]
   > Ova opcija je dostupna samo kada se eliminacija primenjuje na procenjeni projekat. Nije dostupna ako koristite periodična objavljivanja. Ovo podešavanje radi sa podešavanjima na kartici **Procena** , na stranici **Parametri projekta** , u grupi polja **Dozvolite eliminaciju kada postoje neprocenjene transakcije**.
   - **Postavite fazu na Završeno** : Omogućite ovu opciju da biste postavili fazu procene projekta na **Završeno** nakon što pokrenete eliminaciju.
   - **Odštampajte listu procena** : Izaberite informacije koje će biti uključene kada se odštampa lista procena.
   - **Prikaži Infolog** : Omogućite ovu opciju za prikaz Infolog-a.
   - **Datum knjiženja** : Izaberite datum knjiženja procene u knjizi.

4.  Izaberite **U redu**.
5. Nakon završetka postupka eliminacije, projekat sa eliminisanom procenom prikazuje se sa negativnom vrednošću. 

Ako niste nameravali da eliminišete procenu, možete da izaberete eliminisanu procenu i izaberete **Opozovi eliminaciju**.   


[!INCLUDE[footer-include](../includes/footer-banner.md)]