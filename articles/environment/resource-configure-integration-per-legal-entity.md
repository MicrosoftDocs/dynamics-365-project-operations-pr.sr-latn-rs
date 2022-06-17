---
title: Konfigurisanje integracije za Project Operations po pravnom licu
description: Ovaj članak pruža informacije o podešavanju integracije od strane pravnog lica u projektnim operacijama.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3f33e641ee0932655282618c99a26e2603660059
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914695"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Konfigurisanje integracije za Project Operations po pravnom licu 

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ovaj članak vas vodi kroz korake potrebne za konfigurisanje po Dynamics 365 Project Operations pravnom licu.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Omogući tastere funkcija u Dynamics 365 Finance

Dovršite sledeće korake da biste omogućili potrebne funkcije.

1. U Dynamics 365 Finance, idite na radni **prostor za upravljanje** funkcijama.
2. U odeljku **Lista funkcija**, pronađite i omogućite sledeće funkcije:
  
    - **Omogućite više predmeta ugovora za projekat**
    - **Omogući projektne operacije na Dynamics 365 Customer Engagement**

> [!NOTE]
> Ako ne vidite **Ključne funkcije**, proverite da li vaša verzija usluge Finance ispunjava minimalni zahtev za verziju (verzija aplikacije 10.0.13 sa primenjenim svim ispravkama kvaliteta ili novija). Izaberite **Proveri da li ima ažuriranja** da biste osvežili listu funkcija.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Definišite scenario primene usluge Project Operations za pravno lice

Operacije projekta možete omogućiti Dynamics 365 Customer Engagement na nivou pravnog lica. Možete imati jedno pravno lice koje koristi projektne operacije Dynamics 365 Customer Engagement za scenarije zasnovane na resursima/neodovršenim postavkama. U istom okruženju možete imati drugo pravno lice koje koristi Project Operations za scenarije zasnovane na zalihama/porudžbenicama.

1. U Dynamics 365 Finance, idite na Project **management i accounting** > **Setup Global project** > **management i računovodstvene parametre**.
2. Na listi dostupnih pravnih lica izaberite lica kod kojih će biti omogućeno više redova ugovora i projektnih operacija Dynamics 365 Customer Engagement funkcijama. Nemojte birati pravna lica koja će koristiti Project Operations za scenarije zasnovane na zalihama/porudžbenicama.

> [!NOTE]
> Pravno lice se može odabrati samo ako nema postojeće projekte.

## <a name="configure-project-management-and-accounting-parameters"></a>Konfigurisanje parametara upravljanja projektima i računovodstva

Svakom pravnom licu koje koristi operacije projekta Dynamics 365 Customer Engagement potreban je skup podrazumevanih parametara. Ovi parametri su konfigurisani na kartici **Project Operations** na stranici **Upravljanje projektom i računovodstveni parametri**. Parametri su:

  - **Podrazumevane vrednosti tipova obračuna**: Project Operations koristi fiksni skup podrazumevanih zadataka tipa naplate koji se moraju mapirati sa svojstvima stavki usluge Finance. Napravite zapis za svaku vrstu obračuna: **Nije navedeno**, **Naplativo**, **Nenaplativo**, **Besplatno** i **Nije dostupno**.
  - **Podrazumevane kategorije projekata**: Izaberite podrazumevane kategorije projekata koje će se koristiti za svaku vrstu transakcije. Ove podrazumevane vrednosti će se koristiti u **Project Operations dnevniku integracije** i u procenama gde nije navedena kategorija transakcije za stvarni projekat.
  - **Prognoze**: Izaberite model prognoze koji će se koristiti za procenu vremena i troškova.


[!INCLUDE[footer-include](../includes/footer-banner.md)]