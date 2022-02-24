---
title: Kopiranje projekta
description: Ova tema pruža informacije o kopiranju projekata u usluzi Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479536"
---
# <a name="copy-a-project"></a>Kopiranje projekta

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Uz Dynamics 365 Project Operations, možete brzo da pravite nove projekte izborom opcije **Kopiraj projekat** u obrascu **Projekti**. Da biste kopirali projekat, otvorite projekat koji želite da kopirate, a zatim izaberite **Kopiraj projekat**. Radnja će kopirati:

- Svojstva projekta (procenjeni datum početka se kopira iz izvornog projekta)
- Strukturnu analizu posla
- Članovi projektnog tima
- Procene za projekat
- Procene troškova projekta

## <a name="project-properties"></a>Svojstva projekta

Kada se projekat kopira, kopiraju se vrednosti u sledećim poljima:

- +Ime
- Opis
- Klijent
- Predložak kalendara
- Valuta
- Jedinica ugovaranja
- Menadžer projekta
- Status
- Ukupan status projekta
- Komentari
- Procene
- Procenjeni datum početka
- Datum završetka
- Angažovanje (časovi)
- Procenjeni troškovi rada
- Procenjeni iznos troškova

## <a name="work-breakdown-structure"></a>Strukturna analiza posla

Kada se projekat kopira, kopira se celokupna strukturna analiza posla učitanog resursa. Imenovani resurs zamenjuje generičke resurse. Ako imenovani resursi nemaju isto radno vreme kao generički resurs, raspored će se ponovo izračunati i trajanje zadatka se može promeniti.

## <a name="project-team-members"></a>Članovi projektnog tima

Kada se projektni tim kopira iz izvornog projekta, kopiraju se generički resursi. Dodele generičkih resursa takođe se održavaju kao u izvornom projektu. Imenovani resursi će se pretvoriti u generičke članove tima.

## <a name="estimates"></a>Procene

Kada se projekat kopira, iz izvornog projekta se kopiraju i stavke procene resursa i troškova. 

Za informacije o tome kako programski pristupiti opciji Kopiraj projekat, pogledajte [Razvijajte predloške projekata pomoću opcije Kopiraj projekat](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
