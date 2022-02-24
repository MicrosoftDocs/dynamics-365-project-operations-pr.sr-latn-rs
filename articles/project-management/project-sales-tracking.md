---
title: Praćenje prodaje u projektu
description: Ova tema pruža informacije o tome kako Project Operations prati napredak u odnosu na prihode od rada na projektu.
author: rumant
manager: AnnBe
ms.date: 03/24/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 438c44dcfaf9677075eb07688c1e65c6e7053755
ms.sourcegitcommit: a1f9f92546ab5d8d8e5a4710ce4c96414ea55d14
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2021
ms.locfileid: "5711083"
---
# <a name="project-sales-tracking"></a>Praćenje prodaje u projektu

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Dynamics 365 Project Operations prati procene rada i prihoda na najnižoj potrebnoj granularnosti u planu projekta. Procena prihoda od rada se zasniva na planiranom angažovanju i generičkim ili imenovanim resursima koji su dodeljeni svakom zadatku čvora lista u planu projekta. Kada projekat započne i ljudi počnu da izveštavaju o vremenu za razne projektne zadatke, stvarni prihod od rada se rezimira, čime započinje proračun projekcija.

## <a name="labor-revenue-tracking-view"></a>Prikaz praćenja prihoda od rada

Na stranici **Projekti**, na kartici **Praćenje**, možete izabrati **Praćenje** > **Trošak** da otvorite prikaz **Praćenje troškova**. Ili možete izabrati **Korišćenje** > **Stopa naplate** da otvorite prikaz **Praćenje prihoda**, što prikazuje napredak prihoda od rada na svakom zadatku u planu projekta. Ovaj prikaz takođe upoređuje stvarni prihod od rada utrošen na zadatak sa planiranim prihodom od rada. Project Operations koristi sledeće formule za izračunavanje metrike prihoda od rada:

- **Planirani prihod**: Procenjene vrednosti prodaje svih dodela resursa na svakom zadatku čvora lista
- **Stvarni prihod**: Zbir svih nefakturisanih stvarnih prodaja za vreme zabeleženo u zadatku
- **% naplativog prihoda**: Stvarni prihod ÷ Procena prihoda na završetku
- **Preostali prihod**: Procena prihoda na završetku – Stvarni prihod
- **Procenjeni prihod na završetku**: Preostali prihod + Stvarni prihod
- **Odstupanje od prihoda**: Planirani prihod – Procenjeni prihod na završetku


> [!NOTE]
> Project Operations prikazuje samo prihode od rada na stranici **Projekat** na kartici **Praćenje**. Iako se materijal i troškovi mogu proceniti i pratiti za potrošnju, ovi prihodi nisu uključeni u prihode prikazane na kartici **Praćenje**. Ova kartica je dizajnirana da radi samo za ponovno projektovanje prihoda od rada ponovnim projektovanjem angažovanja.  
> Svi prikazani iznosi prihoda pretvaraju se u valutu troškova projekta. Valuta cene projekta je valuta ugovorne jedinice na projektu. Za projekte sa fiksnom cenom, brojevi prihoda u prikazu **Praćenje prihoda od rada** nisu relevantni jer se nefakturisane stvarne vrednosti prodaje ne evidentiraju po odobrenju vremena.
> Procenjene vrednosti prodaje za vreme koje su prikazane na kartici **Procena** za projekat možda neće dostići planiranu vrednost prihoda na kartici **Praćenje**. Izvor ovog neslaganja je iz dva moguća razloga:
><ol>
   ><li> Kartica <b>Procene</b> kartica prikazuje procenjeni prihod u valuti prodaje, dok kartica <b>Praćenje</b> prikazuje planirani prihod pretvoren u valutu cene. </li>
   ><li> Kada se procenjena prodaja pretvori u valutu ugovora, kao što je prikazano na kartici <b>Procene</b>, u valuti projekta, konverzija uključuje korake koji mogu dovesti do određenog gubitka tačnosti: </li>
><ol>
><li> Procenjeni iznos prodaje u valuti ugovora prvo se pretvara u osnovnu valutu (konverzija 1).</li>
><li> Procenjeni iznos prodaje u osnovnoj valuti prvo se pretvara u valutu cene projekta (konverzija 2). </li>
></ol>
></ol>
> Preciznost valute se primenjuje u oba koraka, što rezultira odstupanjem planiranog prihoda u valuti projekta od planirane prodaje u valuti ugovora.
   

## <a name="reprojecting-revenues-on-leaf-node-tasks"></a>Ponovno projektovanje prihoda na zadacima čvora lista

Prihodi od rada na zadatku sa čvorom lista ne mogu se direktno ponovo projektovati na kartici **Praćenje** na stranici **Projekat**. Međutim, možete koristiti prikaz **Praćenje angažovanja** da biste ponovo projektovali preostalo angažovanje na zadatku. To dovodi do ponovnog izračunavanja preostalog prihoda od zadatka. Sledi opis kako ovo funkcioniše.

1. Menadžer projekta može da ponovo projektuje angažovanje na zadacima tako što će ažurirati podrazumevanu vrednost u polju **Preostalo angažovanje** sa novom procenom preostalog angažovanja u zadatku. Ponovno projektovanje dovodi do ponovnog izračunavanja procene angažovanja na završetku (EAC) za zadatak, procenta napredovanja i odstupanja od projektovanog angažovanja na zadatku. EAC, procena do završetka (ETC) i procenat napretka u rezimiranim zadacima takođe se ponovo izračunavaju i stvaraju novu projekciju odstupanja od angažovanja.
2. Na osnovu nove vrednosti za preostalog angažovanja na zadatku, sistem izračunava preostali prihod u prikazu **Praćenje prihoda**. Da bi izračunao preostali prihod na osnovu preostalog angažovanja, sistem prvo izračunava prosečni prihod od jednog sata angažovanja na zadatku kao planirani prihod ili planirano angažovanje. Planirani prihod je zbir prihoda svih dodela resursa na zadatku. Prosečni prihod po satu se koristi za izračunavanje preostalog prihoda za novoprojektovano preostalo angažovanje na zadatku.
3. Procenjeni prihod na završetku i procenat potrošnje prihoda u zadatku čvora lista se preračunavaju.
4. Preračunavaju se sve vrednosti prihoda na završetku zadataka rezimea, sve do osnovnog čvora.

## <a name="reprojecting-revenues-on-summary-tasks"></a>Ponovno projektovanje prihoda na zadacima rezimea

Možete ponovo projektovati prihode od rada na zadacima rezimea ili zadacima kontejnera. Međutim, ne možete direktno ponovo projektovati prihode od rada na zadatku rezimea projekta na kartici **Praćenje** na stranici **Projekat**. Slično zadacima čvorova lista, ponovno projektovanje rezimea i zadataka kontejnera može se izvršiti pomoću prikaza **Praćenje angažovanja**. U ovom prikazu možete ponovo da projektujete preostalo angažovanje na zadatku rezimea koje dovodi do preračunavanja preostalog prihoda na zadatku rezimea. Sledi opis kako ovo funkcioniše.

1. Menadžer projekta može da ponovo projektuje angažovanje na zadacima tako što će ažurirati podrazumevanu vrednost u polju **Preostalo angažovanje** sa novom procenom **preostalog angažovanja** u zadatku. Ponovno projektovanje dovodi do toga da se za zadatak ponovo izračunaju procena po završetku (EAC), procenat napredovanja i odstupanje od projektovanog angažovanja na zadatku. EAC, ETC i procenat napretka u rezimiranim zadacima takođe se ponovo izračunavaju i stvaraju novu projekciju odstupanja od angažovanja.
2. Na osnovu nove vrednosti u polju **Preostalo angažovanje** na zadatku, sistem izračunava preostali prihod u prikazu **Praćenje prihoda**. Da bi izračunao preostali prihod na osnovu preostalog angažovanja, sistem prvo izračunava prosečni prihod od jednog sata angažovanja na zadatku kao planirani prihod ili planirano angažovanje. Planirani prihod je zbir prihoda svih dodela resursa na zadatku. Ovaj prosečni prihod po satu se zatim koristi za izračunavanje prihoda za novoprojektovano preostalo angažovanje na zadatku.
3. Procenjeni prihod na završetku i procenti potrošnje prihoda na zadatku čvora lista se preračunavaju.
4. Nova vrednost procenjenog prihoda po završetku raspoređuje se na podređene zadatke u istoj proporciji kao što je prvobitni planirani prihod bio na zadatku.
5. Izračunava se novi procenjeni prihod na završetku za svaki od pojedinačnih zadataka sve do zadataka čvora lista. Na osnovu ove vrednosti, preostali prihod i procenat potrošnje prihoda podređenih zadataka na koje se ovo odnosi do čvorova lista ponovo se izračunava na osnovu prihoda u celoj vrednosti. To rezultira novom projekcijom odstupanja od prihoda na zadatku. 
6. Preračunavaju se sve vrednosti prihoda na završetku zadataka rezimea, sve do osnovnog čvora.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

