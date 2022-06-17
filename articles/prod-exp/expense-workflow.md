---
title: Tok posla za upravljanje troškovima
description: Ovaj članak sadrži objašnjenja o tome kako možete da koristite sistem Microsoft Dynamics toka posla u programu 365 Finansije da biste podesili proces redigovanja za izveštaje o troškovima u upravljanju troškovima.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 71efc89d9167ef1ee546c67c123efeb37125cc02
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929737"
---
# <a name="expense-management-workflow"></a>Tok posla za upravljanje troškovima

Možete da koristite sistem tokova posla da biste uspostavili postupak pregleda izveštaja o troškovima u upravljanju troškovima. Možete da podesite tok posla koji koristi sledeće kriterijume da biste odredili ko odobrava izveštaje o troškovima:

- Hijerarhija izveštavanja zaposlenih i unapred definisana ograničenja odobrenja
- Odobravanje na više nivoa koje podržava privremene i konačne davaoce odobrenja
- Finansijske dimenzije i projektna odgovornost
- Dodeljivanje određenim korisnicima ili grupama korisnika

Odobravanja tokova posla mogu se kreirati za izveštaje o troškovima, zahteva za putovanje, akontacije i povraćaj poreza na dodatu vrednost (PDV).

**Primer**

Sledeći postupak je primer toka posla za upravljanje troškovima za izveštaj o troškovima.

1. Zaposleni kreira i čuva izveštaj o troškovima.
2. Zaposleni prosleđuje izveštaj o troškovima na odobrenje. Davalac odobrenja se identifikuje na osnovu pravila koja su definisana prilikom podešavanja toka posla.
3. Davalac odobrenja dobija obaveštenje da je izveštaj o troškovima spreman za odobrenje. Davalac odobrenja pregleda izveštaj o troškovima i potvrđuje da su ispunjeni sledeći uslovi:

    - Troškovi ne krše nijednu smernicu troškova. Ako trošak krši smernice, davalac odobrenja potvrđuje da izveštaj o troškovima sadrži valjano poslovno opravdanje.
    - Elektronski računi su priloženi izveštaju o troškovima.

4. Davalac odobrenja odobrava izveštaj o troškovima.
5. Izveštaj o troškovima dodeljuje se koordinatoru za dugovanja na knjiženje.
6. Dolazi do jednog od sledećih koraka, u zavisnosti od toga da li je konfigurisano automatsko knjiženje:

    - Ako je konfigurisano automatsko knjiženje, izveštaj o troškovima se obrađuje za plaćanje i ažurira se status izveštaja o troškovima.
    - Ako automatsko knjiženje nije konfigurisano, koordinator dugovanja verifikuje da su predati svi originalni računi i da su računi usklađeni sa troškovima u izveštaju o troškovima. Sve šifre poreza koje su unete u izveštaj o troškovima takođe moraju biti verifikovane kao tačne.

Nakon što se ovi zahtevi provere, izveštaj o troškovima se knjiži.

Nakon što se proknjiži izveštaj o troškovima, odobrava se plaćanje za izveštaj o troškovima, a zaposlenom se nadoknađuje.


[!INCLUDE[footer-include](../includes/footer-banner.md)]