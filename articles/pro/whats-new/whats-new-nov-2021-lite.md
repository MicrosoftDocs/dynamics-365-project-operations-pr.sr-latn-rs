---
title: Šta je novo u novembru 2021. – Project Operations jednostavna primena
description: Ovaj članak pruža informacije o ažuriranjima kvaliteta koja su dostupna u jednostavnoj primena izdanja Project Operations za novembar 2021. godine.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 947e7f6183ddeef3ab9a88d140331956bbcf23bd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913821"
---
# <a name="whats-new-november-2021---project-operations-lite-deployment"></a>Šta je novo u novembru 2021. – Project Operations jednostavna primena

_Odnosi se na: Jednostavna primena – od pogodbe do profakture_

Ovaj članak se odnosi na sledeće komponente i verzije usluge Microsoft Dynamics 365 Project Operations:

- Project Operations u Dataverse okruženju verzije 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
  
## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

Sledeće funkcije su uključene u ovom izdanju:

- Programski interfejsi aplikacije za planiranje projekta (API-ji) sada podržavaju mogućnost kreiranja i brisanja kontejnera projekta

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-in-dataverse"></a>Project Operations u usluzi Dataverse

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Naplata i određivanje cena | 2358236 | Korekcija fakture mora dozvoliti korekcije koje imaju redove sa nultom cenom. |
| Upravljanje resursima | 2410072 | Dozvolite podešavanje resursa koji je dodeljen zadatku kao menadžer projekta. |
| Naplata i određivanje cena | 2430234 | Rešite problem sa izračunavanjem performansi troška. |
| Vreme i trošak | 2436978 | Dozvolite da se vreme unese u čč:mm formatu. |
| Naplata i određivanje cena | 2448623 | Dozvolite ažuriranje cenovnika nakon što su povezani sa organizacionom jedinicom. |
| Vreme i trošak | 2460396 | Dozvolite brisanje unosa vremena brisanjem ćelije. |
| Naplata i određivanje cena | 2467386 | Dozvolite brisanje projekta koji ima zadatak, čak i kada je zadatak povezan sa dobijenom ponudom. |
| Vreme i trošak | 2461744 | Prikaz **Moje neuspelo odobrenje** sadrži samo odobrenja projekata u fazi **Poslato**. |
| Vreme i trošak | 2464082 | Uklonite vezu iz odobrenja projekta sa skupom odobrenja kada se status cilja podudara. |
| Vreme i trošak | 2468108 | Posao planiranja ne bi trebalo da postavi status **U obradi** za skup odobrenja. |
| Vreme i trošak | 2471503 | Izbrišite skupove odobrenja stare sedam dana. |
| Naplata i određivanje cena | 2480687 | Referenca reda na ponudi ne sme biti uklonjena kada se kreira kontrolna tačka reda ponude. |
