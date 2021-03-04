---
title: Konfigurisanje integracije za Project Operations po pravnom licu
description: Ova tema pruža informacije o tome kako da podesite integraciju po pravnom licu u usluzi Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5d2bb415362a088e01253fbe54f9f06569b4a921
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122900"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Konfigurisanje integracije za Project Operations po pravnom licu 

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ova tema vas vodi kroz korake potrebne za konfigurisanje usluge Dynamics 365 Project Operations po pravnom licu.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Omogućite ključne funkcije u usluzi Dynamics 365 Finance

Dovršite sledeće korake da biste omogućili potrebne funkcije.

1. U usluzi Dynamics 365 Finance idite na radni prostor **Upravljanje podacima**.
2. U odeljku **Lista funkcija**, pronađite i omogućite sledeće funkcije:
  
    - **Omogućite više predmeta ugovora za projekat**
    - **Omogućite Project Operations u usluzi Dynamics 365 Customer Engagement**

> [!NOTE]
> Ako ne vidite **Ključne funkcije**, proverite da li vaša verzija usluge Finance ispunjava minimalni zahtev za verziju (verzija aplikacije 10.0.13 sa primenjenim svim ispravkama kvaliteta ili novija). Izaberite **Proveri da li ima ažuriranja** da biste osvežili listu funkcija.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Definišite scenario primene usluge Project Operations za pravno lice

Project Operations možete da omogućite u usluzi Dynamics 365 Customer Engagement na nivou pravnog lica. Možete da imate jedno pravno lice koje koristi Project Operations u usluzi Dynamics 365 Customer Engagement za scenarije zasnovane na resursima/koji nisu zasnovani na zalihama. U istom okruženju možete imati drugo pravno lice koje koristi Project Operations za scenarije zasnovane na zalihama/porudžbenicama.

1. U usluzi Dynamics 365 Finance idite na **Upravljanje projektima i računovodstvo** > **Podešavanje** > **Globalno upravljanje projektima i računovodstveni parametri**.
2. Na listi dostupnih pravnih lica izaberite entitete u kojima će biti omogućeno više predmeta ugovora i funkcije Project Operations u usluzi Dynamics 365 Customer Engagement. Nemojte birati pravna lica koja će koristiti Project Operations za scenarije zasnovane na zalihama/porudžbenicama.

> [!NOTE]
> Pravno lice se može odabrati samo ako nema postojeće projekte.

## <a name="configure-project-management-and-accounting-parameters"></a>Konfigurisanje parametara upravljanja projektima i računovodstva

Svako pravno lice koje koristi Project Operations u usluzi Dynamics 365 Customer Engagement mora da ima skup podrazumevanih parametara. Ovi parametri su konfigurisani na kartici **Project Operations** na stranici **Upravljanje projektom i računovodstveni parametri**. Parametri su:

  - **Podrazumevane vrednosti tipova obračuna**: Project Operations koristi fiksni skup podrazumevanih zadataka tipa naplate koji se moraju mapirati sa svojstvima stavki usluge Finance. Napravite zapis za svaku vrstu obračuna: **Nije navedeno**, **Naplativo**, **Nenaplativo**, **Besplatno** i **Nije dostupno**.
  - **Podrazumevane kategorije projekata**: Izaberite podrazumevane kategorije projekata koje će se koristiti za svaku vrstu transakcije. Ove podrazumevane vrednosti će se koristiti u **Project Operations dnevniku integracije** i u procenama gde nije navedena kategorija transakcije za stvarni projekat.
  - **Prognoze**: Izaberite model prognoze koji će se koristiti za procenu vremena i troškova.


[!INCLUDE[footer-include](../includes/footer-banner.md)]