---
title: Objavljivanje izveštaja o troškovima
description: Ova j članak objašnjava kako se objavljuju izveštaji o troškovima.
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524887"
---
# <a name="post-expense-reports"></a>Objavljivanje izveštaja o troškovima

Kada se izveštaj o troškovima odobri i prenese u opšti dnevnik, može se knjižiti. Kada objavite izveštaj o troškovima, identifikuju se troškovi koji ispunjavaju uslove za povraćaj poreza na dodatu vrednost (PDV). Zadatak verifikacije i povraćaja plaćanja PDV-a dodeljen je zaposlenom koji je odgovoran za verifikaciju izveštaja o troškovima.

Ako se troškovi u izveštaju o troškovima naplaćuju kompaniji koja nije kompanija koja zapošljava zaposlenog, morate da potvrdite i kompaniju kojoj se ti troškovi duguju i kompaniju koja duguje. Na primer, zaposleni koji je podneo izveštaj o troškovima radi za kompaniju DAT, ali je trošak naplatio kompaniji DIR. U ovom slučaju, DAT je kompanija kojoj se duguje trošak, a DIR kompanija koja duguje trošak. Kada verifikujete ove stavke u glavnoj knjizi, stavke troškova možete knjižiti u glavnu knjigu.

Da biste proknjižili izveštaj o troškovima, na stranici **Odobreni izveštaji o troškovima** izaberite izveštaj o troškovima, a zatim u oknu radnji izaberite **Knjiži**.

Takođe možete istovremeno proknjižiti sve izveštaje o troškovima na listi. Izaberite sve izveštaje o troškovima, a zatim izaberite **Knjiži**.

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>Omogućite mogućnost funkcije knjiženja odgovornosti za troškove u valuti dobavljača za način plaćanja gotovinom

Funkcija **Mogućnost knjiženja odgovornosti za troškove u valuti dobavljača** omogućava knjiženje izveštaja o troškovima u valuti dobavljača za način plaćanja gotovinom.

Trenutno, kada prosleđujete gotovinske troškove, izveštaji o troškovima se knjiže u računovodstvenoj valuti. Zbog konverzije iznosa između valute transakcije, knjigovodstvene valute i valute dobavljača, netačan iznos se plaća dobavljačima ako datum transakcije troška i stvarni datum plaćanja imaju različite devizne kurseve.

Ova funkcija će osigurati da saldo dobavljača bude evidentiran u valuti dobavljača kada se proknjiži izveštaj o troškovima.

1. Idite na stavku **Radni prostori** \> **Upravljanje funkcijama**.
2. Na listi pronađite i izaberite **Mogućnost knjiženja odgovornosti za troškove u valuti dobavljača** za način plaćanja gotovinom, a zatim izaberite **Omogući odmah**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
