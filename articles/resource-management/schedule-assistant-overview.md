---
title: Pregled pomoćnika za zakazivanje
description: Ova tema pruža informacije o radu sa pomoćnikom za planiranje radi rezervisanja resursa.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4d58f5f45ca54691b6e736dee5aab7b273a8e042
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014133"
---
# <a name="schedule-assistant-overview"></a>Pregled pomoćnika za zakazivanje

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Pomoćnik za planiranje se koristi za rezervisanje resursa na osnovu zahteva koje je definisao menadžer projekta. Pomoćnik za planiranje se oslanja na parametre navedene u zahtevu za resursom da bi pronašao resurs. Pomoćnik za planiranje preporučuje resurse koji odgovaraju relevantnim zahtevima, poput dostupnih vremena ili potrebnih veština.

Kada se identifikuju odgovarajući resursi, menadžer resursa ili projekta može rezervisati resurs za rad.

## <a name="prerequisites"></a>Preduslovi

Pomoćnik za planiranje je deo rešenja Universal Resource Scheduling. Ovo rešenje je uključeno i instalirano uz Dynamics 365 Project Operations, Dynamics 365 Field Service i Dynamics 365 Customer Service.

## <a name="matching-requirements-and-resources"></a>Zahtevi i resursi koji se podudaraju

Zahtev za generisanim resursom zasniva se na detaljima kao što su:

-   Karakteristike
-   Uloge
-   Poslovne jedinice
-   Željene postavke resursa
-   Konture angažovanja
-   Vremenska zona

Pomoćnik za planiranje koristi ove detalje za filtriranje resursa.

## <a name="launch-the-schedule-assistant"></a>Pokretanje pomoćnika za planiranje

Postoje dva načina na koje se pokreće pomoćnik za planiranje. Ako koristite hibridni režim, u mreži člana tima možete da izaberete bilo kog člana tima sa neispunjenim zahtevima za resursima, a zatim izaberite **Rezerviši**. Ako koristite centralni režim, menadžer resursa pronalazi i bira resurs.

## <a name="schedule-assistant-filters"></a>Filter pomoćnika za planiranje

Nakon pokretanja pomoćnika za planiranje, detalji iz zahteva za resursom prikazuju se kao filtrirane vrednosti u levom oknu. Menadžer resursa ili menadžer projekata mogu precizno podesiti rezultate prilagođavanjem filtera kako bi udovoljili potrebama rasporeda.

Okno filtera prikazuje opcije vezane za posao, uključujući:

-   Početak i završetak posla
-   Karakteristike
-   Uloge
-   Organizacione jedinice
-   Preduzeće koje obezbeđuje resurse
-   Tipovi resursa
-   Željeni resursi


[!INCLUDE[footer-include](../includes/footer-banner.md)]