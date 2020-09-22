---
title: Obezbeđivanje resursa za projekat
description: Ova tema pruža informacije o obezbeđivanju resursa za projekat.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755102"
---
# <a name="project-resourcing"></a>Obezbeđivanje resursa za projekat

[!include [banner](../includes/banner.md)]

Ova tema pruža informacije o obezbeđivanju resursa za projekat.

Jedan od izazova za menadžere projekata i menadžere resursa tokom faze planiranja projekta je dodela resursa, gde oni moraju odrediti i rezervisati tačan resurs za rad na projektu. U usluzi Dynamics 365 Finance, mogućnosti obezbeđivanja resursa za projekte omogućavaju vam da definišete uloge koje se tretiraju kao privremeni resursi koji mogu biti rezervisani za određeno angažovanje ili deo angažovanja. Ova vrsta resursa omogućava menadžerima projekata i menadžerima resursa da izvrše sledeće zadatke:

- Definišite ulogu koja ima potrebne kompetencije, tako da je lako podudarati resurse.
- Koristite uloge za definisanje početnog rasporeda angažovanja koji se zasniva na rezervisanim resursima.
- Procenite troškove i odredite početni budžet na osnovu dodeljenih uloga i resursa za projekat.
- Koristite uloge za procenu broja rezervacija resursa potrebnih za svako angažovanje.
- Procenite broj resursa koji su potrebni za ceo životni ciklus projekta.
- Napravite strukturnu analizu posla (SAP) koristeći početne dodele resursa.

[![Životni ciklus projekta](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

Kako se planiranje projekta odvija, planirani resursi mogu se zameniti resursima sa osobljem. Menadžer projekta se takođe može vratiti i ažurirati rezervacije resursa tokom bilo koje faze projekta.

## <a name="set-up-project-resources"></a>Podešavanje resursa projekta
Morate postaviti kalendar i povezati ga sa zaposlenim ili radnikom. Kalendar se koristi za planiranje projekta i radno vreme resursa koji su rezervisani za projekat. Tokom podešavanja kalendara, menadžeri projekata mogu izvršiti nivelisanje resursa kao deo optimizacije resursa. Na osnovu kalendarskog rasporeda, resursi se mogu ograničiti. Kalendar možete podesiti na stranici **Kalendari**.

Kada radnika postavite kao resurs projekta, možete da birate između radnika koji rade u kompaniji za koju postavljate resurse. Alternativno, možete da izaberete radnike iz drugih kompanija u vašoj organizaciji. Ti radnici su poznati kao međukompanijski resursi.

Sledeći postupci objašnjavaju kako da postavite radnika kao resurs projekta u vašoj kompaniji i kako da postavite međukompanijski resurs projekta.

### <a name="set-up-a-worker-as-a-project-resource"></a>Postavite radnika kao resurs projekta

1. Na stranici **Radnici**, na listi **Radnici**, izaberite radnika kojeg dodajete kao resurs projekta i otvorite zapis radnika.
2. U oknu radnji izaberite **Projekat** &gt; **Podešavanje** &gt; **Podešavanje projekta**.
3. Izaberite kalendar, a zatim zatvorite stranicu.

Takođe možete odrediti podrazumevane projekte za resurs kao vrstu prethodnog dodeljivanja. Prethodna dodeljivanja se mogu koristiti kada menadžer resursa ili menadžer projekata unapred zna na kojim projektima će resurs raditi. Prethodna dodeljivanja se takođe mogu zasnivati na zahtevu sponzora projekta ili klijenta. Da biste unapred dodelili projekat, na stranici **Dodela projekata**, na kartici **Projekti**, u listi **Preostali projekti** izaberite odgovarajući projekat.

### <a name="set-up-an-intercompany-resource"></a>Podesite međukompanijski resurs

Kada radnika postavite kao međukompanijski resurs, morate dovršiti podešavanje i u kompaniji zajmodavcu i u kompaniji zajmoprimcu.

**U kompaniji zajmodavcu**

1. U usluzi Finance proverite da li je izabrana kompanija zajmodavac, a zatim dovršite postupak u prethodnom odeljku „Postavljanje radnika kao resursa projekta“.
2. Na stranici **Međukompanijsko računovodstvo**, izaberite **Novo**.
3. U polju **ID pravnog lica** izaberite kompaniju zajmodavca. Popunite preostala polja na odgovarajući način, a zatim izaberite opciju **Sačuvaj**.
4. Na stranici **Cena transfera**, izaberite **Novo**.
5. U polju **Pravno lice zajmoprimac** izaberite odgovarajuću kompaniju.
6. Da biste pozajmljivali kompaniji zajmoprimcu samo one resurse koje ste kreirali na početku ovog odeljka, u polju **Resurs** izaberite ime resursa koji ste kreirali. Da biste učinili sve resurse u kompaniji dostupnim kompaniji zajmoprimcu, ostavite polje **Resurs** prazno.
7. Na stranici **Parametri upravljanja projektom i računovodstvenom**, na kartici **Međukompanijsko** podesite opciju **Omogući međukompanijsko raspoređivanje resursa vremenske rasporede** na **Da**.

**U kompaniji zajmoprimcu**

- Na stranici **Lista resursa**, u filter za pretragu unesite ime resursa koji ste kreirali za kompaniju zajmodavca, da biste proverili da li je ime uključeno u listu resursa za kompaniju zajmoprimca.

## <a name="manage-resource-competencies"></a>Upravljanje kompetencijama resursa
Kompetencije resursa su suštinski deo upravljanja resursima. Kompetencije se mogu koristiti kao polazna osnova za određivanje resursa koji imaju tačnu ravnotežu veština, obrazovanja, sertifikacije i projektnog iskustva. Trebalo bi da postaviti te informacije za svaki resurs i da ih redovno ažurirate. Na ovaj način možete maksimizovati mogućnosti kada se odgovarajuće kompetencije resursa poklapaju tokom dodele resursa projektima.

[![Primeri veština, sertifikacija, obrazovanja i iskustva rada na projektima](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

Sledeći postupci objašnjavaju kako da postavite neke kompetencije za resurs.

Da biste postavili kompetencije za radnika, možete da koristite ili stranicu liste **Radnici** u odeljku Ljudski resursi ili stranicu liste **Resursi** u odeljku Upravljanje projektima i računovodstvo. Za sledeće postupke, koristi se stranica liste **Radnici** u odeljku Ljudski resursi.

### <a name="set-up-competencies-certificates"></a>Postavite kompetencije: Certifikati

1. Na stranici liste **Radnici**, izaberite red za radnika za kojeg želite da dodate informacije o certifikatu.
2. U oknu radnje, na kartici **Radnik**, u grupi **Kompetencije** izaberite **Certifikati**.
3. Izaberite **Novo** u polju **Tip certifikata**, a zatim izaberite **PMP**.
4. U polju **Datum početka** izaberite **1.10.2015** i izaberite **Sačuvaj**.

### <a name="set-up-competencies-skills"></a>Postavite kompetencije: Veštine

1. Na stranici liste **Radnici**, uverite se da je radnik kojeg ste koristili u prethodnom postupku i dalje izabran. Zatim u oknu radnji, na kartici **Radnik**, u grupi **Kompetencije** izaberite **Veštine**.
2. Izaberite **Novo**.
3. U polju **Veština**, izaberite **Menadžment projekta**.
4. U polju **Nivo**, izaberite **5 Stručnjak**.
5. U polju **Datum nivoa**, izaberite **14.1.2014**.
6. U polje **Godine iskustva** unesite **10**.
7. Izaberite **Sačuvaj**, a zatim zatvorite stranicu.

## <a name="create-a-new-project"></a>Kreirajte novi projekat
1. Na stranici **Menadžment projekta** izaberite **Novi projekat** i unesite sledeće vrednosti:

    - **Tip projekta:** Vreme i materijal
    - **Naziv projekta:** Nadogradnja XYZ faza 2
    - **Grupa projekata:** TM\_WIP
    - **ID ugovora o projektu:** 00000002

2. Izaberite **Kreirajte projekat**.

### <a name="assign-a-resource-to-a-project"></a>Dodeljivanje resursa projektu

1. Na stranici **Radnici**, na listi **Radnici**, izaberite zapis za radnika za kojeg ste prethodno podesili kompetencije i otvorite zapis radnika.
2. U oknu radnji, na kartici **Projekat**, u grupi **Podešavanje** izaberite **Dodeli projekte**.
3. Na stranici **Dodele projekata za validaciju resursa**, na kartici **Projekti**, u polju **Dodaj projekat izabranim projektima**, filtrirajte prema projektu **Nadogradnja XYZ faza 2**.
4. U oknu **Preostali projekti**, izaberite projekat, a zatim izaberite dugme sa strelicom da biste ga dodali u okno **Izabrani projekti**.

Takođe možete da dodelite kategorije za resurs po potrebi. Tip kategorije je ili **Trošak** ili **Prihod**. Tip kategorije određuje vaša organizacija. Ako za resurs nisu dodeljene kategorije, Finance traži podrazumevanu kategoriju cena po satu za troškove i prihod.

### <a name="set-up-project-resource-and-role-characteristics"></a>Podešavanje karakteristika i uloga resursa projekta

Menadžer projekta može koristiti funkcionalnost resursa za projekat da bi kreirao uloge potrebne za projekat. Uloge se mogu koristiti ako su potvrđeni resursi i dalje nepoznati kada se resursi rezervišu. Uloge se mogu privremeno rezervisati kao planirani resursi, tako da možete nastaviti faze planiranja projekta.

[![Primer uloge](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenario:** Contoso je angažovan da završi projekat Vreme i materijal koji ima odobrenu povelju projekta. Mlađi menadžer projekta još uvek dovršava opseg projekta. Menadžer resursa trenutno identifikuje određene resurse koji će biti rezervisani za rad na novom projektu. Zbog kritične prirode projekta, sponzor projekta zatražio je starijeg menadžera projekta kao jednu od uloga. Menadžer resursa mora nabaviti novi resurs i definisati ulogu u sistemu u slučaju da mlađi menadžer projekta zahteva informacije o resursima tokom planiranja projekta.

Sledeći koraci pokazuju kako menadžer resursa može da postavi ulogu višeg menadžera projekta i poveže karakteristike resursa sa njom. Kasnije se uloga može koristiti za traženje dostupnih resursa koji odgovaraju traženim kompetencijama resursa.

1. Na stranici **Podešavanje uloga** izaberite **Nova** i unesite sledeće vrednosti:

    - **ID uloge:** Viši menadžer projekta
    - **Opis:** Viši menadžer projekta

2. Izaberite **Kreiraj**.
3. Izaberite ulogu **Viši menadžer projekta**, a zatim izaberite **Konfiguriši karakteristike**.
4. U polju **Tip karakteristike**, izaberite **Veština**.
5. U polju **Dostupne karakteristike**, unesite veštinu za traženje.
6. U polju **Tip karakteristike**, izaberite **Certifikat**.
7. U polju **Dostupne karakteristike**, unesite tip certifikata za traženje.

### <a name="assign-a-project-resource-to-a-project"></a>Dodeljivanje resursa projektu

1. Na stranici **Svi projekti** izaberite projekat **Nadogradnja XYZ faza 2**.
2. Na kartici **Projektni tim i raspoređivanje**, izaberite **Dodaj**.
3. U polju **Uloga** izaberite **Član tima**.
4. Izaberite **Rezerviši iz kalendara**.
5. Na stranici **Dostupnost resursa** izaberite **Pogledajte podešavanja**.
6. Na stranici **Prilagodite postavke prikaza**, unesite sledeće vrednosti:

    - **Format za prikaz opsega datuma:** Dan
    - **Prikaži opise dostupnosti:** Da
    - **Prikaži preostali kapacitet:** Da

7. Izaberite resurs u listi resursa.
8. Izaberite **Fiksna rezervacija** i **Puni kapacitet**.


### <a name="assign-a-resource-to-a-default-role"></a>Dodeljivanje resursa podrazumevanoj ulozi

Da bi pomogli menadžerima projekata ili resursa da dalje dubinski pretražuju resurse koji mogu biti rezervisani za projekat. Podrazumevanu ulogu možete povezati sa postojećim ili novostečenim resursom. Na primer, kada je Danijel zaposlen, imao je iskustvo i veštine da popuni ulogu poslovnog analitičara. Menadžer resursa dodelio je ovu ulogu Danijelu kao podrazumevanu. Stoga je menadžer resursa dodao Danijela u skup poslovnih analitičara koji su dostupni za rad na projektima.

Tokom rezervacije resursa, menadžeri projekata mogu filtrirati resurse uloga koji su dostupni za rad na projektima. Ove informacije mogu da koriste kao jedan kriterijum kada obavljaju analizu odluka prema više kriterijuma tokom popunjavanja resursa. Oni takođe mogu da dodaju druge karakteristike resursa u filter za traženje resursa koji imaju specifične veštine, obrazovanje i iskustvo za dati projekat.

**Scenario:** Odobreni projekat je započeo, a uloga višeg menadžera projekta bila je rezervisana kao planirani resurs tokom faze planiranja projekta. Menadžer resursa je sada nabavio resurs za ispunjavanje uloge višeg menadžera projekta.

1. Na stranici **Lista resursa**, izaberite **Danijel Goldšmit**.
2. Na stranici **Uloga resursa** izaberite **Nova** i unesite sledeće vrednosti:

    - **Stupa na snagu:** Unesite trenutni datum.
    - **Isticanje:** Unesite **Nikad**.
    - **Uloga:** Unesite **Viši menadžer projekta**.

3. Izaberite **Sačuvaj**, a zatim zatvorite stranicu.
4. Na kartici **Kompetencije**, dodajte veštinu **Menadžment projekta** i **PMP** certifikat.

## <a name="set-up-role-based-pricing"></a>Postavite određivanje cene zasnovano na ulogama
Sve cene troškova, prodaje i transfera mogu se podesiti za uloge.

1. Na stranici **Prodajna cena (sat)**, izaberite **Nova** i unesite datum stupanja na snagu.
2. U koloni **Uloga**, izaberite ulogu.
3. U koloni **Cene**, unesite cenu za izabranu ulogu resursa.

## <a name="form-a-project-team"></a>Formiranje projektnog tima
Da bi koristio uloge koje su prethodno postavljene u projektu, menadžer projekta mora povezati uloge sa projektom. Za projekat se može dodeliti više uloga. Da bi se sprečila zabuna, ove uloge se automatski označavaju tokom rezervacije. Na primer, ako menadžer projekta zahteva tri softverska inženjera, automatski se generišu tri uloge softverskog inženjera koje imaju oznake **softverski inženjer 1**, **softverski inženjer 2** i **softverski inženjer 3**. Ako su karakteristike uloge prethodno postavljene za ulogu, one se primenjuju kao filter tokom pretraživanja resursa. Dodatne karakteristike se mogu dodati po potrebi za dalje preciziranje pretrage.

Postavke prikaza takođe se mogu prilagoditi kako bi se dobio bolji prikaz dostupnosti resursa. Postoje opcije za prikazivanje raspoloživosti po satima, dnevno, nedeljno, mesečno, kvartalno i godišnje. Takođe postoji opcija za prikaz raspoloživog i preostalog kapaciteta resursa. Ova opcija je korisna za upravljanje vremenom kada procenjujete dostupno vreme za aktivnosti ili dostupnost resursa.

Menadžer projekta može odabrati ulogu na stranici, a zatim, ako postoji dostupan resurs koji odgovara zahtevima, izaberite da rezervišete resurs za popunjavanje uloge. Imajte na umu da resursi u ovom trenutku ne moraju biti rezervisani u fazi planiranja. Kada kreirate SAP, možete zameniti uloge resursima osoblja za projekat. Ako se uloge zamene resursima osoblja u SAP-u, podešavanje resursa automatski ažurira spisak i raspored projektnog tima.

[![Spisak projektnog tima koji uključuje i uloge i stvarne resurse](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Menadžer projekta ima razne mogućnosti za rezervaciju resursa za projekat, kao što su **Preostali kapacitet**, **Pun kapacitet**, **Procenat kapaciteta** i **Navedite radno vreme**. Ove opcije rezervacije mogu se otkazati u bilo kom trenutku ako se promene dodeljivanja resursa. Podržane su dve vrste rezervacija:

- **Fiksna rezervacija** – Rezervacija resursa je odobrena i potvrđena za rad na angažovanju tokom određenog vremena.
- **Uslovna rezervacija** – Rezervacije resursa su uslovno podešene za rad na angažovanju tokom određenog vremena.

Sledeća procedura objašnjava kako da kreirate projektni tim.

### <a name="create-a-project-team"></a>Kreiranje projektnog tima

1. Na stranici liste **Svi projekti** izaberite projekat, a zatim izaberite **Uredi**.
2. Na kartici **Projektni tim i raspoređivanje**, u polje **Datum završetka rasporeda** unesite datum početka rasporeda uvećan za jedan mesec. Na primer, ako je datum početka rasporeda 24. jun 2017. (24.6.2017), Unesite **24.07.2017**.
3. Izaberite **Dodaj**.
4. U oknu **Dodavanje uloga u projekat**, u polju **Uloga** izaberite **Viši menadžer projekta**.
5. Izaberite **Potrebne kompetencije**.
6. Na stranici **Odaberite karakteristike**, karakteristike koje ste prethodno postavili za ulogu višeg menadžera projekta su podrazumevano izabrane. Izaberite **U redu**.
7. Na stranici **Dodavanje uloge projektu**, u polju **Broj resursa** unesite **1**.
8. U polju **Resurs**, pregled prikazuje sve resurse koji imaju potrebne kompetencije. Izaberite **Danijel Goldšmit**, a zatim izaberite **Kreiraj**.
9. Na stranici **Projekat** izaberite **Dodaj**.
10. U oknu **Dodavanje uloga u projekat**, u polju **Uloga** izaberite **Član tima**. U polje **Broj resursa** unesite **5**.
11. Izaberite **Kreiraj**.
12. Na stranici **Projekti**, izaberite **Popuni resurs**.

## <a name="resource-capacity-synchronization"></a>Sinhronizacija kapaciteta resursa
Procesi za sinhronizaciju resursa garantuju da će se informacije za kalendar i osnovni kalendar slivati u planiranje resursa projekta. Ako se kalendar promeni, procesi izvršavaju potrebna ažuriranja rasporeda resursa projekta. Procesi takođe pomažu u poboljšanju performansi, jer su informacije o resursima kalendara unapred sinhronizovane. Stoga se ažuriranja podataka o rasporedu resursa dešavaju brže. Preporučujemo da procese planirate kao pakete umesto kao jedan po jedan. U suprotnom, postoji rizik da će neko zaboraviti sve datume kada su informacije poslednji put sinhronizovane. Ako se ne koriste svi datumi, mogu se pojaviti praznine tokom sinhronizacije datuma.

![Sinhronizacija kalendara](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Sinhronizacija zbirnih vrednosti kapaciteta resursa

Proces sinhronizacije je dizajniran da sinhronizuje sve informacije kalendara resursa. Ove informacije uključuju osnovne informacije o kalendaru o svim promenama u tabeli kapaciteta kalendara resursa projekta. Ako se u projekat dodaju novi resursi, sinhronizacija garantuje dostupnost ažuriranih informacija kalendara. Ova sinhronizacija se može izvršiti u bilo kom trenutku.

Preporučujemo da koristite paket. Opcije su dostupne tokom sinhronizacije rezervacija kapaciteta.

1. Izaberite **Upravljanje projektima i računovodstvo** &gt; **Periodično** &gt; **Sinhronizacija kapaciteta** &gt; **Sinhronizuj zbirne vrednosti kapaciteta resursa**.
2. Podesite opcije u sledećoj tabeli.

    | Opcija      | Opis |
    |-------------|-------------|
    | Šifra perioda | Opcionalno izaberite šifru intervala datuma glavne knjige da biste postavili datume početka i završetka procesa sinhronizacije za zbirne vrednosti kapaciteta resursa. |
    | Datum početka  | Unesite datum početka procesa sinhronizacije za zbirne vrednosti kapaciteta resursa. |
    | Datum završetka    | Unesite datum završetka procesa sinhronizacije za zbirne vrednosti kapaciteta resursa. |

[![Proces sinhronizacije](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Podesite uloge na SAP predlošcima
Menadžeri projekata mogu postaviti SAP predloške koje mogu primeniti kada kreiraju SAP za nove projekte. Menadžeri projekata mogu da dodaju uloge kada kreiraju predložak. Koristite sledeći postupak za dodeljivanje uloge SAP predlošku.

1. Izaberite **Upravljanje projektima i računovodstvo** &gt; **Podešavanje** &gt; **Projekti** &gt; **Predlošci strukturne analize posla**.
2. Izaberite **Detalji** za izabrani SAP predložak.
3. Izaberite zadatak sa liste, a zatim u polju **Uloga** izaberite ulogu koju želite da dodelite zadatku.

### <a name="work-with-a-wbs"></a>Rad sa SAP

Možete da kreirate novi SAP ili da ga kopirate iz postojećeg SAP predloška. Menadžer projekata može lako da upravlja resursima dodeljujući uloge novim zadacima na SAP-u. Uloge se mogu zameniti nakon sticanja resursa ili nakon identifikacije potvrđenog resursa za rad na zadatku. Ova fleksibilnost omogućava menadžerima projekata da izvršavaju sledeće zadatke:

- Identifikujte broj resursa potrebnih za SAP radne pakete.
- Procenite troškove projekta.
- Odredite preliminarni budžet.
- Procenite trajanje aktivnosti na osnovu uloga i resursa.
- Razvijte neke planove upravljanja projektom na osnovu dostupnih informacija o projektu.

Dodatne opcije su dodate u SAP radi boljeg korišćenja funkcionalnosti resursa.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opcija</th>
<th>Opis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Dodele resursa</td>
<td>Pogledajte dodeljene resurse, datume, broj sati i vrstu rezervacije za zadatke na SAP-u.</td>
</tr>
<tr class="even">
<td>Automatsko generisanje tima</td>
<td>Automatski dodajte planirane resurse pomoću uloga povezanih sa zadatkom. Finance automatski predlaže planirane resurse korišćenjem analize odluka sa više kriterijuma, zasnovane na ulogama. Kada se uloge i zalaganje (u satima) postave za zadatke u SAP-u i kada se objavi struktura, izaberite <strong>Automatski generiši tim</strong>. Potreban broj planiranih resursa dodaje se SAP-u i na karticu <strong>Zakazivanje projekata i timova</strong>.</td>
</tr>
<tr class="odd">
<td>Resurs (padajuća lista)</td>
<td>Na stranici <strong>Pokretanje dodele resursa</strong>, možete odabrati resurse za fiksno rezervisanje ili uslovno rezervisanje, na osnovu navedenog trajanja. Možete prilagoditi postavke prikaza da biste videli i postavili trajanje aktivnosti resursa. Možete izabrati i dodeliti resurse na nivou radnog paketa koristeći sledeće opcije:
<ul>
<li><strong>Prihvati</strong> – Potvrdite promene resursa koji je dodeljen zadatku.</li>
<li><strong>Otkaži</strong> – Otkažite promene resursa koji je dodeljen zadatku.</li>
<li><strong>Dodeli automatski</strong> – Dostupni resurs sa osobljem koji ima odgovarajuću ulogu automatski se bira i dodeljuje izabranom zadatku.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Na stranici **Svi projekti** izaberite projekat **Nadogradnja XYZ faza 2**.
2. Izaberite **Plan** &gt; **Aktivnosti** &gt; **Strukturna analiza posla**.
3. Izaberite **Novo** da biste dodali sledeće aktivnosti prvog nivoa u SAP:

    - Pokretanje
    - Planiranje
    - Izvršavanje
    - Nadgledanje i kontrola
    - Zatvaranje

4. Podesite datume i zalaganje (u satima), kao što je prikazano na sledećoj ilustraciji.

    [![Određivanje datuma i zalaganja](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Izaberite red zadatka **Pokretanje**, a zatim u polju **Uloga** izaberite **Viši menadžer projekta**.
6. Izaberite **Objavi**.
7. Na istoj liniji, u polju **Resurs** izaberite **Danijel Goldšmit**, a zatim izaberite **Prihvati**.
8. Izaberite red zadatka **Planiranje**, a zatim u polju **Uloga** izaberite **Poslovni analitičar**.
9. Izaberite **Objavi**, a zatim izaberite **Automatski generiši tim**.
10. U okviru poruke koji se prikaže, izaberite **Da**.
11. U polju **Resurs** proverite da li je vrednost **Poslovni analitičar 1**.
12. Za resurs **Poslovni analitičar 1**, otvorite pronalaženje i izaberite **Pokreni dodelu resursa**. Zatim izaberite radnika za zadatak.
13. Izaberite **Uslovno dodeljivanje** &gt; **Puni kapacitet**.

    > [!NOTE] 
    > Nećete dobiti upozorenje da je navedeni resurs sada 2, jer broj resursa ostaje 1.

14. Na stranici **Strukturna analiza posla** potvrdite dodeljivanje resursa na SAP-u, a zatim izaberite **Sačuvaj**.

## <a name="resource-fulfillment-for-planned-resources"></a>Ispunjavanje resursa za planirane resurse
Menadžer projekta može planirati potrebne uloge resursa za projekat. Menadžer resursa će videti ove planirane resurse kao zahteve na stranici **Ispunjenje resursa** i može dodeliti stvarne resurse.

1. Na stranici **Svi projekti** izaberite projekat **Nadogradnja XYZ faza 2**.
2. Izaberite **Projekat**, a zatim izaberite **Uredi**.
3. Na kartici **Projektni tim i raspoređivanje**, izaberite **Dodaj**.
4. U dijalogu **Dodavanje uloga** izaberite ulogu **Programer softvera**.
5. Izaberite **Kreiraj**, a zatim zatvorite stranicu projekta.
6. Na stranici **Ispunjavanje resursa**, izaberite **Programer softvera 1** za projekat **Projekat nadogradnje XYZ, faza 2**.
7. Izaberite radnika, a zatim izaberite **Dodeli**.
8. Proverite da li je linija za **Programera softvera 1** uklonjena za projekat **Projekat nadogradnje XYZ, faza 2**.
9. Na kartici **Projektni tim i zakazivanje**, za projekat **Nadogradnja XYZ faza 2** proverite da li je radnik kojeg ste izabrali u prethodnom koraku dodat kao **Programer softvera**.

## <a name="requests-for-project-resources"></a>Zahtevi za resurse projekta
Funkcionalnost za raspoređivanje resursa projekta omogućava da samo menadžeri resursa raspoređuju resurse osoblja na angažovanja ili projekte. Da biste omogućili ovu funkcionalnost, izvršite sledeće zadatke ili proverite da li su završeni:

- Podesite sekvence brojeva.
- Podesite tokove posla upravljanja projektima i računovodstvom.
- Omogućite tokove posla zahteva za resursima.

Nakon završetka prethodnih zadataka, možete izvršiti sledeće zadatke po potrebi:

- Kreirajte zahtev za resursom iz uslovno rezervisanog resursa osoblja.
- Nadgledajte zahteve za resursima.
- Ispunite zahteve za resurse.
- Zatražite resurse osoblja iz SAP.
- Rezervišite resurse za projekat bez zahteva za resursima osoblja.

## <a name="monitor-project-teams"></a>Nadgledajte projektne timove
1. Na stranici **Svi projekti**, izaberite vezu **ID projekta** za projekat **Nadogradnja XYZ faza 2**.
2. Na brzoj kartici **Projektni tim i zakazivanje**, uverite se da su navedeni resursi projekta tačni.
