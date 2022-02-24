---
title: Tok posla za upravljanje troškovima
description: Ova tema objašnjava kako možete da koristite sistem tokova posla u usluzi Microsoft Dynamics 365 Finance, da biste uspostavili postupak pregleda izveštaja o troškovima u upravljanju troškovima.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fde336f53d72e9ddf38c5123d9e774a4c3a22a28
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271685"
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