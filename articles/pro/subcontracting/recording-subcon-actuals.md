---
title: Vreme snimanja, troškovi i korišćenje materijala za komponente podizvođačima
description: Ovaj članak sadrži objašnjenja o tome kako Microsoft prati vreme, troškove i upotrebu materijala zapisane na projektima iz komponenti podizvođača Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1c05b941fb51c8b56422e3b5d3868c9b69197187
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927667"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Vreme snimanja, troškovi i korišćenje materijala na projektima za komponente podizvođačima

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Ovaj članak sadrži objašnjenja o tome kako Microsoft prati vreme, troškove i upotrebu materijala zapisane na projektima iz komponenti podizvođača Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Trošak za vreme podizvođača na projektima
U projektno poslovanje, radnici po ugovoru mogu da zabeleže vreme na projekte na sličan način kao zaposleni. Prilikom unošenja vremena na projekte i/ili projektne zadatke, radnik po ugovoru može da izabere određeni red podizvođaca i podizvođači.

Kada se odobri vreme koje su podneli radnici po ugovoru, trošak projekta se zapisuju korišćenjem stope troška po jedinici koja je podešena za taj resurs radnika po **ugovoru u odeljku Cene uloga** nabavnog cenovnog lista na podizvođači.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Troškovi za troškove podizvođačima na projektima
Prilikom unosa troškova nastalih u projektima, možete izabrati red podizvođača i podizvođača u stavci troška. 

Kada se ova stavka troškova prosledi i odobri, trošak troška se zapisuje na projektu na osnovu troška po jedinici koji je podešen za tu kategoriju transakcije **u odeljku "Cene kategorije** " nabavnog cenovnka na podizvođači.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Troškovi za podizvođače materijala na projektima
Prilikom unošenja upotrebe materijala u projekte, u evidenciji korišćenja materijala možete izabrati red podizvođači i podizvođači. Kada se evidencija upotrebe materijala prosledi i odobri, materijalni trošak se zapisuje na projektu na osnovu troška po jedinici **koji je podešen za taj proizvod u odeljku Stavke cenovnik** podizvođač.

Upotreba materijala se takođe može zapisati za proizvode za upis na projektima. Ova vrsta upotrebe materijala takođe može biti povezana sa redom podizvođačima i podizvođačima. Prilikom zapisivanja upotrebe materijala za proizvode za upisivanje, potrebno je da unesete trošak po jedinici proizvoda za upisivanje. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
