---
title: Project Operations podešavanje i integracija podataka o konfiguraciji
description: Ovaj članak pruža informacije o podešavanju i konfigurisanju mapa dvostrukog pisanja operacija projekta.
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

Ovaj članak pruža informacije o integraciji dvostrukog upisivanja operacija projekta za entitete podešavanja i konfiguracije.

## <a name="project-contracts-contract-lines-and-projects"></a>Ugovor za projekat, predmeti ugovora i projekat

Ugovori o projektu, redovi ugovora i projekti se kreiraju i sinhronizuju Dataverse sa aplikacijama za finansiranje i operacije radi dodatnog knjigovodstva. Zapisi u tim entitetima mogu se kreirati i brisati samo u Dataverse. Međutim, računovodstveni atributi kao što su podrazumevane vrednosti grupe poreza na promet i finansijske dimenzije mogu se dodati ovim zapisima u aplikacijama za finansije i operacije.

  ![Koncepti integracije ugovora za projekat.](./media/1ProjectContract.jpg)

Potencijalne klijente, mogućnosti za poslovanje i ponude Dataverse se prate i ne sinhronizuju sa aplikacijama za finansiranje i operacije jer ne postoji nizvodno knjigovodstvo povezano sa ovom aktivnošću.

Funkcionalnost ugovora o projektu kreira zapis ugovora Dataverse o projektu u aplikacijama za finansije i operacije pomoću **mape tabele Zaglavlja ugovora** projekta (prodavci). Čuvanje ugovora o projektu u Dataverse takođe započinje sa kreiranjem evidencije entiteta klijenata o ugovoru o projektu. Ovaj zapis se sinhronizuje sa aplikacijama za finansiranje i operacije pomoću **mape tabele "Izvor finansiranja projekta" (msdyn\_ projectcontractssplitlitlingrules**). Ova mapa takođe sinhronizuje dodavanja, ažuriranja i brisanja klijenata po ugovoru o projektu. Razdeljeni procenti naplate između klijenata projektnog ugovora se ovladaju samo i Dataverse ne sinhronizuju sa aplikacijama za finansije i operacije.

Nakon kreiranja ugovora o projektu Dataverse u programu, knjigovođa projekta može da ažurira računovodstvene atribute za ovaj projektni ugovor u aplikacijama za finansije i operacije tako što će ići **na ugovore o upravljanju projektima** > **i knjigovodstvenim** > **·** > **projektima Podesiti Prikaži podrazumevano knjigovodstvo**. Knjigovođa može da pregleda atribute operativnog ugovora o projektu, kao što su zahtevani datum isporuke i iznos ugovora tako što će izabrati ID ugovora o projektu u aplikacijama za finansije i operacije koji otvara povezani zapis ugovora o projektu u programu Dataverse.

Entitet projekta se sinhronizuje sa aplikacijama za finansiranje i operacije pomoću **mape tabele Projekti V2 (msdyn\_** projekti). Računovođa projekta može:

  - Pregledajte projekte u aplikacijama za finansije i operacije tako što ćete ići na **Project management i računovodstvo** > **Svi projekti**. 
  - Ažurirajte računovodstvene atribute za projekat u aplikacijama za finansije i operacije tako što ćete ići na **upravljanje projektima i računovodstvo** > **Svi projekti** > **Podesite Prikaži podrazumevano** > **knjigovodstvo**.  
  - Pregledajte atribute operativnog projekta, kao što su procenjeni datumi početka i završetka, tako što ćete izabrati ID projekta u aplikacijama za finansije i operacije koji otvara povezani zapis projekta u programu Dataverse.

Projekat je povezan sa projektnim ugovorom putem entiteta **Predmet ugovora o projektu**.

Redovi ugovora o projektu u Dataverse kreiranju pravila o naplati ugovora o projektu u aplikacijama za **finansije i operacije pomoću mape tabele "Redovi ugovora** projekta ( prodajne jedinice)". Način naplate definiše tip pravila o naplati ugovora o projektu u aplikacijama za finansije i operacije:

  - Predmeti projektnih ugovora sa načinom naplate vremena i materijala kreiraju pravilo naplate vremena i vrste materijala.
  - Predmeti ugovora metoda obračuna sa fiksnom cenom kreiraju važno pravilo naplate.

Redove ugovora o projektu može da pregleda knjigovođa projekta u aplikacijama za finansije i operacije tako što će ići na **ugovore o upravljanju** > **projektima i računovodstvu** > **Projekta Podesiti** > **Prikaži podrazumevano** knjigovodstvo i pregledati detalje na **kartici Redovi** ugovora. Knjigovođa takođe može postaviti podrazumevane finansijske dimenzije za redove ugovora o fiksnoj ceni na ovoj kartici.

## <a name="billing-milestones"></a>Kontrolne tačke fakturisanja

Predmeti projektnih ugovora koje koriste metodu obračuna sa fiksnom cenom fakturišu se kroz fakture naplate. Prekretnice u naplati sinhronizuju se sa projektovanjem transakcija na **računu u aplikacijama za finansije i operacije korišćenjem prekretnica reda ugovora o integraciji sa operacijama projekta (msdyn\_ contractlinescheduleofvalues).**

  ![Integracija kontrolnih tačaka fakturisanja.](./media/2Milestones.jpg)

Računovođa može pregledati transakcije na računu i tako prilagoditi računovodstvene atribute za te transakcije ako izabere **Upravljanje projektima i računovodstvo** > **Projektni ugovori** > **Uspostavi** > **Transakcije na nalogu** ili **Upravljanje projektima i računovodstvo** > **Svi projekti** > **Uspostavi** > **Transakcije na nalogu**.

Kada prvi put kreirate prekretnicu za obračun za datu liniju ugovora o projektu, sistem automatski kreira projekat procene prihoda sa fiksnom cenom za projekat povezan sa ovom linijom ugovora. Projekti procene prihoda sa fiksnom cenom mogu se pregledati odlaskom na **Upravljanje projektima i računovodstvo** > **Projekti procene prihoda sa fiksnom cenom**.

### <a name="project-tasks"></a>Projektni zadaci

Projektni zadaci se sinhronizuju sa aplikacijama za finansiranje i operacije **kroz mapu tabele Projektnih zadataka (msdyn\_ projecttasks)** samo u referentne svrhe. Kreiranje, ažuriranje i brisanje operacija nije podržano pomoću aplikacija za finansije i operacije.

  ![Integracija zadataka projekta.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Resursi za projekat

Entitet **uloga resursa projekta** se sinhronizuje sa aplikacijama za finansiranje **i operacije koristeći uloge resursa projekta za sva preduzeća (bookableresourcecategories)** mapu tabele samo u referentne svrhe. Pošto uloge resursa Dataverse u njima nisu specifične za preduzeća, sistem automatski kreira odgovarajuće zapise o ulogama resursa specifičnih za preduzeća u aplikacijama za finansije i operacije automatski za sva pravna lica uključena u opseg integracije sa dva upisivanja.

![Integracija uloga resursa.](./media/5Resources.jpg)

Projektni resursi u operacijama projekta se održavaju i Dataverse ne sinhronizuju sa aplikacijama za finansiranje i operacije.

### <a name="transaction-categories"></a>Kategorije transakcija

Kategorije transakcija se održavaju i sinhronizuju Dataverse sa aplikacijama za finansiranje i operacije pomoću **mape tabele "Kategorije transakcija projekta" (msdyn\_ transactioncategories**). Nakon sinhronizacije zapisa kategorije transakcije, sistem automatski kreira četiri zapisa deljene kategorije. Svaki zapis odgovara vrsti transakcije u aplikacijama za finansije i operacije i povezuje ih sa zapisom kategorije transakcije.

![Integracija kategorija transakcije.](./media/4TransactionCategories.jpg)

Korišćenje kategorija transakcija za procene i stvarne podatke zahteva od knjigovođe projekta ili administratora sistema da kreira odgovarajuće kategorije projekata u svakom pravnom licu. Za više informacija, pogledajte odeljak [Konfigurisanje kategorija projekata](../project-accounting/configure-project-categories.md).
