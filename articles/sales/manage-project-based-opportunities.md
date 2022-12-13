---
title: Upravljanje mogućnostima za poslovanje za projekat
description: Ovaj članak pruža informacije o tome kako raditi sa mogućnostima koje su povezane sa projektima.
author: rumant
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 56eba38476dd5b49f0043eee5d411d51f9bf56b8
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825349"
---
# <a name="manage-project-opportunities"></a>Upravljanje mogućnostima za poslovanje za projekat

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Projektne kompanije obično imaju svoje operacije isporuke raširene u više zemalja i geografskih područja. Troškovi izvršenja i isporuke projekta mogu se razlikovati u zavisnosti od toga koja lokacija ili odeljenje upravlja isporukom. Zauzvrat, ovo može uticati na marže pogodbe. Pružanje projektnih usluga obično uključuje velike količine ljudskih resursa, znatne troškove putovanja, materijalne troškove i druge troškove.

Mogućnosti zasnovane na projektima u usluzi Dynamics 365 Project Operations dizajnirane su pomoću proširenja za Dynamics 365 Sales. Ovaj članak pruža detalje o različitim poljima i poslovnoj logici uključenoj u dodatnu funkcionalnost koja je potrebna kompanijama zasnovanim na projektima kako bi upravljale mogućnostima zasnovanim na projektima.

## <a name="view-all-project-based-opportunities"></a>Prikažite sve mogućnosti za poslovanje zasnovane na projektima

Spisak svih mogućnosti za poslovanje zasnovanih na projektima može se videti na stranici liste **Mogućnost za poslovanje**. 

1. Idite na stavku **Prodaja** > **Mogućnosti za poslovanje**.
2. Koristite **Prebacivač prikaza** da biste izabrali druge filtrirane prikaze mogućnosti za poslovanje. Možete da kreirate sopstvene prikaze sa prilagođenim kriterijumima filtera da biste konfigurisali te prikaze i opcije navigacije.

Mogućnosti za poslovanje zasnovane na projektu mogu se kreirati ili izbrisati sa ove stranice liste ili stranice sa detaljima.

## <a name="business-process-flow-for-project-based-deals"></a>Tok poslovnog procesa za pogodbe zasnovane na projektu

Sledeći tokovi poslovnih procesa podržani su za pogodbe zasnovane na projektu u usluzi Project Operations:

- Poslovni proces od potencijalnog klijenta do mogućnosti za poslovanje
- Proces prodaje mogućnosti za poslovanje

### <a name="lead-to-opportunity-business-process"></a>Poslovni proces od potencijalnog klijenta do mogućnosti za poslovanje 
Poslovni proces od potencijalnog klijenta do mogućnosti za poslovanje podržava sledeće faze:

| Faza | Mapirani entitet | Funkcionalnost |
| --- | --- | --- |
| Kvalifikuj | Potencijalni klijent | Kvalifikujte potencijalnog klijenta da kreira poslovni kontakt, kontakt i mogućnost za poslovanje. |
| Razvij | Mogućnost za poslovanje | Razvijte mogućnost za poslovanje da biste dodali više informacija o obuhvaćenom poslu, ključnim zainteresovanim stranama i konkurenciji. |
| Predloži | Mogućnost za poslovanje | Razvijte predlog i dobijte odobrenje od internog tima za pregled. |
| Zatvaranje | Mogućnost za poslovanje | Ostvarite priliku da zaključite posao. |

### <a name="opportunity-sales-process"></a>Proces prodaje mogućnosti za poslovanje
Proces prodaje mogućnosti za poslovanje u usluzi Project Operations jeste proširenje poslovnog toka procesa prodaje mogućnosti za poslovanje u aplikaciji Prodaja. Ovaj poslovni proces je dizajniran tako da odmah podrži sledeće faze u mogućnosti za poslovanje zasnovanoj na projektu.

| Faza | Mapirani entitet | Funkcionalnost |
| --- | --- | --- |
| Kvalifikuj | Mogućnost za poslovanje | Kvalifikujte potencijalnog klijenta da kreira poslovni kontakt, kontakt i mogućnost za poslovanje. |
| Predloži | Ponuda | Razvijte predlog pomoću ponuda za projekat i dobijte odobrenje od internog tima za pregled. |
| Ugovor | Ugovor za projekat | Ostvarite ponudu da biste kreirali ugovor i započeli izvršenje i isporuku projekta. |
| Zatvaranje | Ugovor za projekat | Završite posao uspešno i zatvorite ugovor o projektu. |

> [!NOTE]
> Ako je vaša pogodba zasnovana na projektu započela sa potencijalnim klijentom, poslovni proces od potencijalnog klijenta do mogućnosti za poslovanje ima prednost.
>
> Ako je vaša pogodba zasnovana na projektu započela sa mogućnošću za poslovanje, poslovni proces prodaje mogućnosti za poslovanje ima prednost.

Možete da uredite tok poslovnog procesa proizvoda ili da kreirate sopstvene tokove poslovnog procesa kako biste pratili svoj prodajni proces po potrebi. Za više informacija o toku poslovnog procesa pogledajte [Pregled tokova poslovnog procesa](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
