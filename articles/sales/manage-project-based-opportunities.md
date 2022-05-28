---
title: Upravljanje mogućnostima za poslovanje zasnovanim na projektima
description: Ova tema pruža informacije o tome kako raditi sa mogućnostima koje su povezane sa projektima.
author: rumant
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f39940ac063a8c202f33797ed649518907563e31
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600437"
---
# <a name="manage-project-based-opportunities"></a>Upravljanje mogućnostima za poslovanje zasnovanim na projektima

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Projektne kompanije obično imaju svoje operacije isporuke raširene u više zemalja i geografskih područja. Troškovi izvršenja i isporuke projekta mogu se razlikovati u zavisnosti od toga koja lokacija ili odeljenje upravlja isporukom. Zauzvrat, ovo može uticati na marže pogodbe. Pružanje projektnih usluga obično uključuje velike količine ljudskih resursa, znatne troškove putovanja, materijalne troškove i druge troškove.

Mogućnosti zasnovane na projektima u usluzi Dynamics 365 Project Operations dizajnirane su pomoću proširenja za Dynamics 365 Sales. Ova tema pruža detalje o različitim poljima i poslovnoj logici uključenoj u dodatnu funkcionalnost koja je potrebna kompanijama zasnovanim na projektima kako bi upravljale mogućnostima zasnovanim na projektima.

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