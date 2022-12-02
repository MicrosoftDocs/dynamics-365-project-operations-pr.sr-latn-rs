---
title: Konfigurisanje tabele rasporeda za prikazivanje radnika po ugovoru i kapaciteta podizvođača
description: Ovaj članak opisuje kako da konfigurišete Tablu rasporeda u usluzi Microsoft Dynamics 365 Project Operations da biste prikazali podugovoreni kapacitet prilikom određivanja osoblja za zahteve za resursima.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 355691b63f437de789afab499369afcdf87e6d3d
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262234"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Konfigurisanje tabele rasporeda za prikazivanje radnika po ugovoru i kapaciteta podizvođača 

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Tabla rasporeda u usluzi Microsoft Dynamics 365 Project Operations može da se koristi za pretragu resursa na dva načina:

- Opšta pretraga resursa bez konteksta bilo kog određenog zahteva za resursom zasnovanog na projektu.
- Pretraga resursa specifična za zahteve, gde će zahtev za projekat obezbediti kontekst predloženih resursa.

Da biste obavestili tablu rasporeda o kapacitetu podugovorenih resursa i radnicima po ugovoru, potrebno je da izvršite ažuriranje postavki Table rasporeda. Ova ažuriranja obuhvataju: 
- Ažuriranje postavki Table rasporeda za opštu pretragu resursa.
- Ažuriranje postavki Table rasporeda za pretragu resursa zasnovanu na zahtevima

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Ažuriranje postavki Table rasporeda za opštu pretragu resursa
### <a name="update-filters-for-general-resource-search"></a>Ažuriranje filtera za opštu pretragu resursa
Kada tražite resurs, filteri dostupni na tabli rasporeda treba da budu ažurirani tako da možete da tražite spoljne resurse tako što ćete navesti neke ili sve sledeće opcije:
  - Vrsta radnika, bez obzira na to da li prikazani resursi treba da budu radnici po ugovoru ili zaposleni.
  - Preduzeće dobavljača kojem bi trebalo da pripada resurs.
  - Resursi koji pripadaju određenom podugovoru ili predmetu podugovora.
    
### <a name="update-retrieve-resource-query"></a>Ažuriranje upita o preuzimanju resursa
Upit koji se koristi za pretragu takođe bi trebalo da bude ažuriran za korišćenje ovih dodatnih atributa filtera. Koristite sledeće korake da biste ažurirali konfiguraciju Table rasporeda za opštu pretragu resursa:  
1. Otvorite **Postavke Table rasporeda** za određenu Tablu rasporeda.
2. Otvorite karticu **Opšte postavke** i idite do **Ostalih postavki**.
3. Na listi postavki u ovom odeljku ažurirajte **Raspored filtera** u **Podrazumevani raspored filtera za Project Operations jednostavna primena**.
4. Ažurirajte **Preuzmi upit za resurs** na **Podrazumevano preuzmi upit za resurs za Project Operations jednostavnu primenu**.

![Ažuriranje postavki Table rasporeda za opštu pretragu resursa](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Ažuriranje postavki Table rasporeda za pretragu resursa zasnovanu na zahtevima
### <a name="update-filters-for-requirement-specific-resource-search"></a>Ažuriranje filtera za pretragu resursa sa određenim zahtevima 
Kada tražite resurs, filteri dostupni na tabli rasporeda treba da budu ažurirani tako da možete da tražite spoljne resurse tako što ćete navesti neke ili sve sledeće opcije:
 - Vrsta radnika, bez obzira na to da li prikazani resursi treba da budu radnici po ugovoru ili zaposleni.
 - Preduzeće dobavljača kojem bi trebalo da pripada resurs.
 - Resursi koji pripadaju određenom podugovoru ili predmetu podugovora.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Ažuriranje preuzimanje upita za resurs za pretragu resursa sa određenih zahtevima 
Upit koji se koristi za pretragu takođe bi trebalo da bude ažuriran za korišćenje ovih dodatnih atributa filtera. Koristite sledeće korake da biste ažurirali konfiguraciju Table rasporeda za pretragu resursa sa određenim zahtevima:

1. Otvorite **Postavke Table rasporeda** za određenu Tablu rasporeda, a zatim izaberite stavku **Otvori podrazumevane postavke** da biste otvorili postavke za pretragu sa određenim zahtevima.
2. Otvorite karticu **Opšte postavke** i idite do **Ostalih postavki**.
3. Na listi postavki u ovom odeljku ažurirajte **Raspored filtera** u **Podrazumevani raspored filtera za Project Operations jednostavna primena**.
4. Ažurirajte **Preuzmi upit za resurs** na **Podrazumevano preuzmi upit za resurs za Project Operations jednostavnu primenu**.
5. Otvorite karticu **Tipovi rasporeda** i idite u **Projekat**.
6. U okviru postavki za **Projekat**, ažurirajte **Upit o preuzimanju resursa pomoćnika za zakazivanje** na **Podrazumevani upit o preuzimanju resursa za Project Operations jednostavnu primenu** i ažurirajte **Upit o ograničenjima resursa pomoćnika za zakazivanje** na **Podrazumevani upit o ograničenjima preuzimanja resursa za Project Operations jednostavnu primenu**.

![Ažuriranje postavki Table rasporeda za pretragu resursa zasnovanu na zahtevima](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
