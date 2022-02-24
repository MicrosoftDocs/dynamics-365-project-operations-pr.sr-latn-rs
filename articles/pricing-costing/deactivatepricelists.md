---
title: Deaktiviranje cenovnika
description: Ova tema objašnjava kako da deaktivirate ili uklonite neiskorišćene ili stare cenovnike.
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701968"
---
# <a name="deactivate-price-lists"></a>Deaktiviranje cenovnika 

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Da biste uklonili stare ili neiskorišćene cenovnike iz usluge Dynamics 365 Project Operations, postoje dva koraka koja morate izvršiti. 

1. Uklonite ili izbrišite cenovnik sa određenih stranica.
2. Deaktivirajte ili izbrišite cenovnik iz aktivnih cenovnika na stranici **Cenovnici**.

>[!IMPORTANT]
> Morate obaviti oba koraka da biste u potpunosti uklonili cenovnik. Nije dovoljno da obavite samo 2. korak, a to je direktno brisanje ili deaktiviranje cenovnika iz prikaza Aktivni cenovnici. Morate izbrisati i povezivanje ovog cenovnika sa svih mesta pomenutih u 1. koraku.

## <a name="delete-the-price-list-from-specific-pages"></a>Brisanje cenovnika sa određenih stranica
1. Da biste izbrisali cenovnik iz usluge Project Operations, idite na sledeće stranice:  

      - Stranica **Parametri projekta** > kartica **Cenovnici**
      - Stranica **Organizaciona jedinica** > mreža **Cenovnici**
      - Stranica **Poslovni kontakt** > mreža **Cenovnici projekta**
      - Stranica **Ponude za projekat** > mreža **Cenovnici projekta**: Ovo se odnosi na sve aktivne ponude za projekat.
      - Stranica **Ugovori o projektu** > mreža **Cenovnici projekta**: Ovo se odnosi na sve aktivne ugovore o projektu.

 2. Za svaku stranicu, morate izabrati cenovnik koji želite da izbrišete, a zatim izaberite **Izbriši**. 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>Brisanje ili deaktiviranje cenovnika sa stranice Cenovnici
 
1. Da biste izbrisali cenovnik iz aktivnih cenovnika, idite na **Prodaja** > **Klijenti** > **Cenovnici**. 
2. Izaberite cenovnik koji želite da izbrišete, a zatim izaberite **Izbriši**. Ako se cenovnik koristi u bilo kojoj transakciji, nećete moći da ga izbrišete. Ako se to dogodi, možete deaktivirati cenovnik tako da se ne prikazuje ni u jednom prikazu. 
3. Da biste deaktivirali cenovnik, ponovo izaberite cenovnik, a zatim izaberite **Deaktiviraj**.   
