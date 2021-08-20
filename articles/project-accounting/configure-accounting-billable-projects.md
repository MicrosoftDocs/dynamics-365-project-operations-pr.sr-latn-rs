---
title: Konfigurisanje računovodstva za naplative projekte
description: Ova tema pruža informacije o računovodstvenim opcijama za naplative projekte.
author: sigitac
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: cbc6bcbfa527486df4c740c52cec8c4be1dabe0478783fb7d2e71a65f18c050f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991053"
---
# <a name="configure-accounting-for-billable-projects"></a>Konfigurisanje računovodstva za naplative projekte

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Dynamics 365 Project Operations podržava razne računovodstvene opcije za naplative projekte koji uključuju vreme i materijal i transakcije sa fiksnom cenom.

- **Transakcije vremena i materijala**: Ove transakcije se fakturišu kako posao napreduje na osnovu potrošnje sati, troškova, stavki ili naknada na projektu. Ovi troškovi transakcija mogu se povezati sa prihodom od svake transakcije, a projekat se fakturiše kako posao napreduje. Prihod od projekta takođe može nastati u trenutku kada dođe do transakcije. Tokom fakturisanja, prihod se prepoznaje i, ako je primenljivo, obračunati prihod se stornira.
- **Transakcije sa fiksnom cenom**: Ove transakcije se fakturišu prema rasporedu naplate koji se zasniva na projektnom ugovoru. Prihod za transakcije sa fiksnom cenom može se prepoznati pri fakturisanju ili izračunavati i knjižiti periodično, u skladu sa metodama **Završen ugovor** ili **Procenat završenosti**.

Projekat se smatra naplativim kada je povezan sa jednim ili više predmeta ugovora. Predmet ugovora o projektu definiše za sebe koji način obračuna i vrste transakcija su dozvoljeni.

Kao primer, kompanija Fabrikam Robotics je ostvarila projektni ugovor sa korporacijom Adatum za optimizaciju opreme. Adatum će platiti fiksni iznos od 10.000 USD za pokrivanje nastalih troškova projekta. To je način naplate sa fiksnom cenom. Vreme i naknade za projekat naplaćivaće se po upotrebi. To je način naplate vremena i materijala. Sav rad biće praćen u okviru jednog projekta pod nazivom „Optimizacija Adatum opreme“.

Član projektnog tima podnosi osam sati rada na projektu optimizacije Adatum opreme. Kada rukovodilac projekta odobri ovo vreme, sistem koristi način naplate vremena i materijala za kreiranje stvarnih transakcija, fakture i naloga. Ova transakcija neće biti uključena u obračun procene prihoda sa fiksnom cenom.

Drugi član projektnog tima podnosi putni trošak od 2000 USD za projekat optimizacije Adatum opreme. Kada rukovodilac projekta odobri podnesak, sistem koristi način naplate sa fiksnom cenom za kreiranje stvarnih transakcija i nalog za ovaj trošak u projektu. Klijent neće dobiti fakturu na osnovu ove transakcije. Umesto toga, biće u fakturisano korišćenjem zasebno konfigurisanih kontrolnih tačaka za naplatu. Ova transakcija troška, zajedno sa procenom troška, biće uključena u obračun procene prihoda sa fiksnom cenom.

Računovodstveni principi za projektne transakcije definisani su u profilima troškova i prihoda projekta. Za svaku projektnu transakciju, sistem određuje odgovarajući profil troškova i prihoda projekta koristeći pravila za profil troškova i prihoda koja su konfigurisana.

## <a name="define-project-cost-and-revenue-profiles"></a>Definisanje profila troškova i prihoda projekta 

Profili troškova i prihoda projekta određuju računovodstvena pravila za transakcije projekta. Ovi profili su konfigurisani u upravljanju projektima i računovodstvu. 

Dovršite sledeće korake da biste kreirali novi profil troškova i prihoda projekta. 

1. Idite na **Upravljanje projektima i računovodstvo** > **Podešavanje** > **Knjiženje** > **Profili troškova i prihoda projekta**. 
2. Izaberite **Novo** da biste kreirali novi profil troškova i prihoda projekta.
3. U polje **Naziv** unesite naziv i kratak opis profila.
4. U polju **Način obračuna** izaberite **Vreme i materijal** ili **Fiksna cena**.
5. Proširite brzu karticu **Glavna knjiga**. Polja na ovoj kartici definišu računovodstvene principe koji se koriste kada se projektne transakcije knjiže u glavnu knjigu pomoću Project Operations dnevnika integracije, a zatim fakturišu kroz predlog fakture za projekat.
6. Izaberite odgovarajuće informacije u sledećim poljima na brzoj kartici **Glavna knjiga**:

    - **Knjiženje troškova – sat**:

       - *Bez glavne knjige*: Troškovi transakcija vremena neće biti knjiženi u glavnu knjigu kada se knjiži Project Operations dnevnik integracije. Međutim, računovođa može naknadno knjižiti troškove pomoću funkcije „Knjiženje troškova“.
       - **Bilans**: Troškovi transakcija vremena biće zaduženi na tipu računa glavne knjige *Prihod u toku – Vrednost troškova* i odobreni na *računu za raspodelu zarada* u podešavanju knjiženja u glavnu knjigu. Računovođa će koristiti funkciju „Knjiženje troškova“ da bi periodično premeštao ovaj trošak sa bilansnog računa na račun dobitka i gubitka.
       - **Dobitak i gubitak**: Prilikom knjiženja Project Operations dnevnika integracije, troškovi transakcija vremena zadužiće se na tipu računa glavne knjige *Trošak* a odobriće se na *računu za raspodelu zarada* definisanom na kartici **Trošak** na stranici **Podešavanje knjiženja u glavnu knjigu** (**Upravljanje projektima i računovodstvo** \> **Podešavanje** \> **Knjiženje** \> **Podešavanje knjiženja u glavnu knjigu**). Ovo je najčešće podešavanje za transakcije vremena i materijala.
        - *Nikad u glavnu knjigu*: Troškovi transakcija vremena nikada neće biti knjiženi u glavnu knjigu.

    - **Knjiženje troškova – trošak**:

         - **Bilans**: Pri knjiženju Project Operations dnevnika integracije, cena transakcije troškova zadužiće se na tipu računa glavne knjige *Prihod u toku – Vrednost troškova* kao što je definisano na kartici **Trošak** na stranici **Podešavanje knjiženja u glavnu knjigu** i odobriće se na računu za prebijanje dugovanja na stavci u glavnoj knjizi. Podrazumevani računi za prebijanje dugovanja i potraživanja za troškove su definisani u odeljku **Upravljanje projektima i računovodstvo** > **Podešavanje** \> **Knjiženje** \> **Podrazumevani račun za prebijanje dugovanja i potraživanja za troškove**. Računovođa će koristiti funkciju **Knjiženje troškova** da bi periodično premeštao ovaj trošak sa bilansnog računa na račun dobitka i gubitka.
        - **Dobitak i gubitak**: Pri knjiženju Project Operations dnevnika integracije, cena transakcije troškova zadužiće tip računa glavne knjige *Trošak* kao što je definisano na kartici **Trošak** na stranici **Podešavanje knjiženja u glavnu knjigu** i odobriće se na računu za prebijanje dugovanja i potraživanja na stavci u glavnoj knjizi. Podrazumevani računi za prebijanje dugovanja i potraživanja za troškove su definisani u odeljku **Upravljanje projektima i računovodstvo** \> **Podešavanje** \> **Knjiženje** \> **Podrazumevani račun za prebijanje dugovanja i potraživanja za troškove**.
      
    - **Knjiženje troškova – stavka**:

         - **Bilans**: Prilikom knjiženja dnevnika Project Operations integracije, troškovi transakcije stavke biće se zaduživati za tip glavne knjige *Posao u toku – Vrednost troškova – stavka* kako je definisano na kartici **Cena** na stranici **Podešavanje knjiženja u glavnoj knjizi** i odobravati za sledeće:
    
              - Za upotrebu vrste dokumenta: **Trošak – stavka** račun na **Podešavanje knjiženja u glavnoj knjizi**.  
              - Za kupovinu vrste dokumenta: **Račun za integraciju nabavki** na **Parametri upravljanja projektom i računovodstvom**.
           Računovođa će koristiti funkciju **Knjiženje troškova** da bi periodično premeštao ovaj trošak sa bilansnog računa na račun dobitka i gubitka.
        - **Profit i gubitak**: Prilikom knjiženja dnevnika Project Operations integracije, troškovi transakcije stavke biće zaduženi za tip glavne knjige *Cena* kako je definisano na kartici **Cena** na stranici **Podešavanje knjiženja u glavnoj knjizi** i odobravati za sledeće:
         
             - Za upotrebu vrste dokumenta: **Trošak – stavka** račun na **Podešavanje knjiženja u glavnoj knjizi**.  
             - Za kupovinu vrste dokumenta: **Račun za integraciju nabavki** na **Parametri upravljanja projektom i računovodstvom**.
       
    - **O fakturisanju poslovnog kontakta**:

        - **Bilans**: Prilikom knjiženja predloga projektne fakture, transakcija na računu (kontrolna tačka za naplatu) biće odobrena na tipu računa glavne knjige *Fakturisani prihod u toku – na računu* kao što je definisano na kartici **Prihod** na stranici **Podešavanje knjiženja u glavnu knjigu** i zadužena na računu bilansa klijenta.
         - **Dobitak i gubitak**: Prilikom knjiženja predloga projektne fakture, transakcija na računu (kontrolna tačka za naplatu) biće odobrena na tipu računa glavne knjige *Fakturisani prihod – na računu* kao što je definisano na kartici **Prihod** na stranici **Podešavanje knjiženja u glavnu knjigu** i zadužena na računu bilansa klijenta. Računi bilansa klijenata definisani su u odeljku **Potraživanja** \> **Podešavanje** \> **Profili knjiženja klijenata**.

   Kada definišete profile knjiženja za metode obračuna vremena i materijala, imate mogućnost prikupljanja prihoda po vrsti transakcije (sat, trošak, stavka i naknada). Ako je opcija **Pripadajući prihod** podešena na **Da**, nenaplaćene prodajne transakcije u Project Operations dnevniku integracije će se evidentirati u glavnu knjigu. Vrednost prodaje se zadužuje na računu **Posao u toku – račun vrednosti prodaje** i odobrava na računu **Pripisani prihod – vrednost prodaje** koji je podešen na stranici **Podešavanje knjiženja u glavnu knjigu**, na kartici **Prihod**. 
  
  > [!NOTE]
  > Opcija **Pripadajući prihod** je dostupna samo kada se odgovarajući tip transakcije **Trošak** knjiži na računu dobitka i gubitka.
    
7. Proširite brzu karticu **Procena**. Polja na ovoj kartici definišu podešavanja proračuna za procene prihoda sa fiksnom cenom. Polja na ovoj kartici važe samo za profile troškova i prihoda projekta sa metodom naplate **Fiksna cena**.
8. Izaberite odgovarajuće informacije u sledećim poljima na brzoj kartici **Procena**:

    - **Princip korišćen za proračun završetka projekta**:

        - **Završen ugovor**: Usklađivanje troškova i prepoznavanje prihoda se dešava tek na kraju projekta. Troškovi se odražavaju kao prihod u toku u bilansu dok se projekat ne završi.
        - **Procenat dovršenosti**: Obračunati prihod se izračunava i knjiži u glavnu knjigu svakog perioda na osnovu procenta dovršenosti projekta. Postoji više metoda za izračunavanje procenta završetka. Ove metode mogu biti automatske na osnovu konfiguracije ili ručne.
        - **Bez prihoda u toku**: Ovo podešavanje se koristi za projekte sa fiksnom cenom sa kratkim vremenskim rasponom i tamo gde se faktura i troškovi javljaju u istom periodu. U ovom slučaju, vrednost polja **Fakturisanje na računu** na brzoj kartici **Glavna knjiga** se automatski postavlja na **Dobitak i gubitak** kako bi se osiguralo prepoznavanje prihoda prilikom fakturisanja. Proces procene prihoda se neće koristiti za ovaj profil troškova i prihoda projekta.

    - **Princip podudaranja**: Ovo polje određuje kako će izračunata vrednost prodaje (obračunati prihod) biti knjižena u glavnu knjigu.

        - Korišćenjem principa **Vrednost prodaje**, sistem će izračunati prodajnu vrednost tako što će podudarati troškove i prihod, a zatim će je knjižiti kao jedan iznos.
        - Korišćenjem principa **Proizvodnja i dobitak**, sistem će vrednost prodaje podeliti na ostvarene troškove i izračunati dobitak. Ti podaci se knjiže zasebno.

    - **Predlošci troškova**: Dozvolite grupisanje projektnih transakcija na osnovu tipa transakcije i kategorije projekta i definišite pravila izračunavanja procenta završetka za ove grupe.
    - **Šifre perioda**: Definišite učestalost izračunavanja procene prihoda za dati profil troškova i prihoda projekta.
    - **Kategorije za procenu**: Koristi se za knjiženje vrednosti prodaje (obračunati prihod) u transakcijama projekta. Prvo konfigurišite namensku kategoriju projekata za tip transakcije **Nadoknada**, a zatim podesite zastavicu **Procena** za ovu kategoriju projekta. Zatim, u zavisnosti od izabranog principa podudaranja, odaberite ovu kategoriju projekta u vrednosti **Prodaja** ili polju **Dobitak** u profilu troškova i prihoda projekta.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>Primeri konfiguracija za profile troškova i prihoda projekta

Vreme i materijali – bez prihoda u toku

![Profil troškova i prihoda: Vreme i materijali - bez posla u toku.](media/time-material-no-wip.png)

Vreme i materijali – prihod u toku (prihod)

![Profil troškova i prihoda: Vreme i materijali – posao u toku.](media/time-material-with-wip.png)

Fiksna cena – Bez prihoda u toku

![Profil troškova i prihoda: Fiksna cena - bez posla u toku.](media/fixed-price-no-wip.png)

Fiksna cena – završen ugovor

![Profil troškova i prihoda: Fiksna cena – završen ugovor.](media/fixed-price-completed-contract.png)

Fiksna cena – procenat dovršenosti

![Profil troškova i prihoda: Fiksna cena – procenat dovršenosti.](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>Primeri računovodstvenog događaja za probne profile troškova i prihoda projekta.

| Računovodstveni događaj                  | Vreme i materijal – Bez prihoda u toku                       | Vreme i materijal – Prihod u toku                                                                                           | Fiksna cena – Bez prihoda u toku                                            | Fiksna cena – Završen ugovor                                                                            | Fiksna cena – Procenat dovršenosti                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Knjiženje vremenskih transakcija u glavnu knjigu    | Duguje – Trošak <br>Potražuje – Raspodela zarada          | Duguje – Trošak <br>Potražuje – Raspodela zarada <br>Duguje – Prodajna vrednost prihoda u toku <br>Potražuje – Vrednost prodaje obračunatog prihoda                | Duguje – Trošak <br>Potražuje – Raspodela zarada                         | Duguje – Trošak <br>Potražuje – Raspodela zarada                                                                    | Duguje – Trošak <br>Potražuje – Raspodela zarada                       |
| Knjiženje transakcija troškova u glavnu knjigu | Duguje – Trošak <br>Potražuje - Račun za prebijanje dugovanja i potraživanja za troškove | Duguje – Trošak <br>Potražuje - Račun za prebijanje dugovanja i potraživanja za troškove <br>Duguje – Prodajna vrednost prihoda u toku <br>Potražuje – Vrednost prodaje obračunatog prihoda      | Duguje – Trošak <br>Potražuje - Račun za prebijanje dugovanja i potraživanja za troškove                 | Duguje – Trošak<br> Potražuje - Račun za prebijanje dugovanja i potraživanja za troškove                                                            | Duguje – Trošak <br>Potražuje - Račun za prebijanje dugovanja i potraživanja za troškove               |
| Klijent kojem se fakturiše                | Duguje – Bilans klijenta <br>Potražuje – Fakturisani prihod | Duguje – Bilans klijenta <br>Potražuje – Fakturisani prihod <br>Potražuje – Vrednost dugovanja prihoda u toku od prodaje – Vrednost obračunatog prihoda od prodaje | Duguje – Bilans klijenta <br>Potražuje – Fakturisani prihod – na računu | Duguje – Bilans klijenta <br>Potražuje – Prihod u toku – Fakturisano na računu                                                  | Duguje – Bilans klijenta <br>Potražuje – Prihod u toku – Fakturisano na računu    |
| Knjiženje procene prihoda             | Nije primenjivo                                   | Nije primenjivo                                                                                                    | Nije primenljivo                                                  | Duguje – Vrednost troškova prihoda u toku <br>Potražuje – Trošak                                                                         | Duguje – Prihod u toku – Prodajna vrednost <br>Potražuje – Vrednost prodaje obračunatog prihoda |
| Eliminiši                         | Nije primenjivo                                   | Nije primenjivo                                                                                                    | Nije primenljivo                                                  | Potražuje – Vrednost troškova prihoda u toku <br>Duguje – Trošak <br>Potražuje – Obračunati prihod – Vrednost prodaje <br>Duguje – Prihod u toku fakturisan na računu | Duguje – Prihod u toku – Fakturisano na računu <br>Potražuje – Prihod u toku od prodajne vrednosti     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>Konfigurisanje pravila za profile troškova i prihoda projekta

Pravila za profile troškova i prihoda projekta određuju profil troškova i prihoda projekta koji se mora koristiti prilikom obrade svih naplativih transakcija projekta. Definišite pravila odlaskom na **Upravljanje projektima i računovodstvo** \> **Podešavanje** \> **Knjiženje** \> **Pravila za profile troškova i prihoda projekta**.

Pravila se mogu definisati projektnim ugovorom, projektnom grupom ili određenim projektom. Sistem će uvek prvo odabrati pravilo sa najvećom granularnošću.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
