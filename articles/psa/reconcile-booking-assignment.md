---
title: Usaglašavanje resursa i dodela
description: Ova tema pruža informacije o stvarnim vrednostima.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
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
ms.openlocfilehash: 264271a5be63cb2e51f175595a48bef5fbff0a42a37795c85dd5b4725deec35e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995148"
---
# <a name="reconcile-bookings-and-assignments"></a>Usaglašavanje resursa i dodela

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Rezervacije projekta i dodele projektnih zadataka člana projektnog tima su labavo povezane. Stoga resurs može imati dodele zadataka koje ne odgovaraju rezervacijama i rezervacije koje ne odgovaraju dodelama zadataka. U idealnom slučaju, rezervacije i dodele za projekat su usklađene tako da resursi imaju potreban kapacitet da izvrše dodeljene zadatke. Međutim, realnost je da se rezervacije mogu obaviti na osnovu raspoloživosti, a vremenski raspored zadataka može se menjati kako projekt napreduje kroz svoj životni ciklus. Stoga labava povezanost omogućava fleksibilnost.

Zbog labave povezanosti rezervacija za projekat i dodela zadataka, kartica **Usaglašenost** je uključena u entitet Projekt. Ova kartica pomaže menadžerima projekata da usklade rezervacije i dodele članova projektnog tima.

Za svakog imenovanog člana tima, kartica **Usaglašenost** prikazuje rezervacije i dodele sve do nivoa dodele pojedinačnog zadatka. Prikazuje sate u ćelijama koji mogu predstavljati vremenske periode, od meseci, pa sve do dana.

U polju **Vremenska skala** možete da odaberete **Mesec**, **Nedelja** ili **Dan**. Podrazumevano je izabrana opcija **Nedelja**. Međutim, podrazumevanu vrednost možete promeniti klikom na dugme **Podešavanja**. Kada se kartica **Usaglašenost** otvori, prikazuje trenutni datum, ali pomoću kontrole kalendara možete se kretati napred ili nazad u vremenu. Kada projekat ima datum početka koji je u budućnosti, kartica prikazuje taj datum kada je otvorena. Kontrola kalendara takođe ima opcije pomoću kojih možete preći na datum početka i završetka projekta.

Možete koristiti kontrole razvijanja za svaki resurs da biste prikazali detalje rezervacija tog resursa. Takođe možete proširiti dodele svakog resursa do nivoa pojedinačnog zadatka.

U dnu kartice **Usaglašenost** prikazuje se ukupni neto iznos za projekat, a kartica takođe sadrži i kolonu Ukupno. Kartica za svaki resurs uzima u obzir razliku između rezervacija člana tima za projekat i ukupnog broja dodeljenih zadataka tog člana tima. U idealnom slučaju, razlika bi trebalo da bude 0 (nula). Drugim rečima, ne bi trebalo da postoji razlika između rezervacija resursa i dodela zadataka za resurs. Bilo kakve razlike su označene bojom i senčenjem kako biste pozvali dve pojave:

- **Nedostatak rezervacija** – Nedostatak rezervacija nastaje kada resurs ima više dodela nego rezervacija. Budući da ovaj kapacitet nije rezervisan, menadžer projekta može da koriguje tu pojavu tako što proširuje rezervacije resursa kako bi pokrio nedostatak.
- **Prekomerne rezervacije** – Prekomerna rezervacija nastaje kada je resurs rezervisan za projekat, ali nije dodeljen zadacima. Ova pojava može biti prihvatljiva, na primer ako je resurs rezervisan pre dodele zadatka. Međutim, u drugim slučajevima se možda ne planira dodeljivanje resursa. U tim slučajevima, menadžer projekta treba da razmotriti otkazivanje rezervacija resursa, tako da se kapacitet može koristiti za drugi projekat.

> [!NOTE]
> Legenda ovih pojava može da bude skrivena kako bi se ostavilo više prostora za mrežu. U ovom slučaju, legendu možete učiniti vidljivom ako kliknete na dugme **Podešavanja**.

U nekim slučajevima, kada je polje **Vremenska skala** podešeno na nivo viši od **dana**, razlike se mogu izračunati kao 0 (nula). Na primer, na nivou **meseca**, neto razlika za resurs može biti 0 (nula) što bi značilo da su rezervacije jednake dodelama. Međutim, ako gledate nivo **nedelje**, možda ćete videti da postoje dodele od 0 (nula) sati i rezervacije od 40 sati u prvoj nedelji meseca, kao i dodele od 40 sati i rezervacije od 0 (nula) sati u drugoj nedelji meseca. Iako je ukupan broj rezervacija i dodela za mesec jednak, razlikuju se po nedeljama.

Kada pregledate više nivoe vremena, kartica **Usaglašenost** prikazuje indikator ćelija koji će vas obavestiti da postoje razlike na nižim nivoima vremena. Na primer, na sledećoj ilustraciji, indikator ćelije se pojavljuje u ćeliji za mesec oktobar 2018. za resurs koji se zove Srebrenka Radić. Stoga možete videti da, iako su rezervacije i dodele resursa jednake kada su objedine na nivou **meseca**, ne podudaraju se na nižim nivoima.

![Neusaglašene rezervacije i dodele na mesečnom nivou.](media/reconcile-assignments-01.JPG)

Dvaput kliknite na ćeliju da biste povećali na prvi niži nivo i videli razliku. Na primer, ako dvaput kliknete na razliku u oktobru 2018. godine za Srebrenku Radić, dubinski ćete pretraživati do nivoa **nedelje**. Zatim možete da vidite da resurs ima rezervisanja od 16 sati, ali da nema dodele u prve dve nedelje oktobra, kao i da ima 16 sati dodela, ali ne i rezervacije u trećoj nedelji oktobra.

![Neusaglašene rezervacije i dodele na sedmičnom nivou.](media/reconcile-assignments-02.JPG)

Možete desnim tasterom miša da kliknete na ćeliju da biste umanjili naredni viši nivo. Takođe možete isključiti indikator ćelije klikom na dugme **Podešavanja**. 

Takođe možete da koristite dugmad **Prethodna** i **Sledeća** iznad mreže da biste se kretali kroz bilo kakve razlike u projektu. Da biste koristili ovu dugmad, prvo morate odabrati resurs. Izaberite **Sledeća** da pređete na sledeću razliku između rezervacija i dodela za taj resurs. Izaberite **Prethodna** da biste prešli na prethodnu razliku.

U situacijama kada imate dodele zadataka za resurs, ali nema rezervacija, možete da odaberete nedostatak rezervacija, a zatim **Produži rezervaciju**. Tada možete videti rezervaciju koja je potrebna kako biste rešili problem sa nedostatkom resursa. Takođe možete pregledati rezervacije resursa za trenutni projekat i druge projekte. Izaberite **U redu** da biste kreirali rezervaciju za resurs bez obzira na trenutnu dostupnost. Menadžer projekta ili menadžer resursa tada može da koristi tabelu rasporeda kako bi upravljao situacijama u kojima je resurs postao prekomerno rezervisan u odnosu na njegov kapacitet jer su rezervacije produžene.

## <a name="managing-with-time-zones"></a>Upravljanje vremenskim zonama
Da biste osigurali tačne i predvidljive rezultate prilikom korišćenja „Produženje rezervacije“, potrebno je ispuniti dva ključna preduslova:  

- Korisnik mora konfigurisati vremensku zonu svog uređaja kako bi odgovarala vremenskoj zoni definisanoj u podešavanjima personalizacije vašeg sistema.
 
  ![Podešavanja vremenske zone u operativnom sistemu Windows 10.](media/reconcile-assignments-03.png)

  ![Podešavanja vremenske zone u podešavanjima personalizacije.](media/reconcile-assignments-04.png)
 
- Resurs koji može da se rezerviše mora imati najmanje jedan minut radnog vremena koji se preklapa sa konturama koje se koriste za definisanje traženog produžetka. Na primer, sledeći primer prikazuje resurse za pregled sa radnim vremenima koji padaju između 9:00 i 19:00. 

  ![Poređenje kontura resursa.](media/reconcile-assignments-05.png)

Sledeća tabela prikazuje:

- Predložak kalendara projekta.
- Resurs A: ovaj resurs ima isti kalendar i nalazi se u istoj vremenskoj zoni kao i projekat. Početno vreme rezervacije će biti u 9:00.
- Resursi B: ovaj resurs se nalazi u drugoj vremenskoj zoni u odnosu na projekat i zato počinje u 7:00 u svojoj vremenskoj zoni. Međutim, rezervacije će početi u 9:00, jer je to najranije vreme početka konture zadatka.
- Resursi C i D: resursi se takođe nalaze u različitim vremenskim zonama, koje se razlikuju međusobno i unutar projekata, a njihove rezervacije ne počinju ranije od odgovarajućeg raspoloživog vremena početka.

|Entity  |Kalendar  |
|-|-|
|Predložak kalendara projekta   | ![kalendar projekta.](media/reconcile-assignments-06.png) |
|Resurs A  | ![Kalendar resursa A.](media/reconcile-assignments-06.png) |
|Resurs B  |  ![Kalendar resursa B.](media/reconcile-assignments-07.png) |
|Resurs C  |  ![Kalendar resursa C.](media/reconcile-assignments-08.png) |
|Resurs D  | ![Kalendar resursa D.](media/reconcile-assignments-09.png)  |
 
Kada pređete na prikaz usklađivanja, biće prikazane dodele resursa i povezani nedostaci rezervacije.
 ![Prikaz usklađivanja pre produžetka.](media/reconcile-assignments-10.png)

Nakon što se funkcija „Produženje rezervacije“ izvrši na svakom resoru, rezervacije se uspešno produžuju za svaki resurs. To je zato što se radno vreme svakog resursa preklapalo sa konturama nedostatka.
 ![Prikaz usklađivanja nakon produženja rezervacije.](media/reconcile-assignments-11.png) 

Međutim, bolji pogled na detalje rezervacije pokazuje razlike u vremenu početka rezervacija. Rezervacije neće početi ranije od vremena početka konture zadatka i ne ranije od raspoloživog vremena početka resursa.
 ![Nove rezervacije resursa na tabeli rasporeda.](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]