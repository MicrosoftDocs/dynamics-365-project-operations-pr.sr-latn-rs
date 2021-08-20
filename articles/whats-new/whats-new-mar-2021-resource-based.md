---
title: Šta je novo u martu 2021. – Project Operations za scenarije zasnovane na resursima/bez zaliha
description: Ova tema pruža informacije o ispravkama kvaliteta dostupnim u izdanju usluge Project Operations za mart 2021. za scenarije zasnovane na resursima/bez zaliha.
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b11a57ae152be154fd6a7d330c8520f3b295ce3ef5cc7051ac9b343e3bcdbe12
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006353"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Šta je novo u martu 2021. – Project Operations za scenarije zasnovane na resursima/bez zaliha

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ova tema se odnosi na sledeće komponente i verzije usluge Dynamics 365 Project Operations:

- Project Operations u Dataverse okruženju verzije 4.8.0.91 
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzije 10.0.16 

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-on-dataverse"></a>Project Operations u usluzi Dataverse


| **Oblast funkcija** | **Referentni broj** | **Ispravka kvaliteta** |
| --- | --- | --- |
| Naplata i određivanje cena | 2133873 | Popravljen je prikaz simbola valute **Prodajna cena po jedinici** na mreži **Procene troškova**. |
| Naplata i određivanje cena | 2174616 | Kada se osvoji ponuda, prilagođeni cenovnik ugovora navodi se u detaljima o predmetu ugovora koji se kopiraju iz ponude. |
| Upravljanje mogućnostima za poslovanje | 2167475 | Popravljen je iznos poreza u fakturi za korekciju koji je pokretao nefakturisani stvarni unos. |
| Upravljanje mogućnostima za poslovanje | 2176285 | Iznos poreza ne sme se kopirati iz detalja ugovora o prodaji/stavke ponude u detalje ugovora o ceni/stavke ponude. |
| Upravljanje mogućnostima za poslovanje | 2188079 | Pravilo deljene naplate ne sme se kreirati za ugovore koji nisu zasnovani na poslu. |
| Planiranje i praćenje | 2125274 | Atribut **Projektovanje mape sa dvostrukim upisivanjem** za **Mapiranje datuma početka projekta** ažurirano je sa **msdyn\_taskearlieststart** na **msdyn\_actualstart**. |
| Planiranje i praćenje | 2138853 | Ažurirana je funkcija kopiranja projekta kako bi se osiguralo da se linije procene troškova koje upućuju na zadatke kopiraju u odredišni projekat. |
| Planiranje i praćenje | 2154306 | Rešeni su problemi sa brisanjem procena troškova u usluzi Project Operations za scenarije zasnovane na resursima. |
| Planiranje i praćenje | 2173259 | Ažurirana je funkcija kopiranja projekta kako bi se osiguralo da ne prikazuje poruku o grešci **Kopiranje SAP-a** u određenim scenarijima. |
| Vreme i trošak | 2148910 | Ispravljen je problem sa prikazom stranice **Izmena unosa** na mreži **Stavka vremena**. |
| Vreme i trošak | 2159798 | Pojačane su kontrole kako bi se osiguralo da se odobreni unosi troškova ne mogu uređivati. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Upravljanje projektima i računovodstvo u usluzi Dynamics 365 Finance

Dodatne informacije potražite u odeljku [Šta je novo u januaru 2021. – Project Operations za scenarije zasnovane na resursima/bez zaliha](whats-new-jan-2021-resource-based.md).

## <a name="regulatory-updates"></a>Regulatorne ispravke

Za informacije o regulatornim ispravkama za Finance and Operations aplikacije, pogledajte članak [Regulatorne ispravke](/dynamics365/finance/localizations/regulatory-updates). Drugi način da saznate više o regulatornim ispravkama je da se prijavite na LCS i pregledate planirane regulatorne ispravke pomoću alatke za pretragu problema. Pretraga problema vam omogućava pretragu po zemlji, tipu funkcije i izdanju.


[!INCLUDE[footer-include](../includes/footer-banner.md)]