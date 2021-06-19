---
title: Ključni koncepti
description: Ova tema pruža veze ka informacijama o ključnim konceptima za upravljanje resursima u aplikaciji Project Service Automation.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 5f314e3a6cc70748628145f693fb81b598e568dc
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008868"
---
# <a name="key-concepts"></a>Ključni koncepti

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Sledeća tabela definiše ključne koncepte koji se koriste u aplikaciji Dynamics 365 Project Service Automation.

| Koncept                    | Definicija |
|----------------------------|------------|
| Član projektnog tima        | Kao deo projektnog tima, član projektnog tima može biti imenovani resurs koji ima rezervacije, imenovani resurs koji nema rezervacije ili generički resurs. Generički resursi nemaju rezervacije, usko su vezani za projekat i nemaju ograničenja kapaciteta za projekte. |
| Generički resurs projekta   | Čuvar mesta resursa koji vam omogućava da formirate tim i obezbedite resurse za projektni plan bez potrebe da je upoznat sa imenovanim resursom. Kalendar projekta koristi se kao kalendar generičkog resursa. Generički resursi mogu se dodati u projektni tim i dodeliti zadacima. |
| Rezervisani sati               | Sati resursa su fiksno rezervisani u odnosu na projekat kako bi se osiguralo da će posao na projektu biti završen. Rezervisani sati se troše iz ukupnog kapaciteta resursa. Rezervacije se odnose samo na imenovane resurse, a ne na generičke resurse. |
| Dodeljeni sati             | Sati resursi dodeljeni su zadacima u rasporedu projekata. Dodele mogu biti za imenovane ili generičke resurse. Dodele mogu biti nezavisne od rezervacija. |
| Zahtevani sati             | Kapacitet koji je zatražen, ali ga još nije ispunio imenovani resurs. Zahtevani sati su relevantni samo za generičke članove tima sa generisanim potrebama za resursima. |
| Potražnja                     | Trenutno i predstojeće radno opterećenje. U aplikaciji Project Service Automation, potražnja se prikazuje kao potreba za resursima ili zahtev za resurs. |
| Zahtev za resursima       | Entitet koji se koristi za evidentiranje zahtevanih sati, datuma početka i završetka, veština, geografske lokacije i drugih dimenzija za određivanje cena za potrebne resurse. Potrebe za resursima su generisane od članova projektnog tima ili su kreirane pojedinačno. |
| Zahtev za resurs           | Entitet koji se koristi kao „koverta“ za prenos potrebe za resursom koja mora biti ispunjena od strane menadžera resursa. |
| Podrazumevana uloga resursa      | Uloga pod kojom je resurs grupisan radi izračunavanja ukupne iskorišćenosti. Pretpostavlja se da resurs poseduje potrebne veštine za ulogu i da ispunjava ciljnu ukupnu iskorišćenost za tu ulogu. |
| Organizaciona jedinica resursa | Organizaciona jedinica kojoj je resurs dodeljen. |
| Skiciranje                    | Zadatak, zahtev ili sati za dodelu, onako kako su raščlanjeni prema dnevnoj distribuciji. Na primer, petodnevni zadatak od 40 sati može se skicirati u osam sati dnevno tokom pet dana. |
| Prikaz usaglašenosti        | Prikaz koji prikazuje rezervacije i dodele za svakog člana projektnog tima. Ovaj prikaz omogućava menadžeru projekta da traži bilo kakvu neusklađenost između rezervacija i dodela i da preduzme korektivne mere ako dođe do bilo kakve neusklađenosti. |
| Radni časovi                 | Entitet koji se koristi za identifikaciju kapaciteta resursa, radnog vremena i neradnih sati. Ovaj entitet se takođe naziva i kalendar resursa. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]