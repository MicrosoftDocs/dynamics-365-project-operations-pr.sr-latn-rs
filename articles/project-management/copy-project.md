---
title: Kopiranje projekta
description: Ova tema pruža informacije o kopiranju projekata u usluzi Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e35dc725e7938e9f59f7151dd1b37500fabf77a4
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908539"
---
# <a name="copy-a-project"></a>Kopiranje projekta

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

U usluzi Dynamics 365 Project Operations možete brzo da gradite nove projekte pomoću radnje **Kopiraj projekat** na obrascu **Projekti**. Da biste kopirali projekat, izaberite projekat, a zatim izaberite **Kopiraj**. Radnja će kopirati:

- Svojstva projekta
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