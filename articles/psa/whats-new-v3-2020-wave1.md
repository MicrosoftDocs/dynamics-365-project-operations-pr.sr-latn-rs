---
title: Šta je novo ili promenjeno u aplikaciji Project Service Automation u verziji 3.x talasu 1 za 2020. godinu
description: U ovoj temi date su informacije o tome šta je novo i šta se promenilo u rešenju Project Service Automation u verziji 3 talasu 1 za 2020.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2308f83e09c25059b6a36599b04b5b00f66c704f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126500"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Šta je novo ili promenjeno u aplikaciji Project Service Automation u verziji 3 talasu 1 za 2020. godinu
Tema ističe ključne činjenice koje treba uzeti u obzir prilikom nadogradnje kada prelazite na najnovije izdanje rešenja Project Service Automation (PSA) verzije 3.x talasa 1 za 2020.

## <a name="time-entry"></a>Stavka vremena
Iskustvo stavke vremena je prošireno kako bi isporučilo mogućnosti produžetka stavke vremena u više scenarija klijenata. Ovo obuhvata mogućnost dodavanja tipova stavki, koji sada pokreću određeno ponašanje na osnovu naziva plana polja **Podešavanja stavke vremena**, prikazano kao **Izvor vremena**. Novo rešenje, pod nazivom „Time, Expense, Statusing, and Approvals“ (TESA) je dodat kako bi bila podržana ova funkcionalnost.

### <a name="upgrade-consideration"></a>Činjenica koju treba uzeti u obzir prilikom nadogradnje
Kako bi ova funkcionalnost bila podržana, uloge u okviru rešenja PSA su ažurirana tako da obuhvataju nove privilegije. Ove privilegije omogućavaju pristup za čitanje novom entitetu, **Podešavanja stavke vremena**.

Korisnicima koji zahtevaju mogućnost evidentiranja vremena bi pored postojećih uloga trebalo dodeliti korisničku ulogu **Korisnik stavke vremena**. Ova uloga uključuje novu funkcionalnost i obezbeđuje da stavka vremena i dalje radi.

Pored toga, ako imate prilagođene module aplikacija koji sadrže sve obrasce za entitet unosa vremena, moraćete da uklonite **TESA obrazac za brzo kreiranje stavke vremena** iz modula.

### <a name="currently-extended-time-entry-changes"></a>Trenutno promenjene proširene stavke vremena
Kako bi se smanjio uticaj na trenutne korisnike stavke vremena, ova promena uloge je jedini suštinski zahtev koji je neophodan kako bi se i dalje koristila stavka vremena. Ako ste kreirali prilagođene prikaze ili odvojena iskustva stavki vremena, morate podesiti polja **Podešavanje stavke vremena** na ispravnu PSA vrednost.
