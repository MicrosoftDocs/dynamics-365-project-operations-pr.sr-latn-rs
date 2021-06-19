---
title: Kopiranje projekta
description: Ova tema pruža informacije o kopiranju projekata u usluzi Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091271"
---
# <a name="copy-a-project"></a>Kopiranje projekta

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Uz Dynamics 365 Project Operations, možete brzo da pravite nove projekte izborom opcije **Kopiraj projekat** u obrascu **Projekti**. Da biste kopirali projekat, otvorite projekat koji želite da kopirate, a zatim izaberite **Kopiraj projekat**. Radnja će kopirati sledeće:

- Svojstva projekta 
- Strukturna analiza posla
- Članovi projektnog tima
- Procene za projekat
- Procene troškova projekta
- Procene materijala za projekat

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
- Procenjeni datum početka: Ovo je datum kada se projekat kreira iz kopije.
- Procenjeni datum završetka: Ovaj datum se prilagođava na osnovu datuma početka novog projekta koji je napravljen iz kopije.
- Angažovanje (časovi)
- Procenjeni troškovi rada
- Procenjeni iznos troškova
- Iznos procenjenih troškova materijala

> [!NOTE]
> Kopiranje projekta je dugotrajna operacija. Kopiraju se i zapisi projekta, njihovi relevantni atributi i mnogi povezani entiteti. Zbog dugotrajne prirode operacije, nakon započinjanja kopiranja, ciljna stranica projekta se zaključava za uređivanje dok se operacija kopiranja ne dovrši.

## <a name="work-breakdown-structure"></a>Strukturna analiza posla

Kada se projekat kopira, kopira se celokupna strukturna analiza posla učitanog resursa. Imenovani resurs zamenjuje generičke resurse. Ako imenovani resursi nemaju isto radno vreme kao generički resurs, raspored će se ponovo izračunati i trajanje zadatka se može promeniti.

## <a name="project-team-members"></a>Članovi projektnog tima

Kada se projektni tim kopira iz izvornog projekta, kopiraju se generički resursi. Dodele generičkih resursa takođe se održavaju kao u izvornom projektu. Imenovani resursi će se pretvoriti u generičke članove tima.

## <a name="estimates"></a>Procene

Kada se projekat kopira, stavke resursa, troškova i procene materijala kopiraju se iz izvornog projekta. 

Za informacije o tome kako programski pristupiti opciji Kopiraj projekat, pogledajte [Razvijajte predloške projekata pomoću opcije Kopiraj projekat](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
