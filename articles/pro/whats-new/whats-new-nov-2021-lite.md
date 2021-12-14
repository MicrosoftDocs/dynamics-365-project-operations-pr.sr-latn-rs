---
title: Šta je novi novembar 2021 - Project Operations lite deployment
description: Ovaj tema pruža informacije o kvalitetnim ispravkama koje su dostupne u novembru 2021.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e8560e7c7d6bae1bb2fda389a63bde1c57654bcb
ms.sourcegitcommit: 04ebe764afa22742b3fbf8f12af31e8eea93682e
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/23/2021
ms.locfileid: "7827298"
---
# <a name="whats-new-november-2021---project-operations-lite-deployment"></a>Šta je novi novembar 2021 - Project Operations lite deployment

_Odnosi se na: Jednostavna primena – od pogodbe do profakture_

Ova tema se primenjuje na sledeće komponente i verzije programa Microsoft Dynamics 365 Project Operations:

- Operacije projekta u verziji Dataverse okruženja 4.26.0.145, 4.26.0.148, ili 4.26.0.150
  
## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

Sledeće funkcije su uključene u ovom izdanju:

- Programski interfejsi aplikacija za planiranje projekta (API) sada podržavaju mogućnost kreiranja i brisanja kofa projekta

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-in-dataverse"></a>Projektne operacije u Dataverse

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Naplata i određivanje cena | 2358236 | Korekcija fakture mora dozvoliti korekcije koje imaju redove nulte cene. |
| Upravljanje resursima | 2410072 | Dozvoli podešavanje resursa koji je dodeljen zadatku kao menadžer projekta. |
| Naplata i određivanje cena | 2430234 | Rešite problem sa izračunavanjem performansi troška. |
| Vreme i trošak | 2436978 | Dozvolite da se vreme unese u hh:mm formatu. |
| Naplata i određivanje cena | 2448623 | Dozvoli ažuriranje cenovnika nakon što su povezani sa organizacionom jedinicom. |
| Vreme i trošak | 2460396 | Dozvolite brisanje vremenskog unosa brisanjem ćelije. |
| Naplata i određivanje cena | 2467386 | Dozvolite brisanje projekta koji ima zadatak, čak i kada je zadatak povezan sa izabranom ponudom. |
| Vreme i trošak | 2461744 | Prikaz **"Moje neuspešno** odobravanje" sadrži samo odobrenja projekta u fazi **"Prosleđeno".** |
| Vreme i trošak | 2464082 | Uklonite vezu iz odobravanja projekta sa skupom odobravanja kada se status cilja podudara. |
| Vreme i trošak | 2468108 | Zadatak "Raspored" ne bi trebalo da postavi **status** obrade za skup odobravanja. |
| Vreme i trošak | 2471503 | Izbrišite skupove odobravanja stare sedam dana. |
| Naplata i određivanje cena | 2480687 | Referenca reda ponude ne sme biti uklonjena kada se kreira prekretnica reda ponude. |
