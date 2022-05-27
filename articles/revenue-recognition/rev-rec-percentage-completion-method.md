---
title: Procena prihoda projekata sa fiksnom cenom
description: Ova tema pruža informacije o proceni prihoda sa fiksnom cenom u projektima.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 290608e5663f9c953212c156771bbf1ad6b1e901
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578725"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Procena prihoda projekata sa fiksnom cenom 

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Kada kreirate predmet projektnog ugovora sa sledećim atributima u usluzi Dynamics 365 Project Operations na platformi Microsoft Dataverse, sistem automatski kreira projekat procene prihoda sa fiksnom cenom. Informacije u ovom projektu zasnivaju se na sledećem:

  - Način obračuna sa fiksnom cenom.
  - Vezani projekat.
  - Najmanje jedna kontrolna tačka definisana na kartici **Raspored faktura** na stranici **Predmet projektnog ugovora**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Pregled procena prihoda projekata sa fiksnom cenom
Da biste pregledali procene prihoda projekata sa fiksnom cenom, dovršite sledeće korake:

1. U okruženju Dynamics 365 Finance, idite na projekte upravljanja **projektima i knjigovodstvenih** > **projekata** > **Fiksna procena prihoda od cena**.
2. Izaberite projekat koji želite da prikažete i dvaput kliknite na **ID procene projekta** kako biste otvorili zapis i pregledali detalje projekta.
3. RAzvijte karticu **Projekat**. Videćete jedan projekat u mreži **Izabrani projekti**. Sistem ovo koristi kao podrazumevani projekat, jer je to projekat povezan sa predmetom projektnog ugovora. 
4. Da biste promenili povezivanje, izaberite dodatne projekte i dodajte ih u mrežu **Izabrani projekti**. Ako je u ovoj mreži izabrano više projekata, procenat dovršenja projekta i procene prihoda izračunavaju se zajedno za sve izabrane projekte.

  Trošak projekta, profil prihoda, predložak troškova i kôd perioda mogu se ručno podesiti. Ako ih ne postavite ručno, vrednosti će biti podrazumevane na prvo izračunavanje procene za projekat koristeći pravila konfigurisana za profile troškova i prihoda projekta.



[!INCLUDE[footer-include](../includes/footer-banner.md)]