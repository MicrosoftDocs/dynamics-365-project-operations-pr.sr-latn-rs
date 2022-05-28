---
title: Integracija upravljanja troškovima
description: Ova tema pruža informacije o integraciji upravljanja troškovima u Project Operations pomoću dvostrukog upisivanja.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b41be519dbfa89668712bc28ccb1888cd08c38a2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585809"
---
# <a name="expense-management-integration"></a>Integracija upravljanja troškovima

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ova tema pruža informacije o integraciji upravljanja izveštajima u Project Operations [punoj primeni troškova](../expense/expense-overview.md) pomoću dvostrukog upisivanja.

## <a name="expense-categories"></a>Kategorije troškova

U potpunom raspoređivanju troškova kategorije troškova se kreiraju i održavaju u aplikacijama "Finansije i operacije". Da biste kreirali novu kategoriju troškova, izvršite sledeće korake:

1. U Microsoft Dataverse kreirajte kategoriju **Transakcija**. Integracija sa dva pisanja će sinhronizovati ovu kategoriju transakcije sa aplikacijama za finansije i operacije. Za više informacija pogledajte [Konfigurišite kategorije projekata](/dynamics365/project-operations/project-accounting/configure-project-categories) i [Integracija podataka za podešavanje i konfiguraciju usluge Project Operations](resource-dual-write-setup-integration.md). Kao rezultat ove integracije, sistem kreira četiri deljena zapisa kategorije u aplikacijama za finansije i operacije.
2. U Finance idite na **Upravljanje troškovima** > **Podesi** > **Deljene kategorije** i izaberite zajedničku kategoriju sa klasom transakcije **Trošak**. Podesite parametar **Može se koristiti u troškovima** na **Tačno** i definišite vrstu troškova koje ćete koristiti.
3. Koristeći ovaj deljeni zapis o kategoriji, kreirajte novu kategoriju troškova odlaskom na **Upravljanje troškovima** > **Podesi** > **Kategorije troškova** i odaberite **Novo**. Kada je zapis sačuvan, dvostruko upisivanje koristi mapu tabele, **Entitet izvoza kategorija projektnih troškova Project Operations integracije (msdyn\_expensecategories)** za sinhronizaciju ovog zapisa sa Dataverse.

  ![Integracija kategorija troškova.](./media/DW6ExpenseCategories.png)

Kategorije troškova u aplikacijama za finansije i operacije su specifične za preduzeće ili pravno lice. Postoje zasebne, odgovarajuće evidencije specifične za pravno lice u Dataverse. Kada menadžer projekta proceni troškove, ne može da odabere kategorije troškova stvorene za projekat koji je u vlasništvu druge kompanije od kompanije koja je vlasnik projekta na kojem rade. 

## <a name="expense-reports"></a>Izveštaji o troškovima

Izveštaji o troškovima se kreiraju i odobravaju u aplikacijama "Finansije i operacije". Za više informacija pogledajte [Kreirajte i obradite izveštaje o troškovima u Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/). Nakon što menadžer projekta odobri izveštaj o troškovima, on se knjiži u glavnoj knjizi. U Project Operations, redovi izveštaja o troškovima u vezi sa projektom objavljuju se koristeći posebna pravila knjiženja:

  - Troškovi povezani sa projektom (uključujući nepovratni porez) ne knjiže se odmah na račun troškova projekta u glavnoj knjizi, već se knjiže na račun integracije troškova. Nalog konfigurisan u **Upravljanje projektima i računovodstvo** > **Podešavanje** > **Parametri upravljanja projektom i računovodstveni parametri**, kartica **Project Operations u usluzi Dynamics 365 Customer Engagement**.
  - Dvostruko pisanje se sinhronizuje sa Dataverse koristeći **Project Operations entitet izvoza troškova integracije projekta (msdyn\_expenses)** mapu tabela.
  - Pomoćna knjiga poreza, pomoćna knjiga dobavljača i druga finansijska knjiženja evidentiraju se prema potrebi u vreme knjiženja izveštaja o troškovima.

  ![Integracija izveštaja o troškovima.](./media/DW6ExpenseReports.png)

Kada se zapis upiše u entitet **Trošak** u Dataverse, sistem pokreće automatski postupak odobravanja zapisa. Ako je potrebno, status automatskog postupka odobravanja može se pregledati u Dataverse odlaskom u **Napredna podešavanja** > **Sistem** > **Sistemski poslovi**. Nakon završetka odobrenja, u klasi se kreiraju zapisi klase transakcija troškova entiteta **Stvarni podaci**.

Stvarni podaci povezani sa troškovima se zatim obrađuju pomoću mape tabela dvostrukog pisanja **Project Operations stvarne vrednosti integracije (msdyn\_actuals)**. Više informacija potražite u članku [Procene i stvarne vrednosti](resource-dual-write-estimates-actuals.md).

Periodični proces, **Uvoz iz pripreme** kreira stavke u glavnoj knjizi koje se odnose na izveštaj o troškovima u dnevniku Project Operations integracije. Račun za prebijanje dugovanja podrazumevano je račun za integraciju troškova. Dnevnik integracije knjiženja briše stanje računa za transakciju troškova i premešta iznos troškova na račun troškova projekta. Sistem takođe kreira projektne hipoteke za dalje fakturisanje i priznavanje prihoda.
