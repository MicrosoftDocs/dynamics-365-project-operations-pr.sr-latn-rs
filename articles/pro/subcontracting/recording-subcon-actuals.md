---
title: Vreme snimanja, troškovi i korišćenje materijala za komponente podizvođačima
description: Ovaj članak objašnjava kako Microsoft Dynamics 365 Project Operations prati vreme, troškove i korišćenje materijala evidentiranih na projektu iz komponenti podugovora.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b82c14412cfb0405040902a2329c3b6692422d89
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522531"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Vreme snimanja, troškovi i korišćenje materijala na projektu za komponente podugovora

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Ovaj članak objašnjava kako Microsoft Dynamics 365 Project Operations prati vreme, troškove i korišćenje materijala evidentiranih na projektu iz komponenti podugovora.

## <a name="costing-for-subcontractor-time-on-projects"></a>Određivanje cena za vreme podugovarača na projektima
U usluzi Project Operations, radnici po ugovoru mogu da evidentiraju vreme na projektima na sličan način kao i zaposleni. Prilikom unosa vremena na projektima i/ili projektnim zadacima, radnik po ugovoru može izabrati određeni podugovor i predmet podugovora.

Kada se odobri vreme koje su podneli radnici po ugovoru, cena projekta se evidentira korišćenjem stope cene jedinice koja je podešena za taj resurs radnika po ugovoru u odeljku **Cene uloga** cenovnika nabavke na podugovoru.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Određivanje cena za podugovorene troškove na projektima
Prilikom unosa troškova nastalih na projektima, možete izabrati podugovor ili predmet podugovora u stavci troška. 

Kada se prosledi i odobri ova stavka troška, cena troška se evidentira u projektu na osnovu cene jedinice koja je podešena za tu kategoriju transakcije u odeljku **Cene kategorija** cenovnika nabavke na podugovoru.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Određivanje cena za podugovorene materijale na projektima
Prilikom unosa korišćenja materijala na projektima, možete izabrati podugovor ili predmet podugovora u evidenciji korišćenja materijala. Kada se prosledi i odobri evidencija korišćenja materijala cena materijala se evidentira u projektu na osnovu cene jedinice koja je podešena za taj proizvod u odeljku **Stavke cenovnika** cenovnika podugovora.

Korišćenje materijala se takođe može evidentirati za ručno unete proizvode na projektima. Ova vrsta korišćenja materijala takođe može biti povezana sa podugovorom i predmetom podugovora. Prilikom evidentiranja korišćenja materijala za ručno dodate proizvode, potrebno je da unesete cenu po jedinici ručno unetog proizvoda. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
