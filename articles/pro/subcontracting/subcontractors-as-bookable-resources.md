---
title: Podešavanje podugovarača kao resursa koji mogu da se rezervišu
description: Ovaj članak objašnjava kako podesiti i održavati resurse podizvođača kreirane od korisnika i kontakata u sistemu, tako da se mogu povezati sa podugovorima u usluzi Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 727508c41c190c3703e9cd1420066fa0e551f147
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522719"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Podešavanje podugovarača kao resursa koji mogu da se rezervišu

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Pratite ove korake da biste podesili podizvođače kao resurse koji mogu da se rezervišu u usluzi Microsoft Dynamics 365 Project Operations.

1. Idite na **Projekat** \> **Resursi** i izaberite stavku **Novo**.
2. Na stranici **Novi resurs koji može da se rezerviše**, u polju **Vrsta resursa** izaberite jednu od sledećih opcija:

    - **Korisnik** – Odaberite ovaj tip resursa ako podizvođač mora da pristupi usluzi Project Operations radi unosa vremena ili troškova. Ako izaberete opciju **Korisnik**, podizvođaču je potrebna važeća licenca za pristup sistemu.
    - **Kontakt** ili **Poslovni kontakt** – Odaberite jedan od ovih tipova resursa ako podizvođaču nije potreban pristup usluzi Project Operations, ali mora biti dostupan za dodeljivanje zakazanih obaveza ili rezervacija na projektima. Nijedan od ovih tipova resursa ne pruža pristup sistemu. Izaberite **Poslovni kontakt** da predstavlja kompaniju dobavljača kao resurs koji može da se rezerviše. Izaberite **Kontakt** da predstavlja pojedinačne zaposlene dobavljača.

3. U zavisnosti od vrste izvora koji ste izabrali, od vas će se tražiti da izaberete odgovarajućeg korisnika, poslovni kontakt ili zapis o kontaktu.
4. U polju **Vrsta radnika** izaberite „Radnik po ugovoru“ da biste podesili podizvođača kao resurs koji može da se rezerviše.

    > [!NOTE]
    > Ako ostavite polje **Vrsta radnika** prazno, resurs koji može da se rezerviše posmatraće se kao zaposleni.

5. Ako ste kao vrstu radnika izabrali **Radnik po ugovoru**, izaberite dobavljača za kojeg resurs radi.
6. Izaberite vremensku zonu resursa, a zatim izaberite **Sačuvaj**. Da biste resursu za koji može da se rezerviše dodelili šablon radnog vremena, možete da izaberete opciju **Podešavanje kalendara** na stranici sa listom **Resurs koji može da se rezerviše**.

Da bi mogao da bude povezan sa stavkom podugovora, resurs koji može da se rezerviše mora da ispunjava sledeće uslove:

- Resurs koji može da se rezerviše mora da bude radnik po ugovoru.
- Resurs koji može da se rezerviše sa tipom resursa **Kontakt** mora da bude povezan sa poslovnim kontaktom dobavljača kao kontakt. Resurs koji može da se rezerviše sa tipom resursa **Korisnik** ne mora da bude povezan sa poslovnim kontaktom dobavljača kao kontakt.
- Vrednost polja **Dobavljač** za resurs koji može da se rezerviše mora odgovarati vrednosti polja **Dobavljač** za podugovor.

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>Ažurirajte tip mapiranja radnika i dobavljača za resurse koji mogu da se rezervišu

Polje **Vrsta radnika** za resurs koji može da se rezerviše određuje da li je resurs koji može da se rezerviše radnik po ugovoru ili zaposleni. Polje **Dobavljač** polje definiše poslovni kontakt dobavljača sa kojim je povezan resurs koji može da se rezerviše. Povezivanjem resursa koji može da se rezerviše sa dobavljačem kao kontaktom, ukazujete na to da je kontakt zaposleni u kompaniji dobavljača.

Ako se polja **Vrsta radnika** i **Dobavljač** za resurs koji može da se rezerviše izmene, promene utiču na buduće provere valjanosti novih zapisa koje resurs koji može da se rezerviše kreira, kao što su vremenski unosi. Međutim, promene ne poništavaju postojeće zapise.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
