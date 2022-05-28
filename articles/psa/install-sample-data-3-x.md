---
title: Instaliranje probnih podataka
description: Ova tema pruža informacije o instaliranju uzoraka podataka u usluzi Project Service Automation.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.reviewer: johnmichalak
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 952f3c3c037bb8459bdd1400288c4ea8604ce282
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581853"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Instaliranje probnih podataka za aplikaciju Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

Da bismo vam pomogli da izgradite sopstvena demonstraciona okruženja, Microsoft pruža probne pakete podataka koje možete da preuzmete i koji prikazuju mogućnosti aplikacija. Postoje dva tipa paketa probnih podataka:
- podaci za referencu/podešavanje
- demo podaci (referenca/podešavanje i transakcioni podaci, kao što su radni nalozi i projekti)

Pakete probnih podataka za **referencu** možete da preuzmete u tri zasebna paketa, tako da možete da instalirate podatke samo za Project Service ili samo za Field Service, a možete i odjednom da instalirate probne podatke za obe aplikacije.

Paketi probnih podataka za podešavanje/referencu su:

- [**V902PSMasterData** – Samo Project Service u verziji 3.x](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** – Samo Field Service u verziji 8.x](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** – Field Service 8.x i Project Service 3.x](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

Najnoviji paket **demo** podataka je:

 - [**FPSDemoData** – Field Service 8.x i Project Service 3.x](https://aka.ms/fpsdemodatapackage)

   Uputstva za instalaciju se neznatno razlikuju za korisnike koji kreiraju i konfigurišu odeljak, ali ostalo je isto kao i u prethodnoj [**poruci na blogu**](https://aka.ms/fpsdemodatablog). Ovaj paket predstavlja ograničeni skup demo podataka potrebno je približno 3 časa da se instalira.

Ovi paketi probnih podataka su dostupni samo na engleskom jeziku.

> [!IMPORTANT]
> **Ne postoji način da deinstalirate probne podatke.** Trebalo bi da instalirate ove paket samo u sistemima za demonstraciju, procenu, obuku ili testiranje. Takođe, imajte na umu da instaliranje pojedinačnog paketa, pa naknadno instaliranje drugog pojedinačnog paketa nije podržano. (Drugim rečima, ne možete da instalirate **FSMasterData**, a nakon njega **PSMasterData** ili obrnuto.) Ako smatrate da će vam u nekom trenutku u budućnosti biti potrebni probni podaci za obe aplikacije, trebalo bi da instalirate paket **v902FPSMasterData**.

Kada instalirate neki od paketa probnih podataka, proces instalacije vrši sledeće radnje:

- Kreira ili podešava podrazumevane parametre za korišćenje programa Project Service, Field Service ili obe aplikacije (ako je primenjivo).

- Uvozi probne podatke aplikacija, kao što su resursi koji mogu da se rezervišu, uloge specifične za aplikacije, prodajni i cenovnici troškova, organizacione jedinice, zapisi prodajnog procesa i ostali entiteti radi prikaza ključnih mogućnosti.  

Sa paketom **demo podataka**, dobijate sve navedeno i dodatne transakcione podatke, kao što su radni nalozi i projekti.

Da li se pitate koje mogućnosti možete da demonstrirate sa probnim podacima? Pogledajte fiktivni scenario kompanije Fabrikam Robotics u okviru [tehničkih beleški](#technical-notes).

Ako imate pitanja o instaliranju ovih paketa probnih podataka, [pošaljite nam e-poruku na adresu fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).

## <a name="requirements"></a>Zahtevi

Protokom instalacije pretpostavlja sledeće o vašoj ciljnoj instanci (organizaciji):

- Osnovni jezik je engleski, a osnovna valuta je SAD dolar (USD, $).

- Organizacija nema prethodne Project Service ili Field Service podatke ili ima samo osnovne podrazumevane podatke koji se dobijaju sa svakom novom organizacijom.

- Ispravna verzija poslovne aplikacije je već instalirana:
       
    - **Za FPSDemoData ili v902FPSMasterData:** Organizacija ima instalirane usluge Field Service, verziju 8.x i Project Service, verziju 3.x.

    - **Za v902PSMasterData:** Organizacija ima instaliran program Project Service, verziju 3.x.

    - **Za v902FSMasterData:** Organizacija ima instaliran program Field Service, verziju 8.x.

> [!NOTE]
> Ako je potrebno da instalirate probne podatke povrh postojećeg probnog ili demonstracionog okruženja usluge Project Service i Field Service koji već imaju podatke (nije preporučljivo), potrebno je da obustavite bezbednosne prethodne provere koje izvršava program za instaliranje. Više informacija potražite u tehničkim napomenama u nastavku.

## <a name="prepare-for-installation"></a>Priprema za instalaciju

Morate da pokrenete program za instaliranje na računaru sa nedavnom verzijom operativnog sistema Windows (poželjno Windows 10).

Trebalo bi da planirate da računar ostane povezan sa mrežom i da instalacija traje do oko **sat vremena** za podatke za **podešavanje/referencu**. (Instalacija obično traje oko 30 minuta za **FPSMasterData**, koja uključuje probne podataka za obe aplikacije.) Za **FPSDemoData**, instalacija će potrajati oko **3 časa**.

Računar bi trebalo da ima isključenu funkciju čuvara ekrana. U suprotnom, akreditivi sesije za instalaciju mogu biti izgubljeni kada se aktivira čuvar ekrana (osim ako sesiju zadržite aktivnom sve vreme).

> [!div class="mx-imgBorder"]
> ![Snimak ekrana podešavanja čuvara ekrana sa isključenim čuvarom ekrana.](media/sample-data-1.png)

## <a name="download-and-unpack"></a>Preuzimanje i raspakivanje

Program za instaliranje Project Service i Field Service probnih podataka se distribuira kao izvršna datoteka koja se sama izdvaja. Imena datoteka mogu da variraju u zavisnosti paketa probnih podataka, ali inače su koraci isti bez obzira koji paket da instalirate.

Nakon preuzimanja paketa, pokrenite .exe datoteku, a zatim prihvatite uslove i odredbe za raspakivanje komprimovane zip datoteke. Zatim morate da izvučete sadržaj te datoteke u fasciklu na računaru.

U zavisnosti od operativnog sistema i bezbednosnih podešavanja, možda ćete morati da obavite sledeće korake nakon raspakivanja zip datoteke:

1. Potražite datoteku **FPSDemoData.dll** i kliknite na nju desnim tasterom miša u fascikli **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.

2. Odaberite **Otključaj**.

3. Izaberite **Primeni**.

4. Izaberite **U redu**.


## <a name="create-or-configure-users"></a>Kreiranje ili konfigurisanje korisnika

Paket **FPSDemoData** zahteva šest korisnika, dok paketi **FPSMasterData** zahtevaju jednog korisnika. Proverite šta je ispravno za vaš paket probnih podataka.

## <a name="create-or-configure-users---setupreference-data-packages"></a>Kreirajte ili konfigurišite korisnike – paketi podataka za podešavanje/referencu

**FPSMasterData** paket je dizajniran da bude instaliran sa jednim korisnikom pod imenom Spencer Low sa podešavanjima opisanim ovde. Da biste pravilno instalirali paket, morate da kreirate (ili privremeno preimenujte) korisnike u okruženju kako bi se podudarali sa konfiguracijom dolaznih probnih podataka.

Da biste kreirali ili konfigurisali korisnike, idite na opciju **Postavke** > **Bezbednost** > **Korisnici** i postupite na sledeći način:

1. Podesite UserFullname="Spencer Low" sa korisničkim imenom „spencerl“ (**mala slova**) za uloge menadžera projekta i menadžera vežbe.

2. Izaberite korisnika **Spencer Low**, a zatim izaberite **Upravljaj ulogama**. Pronađite i izaberite ulogu **Administrator sistema**, a zatim izaberite **U redu** da biste odobrili puna prava administratora za korisnika Spencer Low. Ovaj korak je neophodan kako biste osigurali da se probni zapisi kreiraju sa vlasništvom ispravnog korisnika i stoga pravilno popune prikaze.

3. Iz preuzetog paketa, potrebno je da ispravite datoteku za mapiranje podataka sa e-adresama konteksta podrazumevanog korisnika. Da biste to uradili, otvorite **PkgFolder**, a zatim pronađite i otvorite datoteku **ImportUserMapFile.xml** u Beležnici (ili programu Visual Studio ili drugom XML uređivaču). Podesite polje **DefaultUserToMapTo =** na e-adresu korisnika Spencer Low.

4. Ako ne koriste Spencer Low sa korisničkim imenom **spencerl**, potrebno je da ispravite dodatnu datoteku. Otvorite datoteku **DemoDataPreImportConfig.xml**, a zatim pronađite oznaku **userstocreateandconfigure**. Ažurirajte oznaku **\<login\>** korisničkim imenom korisnika Sava Simić. Za dodatne detalje, pogledajte [tehničke napomene](#technical-notes).

## <a name="create-or-configure-users---demo-data-package"></a>Kreiranje ili konfigurisanje korisnika – paket demo podataka

Paket demo podataka zahteva šest korisnika. Da bi se paket instalirao ispravno, uradite sledeće:

 1. Kreirajte ili privremeno preimenujte postojeće korisnike tako da odgovaraju konfiguraciji dolaznih probnih podataka tako što ćete otići na **Podešavanja** > **Bezbednost** > **Korisnici**.
 
    Ove uloge su potrebne samo za demonstracije zasnovane na osobama.  
    - Puno ime korisnika="David So" kao tehničar terenske službe   
    - Puno ime korisnika="Jamie Reding" kao dispečer korisničke službe i terenske službe   
    - Puno ime korisnika="Molly Clark" kao menadžer poslovnih kontakata   
    - Puno ime korisnika="Spencer Low" kao menadžer prakse i projekata  
    - Puno ime korisnika="Veronica Quek" kao član tima   
    - Puno ime korisnika="William Contoso"
  
2. U svrhu uvoza demo podataka, dodelite šest korisnika iznad uloge Administratora kako bi se probni zapisi uvezli ispravno. 

3. Otvorite **PkgFolder**, a zatim pronađite i otvorite **ImportUserMapFile.xml**. Ažurirajte polja **Novo=** za e-adrese odgovarajućih korisnika u sistemu.

   > [!div class="mx-imgBorder"]
   > ![Snimak ekrana UserMapFile.](media/sample-data-7.png)

4. Ako korisnik punog imena "Spencer Low" ima ID korisnika različit od **"spencerl"**, tada treba da ažurirate dodatnu datoteku. Otvorite datoteku **DemoDataPreImportConfig.xml**, a zatim pronađite oznaku **userstocreateandconfigure**. Ažurirajte oznaku **\<login\>** oznakom loginId (pazite na velika i mala slova). 

5. Kalendar prvog korisnika (u oznaci **userstocreateandconfigure**) koristi se za popunjavanje radnog vremena svih resursa koji mogu da se rezervišu za uvoz demo podataka. Idite na **Podešavanja** > **Bezbednost** > **Korisnici**, pronađite korisnika "Spencer Low" pretraga i otvorite opciju "Radno vreme". Unesite postojeće radno vreme birajući opciju **Ceo periodični sedmični raspored od početka do kraj**. Uverite se da je **Radno vreme podešeno na 8:00–17:00 (9 časova), od ponedeljka do petka i sa vremenskom zonom podešenom na pacifičko vreme (SAD i Kanada)**. To je potrebno da bi se tabele projekta i rasporeda prikazivale kao što se očekuje.

**Preporuka:** Razmotrite da sada kreirate rezervnu kopiju vaše organizacije u slučaju da treba da se vratite na polaznu tačku ukoliko nešto krene naopako tokom instalacije probnih podataka. Za još informacija pogledajte [Pravljenje rezervnih kopija i vraćanje instanci](/dynamics365/customer-engagement/admin/backup-restore-instances).

## <a name="run-the-package-deployer"></a>Pokrenite Package Deployer

1. Pronađite i pokrenite **PackageDeployer.exe** u fascikli **v902FPSMasterData** ILI **PackageDeployer_FPSDemoData**.

2. Prihvatite uslove i odredbe.

3. U sledećem prozoru:

   a. Izaberite tip primene **Office 365**.

   b. Koristite korisnika i lozinku korisnika administrator sistema konfigurisane u opciji „Kreiranje ili konfigurisanje korisnika“ („Spencer Low“ sa korisničkim imenom „spencerl“).

   c. Uverite se da je izabrana opcija **Prikaži listu dostupnih organizacija**.

      > [!div class="mx-imgBorder"]
      > ![Snimak ekrana programa Package Deployer sa označenom opcijom „Prikaži listu dostupnih organizacija“](media/sample-data-2.png)

4. Izaberite organizaciju gde želite da instalirate probne podatke.

5. Izaberite **Sledeće** sve dok ne vidite dijalog **Podešavanje demo podataka**.

   > [!div class="mx-imgBorder"]
   > ![Snimak ekrana prozora sa statusom programa za instaliranje demo podataka.](media/sample-data-3.png)

6. Pre nego što nastavite, imajte u vidu da instaliranje probnih podataka može da potraje do sat vremena (uobičajeno ~ 10 minuta). Potrebno je da se uverite da će računar ostati uključen i povezan na mrežu tokom procesa instalacije i da će vaša sesija ostati aktivna.   

7. Kada budete spremni, kliknite na dugme **Sledeće** da biste započeli proces instaliranja probnih podataka. Kada se probni podaci učitaju, kliknite na dugme **Završi**.

## <a name="verify-the-sample-data-installation"></a>Proverite instalaciju probnih podataka

Za svaki slučaj, uverite se da su broj zapisa i tipovi entiteta navedeni u fiktivnom scenariju kompanije Fabrikam Robotics pojavljuju kao što je očekivano.

Kada se probni podaci potpuno učitaju, prijavite se kao korisnik Spencer Low i potvrdite sledeće:

- Ako je instalirana aplikacija Project Service, idite na stavku **Project Service** > **Podešavanja** > **Cenovnici**. Potvrdite da li postoje stope naplate i stope troškova sa odgovarajućom valutom za svaku zemlju/region u skupu podataka.

- Ako je instalirana aplikacija Project Service idite na stavku Project **Universal Resource Scheduling** > **Podešavanja** > **Organizacione jedinice**. Potvrdite da je cenovnik troškova sa odgovarajućom valutom povezan sa svakom organizacionom jedinicom (bez stavki za grad). Ako bilo šta nedostaje, pronađite i povežite odgovarajući cenovnik troškova.

- Ako je instalirana aplikacija Field Service, idite na stavku **Project Service** > **Podešavanja** > **Cenovnici**. Potvrdite da postoje stope naplate i stope troškova. Idite na stavku **Field Service** > **Podešavanja** > **Cenovnici** i proverite da li postoje naplate i cene, sa odgovarajućom valutom, za svaku zemlju/region u skupu podataka.

  > [!div class="mx-imgBorder"]
  > ![Snimak ekrana aktivnih cenovnika.](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![Snimak ekrana aktivnih organizacionih jedinica.](media/sample-data-5.png)

## <a name="technical-notes"></a>Tehničke beleške

Pogledajte u nastavku za više tehničkih detalja o instalaciji ovih podataka.

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>Instaliranje probnih podataka povrh postojećih podataka (ne preporučuje se)

Ako je potrebno da instalirate probne podatke povrh postojećeg probnog ili demonstracionog okruženja programa Field Service ili Project Service koji već imaju podatke, potrebno je da obustavite bezbednosne prethodne provere koje izvršava program za instaliranje.

Da biste to uradili, idite u fasciklu **PkgFolder** da biste pronašli i otvorili datoteku **DemoDataPreImportConfig.xml** u Beležnici (ili drugom XML uređivaču).

Pronađite sledeću vrednost, a zatim promenite podešavanja iz vrednosti tačno u netačno:

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

Ova promena prouzrokuje da program za instaliranje zaobilazi neke važne bezbednosne provere, uključujući:

- Potvrdu da ne postoji više od jednog aktivnog zapisa **Organizaciona jedinica**, a zatim ga preimenuje u **Fabrikam US**.

- Potvrdu da ne postoji više od jednog aktivnog zapisa **Radni predložak**.

- Potvrdu da ne postoji više od jednog aktivnog zapisa **Parametar projekta**, a zatim preimenuje taj zapis u **Parametri**.

### <a name="configuration-components"></a>Komponente konfiguracije

Postoji određeni broj drugih komponenti konfiguracije u ovoj datoteci za konfiguraciju pre uvoza. Za tehničke korisnike, neki od ovih uključuju:

- Oznaka **\<RequiredSolutions\>** navodi neophodne instalacije rešenja i njihove brojeve verzija.

- **\<InstallSampleData\>** kontroliše da li su instalirani gotovi probni podaci za aplikacije.

    - netačno – preskače instalaciju ovih ugrađenih podataka (koji mogu da se uklanjaju)

    - tačno – instalira ugrađene podatke uporedno sa instalacijom probnih podataka za FS i PSA

- **\<PreImportDataCollection\>** navodi mape podataka ravne datoteke i povezane zapise koji se uvoze unapred pre glavne instalacije probnih podataka.

- **\<EntitiesToEnableScheduling\>** navodi koje entitete treba omogućiti za rezervaciju u Microsoft Dynamics Scheduling (tj. Universal Resource Scheduling).

- **\<UsersToCreateAndConfigure\>** navodi resurse koji mogu da se rezervišu i koji će biti kreirani (ako već ne postoje) pre nego što se izvrši uvoz probnih podataka. Imajte na umu da se izvorni sistemski probni podaci za resurse koji mogu da se rezervišu podudaraju sa ciljnim sistemskim zapisima za resurse koji mogu da se rezervišu za vrednost FullName i prijavljivanje svakog resursa. Stoga NIJE moguće da promenite imena u ovoj unapred konfigurisanoj datoteci osim ako prvo ne uvezete probne podatke u ciljni sistem pomoću ovih imena, a zatim preimenujte Resurse koji mogu da se rezervišu u željeni skup imena zajedno sa zapisima Omogućeni korisnik, a da zatim ponovo izvezete podatke za uvoz u vaš konačni odredišni sistem (i u skladu sa tim ispravite **ImportUserMapFile.xml** stare i nove stavke).

- **\<PluginsToDisable\>** navodi veoma diskretne dodatne komponente linijske stavke koje moraju biti onemogućene tokom uvoza probnih podataka, a zatim ponovo omogućene nakon toga.

### <a name="fabrikam-robotics-fictitious-scenario"></a>Fabrikam Robotics fiktivni scenario

Paketi sa probnim podacima referenci za Field Service i Project Service instaliraju **rešenje Fabrikam Manufacturing Master Data (v3.0.0.0)**, zajedno sa otprilike 4000 zapisa i približno 40 različitih entiteta. Zasebni paketi probnih podataka za programe Field Service ili Project Service sadrže podskup **v902FPSMasterData** probnih podataka za tu aplikaciju. Paket **demo podataka** instalira **rešenje Fabrikam Manufacturing Demo Data (v3.0.0.7)** sa približno 22.000 zapisa u 148 entiteta.

Fiktivno preduzeće Fabrikam Robotics je proizvođač robota za linije za sklapanje elektronskih uređaja i poznato je po kvalitetu proizvoda, inovaciji i dobroj korisničkoj službi, uključujući planiranje instalacija, primenu i usluge tekućeg održavanja. Fabrikam ima sedište u SAD (Fabrikam US) i ima servisne operacije zasnovane na projektima u Francuskoj, Indiji, Ujedinjenom Kraljevstvu i Švajcarskoj.

Operacije terenske službe su centrirane u SAD, većim delom u široj oblasti oko Sijetla. Kompanija je fokusirana na pružanje povezanosti interneta stvari (IoT) za nadgledanje performansi sredstava klijenta i pružanje sve proaktivnijih usluga na lokaciji.

Pregled visokog nivoa probnih podataka je sledeći:

- Zajednički elementi probnih podataka (uključeno u obe aplikacije)

    - 1 korisnik

    - 71 poslovni kontakt

    - 137 kontakata

    - Razni tipovi transakcija i kategorija

    - 50 proizvoda sa 1 cenovnikom za proizvod

    - 14 cenovnika/cena koštanja

    - 31 karakteristike (veštine resursa) u 2 modela ocenjivanja sa 3 nivoa (vrednosti ocenjivanja)

- Project Service

    - 8 organizacionih jedinica

    - 6 nivoa ukupne iskorišćenosti specifičnih za ulogu

    - preko 2.800 specifikacija uloge i cene

- Field Service

    - 4 teritorije

    - 5 tipova radnih naloga

    - 22 sredstva klijenta

    - 9 tipova incidenata sa opsegom povezanih karakteristika resursa (9) usluga (13) i servisnih zadataka (13)
   
Paket **demo podataka** instalira približno 179 radnih naloga, 12 projekata i povezane transakcione podatke. 

### <a name="change-the-work-hours-for-sample-resources"></a>Promena radnog vremena za probne resurse

Podrazumevano, svi resursi koji mogu da se rezervišu imaju kalendar sa podrazumevanim 24-časovnim radnim vremenom.

Ako morate da promenite radno vreme za probne resurse koji mogu da se rezervišu, idite u opciju **Universal Resource Scheduling** > **Planiranje** > **Resursi**.

Izaberite korisnika (na primer, Spencer Low) i promenite radno vreme za zaposlenog Spencer na radno vreme koje želite da primenite na više korisnika. Idite na stavku **Universal Resource Scheduling** > **Podešavanja** > **Predlošci radnog vremena** i uredite zapis **Podrazumevani predložak rada**. U polju **Resurs predloška**, izaberite korisnika sa radnim vremenom koje želite da primenite na druge resurse. Idite na **Universal Resource Scheduling** > **Planiranje** > **Resursi** > **Aktivni resursi koji mogu da se rezervišu**. Izaberite resurse koje želite da promenite, a zatim izaberite **Postavi kalendar**. Na padajućoj listi **Predložak rada** izaberite predložak **Podrazumevano radno vreme** ili drugi predložak sa ispravnim resursom za predložak. Kada odete na tabelu rasporeda, trebalo bi da možete da vidite da resursi sada imaju ispravljeno radno vreme.

> [!div class="mx-imgBorder"]
> ![Snimak ekrana aktivnih resursa koji mogu da se rezervišu.](media/sample-data-6.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]