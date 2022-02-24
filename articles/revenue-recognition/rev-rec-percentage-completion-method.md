---
title: Procena prihoda projekata sa fiksnom cenom
description: Ova tema pruža informacije o proceni prihoda sa fiksnom cenom u projektima.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 80fe1d4171d80ca39e8b7ebb1eefaa524a4f2b07
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531540"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Procena prihoda projekata sa fiksnom cenom 

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Kada kreirate predmet projektnog ugovora sa sledećim atributima u usluzi Dynamics 365 Project Operations na platformi Microsoft Dataverse, sistem automatski kreira projekat procene prihoda sa fiksnom cenom. Informacije u ovom projektu zasnivaju se na sledećem:

  - Način obračuna sa fiksnom cenom.
  - Vezani projekat.
  - Najmanje jedna kontrolna tačka definisana na kartici **Raspored faktura** na stranici **Predmet projektnog ugovora**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Pregled procena prihoda projekata sa fiksnom cenom
Da biste pregledali procene prihoda projekata sa fiksnom cenom, dovršite sledeće korake:

1. U Dynamics 365 Finance okruženju, idite na **Upravljanje projektima i računovodstvo** > **Projekti** > **Procena prihoda projekata sa fiksnom cenom**.
2. Izaberite projekat koji želite da prikažete i dvaput kliknite na **ID procene projekta** kako biste otvorili zapis i pregledali detalje projekta.
3. RAzvijte karticu **Projekat**. Videćete jedan projekat u mreži **Izabrani projekti**. Sistem ovo koristi kao podrazumevani projekat, jer je to projekat povezan sa predmetom projektnog ugovora. 
4. Da biste promenili povezivanje, izaberite dodatne projekte i dodajte ih u mrežu **Izabrani projekti**. Ako je u ovoj mreži izabrano više projekata, procenat dovršenja projekta i procene prihoda izračunavaju se zajedno za sve izabrane projekte.

  Trošak projekta, profil prihoda, predložak troškova i kôd perioda mogu se ručno podesiti. Ako ih ne postavite ručno, vrednosti će biti podrazumevane na prvo izračunavanje procene za projekat koristeći pravila konfigurisana za profile troškova i prihoda projekta.

