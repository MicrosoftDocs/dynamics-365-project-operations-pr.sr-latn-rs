---
title: Project Operations podešavanje i integracija podataka o konfiguraciji
description: Ovaj članak pruža informacije o postavljanju i konfigurisanju mapa dvostrukog upisivanja u Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d03393de893c39ceb53c06a3031395f765a26f55
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029169"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Project Operations podešavanje i integracija podataka o konfiguraciji

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ovaj članak pruža informacije o Project Operations integraciji dvostrukog upisivanja za entitete podešavanja i konfiguracije.

## <a name="project-contracts-contract-lines-and-projects"></a>Ugovor za projekat, predmeti ugovora i projekat

Ugovori o projektima, predmeti ugovora i projekti kreiraju se u usluzi Dataverse i sinhronizuju sa aplikacijama za finansije i operacije za dodatno računovodstvo. Zapisi u tim entitetima mogu se kreirati i brisati samo u Dataverse. Međutim, računovodstveni atributi kao što su podrazumevane vrednosti poreza na promet i finansijske dimenzije mogu se dodati ovim evidencijama u aplikacijama za finansije i operacije.

  ![Koncepti integracije ugovora za projekat.](./media/1ProjectContract.jpg)

Potencijalni klijenti aktivnosti prodaje, poslovne mogućnosti i ponude se prate u usluzi Dataverse i ne sinhronizuju se sa aplikacijama za finansije i operacije jer sa ovom aktivnošću nije povezano računovodstvo na nižem nivou.

Funkcionalnost projektnog ugovora u usluzi Dataverse kreira evidenciju ugovora o projektu u aplikacijama za finansije i operacije koje koristi mapa tabela **Zaglavlja projektnih ugovora (porudžbine prodaje)**. Čuvanje ugovora o projektu u Dataverse takođe započinje sa kreiranjem evidencije entiteta klijenata o ugovoru o projektu. Ovaj zapis je sinhronizovan sa aplikacijama za finansije i operacije koje koriste **Izvor finansiranja projekata (msdyn\_projectcontractssplitbillingrules)** mapu tabela. Ova mapa takođe sinhronizuje dodavanja, ažuriranja i brisanja klijenata po ugovoru o projektu. Podeljeni procenti naplate između klijenata projektnih ugovora savladani su samo u usluzi Dataverse i ne sinhronizuju se sa aplikacijama za finansije i operacije.

Nakon kreiranja projektnog ugovora u usluzi Dataverse, projektni računovođa može ažurirati računovodstvene atribute za ovaj projektni ugovor u aplikacijama za finansije i operacije odlaskom na **Upravljanje projektima i računovodstvo** > **Projektni ugovori** > **Podesi** > **Prikaži podrazumevano računovodstvo**. Računovođa može pregledati operativne atribute projektnog ugovora, kao što su traženi datum isporuke i iznos ugovora, izborom ID-a projektnog ugovora u aplikacijama za finansije i operacije koji otvara odgovarajući zapis o ugovoru o projektu u usluzi Dataverse.

Entitet projekta je sinhronizovan sa aplikacijama za finansije i operacije koje koriste **Projekti V2 (msdyn\_projects)** mapu tabela. Računovođa projekta može:

  - da pregleda projekte u aplikacijama za finansije i operacije odlaskom na **Upravljanje projektima i računovodstvo** > **Svi projekti**. 
  - da ažurira računovodstvene atribute za projekat u aplikacijama za finansije i operacije odlaskom na **Upravljanje projektima i računovodstvo** > **Svi projekti** > **Podesi** > **Prikaži podrazumevano računovodstvo**.  
  - pregleda operativne atribute projekta, kao što su procenjeni datumi početka i završetka, izborom ID-a projekta u aplikacijama za finansije i operacije koji otvara srodni projektni zapis u usluzi Dataverse.

Projekat je povezan sa projektnim ugovorom putem entiteta **Predmet ugovora o projektu**.

Predmeti projektnog ugovora u usluzi Dataverse kreiraju evidenciju ugovora o projektu u aplikacijama za finansije i operacije koje koristi mapa tabela **Predmeti ugovora projekta (salesorderdetails)**. Način naplate definiše tip pravila o naplati projektnog ugovora u aplikacijama za finansije i operacije:

  - Predmeti projektnih ugovora sa načinom naplate vremena i materijala kreiraju pravilo naplate vremena i vrste materijala.
  - Predmeti ugovora metoda obračuna sa fiksnom cenom kreiraju važno pravilo naplate.

Predmete projektnih ugovora može pregledati računovođa u aplikacijama za finansije i operacije odlaskom na **Upravljanje projektima i računovodstvo** > **Projektni ugovori** > **Podesi** > **Prikaži podrazumevano računovodstvo**, i pregledom detalja na kartici **Predmeti ugovora**. Računovođa na ovoj kartici takođe može postaviti zadate finansijske dimenzije za predmete ugovora metoda obračuna sa fiksnom cenom.

## <a name="billing-milestones"></a>Kontrolne tačke fakturisanja

Predmeti projektnih ugovora koje koriste metodu obračuna sa fiksnom cenom fakturišu se kroz fakture naplate. Kontrolne tačke u obračunu sinhronizuju se sa transakcijama na nalogu projekta u aplikacijama za finansije i operacije pomoću mape tabela **Kontrolne tačke predmeta ugovora o Project Operations integraciji (msdyn\_contractlinescheduleofvalues)**.

  ![Integracija kontrolnih tačaka fakturisanja.](./media/2Milestones.jpg)

Računovođa može pregledati transakcije na računu i tako prilagoditi računovodstvene atribute za te transakcije ako izabere **Upravljanje projektima i računovodstvo** > **Projektni ugovori** > **Uspostavi** > **Transakcije na nalogu** ili **Upravljanje projektima i računovodstvo** > **Svi projekti** > **Uspostavi** > **Transakcije na nalogu**.

Kada prvi put kreirate prekretnicu za obračun za datu liniju ugovora o projektu, sistem automatski kreira projekat procene prihoda sa fiksnom cenom za projekat povezan sa ovom linijom ugovora. Projekti procene prihoda sa fiksnom cenom mogu se pregledati odlaskom na **Upravljanje projektima i računovodstvo** > **Projekti procene prihoda sa fiksnom cenom**.

### <a name="project-tasks"></a>Projektni zadaci

Projektni zadaci su sinhronizovani sa aplikacijama za finansije i operacije kroz mapu tabela **Projektni zadaci (msdyn\_projecttasks)** samo za referencu. Stvaranje, ažuriranje i brisanje nisu podržani putem aplikacija za finansije i operacije.

  ![Integracija zadataka projekta.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Resursi za projekat

Entitet **Uloge projektnih resursa** je sinhronizovan sa aplikacijama za finansije i operacije koje koriste mapu tabele **Uloge projektnih resursa za sve kompanije (kategorije koje se mogu rezervisati)** samo za referencu. Pošto uloge resursa u usluzi Dataverse nisu specifične za kompaniju, sistem automatski kreira odgovarajuće zapise o ulogama resursa specifičnih za kompaniju u aplikacijama za finansije i operacije automatski za sva pravna lica uključena u obim integracije dvostrukog upisivanja.

![Integracija uloga resursa.](./media/5Resources.jpg)

Projektni resursi u Project Operations održavaju se u usluzi Dataverse i nisu sinhronizovani sa aplikacijama za finansije i operacije.

### <a name="transaction-categories"></a>Kategorije transakcija

Kategorije transakcija se održavaju u usluzi Dataverse i sinhronizuju se sa aplikacijama za finansije i operacije koje koriste mapu tabela **Kategorije projektnih transakcija (msdyn\_transactioncategories)**. Nakon sinhronizacije zapisa kategorije transakcije, sistem automatski kreira četiri zapisa deljene kategorije. Svaki zapis odgovara tipu transakcije u aplikacijama za finansije i operacije i povezuje ih sa zapisom kategorije transakcije.

![Integracija kategorija transakcije.](./media/4TransactionCategories.jpg)

Korišćenje kategorija transakcija za procene i stvarne podatke zahteva od knjigovođe projekta ili administratora sistema da kreira odgovarajuće kategorije projekata u svakom pravnom licu. Za više informacija, pogledajte odeljak [Konfigurisanje kategorija projekata](../project-accounting/configure-project-categories.md).
