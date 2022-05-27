---
title: Kopiranje projekta
description: Ova tema pruža informacije o kopiranju projekata u usluzi Dynamics 365 Project Operations.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e9b637d2d282d123dfacb8a295292ea06549aa1e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574447"
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
- Liste za proveru projekta
- Kofe projekta

## <a name="project-properties"></a>Svojstva projekta

Kada se projekat kopira, kopiraju se vrednosti u sledećim poljima.

| Polje | Nenapušteni materijali za projektne operacije | Projektne operacije Lite | Projekat za Web |
|-------|------------------------------------------|-------------------------|---------------------|
| Imenuj | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Opis | :heavy_check_mark: | :heavy_check_mark: | |
| klijentu | :heavy_check_mark: | :heavy_check_mark: | |
| Predložak kalendara | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Valuta | :heavy_check_mark: | :heavy_check_mark: | |
| Jedinica ugovaranja | :heavy_check_mark: | :heavy_check_mark: | |
| Preduzeće-vlasnik | :heavy_check_mark: | | |
| Menadžer projekta | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Status | :heavy_check_mark: | :heavy_check_mark: | |
| Ukupan status projekta | :heavy_check_mark: | :heavy_check_mark: | |
| komentara | :heavy_check_mark: | :heavy_check_mark: | |
| Procene | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Procenjeni datum početka</p><p><strong>Napomena:</strong> Ovo polje navodi datum kreiranja projekta iz kopije. | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Procenjeni datum završetka</p><p><strong>Napomena: Datum</strong> u ovom polju se koriguje na osnovu datuma početka novog projekta koji je napravljen iz kopije.</p> | :heavy_check_mark: | :heavy_check_mark: | |
| Angažovanje (časovi) | :heavy_check_mark: | :heavy_check_mark: | |
| Procenjeni troškovi rada | :heavy_check_mark: | :heavy_check_mark: | |
| Procenjeni iznos troškova | :heavy_check_mark: | :heavy_check_mark: | |
| Iznos procenjenih troškova materijala | | :heavy_check_mark: | |

> [!NOTE]
> Kopiranje projekta je dugotrajna operacija. Kopiraju se i zapisi projekta, njihovi relevantni atributi i mnogi povezani entiteti. Zbog dugotrajne prirode operacije, nakon započinjanja kopiranja, ciljna stranica projekta se zaključava za uređivanje dok se operacija kopiranja ne dovrši.

## <a name="work-breakdown-structure"></a>Strukturna analiza posla

Kada se projekat kopira, kopira se celokupna strukturna analiza posla učitanog resursa. Imenovani resurs zamenjuje generičke resurse. Ako imenovani resursi nemaju isto radno vreme kao generički resurs, raspored će biti ponovo obračunat, a trajanje zadatka može da se promeni.

## <a name="project-team-members"></a>Članovi projektnog tima

Kada se projektni tim kopira iz izvornog projekta, kopiraju se generički resursi. Dodele generičkih resursa takođe se održavaju kao u izvornom projektu. Imenovani resursi će se pretvoriti u generičke članove tima.

> [!NOTE]
> Članovi tima i dodele se ne kopiraju u projektu za Web.

## <a name="estimates"></a>Procene

Kada se projekat kopira, stavke resursa, troškova i procene materijala kopiraju se iz izvornog projekta. 

Za informacije o tome kako programski pristupiti opciji Kopiraj projekat, pogledajte [Razvijajte predloške projekata pomoću opcije Kopiraj projekat](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Ponude i ugovori

Ponude i ugovori nisu povezani sa odredišnim projektom.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
