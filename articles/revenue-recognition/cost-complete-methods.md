---
title: Metodi cene za dovršetak
description: Ova tema pruža informacije o metodama koje se koriste za izračunavanje cene za dovršetak projekta.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 790b5c98182acdc0a37e3741a40baf7152f0bf66
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531538"
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
