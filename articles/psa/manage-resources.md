---
title: Upravljanje resursima
description: Ova tema pruža informacije o tome kako možete da upravljate resursima.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 548595e3951f824e1c79a641d3f336e381fcaaf9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132350"
---
# <a name="manage-resources"></a>Upravljanje resursima

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation uključuje kontrolnu tablu menadžera resursa koja pruža vizuelni pregled potražnje i ukupne iskorišćenosti resursa u celoj organizaciji. Možete koristiti grafikone na ovoj kontrolnoj tabli da biste vizualizovali sledeće informacije:

- **Potražnja za resursima** - Grafikon **Aktivni zahtevi za resurse** prikazuje resurse koji su prosleđeni. Resursi se objedinjuju po ulozi ili projektu.
- **Neprosleđena potražnja za resursima** - Grafikon **Nedodeljena potražnja za resursima** prikazuje sve potrebe za resursima koje nisu prosleđene. To pomaže menadžerima resursa da pogledaju potražnju koja nije čvrsta i koja može biti prosleđena putem zahteva za resurse.
- **Naplativa ukupna iskorišćenost tokom prošle sedmice** - Grafikon **Ukupna iskorišćenost prema ulozi** prikazuje procenat stvarne ukupne iskorišćenosti prema ulogama u organizaciji u odnosu na ciljanu naplativu ukupnu iskorišćenost po ulozi.

    > [!NOTE]
    > Da bi grafikon **Ukupna iskorišćenost prema ulozi** bio dostupan, kreirajte posao koji pokreće tok posla UpdateRoleUtilization. Ovaj periodičan posao se pokreće svakih sedam dana kako bi se izračunala naplativa ukupna iskorišćenost za prethodnih sedam dana. Rezultati se objedinjuju po ulogama.

## <a name="manage-project-team-members"></a>Upravljanje članovima projektnog tima

Menadžeri projekata mogu koristiti kontrolnu tablu za upravitelje resursima za upravljanje resursima na projektima. Na primer, mogu da dodaju člana tima direktno u projekat i rezervišu člana tima da ispune potrebe za resursima koje je evidentirao generički resurs.

### <a name="add-a-team-member-directly-to-a-project"></a>Dodavanje člana tima direktno u projekat

Da biste direktno dodali člana tima u projekat, na stranici **Projekti**, na kartici **Tim** odaberite **Novi**. Pojaviće se dijalog **Brzo kreiranje člana projektnog tima**. U ovom dijalogu možete izvršiti ove zadatke:

- **Rezervisanje imenovanog resursa** - U polju **Resurs koji može da se rezerviše** odaberite ime resursa. Zatim izaberite ulogu, podesite period i izaberite način dodeljivanja. Imenovani resurs koji ste odabrali dodaje se projektu upotrebom odabranog načina dodele i kalendara resursa.
- **Dodavanje generičkog resursa** - Ostavite polje **Resurs koji može da se rezerviše** prazno, a zatim odaberite ulogu, podesite period i izaberite željeni način dodeljivanja. U tim se dodaje generički resurs kao čuvar mesta koji sadrži obrazac potražnje koji se koristi za rezervisanje imenovanih resursa za tim. Zahtev se postavlja prema kalendaru projekta.
- **Dodavanje imenovanog resursa u tim bez trošenja kapaciteta resursa** - U polju **Resurs koji može da se rezerviše** odaberite resurs. Zatim izaberite period i izaberite **Nijedan** kao način dodeljivanja. Resurs se dodaje u tim, ali kapacitet resursa se ne troši rezervacijom.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Rezervisanje člana tima radi ispunjavanja potrebe za generičkim resursom

U aplikaciji PSA možete da rezervišete generički resurs za projektni tim i možete da odredite ulogu, potrebni kapacitet i kako se taj kapacitet distribuira. U okviru potrebe za resursom možete da navedete atribute koji su povezani sa generičkim resursom. Ovi atributi uključuju tražene veštine, željenu organizacionu jedinicu i željene resurse.

Sledite ove korake da biste naveli potrebne veštine generičkog resursa za programera.

1. Na stranici **Projekti** na kartici **Tim** odaberite **Novi** da rezervišete generički resurs.

    ![Generički resurs rezervisan za tim](media/Resource-Management-image9.png)

2. U prikazu **Svi članovi tima**, u koloni **Potreba za resursom** izaberite vezu da dodate potrebne veštine za generički resurs.

    ![Veza zahteva](media/Resource-Management-image10.png)

3. Na stranici **Potreba za resursom** koja se pojavljuje u mreži **Veštine** odaberite tri tačke (**...**), a zatim izaberite **Dodaj novu karakteristiku zahteva** da dodate potrebne veštine za programera.

    ![Komanda za dodavanje nove karakteristike zahteva](media/Resource-Management-image11.png)

4. U dijalogu **Brzo kreiranje karakteristike zahteva** koji se pojavljuje, u polju **Karakteristike** odaberite željenu veštinu. Zatim, u polju **Vrednost ocene** odaberite nivo stručnosti za ovu veštinu. Konačno u polju **Potreba za resursom** podesite potrebu da biste obezbedili resurse iz organizacionih jedinica ili čak imenovanih resursa. Kada završite, izaberite **Sačuvaj**.

    ![Dijalog za brzo kreiranje karakteristika zahteva](media/Resource-Management-image12.png)

5. Na stranici **Potreba za resursom** izaberite **Rezerviši** da biste ispunili potrebu za resursom.

    ![Dugme za rezervisanje na stranici Potreba za resursom](media/Resource-Management-image13.png)

    Takođe možete odabrati generički resurs u mreži **Svi članovi tima**, a zatim izabrati **Rezerviši**.

    ![Dugme za rezervaciju iznad mreže Svi članovi tima](media/Resource-Management-image14.png)

    > [!NOTE]
    > U ovom primeru, postoji 40 zahtevanih sati, ali nema stvarno rezerviranih sati, jer generički resursi nemaju rezervacije. Uz to, nema dodeljenih sati, jer je generički resurs dodat direktno u tim. Nije dodat dodeljivanjem zadatka.

    Na stranici **Pomoćnik za zakazivanje** možete filtrirati dostupne resurse prema potrebama koje su navedene u potrebi za resursom. Resursi su sortirani prema parametrima sortiranja koji su navedeni na tabeli rasporeda.

    ![Stranica Pomoćnik za zakazivanje](media/Resource-Management-image15.png)

    Evo nekoliko filtera koji se često koriste:

    - **Karakteristike uz ocenu** - Filtrirajte po veštinama, certifikacijama i drugim kvalitetima resursa, pored ocena stručnosti.
    - **Uloge** - Filtrirajte prema podrazumevanim ulogama koje su dodeljene resursima koji mogu da se rezervišu.
    - **Organizacione jedinice** - Filtrirajte resurse koji mogu da se rezervišu prema organizacionim jedinicama kojima su dodeljeni.

6. Ako niste zadovoljni rezultatima inicijalne pretrage zahteva, možete promeniti kriterijume filtriranja. Proširite okno **Prikaz filtera** sa leve strane, a zatim izaberite **Pretraži** da biste pronašli dodatne resurse.

    ![Okno sa prikazom filtera](media/Resource-Management-image16.png)

7. Da biste promenili način sortiranja rezultata, izaberite **Sortiraj**.

    ![Komanda za sortiranje](media/Resource-Management-image17.png)

8. Odaberite resurse u skladu sa potražnjom koja je navedena u zahtevu, kao što je naznačeno u vrhu mreže. Možete izbrisati izbor ćelija u mreži i ostaviti otvoren kapacitet resursa. Samo jedan resurs može biti izabran kao rezervisan u određenom trenutku.

9. Izaberite **Rezerviši** da rezervišete izabrani resurs i ostavite tabelu rasporeda otvorenu, tako da možete da izaberete dodatne resurse. Ili odaberite **Rezerviši i izađi** da rezervišete izabrani resurs i zatvorite tabelu rasporeda.

    ![Resurs za rezervaciju](media/Resource-Management-image19.png)

    Dobijate obaveštenje o rezervisanim satima. Pokazatelji potražnje pokazuju koliko je zahtev za rezervaciju ispunjen i koliko još ostaje. Takođe možete videti koliko je potrošeno kapaciteta odabranog resursa. Izaberite **Proširi** da biste videli više detalja o rezervacijama resursa.

9. Vratite se na prikaz **Svi članovi tima**. U mreži možete da primetite da je generički resurs zamenjen imenovanim resursom i da je 40 sati navedeno kao rezervirano za taj resurs.

    ![Mreža Ažurirani svi članovi tima](media/Resource-Management-image20.png)

    > [!NOTE]
    > Nisu prikazani dodeljeni sati jer su rezervisani direktno u timu. Nisu rezervisani korišćenjem dodela zadatka.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Dodeljivanje generičkih resursa zadacima i generisanje potreba za resursima

U aplikaciji PSA možete da kreirate zadatke i da im onda dodelite generičke resurse. Na ovaj način, potražnja za resursima može biti predstavljena čuvarima mesta dok procenjujete svoj raspored i finansijske brojke. Zatim možete da generišete potrebe za generičkim resursima i ispunite ih.

1. Na stranici **Projekti** na kartici **Raspored** odaberite **Dodaj** da kreirate zadatak.

    ![Kreiran je novi zadatak](media/Resource-Management-image21.png)

2. U polju **Resursi** izaberite simbol **birača resursa**. Pojavljuje se birač resursa i pokazuje postojeće članove tima za projekat.

    ![Birač resursa](media/Resource-Management-image22.png)

3. Unesite ime novog generičkog resursa, a zatim izaberite **Kreiraj**.

    ![Uneto je ime novog generičkog resursa](media/Resource-Management-image23.png)

4. U dijalogu **Brzo kreiranje člana projektnog tima** koji se pojavljuje, u polju **Uloga** odaberite ulogu generičkog resursa. U polju **Jedinica za obezbeđivanje resursa** izaberite organizacionu jedinicu za generički resurs. Zatim izaberite **Sačuvaj**.

    ![Dijalog za brzo kreiranje člana projektnog tima](media/Resource-Management-image24.png)

    Generički član tima je sada dodeljen zadatku.

    ![Generički član tima je dodeljen zadatku](media/Resource-Management-image25.png)

    Na kartici **Tim** videćete novog generičkog člana tima. Imajte na umu da ima samo dodeljene sate. Ovi časovi su zbir svih zadataka koji su dodeljeni generičkom članu tima. Generički član tima još uvek nema zahtevane sate niti potrebu za resursom.

    ![Generički član tima na kartici Tim](media/Resource-Management-image26.png)

5. Sada možete dodeliti generičkog člana tima drugim zadacima pomoću birača resursa.

    ![Generički član tima u biraču resursa](media/Resource-Management-image27.png)

    Kada završite sa dodeljivanjem generičkog resursa zadacima, možete da generišete potrebu za generičkim resursom.

5. Na kartici **Tim** izaberite generički resurs, a zatim izaberite **Generiši zahtev**.

    ![Komanda za generisanje zahteva](media/Resource-Management-image28.png)

    Kada se zahtev generiše, član generičkog tima će imati zahtevane sate i vezu ka potrebi za resursom.

    ![Veza ka potrebi za resursom](media/Resource-Management-image29.png)

    Kada rezervišete imenovani resurs, generički resurs se uklanja iz tima i zamenjuje imenovanim resursom.

    ![Generički resurs je zamenjen imenovanim resursom](media/Resource-Management-image30.png)

    Na kartici **Raspored** se dodele generičkim resursima uklanjaju i zamenjuju imenovanim resursom.

    ![Dodele generičkim resursima su zamenjene imenovanim resursom na kartici Raspored](media/Resource-Management-image31.png)

    > [!NOTE]
    > Ovo ponašanje se dešava samo kada je imenovani resurs u potpunosti rezervisan za potrebu za generičkim resursom. Kada imenovani resurs delimično zamenjuje potrebu za generičkim resursom ili više imenovanih resursa zamenjuje potrebu za generičkim resursima, generički resurs ostaje dodeljen zadatku.

    Na sledećoj ilustraciji, zadatak od 80 sati je planiran za period od pet dana (16 sati dnevno tokom pet dana) i dodeljen je generičkom resursu koji se zove **Funkcionalni**.

    ![Osamdesetčasovni zadatak za pet dana je dodeljen funkcionalnom generičkom resursu](media/Resource-Management-image32.png)

    Kada generišete zahtev, on je za 80 sati tokom petodnevnog perioda.

    ![Zahtev je generisan za 80 sati tokom pet dana](media/Resource-Management-image33.png)

    Budući da dostupni resursi rade samo osam sati dnevno, potrebna su dva resursa da bi se ispunio zahtev.

    ![Drugi resurs](media/Resource-Management-image35.png)

    Na kartici **Tim** sada možete videti da generički resurs nema zahtevane sate, ali dodeljeni sati se i dalje pojavljuju zajedno sa dva imenovana resursa koja čine ispunjenje.

    ![Dva imenovana resursa na kartici Tim](media/Resource-Management-image36.png)

    Na kartici **Raspored** generički resurs ostaje dodeljen zadatku.

    ![Generički resursi na kartici Raspored](media/Resource-Management-image37.png)

PSA ne dodeljuje oba resursa zadatku, jer bi takvim ponašanjem nastao manje predvidljiv raspored. U ovom jednostavnom primeru lako je podjednako podeliti sate na dva resursa. Međutim, u složenijim scenarijima koji uključuju više zadataka i više resursa, PSA bi morao da pretpostavi kako treba da rasporedi rezervacije koje su primljene za više resursa u više zadataka.

Stoga je u tim scenarijima rukovodilac projekta odgovoran za raščlanjivanje više rezervacija i njihovo dodeljivanje prema potrebi. Da bi dodelio rezervacije, menadžer projekta dodeljuje zadatke iz generičkih resursa imenovanim resursima i zatim koristi prikaz **Usaglašenost** da bi osigurao da dodela funkcioniše sa rezervacijama.

### <a name="edit-a-resource-requirement"></a>Uređivanje potrebe za resursom

Nakon što kreira potrebu za resursom, menadžer projekta ili menadžer resursa možda će želeti da izmeni detalje kako bi precizirao kriterijume za pretragu kada se koristi tabela rasporeda. Da biste uredili potrebu za resursom, sledite ove korake.

1. Na stranici **Projekti** na kartici **Tim** odaberite vezu ka bilo kom zahtevu za generički resurs.
2. Na stranici **Potreba za resursom** koja se pojavljuje možete ažurirati nekoliko atributa. U nastavku su navedeni neki primeri:

    - Ime
    - Od datuma
    - Do datuma
    - Trajanje
    - Tip resursa

Na stranici **Potreba za resursom** menadžer projekta ili menadžer resursa takođe može definisati sledeće informacije:

- Veštine
- Uloge
- Željene postavke resursa
- Željenu organizacionu jedinicu

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Ažuriranje rezervacija resursa nakon njihovog rezervisanja za projekat

Nakon što dodate generički ili imenovani resurs u projektni tim, možete promeniti rezervacije resursa.

1. Na stranici **Projekti** na kartici **Tim** odaberite člana tima, a zatim izaberite **Održavanje rezervacija**.

    ![Tabela rasporeda se otvara za izabranog člana tima](media/Resource-Management-image40.png)

    Pojavljuje se tabela rasporeda i prikazuje rezervacije člana projektnog tima. Proširite evidenciju člana tima da biste videli sate koji su rezervisani za ovaj projekat i druge projekte koji troše kapacitet člana tima.

2. Izaberite i prevucite rezervaciju da biste je proširili ili skratili. Pojaviće se dijalog **Kreiranje rezervacije resursa** koji vam omogućava da podesite rezervaciju.

    ![Dijalog za kreiranje rezervacije resursa](media/Resource-Management-image41.png)

3. Kliknite desnim tasterom miša na rezervaciju. Zatim možete da koristite meni sa prečicama da biste dovršili sledeće radnje:

    - Promenite status rezervacije.
    - Uredite rezervaciju.
    - Zamenite resurs u projektnom timu.

### <a name="change-the-booking-status"></a>Promena statusa rezervacije

Možete promeniti bilo koji podrazumevani ili prilagođeni status rezervacije.

![Komanda za promenu statusa](media/Resource-Management-image42.png)

Sledeći statusi su uvršteni u PSA:

- **Otkazan** - Ovaj status otkazuje rezervaciju resursa i oslobađa kapacitet resursa.
- **Fiksna rezervacija** - Ovaj status troši kapacitet resursa. Rezervacija obično ima ovaj status kada se otvorite **Održavanje rezervacija** na mreži **Svi članovi tima** na stranici **Projekti**.
- **Uslovna rezervacija** - Ovaj status dodaje resurs u tim, ali ne troši njegov kapacitet. Ukazuje da je resurs rezervisan za potencijalni rad, ali još uvek ima kapacitet ako je potreban na drugim poslovima. S obzirom na ukupnu dostupnost resursa, uslovne rezervacije imaju drugačiji status od fiksnih rezervacija.
- **Predložen** - Ovaj status predstavlja predlog menadžera resursa ili menadžera projekata za resurs. Predlozi ne troše kapacitet resursa i resurs se ne dodaje projektnom timu. Da bi rezervacija resursa za tim bila fiksna, menadžer projekta mora prihvatiti predlog.

### <a name="submit-resource-requests"></a>Prosledite zahteve za resurse

Zahtevi za resurse koriste se da prenesu potražnju (potrebe za resursima) koja mora biti ispunjena od strane menadžera resursa. Za generički resurs koji je već u timu možete direktno da prosledite zahtev za resurs. Zahtev za resurs može se ispuniti na dva načina:

- Menadžer resursa direktno ispunjava zahtev. U ovom slučaju, generički resurs zamenjuje fiksna rezervacija koja ima imenovani resurs.
- Menadžer resursa predlaže resurs menadžeru projekata, a menadžer projekta odobrava ili odbacuje predloženi resurs.

#### <a name="direct-fulfillment-of-resource-requests"></a>Direktno ispunjavanje zahteva za resurse

Kada se generiše potreba za resursom, projektni menadžer može da prosledi zahtev za generički resurs ako izabere resurs, a zatim opciju **Prosledi zahtev**.

![Dugme Prosledi zahtev](media/Resource-Management-image45.png)

Komentari o resursu mogu se dostaviti menadžeru resursa koji ispunjava zahtev. Nakon prosleđivanja zahteva, polje **Status** za člana tima se menja u **Prosleđen**.

![Unošenje opcionalnih komentara](media/Resource-Management-image46.png)

Kada menadžer resursa ispuni zahtev, generičkog člana tima zamenjuje imenovani resurs u mreži **Svi članovi tima**.

![Generički član tima zamenjen je imenovanim resursom u mreži Svi članovi tima](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Korišćenje predloga resursa za zahteve za resurse

Umesto da direktno rezerviše resurs u zahtevu za resurse, menadžer resursa može da predloži resurs menadžeru projekata. Menadžer resursa mogao bi koristiti ovu opciju kada nije dostupno tačno podudaranje sa potrebama. Kada menadžer resursa predloži resurs, menadžer projekata vidi da je polje **Status** za generičkog člana tima promenjeno u **Zahteva pregled**.

![Status generičkog člana tima promenjen je u Zahteva pregled](media/Resource-Management-image48.png)

Da biste pregledali predloženi resurs zajedno sa vizuelizacijom efekta rezervacije predloga, dvaput kliknite na člana tima koji ima status **Zahteva pregled**. Zatim izaberite karticu **Predloženi resursi**.

![Kartica Predloženi resursi](media/Resource-Management-image49.png)

Izaberite **Prihvati sve predloge** da prihvate sve predložene resurse ili **Odbacite sve predloge** da ih odbacite. Ako prihvatite predložene resurse, oni se fiksno rezervišu za projekat kao članovi tima i zamenjuju generičke resurse.

> [!NOTE]
> Morate ili prihvatiti ili odbaciti sve predložene resurse. Ne možete ih delimično prihvatiti ni odbaciti.

### <a name="substitute-a-resource-on-the-project-team"></a>Zamena resursa u projektnom timu

Ponekad menadžer projekta mora zameniti rezervisanog člana tima za projekat.

1. Na stranici **Projekti** na kartici **Tim** odaberite resurs kome je potrebna zamena, a zatim izaberite **Održavanje rezervacija**.
2. Proširite resurs za pregled projekata kojima je dodeljen.

    ![Resurs je proširen radi prikaza dodeljenih projekata](media/Resource-Management-image50.png)

3. Kliknite desnim tasterom miša na projekat, a zatim izaberite **Zamena resursa**.
4. Ako znate resurs koji želite zameniti trenutnim resursom, odaberite ili unesite ime, a zatim izaberite **Ponovo dodeli**.

    ![Određivanje zamenskog resursa](media/Resource-Management-image51.png)

    Alternativno, sledite ove korake da biste potražili resurs:

    1. Izaberite **Pronalaženje zamene**.

        ![Traženje zamenskog resursa](media/Resource-Management-image52.png)

        Pomoćnik za zakazivanje prikazuje listu dostupnih zamena. U pomoćniku za zakazivanje možete dodatno filtrirati dostupne resurse da biste pronašli odgovarajuću zamenu.

        ![Lista dostupnih zamena](media/Resource-Management-image53.png)

    2. Da biste zamenili resurs, odaberite resurs koji želite, a zatim izaberite **Zameni**.

        ![Izabran je zamenski resurs](media/Resource-Management-image54.png)

    Rezervacije i dodele zamenjuju se novim resursom.

    ![Rezervacije i dodele zamenjuju se novim resursom](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a>Usaglašavanje rezervacija i dodela članova tima

Za članove tima, rezervacije i dodele su labavo povezane. Drugim rečima, resursi mogu imati dodele, ali ne i rezervacije ili mogu imati rezervacije, ali ne i dodele. U idealnom slučaju, rezervacije i dodele treba da se usklade tako da resursi imaju potreban kapacitet da izvrše dodeljene zadatke. Međutim, rezervacije se mogu zasnivati na dostupnosti, a vremenski raspored zadataka može se menjati tokom projekta. Stoga, labava povezanost rezervacija i dodela pruža fleksibilnost.

PSA ima karticu **Usaglašenost** koja omogućava menadžerima projekata da usaglase rezervacije članova tima i njihove dodele za projektne timove.

![Kartica Usaglašenost](media/Resource-Management-image56.png)

Kartica **Usaglašenost** prikazuje rezervacije i dodele sve do nivoa dodele pojedinačnog zadatka za svakog člana tima. Prikazuje sate u ćelijama koji predstavljaju vremenske periode, od meseci, pa sve do dana.

Kartica takođe prikazuje ukupni neto iznos projekta, zajedno sa kolonom za ukupnu vrednost.

Kartica za svaki resurs izračunava razliku između rezervacija člana tima i ukupnog broja dodeljenih zadataka člana tima. U idealnom slučaju, ta razlika bi trebalo da bude 0 (nula). Drugim rečima, ne bi trebalo da postoji razlika između rezervacija i dodela. Razlike su obojene i zasenčene kako bi se skrenula pažnja na dve pojave:

- **Nedostatak rezervacija** - Nedostatak rezervacija nastaje kada resurs ima više dodela nego rezervacija. Budući da ovaj kapacitet nije rezervisan, menadžer projekta može da koriguje tu pojavu proširivanjem rezervacija resursa kako bi pokrio deficit.
- **Prekomerne rezervacije** – Prekomerna rezervacija nastaje kada je resurs rezervisan za projekat, ali nije dodeljen zadacima. Ta pojava može biti prihvatljiva u slučajevima kada je resurs rezervisan za projekat pre dodele zadatka. Međutim, u drugim slučajevima se ne planira dodeljivanje resursa zadacima. U tim slučajevima, menadžer projekta treba da razmotriti otkazivanje rezervacija resursa, tako da se kapacitet može koristiti za drugi projekat.

U nekim slučajevima, kada pregledate vreme na višem nivou od nivoa dana (na primer, na mesečnom nivou), možda ćete videti ukupnu razliku koja je nula za neki resurs (drugim rečima, rezervacije = dodele). Međutim, ako pregledate vreme na nivou nedelje, možda ćete videti da postoje dodele od nula sati i rezervacije od 40 sati u prvoj nedelji, ali dodele od 40 sati i rezervacije od nula sati u drugoj nedelji. Sve u svemu, rezervacije i dodele se usklađuju, ali se razlikuju od jedne do druge nedelje.

Kada pregledate vreme na višim nivoima, ćelije na kartici **Usaglašenost** imaju indikator koji će vas obavestiti da postoje razlike na nižim nivoima. Duplim klikom na ćeliju možete da je povećate kako biste videli razliku. Zatim možete da kliknite desnim tasterom miša da biste je umanjili. Ako odaberete resurs, a zatim koristite kontrolu **Sledeća razlika** na traci sa alatkama mreže, možete preći na sledeću razliku između rezervacija i dodela za taj resurs. Zatim možete da koristite kontrolu **Prethodna razlika** za povratak. Takođe možete isključiti indikator razlike i ponašanje u navigaciji u delu **Podešavanja**.

![Indikator razlike](media/Resource-Management-image57.png)

Ako imate dodele zadataka za resurs, ali nema rezervacija, na stranici **Projekti** na kartici **Usaglašenost** izaberite nedostatak rezervacija, a zatim **Produži rezervaciju**. Pojavljuje se dijalog **Produženje rezervacije** i prikazuje rezervaciju koja je potrebna da se reši problem sa nedostatkom resursa. Takođe pokazuje postojeće rezervacije resursa za sve projekte ili druge entitete koji se mogu zakazivati. Ako izaberete **U redu** da biste kreirali rezervaciju za resurs, bez obzira na dostupnost tog resursa, možete prouzrokovati prekomernu rezervaciju.

![Dijalog Produženje rezervacije](media/Resource-Management-image58.png)

Menadžer projekta ili menadžer resursa tada može da koristi tabelu rasporeda kako bi upravljao bilo kojom situacijom u kojoj je resurs prekomerno rezervisan u odnosu na njegov kapacitet.
