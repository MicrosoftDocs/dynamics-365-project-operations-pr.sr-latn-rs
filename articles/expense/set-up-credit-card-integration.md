---
title: Podešavanje integracije kreditne kartice
description: Ovaj članak objašnjava kako se radi sa transakcijama kreditnom karticom povezanim sa troškovima.
author: suvaidya
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4d32754548af67bdd5b9f7345f6363bd6193b36d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924512"
---
# <a name="set-up-credit-card-integration"></a>Podešavanje integracije kreditne kartice

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Transakcije povezane sa troškovima kreditne kartice mogu se podesiti tako da se automatski uvoze po redovnom rasporedu. Osim toga, transakcije se mogu ručno uvesti po potrebi. Transakcije kreditnom karticom se uvoze preko entiteta podataka transakcija kreditnom karticom.

## <a name="import-credit-card-transactions"></a>Uvoz transakcija kreditnom karticom

Da biste uvezli transakcije kreditnom karticom, sledite ove korake:

1. Na stranici **Transakcije kreditnim karticama** izaberite **Uvezi transakcije**. Ako prvi put otvarate upravljanje podacima, sistem mora da ažurira listu entiteta podataka pre nego što možete da nastavite.
2. U polje **Naziv** unesite jedinstveni opis posla uvoza.
3. U polju **Format izvornih podataka** izaberite format datoteke koja sadrži transakcije kreditnom karticom za uvoz.
4. Izaberite **Otpremi**, a zatim pronađite i izaberite datoteku za uvoz.
5. Kada otpremite datoteku, potvrdite mapiranje datoteke transakcije kreditne kartice i kolone entiteta podataka transakcija kreditnom karticom izborom veze **Prikaži mapu** na pločici. Ako postoje greške u mapiranju ili ako morate da promenite mapiranje, napravite promene u mapiranju sa kartice **Vizuelizacija mapiranja** ili **Detalji mapiranja**.
6. Da biste automatizovali transakcije kreditnom karticom, izaberite **Kreiraj periodičan posao sa podacima**. Zatim možete podesiti ponavljanje koje definiše koliko često treba uvoziti transakcije kreditnim karticama. Kada završite, izaberite **U redu**.
7. Da biste sada uvezli izabranu datoteku, izaberite **Uvezi**.
8. Ako se tokom uvoza pojave greške, možete pregledati evidenciju izvršenja ili pripremne podatke da biste videli greške koje morate ispraviti da biste obezbedili uspešan uvoz.

> [!NOTE]
> Ako treba da uvezete više od jednog formata datoteke, morate kreirati zasebne poslove uvoza za svaki tip formata.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Ponovo dodelite transakcije kreditnom karticom otkazanim zaposlenima

Nakon ukidanja evidencije zaposlenog, onemogućen je njegov Active Directory Domain Services (AD DS) nalog. Međutim, možda postoje aktivne transakcije kreditnim karticama koje se i dalje moraju trošiti i nadoknaditi. Na stranici **Transakcije kreditnim karticama** možete ponovo dodeliti zaposlenog za bilo koju transakciju kreditnom karticom u kojoj je povezani zaposleni prekinut.

Izaberite jednu ili više transakcija kreditnom karticom, a zatim izaberite **Ponovo dodelite transakcije**. Zatim možete da izaberete drugog zaposlenog kome ćete dodeliti transakcije kreditnom karticom. Nakon što se transakcije sa kreditnom karticom prerasporede, mogu se odabrati za izveštaj o troškovima i platiti kroz uobičajeni postupak za nadoknadu troškova.

## <a name="delete-credit-card-transactions"></a>Brisanje transakcija kreditnom karticom 

Ponekad, nakon uvoza transakcija kreditnom karticom, određene transakcije možda treba izbrisati. To je možda zato što su transakcije duplikati ili što podaci nisu tačni. Administratori mogu da koriste funkciju **„Brisanje transakcija kreditnom karticom“** za odabir i brisanje transakcija kreditnom karticom koje **nisu priložene** na izveštaj o troškovima. 

1. Idite na stranicu **Periodični zadaci** > **Brisanje transakcija kreditnom karticom**.
2. Izaberite **Filter** i navedite informacije za identifikaciju zapisa koje treba uključiti.
3. Izaberite **U redu** da biste izbrisali zapise. 

## <a name="storing-credit-card-numbers"></a>Skladištenje brojeva kreditnih kartica

Za skladištenje brojeva kreditnih kartica dostupne su tri opcije. Brojevi kreditnih kartica se skladište na stranici **Parametri upravljanja troškovima**.

- **Sprečavanje unosa broja kartice** – Brojevi kreditnih kartica se ne čuvaju.
- **Heširaj brojeve kartica (skladišti poslednje četiri cifre)** – Poslednje četiri cifre brojeva kreditnih kartica skladište se u šifrovanom formatu.
- **Skladišti brojeve kartica** – Brojevi kreditnih kartica skladište se u nešifrovanom formatu. Ova opcija nije u skladu sa Standardom bezbednosti podataka industrije platnih kartica (PCI) (DSS). Stoga, da bi njihova organizacija bila usaglašena sa PCI DSS propisima, administratori organizacije bi trebalo da izaberu da ne skladište brojeve kreditnih kartica ili da skladište heširane brojeve kartica.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
