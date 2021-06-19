---
title: Tipovi perioda
description: U ovoj temi se pružaju informacije o tome kako da konfigurišete tipove perioda za procenu prihoda.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07cc9cde5fab10accb1fd6efede58926918f614c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013503"
---
# <a name="period-types"></a>Tipovi perioda

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Tip perioda definiše koliko se često procenjuje prihod od projekta. U ovoj temi se pružaju informacije o tome kako da konfigurišete tipove perioda za procenu prihoda. 

## <a name="create-and-work-with-period-types"></a>Kreiranje i rad sa tipovima perioda
Da biste kreirali i radili sa tipovima perioda, izvršite sledeće korake:

1. U Dynamics 365 Finance okruženju, idite na **Upravljanje projektima i računovodstvo** > **Podešavanje** > **Procene** > **Tipovi perioda**.
2. Da biste kreirali novi tip perioda, izaberite **Novo**. Unesite naziv i opis.
3. U polju **Učestalost**, izaberite vrednost:

    - Ako izaberete **sedmica**, **Dvonedeljno**, **Polumesečno**, **Mesec**, **Dan**, **Kvartal** ili **Godina**, kalendar će se koristiti za generisanje perioda. 
    - Ako izaberete **Period knjige**, periodi knjige iz konfiguracije glavne knjige će se koristiti za generisanje perioda.
    - Ako izaberete **Neograničeno**, možete odrediti prilagođene periode.
4. Izaberite zapis tipa perioda, a zatim izaberite **Generiši periode** da biste kreirali periode za tip perioda. Na osnovu učestalosti perioda koju ste izabrali, možda ćete moći da odredite datum početka ili broj perioda koji treba generisati.
5. Izaberite **Periodi** da biste pregledali generisane periode.



[!INCLUDE[footer-include](../includes/footer-banner.md)]