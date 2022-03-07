---
title: Konfigurisanje automatskog kreiranja fakture
description: Ova tema pruža informacije o podešavanju i konfigurisanju automatskog kreiranja predračuna.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1cce457fbc04ba9d3890d73439e6e7fd3db44d84a4498d5dc68ed82d362158b5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997533"
---
# <a name="set-up-automatic-invoice-creation"></a>Konfigurisanje automatskog kreiranja fakture 
 
_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture, Project Operations za scenarije zasnovane na resursima / bez zaliha_

Možete da konfigurišete automatsko kreiranje faktura u usluzi Dynamics 365 Project Operations. Sistem kreira nacrt predračuna na osnovu rasporeda faktura za svaki ugovor o projektu i predmet ugovora. Rasporedi faktura se konfigurišu na nivou predmeta ugovora. Svaka linija ugovora može imati različit raspored faktura ili isti raspored faktura može biti uključen u svaki red ugovora.

Kada kreirate fakturu, sistem uvek kreira najmanje jednu fakturu po ugovoru o projektu. U nekim slučajevima može biti napravljeno više faktura. Na primer, ako ugovor ima više klijenata, stvoriće se isti broj faktura kao i broj klijenata koji imaju fakturisane transakcije za fakturisanje na tom ugovoru o projektu.

## <a name="understand-how-transactions-are-included-on-an-invoice"></a>Shvatite kako su transakcije uključene u fakturu 

Ponekad svaki predmet ugovora zasnovanog na projektu navodi zaseban raspored faktura. Na primer, usluge implementacije za Adatum ugovor imaju sledeće predmete ugovora:

- Prototip rada koji je fiksna cena sa dve ručno kreirane kontrolne tačke.
- Radovi primene koji uključuju vreme i koji će se naplaćivati na dve nedelje ponedeljkom.
- Nastali troškovi koji treba da se obračunavaju mesečno prvog ponedeljka u mesecu.

Rasporedi faktura definisani za svaku od ove dve stavke porudžbina izgledaju kao sledeća tabela:

| Predmet ugovora | Datum za pokretanje fakture | Datum isključivanja transakcije | Datum kontrolne tačke | Iznos kontrolne tačke |
| --- | --- | --- | --- | --- |
| Prototip rada | 5. oktobar, ponedeljak | - | 5. oktobar, ponedeljak | 5000 USD |
| - | 3. novembar, utorak | - | 3. novembar, utorak | 12,000 USD |
| Rad primene | 5. oktobar, ponedeljak | 4. oktobar, nedelja | - | - |
| - | 19. oktobar, ponedeljak | 18. oktobar, nedelja | - | - |
| - | 2. novembar, ponedeljak | 1. novembar, nedelja | - | - |
| - | 16. novembar, ponedeljak | 15. novembar, nedelja | - | - |
| Troškovi nastali | 5. oktobar, ponedeljak | 4. oktobar, nedelja | - | - |
| - | 2. novembar, ponedeljak | 1. novembar, nedelja | - | - |

U ovom primeru, kada se pokreće automatsko fakturisanje:

- **4. oktobar ili bilo koji datum pre**: Za ovaj ugovor se ne generiše faktura jer tabela **Raspored faktura** za svaki od ovih predmeta ugovora ne poziva 4. oktobar, nedelju kao datum pokretanja fakture.
- **5. oktobar, ponedeljak**: Jedna faktura se generiše za:

    - Prototip rada koji uključuje kontrolnu tačku, ako je označena kao **Spremno za fakturisanje**.
    - Rad primene koji uključuje sve vremenske transakcije kreirane pre datuma preseka transakcije 4. oktobra, nedelja, označene kao **Spremno za fakturisanje**.
    - Nastali troškovi koji uključuju sve transakcije troškova kreirane pre datuma preseka transakcije 4. oktobra, nedelja, označene kao **Spremno za fakturisanje**.
  
- **6. oktobar ili bilo koji datum pre 19. oktobra**: Za ovaj ugovor se ne generiše faktura jer tabela **Raspored faktura** za svaki od ovih predmeta ugovora ne poziva 6. oktobar niti bilo koji datum pre 19. oktobra kao datum pokretanja fakture.
- **19. oktobar, ponedeljak**: Jedna faktura se generiše za rad primene koji uključuje sve vremenske transakcije kreirane pre datuma preseka transakcije 18. oktobra, nedelja, označene kao **Spremno za fakturisanje**.
- **2. novembar, ponedeljak**: Jedna faktura se generiše za:

    - Rad primene koji uključuje sve vremenske transakcije kreirane pre datuma preseka transakcije 1. novembra, nedelja, označene kao **Spremno za fakturisanje**.
    - Nastali troškovi koji uključuju sve transakcije troškova kreirane pre datuma preseka transakcije 1. novembra, nedelja, označene kao **Spremno za fakturisanje**.

- **3. novembar, utorak**: Jedna faktura se generiše za prototip rada koji uključuje kontrolnu tačku za 12.000 USD, ako je označena kao **Spremno za fakturisanje**.

## <a name="configure-automatic-invoicing"></a>Konfigurišite automatsko fakturisanje

Dovršite sledeće korake da biste konfigurisali automatsko pokretanje faktura.

1. U odeljku **Project Operations**, idite na **Podešavanja** > **Podešavanje periodične fakture**.
2. Kreirajte grupni posao i imenujte ga **Kreiranje faktura u usluzi Project Operations**. Naziv grupnog posla mora da sadrži reči „kreiranje faktura“.
3. U polju **Tip posla** izaberite **Nijedan**. Podrazumevano se polja **Dnevna učestalost** i **Je aktivna** podešavaju na **Da**.
4. Izaberite **Pokreni tok posla**. U dijalogu **Pronalaženje zapisa** ćete videti tri toka posla:

- ProcessRunCaller
- ProcessRunner
- UpdateRoleUtilization

5. Izaberite **ProcessRunCaller**, a zatim **Dodaj**.
6. U sledećem dijalogu izaberite **U redu**. Tok posla **Hibernacija** prati tok posla **Proces**. 

> [!NOTE]
> Možete izabrati i **ProcessRunner** u koraku 5. Nakon toga, kada izaberete **U redu**, tok posla **Proces** će biti praćen tokom posla **Hibernacija**.

Tokovi posla **ProcessRunCaller** i **ProcessRunner** kreiraju fakture. **ProcessRunCaller** poziva **ProcessRunner**. **ProcessRunner** je tok posla koji zapravo kreira fakture. Tok posla prolazi kroz sve predmete ugovora za koje se moraju kreirati fakture i kreira fakture za te predmete. Da bi odredio predmete ugovora za koje fakture moraju biti kreirane, posao traži datume pokretanja fakture za predmete ugovora. Ako predmeti ugovora koji pripadaju jednom ugovoru imaju isti datum pokretanja fakture, transakcije se kombinuju u jednu fakturu koja ima dve stavke fakture. Ako ne postoje transakcije za koje treba kreirati fakture, posao preskače kreiranje fakture.

Nakon što se **ProcessRunner** pokrene, on poziva **ProcessRunCaller**, obezbeđuje vreme završetka i zatvara se. **ProcessRunCaller** zatim pokreće tajmer koji će biti pokrenut tokom perioda od 24 časa od određenog vremena završetka. Na kraju tajmera **ProcessRunCaller** se zatvara.

Posao grupne obrade za kreiranje faktura je periodični posao. Ako se ova grupna obrada pokreće više puta, kreira se više instanci posla i izazivaju greške. Zbog toga bi trebalo samo jednom da pokrenete grupnu obradu i da je ponovo pokrenete samo ako prestane da radi.

> [!NOTE]
> Grupno fakturisanje u usluzi Project Operations se izvodi samo za predmete ugovora o projektu koji su konfigurisani prema rasporedima faktura. Predmet ugovora sa načinom naplate uz fiksnu cenu mora da ima konfigurisane kontrolne tačke. Predmet ugovora za projekat sa načinom naplate vremena i materijala treba da uspostavi raspored faktura na osnovu datuma.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
