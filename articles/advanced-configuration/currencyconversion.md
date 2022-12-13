---
title: Podešavanje konverzije valute za izračunavanje prodajnih cena iz stope troška
description: Ovaj članak sadrži objašnjenja o tome kako da konfigurišete ponašanje konverzije valute koje će se koristiti u korporaciji Microsoft Dynamics 365 Project Operations kada se transakcije prodaje generišu iz transakcija troškova.
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816698"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>Podešavanje konverzije valute za izračunavanje prodajnih cena iz stope troška

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

U korporaciji Microsoft Dynamics 365 Project Operations prodajne cene za kategorije troškova mogu da se podese kao numeričke vrednosti ili da se podese tako da se izračunavaju na osnovu nastalih troškova.

Kada su podešeni da se izračunavaju na osnovu nastalog troška, dostupne su sledeće opcije:

- Po ceni
- Označavanje procenta preko troška

U scenarijima u kojima se trošak troškova snosi u valuti koja se razlikuje od valute prodaje za ugovor o projektu, za izračunavanje prodajne cene na osnovu troška potrebna je konverzija valute.

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>Ponašanje konverzije valute koje koristi izvorne Dataverse kurseve valuta

Projektne operacije podrazumevano koriste kurseve valuta koji su uskladišteni u tabeli Valuta u Dataverse. Da biste konfigurisali operacije projekta tako da koriste osnovne kurseve valuta za izračunavanje prodajnih cena od troška, sledite ove korake.

1. Idite na parametre **postavki \> operacija \> projekta**.
1. Otvorite stranicu **Sa detaljima** parametra projekta.
1. Postavite polje **Logika konverzije** valute na praznu vrednost.

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>Ponašanje konverzije valute koje koristi kurseve valuta iz aplikacija za finansije i operacije

Kursevi valuta u tabeli "Valuta" koji su izvorno dostupni Dataverse nisu efektivni. Zbog toga one možda neće uvek biti povećane na zahteve koje imate za obračun prodajnih cena od stope troškova.

Kurseve valuta iz okruženja finansija i operacija možete koristiti za izračunavanje prodajne cene u prodajnoj valuti od kursa troška u valuti troška. Da biste konfigurisali ovo ponašanje konverzije valute, sledite ove korake.

1. Na stranici **"Parametri projekta** " dodajte polje Logika **konverzije valute** . Zatim sačuvajte i objavite prilagođavanje.
1. Idite na parametre **postavki \> operacija \> projekta**.
1. Otvorite stranicu **Sa detaljima** parametra projekta. 
1. Postavite polje Ponašanje **konverzije valute** na prošireno **sa zao jedavljanjem na podrazumevano**.
1. Dajte dozvolu **korisniku aplikacije "** Dual-write bezbednosna uloga **Global Read** " u sledećim tabelama:

    - msdyn\_ valutaexchangerates
    - msdyn\_ currencyexchangeratepairs
    - msdyn\_ exchangeratetypes

1. U okruženju finansija i operacija pokrenite sledeće mape za dvostruko pisanje sa početnom sinhronizacijom:

    - Vrsta kursa valute (msdyn\_ exchangeratetypes)
    - Valutni par kursne valute (msdyn\_ currencyexchangeratepairs)
    - Kursevi VALUTA CDS-a (msdyn\_ currencyexchangerates)

Kada se ove promene završe, dvostruko pisanje će učiniti kurseve iz okruženja finansija i operacija dostupnim u Dataverse. Operacije projekta će zatim koristiti te kurseve za konvertovanje kurseva troškova u prodajnu valutu ugovora.

> [!NOTE]
> Ovo ponašanje konverzije valute primenjuje se samo na obračun prodajnih cena od stope troška. Neće se koristiti za generičko izračunavanje vrednosti osnovne valute. Vrednosti osnovne valute će uvek koristiti osnovne Dataverse kurseve valuta, bez obzira na to da li dovršite ovu proceduru.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
