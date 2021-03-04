---
title: Kako da dodelim resurs koji može da se rezerviše zadatku u veb aplikaciji
description: Pregled načina na koji možete dodeliti resurse koje je moguće dodeliti.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 27a93c41243f300cadb632c697672180e5a3817b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146590"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>Kako da dodeljujete resurs koji može da se rezerviše zadatku u veb aplikaciji (aplikacija Project Service v2.x)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Postoje dva načina dodele resursa zadatku u programu Project Service. Resurs možete da rezervišete kao član tima, a zatim da ga dodelite zadatku. Ili možete da kreirate generičkog člana tima preko dodele uloga na zadacima, generisanja tima, a zatim popunjavanjem zahteva za pravljenje rezervne kopije sa imenovanim resursom.

Imajte u vidu da ako želite da dodelite resurs koji može da se rezerviše zadatku, član tima resursa koji može da se rezerviše mora da ima dovoljno dostupnih rezervacija. Status rezervacije mora da bude tip izvršavanja Fiksno rezerviši i sa statusom Izvršeno. Ako nema dovoljno rezervacija za resurs, Project Service uklanja zadatak i prikazuje sledeću poruku o grešci:

*Nije moguće dodeliti resurs zadatku – Sledeće resursi nemaju dovoljno rezervisanih radnih sati za projekat*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Rezervišite resurs kao član tima, a zatim dodelite resurs zadatku

Sa ovim metodom dodajete resurs u projektni tim, a zatim dodeljujete zadatke resursu u rasporedu projekta. Evo kako to da uradite:
1.  U koordinatnoj mreži člana tima dodajte novog člana tima tako što ćete izabrati **Novi**.
2.  Na ekranu brzog kreiranja člana tima, izaberite ime resursa koji može da se rezerviše i podesite ulogu.
3.  Izaberite datume **Od** i **Do**.

    > [!div class="mx-imgBorder"] 
    > ![Snimak ekrana dodavanja člana tima](media/FAQ-Resources-to-Tasks2-1.png "Snimak ekrana dodavanja člana tima")
 
4.  Izaberite jedan od sledećih načina dodele za rezervaciju resursa:
    - **Puni kapacitet** rezerviše puni kapacitet resursa za navedene početne i krajnje datume.
    - **Procenat kapaciteta** rezerviše određeni procenat kapaciteta resursa za navedene datume početka i završetka.
    - **Po satima – Ravnomerno raspoređivanje** rezerviše resurs za određeni broj časova, ravnomerno ih raspoređujući po danu tokom navedenih datuma početka i završetka.
    - **Po satima – Početno opterećenje** rezerviše resurs za određeni broj časova, raspoređujući časove rada po danu na prve dane tokom navedenih datuma početka i završetka.

    Nemojte izabrati **Nijedno** jer on dodaje resurs timu, ali ne kreira nijednu rezervaciju koja troši kapacitet resursa.
5.  Izaberite **Sačuvaj**.

    Imajte u vidu da sati rezervacije moraju da budu dovoljni da pokriju časove angažovanja i periode datuma zadataka kojima dodeljujete ovaj resurs. Ako oni nisu usklađeni, ne možete dodeliti resurs zadatku.

6.  Na strukturnoj analizi posla (SAP) za zadatak, kliknite na padajući meni ćelija resursa. Zatim: 

    1. Izaberite **Dodaj**.
    2. Izaberite padajući meni u okviru opcije **Resursi** i izaberite člana tima kojeg ste dodali iznad.
    3. Izaberite **U redu**. Član tima je sada dodeljen zadatku.

    > [!div class="mx-imgBorder"] 
    > ![Snimak ekrana dodavanja resursa pomoću SAP-a](media/FAQ-Resources-to-Tasks2-2.png "Snimak ekrana dodavanja resursa pomoću SAP-a")
 
U koordinatnoj mreži člana tima, u okviru stavke Dodeljeni časovi videćete agregirane dodeljene radne sate resursa. To će biti manje ili jednako rezervisanim časovima za resurs. 

> [!div class="mx-imgBorder"] 
> ![Snimak ekrana dodeljenih časova resursu](media/FAQ-Resources-to-Tasks2-3.png "Snimak ekrana dodeljenih časova resursu")
 
Ako zadatak koji pokušavate da dodelite resursu počinje nakon datuma završetka rezervacija resursa, resurs se neće pojaviti na padajućoj listi.

Imajte u vidu da resursu možete da dodelite više časova nego što su njegovi rezervisani časovi ako resurs ima preostali nedodeljeni kapacitet. U tom slučaju, resurs će biti samo delimično dodeljen do njegovih rezervacija. Te preostale nedodeljene sate možete da vidite dodavanjem kolone Časovi bez resursa u strukturnu analizu posla.

Ako su resursi dodeljeni svojim rezervisanim časovima (njihovi rezervisani časovi su jednaki njihovim dodeljenim časovima), videćete sledeću poruku o grešci kada pokušate da im dodelite još zadataka:

*Nije moguće dodeliti resurs zadatku – Sledeće resursi nemaju dovoljno rezervisanih radnih sati za projekat.*

Osim toga, podrazumevani član tima menadžera projekta koji je dodat u tim kada ste kreirali projekat se dodaje bez ikakvih rezervacija i nije mu moguće dodeliti nijedan zadatak. On se neće prikazivati u padajućoj listi resursa za zadatak.

Ako želite da dodelite ovaj resurs, potrebno je da ga uklonite iz tima, a zatim ponovo da ga dodate sa načinom dodele koji nije Nijedno. Razlog zbog kog se dodaju timu kada se projekat kreira jeste da bi projekat imao bar jednu podrazumevanu osobu koja odobrava projekat.

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>Kreiranje generičkog člana tima preko dodele uloga za zadatke

Ovaj metod osigurava da resursi imaju dovoljno rezervacija za zadatke. Kao prvo, kreirate čuvar mesta ili generički resurs koji opisuje karakteristike imenovanog resursa za kojeg naposletku želite da radi na zadacima generisanjem tima nakon dodele uloga zadacima. Evo kako to da uradite:

1. Na strukturnoj analizi posla, izaberite zadatak.
2. Izaberite ikonu padajućeg liste **Dodeljena uloga** u ćeliji resursa.
3. Izaberite padajuću listu **Uloga** i izaberite ulogu za generički resurs.
4. Izaberite **U redu**.

    > [!div class="mx-imgBorder"] 
    > ![Snimak ekrana korišćenja SAP-a za dodavanje resursa](media/FAQ-Resources-to-Tasks2-4.png "Snimak ekrana korišćenja SAP-a za dodavanje resursa")
 
Nakon što ste dovršili dodeljivanje uloga zadacima u SAP-u, izaberite **Generisanje projektnog tima**. Project Service kreira minimalni broj generičkih članova tima na osnovu uloga, jedinica za određivanje resursa organizacije i kalendara projekta agregiranjem dodela zadatka.

> [!div class="mx-imgBorder"] 
> ![Snimak ekrana generisanja projektnog tima](media/FAQ-Resources-to-Tasks2-5.png "Snimak ekrana generisanja projektnog tima")
 
Na koordinatnoj mreži člana tima videćete resurse tipa Generički resurs sa ulogom i imenom položaja. Ako su potrebna dva resursa za ulogu kako biste dovršili rad, funkcija Generisanje tima kreira dva člana tima i koristi ime položaja kako bi ih razlikovala.

> [!div class="mx-imgBorder"] 
> ![Snimak ekrana dodavanja dva generička resursa](media/FAQ-Resources-to-Tasks2-6.png "Snimak ekrana dodavanja dva generička resursa")
 
Možete otvoriti zahtev za pravljenje rezervne kopije resursa za generičkog člana tima tako što ćete izabrati vezu u okviru opcije Zahtev za resurs.

> [!div class="mx-imgBorder"] 
> ![Snimak ekrana otvaranja zahteva za pravljenje rezervne kopije resursa](media/FAQ-Resources-to-Tasks2-7.png "Snimak ekrana otvaranja zahteva za pravljenje rezervne kopije resursa")

Izaberite stavku **Rezerviši** za generički resurs, a zatim možete da koristite tabelu rasporeda da biste pronašli i rezervisali stvarni resurs. Možete u da prosledite zahtev za ispunjenje po menadžeru resursa tako što ćete izabrati **Prosledi zahtev**.

Kada generički resurs bude ispunjen imenovanim resursom, generički resurs se uklanja iz tima, a dodele zadatka iz generičkog resursa se dodeljuju imenovanom resursu koji je ispunio zahtev za resursom generičkog resursa.
 

