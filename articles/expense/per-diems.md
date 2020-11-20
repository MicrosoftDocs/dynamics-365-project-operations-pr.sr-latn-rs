---
title: Dnevnice
description: Ova tema pruža informacije o pravilima dnevnica koja se koriste u upravljanju troškovima.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 8d723b49e9556401c364b323cf58eaaf44906275
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128525"
---
# <a name="per-diems"></a>Dnevnice

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_


Dnevnica je nadoknada koja se isplaćuje radniku koji putuje zbog posla. U upravljanju troškovima možete kreirati pravila za dnevnice za različite situacije putovanja. Iznosi dnevnica mogu se zasnivati na dobu godine, lokaciji putovanja ili oboje. Kada kreirate pravilo za dnevnicu, možete da odredite da se procenat dnevnice zadržava ako radnik dobije besplatne obroke ili usluge. Takođe možete da odredite minimalni i maksimalni broj sati za koji dnevnica može da se primenjuje na putovanje radnika.

## <a name="configuration"></a>Konfigurisanje 

1. Da biste dodali lokacije za dnevnice, idite na **Podešavanje** > **Proračuni i šifre** > **Lokacije za dnevnice**.
2. Za svaku od gore dodatih lokacija izaberite iznos dnevnice i valutu koja važi između određenog datuma početka i završetka za hotel, obroke i ostale troškove. Stope dnevnica i valute su konfigurisane u odeljku **Podešavanje** > **Proračuni i šifre** > **Dnevnice**.
3. Na stranici **Lokacije za dnevnice**, konfigurišite nivoe iznosa dnevnica. Nivoi iznosa dnevnica omogućavaju vam da definišete procentualnu podelu dnevne nadoknade za hotel, obroke i druge troškove. 
4. Da biste odredili smanjenje procenta obroka za doručak, ručak ili večeru, ažurirajte polja na stranici **Parametri upravljanja troškovima** na kartici **Dnevnice**. 
    
## <a name="submit-expenses-using-per-diem"></a>Prosleđivanje troškova korišćenjem dnevnica
Da biste prosledili troškove koristeći dnevnice, koristite kategoriju troška **Dnevnica** kada kreirate izveštaj o troškovima. Unesite **početni datum dnevnice**, **krajnji datum dnevnice** i **lokaciju dnevnice**. Iznos će se izračunati na osnovu iznosa dnevnice za izabranu lokaciju, a smanjenje obroka na osnovu nivoa dnevnica.
