---
title: Dodavanje obaveznih prilagođenih polja u podešavanje cena i entitete transakcije
description: Ova tema pruža informacije o tome kako treba dodati potrebne reference prilagođenih polja u entitete i u obrasce i prikaze.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e589465eb98723b3b49c5d96e263eb3abf15eb2c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083620"
---
# <a name="add-required-custom-fields-to-price-setup-and-transactional-entities"></a>Dodavanje obaveznih prilagođenih polja u podešavanje cena i entitete transakcije

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Ova tema pretpostavlja da ste dovršili procedure u temi [Kreiranje prilagođenih polja i entiteta koji se koriste kao dimenzije za određivanje cena](create-custom-fields-entities-pricing-dimensions.md). Ako niste dovršili te procedure, vratite se i dovršite ih, a zatim se vratite na ovu temu. 

U ovoj temi, procedure će vam pokazati kako možete da dodate zahtevane reference prilagođenog polja u entitete i elemente korisničkog interfejsa kao što su obrasci i prikazi.

## <a name="add-custom-pricing-dimension-fields"></a>Dodavanje prilagođenog polja dimenzija za određivanje cena 
Nakon kreiranja prilagođenih polja i entiteta, sledeći korak jeste da podešavanje cena i transakcioni entiteti postanu svesni svih prilagođenih entiteta ili skupova opcija kreiranjem referentnih polja. U zavisnosti od toga da li lista dimenzija za određivanje cena uključuje dimenzije skupa opcija, dimenzije entiteta ili oboje, sledite samo korake u prilagođenim dimenzijama za određivanje cena **Prilagođene dimenzije za određivanje cena zasnovane na skupu opcija** ili **Prilagođene dimenzije za određivanje cena zasnovane na entitetu**.

### <a name="option-set-based-custom-pricing-dimensions"></a>Prilagođene dimenzije za određivanje cena zasnovane na skupu opcija
Kada je prilagođena dimenzija za određivanje cena zasnovana na skupu opcija, dodajte je kao polje u ključne entitete. U sledećoj proceduri, **Radna lokacija resursa** i **Radno vreme resursa** koriste se kao dimenzije za određivanje cena zasnovane na skupu opcija. One prvo moraju da se dodaju kao polja u entitete za određivanje cena **Cena uloge** i **Provizija na cenu uloge**.

1. U odeljku Projektne radnje izaberite **Podešavanja** > **Rešenja** , a zatim dvaput kliknite na **\<your organization name> dimenzije za određivanje cena**. 
2. U levom oknu za navigaciju istraživača rešenja izaberite **Entiteti > Cena uloge**.
3. Razvijte entitet **Cena uloge** i izaberite opciju **Polja**.
4. Izaberite **Novo** da biste kreirali novo polje pod nazivom **Radna lokacija resursa** i izaberite **Skup opcija** kao tip polja. 
5. Izaberite **Koristi postojeći skup opcija** , pa skup opcija **Radna lokacija resursa** , a zatim izaberite **Sačuvaj**.
6. Ponovite korake 1-5 da biste dodali ovo polje u entitet **Provizija na cenu uloge**. 
7. Ponovite korake 1-5 za skup opcija **Radno vreme resursa**.

> [!IMPORTANT]
> Kada dodate polje u više od jednog entiteta, koristite isto ime polja u svim entitetima. 

U fazama prodaje i procene projekta, procena radnih napora koji su neophodni da bi se dovršio **lokalni** posao i posao **na lokaciji** ako se koriste **Standardno radno vreme** i **Prekovremeno radno vreme** , koriste se za procenu vrednost ponude/projekta. Polja **Radna lokacija resursa** i **Radno vreme resursa** će biti dodati u entitete procena **Detalj stavke ponude** , **Detalji predmeta ugovora** , **Član projektnog tima** i **Stavka procene**.

1. U odeljku Projektne radnje izaberite **Podešavanja** > **Rešenja** , a zatim dvaput kliknite na **\<your organization name> dimenzije za određivanje cena**. 
2. U levom oknu za navigaciju istraživača rešenja izaberite **Entiteti > Detalj stavke ponude**.
3. Razvijte entitet **Detalj stavke ponude** i izaberite **Polja**.
4. Izaberite **Novo** da biste kreirali novo polje pod nazivom **Radna lokacija resursa** i izaberite tip polja **Skup opcija**. 
5. Izaberite **Koristi postojeći skup opcija** i **Radna lokacija resursa** , a zatim izaberite **Sačuvaj**.
6. Ponovite korake 1-5 da biste dodali ovo polje u entitete **Detalj predmeta ugovora za projekat** , **Član projektnog tima** i **Stavka procene**.
7. Ponovite korake 1-6 za skup opcija **Radno vreme resursa**. 

Za isporuku i fakturisanje, cena dovršenog posla treba da bude precizno određena da biste izabrali da li je obavljen **lokalno** ili **na lokaciji** , kao i da li je dovršen uz opciju **Standardno radno vreme** ili **Prekovremeno** u delu Stvarne vrednosti projekta. Polja **Radna lokacija resursa** i **Radno vreme resursa** treba da dodate u entitete **Stavka vremena** , **Stvarna vrednost** , **Detalj stavke fakture** i **Stavka u glavnoj knjizi**.

1. Izaberite **Podešavanja** > **Rešenja** , a zatim dvaput kliknite na **\<your organization name> dimenzije za određivanje cena**.
2. U levom oknu za navigaciju istraživača rešenja izaberite **Entiteti > Stavka vremena**.
3. Razvijte entitet **Detalj stavke ponude** , a zatim izaberite **Polja**.
4. Izaberite **Novo** da biste kreirali novo polje pod nazivom **Radna lokacija resursa** i izaberite **Skup opcija** kao tip polja. 
5. Izaberite **Koristi postojeći skup opcija** , pa skup opcija **Radna lokacija resursa** , a zatim izaberite **Sačuvaj**.
6. Ponovite korake 1-5 da biste dodali ovo polje u entitete **Stvarna vrednost** , **Detalj stavke fakture** i **Stavka u glavnoj knjizi**.
7. Ponovite korake 1-6 za skup opcija **Radno vreme resursa**. 

Ovim se dovršava promena šeme potrebna za prilagođene dimenzije zasnovane na skupu opcija.

## <a name="entity-based-custom-pricing-dimensions"></a>Prilagođene dimenzije za određivanje cena zasnovane na entitetu

Kada je prilagođena dimenzija za određivanje cena entitet, treba da dodate 1:N odnose između entiteta dimenzije i ključnih entiteta. Koristeći primer standardne pozicije gore, bilo bi razumno očekivati da svakom zaposlenom bude dodeljena standardna pozicija. Stoga će vam trebati 1: N odnos između standardne pozicije i resursa koji može da se rezerviše, ili N:1 odnos ako je kreiran iz resursa koji se može rezervisati u standardnu poziciju.

1. U odeljku Projektne radnje izaberite **Podešavanja** > **Rešenja** , a zatim dvaput kliknite na **\<your organization name> dimenzije za određivanje cena**. 
2. U levom oknu za navigaciju istraživača rešenja izaberite **Entiteti > Standardna pozicija**.
3. Proširite entitet **Standardna pozicija** i izaberite **1:N odnos**.
4. Izaberite **Novo** da biste kreirali novu 1:N relaciju pod nazivom **Između standardne pozicije i resursa koji može da se rezerviše**. Unesite potrebne informacije, a zatim izaberite **Sačuvaj**.

Standardna pozicija će takođe morati da se doda u entitete za određivanje cena **Cena uloge** i **Provizija na cenu uloge**. Ovo se takođe završava pomoću 1:N odnosa između entiteta **Standardna pozicija** i **Cene uloge** i entiteta **Standardna pozicija** i **Provizija na cenu uloge**.

1. U levom oknu za navigaciju istraživača rešenja izaberite **Entiteti > Standardna pozicija**.
2. Proširite entitet **Standardna pozicija** i izaberite **1:N odnos**.
3. Izaberite **Novo** da biste kreirali novu 1:N relaciju **Između standardne pozicije i cene uloge**. Unesite potrebne informacije, a zatim izaberite **Sačuvaj**.
4. Ponovite korake 1-4 da biste kreirali 1:N odnose između entiteta **Standardna pozicija** i **Provizija na cenu uloge**.

U fazama prodaje i procene projekta, da bi se odredila cena ponude/projekta, za svaku standardnu poziciju su neophodne procene radnih aktivnosti. To znači da su potrebne 1:N relacije između standardne pozicije i svakog od ovih entiteta procene: 

- **Detalj stavke ponude**
- **Detalj predmeta ugovora za projekat**
- **Član projektnog tima**
- **Stavka procene**

5. Ponovite korake 1-5 da biste kreirali 1:N odnose između stavke **Standardna pozicija** i **Detalj stavke ponude** , **Detalj predmeta ugovora za projekat** , **Član projektnog tima** i **Stavka procene**.

  U fazama isporuke i fakturisanja, cena obavljenog posla svake standardne pozicije mora biti precizno određena u delu Stvarne vrednosti projekta. To znači da treba da postoje 1:N odnosi između stavke **Standardna pozicija** i sledećih entiteta: **Stavka vremena** , **Stvarna vrednost** , **Detalj stavke fakture** i **Stavka u glavnoj knjizi**.

6. Ponovite korake 1-6 da biste kreirali 1:N odnose između stavke **Standardna pozicija** i sledećih entiteta: **Stavka vremena** , **Stvarna vrednost** , **Detalj stavke fakture** i **Stavka u glavnoj knjizi**.

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Podešavanje podrazumevane vrednosti dimenzije pomoću funkcija mapiranja u okviru platforme
Za stavku vremena, bilo bi od pomoći da sistem kao podrazumevanu vrednost podesi standardnu poziciju za stavku vremena iz resursa koji se može rezervisati i koji evidentira stavku vremena. Koristite sledeće korake da biste dodali mapiranja polja za 1:N odnos između entiteta **Resurs koji se može rezervisati** i **Stavka vremena**.

1. U levom oknu za navigaciju istraživača rešenja izaberite **Entiteti > Standardna pozicija**.
2. Proširite entitet **Standardna pozicija** i izaberite **1:N odnos**.
3. Dvaput kliknite na **Resursa koji se može rezervisati za stavku vremena**. Na stranici **Odnos** izaberite **Korišćenje mapiranja polja**. 
4. Izaberite **Novo** da biste kreirali novo mapiranje iz polja **Standardna pozicija** u entitetu **Resurs koji može da se rezerviše** u referentno polje **Standardna pozicija** entiteta **Stavka vremena**. 

Ovim se dovršava promena šeme potrebna za prilagođene dimenzije zasnovane na entitetima.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Dodavanje prilagođenih polja u obrasce, prikaze i poslovna pravila

Kada izvršite sve zahtevane promene šeme, sledeći korak jeste da polja budu vidljiva u korisničkom interfejsu tako što ćete dodati polja u obrasce i prikaze.

1. Otvorite obrazac ili prikaz. U desnom oknu za navigaciju izaberite polje i prevucite ga na podlogu obrasca. 
2. Ako uređujete prikaz, koristite desno okno za navigaciju, izaberite **Dodaj polja** i u dijalogu **Lista polja** izaberite potrebna polja i izaberite **U redu**.

Sledeća tabela pruža sveobuhvatnu listu unapred definisanih obrazaca i prikaza koji su navedeni prema entitetu, a koji će morati da se ažuriraju pomoću novih polja. Ako imate dodatne prikaze ili obrasce u okviru prilagođavanja za ove entitete, dodajte nova polja i u njih.

| Entity        | Obrasci kojima je potrebno novo polje   |Prikazi kojima je potrebno novo polje      |
| ------------------------------|---------------------------------|----------------------------------|
|  Cena uloge|• Informacije |• Aktivne cene kategorija resursa<br> • Vezani prikaz cena kategorija resursa|
|  Provizija na cenu uloge|• Informacije|• Aktivne provizije na cenu uloge<br>• Vezani prikaz provizija na cenu uloge|
|  Detalj stavke ponude|• Informacije o projektu<br>• Brzo kreiranje projekta|• Aktivni detalj stavke ponude<br>• Kombinovani detalji stavke ponude<br>• Vezani prikaz detalja stavki ponude|
|  Detalj predmeta ugovora za projekat|• Informacije o projektu<br>• Brzo kreiranje projekta|• Kombinovani detalji predmeta ugovora<br>• Aktivni detalji predmeta ugovora<br>• Vezani prikaz detalja predmeta ugovora|
|  Član projektnog tima|• Informacije<br>• Novi obrazac|• Aktivni članovi projektnog tima<br>• Članovi projektnog tima<br>• Vezani prikaz članova projektnog tima|
|  Stavka vremena|• Informacije<br>• Kreiranje stavke vremena|• Moje stavke vremena prema datumu<br>• Moje stavke vremena za ovu sedmicu<br>• Stavke vremena za odobrenje|
|  Stavka u glavnoj knjizi|• Informacije<br>• Brzo kreiranje|• Aktivne stavke u glavnoj knjizi<br>• Vezani prikaz stavki u glavnoj knjizi|
|  Detalj stavke fakture|• Informacije<br>• Brzo kreiranje|• Aktivni detalji stavke fakture<br>• Naplative transakcije fakture<br>• Besplatne transakcije fakture<br>• Vezani prikaz detalja stavki fakture<br>• Nenaplative transakcije fakture|
|  Stvarno|• Informacije<br>• Aktivne stvarne vrednosti|• Vezani prikaz stvarnih vrednosti|

I prilagođena polja ćete možda morati da dodate u poslovna pravila, u zavisnosti od toga šta ste definisali. Jedan od unapred definisanih primera je za poslovno pravilo **Mogućnost uređivanja stavke vremena na osnovu statusa**. Ovo pravilo definiše polja koja treba da budu zaključana kada stavka vremena ima status koji ne može da se uređuje, npr. **Odobreno**. Dodajte polja u ovo poslovno pravilo tako da polja budu zaključana za uređivanje kada se status stavke vremena razlikuje od **Radna verzija** ili **Vraćena**.
