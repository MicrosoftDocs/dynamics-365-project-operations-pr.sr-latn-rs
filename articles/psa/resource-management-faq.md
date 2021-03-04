---
title: Najčešća pitanja o upravljanju resursima
description: Ova tema nudi odgovore na najčešća pitanja o upravljanju resursima.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: d335a12a9b478bff63b6c93809c89dac9718a4be
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144385"
---
# <a name="resource-management-faq"></a>Najčešća pitanja o upravljanju resursima

[!include [banner](../includes/psa-now-project-operations.md)]

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

**Korisnik** i **Kontakt** su jedine vrste resursa koje podržava Dynamics 365 Project Service Automation. Iako možete da kreirate druge vrste resursa (na primer, **Oprema** i **Grupa**), nijedan slučaj njihovog kompletnog korišćenja nije podržan.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>Koja je razlika između dodele i rezervacije?

Dodele predstavljaju dodele resursa projektnim zadacima u rasporedu projekata. Resursi mogu biti stvarni ili generički resursi. Rezervacije predstavljaju fiksnu ili uslovnu raspodelu resursa za projekat. Fiksne rezervacije troše kapacitet resursa. Idealno bi bilo da se za stvarne resurse slažu rezervacije i dodele, jer se ne razlikuju. Međutim, PSA ne sprovodi ovaj dogovor. Prikaz Usaglašenost pokazuje menadžeru projekata mesta gde se rezervacije i dodele resursa ne slažu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]