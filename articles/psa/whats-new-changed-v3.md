---
title: Šta je novo ili promenjeno u aplikaciji Project Service Automation verzije 3
description: U ovoj temi date su informacije o tome šta je novo i šta se promenilo u rešenju Project Service Automation verzije 3.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: 6ce4c549b04716d466efa262dbc6a4abf28ea9eb
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150685"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3"></a>Šta je novo ili promenjeno u aplikaciji Project Service Automation verzije 3

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Ova tema pruža informacije o promenama korisničkog interfejsa, funkcionalnosti i terminologije u aplikaciji Project Service Automation između verzije 2 ili verzije 1 i verzije 3.

## <a name="project-scheduling"></a>Zakazivanje projekta
Raspored projekta, koji je u prethodnim verzijama bio poznat pod nazivom strukturna analiza posla (SAP), preimenovan je u raspored, a njemu se pristupa klikom na karticu **Raspored**. 

![Raspored projekata](media/psa-schedule-01.png)

Raspored sada ima novu površinu za interakciju koja je i moderna i pristupačna. Međutim, osnovni mehanizam planiranja u rešenju Project Service Automation se nije promenio. Kontrolna dugmad na traci mreže rasporeda omogućavaju vam interakciju sa rasporedom slično kao i u prethodnoj verziji rešenja Project Service Automation. Dodatne promene rasporeda:

- **Gantt grafikon** – Gantt grafikon više ne postoji. Nova Gannt vizuelizacija vraća se u budućoj ispravci.
- **Zaglavlja kolona** – Zaglavlja kolona možete sakriti u mreži klikom na znak nadole pored naziva kolone. 
- **Kolone** – Možete prikazati skrivene kolone klikom na **Dodaj kolonu**. 
- **Kategorija transakcije** – Pronalaženje **kategorije transakcije** je dodato u mrežu rasporeda i prikazuje se podrazumevano. 
 
## <a name="project-templates"></a>Predlošci projekata
Sledeće promene su unete u funkcionalnost predloška projekta.

### <a name="create-a-project-template"></a>Kreirajte predložak projekta 
Možete da kreirate predložak projekta u verziji 3 slično kao u prethodnim verzijama rešenja Project Service Automation. Predložak može da sadrži samo raspored, a raspored može da sadrži dodele, ali one nisu obavezne. Ako raspored ima dodele, one mogu biti samo za generičke resurse. Možete generisati potrebe za generičkim resursima, ali oni se ne mogu rezervisati pomoću stvarnih resursa u predlošku. Ne možete rezervisati pravi resurs za tim u šablonu. 

### <a name="create-a-template-from-an-existing-template"></a>Kreiranje predloška od postojećeg predloška
Kada kreirate novi predložak projekta iz postojećeg predloška u rešenju Project Service Automation u verziji 3, događa se sledeće: 

- Raspored izvornog projekta kopira se u predložak. 
- U tim se kopiraju generički resursi i sve dodele generičkih resursa. Potrebe za generičkim resursima se ne kopiraju. 

### <a name="create-a-template-from-an-existing-project"></a>Kreiranje predloška od postojećeg projekta
Kada kreirate novi predložak projekta od postojećeg projekta, događa se sledeće: 

- Raspored izvornog projekta kopira se u predložak. 
- U tim se kopiraju generički resursi, a sve dodele generičkih resursa se čuvaju. Potrebe za generičkim resursima se ne kopiraju.    
- Imenovani resursi, dodeljeni ili nedodeljeni, uklonjeni su iz tima i zamenjeni generičkim resursima.
- Ako postoje, informacije o klijentima se uklanjaju. 
- Ako postoje, reference na ponude i ugovore se uklanjaju. 

### <a name="create-a-project-from-a-template"></a>Kreiranje projekta iz predloška
U rešenju Project Service Automation u verziji 3, kada kreirate novi projekat iz predloška, događa se sledeće:

- Raspored, tim i dodele kopiraju se u novi projekat.   
- Datum početka predstavlja datum kopije ili datum koji je odabrao korisnik.   
- Za sve generičke članove tima sa potrebama za resurse u predlošku, potrebe se ne kopiraju niti generišu automatski. Morate da ih generišete. 

## <a name="copy-a-project"></a>Kopiranje projekta
U rešenju Project Service Automation u verziji 3, kada kopirate projekat, događa se sledeće: 

- Procenjeni datum početka kopira se, ali se može menjati.  
- Raspored i zadaci projekta se kopiraju. 
- Kopiraju se generički resursi i njihove dodele. Potrebe za generičkim resursima se ne kopiraju. Morate ponovo da ih generišete. 
- Ne kopiraju se stvarni resursi i njihove dodele. Umesto toga, zamenjuju ih generički resursi. 
- Stvarne vrednosti se ne kopiraju u novi projekat. 

## <a name="move-a-scheduled-project"></a>Pomeranje zakazanog projekta
Kada pomerite raspored postojećeg projekta napred, događa se sledeće: 

- Datumi zadataka automatski se premeštaju da bi odgovarali periodu pomeranja. 
- Dodeljeni generički resursi ostaju dodeljeni.   
- Ako su generisani pre pomeranja projekta, potrebe za generičkim resursima ostaju iste i automatski se ne generišu ponovo. Moraćete ih ponovo generisati tako da odražavaju nove dodele zbog pomeranja zadatka. 
- Dodele za stvarne resurse se menjaju kako bi odgovarale pomeranju datuma zadatka. Rezervacije stvarnih resursa se ne menjaju. Morate modifikovati rezervacije koristeći prikaz usaglašenosti. 
- Timski resursi sa rezervacijama, ali bez dodela se ne menjaju. 
- Stvarne vrednosti se ne premeštaju. 

## <a name="estimates"></a>Procene
Procene su podeljene na dve kartice, **Dodela resursa** i **Procene**. Kartica **Dodela resursa** sadrži procene angažovanja i prikazuje dodele resursa za zadatke u prikazu po fazama vremena. Procene možete uređivati na osnovu onoga što je generisao sistem za zakazivanje.

![Kartica sa dodelama resursa prikazuje procene napora i dodele resursa za zadatke](media/resource-assignments-tab-02.png)

Kartica **Procene** prikazuje iznose troškova i prodaje za dodele resursa. Iznosi su samo za čitanje. Cene troškova i prodaje sada se formiraju iz dodela članova tima u rasporedu. To znači da ako imate zadatak bez ikakve dodele, zadatak će se prikazati u okviru nedodeljene grupe. To takođe znači da bez **uloge**, koja predstavlja podrazumevanu dimenziju određivanja cena, neće biti procenjenih troškova ni prodaje ako imate klijenta ili ugovor/ponudu povezanu sa projektom. 

![Kartica Procene koja prikazuje iznose troškova i prodaje](media/estimates-tab-03.png)
  
Kategorija je takođe podržana za zadatke u prikazu rasporeda. Grupisanje po kategorijama na prikazu prema fazama vremena pruža bolje iskustvo, posebno kada u projektu imate i procene troškova. Procene troškova se unose pomoću mreže na zasebnoj kartici. 

Procene troškova mogu da se unose u mrežu na kartici **Procene troškova**. 

![Kartica Procena troškova koja prikazuje mrežu procena troškova](media/expense-estimates-tab-04.png)

## <a name="resource-management"></a>Upravljanje resursima
U aplikaciji Project Service Automation u verziji 3, sa novim objedinjenim klijentskim interfejsom i promenama odnosa između rezervacija i dodela, popunjavanje projekta generičkim ili stvarnim resursima značajno se promenilo u odnosu na verziju 2 i 1. Međutim, koncepti resursa koji mogu da se rezervišu, **stvarnih** i **generičkih** ostaju isti, kao i članovi tima, potrebe, dodele i rezervacije.   

![Korišćenje birača resursa](media/resource-management-05.png)

### <a name="assign-a-real-bookable-resource"></a>Dodeljivanje stvarnog resursa koji može da se dodeli 
U rešenju Project Service Automation u verziji 3, rezervacije i dodele zadataka nisu tesno isprepletane kao u prethodnim verzijama rešenja Project Service Automation. Možete da koristite mrežu tima za rezervaciju **stvarnog** člana tima, slično kao na tržištu.

Koristeći birač resursa u rasporedu, možete odabrati člana tima kreiranog u prikazu tima, a zatim mu dodeliti zadatke. Možete da nastavite da mu dodeljujete zadatke, čak i mimo rezervacija. Koristite karticu **Usaglašenost** da biste usaglasili članove tima koji se razlikuju prema rezervacijama i dodelama.

Birač resursa će pokazati članove tima za projekat. Takođe možete koristiti birač resursa da biste potražili i pregledali druge resurse koji mogu da se rezervišu, a koji nisu deo projektnog tima. Možete ih dodeliti zadatku i oni će postati deo projektnog tima. Morate da ih rezervišete koristeći karticu **Raspored** ili **Usaglašenost**.

### <a name="assign-a-generic-bookable-resource-on-a-task-and-project-team-and-then-fulfill-with-a-real-resource-via-schedule-board"></a>Dodeljivanje generičkog resursa koji može da se rezerviše zadatku i projektnom timu i popunjavanje stvarnim resursom pomoću tabele rasporeda 
U aplikaciji Project Service Automation u verziji 3, funkcionalnost za generisanje tima se ne koristi za generičke resurse. Umesto toga, možete da kreirate i direktno dodelite generički resurs iz rasporeda tako što ćete upisati naziv pozicije generičkog resursa u ćeliju resursa u okviru rasporeda. Možete i da izaberete ikonu resursa u ćeliji, a zatim unesete ime generičkog resursa koji želite da kreirate, pomoću birača resursa. Ovako ćete otvoriti tablu za brzo kreiranje koja vam omogućava da podesite ulogu i organizacionu jedinicu generičkog člana tima resursa. Nakon što kreirate resurs, on se dodeljuje zadatku i možete nastaviti da dodeljujete taj generički resurs drugim zadacima u rasporedu.    
 
Kada resursu dodelite sve odgovarajuće zadatke, možete generisati potrebu za resursom i zatim je ispuniti direktnom rezervacijom koristeći **tabelu rasporeda** ili prosleđivanjem zahteva za resurs. Takođe možete dodati generičke resurse direktno u mrežu članova tima. 

Generički resursi se dodaju projektnom timu bez potreba za resursima i sa datumima početka/završetka projekta dok se generiše potreba za resursima. Da biste generisali zahtev, izaberite generički resurs i kliknite na **Generiši**. Sada se prikazuje veza zahteva, a potrebni sati će biti popunjeni dodeljenim satima. Možete da kliknete na vezu da biste otvorili i ažurirali zahtev.
  
Kada je rezervacija dovršena i u potpunosti ispunjena imenovanim resursom, generički resurs se zamenjuje imenovanim resursom i dodela u rasporedu se ažurira imenovanim resursom. 

Predloženi resursi za potrebe sada se čuvaju na kartici umesto u zasebnom odeljku.

### <a name="multiple-named-resources-fulfilling-a-generic-resource"></a>Više imenovanih resursa koji popunjavaju generički resurs
Kada se zahtev ispuni sa više resursa, generički resurs ostaje u timu i dodeljen zadatku. Imenovani članovi tima koji su rezervisani nisu dodeljeni kao deo pozicije. Menadžer projekta može po potrebi da dodeli posao stvarnim resursima.  Prikaz **Usaglašenost** pruža analizu rezervacija više resursa za veći broj dodela zadataka. Ovo se ne radi automatski jer u komplikovanijem scenariju, na primer kada imate skup zadataka koji sačinjavaju zahtev, mora da se pretpostavi kako menadžer projekta namerava da dodeli resurse. Pošto sistem ne može da razume nameru, pretpostavke će se verovatno razlikovati od predviđenih, pa će doći do netačnog ili nepredvidivog rezultata. Predvidiv ishod je da generički resurs ostaje dodeljen dok menadžer projekta namerno dodeljuje resurse, uz pomoć prikaza **Usaglašenost**.

### <a name="reconciliation"></a>Usaglašenost
Kartica **Usaglašenost** prikazuje rezervacije i sve dodele za svakog člana projektnog tima. Prikaz prikazuje sate u ćelijama koji mogu predstavljati vremenske tačke, od meseci do dana. Ovaj prikaz omogućava menadžerima projekata da usklade rezervacije i dodele članova projektnog tima. Ovo je korisno jer rezervacije i dodele zadataka nisu čvrsto povezane, što omogućava veću fleksibilnost prilikom planiranja projekta. 

![Kartica Usaglašenost koja prikazuje rezervacije i dodele za članove projektnog tima](media/resource-reconciliation-tab-06.png)

Za svaki resurs, prikaz uzima razliku između rezervacija člana tima i ukupnih dodela zadataka i prikazuje sledeće dve razlike koje se mogu javiti kod rezervacija i dodela u projektu: 

- **Nedostatak rezervacija** – Nedostatak rezervacija nastaje kada resurs ima više dodela nego rezervacija. Budući da ovaj kapacitet nije rezervisan, menadžer projekta to može ispraviti tako što proširuje rezervacije resursa kako bi pokrio deficit. 
- **Prekomerne rezervacije** – Prekomerna rezervacija nastaje kada je resurs rezervisan za projekat, ali nije dodeljen zadacima.  Ovo može biti prihvatljiva pojava, na primer ako je resurs rezervisan pre dodele zadatka. Međutim, u drugim slučajevima, možda se ne planira dodeljivanje resursa, a menadžer projekta treba razmotriti otkazivanje rezervacije resursa kako bi omogućio korišćenje kapaciteta za drugi projekat. 

Kada imate dodele zadataka za resurs bez rezervisanja (nedostatak rezervacije), možete da odaberete zbirni nedostatak rezervacije i kliknete na **Produži rezervaciju**. Odavde možete videti rezervaciju koja je potrebna da biste rešili probleme sa nedostatkom resursa i njihovom dostupnošću. 
 
## <a name="time-and-expense"></a>Vreme i trošak
Ovaj odeljak pruža informacije o promenama vremena, troškova i odobrenja u verziji 3 aplikacije Project Service Automation. Kao deo rešenja Dynamics 365 Project Service Automation, funkcija **Stavka vremena** je osvežena da bi iskoristila okvir objedinjenog interfejsa. To omogućava isporuku konzistentnog, jedinstvenog korisničkog interfejsa koji sledi prilagodljiv dizajn za optimalni pregled na bilo kojoj veličini ekrana ili uređaju. 

### <a name="landing-page"></a>Odredišna stranica
Iskustvo neproširive prilagođene stavke vremena zastarelo je u verziji 3. Umesto toga, sada postoji proširivo i dostupno iskustvo uklopljene mreže. Funkcionalnosti za stavku vremena možete pristupiti pomoću mape sajta sa leve strane. Zbog ove promene više nećete moći odjednom da unosite vreme za jednu sedmicu. Umesto toga, moraćete da kreirate stavku vremena za svaki dan u mreži. Nakon kreiranja nekoliko stavki, korisnici mogu grupno da kreiraju stavke vremena pomoću funkcije za **kopiranje** koja je objašnjena kasnije u ovoj temi. 

![Odredišna stranica stavke vremena](media/time-entry-landing-page-07.png)
 
### <a name="create-new-time-entries"></a>Kreiranje novih stavki vremena 
Kliknite na **Nova** na traci da biste otvorili stranicu za brzo kreiranje stavke vremena gde unosite trajanje u minutima, satima ili danima. Da biste to učinili, samo počnite da kucate s, m ili d, zajedno sa količinom.  

![Brzo kreiranje stavke vremena](media/quick-create-time-entry-08.png)

Polja za pronalaženje podržavaju sistemski prikazi. Na primer, nakon što unesete informacije o projektu, polje **Projektni zadatak** se podrazumevano podešava na prikaz **Moji otvoreni projektni zadaci**. Da biste kreirali stavke vremena za zadatke koji nisu dodeljeni korisniku, kliknite na **Promena pogled** na pretraživanju i izaberite **Svi zadaci aktivnog projekta**. Nakon što je kreirana stavka vremena i prikazana u mreži, možete da uredite bilo koje vrednosti stavke direktno na mreži.  

### <a name="bulk-createcopy"></a>Grupno kreiranje/kopiranje 
Nakon kreiranja nekoliko stavki vremena, možete koristiti funkcionalnost kopiranja da biste grupno kreirali dodatne stavke vremena. Kliknite na **Kopiraj** da biste otvorili dijalog **Kopiranje**. U delu **Iz perioda: datum početka** podesite opseg datuma iz kojeg se moraju kopirati vremenski periodi. U delu **U period: datum početka** odredite datum za koji stavke vremena moraju biti kreirane. Kliknite na **Kopiraj** da kopirate stavke vremena u odgovarajući dan u nedelji naveden u stavci **U period**. Na primer, stavka vremena za ponedeljak iz prošle nedelje biće kopirana u ponedeljak one sedmice koja je navedena u stavci **U period**. 

![Grupno kopiranje stavki vremena](media/bulk-copy-time-entry-09.png)
 
### <a name="import-data"></a>Uvoz podataka 
Dodele i razmena slede isti obrazac korisničkog interfejsa koji korisniku omogućava da navede opseg datuma od trenutka kada je potrebno uvesti rezervacije. Tada morate izričito izabrati rezervacije koje treba kopirati u stavke vremena **Radna verzija**. U verziji 3 više ne možete videti obrazac stavke vremena **Predloženo** na mreži i u kalendaru.  

### <a name="change-in-calendar-control"></a>Promena kontrole kalendara
U verziji 3 smo uklonili kontrolu prilagođenog kalendara i sada koristimo UC kalendar za prikazivanje stavki vremena u nedelji. Pomoću ovog kalendara možete da vidite dan, nedelju i mesec. 

> [!NOTE]
> Ograničenje kalendara je da ova kontrola ne podržava radnje za pojedinačne stavke kalendara. Na primer, nećete moći da odaberete jednu ili više stavki kalendara, kao ni da ih prosledite ili izbrišete. Klikom na stavku kalendara otvoriće se stranica **Entitet stavke vremena** za dodatne radnje. 

### <a name="extensibility"></a>Proširivost
**Evidentiranje podataka iz prilagođenih polja samo u entitetima stavki vremena i troškova** – Stavka vremena koristi mrežu koja se može uređivati, mrežu samo za čitanje i kontrole kalendara iz platforme. Sve ove kontrole su ugrađene i zato podržavaju prilagođavanja. U rešenju Project Service Automation u verziji 3, možete dodati dodatna prilagođena polja, podesiti polja za pretraživanje i napraviti njihove rezervne kopije pomoću prilagođenih prikaza. Takođe možete podesiti prilagođenu poslovnu logiku na osnovu izabranih vrednosti u prilagođenim poljima.  

**Evidentirajte podatke iz prilagođenih polja u entitetu vremena i troška i prosledite ih kroz entitete koji podržavaju tok prosleđivanja i odobravanja** – Tipična obrada stavki vremena prikazana je na sledećem dijagramu.

![Obrada toka stavke vremena](media/process-time-entries-10.png)

Ako poslovne potrebe predviđaju da entiteti vremena i troškova moraju da evidentiraju prilagođene dimenzije određivanja cena i prosleđuju vrednosti koje podešava vreme za resurs i ulazni resurs u prilagođenoj dimenziji određivanja cena kroz sve entitete na prethodnom grafikonu, pogledajte članak [Podešavanje prilagođenih polja kao dimenzija određivanja cena](set-up-pricing-dimensions.md)

Da biste podržali poslovne potrebe u kojima entiteti vremena i troškova moraju da evidentiraju prilagođene dimenzije koje se ne koriste za određivanje cena i prosleđuju vrednosti, možete koristiti podešavanje dimenzija za određivanje cena i izraziti prilagođene dimenzije kao dimenzije za određivanje cena bez troškova ili stope naplate. Drugi scenario bi bio dodavanje prilagođenog polja svakom entitetu, koristeći isto ime polja u svim entitetima. Prilagođene dodatne komponente mogu se kreirati za povezivanje zapisa u entitetima koji učestvuju u toku prosleđivanja/odobrenja koristeći entitete porekla transakcije i povezivanja transakcija.  

### <a name="delegate-time-and-expense-entry"></a>Delegirane stavke vremena i troškova
Platforma Common Data Service ne podržava da jedan korisnik lažno predstavlja drugog, što znači da u verziji 3 rešenja Project Service Automation ne postoji podrška za delegiranu stavku vremena i troškova. Međutim, partneri i klijenti su iskoristili zaobilazno rešenje kako bi omogućili podršku za iskustvo delegiranih stavki vremena u verziji 3. Ovo je samo zaobilazno rešenje, a ne celovito rešenje, tako da je važno razumeti ograničenja i koristiti ovaj pristup samo ako su ograničenja prihvatljiva. 

> [!IMPORTANT]
> Ove informacije treba smatrati samo preporučenim smernicama za prilagođenu implementaciju od strane partnera/klijenta. Tim proizvoda neće nuditi formalnu podršku za ovu funkcionalnost kroz naše kanale podrške.

### <a name="customization-details"></a>Detalji prilagođavanja 
Prilagođavanje vam omogućava da dodate **Resurs koji može da se rezerviše** kako biste kreirali i uređivali iskustava, što će omogućiti korisniku da deluje kao delegat menjajući polje **Rezervacija resursa** na drugog korisnika za koga je potrebno evidentirati stavke vremena i troškova. Sledeći koraci pokrivaju delegiranje stavki vremena i troškova. Iste informacije se odnose i na delegiranje stavke troška. 
 
1.  Osigurajte da delegirani korisnik ima globalni sigurnosni pristup projektima i projektnim zadacima. 
1.  Pošto polje **Resurs koji može da se rezerviše**, u okviru entiteta **Stavka vremena** nije prikazano na stranici **Brzo kreiranje**, morate da ga dodate.

    – ili –

    Kreirajte prilagođeni prikaz koji sadrži kolonu **Resurs koji može da se rezerviše** da biste videli samo stavke vremena koje su kreirane za resurs. Objavite prilagođavanja u dizajneru modula aplikacije da bi se ovaj prikaz pojavio u okviru stavke **Birač prikaza** na stranici **Stavke vremena**. Postoje dve dodatne komponente koje upravljaju podešavanjem menadžera za stavke vremena koje se ne odnose na projekat:

    - PreValidateTimeEntryCreate
    - PreValidateTimeEntryUpdate
 
1. Kreirajte novu dodatnu komponentu da biste zamenili polje **Menadžer** menadžerom korisnika dodeljenog u polju **Resurs koji može da se rezerviše**. Koristite istu **fazu izvršenja** kao i zasebna dodatna komponenta (preliminarna validacija) i koristite **Redosled izvršavanja** koji je na višem nivou od zasebne dodatne komponente (veći od 1). Ovo će osigurati da se prilagođena dodatna komponenta izvršava nakon zasebnih dodatnih komponenti.  
 
### <a name="end-user-experience"></a>Iskustvo krajnjeg korisnika
1.  Kada kreirate stavku vremena na stranici za brzo kreiranje, unesite detalje projekta i projektnog zadatka, a zatim odaberite korisnika u polju **Resurs koji može da se rezerviše** za koga treba da se evidentiraju stavke vremena. 
2.  Podrazumevana vrednost ovog polja je prijavljeni korisnik. Međutim, s obzirom da je korisnik zamenio ovo polje, sada se stavka vremena kreira za odabrani **Resurs koji može da se rezerviše**.
3.  Kada prosledite stavke vremena koje ste kreirali za ove zapise, stavke će se staviti u red za davaoca odobrenja u projektu onako kako se očekuje. 
4.  Kada opozovete stavke vremena kreirane za drugog korisnika, stavke vremena će se vratiti u status **Radna verzija**, a polje **Resurs koji može da se rezerviše** će biti podešeno na drugog korisnika. 
5.  Opcionalno, možete preći na prilagođeni prikaz da biste filtrirali stavke vremena kreirane za drugog korisnika. 
 
### <a name="limitations"></a>Ograničenja
Funkcionalnost **Kopiraj** i **Uvezi** funkcionišu samo u kontekstu korisnika koji je prijavljen. To znači da nije moguće kopirati ili uvoziti stavke vremena kreirane za korisnika koji je prijavljen kao resurs koji može da se rezerviše.

Stavke vremena koje nisu za projekat biće usmerene na odobrenje menadžeru resursa koji može da se rezerviše samo ako je korak 4 u gorenavedenom odeljku **Detalji prilagođavanja** obavljen. U suprotnom, stavke vremena koje se ne odnose na projekat i koje su za drugog korisnika biće pogrešno usmerene menadžeru prijavljenog korisnika. 

### <a name="other-changes"></a>Ostale promene 
Funkcionalnost **Rezervacije i zadaci** je uklonjena. 

## <a name="multidimensional-pricing"></a>Višedimenzionalne cene
Da bi se maksimalno iskoristila fleksibilnost i zadovoljile različite poslovne potrebe, verzija 3 aplikacije Project Service Automation podržava posebnu primenu skupova dimenzija za određivanje cena na stope troškova i naplate. Vrednosti dimenzija mogu se podesiti kao podrazumevane vrednosti i zatim se proslediti kroz proces uspostavljanja troškova i određivanja cena, od profilisanja resursa preko stavke vremena do stvarnih vrednosti. Konfiguracija i modifikacija ili proširenje koji su specifični za klijenta koriste standardnu infrastrukturu prilagodljivosti.

Project Service Automation se isporučuje sa podrazumevanim skupom dimenzija za određivanje cena, uloga i jedinica resursa i omogućava podešavanje cena i troškova za svaku kombinaciju uloga i organizacionih jedinica.

Za Project Service Automation klijente koji žele da nastave da koriste ova unapred definisana polja kao dimenzije za određivanje cena u verziji 3, neće biti nikakvih primetnih promena. Možete da nastavite da koristite Project Service Automation kao i obično. Ako pak trebate da odredite cene ili troškove resursa koristeći druge dodatne atribute, verzija 3 vam omogućava da dodajete sopstvene dimenzije za određivanje cena u rešenju Project Service Automation. Proširenje prilagođenih dimenzija za određivanje cena je komplikovano iskustvo konfiguracije. 

## <a name="quotes-and-contracts"></a>Ponude i ugovori
U verziji 3 rešenja Project Service Automation aspekti podešavanja ponuda i ugovora su se promenili, kao i upravljanje njima. Sledeći odeljci pružaju detaljnije informacije.

### <a name="set-up-chargeability-options"></a>Podešavanje opcija naplativosti
U verzijama 1 i 2, podešavanje naplativosti za uloge i kategorije za posebne ponude i ugovore je obavljano pomoću prikaza **Naplativost** koji se nalazi u gornjoj navigaciji stavke ponude ili predmeta ugovora. Ovde ste takođe mogli da podesite cene za te uloge i kategorije troškova.

Od verzije 3, podešavanje opcija naplativosti prema ulozi i kategoriji troškova se obavlja na nivou ponude ili predmeta ugovora. Podešavanje cena je odvojeno od podešavanja naplativosti. Moći ćete da pronađete kartice **Naplative uloge** i **Naplative kategorije** na stranicama **Stavka ponude** i **Predmet ugovora** bez upotrebe gornje navigacije.

![Naplative uloge](media/chargeable-12.png)
 
Podešavanje kartica Naplative uloge i Naplative kategorije takođe koristi unapred definisanu kontrolu mreže koju je moguće uređivati. Za svaku ulogu i kategoriju, podržane opcije načina naplate tokom faze davanja ponude i ugovaranja ostaju nepromenjene u odnosu na prethodne verzije kao **Naplativo** i **Nenaplativo**. **Besplatno** nije podržani tip tokom faze davanja ponude i ugovaranja. **Besplatno** je podržano samo tokom odobrenja vremena ili troškova.  
 
### <a name="create-and-edit-custom-pricing-for-a-project-service-automation-quote-and-project-contract"></a>Kreiranje i uređivanje prilagođenih cena za Project Service Automation ponudu i ugovor o projektu
U verzijama 1 i 2 ste prilagođeni cenovnik za određene ponude i ugovore koristili pomoću stavke **Izmena cena** u prikazu **Naplativost**. Prikaz **Naplativost** se nalazio u gornjoj navigaciji stavke ponude ili predmeta ugovora. Ovde ste takođe mogli da podesite opcije naplativosti za uloge i kategorije troškova.

Od verzije 3, kreiranje i korišćenje prilagođenog cenovnika za Project Service Automation ponudu i Project Service Automation ugovor o projektu je odvojeno od podešavanja naplativosti. Project Service Automation ponuda i Project Service Automation ugovori za projekat imaju novu karticu pod nazivom **Cenovnici projekta**. Ova kartica prikazuje vezani prikaz svih cenovnika projekta koji su priloženi uz Project Service Automation ponudu ili ugovoru o projektu. Da biste kreirali prilagođeni cenovnik iz postojećeg cenovnika koji je već povezan s projektnom ponudom ili ugovorom, kliknite na **Kreiranje prilagođenih cena**. Na taj način ćete napraviti kopiju svih povezanih cenovnika i priložiti ih uz ponudu ili ugovor. Sada možete otvoriti cenovnik i urediti cenu uloge ili kategorije troška tako da se te promene cena primenjuju samo na ovu ponudu ili ugovor. 
  
Sledeći grafikon je pre kreiranja prilagođenih cenovnika.

![Pre prilagođenih cenovnika](media/before-custom-price-lists-13.png)

Sledeći grafikon se prikazuje nakon kreiranja prilagođenih cenovnika.

![Posle prilagođenih cenovnika](media/after-custom-price-lists-14.png)

> [!NOTE]
> Može doći do kratkog kašnjenja od klika na **Kreiranje prilagođenih cena** do kreiranja prilagođenog cenovnika. Preporučujemo da osvežite mrežu umesto da kliknete više puta. Prilagođeni cenovnik je kreiran ako je nazivu povezanog cenovnika dodat naziv ponude ili ugovora o projektu.
