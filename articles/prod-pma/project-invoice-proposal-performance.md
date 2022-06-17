---
title: Performanse predloga projektnih faktura
description: Ovaj članak pruža informacije o poboljšanju performansi predloga faktura projekta.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: johnmichalak
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 70069778b7d4326cb23d6bb36e2c78a33da12573
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927207"
---
# <a name="project-invoice-proposal-performance"></a>Performanse predloga projektnih faktura

[!include [banner](../includes/banner.md)]

Kada kreirate novi predlog fakture, možda ćete naići na probleme sa performansama kako se bude povećavao broj projekata i potprojekata. Da bi se poboljšale performanse, dostupna je funkcija koja smanjuje vreme potrebno za kreiranje novog predloga fakture za knjižene transakcije projekata.

## <a name="enable-project-invoice-proposal-performance-enhancement"></a>Omogućite poboljšanje performansi predloga projektnih faktura
Da biste omogućili funkciju poboljšanja performansi predloga projektnih faktura, izvršite sledeće korake.

1.  Idite na **Upravljanje funkcijama** > **Sve**. Na listi funkcija, pronađite **Poboljšanje performansi predloga projektnih faktura**.
2.  Izaberite dugme **Omogući odmah**.
3.  Osvežite pregledač, a zatim napravite novi predlog fakture.

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a>Isključite poboljšanje performansi predloga projektnih faktura
Izvršite sledeće korake da biste isključili funkciju poboljšanja performansi predloga projektnih faktura.

1.  Idite na **Upravljanje funkcijama** > **Sve**. Na listi funkcija, pronađite **Poboljšanje performansi predloga projektnih faktura**.
2.  Izaberite dugme **Onemogući**.
3.  Osvežite pregledač.

> [!NOTE]
> Performanse predloga fakture se ne mogu primeniti kada su omogućena pravila obračuna.
> 
> Tokom grupnog postupka za kreiranje predloga faktura, broj podzadataka podeliće zadatke na maksimalan broj na osnovu broja ugovora sa transakcijama podložnim fakturisanju, bez obzira na to šta ste uneli. Na primer, ako unesete **3** za broj podzadataka za kreiranje predloga fakture u paketu, a postoje samo dva ugovora sa transakcijama koje mogu da se fakturišu, kreiraju se samo dva podzadatka.
