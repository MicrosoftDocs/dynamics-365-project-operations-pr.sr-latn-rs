---
title: Šta je novo ili promenjeno u aplikaciji Project Service Automation u verziji 3.x talasu 1 za 2020. godinu
description: U ovoj temi date su informacije o tome šta je novo i šta se promenilo u rešenju Project Service Automation u verziji 3 talasu 1 za 2020.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755161"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Šta je novo ili promenjeno u aplikaciji Project Service Automation u verziji 3 talasu 1 za 2020. godinu
Tema ističe ključne činjenice koje treba uzeti u obzir prilikom nadogradnje kada prelazite na najnovije izdanje rešenja Project Service Automation (PSA) verzije 3.x talasa 1 za 2020.

## <a name="time-entry"></a>Stavka vremena
Iskustvo stavke vremena je prošireno kako bi isporučilo mogućnosti produžetka stavke vremena u više scenarija klijenata. Ovo obuhvata mogućnost dodavanja tipova stavki, koji sada pokreću određeno ponašanje na osnovu naziva plana polja **Podešavanja stavke vremena**, prikazano kao **Izvor vremena**.

### <a name="upgrade-consideration"></a>Činjenica koju treba uzeti u obzir prilikom nadogradnje
Kako bi ova funkcionalnost bila podržana, uloge u okviru rešenja PSA su ažurirana tako da obuhvataju nove privilegije. Ove privilegije omogućavaju pristup za čitanje novom entitetu, **Podešavanja stavke vremena**.

Korisnicima koji zahtevaju mogućnost evidentiranja vremena bi pored postojećih uloga trebalo dodeliti korisničku ulogu **Korisnik stavke vremena**. Ova uloga uključuje novu funkcionalnost i obezbeđuje da stavka vremena i dalje radi.

### <a name="currently-extended-time-entry-changes"></a>Trenutno promenjene proširene stavke vremena
Kako bi se smanjio uticaj na trenutne korisnike stavke vremena, ova promena uloge je jedini suštinski zahtev koji je neophodan kako bi se i dalje koristila stavka vremena. Ako ste kreirali prilagođene prikaze ili odvojena iskustva stavki vremena, morate podesiti polja **Podešavanje stavke vremena** na ispravnu PSA vrednost.
