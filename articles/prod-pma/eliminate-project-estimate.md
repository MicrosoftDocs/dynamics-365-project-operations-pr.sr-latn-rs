---
title: Eliminisanje procene za projekat
description: Ovaj članak pruža informacije o eliminisanju procene projekta nakon dovršavanja.
author: Yowelle
ms.date: 05/26/2020
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
ms.openlocfilehash: de54659f9e69daf1566f86bec16436c19eeacf49
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932221"
---
# <a name="eliminate-a-project-estimate"></a>Eliminisanje procene za projekat

[!include [banner](../includes/banner.md)]

Procene projekta pružaju finansijski prikaz za posao koji je procenjen i zakazan za projekat. Da biste radili sa procenama za projekat, morate priložiti projekat projektu za procenu. Projekt procene uvek se zasniva na postojećem projektu, međutim više projekata može se odnositi na jedan projekat procene. Za procenu projekata mogu se priložiti samo projekti sa fiksnom cenom i investicioni projekti, koji moraju pripadati istoj projektnoj grupi kao i projekat procene.

Da bi se eliminisao projekt procene, on mora biti potpun. Sledeći koraci objašnjavaju kako eliminisati procenu.

1. Idite na **Upravljanje projektima i računovodstvo** > **Svi projekti** i otvorite projekat. 
2. Na kartici **Upravljanje** izaberite **Procene** i na stranici **Procena** izaberite stranicu **Eliminisanje**.
3. Na stranici **Eliminišite procenu** na kartici **Opšti podaci** postavite sledeće opcije:

   - **Šifra perioda**: Izaberite šifru perioda da biste izabrali odgovarajuće procene projekata. 
   - **Datum procene**: Izaberite odgovarajući datum procene za eliminisanje.
   - **Eliminišite WIP upozorenja**: Omogućite ovu opciju da biste pružili obaveštenje kada će procena koja je povezana sa radom u toku (WIP) biti uklonjena. Kada ova opcija nije omogućena, uklanjanje se ne može nastaviti ako postoje neprocenjene transakcije. 
   > [!NOTE]
   > Ova opcija je dostupna samo kada se eliminacija primenjuje na procenjeni projekat. Nije dostupna ako koristite periodična objavljivanja. Ovo podešavanje radi sa podešavanjima na kartici **Procena**, na stranici **Parametri projekta**, u grupi polja **Dozvolite eliminaciju kada postoje neprocenjene transakcije**.
   - **Postavite fazu na Završeno**: Omogućite ovu opciju da biste postavili fazu procene projekta na **Završeno** nakon što pokrenete eliminaciju.
   - **Odštampajte listu procena**: Izaberite informacije koje će biti uključene kada se odštampa lista procena.
   - **Prikaži Infolog**: Omogućite ovu opciju za prikaz Infolog-a.
   - **Datum knjiženja**: Izaberite datum knjiženja procene u knjizi.

4.  Izaberite **U redu**.
5. Nakon završetka postupka eliminacije, projekat sa eliminisanom procenom prikazuje se sa negativnom vrednošću. 

Ako niste nameravali da eliminišete procenu, možete da izaberete eliminisanu procenu i izaberete **Opozovi eliminaciju**.   


[!INCLUDE[footer-include](../includes/footer-banner.md)]