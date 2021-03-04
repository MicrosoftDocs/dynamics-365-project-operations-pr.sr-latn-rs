---
title: Podrazumevane vrednosti finansijske dimenzije
description: Ova tema pruža informacije o načinu postavljanja podrazumevanih vrednosti finansijskih dimenzija.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 03b9a9028c1610b191db9c1bfb0163adc88bdf3e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642380"
---
# <a name="financial-dimension-defaults"></a>Podrazumevane vrednosti finansijske dimenzije

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations koristi radni okvir za [finansijske dimenzije](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) u usluzi Dynamics 365 Finance kako bi pružio dodatni uvid u transakcije potknjige i glavne knjige.

Podrazumevane finansijske dimenzije mogu se postaviti na osnovu klijenta, izvora finansiranja projekta, kontrolne tačke, predmeta ugovora za projekat ili projekta.

## <a name="define-default-financial-dimensions-for-a-customer"></a>Definisanje podrazumevanih finansijskih dimenzija za klijenta

Podrazumevane vrednosti za dimenziju klijenta navedene su u usluzi Finance. Dovršite sledeće korake da biste podesili podrazumevane vrednosti dimenzija.

1. Idite na **Potraživanja** > **Klijenti** > **Svi klijenti**.
2. Na stranici **Klijenti**, na kartici **Finansijske dimenzije**, podesite vrednosti finansijskih dimenzija za određenog klijenta.

## <a name="define-default-financial-dimensions-for-project-contracts"></a>Definisanje podrazumevanih finansijskih dimenzija za ugovore za projekat

Ugovori za projekat se kreiraju i održavaju u usluzi Common Data Service (CDS). Atributi računovodstva za ugovore za projekat postavljeni su u modul **Upravljanje projektima i računovodstvo** u usluzi Finance.

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>Podesite finansijske dimenzije za izvor finansiranja projekta

1. Idite na **Upravljanje projektima i računovodstvo** > **Projekti** > **Ugovori za projekat**.
2. Izaberite zapis koji želite da ažurirate, a zatim na kartici **Ugovor o projektu** izaberite **Prikaži podrazumevano računovodstvo**.
3. Proširite **Srodne informacije** i izaberite karticu **Izvori finansiranja**.
4. Podesite podrazumevane vrednosti finansijskih dimenzija. Imajte u vidu da se podrazumevane vrednosti finansijskih dimenzija uzimaju sa naloga klijenta.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Podesite finansijske dimenzije za predmet ugovora za projekat

1. Idite na **Upravljanje projektima i računovodstvo** > **Projekti** > **Ugovori za projekat**.
2. Izaberite zapis koji želite da ažurirate, a zatim na kartici **Ugovor o projektu** izaberite **Prikaži podrazumevano računovodstvo**.
3. Proširite **Srodne informacije** i izaberite karticu **Predmeti ugovora**.
4. Podesite podrazumevane vrednosti finansijskih dimenzija. Podrazumevane finansijske dimenzije su primenljive i mogu se koristiti samo sa predmetima ugovora sa fiksnom cenom (kontrolnom tačkom).

Ove podrazumevane vrednosti se koriste za povezane transakcije za poslovnog klijenta na projektu i stavke faktura.

## <a name="define-default-financial-dimensions-for-projects"></a>Definisanje podrazumevanih finansijskih dimenzija za projekte

Projekti se kreiraju i održavaju u usluzi CDS. Atributi računovodstva za projekat postavljeni su u modul **Upravljanje projektima i računovodstvo** u usluzi Finance.

1. Idite na **Upravljanje projektima i računovodstvo** > **Projekti** > **Svi projekti**.
2. Izaberite zapis koji želite da ažurirate, a zatim na kartici **Projekat** izaberite **Prikaži podrazumevano računovodstvo**.
3. Proširite **Srodne informacije** i izaberite karticu **Podešavanje**.
4. Podesite podrazumevane vrednosti finansijskih dimenzija. Imajte u vidu da se podrazumevane vrednosti finansijskih dimenzija uzimaju sa naloga klijenta. Ako je projekat povezan sa predmetom ugovora sa više klijenata ugovora za projekat, primarni klijent se koristi za podrazumevane finansijske dimenzije.

Podrazumevane finansijske dimenzije projekta koriste se za postavljanje podrazumevanih vrednosti stavke u glavnoj knjizi za transakcije vremena, troškova i naknada u **Project Operations dnevniku integracije** i na povezanim stavkama fakture projekta.


[!INCLUDE[footer-include](../includes/footer-banner.md)]