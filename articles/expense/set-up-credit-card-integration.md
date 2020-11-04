---
title: Podešavanje integracije kreditne kartice
description: Ova tema objašnjava kako da uvedete i održavate transakcije kreditne kartice povezane sa troškovima.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 12c7971204b485ee7cb222cd9cffdfdfde93dcf4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083543"
---
# <a name="set-up-credit-card-integration"></a>Podešavanje integracije kreditne kartice

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Transakcije povezane sa troškovima kreditne kartice mogu se podesiti tako da se automatski uvoze po redovnom rasporedu. Osim toga, transakcije se mogu ručno uvesti po potrebi. Transakcije kreditnom karticom se uvoze preko entiteta podataka transakcija kreditnom karticom.

## <a name="import-credit-card-transactions"></a>Uvoz transakcija kreditnom karticom

1. Na stranici **Transakcije kreditnim karticama** izaberite **Uvezi transakcije**. Ako prvi put otvarate upravljanje podacima, sistem mora da ažurira listu entiteta podataka pre nego što možete da nastavite.
2. U polju **Naziv** unesite jedinstveni opis posla uvoza.
3. U polju **Format izvornih podataka** izaberite format datoteke koja sadrži transakcije kreditnom karticom za uvoz.
4. Izaberite **Otpremi** , a zatim pronađite i izaberite datoteku za uvoz.
5. Nakon što je datoteka otpremljena, potvrdite mapiranje datoteke transakcije kreditne kartice i kolona entiteta podataka transakcija kreditnom karticom izborom veze **Prikaži mapu** na pločici. Ako postoje greške u mapiranju ili ako morate da promenite mapiranje, napravite promene u mapiranju sa kartice **Vizuelizacija mapiranja** ili **Detalji mapiranja**.
6. Da biste automatizovali transakcije kreditnom karticom, izaberite **Kreiraj periodičan posao sa podacima**. Zatim možete podesiti ponavljanje koje definiše koliko često treba uvoziti transakcije kreditnim karticama. Kada završite, izaberite **U redu**.
7. Da biste sada uvezli izabranu datoteku, izaberite **Uvezi**.
8. Ako se tokom uvoza pojave greške, možete pregledati evidenciju izvršenja ili podatke o pripremi da biste videli greške koje morate ispraviti da biste garantovali uspešan uvoz.

> [!NOTE]
> Ako morate uvesti više od jednog formata datoteke, morate stvoriti zasebne poslove uvoza za svaki tip formata.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Ponovo dodelite transakcije kreditnom karticom otkazanim zaposlenima

Nakon ukidanja evidencije zaposlenog, onemogućen je njegov Active Directory Domain Services (AD DS) nalog. Međutim, možda postoje aktivne transakcije kreditnim karticama koje se i dalje moraju trošiti i nadoknaditi. Na stranici **Transakcije kreditnim karticama** možete dodeliti zaposlenog bilo kojoj transakciji kreditnom karticom za koju je povezani zaposleni ukinut.

Izaberite jednu ili više transakcija kreditnom karticom, a zatim izaberite **Ponovo dodelite transakcije**. Zatim možete da izaberete drugog zaposlenog kome ćete dodeliti transakcije kreditnom karticom. Nakon što se transakcije sa kreditnom karticom prerasporede, mogu se odabrati za izveštaj o troškovima i platiti kroz uobičajeni postupak za nadoknadu troškova.
