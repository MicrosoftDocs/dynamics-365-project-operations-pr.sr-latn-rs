---
title: Najčešća pitanja o upravljanju resursima
description: Ova tema nudi odgovore na najčešća pitanja o upravljanju resursima.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 395aa57d73e5d4a0c9c827c79bf4e7ef229c3981
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083791"
---
# <a name="resource-management-faq"></a>Najčešća pitanja o upravljanju resursima

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>Koja je razlika između člana tima i potrebe za resursom?

Član projektnog tima može biti dodeljen zadacima, rezervisan ili prebukiran, kao i podešen kao davalac odobrenja. Potreba za resursom može postojati bez člana projektnog tima, kao radna verzija napomene o potražnji. 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>Koja je razlika između predloženih i uslovno rezerviranih sati?

Predloženi sati i uslovno rezervisani sati razlikuju se po vidljivosti. Predloženi sati su vidljivi samo menadžerima resursa i menadžeru projekata koji su pokrenuli potražnju koristeći zahtev za resurs. Uslovno rezervisani sati su vidljivi svima koji imaju pristup tabeli rasporeda.

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>Kako mogu da vidim uslovno rezervisane sate za resurse u timu?

Uslovne rezervacije možete da obavite kada rezervišete potrebu za resursom. Resursi koji su uslovno rezervisani u projektnom timu prikazuju se kao članovi tima koji imaju uslovno rezervisane sate. Prikazuju se i na tabeli rasporeda.

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>Kako da promenim zahtevane sate, datum početka i završetka za (generički ili imenovani) resurs koji je rezervisan?

Nakon rezervisanja resursa, izaberite **Održavanje rezervacija** da unesete promene koje su neophodne.

## <a name="what-resources-types-does-project-service-automation-support"></a>Koje vrste resursa podržava Project Service Automation?

**Korisnik** i **Kontakt** su jedine vrste resursa koje podržava Dynamics 365 Project Service Automation. Iako možete da kreirate druge vrste resursa (na primer, **Oprema** i **Grupa** ), nijedan slučaj njihovog kompletnog korišćenja nije podržan.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>Koja je razlika između dodele i rezervacije?

Dodele predstavljaju dodele resursa projektnim zadacima u rasporedu projekata. Resursi mogu biti stvarni ili generički resursi. Rezervacije predstavljaju fiksnu ili uslovnu raspodelu resursa za projekat. Fiksne rezervacije troše kapacitet resursa. Idealno bi bilo da se za stvarne resurse slažu rezervacije i dodele, jer se ne razlikuju. Međutim, PSA ne sprovodi ovaj dogovor. Prikaz Usaglašenost pokazuje menadžeru projekata mesta gde se rezervacije i dodele resursa ne slažu.
