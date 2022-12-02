---
title: Integracija usluge Microsoft Project Client
description: Planiranje i održavanje rasporeda projekta može biti složeno, pa menadžeri projekata moraju da koriste alate koji im pomažu u upravljanju ovim zadatkom. Integracija sa uslugom Microsoft Project Client pruža podršku za otvaranje i upravljanje strukturne analize posla na projektu.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: d2994195ba916ac7a128e8bdd53bea6acb7bd0ba
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685002"
---
# <a name="microsoft-project-client-integration"></a>Integracija usluge Microsoft Project Client

[!include [banner](../includes/banner.md)]

Planiranje i održavanje rasporeda projekta može biti složeno, pa menadžeri projekata moraju da koriste alate koji im pomažu u upravljanju ovim zadatkom. Integracija sa uslugom Microsoft Project Client pruža podršku za otvaranje i upravljanje strukturne analize posla na projektu. Menadžer projekta može objaviti sve promene na strukturnoj analizi posla Dynamics 365 Finance projekta.

> [!NOTE]
> Ako koristite ispravku iz jula (verzija 10.0.4), morate instalirati KB 4054797 i 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Konfigurisanje programskog dodatka za Microsoft Project Client
Da biste omogućili integraciju sa uslugom Microsoft Project Client, potrebno je da instalirate Microsoft Dynamics 365 programski dodatak u korisnikovoj klijentskoj aplikaciji Microsoft Project. To se postiže otvaranjem **Radnog prostora za upravljanje projektima**.

•   Kliknite na **Konfiguriši programski dodatak za klijenta** iz odeljka **Veze** > **Podešavanje** radnog prostora.

•   Kliknite na **Otvori**, a zatim kliknite na **Pokreni** kada to bude zatraženo.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Otvorite i uredite postojeću probnu verziju strukturne analize posla u programu Microsoft Project Client
Ako projekat u usluzi Dynamics 365 Finance već ima kreiranu strukturnu analizu posla, strukturna analiza posla može se otvoriti u aplikaciji Microsoft Project Client ako je strukturna analiza posla u statusu radne verzije. Da biste otvorili stranicu **Projekat**, kliknite na vezu **Otvori u programu Microsoft Project** na kartici **Plan**. Ova stranica se takođe može otvoriti iz aplikacije Microsoft Project Client klikom na **Otvori** na kartici **Microsoft Dynamics 365**. Izaberite **Pravno lice** i **Projekat** sa liste.

> [!NOTE]
> Ako koristite Internet Explorer kao pregledač, moraćete da kliknete na **Sačuvaj** da biste je ručno otvorili sa lokacije na koju se datoteka preuzima. Ili kliknite na **Sačuvaj i otvori** da biste otvorili datoteku u programu Microsoft Project Client. Nemojte da preimenujete naziv datoteke prilikom čuvanja.

Pre nego što izvršite bilo kakvu izmenu datoteke koristeći Microsoft Project Client, treba da je proverite. Kliknite na **Proveri** na kartici **Microsoft Dynamics 365**. Ovo će sprečiti druge korisnike da istovremeno uređuju strukturnu analizu posla iz usluge Finance. Da biste objavili strukturnu analizu posla nakon dovršavanja bilo kakvih izmena, kliknite na **Prijavi** na kartici **Microsoft Dynamics 365**.

Ako je projektni tim već dodat projektu u usluzi Finance, lista resursa će se popuniti članovima tima. Ako projektni tim još nije dodat u projekat, možete odabrati resurse i izgraditi tim unutar aplikacije Microsoft Project Client klikom na dugme **Resursi** na kartici **Microsoft Dynamics 365**. 

Sledeći podaci će se sinhronizovati natrag u Finance kao deo procesa prijave:

•   Naziv zadatka

•   Datum početka

•   Datum završetka

•   Prethodni zadaci

•   Nazivi resursa

•   Kategorija

•   Kategorija resursa

•   Radno vreme

•   Napomene

•   Prioritet

> [!NOTE]
> Ako dodate bilo koju drugu kolonu u Microsoft Project Client datoteku, ona neće biti sačuvana u datoteci i neće se prikazati kada se datoteka ponovo otvori.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Napravite strukturnu analizu posla za postojeći projekat koristeći Microsoft Project Client
Da biste kreirali strukturnu analizu posla koristeći Microsoft Project Client, sledite ove korake:


1.  Otvorite Microsoft Project Client.

2.  Na kartici **Microsoft Dynamics 365**, kliknite na **Otvori**.

3.  Izaberite **Pravno lice** za projekat.

4.  Izaberite **Projekat**.

5.  Kliknite na **Proveri** na kartici **Microsoft Dynamics 365**.

6.  Kada budete spremni za objavljivanje u Finance, kliknite na **Prijavi** na kartici **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Zamenite postojeću strukturnu analizu posla za postojeći projekat koristeći Microsoft Project Client
Da biste kreirali novu strukturnu analizu posla pomoću aplikacije Microsoft Project Client i zamenili postojeću strukturnu analizu posla za postojeći projekat, sledite ove korake:

1.  Otvorite Microsoft Project Client.

2.  Kreirajte raspored u aplikaciji Microsoft Project Client.

3.  Na kartici **Microsoft Dynamics 365**, kliknite na **Sačuvaj promene** > **Zameni postojeći projekat**.

4.  Izaberite **Pravno lice** za projekat.

5.  Izaberite **Projekat**.

6.  Kliknite na dugme **U redu**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Kreirajte novi projekat iz aplikacije Microsoft Project Client


1.  Otvorite Microsoft Project Client.

2.  Kreirajte raspored u aplikaciji Microsoft Project Client.

3.  Na kartici **Microsoft Dynamics 365**, kliknite na **Sačuvaj promene** > **Sačuvaj u novi projekat**.

4.  Izaberite **Pravno lice** za projekat.

5.  Unesite **ID projekta**, ako je neophodno.

6.  Unesite **Naziv projekta**.

7.  Izaberite **Tip projekta**, **Grupu projekta** i **ID ugovora o projektu**. Alternativno, možete da kreirate novi ugovor o projektu klikom na **Novo**.

8.  Izaberite **Kalendar** koji ćete koristiti za obezbeđivanje resursa.

11. Kliknite na dugme **U redu**.

> [!NOTE]
> Programski dodatak Project Client ne podržava sledeće znakove u formatu ID-a projekta:
> 
>   - Donja crta
>   - Period
>   - Razmak
>   - Kosa crta

[!INCLUDE[footer-include](../includes/footer-banner.md)]
