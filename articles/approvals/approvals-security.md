---
title: Bezbednost i odobrenja
description: Ovaj članak pruža informacije o bezbednosnom podešavanju za rad sa odobrenjima korporacije Microsoft Dynamics 365 Project Operations.
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

Microsoft Dynamics 365 Project Operations koristi dve bezbednosne uloge da bi dozvolio odobravanje stavki vremena, troškova i materijala:

- Davalac odobrenja za projekat
- Administrator projekta koji vrši odobravanje

## <a name="project-approver"></a>Davalac odobrenja za projekat

Morate imati datume koji **vrše bezbednosna uloga** da biste odobrili vreme projekta, troškove i stavke materijala. Takođe morate imati pristup relevantnim povezanim entitetima, kao što je "Projekat **"**. Taj pristup može da dodeli neko ko ima ulogu Menadžera **projekta**. Pored toga, morate biti član tima projekta i označeni kao osoba koja vrši odobravanje.

Da biste odobrili stavke koje nisu projektne, morate biti menadžer prosledioca.

## <a name="project-approver-admin"></a>Administrator projekta koji vrši odobravanje

> [!NOTE]
> Funkcija [skupova odobravanja](approval-sets.md) mora biti omogućena da biste mogli da koristite funkcionalnost administratora koji vrši odobravanje projekta.

Administrator **smernica za odobravanje** bezbednosna uloga omogućava korisnicima da zaobiđu smernice i omogućava odobravanje stavki u svim projektima. Dodeljivanje ove uloge će zaobići logiku provere valjanosti koja zahteva članstvo u timu i biti označena kao osoba koja vrši odobravanje. Morate imati pristup relevantnim povezanim tabelama, kao što je "Projekat **",** putem bezbednosnih uloga koje su vam dodeljene.

Kontekst korisnika sistema zaobilazi provere valjanosti na isti način kao i administrator administratora koji vrši bezbednosna uloga.
