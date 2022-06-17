---
title: Dodavanje članova tima iz mreže članova tima
description: Ovaj članak pruža informacije o tome kako možete da upravljate resursima članova tima.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3c0c277ca1fe2b709a6ff1c626f5ea7ec63705d6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928587"
---
# <a name="add-team-members-from-the-team-member-grid"></a>Dodavanje članova tima iz mreže članova tima

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Dynamics 365 Project Operations uključuje kontrolnu tablu menadžera resursa koja pruža vizuelni pregled potražnje i ukupne iskorišćenosti resursa u celoj organizaciji. Možete koristiti grafikone na ovoj kontrolnoj tabli da biste vizualizovali sledeće informacije:

- **Potražnja za resursima**: Grafikon **Aktivni zahtevi za resursima** prikazuje resurse koji su prosleđeni. Resursi se objedinjuju po ulozi ili projektu.
- **Neprosleđena potražnja za resursima**: Grafikon **Nedodeljena potražnja za resursima** prikazuje sve zahteve za resursima koji nisu prosleđeni. Ovaj grafikon pomaže menadžerima resursa da pogledaju potražnju koja nije čvrsta i koja može biti prosleđena putem zahteva za resurse.
- **Naplativa ukupna iskorišćenost tokom prošle sedmice**: Grafikon **Ukupna iskorišćenost prema ulozi** prikazuje procenat stvarne ukupne iskorišćenosti prema ulogama u organizaciji u odnosu na ciljanu naplativu ukupnu iskorišćenost po ulozi.

    > [!NOTE]
    > Da bi grafikon **Ukupna iskorišćenost prema ulozi** bio dostupan, kreirajte posao koji pokreće tok posla **UpdateRoleUtilization**. Ovaj periodičan posao se pokreće svakih sedam dana kako bi se izračunala naplativa ukupna iskorišćenost za prethodnih sedam dana. Rezultati se objedinjuju po ulogama.

## <a name="manage-project-team-members"></a>Upravljanje članovima projektnog tima

Menadžeri projekata mogu koristiti kontrolnu tablu za menadžere resursa koji će upravljati resursima na projektima. Na primer, mogu da dodaju člana tima direktno u projekat i rezervišu člana tima da ispune potrebe za resursima koje je evidentirao generički resurs.

### <a name="add-a-team-member-directly-to-a-project"></a>Dodavanje člana tima direktno u projekat

Da biste direktno dodali člana tima u projekat, u obrascu **Projekti**, na kartici **Tim** izaberite **Novi**. Pojaviće se dijalog **Brzo kreiranje člana projektnog tima**. U ovom dijalogu možete izvršiti ove zadatke:

- **Rezervisanje imenovanog resursa**: U polju **Resurs koji može da se rezerviše** izaberite ime resursa. Zatim izaberite ulogu, podesite period i izaberite način dodeljivanja. Imenovani resurs koji ste odabrali dodaje se projektu upotrebom odabranog načina dodele i kalendara resursa.
- **Dodavanje generičkog resursa**: Ostavite polje **Resurs koji može da se rezerviše** prazno, a zatim izaberite ulogu, podesite period i izaberite željeni način dodeljivanja. Generički resurs se dodaje timu kao čuvar mesta. Rezervisano mesto sadrži obrazac potražnje koji se koristi za rezervisanje imenovanih resursa u timu. Zahtev se postavlja prema kalendaru projekta.
- **Dodavanje imenovanog resursa u tim bez trošenja kapaciteta resursa**: U polju **Resurs koji može da se rezerviše** izaberite resurs. Izaberite period, a zatim izaberite **Nijedan** kao način dodeljivanja. Resurs se dodaje u tim, ali kapacitet resursa se ne troši rezervacijom.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Rezervisanje člana tima radi ispunjavanja potrebe za generičkim resursom

U usluzi Project Operations možete rezervisati generički resurs za projektni tim. Takođe možete odrediti ulogu, potreban kapacitet i način na koji se taj kapacitet distribuira. Za potrebu za resursom možete da navedete atribute koji su povezani sa generičkim resursom. Ovi atributi uključuju tražene veštine, željenu organizacionu jedinicu i željene resurse.

Obavite sledeće korake da biste naveli potrebne veštine generičkog resursa za programera.

1. U obrascu **Projekti**, na kartici **Tim**, izaberite **Novi** da biste rezervisali generički resurs.
2. U prikazu **Svi članovi tima**, u koloni **Potreba za resursom** izaberite vezu da dodate potrebne veštine za generički resurs.
3. U obrascu **Zahtev za resursom**, u mreži **Veštine** izaberite tri tačke (**...**), a zatim izaberite **Dodaj novu karakteristiku zahteva** da biste dodali potrebne veštine za programera.
4. U obrascu dijaloga **Brzo kreiranje: Karakteristike zahteva**, u polju **Karakteristike** izaberite željenu veštinu.
5. U polju **Vrednost ocene** izaberite nivo stručnosti za ovu veštinu. 
6. U polju **Zahtev za resursom** podesite zahtev da biste obezbedili izvorne resurse iz organizacionih jedinica ili čak imenovanih resursa. Kada završite, izaberite **Sačuvaj**.
7. U obrascu **Zahtev za resursom** izaberite **Rezerviši** da biste ispunili zahtev za resursom. Takođe možete odabrati generički resurs u mreži **Svi članovi tima**, a zatim izabrati **Rezerviši**.

    > [!NOTE]
    > U ovom primeru, postoji 40 zahtevanih sati, ali nema stvarno rezervisanih sati, jer generički resursi nemaju rezervacije. Pored toga, nema dodeljenih sati, jer je generički resurs dodat direktno u tim umesto da je dodat korišćenjem dodele zadatka.

    U obrascu **Pomoćnik za planiranje** možete filtrirati dostupne resurse prema potrebama koje su navedene u potrebi za resursom. Resursi su sortirani prema parametrima sortiranja koji su navedeni na tabeli rasporeda.

   Neki od najčešće korišćenih filtera su:

    - **Karakteristike uz ocenu**: Filtrirajte po veštinama, certifikacijama i drugim kvalitetima resursa, pored ocena stručnosti.
    - **Uloge**: Filtrirajte prema podrazumevanim ulogama koje su dodeljene resursima koji mogu da se rezervišu.
    - **Organizacione jedinice**: Filtrirajte resurse koji mogu da se rezervišu prema organizacionim jedinicama kojima su dodeljeni.

8. Ako niste zadovoljni rezultatima inicijalne pretrage zahteva, možete promeniti kriterijume filtriranja. Proširite okno **Prikaz filtera** sa leve strane, a zatim izaberite **Pretraži** da biste pronašli dodatne resurse. Da biste promenili način sortiranja rezultata, izaberite **Sortiraj**.
9. Odaberite resurse u skladu sa potražnjom koja je navedena u zahtevu, kao što je naznačeno u vrhu mreže. Možete izbrisati izbor ćelija u mreži i ostaviti otvoren kapacitet resursa. Samo jedan resurs može biti izabran kao rezervisan u određenom trenutku.
10. Izaberite **Rezerviši** da rezervišete izabrani resurs i ostavite tabelu rasporeda otvorenu, tako da možete da izaberete dodatne resurse. Ili odaberite **Rezerviši i izađi** da rezervišete izabrani resurs i zatvorite tabelu rasporeda.
11. Vratite se na prikaz **Svi članovi tima**. U mreži možete da primetite da je generički resurs zamenjen imenovanim resursom i da je 40 sati navedeno kao rezervisano za taj resurs.

    > [!NOTE]
    > Nisu prikazani dodeljeni sati jer su rezervisani direktno u timu. Nisu rezervisani korišćenjem dodela zadatka.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Dodeljivanje generičkih resursa zadacima i generisanje potreba za resursima

U usluzi Project Operations možete da kreirate zadatke i da im onda dodelite generičke resurse. Potražnja za resursima potom može biti predstavljena čuvarima mesta dok procenjujete svoj raspored i finansijske pokazatelje. Zatim možete da generišete potrebe za generičkim resursima i ispunite ih.

1. U obrascu **Projekti**, na kartici **Raspored** izaberite **Dodaj** da kreirate zadatak.
2. U polju **Resursi** izaberite simbol **birača resursa**. Pojavljuje se birač resursa i pokazuje postojeće članove tima za projekat.
3. Unesite ime novog generičkog resursa, a zatim izaberite **Kreiraj**.
4. U dijalogu **Brzo kreiranje člana projektnog tima** koji se pojavljuje, u polju **Uloga** odaberite ulogu generičkog resursa. 
5. U polju **Jedinica za obezbeđivanje resursa** izaberite organizacionu jedinicu za generički resurs. Zatim izaberite **Sačuvaj**. Generički član tima je sada dodeljen zadatku.

   Na kartici **Tim** videćete novog generičkog člana tima. Imajte na umu da ima samo dodeljene sate. Ovi časovi su zbir svih zadataka koji su dodeljeni generičkom članu tima. Generički član tima nema zahtevane sate niti potrebu za resursom.

6. Sada možete dodeliti generičkog člana tima drugim zadacima pomoću birača resursa.

   Kada završite sa dodeljivanjem generičkog resursa zadacima, možete da generišete potrebu za generičkim resursom.

7. Na kartici **Tim** izaberite generički resurs, a zatim izaberite **Generiši zahtev**. Kada se zahtev generiše, član generičkog tima će imati zahtevane sate i vezu ka potrebi za resursom.

  Kada rezervišete imenovani resurs, generički resurs se uklanja iz tima i zamenjuje imenovanim resursom. Na kartici **Raspored** se dodele generičkim resursima uklanjaju i zamenjuju imenovanim resursom.

  > [!NOTE]
  > Ovo ponašanje se dešava samo kada je imenovani resurs u potpunosti rezervisan za potrebu za generičkim resursom. Kada imenovani resurs delimično zamenjuje potrebu za generičkim resursom ili više imenovanih resursa zamenjuje potrebu za generičkim resursima, generički resurs ostaje dodeljen zadatku.

Project Operations ne dodeljuje oba resursa zadatku, jer bi takvim ponašanjem nastao manje predvidljiv raspored. U ovom jednostavnom primeru lako je podjednako podeliti sate na dva resursa. Međutim, u složenijim scenarijima koji uključuju više zadataka i više resursa, PSA bi morao da pretpostavi kako treba da rasporedi rezervacije koje su primljene za više resursa u više zadataka.

Stoga je u tim scenarijima menadžer projekta odgovoran za raščlanjivanje više rezervacija i njihovo dodeljivanje prema potrebi. Da bi dodelio rezervacije, menadžer projekta dodeljuje zadatke iz generičkih resursa imenovanim resursima i zatim koristi prikaz **Usaglašenost** da bi osigurao da dodela funkcioniše sa rezervacijama.

### <a name="edit-a-resource-requirement"></a>Uređivanje potrebe za resursom

Kada kreira zahtev za resursom, menadžer projekta ili menadžer resursa možda će možda morati da izmeni detalje kako bi precizirao kriterijume za pretragu kada se koristi tabela rasporeda. Da biste uredili potrebu za resursom, sledite ove korake.

1. U obrascu **Projekti**, na kartici **Tim**, izaberite vezu ka bilo kom zahtevu za generički resurs.
2. U obrascu **Zahtev za resursima** koji se pojavi, unesite potrebne podatke o polju

   U obrascu **Zahtev za resursima**, menadžer projekta ili menadžer resursa takođe mogu da definišu veštine, uloge, željene opcije resursa i željenu organizacionu jedinicu.

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Ažuriranje rezervacija resursa nakon njihovog rezervisanja za projekat

Nakon što dodate generički ili imenovani resurs u projektni tim, možete promeniti rezervacije resursa.

1. U obrascu **Projekti**, na kartici **Tim**, izaberite člana tima, a zatim izaberite **Održavanje rezervacija**.
 
   Pojavljuje se tabela rasporeda i prikazuje rezervacije člana projektnog tima. Proširite evidenciju člana tima da biste videli sate koji su rezervisani za ovaj projekat i druge projekte koji troše kapacitet člana tima.

2. Izaberite i prevucite rezervaciju da biste je proširili ili skratili. Pojaviće se dijalog **Kreiranje rezervacije resursa** koji vam omogućava da podesite rezervaciju.
3. Kliknite desnim tasterom miša na rezervaciju. Zatim možete da koristite meni sa prečicama da biste dovršili sledeće radnje:

    - Promena statusa rezervacije
    - Uređivanje rezervacije
    - Zamena resursa u projektnom timu

### <a name="change-the-booking-status"></a>Promena statusa rezervacije

Možete promeniti bilo koji podrazumevani ili prilagođeni status rezervacije.

Sledeći statusi su uvršteni u Project Operations:

- **Otkazano**: Otkazuje rezervaciju resursa i oslobađa kapacitet resursa.
- **Fiksna rezervacija**: Troši kapacitet resursa. Rezervacija obično ima ovaj status kada otvorite stranicu **Održavanje rezervacija** na mreži **Svi članovi tima** u obrascu **Projekti**.
- **Uslovna rezervacija**: Dodaje resurs u tim, ali ne troši njegov kapacitet. Ovaj status ukazuje na to da je resurs rezervisan za potencijalni rad, ali još uvek ima kapacitet ako je potreban na drugim poslovima. S obzirom na ukupnu dostupnost resursa, uslovne rezervacije imaju drugačiji status od fiksnih rezervacija.
- **Predložen**: Predstavlja predlog menadžera resursa ili menadžera projekta za resurs. Predlozi ne troše kapacitet resursa i resurs se ne dodaje projektnom timu. Da bi rezervacija resursa za tim bila fiksna, menadžer projekta mora da prihvati predlog.

### <a name="submit-resource-requests"></a>Prosleđivanje zahteva za resursom

Zahtevi za resurse se koriste da prenesu potražnju (ili zahtev za resursima) koju mora da ispuni menadžer resursa. Za generički resurs koji je već u timu možete direktno da prosledite zahtev za resurs. Zahtev za resurs može se ispuniti na dva načina:

- Menadžer resursa direktno ispunjava zahtev. U ovom slučaju, generički resurs zamenjuje fiksna rezervacija koja ima imenovani resurs.
- Menadžer resursa predlaže resurs menadžeru projekata, a menadžer projekta odobrava ili odbacuje predloženi resurs.

#### <a name="direct-fulfillment-of-resource-requests"></a>Direktno ispunjavanje zahteva za resurse

Kada se generiše potreba za resursom, menadžer projekta može da prosledi zahtev za generički resurs ako izabere resurs, a zatim opciju **Prosledi zahtev**. Komentari o resursu mogu se dostaviti menadžeru resursa koji ispunjava zahtev. Nakon prosleđivanja zahteva, polje **Status** za člana tima se menja u **Prosleđen**. Kada menadžer resursa ispuni zahtev, generičkog člana tima zamenjuje imenovani resurs u mreži **Svi članovi tima**.

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Korišćenje predloga resursa za zahteve za resurse

Umesto da direktno rezerviše resurs u zahtevu za resurse, menadžer resursa može da predloži resurs menadžeru projekta. Menadžer resursa mogao bi koristiti ovu opciju kada nije dostupno tačno podudaranje sa zahtevima. Kada menadžer resursa predloži resurs, menadžer projekata vidi da je polje **Status** za generičkog člana tima promenjeno u **Zahteva pregled**.

Možete pogledati predloženi resurs zajedno sa vizuelizacijom efekta rezervacije predloga. 

1. Dvaput kliknite na člana tima koji ima status **Potreban pregled**. 
2. Izaberite karticu **Predloženi resursi**.
3. Izaberite **Prihvati sve predloge** da prihvate sve predložene resurse ili **Odbacite sve predloge** da ih odbacite. Ako prihvatite predložene resurse, oni se fiksno rezervišu za projekat kao članovi tima i zamenjuju generičke resurse.

> [!NOTE]
> Morate ili prihvatiti ili odbaciti sve predložene resurse. Ne možete ih delimično prihvatiti ni odbaciti.

### <a name="substitute-a-resource-on-the-project-team"></a>Zamena resursa u projektnom timu

Ponekad menadžer projekta mora zameniti rezervisanog člana tima za projekat.

1. U obrascu **Projekti**, na kartici **Tim**, izaberite resurs kojem je potrebna zamena, a zatim izaberite **Održavanje rezervacija**.
2. Proširite resurs za pregled projekata kojima je dodeljen.
3. Kliknite desnim tasterom miša na projekat, a zatim izaberite **Zamena resursa**.
4. Ako znate resurs koji želite da zamenite trenutnim resursom, izaberite ili unesite ime, a zatim izaberite **Ponovo dodeli**.

Ili. ako treba da potražiti resurs, izvršite sledeće korake.

1. Izaberite **Pronalaženje zamene**.

   Pomoćnik za zakazivanje prikazuje listu dostupnih zamena. U pomoćniku za zakazivanje možete dodatno filtrirati dostupne resurse da biste pronašli odgovarajuću zamenu.

2. Da biste zamenili resurs, odaberite resurs koji želite, a zatim izaberite **Zameni**.   

   Rezervacije i dodele zamenjuju se novim resursom.

## <a name="reconcile-team-member-bookings-and-assignments"></a>Usaglašavanje rezervacija i dodela članova tima

Za članove tima, rezervacije i dodele su labavo povezane. Drugim rečima, resursi mogu imati dodele, ali ne i rezervacije ili mogu imati rezervacije, ali ne i dodele. U idealnom slučaju, rezervacije i dodele treba da se usklade tako da resursi imaju potreban kapacitet da izvrše dodeljene zadatke. Međutim, rezervacije se mogu zasnivati na dostupnosti, a vremenski raspored zadataka može se menjati tokom projekta. Stoga, labava povezanost rezervacija i dodela pruža fleksibilnost.

Project Operations ima karticu **Usaglašavanje** koja omogućava menadžerima projekata da usaglase rezervacije članova tima i njihove dodele za projektne timove.

Kartica **Usaglašenost** prikazuje rezervacije i dodele sve do nivoa dodele pojedinačnog zadatka za svakog člana tima. Prikazuje sate u ćelijama koji predstavljaju vremenske periode, od meseci, pa sve do dana.

Kartica takođe prikazuje ukupni neto iznos projekta, zajedno sa kolonom za ukupnu vrednost.

Kartica za svaki resurs izračunava razliku između rezervacija člana tima i ukupnog broja dodeljenih zadataka člana tima. U idealnom slučaju, ta razlika bi trebalo da bude 0 (nula). Drugim rečima, ne bi trebalo da postoji razlika između rezervacija i dodela. Razlike su obojene i zasenčene kako bi se skrenula pažnja na dve pojave:

- **Nedostatak rezervacija**: Nastaje kada resurs ima više dodela nego rezervacija. Budući da ovaj kapacitet nije rezervisan, menadžer projekta može da koriguje tu pojavu proširivanjem rezervacija resursa kako bi pokrio nedostatak.
- **Prekomerne rezervacije**: Nastaje kada je resurs rezervisan za projekat, ali nije dodeljen zadacima. Ta pojava može biti prihvatljiva u slučajevima kada je resurs rezervisan za projekat pre dodele zadatka. Međutim, u drugim slučajevima se ne planira dodeljivanje resursa zadacima. U tim slučajevima, menadžer projekta treba da razmotri otkazivanje rezervacija resursa, tako da kapacitet može da se koristi za drugi projekat.

U nekim slučajevima, kada pregledate vreme na višem nivou od nivoa dana, npr. na mesečnom nivou, možda ćete videti neto razliku koja je nula za resurs. Drugim rečima, rezervacije = dodele. Međutim, ako pregledate vreme na nivou nedelje, možda ćete videti da postoje dodele od nula sati i rezervacije od 40 sati u prvoj nedelji, ali dodele od 40 sati i rezervacije od nula sati u drugoj nedelji. Sve u svemu, rezervacije i dodele se usklađuju, ali se razlikuju od jedne do druge nedelje.

Kada pregledate vreme na višim nivoima, ćelije na kartici **Usaglašenost** imaju indikator koji će vas obavestiti da postoje razlike na nižim nivoima. Dvaput kliknite na ćeliju možete da je povećate kako biste videli razliku. Zatim možete da kliknite desnim tasterom miša da biste je umanjili. Ako izaberete resurs, a zatim izaberete kontrolu **Sledeća razlika** na traci sa alatkama mreže, možete preći na sledeću razliku između rezervacija i dodela za taj resurs. Izaberite **Prethodna razlika** da se vratite. Takođe možete isključiti indikator razlike i ponašanje u navigaciji u delu **Podešavanja**.

Ako imate dodele zadataka za resurs, ali nema rezervacija, na obrascu **Projekti** na kartici **Usaglašavanje** izaberite nedostatak rezervacija, a zatim **Produži rezervaciju**. Pojavljuje se dijalog **Produženje rezervacije** i prikazuje rezervaciju koja je potrebna da se reši problem sa nedostatkom resursa. Dijalog takođe pokazuje postojeće rezervacije resursa za sve projekte ili druge entitete koji se mogu zakazivati. Ako izaberete **U redu** da biste kreirali rezervaciju za resurs, bez obzira na dostupnost tog resursa, možete prouzrokovati prekomernu rezervaciju.

Menadžer projekta ili menadžer resursa tada može da koristi tabelu rasporeda kako bi upravljao bilo kojom situacijom u kojoj je resurs prekomerno rezervisan u odnosu na njegov kapacitet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]