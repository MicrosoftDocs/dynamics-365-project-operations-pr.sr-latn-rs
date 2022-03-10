---
title: Šta je novi novembar 2021 - Project Operations lite deployment
description: Ovaj tema pruža informacije o kvalitetnim ispravkama koje su dostupne u novembru 2021.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0fd910fb1b1e4e4576afa386a600e56e6f2dd504
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942948"
---
# <a name="whats-new-november-2021---project-operations-lite-deployment"></a>Šta je novi novembar 2021 - Project Operations lite deployment

_Odnosi se na: Jednostavna primena – od pogodbe do profakture_

Ova tema se odnosi na sledeće komponente i verzije korporacije Dynamics 365 Project Operations Microsoft:

- Operacije projekta u Dataverse verziji okruženja 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
  
## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

Sledeće funkcije su uključene u ovom izdanju:

- Programski interfejsi aplikacija za planiranje projekta (API) sada podržavaju mogućnost kreiranja i brisanja kofa projekta

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-in-dataverse"></a>Operacije projekta u Dataverse

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
