---
title: Razmatranja nadogradnje strukturne analize posla
description: Ova tema pruža informacije o nadogradnji strukturne analize posla iz aplikacije Project Service Automation verzije 2.x u verziju 3.x.
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: 5258813410c3cea015775898cc72ba1574549edd8ee0c8b7aad8c94943eb5a60
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992358"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Razmatranja nadogradnje strukturne analize posla

[!include [banner](../includes/psa-now-project-operations.md)]

Ova tema pruža informacije o nadogradnji strukturne analize posla iz aplikacije Project Service Automation verzije 2.x u verziju 3.x. Ova tema definiše ispravno stanje projekta u aplikaciji Project Service Automation (PSA), potrebno za uspešnu nadogradnju. Postoje i informacije o uobičajenim uslovima blokiranja koji će dovesti do neuspešne nadogradnje. Više informacija o definisanju projektnih zadataka i njihovim funkcijama u okviru rasporeda projekta potražite u članku [Rasporedi projekata](project-creating.md).

## <a name="key-entities"></a>Ključni entiteti
Za ispravnu strukturnu analizu posla koja je već učitana sa resursima, potrebni su sledeći entiteti:

- [Projekat](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [Projektni tim](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [Projektni zadatak](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [Dodele resursa](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [Zavisnost projektnog zadatka](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [Resursi koji mogu da se rezervišu](/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

Da biste definisali strukturnu analizu posla koju je učitao resurs, morate da dovršite sledeće korake:

1. Kreirajte novi projekat. Za više informacija o tome kako da kreirate novi projekat, pogledajte [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).
2. Kreirajte jedan ili više zadataka. Za više informacija o tome kako da kreirate novi zadatak, pogledajte [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).
3. Definišite zavisne elemente zadatka. Za još informacija pogledajte [Zavisnost projektnog zadatka](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).
4. Dodelite članove projektnog tima projektu. Za više informacija, pogledajte [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).
5. Dodelite članove projektnog tima zadacima. Za više informacija, pogledajte [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).

## <a name="project-team-relationships"></a>Odnosi unutar projektnog tima

Da biste osigurali uspešnu nadogradnju, sledeći odnosi moraju se pravilno održavati:
- Svi članovi projektnog tima moraju biti povezani sa resursom koji se može rezervisati.
- Svi članovi projektnog tima moraju biti povezani sa istim projektom. 

## <a name="project-task-relationships"></a>Odnosi u okviru projektnog zadatka
Da biste osigurali uspešnu nadogradnju, sledeći odnosi moraju se pravilno održavati:

- Svi povezani zadaci moraju biti povezani sa istim projektom.
- Svaki zadatak stavke mora imati nadređeni zadatak.
- Svaki zadatak mora imati nadređeni projekat.

### <a name="valid-conditions"></a>Važeći uslovi

- Trajanje svakog zadatka mora biti duže od sat vremena ili jednako tom vremenu (>=) i kraće od 1.800.000 minuta (1250 dana).*
- Svi zadaci moraju imati datum početka koji nije pre 1.1.2000.*
- Svi zadaci moraju imati datum početka koji je najdalje 17 godina od današnjeg dana.*
- Svi zadaci moraju da imaju datum početka koji je pre datuma završetka ili isti kao taj datum.
- Sve vrste transakcija za klasifikacije (Troškovi, Materijal, Porez i Vreme) moraju imati vrednosti za stavke **Podrazumevana jedinica** i **Grupa jedinica**.
- Formate datuma sa slovima treba izbegavati.

### <a name="potential-mitigation-steps"></a>Potencijalni koraci za ublažavanje
- Koristite naprednu pretragu za identifikaciju projektnih zadataka koji ne sadrže ID projekta.
- Koristite naprednu pretragu da biste identifikovali projektne zadatke gde je zakazano trajanje duže od > 1.800.000.
- Pre nego što unesete bilo kakve promene podataka, trebalo bi da istražite sva prilagođavanja povezana sa entitetom koja su mogla dovesti do toga da se podaci dovedu u loš status. Trebalo bi da se pozabavite sa ovim prilagođavanjima pre nego što nastavite sa bilo kakvim ispravkama koje se odnose na podatke.
- Za identifikovane zadatke koji su nasleđeni, razmotrite brisanje ovih zadataka ako vam nisu potrebni ili ako bi trebalo biti povezani sa ispravnih nadređenim projektom.
- Za sve zadatke u kojima je trajanje duže od 1250 dana, razmotrite dodavanje više zadataka kako biste predstavljali ukupno trajanje, ako je dostupno.

> [!NOTE]
> Stavke zabeležene zvezdicom (\*) imaju ograničenja zbog činjenice da upravljanje odnosima sa klijentima (CRM) podržava samo 7320 proširenja ponavljanja. Ne smete da prekoračite ovo ograničenje.

## <a name="resource-assignment-relationships"></a>Odnosi između dodela resursa
Da biste osigurali uspešnu nadogradnju, sledeći odnosi moraju se pravilno održavati:

- Sve dodele resursa u strukturnoj analizi posla moraju biti povezane sa istim projektom.
- Sve dodele resursa u strukturnoj analizi posla moraju biti povezane sa članovima projektnog tima u istom projektu.

### <a name="potential-mitigation-steps"></a>Potencijalni koraci za ublažavanje
- Identifikujte sve zadatke koji spadaju van goreopisanih uslova.  
- Sve dodele resursa koje više nisu važeće bi trebalo biti obrisane.

## <a name="project-task-dependency-relationships"></a>Odnosi između zavisnih elemenata projektnog zadatka
Da biste osigurali uspešnu nadogradnju, sledeći odnosi moraju se pravilno održavati:

- Svi zavisni elementi zadatka projekta moraju biti povezani sa istim projektom.
- Zadatak ne može da ima isti zavisni element na koji se upućuje više puta.


[!INCLUDE[footer-include](../includes/footer-banner.md)]