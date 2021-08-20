---
title: Rezervacije u odnosu na dodele
description: Ova tema pruža informacije o razlikama između rezervisanja resursa i dodeljivanja resursa.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1906ebd76f5fc66215aa5963242de13206a81668cb4973cccaf5b153514672d5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008468"
---
# <a name="bookings-vs-assignments"></a>Rezervacije u odnosu na dodele

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Rezervacije predstavljaju fiksnu ili uslovnu raspodelu resursa za projekat. Fiksne rezervacije troše kapacitet resursa. Rezervacije predstavljaju organizacione koncepte timova kako bi mogli da razumeju kako će se resursi angažovati na različitim projektima. Dynamics 365 Project Operations smatra rezervacije konceptom na nivou projekta. 

Za razliku od rezervacija, dodele predstavljaju obavezivanje resursa za projektne zadatke u rasporedu projekata. Resursi mogu biti imenovani ili generički.  Kada se zahtev za resurs izvede iz dodele projektnog zadatka, Project Operations koristi konture aktivnosti dodele resursa za izradu kontura detalja o zahtevu za resurs. Međutim, pozivanje na dodele resursa se ne održava. Ažuriranja rezervacija izvedenih iz zahteva za resurs ne ažuriraju nijednu dodelu resursa.

Uobičajeno je da je zbir rezervacija za resurs jednak zbiru dodela resursa za jedan ili više zadataka. Međutim, Project Operations ne sprovodi ovaj dogovor. Prikaz **Usaglašenost** pokazuje menadžeru projekata mesta gde se rezervacije i dodele resursa ne slažu.




[!INCLUDE[footer-include](../includes/footer-banner.md)]