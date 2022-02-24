---
title: Uvoz i održavanje transakcija kreditnim karticama
description: Ova tema objašnjava kako da uvedete i održavate transakcije kreditne kartice povezane sa troškovima. Ove transakcije se mogu podesiti tako da se automatski uvoze po redovnom rasporedu ili se mogu ručno uvesti po potrebi.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: df5c6bce8a534f4f8b1872e2bd5cc8a58ef11189
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271595"
---
# <a name="import-and-maintain-credit-card-transactions"></a>Uvoz i održavanje transakcija kreditnim karticama

Transakcije povezane sa troškovima kreditne kartice mogu se podesiti tako da se automatski uvoze po redovnom rasporedu. Osim toga, transakcije se mogu ručno uvesti po potrebi. Transakcije kreditnom karticom se uvoze preko entiteta podataka transakcija kreditnom karticom.

Za više informacija o entitetima podataka pogledajte [Entiteti podataka](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).

## <a name="import-credit-card-transactions"></a>Uvoz transakcija kreditnom karticom

1. Na stranici **Transakcije kreditnim karticama** izaberite **Uvezi transakcije**. Ako prvi put otvarate upravljanje podacima, sistem mora da ažurira listu entiteta podataka pre nego što možete da nastavite.
2. U polju **Naziv** unesite jedinstveni opis posla uvoza.
3. U polju **Format izvornih podataka** izaberite format datoteke koja sadrži transakcije kreditnom karticom za uvoz.
4. Izaberite **Otpremi**, a zatim pronađite i izaberite datoteku za uvoz.
5. Nakon što je datoteka otpremljena, potvrdite mapiranje datoteke transakcije kreditne kartice i kolona entiteta podataka transakcija kreditnom karticom izborom veze **Prikaži mapu** na pločici. Ako postoje greške u mapiranju ili ako morate da promenite mapiranje, napravite promene u mapiranju sa kartice **Vizuelizacija mapiranja** ili **Detalji mapiranja**.
6. Da biste automatizovali transakcije kreditnom karticom, izaberite **Kreiraj periodičan posao sa podacima**. Zatim možete podesiti ponavljanje koje definiše koliko često treba uvoziti transakcije kreditnim karticama. Kada završite, izaberite **U redu**.
7. Da biste sada uvezli izabranu datoteku, izaberite **Uvezi**.
8. Ako se tokom uvoza pojave greške, možete pregledati evidenciju izvršenja ili podatke o pripremi da biste videli greške koje morate ispraviti da biste garantovali uspešan uvoz.

> [!NOTE]
> Ako morate uvesti više od jednog formata datoteke, morate stvoriti zasebne poslove uvoza za svaki tip formata.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Ponovo dodelite transakcije kreditnom karticom otkazanim zaposlenima

Nakon ukidanja evidencije zaposlenog, onemogućen je njegov Active Directory Domain Services (AD DS) nalog. Međutim, možda postoje aktivne transakcije kreditnim karticama koje se i dalje moraju trošiti i nadoknaditi. Na stranici **Transakcije kreditnim karticama** možete dodeliti zaposlenog bilo kojoj transakciji kreditnom karticom za koju je povezani zaposleni ukinut.

Izaberite jednu ili više transakcija kreditnom karticom, a zatim izaberite **Ponovo dodelite transakcije**. Zatim možete da izaberete drugog zaposlenog kome ćete dodeliti transakcije kreditnom karticom. Nakon što se transakcije sa kreditnom karticom prerasporede, mogu se odabrati za izveštaj o troškovima i platiti kroz uobičajeni postupak za nadoknadu troškova.


[!INCLUDE[footer-include](../includes/footer-banner.md)]