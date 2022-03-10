---
title: Konfigurisanje table rasporeda za prikazivanje radnika po ugovoru i kapaciteta podizvođačima
description: Ovaj tema opisuje kako da konfigurišete Schedule Board u korporaciji Microsoft Dynamics 365 Project Operations da prikaže kapacitet resursa podizvođačem prilikom osoblja zahteva za resurse projekta.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d645dee741a45dcb0219e4e4f58a329b7b873e10
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903754"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Konfigurisanje table rasporeda za prikazivanje radnika po ugovoru i kapaciteta podizvođačima 

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Tabla rasporeda u korporaciji Microsoft Dynamics 365 Project Operations može da se koristi za traženje resursa na dva načina:

- Opšta pretraga resursa bez konteksta bilo kog određenog zahteva resursa zasnovanog na projektu.
- Pretraživanje resursa specifično za zahteve, gde će zahtev za projekat obezbediti kontekst predloženih resursa.

Da biste obavestili odbor rasporeda o kapacitetu resursa podizvođača i radnicima po ugovoru, potrebno je da izvršite ažuriranje postavki Odbora rasporeda. Ove ispravke obuhvataju: 
- Ažurirajte postavke Table rasporeda za opštu pretragu resursa.
- Ažurirajte postavke Table rasporeda za pretraživanje resursa zasnovanih na zahtevima.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Ažuriranje postavki table rasporeda za opšte pretraživanje resursa
### <a name="update-filters-for-general-resource-search"></a>Ažuriranje filtera za opštu pretragu resursa
Kada tražite resurs, filteri dostupni na tabli rasporeda treba da budu ažurirani tako da možete da tražite spoljne resurse tako što ćete navesti neke od sledećih opcija:
  - Vrsta radnika, bez obzira na to da li prikazani resursi treba da budu radnici po ugovoru ili zaposleni.
  - Preduzeće dobavljača kome resurs treba da pripada.
  - Resursi koji pripadaju određenom redu podizvođači ili podizvođači.
    
### <a name="update-retrieve-resource-query"></a>Ažuriranje preuzmi upit resursa
Upit koji se koristi za pretraživanje takođe bi trebalo da bude ažuriran da bi se koristili ovi dodatni atributi filtera. Koristite sledeće korake da biste ažurirali konfiguraciju Schedule Board-a za opšte pretraživanje resursa:  
1. Otvorite **postavke table** rasporeda za određenu tablu rasporeda.
2. Otvorite karticu **Opšte** postavke i pomerite se **do ostalih postavki**.
3. Na listi postavki u ovom odeljku ažurirajte raspored **filtera u** podrazumevani **raspored filtera za operacije projekta Lite**.
4. Ažuriraj **Preuzmi upit resursa** na **podrazumevano preuzimanje upita resursa za operacije projekta Lite**.

![Ažuriranje postavki table rasporeda za opšte pretraživanje resursa](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Ažuriranje postavki Odbora rasporeda za pretraživanje resursa zasnovanog na zahtevima
### <a name="update-filters-for-requirement-specific-resource-search"></a>Ažuriranje filtera za pretraživanje resursa specifičnih za zahtev 
Kada tražite resurs, filteri dostupni na tabli rasporeda treba da budu ažurirani tako da možete da tražite spoljne resurse tako što ćete navesti neke od sledećih opcija:
 - Vrsta radnika, bez obzira na to da li prikazani resursi treba da budu radnici po ugovoru ili zaposleni.
 - Preduzeće dobavljača kome resurs treba da pripada.
 - Resursi koji pripadaju određenom redu podizvođači ili podizvođači.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Ažuriranje preuzmi upit resursa za pretraživanje resursa specifičnog za zahtev 
Upit koji se koristi za pretraživanje takođe bi trebalo da bude ažuriran da bi se koristili ovi dodatni atributi filtera. Koristite sledeće korake da biste ažurirali konfiguraciju Schedule Board-a za pretraživanje resursa zasnovanog na zahtevima:

1. Otvorite **postavke table** rasporeda za određenu tablu rasporeda, a zatim **izaberite stavku Otvori podrazumevane** postavke da biste otvorili postavke za pretragu specifičnu za zahtev.
2. Otvorite karticu **Opšte** postavke i pomerite se **do ostalih postavki**.
3. Na listi postavki u ovom odeljku ažurirajte raspored **filtera u** podrazumevani **raspored filtera za operacije projekta Lite**.
4. Ažuriraj **Preuzmi upit resursa** na **podrazumevano preuzimanje upita resursa za operacije projekta Lite**.
5. Otvorite **karticu Tipovi** rasporeda i idite na **stavku Projekat**.
6. U okviru postavki **za** Project, **ažurirajte Schedule Assistant Retrieve Resources Query** to Default Retrieve Resources Query for Project Operations **Lite and update Schedule Assistant** Retrieve **Constraints Query** to Default Retrieve **Constraints Query for Project Operations Lite**.

![Ažuriranje postavki Odbora rasporeda za pretraživanje resursa zasnovanog na zahtevima](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]