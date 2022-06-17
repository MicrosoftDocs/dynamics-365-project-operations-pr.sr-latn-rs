---
title: Praćenje cene projekta
description: Ovaj članak pruža informacije o tome kako projektne operacije prate napredak u odnosu na troškove rada i troše na projekat.
author: rumant
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c069a28c6dc546e5e632c4dff29686dc7965f23e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923757"
---
# <a name="labor-cost-tracking-on-projects"></a>Praćenje cene rada na projektima

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Dynamics 365 Project Operations prati procene rada i potrošnju na najnižoj potrebnoj granularnosti u planu projekta. Finansijska procena cene rada se zasniva na planiranom angažovanju i generičkim ili imenovanim resursima koji su dodeljeni svakom zadatku čvora lista u planu projekta. Kada projekat započne i ljudi počnu da izveštavaju o vremenu za razne projektne zadatke, stvarna potrošnja rada se rezimira, čime započinje proračun projekcija.

## <a name="labor-cost-tracking-view"></a>Prikaz praćenja cene rada

Na stranici **Projekti**, na kartici **Praćenje** možete izabrati **Praćenje** > **Cena** da biste otvorili prikaz **Praćenje troškova** i videli napredak utroška rada za svaki zadatak u planu projekta. Ovaj prikaz takođe upoređuje stvarnu cenu rada utrošenu na zadatku sa planiranom cenom rada. Project Operations koristi sledeće formule za izračunavanje metrika cene rada:

- **Planirana cena**: Procenjena cena svih dodela resursa na svakom zadatku čvora lista
- **Stvarna cena**: Zbir svih stvarnih cena za vreme evidentirano u zadatku
- **Procenat potrošnje cene**: Stvarna cena ÷ Procena cene na završetku
- **Preostala cena**: Procena cene na završetku – Stvarna cena
- **Cena na završetku**: Preostala cena + Stvarna cena
- **Odstupanje od cene**: Planirana cena – Procena cene na završetku

Svaki zadatak prikazuje projekciju odstupanja od cene u zadatku. Ako je kompletna procena cene na završetku veća od planirane cene, predviđa se da će zadatak premašiti budžet. Ako je procena cene na završetku manja od planirane cene, predviđa se da će se zadatak završiti u okviru budžeta.

>[!NOTE]
> Project Operations prikazuje samo cene rada na stranici **Projekat** na kartici **Praćenje**. Iako se materijal i troškovi mogu proceniti i pratiti za potrošnju, ove cene nisu uključene u cene prikazane na kartici **Praćenje**. Ova kartica je dizajnirana da radi samo za ponovno projektovanje prihoda od rada ponovnim projektovanjem angažovanja.
Svi prikazani iznosi cena pretvaraju se u valutu cene projekta iz valute cene koštanja projekta koja se koristi za određivanje stope troškova. Valuta cene projekta je valuta ugovorne jedinice na projektu. Procenjene vrednosti troškova za vreme koje su prikazane na kartici **Procene** na stranici **Projekat** možda neće dovesti do planirane cene na kartici **Praćenje**. Razlog za ovo odstupanje je zbog razlika u načinu sabiranja procenjene cene na mreži **Procene** i načina izračunavanja planirane cene na mreži **Praćenje**. 
>
> - **Kartica Procene** izračunava procenjenu cenu koristeći istu valutu stope troškova u cenovniku. Zatim se procenjeni trošak u valuti cenovnika konvertuje u procenjenu cenu u valuti cene projekta. Procenjena cena u valuti projekta prikazana je zaokružena na 2 decimale. Preciznost valute se ni u jednom trenutku tokom ove konverzije ne primenjuje. 
> - Na kartici **Praćenje**, obračun planirane cene prati nešto drugačiji redosled obračuna koji uključuje preciznost valuta koja se primenjuje u dve faze: 
   ><ol>
   ><li>Procenjeni iznos troškova u valuti cenovnika se konvertuje u osnovnu valutu (konverzija 1).</li>
   ><li>Procenjeni iznos troškova u osnovnoj valuti se konvertuje u valutu cene projekta (konverzija 2). </li>
   ></ol>
   >Preciznost valute se primenjuje u oba koraka da bi se dobila planirana cena (na kartici **Praćenje**) koja neznatno odstupa od procenjene cene (na prikazu **Po fazama vremena** na kartici **Procene**). 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a>Ponovno projektovanje cena na zadacima čvora lista

Cene rada na zadatku čvora lista ne mogu se direktno ponovo projektovati na kartici **Praćenje** na **stranici Projekat**. Međutim, možete koristiti prikaz **Praćenje angažovanja** da biste ponovo projektovali preostalo angažovanje na zadatku. To dovodi do ponovnog izračunavanja preostale cene zadatka. Sledi opis kako ovo funkcioniše.

1. Menadžer projekta može da ponovo projektuje angažovanje na zadacima tako što će ažurirati podrazumevanu vrednost u polju **Preostalo angažovanje** sa novom procenom preostalog angažovanja u zadatku. Ponovno projektovanje dovodi do ponovnog izračunavanja procene angažovanja na završetku (EAC) za zadatak, procenta napredovanja i odstupanja od projektovanog angažovanja na zadatku. EAC, procena do završetka (ETC) i procenat napretka u rezimiranim zadacima takođe se ponovo izračunavaju i stvaraju novu projekciju odstupanja od angažovanja.
2. Na osnovu nove vrednosti za preostalo angažovanje na zadatku, sistem izračunava preostalu cenu u prikazu **Praćenje cene**. Da bi izračunao preostalu cenu na osnovu preostalog angažovanja, sistem prvo izračunava prosečnu cenu jednog sata angažovanja na zadatku kao planiranu cenu ili planirano angažovanje. Planirana cena je zbir cena svih dodela resursa na zadatku. Prosečna cena po satu se koristi za izračunavanje preostale cene za novoprojektovano preostalo angažovanje na zadatku.
3. Cena na završetku i procenat potrošnje cene u zadatku čvora lista se ponovo izračunavaju.
4. Preračunavaju se sve cene na završetku zadataka rezimea, sve do osnovnog čvora.

## <a name="reprojecting-costs-on-summary-tasks"></a>Ponovno projektovanje cena na zadacima rezimea

Možete ponovo projektovati cene rada na zadacima rezimea ili zadacima kontejnera. Međutim, ne možete direktno ponovo projektovati cenu rada na zadatku rezimea projekta na kartici **Praćenje** na stranici **Projekat**. Slično zadacima čvorova lista, ponovno projektovanje rezimea i zadataka kontejnera može se izvršiti pomoću prikaza **Praćenje angažovanja**. U ovom prikazu možete ponovo da projektujete preostalo angažovanje na zadatku rezimea koje dovodi do preračunavanja preostale cene na zadatku rezimea. Sledi opis kako ovo funkcioniše.

1. Menadžer projekta može da ponovo projektuje angažovanje na zadacima rezimea ažuriranjem podrazumevane vrednosti preostalog angažovanja sa novom procenom zadatka. Ova ispravka dovodi do toga da se za zadatak rezimea ponovo izračunaju procena po završetku (EAC), procenat napretka i odstupanje od projektovanog angažovanja na zadatku. EAC, ETC i procenat napretka u rezimiranim zadacima takođe se ponovo izračunavaju i stvaraju novu projekciju odstupanja od angažovanja.
2. Na osnovu nove vrednosti za preostalo angažovanje na zadatku rezimea, sistem izračunava preostalu cenu u prikazu **Praćenje cene**. Da bi izračunao preostalu cenu na osnovu preostalog angažovanja, sistem prvo izračunava prosečnu cenu jednog sata angažovanja na zadatku rezimea kao planiranu cenu ili planirano angažovanje. Prosečna cena po satu se koristi za izračunavanje cene za novoprojektovano preostalo angažovanje na zadatku rezimea.
3. Cena na završetku i procenat potrošnje cene u zadatku rezimea se ponovo izračunavaju.
4. Nova cena po završetku raspoređuje se na podređene zadatke u istoj proporciji kao što je prvobitna planirana cena bila na zadatku.
5. Izračunava se nova vrednost cene na završetku za svaki od pojedinačnih zadataka sve do zadataka čvora lista. Na osnovu ove vrednosti, preostala cena i procenat potrošnje cene podređenih zadataka na koje se ovo odnosi do čvorova lista ponovo se izračunava na osnovu vrednosti cene na završetku. Ta vrednost rezultira novom projekcijom odstupanja od cene zadatka. 


Polje **Performanse cene** se može podesiti iz podataka praćenja. Kada je odstupanje od cene za osnovni čvor u prikazu **Praćenje cene** negativno, ovo polje možete da podesite na **U okviru budžeta**. Kada je odstupanje od cene za osnovni čvor pozitivno, možete da podesite vrednost na **Preko budžeta**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
