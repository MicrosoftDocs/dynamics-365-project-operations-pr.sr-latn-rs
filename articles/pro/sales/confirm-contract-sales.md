---
title: Potvrdite ugovor za projekat
description: Ova tema pruža informacije o načinu potvrđivanja ugovora u usluzi Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e0ca43eb6005948f440fca16e98a6d05db3493c82e518441bb50f9413da91ead
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989838"
---
# <a name="confirm-a-project-contract"></a>Potvrdite ugovor za projekat

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Ugovor o projektu u usluzi Dynamics 365 Project Operations može biti aktivan uz razlog **Potvrđeno** ili zatvoren uz razlog **Izgubljeno**. Kada potvrdite ugovor o projektu, status se ažurira sa **Radna verzija** na **Aktivno**, a razlog statusa je **Potvrđeno**. Aktivni ili zatvoreni ugovor ne može se uređivati ili ponovo otvarati. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Finansijski uticaj potvrđivanja ugovora za projekat

Nakon što se ugovor za projekat potvrdi, aplikacija će ponovo izračunati troškove storniranjem starijih stvarnih troškova i kreiranjem novih stvarnih troškova. Novi stvarni troškovi se zatim obrađuju na osnovu metode naplate povezanog predmeta ugovora o projektu. Ako se stvarni troškovi odnose na predmet ugovora o vremenu i materijalu, aplikacija automatski ponovo kreira odgovarajuće nenaplaćene stvarne troškove prodaje. Ako se stvarni podaci o troškovima odnose na predmet ugovora sa fiksnom cenom, aplikacija zaustavlja ponovnu obradu stvarnih troškova.

Ograničenja koja se ne smeju premašiti, podešavanje naplativosti i utvrđivanje cena i troškova na stvarnim podacima procenjuju se, a zatim ažuriraju kao deo procesa potvrde.

## <a name="close-a-project-contract-as-lost"></a>Zatvorite ugovor za projekat kao izgubljen

Kada ugovor o projektu zatvorite kao izgubljen, status ugovora se ažurira na **Zatvoreno**, a razlog statusa je **Izgubljeno**. Ugovor o projektu postaje samo za čitanje. Dijalog za potvrdu se navodi pre nego što se promene dovrše jer ne možete ponovo otvoriti zatvoreni ugovor o projektu.

Ako ugovor o projektu koji je zatvoren kao izgubljen upućuje na projekat na svojim stavkama, taj projekat je takođe označen kao zatvoren. Sve rezervacije resursa od tog dana nadalje otkazuju se. Svi nenaplaćeni stvarni troškovi prodaje na ugovoru za projekt koji već nisu na fakturi biće stornirani.

> [!NOTE]
> U usluzi Dynamics 365 Project Operations zatvaranje projektnog ugovora kao izgubljenog neće uticati na taj status povezane mogućnosti. Mogućnost za poslovanje će ostati otvorena i mora se ručno zatvoriti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]