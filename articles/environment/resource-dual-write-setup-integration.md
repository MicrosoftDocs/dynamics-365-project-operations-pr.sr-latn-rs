---
title: Project Operations podešavanje i integracija podataka o konfiguraciji
description: Ova tema pruža informacije o postavljanju i konfigurisanju mapa dvostrukog upisivanja u Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1e9ca9407404274648f359be42d350137775ae55
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001083"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Project Operations podešavanje i integracija podataka o konfiguraciji

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ova tema pruža informacije o Project Operations integraciji dvostrukog upisivanja za entitete podešavanja i konfiguracije.

## <a name="project-contracts-contract-lines-and-projects"></a>Ugovor za projekat, predmeti ugovora i projekat

Ugovori o projektima, predmeti ugovora i projekti kreiraju se u Dataverse i sinhronizuju sa Finance and Operations aplikacijama za dodatno računovodstvo. Zapisi u tim entitetima mogu se kreirati i brisati samo u Dataverse. Međutim, računovodstveni atributi kao što su podrazumevane vrednosti poreza na promet i finansijske dimenzije mogu se dodati ovim evidencijama u Finance and Operations aplikacijama.

  ![Koncepti integracije ugovora za projekat](./media/1ProjectContract.jpg)

Potencijalni klijenti aktivnosti prodaje, poslovne mogućnosti i ponude se prate u Dataverse i ne sinhronizuju se sa Finance and Operations aplikacijama jer sa ovom aktivnošću nije povezano računovodstvo na nižem nivou.

Funkcionalnost projektnog ugovora u Dataverse kreira evidenciju ugovora o projektu u Finance and Operations aplikacijama koje koristi mapa tabela **Zaglavlja projektnih ugovora (porudžbine prodaje)**. Čuvanje ugovora o projektu u Dataverse takođe započinje sa kreiranjem evidencije entiteta klijenata o ugovoru o projektu. Ovaj zapis je sinhronizovan sa Finance and Operations aplikacijama koje koriste **Izvor finansiranja projekata (msdyn\_projectcontractssplitbillingrules)** mapu tabela. Ova mapa takođe sinhronizuje dodavanja, ažuriranja i brisanja klijenata po ugovoru o projektu. Podeljeni procenti naplate između klijenata projektnih ugovora savladani su samo u Dataverse i ne sinhronizuju se sa Finance and Operations aplikacijama.

Nakon kreiranja projektnog ugovora u Dataverse, projektni računovođa može ažurirati računovodstvene atribute za ovaj projektni ugovor u Finance and Operations aplikacijama odlaskom na **Upravljanje projektima i računovodstvo** > **Projektni ugovori** > **Podesi** > **Prikaži podrazumevano računovodstvo**. Računovođa može pregledati operativne atribute projektnog ugovora, kao što su traženi datum isporuke i iznos ugovora, izborom ID-a projektnog ugovora u Finance and Operations aplikacijama koji otvara odgovarajući zapis o ugovoru o projektu u Dataverse.

Entitet projekta je sinhronizovan sa Finance and Operations aplikacijama koje koriste **Projekti V2 (msdyn\_projects)** mapu tabela. Računovođa projekta može:

  - da pregleda projekte u Finance and Operations aplikacijama odlaskom na **Upravljanje projektima i računovodstvo** > **Svi projekti**. 
  - da ažuriraj računovodstvene atribute za projekat u Finance and Operations aplikacijama odlaskom na **Upravljanje projektima i računovodstvo** > **Svi projekti** > **Podesi** > **Prikaži podrazumevano računovodstvo**.  
  - Pregledajte operativne atribute projekta, kao što su procenjeni datumi početka i završetka, izborom ID-a projekta u Finance and Operations aplikacijama koji otvara srodni projektni zapis u Dataverse.

Projekat je povezan sa projektnim ugovorom putem entiteta **Predmet ugovora o projektu**.

Predmeti projektnog ugovora u Dataverse kreiraju evidenciju ugovora o projektu u Finance and Operations aplikacijama koje koristi mapa tabela **Predmeti ugovora projekta (salesorderdetails)**. Metod naplate definiše tip pravila za obračun ugovora u Finance and Operations aplikacijama:

  - Predmeti projektnih ugovora sa načinom naplate vremena i materijala kreiraju pravilo naplate vremena i vrste materijala.
  - Predmeti ugovora metoda obračuna sa fiksnom cenom kreiraju važno pravilo naplate.

Predmete projektnih ugovora može pregledati računovođa u Finance and Operations aplikacijama odlaskom na **Upravljanje projektima i računovodstvo** > **Projektni ugovori** > **Podesi** > **Prikaži podrazumevano računovodstvo**, i pregledom detalja na kartici **Predmeti ugovora**. Računovođa na ovoj kartici takođe može postaviti zadate finansijske dimenzije za predmete ugovora metoda obračuna sa fiksnom cenom.

## <a name="billing-milestones"></a>Kontrolne tačke fakturisanja

Predmeti projektnih ugovora koje koriste metodu obračuna sa fiksnom cenom fakturišu se kroz fakture naplate. Kontrolne tačke u obračunu sinhronizuju se sa transakcijama na nalogu projekta u Finance and Operations aplikacijama pomoću **Kontrolne tačke predmeta ugovora o Project Operations integraciji (msdyn\_contractlinescheduleofvalues)** mape tabela.

  ![Integracija kontrolnih tačaka fakturisanja](./media/2Milestones.jpg)

Računovođa može pregledati transakcije na računu i tako prilagoditi računovodstvene atribute za te transakcije ako izabere **Upravljanje projektima i računovodstvo** > **Projektni ugovori** > **Uspostavi** > **Transakcije na nalogu** ili **Upravljanje projektima i računovodstvo** > **Svi projekti** > **Uspostavi** > **Transakcije na nalogu**.

Kada prvi put kreirate prekretnicu za obračun za datu liniju ugovora o projektu, sistem automatski kreira projekat procene prihoda sa fiksnom cenom za projekat povezan sa ovom linijom ugovora. Projekti procene prihoda sa fiksnom cenom mogu se pregledati odlaskom na **Upravljanje projektima i računovodstvo** > **Projekti procene prihoda sa fiksnom cenom**.

### <a name="project-tasks"></a>Projektni zadaci

Projektni zadaci su sinhronizovani sa Finance and Operations aplikacijama kroz **Projektni zadaci (msdyn\_projecttasks)** mapu tabela samo za referencu. Stvaranje, ažuriranje i brisanje nisu podržani putem Finance and Operations aplikacija.

  ![Integracija zadataka projekta](./media/3Tasks.jpg)

## <a name="project-resources"></a>Resursi za projekat

Entitet **Uloge projektnih resursa** je sinhronizovan sa Finance and Operations aplikacijama koje koriste **Uloge projektnih resursa za sve kompanije (kategorije koje se mogu rezervisati)** mapu tabele samo za referencu. Pošto uloge resursa u Dataverse nisu specifične za kompaniju, sistem automatski kreira odgovarajuće zapise o ulogama resursa specifičnih za kompaniju u Finance and Operations aplikacijama automatski za sva pravna lica uključena u obim integracije dvostrukog upisivanja.

![Integracija uloga resursa](./media/5Resources.jpg)

Projektni resursi u Project Operations održavaju se u Dataverse i nisu sinhronizovani sa Finance and Operations aplikacijama.

### <a name="transaction-categories"></a>Kategorije transakcija

Kategorije transakcija se održavaju u Dataverse i sinhronizuju se sa Finance and Operations aplikacijama koje koriste **Kategorije projektnih transakcija (msdyn\_transactioncategories)** mapu tabela. Nakon sinhronizacije zapisa kategorije transakcije, sistem automatski kreira četiri zapisa deljene kategorije. Svaki zapis odgovara tipu transakcije u Finance and Operations aplikacijama i povezuje ih sa zapisom kategorije transakcije.

![Integracija kategorija transakcije](./media/4TransactionCategories.jpg)

Korišćenje kategorija transakcija za procene i stvarne podatke zahteva od knjigovođe projekta ili administratora sistema da kreira odgovarajuće kategorije projekata u svakom pravnom licu. Za više informacija, pogledajte odeljak [Konfigurisanje kategorija projekata](../project-accounting/configure-project-categories.md).
