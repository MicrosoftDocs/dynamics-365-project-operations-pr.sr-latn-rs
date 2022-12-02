---
title: Razmatranja o nadogradnji za moderna odobrenja
description: Članak pokriva tačke koje administratori treba da razmotre kada omogućavaju funkcionalnost modernih odobrenja.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 44a933c92d4ef8dff40f20200d74c4bbdf8caa76
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931761"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Razmatranja o nadogradnji za moderna odobrenja 

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

U okviru izdanja 1. talasa za april 2022. godine, funkcionalnost modernih odobrenja će podrazumevano biti omogućena. Ova funkcionalnost poboljšava pouzdanost logike odobravanja i obezbeđuje da utvrdite razlog ako logika odobravanja ne uspe.

U sklopu ove promene, ažuriraju se statusne promene za odobravanja projekta. Status sada prelazi direktno iz **Prosleđeno** u **Odobreno**. **Na čekanju** više nije status za odobrenja. Da biste utvrdili da li je odobrenje na čekanju, proverite da li je odobrenje deo skupa odobrenja, a pregledajte status priloženog skupa odobrenja.

## <a name="before-you-upgrade"></a>Pre nego što nadogradite

Pre nego što izvršite nadogradnju na opciju Moderna odobrenja, uverite se da nemate odobrenja na čekanju. Moderna odobrenja ne koriste status **Na čekanju**. Zbog toga sva odobrenja koja su i dalje označena kao **Na čekanju** nakon nadogradnje neće biti obrađena.

## <a name="after-you-upgrade"></a>Nakon nadogradnje

Kada izvršite nadogradnju na Moderna odobrenja, administrator mora da proveri da li je omogućen tok u oblaku koji obrađuje odobrenja.

1. Prijavite se na [flow.microsoft.com](https://flow.microsoft.com)
2. U gornjem desnom uglu stranice prebacite okruženje na okruženje koje ste nadogradili.
3. Izaberite **Rešenja** da biste naveli rešenja koja su instalirana u okruženju.
4. Sa liste rešenja izaberite **Project Operations** ili **Project Service**.
5. Promenite filter iz **Sve** u **Tokovi u oblaku**.
6. Proverite da li je opcija **Project Service – Periodično zakazivanje skupova odobrenja projekta** postavljena na **Uključeno**. Ako nije, izaberite tok, a zatim izaberite **Uključi**.
7. Proverite da li do obrade dolazi svakih pet minuta tako što ćete pregledati listu **Sistemski poslovi** u oblasti **Postavke**.

## <a name="short-term-rollback"></a>Kratkoročno vraćanje

Ako ne možete da preuzmete promene ili ako naiđete na ozbiljan problem sa ovom funkcijom, možete privremeno da se vratite na prvobitni tok odobrenja izvršavanjem sledećih koraka:
1. Prijavite se u okruženje i proverite da li postoje odobrenja na čekanju.
2. Idite na **Postavke** > **Parametri projekta**.
3. Izaberite **Kontrola funkcije**, a zatim izaberite **Moderna odobrenja** da biste isključili funkciju.

## <a name="removing-the-feature-flag"></a>Uklanjanje zastavice funkcije

U ažuriranju 2. talasa u oktobru 2022. godine, mogućnost isključivanja ove funkcije će biti isključena.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
