---
title: Dodavanje prilagođenih polja u podešavanje cena i entitete transakcije
description: Ova tema pruža informacije o dodavanju prilagođenih polja u podešavanje cena i entitete transakcije.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3ca48b8d5d55b1b2178f9bd84e19d9599f057aa296a728cca57577c18fdaf307
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985788"
---
# <a name="add-custom-fields-to-price-setup-and-transactional-entities"></a>Dodavanje prilagođenih polja u podešavanje cena i entitete transakcije 

[!include [banner](../includes/psa-now-project-operations.md)]

Ova tema pretpostavlja da ste dovršili procedure u temi [Kreiranje prilagođenih polja i entiteta](create-custom-fields-entities.md). Ako niste dovršili te procedure, vratite se i dovršite ih, a zatim se vratite na ovu temu. 

U ovoj temi, procedure će vam pokazati kako možete da dodate zahtevane reference prilagođenog polja u entitete i elemente korisničkog interfejsa kao što su obrasci i prikazi.

## <a name="add-custom-pricing-dimension-fields"></a>Dodavanje prilagođenog polja dimenzija za određivanje cena 
Nakon kreiranja prilagođenih polja i entiteta, sledeći korak jeste da podešavanje cena i transakcioni entiteti postanu svesni svih prilagođenih entiteta ili skupova opcija kreiranjem referentnih polja. U zavisnosti od toga da li lista dimenzija za određivanje cena uključuje dimenzije skupa opcija, dimenzije entiteta ili oboje, sledite samo korake u prilagođenim dimenzijama za određivanje cena **Prilagođene dimenzije za određivanje cena zasnovane na skupu opcija** ili **Prilagođene dimenzije za određivanje cena zasnovane na entitetu**.

### <a name="option-set-based-custom-pricing-dimensions"></a>Prilagođene dimenzije za određivanje cena zasnovane na skupu opcija
Kada je prilagođena dimenzija za određivanje cena zasnovana na skupu opcija, dodajte je kao polje u ključne Project Service entitete. U sledećoj proceduri, **Radna lokacija resursa** i **Radno vreme resursa** koriste se kao dimenzije za određivanje cena zasnovane na skupu opcija. One prvo moraju da se dodaju kao polja u entitete za određivanje cena **Cena uloge** i **Provizija na cenu uloge**.

1. U usluzi Project Service Automation (PSA) kliknite na **Podešavanja** > **Rešenja**, a zatim dvaput kliknite na **\<your organization name> dimenzije cene**. 
2. U levom oknu za navigaciju istraživača rešenja izaberite **Entiteti > Cena uloge**.
3. Razvijte entitet **Cena uloge** i izaberite opciju **Polja**.
4. Kliknite na **Novo** da biste kreirali novo polje pod nazivom **Radna lokacija resursa** i izaberite **Skup opcija** kao tip polja. 
5. Izaberite **Koristi postojeći skup opcija**, pa skup opcija **Radna lokacija resursa**, a zatim kliknite na **Sačuvaj**.
6. Ponovite korake 1-5 da biste dodali ovo polje u entitet **Provizija na cenu uloge**. 
7. Ponovite korake 1-5 za skup opcija **Radno vreme resursa**.

> [!IMPORTANT]
> Kada dodate polje u više od jednog entiteta, koristite isto ime polja u svim entitetima. 

> ![Dodavanje radne lokacije resursa u cenu uloge.](media/RWL-Field.png)

U fazama prodaje i procene projekta, procena radnih napora koji su neophodni da bi se dovršio **lokalni** posao i posao **na lokaciji** ako se koriste **Standardno radno vreme** i **Prekovremeno radno vreme**, koriste se za procenu vrednost ponude/projekta. Polja **Radna lokacija resursa** i **Radno vreme resursa** će biti dodata u entitete procene **Detalj stavke ponude**, **Detalji predmeta ugovora**, **Projektni zadatak**, **Član projektnog tima** i **Stavka procene**.

1. U PSA kliknite na **Podešavanja** > **Rešenja**, a zatim dvaput kliknite na **\<your organization name> dimenzije cene**. 
2. U levom oknu za navigaciju istraživača rešenja izaberite **Entiteti > Detalj stavke ponude**.
3. Razvijte entitet **Detalj stavke ponude** i izaberite **Polja**.
4. Kliknite na **Novo** da biste kreirali novo polje pod nazivom **Radna lokacija resursa** i izaberite tip polja **Skup opcija**. 
5. Izaberite **Koristi postojeći skup opcija** i **Radna lokacija resursa**, a zatim kliknite na **Sačuvaj**.
6. Ponovite korake 1–5 da biste dodali ovo polje u entitete **Detalj predmeta ugovora za projekat**, **Projektni zadatak**, **Član projektnog tima** i **Stavka procene**.
7. Ponovite korake 1-6 za skup opcija **Radno vreme resursa**. 

> ![Dodavanje radne lokacije resursa u stavku procene.](media/RWL-Default-Value.png)


Za isporuku i fakturisanje, cena dovršenog posla treba da bude precizno određena da biste izabrali da li je obavljen **lokalno** ili **na lokaciji**, kao i da li je dovršen uz opciju **Standardno radno vreme** ili **Prekovremeno** u delu Stvarne vrednosti projekta. Polja **Radna lokacija resursa** i **Radno vreme resursa** treba da dodate u entitete **Stavka vremena**, **Stvarna vrednost**, **Detalj stavke fakture** i **Stavka u glavnoj knjizi**.

1. U PSA kliknite na **Podešavanja** > **Rešenja**, a zatim dvaput kliknite na **\<your organization name> dimenzije cene**.
2. U levom oknu za navigaciju istraživača rešenja izaberite **Entiteti > Stavka vremena**.
3. Razvijte entitet **Detalj stavke ponude**, a zatim izaberite **Polja**.
4. Kliknite na **Novo** da biste kreirali novo polje pod nazivom **Radna lokacija resursa** i izaberite **Skup opcija** kao tip polja. 
5. Izaberite **Koristi postojeći skup opcija**, pa skup opcija **Radna lokacija resursa**, a zatim kliknite na **Sačuvaj**.
6. Ponovite korake 1-5 da biste dodali ovo polje u entitete **Stvarna vrednost**, **Detalj stavke fakture** i **Stavka u glavnoj knjizi**.
7. Ponovite korake 1-6 za skup opcija **Radno vreme resursa**. 

> ![Dodavanje radne lokacije resursa u stavku vremena.](media/RWL-time-entry.png)

Ovim se dovršava promena šeme potrebna za prilagođene dimenzije zasnovane na skupu opcija.

## <a name="entity-based-custom-pricing-dimensions"></a>Prilagođene dimenzije za određivanje cena zasnovane na entitetu

Kada je prilagođena dimenzija za određivanje cena entitet, treba da dodate 1:N odnose između entiteta dimenzije i ključnih Project Service entiteta. Koristeći primer standardne pozicije gore, bilo bi razumno očekivati da svakom zaposlenom bude dodeljena standardna pozicija. Stoga će vam trebati 1: N odnos između standardne pozicije i resursa koji može da se rezerviše, ili N:1 odnos ako je kreiran iz resursa koji se može rezervisati u standardnu poziciju.

1. U PSA kliknite na **Podešavanja** > **Rešenja**, a zatim dvaput kliknite na **\<your organization name> dimenzije cene**. 
2. U levom oknu za navigaciju istraživača rešenja izaberite **Entiteti > Standardna pozicija**.
3. Proširite entitet **Standardna pozicija** i izaberite **1:N odnos**.
4. Kliknite na **Novi** da biste kreirali novi 1:N odnos **Između standardne pozicije i resursa koji može da se rezerviše**. Unesite potrebne informacije, a zatim kliknite na **Sačuvaj**.

> ![Dodavanje standardne pozicije kao referentnog polja u resurs koji može da se rezerviše.](media/ST-BR.png)

Standardna pozicija će takođe morati da se doda u Project Service entitete za određivanje cena **Cena uloge** i **Provizija na cenu uloge**. Ovo se takođe završava pomoću 1:N odnosa između entiteta **Standardna pozicija** i **Cene uloge** i entiteta **Standardna pozicija** i **Provizija na cenu uloge**.

1. U levom oknu za navigaciju istraživača rešenja izaberite **Entiteti > Standardna pozicija**.
2. Proširite entitet **Standardna pozicija** i izaberite **1:N odnos**.
3. Kliknite na **Novi** da biste kreirali novi 1:N odnos **Između standardne pozicije i cene uloge**. Unesite potrebne informacije, a zatim kliknite na **Sačuvaj**.
4. Ponovite korake 1-4 da biste kreirali 1:N odnose između entiteta **Standardna pozicija** i **Provizija na cenu uloge**.

U fazama prodaje i procene projekta, da bi se odredila cena ponude/projekta, za svaku standardnu poziciju su neophodne procene radnih aktivnosti. To znači da su potrebni 1:N odnosi između standardne pozicije i svakog od ovih entiteta procene u usluzi Project Service: 

- **Detalj stavke ponude**
- **Detalj predmeta ugovora za projekat**
- **Projektni zadatak**
- **Član projektnog tima**
- **Stavka procene**

5. Ponovite korake 1–5 da biste kreirali relacije 1:N između stavke **Standardna pozicija** i entiteta **Detalj stavke ponude**, **Detalj predmeta ugovora za projekat**, **Projektni zadatak**, **Član projektnog tima** i **Stavka procene**.

> ![Dodavanje standardne pozicije kao referentnog polja u stavku procene.](media/ST-Estimate-Line.png)

U fazama isporuke i fakturisanja, cena obavljenog posla svake standardne pozicije mora biti precizno određena u delu Stvarne vrednosti projekta. To znači da treba da postoje 1:N odnosi između stavke **Standardna pozicija** i sledećih entiteta: **Stavka vremena**, **Stvarna vrednost**, **Detalj stavke fakture** i **Stavka u glavnoj knjizi**.

6. Ponovite korake 1-6 da biste kreirali 1:N odnose između stavke **Standardna pozicija** i sledećih entiteta: **Stavka vremena**, **Stvarna vrednost**, **Detalj stavke fakture** i **Stavka u glavnoj knjizi**.

> ![Dodavanje standardne pozicije kao referentnog polja u stavku vremena.](media/ST-Mapping.png)

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Podešavanje podrazumevane vrednosti dimenzije pomoću funkcija mapiranja u okviru platforme
Za stavku vremena, bilo bi od pomoći da sistem kao podrazumevanu vrednost podesi standardnu poziciju za stavku vremena iz resursa koji se može rezervisati i koji evidentira stavku vremena. Koristite sledeće korake da biste dodali mapiranja polja za 1:N odnos između entiteta **Resurs koji se može rezervisati** i **Stavka vremena**.

1. U levom oknu za navigaciju istraživača rešenja izaberite **Entiteti > Standardna pozicija**.
2. Proširite entitet **Standardna pozicija** i izaberite **1:N odnos**.
3. Dvaput kliknite na **Resursa koji se može rezervisati za stavku vremena**. Na stranici **Odnos** kliknite na **Korišćenje mapiranja polja**. 
4. Kliknite na **Novo** da biste kreirali novo mapiranje iz polja **Standardna pozicija** u entitetu **Resurs koji može da se rezerviše** u referentno polje **Standardna pozicija** entiteta **Stavka vremena**. 

> ![Podešavanje mapiranja polja radi dozvoljavanja podešavanja podrazumevane vrednosti standardne pozicije iz Resurs koji se može rezervisati u Stavka vremena.](media/ST-Mapping2.png)


Ovim se dovršava promena šeme potrebna za prilagođene dimenzije zasnovane na entitetima.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Dodavanje prilagođenih polja u obrasce, prikaze i poslovna pravila

Kada izvršite sve zahtevane promene šeme, sledeći korak jeste da polja budu vidljiva u korisničkom interfejsu tako što ćete dodati polja u obrasce i prikaze.

1. Otvorite obrazac ili prikaz. U desnom oknu za navigaciju izaberite polje i prevucite ga na podlogu obrasca. 
2. Ako uređujete prikaz, koristite desno okno za navigaciju, kliknite na **Dodaj polja** i u dijalogu **Lista polja** izaberite potrebna polja i kliknite na **U redu**.

Sledeća tabela pruža sveobuhvatnu listu unapred definisanih obrazaca i prikaza koji su navedeni prema entitetu, a koji će morati da se ažuriraju pomoću novih polja. Ako imate dodatne prikaze ili obrasce u okviru prilagođavanja za ove entitete, dodajte nova polja i u njih.

| Project Service entitet        | Obrasci kojima je potrebno novo polje   |Prikazi kojima je potrebno novo polje      |
| ------------------------------|---------------------------------|----------------------------------|
|  Cena uloge|• Informacije |• Aktivne cene kategorija resursa<br> • Vezani prikaz cena kategorija resursa|
|  Provizija na cenu uloge|• Informacije|• Aktivne provizije na cenu uloge<br>• Vezani prikaz provizija na cenu uloge|
|  Detalj stavke ponude|• Informacije o projektu<br>• Brzo kreiranje projekta|• Aktivni detalj stavke ponude<br>• Kombinovani detalji stavke ponude<br>• Vezani prikaz detalja stavki ponude|
|  Detalj predmeta ugovora za projekat|• Informacije o projektu<br>• Brzo kreiranje projekta|• Kombinovani detalji predmeta ugovora<br>• Aktivni detalji predmeta ugovora<br>• Vezani prikaz detalja predmeta ugovora|
|  Projektni zadatak|• Informacije<br>• Novi obrazac||
|  Član projektnog tima|• Informacije<br>• Novi obrazac|• Aktivni članovi projektnog tima<br>• Članovi projektnog tima<br>• Vezani prikaz članova projektnog tima|
|  Stavka vremena|• Informacije<br>• Kreiranje stavke vremena|• Moje stavke vremena prema datumu<br>• Moje stavke vremena za ovu sedmicu<br>• Stavke vremena za odobrenje|
|  Stavka u glavnoj knjizi|• Informacije<br>• Brzo kreiranje|• Aktivne stavke u glavnoj knjizi<br>• Vezani prikaz stavki u glavnoj knjizi|
|  Detalj stavke fakture|• Informacije<br>• Brzo kreiranje|• Aktivni detalji stavke fakture<br>• Naplative transakcije fakture<br>• Besplatne transakcije fakture<br>• Vezani prikaz detalja stavki fakture<br>• Nenaplative transakcije fakture|
|  Stvarno|• Informacije<br>• Aktivne stvarne vrednosti|• Vezani prikaz stvarnih vrednosti|

I prilagođena polja ćete možda morati da dodate u poslovna pravila, u zavisnosti od toga šta ste definisali. Jedan od unapred definisanih primera je za poslovno pravilo **Mogućnost uređivanja stavke vremena na osnovu statusa**. Ovo pravilo definiše polja koja treba da budu zaključana kada stavka vremena ima status koji ne može da se uređuje, npr. **Odobreno**. Dodajte polja u ovo poslovno pravilo tako da polja budu zaključana za uređivanje kada se status stavke vremena razlikuje od **Radna verzija** ili **Vraćena**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]