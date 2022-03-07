---
title: Metodi cene za dovršetak
description: Ova tema pruža informacije o metodama koje se koriste za izračunavanje cene za dovršetak projekta.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fe42ea0e1a5c562ec648fbf2a2924648af80381b9db8ffe0c209cb5247bb2ba2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997983"
---
# <a name="cost-to-complete-methods"></a>Metodi cene za dovršetak

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ova tema pruža informacije o metodama koje se koriste za izračunavanje cene za dovršetak projekta. Postoji više metoda pomoću kojih možete izračunati cene za dovršetak projekta. 

Kada kreirate procenu za projekat, na stranici **Kreiranje procene**, u polju **Metod cene za dovršetak**, možete izabrati jedan od sledećih metoda cene za dovršetak.

| Metod cene za dovršetak    | Opis                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ukupna cena – stvarne vrednosti            | Ručno unesite procenjene cene u polja **Ukupna cena** ili **Ukupna količina** pomoću dugmeta **Procena cene** na **stranici Procena**. Sistem oduzima stvarnu cenu od ukupnih vrednosti koje ste uneli. Ukupne vrednosti su cena za dovršetak projekta. Ovaj metod ne koristi procene troškova i dodeljivanja resursa unetih u Project Operations izgrađene u okviru usluge Microsoft Dataverse. Po potrebi možete ručno ažurirati ukupnu cenu ili ukupnu količinu.  |
| Ukupno predviđanje – stvarne vrednosti        | Dodele resursa i procene troškova koriste se za određivanje ukupnog predviđenog iznosa projekta. Stvarne cene se upoređuju sa ovim predviđanjem radi izračunavanja cene za dovršetak.                                                                                                                                                                                                                                                                          |
| Kao i prethodna procena         | Isti metodi procene koji su korišćeni u prethodnom periodu se koriste ovde. Ova metoda zahteva model predviđanja ako je prethodni period zahtevao model predviđanja.                                                                                                                                                                                                                                                                                                                           |
| Postavljanje troška do završetka na nulu | Obično se koristi pre nego što se projekat procene eliminiše, ovaj metod podudara ukupne procene sa objavljenim stvarnim transakcijama i briše kolonu **Cena za dovršetak**. Po završetku, rezultat je uvek 100 odsto. Za svaku liniju troškova koju kreirate, polje za potvrdu **Predviđanje** se briše i ukupna procena se kopira iz prethodne procene cene. Stvarna potrošnja za procenjeni period oduzima se od troškova za završetak projekta.              |
| Iz predloška troškova           | Metoda cene za dovršetak koja je konfigurisana u predlošku cena koji je povezan sa izabranim projektom procene.                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]