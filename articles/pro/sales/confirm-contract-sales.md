---
title: Potvrdite ugovor za projekat
description: Ova tema pruža informacije o načinu potvrđivanja ugovora u usluzi Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: babce9c64098a9c87072786d914d2340251a8986
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083700"
---
# <a name="confirm-a-project-contract"></a>Potvrdite ugovor za projekat

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Ugovor za projekat u programu Dynamics 365 Project Operations može biti aktivan sa razlogom **Potvrđeno** ili zatvoren sa razlogom **Izgubljeno**. Kada potvrdite ugovor o projektu, status se ažurira sa **Radna verzija** na **Aktivno** , a razlog statusa je **Potvrđeno**. Aktivni ili zatvoreni ugovor ne može se uređivati ili ponovo otvarati. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Finansijski uticaj potvrđivanja ugovora za projekat

Nakon što se ugovor za projekat potvrdi, aplikacija će ponovo izračunati troškove storniranjem starijih stvarnih troškova i kreiranjem novih stvarnih troškova. Novi stvarni troškovi se zatim obrađuju na osnovu metode naplate povezanog predmeta ugovora o projektu. Ako se stvarni troškovi odnose na predmet ugovora o vremenu i materijalu, aplikacija automatski ponovo kreira odgovarajuće nenaplaćene stvarne troškove prodaje. Ako se stvarni podaci o troškovima odnose na predmet ugovora sa fiksnom cenom, aplikacija zaustavlja ponovnu obradu stvarnih troškova.

Ograničenja koja se ne smeju premašiti, podešavanje naplativosti i utvrđivanje cena i troškova na stvarnim podacima procenjuju se, a zatim ažuriraju kao deo procesa potvrde.

## <a name="close-a-project-contract-as-lost"></a>Zatvorite ugovor za projekat kao izgubljen

Kada ugovor o projektu zatvorite kao izgubljen, status ugovora se ažurira na **Zatvoreno** , a razlog statusa je **Izgubljeno**. Ugovor o projektu postaje samo za čitanje. Dijalog za potvrdu se navodi pre nego što se promene dovrše jer ne možete ponovo otvoriti zatvoreni ugovor o projektu.

Ako ugovor o projektu koji je zatvoren kao izgubljen upućuje na projekat na svojim stavkama, taj projekat je takođe označen kao zatvoren. Sve rezervacije resursa od tog dana nadalje otkazuju se. Svi nenaplaćeni stvarni troškovi prodaje na ugovoru za projekt koji već nisu na fakturi biće stornirani.

> [!NOTE]
> U usluzi Dynamics 365 Project Operations, zatvaranje ugovora o projektu kao izgubljenog neće uticati na taj status povezane mogućnosti za poslovanje. Mogućnost za poslovanje će ostati otvorena i mora se ručno zatvoriti.
