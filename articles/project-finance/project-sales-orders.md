---
title: Ulazne porudžbine projekta za projekte vremena i materijala
description: Ova tema objašnjava kako se kreiraju ulazne porudžbine zasnovane na projektima vremena i materijala.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755120"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Ulazne porudžbine projekta za projekte vremena i materijala

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Ovaj tema opisuje kako se kreira ulazna porudžbina za projekat. Ulazne porudžbine mogu se kreirati samo za projekte tog tipa **vreme i materijal**.

Ako projekat vremena i materijala sadrži više izvora finansiranja u ugovoru o projektu, morate omogućiti parametar **Dozvoli ulazne porudžbine za projekte sa više izvora finansiranja** na stranici **Upravljanje projektom i računovodstveni parametri**. 

> [!NOTE]
> - Podrška za ulazne porudžbine projekata sa više izvora finansiranja dostupna je počev od izdanja aplikacije 10.0.2 i novije.
> - Parametar koji će omogućiti podršku za ulazne porudžbine projekata sa više izvora finansiranja ukloniće se u talasu izdanja iz aprila 2020. godine, nakon čega će funkcionalnost uvek biti omogućena.

Ulazne porudžbine zasnovane na projektu možete kreirati na dva načina:

- Idite na sam projekat. U oknu radnji izaberite **Upravljanje > Zadaci predmeta > Ulazna porudžbina**. Informacije o projektu podrazumevano se stavljaju u ulaznu porudžbinu iz projekta. Ako ugovor o projektu ima više izvora finansiranja, moraćete da izaberete izvor finansiranja da biste postavili klijenta za ulaznu porudžbinu. Ako postoji samo jedan izvor finansiranja za projekat, klijent će biti automatski podešen.
- Idite na stranicu liste **Sve ulazne porudžbine** i kreirajte novu ulaznu porudžbinu. Za ulaznu porudžbinu ćete morati da izaberete projekat. Kada izaberete projekat, klijent će biti postavljen iz izvora finansiranja ili ćete morati izabrati izvor finansiranja ako ugovor o projektu ima više izvora finansiranja.

