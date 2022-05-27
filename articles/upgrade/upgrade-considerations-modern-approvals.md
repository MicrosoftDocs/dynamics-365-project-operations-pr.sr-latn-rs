---
title: Razmatranja nadogradnje za savremena odobrenja
description: Zakon tema tačke koje bi administratori trebalo da razmotre kada omogućavaju funkcionalnost modernih odobrenja.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: a3757f057a801318feccde9be3e49c7b40fa8fcb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578403"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Razmatranja nadogradnje za savremena odobrenja 

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

U okviru izdanja Wave 1 za april 2022, funkcionalnost modernih odobrenja će podrazumevano biti omogućena. Ova funkcionalnost poboljšava pouzdanost logike odobravanja i obezbeđuje da utvrdite razlog ako logika odobravanja ne uspe.

U sklopu ove promene ažuriraju se statusne promene za odobravanja projekta. Status sada ide direktno iz prosleđenog **u odobreno** **·**. **Neobrađeno** više nije status za odobravanje. Da biste utvrdili da li je odobravanje na čekanju, proverite da li je odobrenje deo skupa odobravanja, a redigujte stanje priloženog skupa odobravanja.

## <a name="before-you-upgrade"></a>Pre nadogradnje

Pre nego što izvršite nadogradnju na opciju "Savremena odobrenja", uverite se da nemate neobrađena odobrenja. Savremena odobrenja ne koriste status "Neobrađeno **·**". Zbog toga sva odobrenja koja su i dalje označena kao "Neobrađena **·**" nakon nadogradnje neće biti obrađena.

## <a name="after-you-upgrade"></a>Nakon nadogradnje

Kada izvršite nadogradnju na opciju "Savremena odobrenja", administrator mora da proveri da li je omogućen protok oblaka koji obrađuje odobravanja.

1. Prijavljivanje u [flow.microsoft.com](https://flow.microsoft.com)
2. U gornjem desnom uglu stranice prebacite okruženje na okruženje koje ste nadogradili.
3. Izaberite **rešenja** da biste nabrajali rešenja koja su instalirana u okruženju.
4. Sa liste rešenja izaberite stavku Operacije **projekta ili** uslugu **projekta**.
5. Promenite filter iz "Sve **"** u tokove **oblaka**.
6. Proverite da li **je opcija "Usluga projekta – periodično planiranje skupova odobravanja** projekta" postavljena na " **Dalje"**. Ako nije, izaberite tok, a zatim izaberite **Uključi**.
7. Proverite da li se obrada odvija svakih pet minuta tako što ćete pregledati **listu sistemskih** poslova u oblasti **"Postavke** ".

## <a name="short-term-rollback"></a>Kratkoročno vraćanje

Ako ne možete da preuzmete promene ili ako naiđete na ozbiljan problem sa ovom funkcijom, možete privremeno da se vratite na originalni tok odobravanja izvršavanjem sledećih koraka:
1. Prijavite se u okruženje i proverite da li postoje neobrađena odobrenja.
2. Idite na **parametre** > **projekta "Postavke"**.
3. Izaberite **kontrolu funkcije**, a zatim izaberite **opciju "Moderna odobrenja** " da biste isključili funkciju.

## <a name="removing-the-feature-flag"></a>Uklanjanje zastavice funkcije

U ažuriranju Talasa 2 u oktobru 2022.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
