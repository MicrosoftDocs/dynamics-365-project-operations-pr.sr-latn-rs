---
title: Bezbednost i odobrenja
description: Ovaj članak pruža informacije o bezbednosnom podešavanju za rad sa odobrenjima u rešenju Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 0dcadaa142bf46e4c54f160759602ac749022108
ms.sourcegitcommit: 73aff2b3c5e5b8a2254735b0b25931cbb6754c87
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709415"
---
# <a name="security-and-approvals"></a>Bezbednost i odobrenja

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Microsoft Dynamics 365 Project Operations koristi dve bezbednosne uloge da bi dozvolio odobrenje stavki vremena, troškova i materijala:

- Davalac odobrenja za projekat
- Administrator davaoca odobrenja za projekat

## <a name="project-approver"></a>Davalac odobrenja za projekat

Morate imati bezbednosnu ulogu **Davalac odobrenja za za projekat** da biste odobrili stavke vremena projekta, troškova i materijala. Takođe morate imati pristup relevantnim srodnim entitetima, kao što je **Projekat**. Taj pristup može da vam dodeli neko ko ima ulogu **Menadžera projekta**. Pored toga, morate biti član projektnog tima i označeni kao davalac odobrenja.

Da biste odobrili stavke koje nisu projektne, morate biti menadžer podnosioca zahteva.

## <a name="project-approver-admin"></a>Administrator davaoca odobrenja za projekat

> [!NOTE]
> Funkcija [Skupovi odobrenja](approval-sets.md) mora biti omogućena pre nego što možete da koristite funkcionalnost administratora davaoca odobrenja za projekat.

Bezbednosna uloga **Administrator davaoca odobrenja za projekat** omogućava korisnicima da zaobiđu smernice i omogućava odobravanje stavki u svim projektima. Dodeljivanje ove uloge će zaobići logiku provere valjanosti koja zahteva članstvo u timu i oznaku da ste davalac odobrenja. Morate imati pristup relevantnim povezanim tabelama, kao što je **Projekat**, putem bezbednosnih uloga koje su vam dodeljene.

Kontekst SISTEMSKOG korisnika zaobilazi provere valjanosti na isti način kao i bezbednosna uloga administratora davaoca odobrenja za projekat.
