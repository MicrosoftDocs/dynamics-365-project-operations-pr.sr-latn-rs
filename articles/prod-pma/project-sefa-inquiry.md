---
title: Raspored troškova istrage savezne pomoći
description: Ova tema pruža informacije o Rasporedu troškova istrage savezne pomoći.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eaf523ab147cbe974fed6e7eab21967404583fe6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083564"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>Raspored troškova istrage savezne pomoći

[!include [banner](../includes/banner.md)]

Prema cirkularnom obaveštenju A-133 Kancelarije za upravljanje i budžet, agencije koje primaju savezna sredstva podležu zahtevima revizije, koje su poznate i kao pojedinačne revizije. Proces revizije se koristi za redovno izveštavanje o prihodima i rashodima saveznih bespovratnih sredstava. Deo izveštaja pojedinačne revizije uključuje Raspored troškova istrage savezne pomoći (SEFA).

Raspored troškova istrage savezne pomoći uključuje naziv i broj Kataloga savezne domaće pomoći (CFDA), broj bespovratne pomoći, godinu dodele, naziv savezne agencije koja obezbeđuje sredstva i naziv entiteta koji daje odobrenje. Upit se odnosi na određeni period. Tipično je taj period isti kao i period finansijskih izveštaja, koji je fiskalna godina.

Upit uključuje grantove koji imaju datume projekcije u odabranom vremenskom rasponu. Kolona **Agencija koja daje pomoć** u upitu prikazuje klijenta pomoći ili, za prolaznu pomoć, agenciju koja daje pomoć. Za prolaznu pomoć, kolona **Prolazna agencija** prikazuje klijenta koji je dobio pomoć. Ako pomoć nije prolazna, kolona **Prolazna agencija** je prazna.

## <a name="set-up-the-cfda-clusters"></a>Podešavanje CFDA grupa

Morate da postavite CFDA grupe koji se mogu povezati sa CFDA brojevima u Rasporedu troškova istrage savezne pomoći.

1. Idite na **Upravljanje projektima i računovodstvo \> Podešavanje \> Pomoć \> Katalog grupa savezne domaće pomoći**.
2. Da biste kreirali CFDA grupu, izaberite **Novo**.
3. Unesite naziv grupe.
4. Izaberite **Sačuvaj** da biste sačuvali promene.

## <a name="set-up-cfda-numbers"></a>Podesite CFDA brojeve

Morate da postavite CFDA brojeve koji se mogu dodati u pomoć i uključiti u Raspored troškova istrage savezne pomoći.

1. Idite na **Upravljanje projektima i računovodstvo \> Podešavanje \> Pomoć \> Katalog brojeva savezne domaće pomoći**.
2. Da biste kreirali CFDA broj, izaberite **Novo**.
3. U kolonu **Broj** unesite CFDA broj.
4. Pritisnite taster **Tab**.
5. U kolonu **Opis** unesite CFDA naziv.
6. Pritisnite taster **Tab**.
7. Opcionalno: U polje **Grupa programa** dodajte odgovarajuću CFDA grupu.
8. Izaberite **Sačuvaj** da biste sačuvali promene.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Postavite pomoć radi izveštavanja o Rasporedu troškova istrage savezne pomoći

1. Idite na **Upravljanje projektima i računovodstvo \> Pomoć \> Pomoć** , i izaberite postojeću pomoć.
2. Na brzoj kartici **Podešavanje** , u polju **Katalog savezne domaće pomoći** dodelite CFDA broj. CFDA broj na pomoći određuje CFDA grupu za izveštavanje.
3. Na brzoj kartici **Kontakt informacije** unesite informacije o davaocu pomoći prateći ove korake:

    1. U polju **Odobri klijenta** unesite klijenta koji je odgovoran za pomoć. Za postojeću pomoć ove informacije su možda već unete.
    2. Navedite da li je korisnik pomoći donator. Ako je korisnik pomoći donator, ostavite polje za potvrdu **Prolazno** prazno. Ako je drugi klijent donator, a korisnik bespovratne pomoći je odgovoran za trošenje i praćenje novca, potvrdite izbor u polju za potvrdu **Prolazno**.

4. Ako ste izabrali polje za potvrdu **Prolazno** u prethodnom koraku, u polje **Agencija koja daje pomoć** polje, unesite klijenta koji je obezbedio pomoć. Agencija koja daje pomoć i korisnik pomoći ne može biti isti klijent.

Evo primera prolazne pomoći:

Savezna vlada finansirala je infrastrukturni projekat za državu. Savezna vlada dala je novac državi da ga potroši. U ovom slučaju, savezna vlada je agencija koja daje pomoć, a država je korisnik pomoći.

> [!NOTE] 
> Kada prvi put uključite funkciju, početni CFDA brojevi će se uneti pomoću postojećih brojeva u pomoći.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>Isključite pomoći iz SEFA izveštavanja na osnovu vrste pomoći

1. Idite na **Upravljanje projektima i računovodstvo \> Podešavanje \> Pomoć \> Vrste pomoći**.
2. Na brzoj kartici **Podrazumevane informacije** izaberite polje za potvrdu **Raspored troškova istrage savezne pomoći**.
3. Izaberite **Sačuvaj** da biste sačuvali promene.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Pokrenite Raspored troškova istrage savezne pomoći

1. Idite na **Upravljanje projektima i računovodstvo \> Upiti i izveštaji \> Upit za pomoć \> Raspored troškova istrage savezne pomoći**.
2. U odeljku **Parametri** pratite sledeće korake:

    1. U polju **Interval datuma** izaberite kôd za interval datuma. Alternativno, u poljima **Od datuma** i **Do danas** definišite datumski interval.
    2. Opcionalno: Da biste u upit uključili samo obračunate transakcije kao prihod, postavite opciju **Uključite samo obračunate prihode** na **Da**.

## <a name="columns"></a>Kolone

Raspored troškova istrage savezne pomoći uključuje sledeće kolone:

- Katalog naziva grupa Savezne domaće pomoći
- Agencija koja daje pomoć
- Prolazna agencija
- Naziv pomoći
- ID pomoći
- ID prijave za pomoć
- Katalog Savezne domaće pomoći
- Priznanice
- Rashodi
