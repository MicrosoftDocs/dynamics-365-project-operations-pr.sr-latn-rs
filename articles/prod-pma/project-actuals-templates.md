---
title: Sinhronizacija stvarnih vrednosti projektu direktno iz usluge Project Service Automation sa dnevnikom integracije projekta za knjiženje u usluzi Finance and Operations
description: Ova tema opisuje predloške i osnovne zadatke koji se koriste za sinhronizaciju stvarnih vrednosti projekta direktno iz usluge Microsoft Dynamics 365 Project Service Automation u Finance and Operations.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 11ccbd64c37341b2969e10e9a737f1aa4b4a61f9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289701"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Sinhronizacija stvarnih vrednosti projektu direktno iz usluge Project Service Automation sa dnevnikom integracije projekta za knjiženje u usluzi Finance and Operations

[!include[banner](../includes/banner.md)]

Ova tema opisuje predloške i osnovne zadatke koji se koriste za sinhronizaciju stvarnih vrednosti projekta direktno iz usluge Dynamics 365 Project Service Automation u Dynamics 365 Finance.

Predložak sinhronizuje transakcije iz usluge Project Service Automation u pripremnu tabelu u usluzi Finance. Po završetku sinhronizacije, **morate** da uvezete podatke iz pripremne tabele u dnevnik integracije.

> [!NOTE]
> - Integracija trenutnog stanja projekta dostupna je počev od verzije 8.0.1.
> - Ako koristite Enterprise Edition 7.3.0 kada instalirate KB 4132657 i KB 4132660, moći ćete da koristite predloške za integrisanje projektnih zadataka, kategorije transakcija troškova, procene sati, procene troškova i stvarnih podataka, kao i da konfigurišite zaključavanje funkcionalnosti. Ako morate da resetujete računovodstvene distribucije, preporučujemo da instalirate i KB 4131710.
> - Ako koristite verziju 7.3.0, a transakcije naknada prenosite iz usluge Project Service Automation, morate instalirati KB 4345320 da biste te naknade uključili u fakturu projekta.
> - Ako unosite iznose poreza na promet za transakcije vremena ili troškova u Project Service Automation, morate instalirati Project Service Automation sa ispravkom 7. U suprotnom, trenutno stanje poreza neće biti povezano sa povezanim činjenicama o vremenu ili trenutnim troškovima i neće biti sinhronizovano sa uslugom Finance. Za više informacija kontaktirajte tehničku podršku.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Tok podataka iz usluge Project Service Automation u Finance

Rešenje za integraciju iz usluge Project Service Automation u Finance koristi funkciju integracije podataka za sinhronizaciju podataka u svim instancama usluga Project Service Automation i Finance. Predlošci za integraciju koji su dostupni sa funkcijom Integracija podataka omogućavaju tok podataka o trenutnom stanju projekta iz usluge Project Service Automation u Finance.

Sledeća ilustracija prikazuje kako se podaci sinhronizuju između usluga Project Service Automation i Finance.

[![Tok podataka za integraciju usluge Project Service Automation sa uslugom Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Stvarne vrednosti projekta iz usluge Project Service Automation

### <a name="template-and-tasks"></a>Predlošci i zadaci

Da biste pristupili dostupnim predlošcima, u Microsoft Power Apps centru administracije izaberite **Projekti**, a zatim u gornjem desnom uglu izaberite **Novi projekat** za izbor javnih predložaka.

Sledeći predložak i osnovni zadaci koji se koriste za sinhronizaciju stvarnih vrednosti projekta iz usluge Project Service Automation u Finance:

- **Naziv predloška u Integraciji podataka:** Stvarne vrednosti projekta (iz PSA u Fin and Ops)
- **Naziv zadataka u projektu:**

    - Stvarne vrednosti
    - TransactionConnections

### <a name="entity-set"></a>Skup entiteta

| Project Service Automation | Finance                                   |
|----------------------------|----------------------------------------------------------|
| Stvarne vrednosti                    | Entitet integracije za stvarne vrednosti projekta                   |
| Veze transakcija    | Entitet integracije za odnose transakcija projekta |

### <a name="entity-flow"></a>Tok entiteta

Stvarnim vrednostima projekta se upravlja u usluzi Project Service Automation i oni se sinhronizuju sa dnevnikom integracije projekta u usluzi Finance. Računovodstvo će se primenjivati na osnovu zadatih finansijskih aspekata i postavke knjiženja.

### <a name="prerequisites"></a>Preduslovi

Da bi moglo doći do sinhronizacije stvarnih vrednosti, morate konfigurisati parametre integracije usluge Project Service Automation i sinhronizovati projekte, projektne zadatke i kategorije transakcija troškova projekta.

### <a name="power-query"></a>Power Query

U predlošku stvarnih vrednosti projekta, morate da koristite Microsoft Power Query za Excel da biste izvršili ove zadatke:

- Transformišite vrstu transakcije u usluzi Project Service Automation u ispravnu vrstu transakcije u usluzi Finance. Ova transformacija je već definisana u predlošku stvarnih vrednosti projekta (iz PSA u Fin and Ops).
- Transformišite tip naplate u usluzi Project Service Automation u ispravan tip naplate u usluzi Finance. Ova transformacija je već definisana u predlošku stvarnih vrednosti projekta (iz PSA u Fin and Ops). Tip naplate se zatim mapira na svojstvo reda, zasnovano na konfiguraciji na stranici **Parametri integracije usluge Project Service Automation**.
- Filtrirajte do određenih organizacionih jedinica resursa koje moraju biti sinhronizovane sa ovim predloškom.
- Ako će međukompanijsko vreme ili stvarne vrednosti međukompanijskih troškova biti sinhronizovani sa uslugom Finance, morate da transformišete organizacionu jedinicu ugovora u ispravno pravno lice u usluzi Finance. U predlošku stvarnih vrednosti projekta (iz PSA u Fin and Ops), uslovna kolona je definisana na osnovu demo podataka. Morate ažurirati poslednju umetnutu uslovnu kolonu na tačna pravna lica. U suprotnom, može doći do greške integracije ili se u Finance mogu uvesti transakcije netačnih stvarnih vrednosti.
- Ako se međukompanijsko vreme ili stvarne vrednosti međukompanijskih troškova neće sinhronizovati sa uslugom Finance, morate da izbrišete poslednju umetnutu uslovnu kolonu iz predloška. U suprotnom, može doći do greške integracije ili se u Finance mogu uvesti transakcije netačnih stvarnih vrednosti.

#### <a name="contract-organizational-unit"></a>Organizaciona jedinica ugovora
Da biste ažurirali umetnutu uslovnu kolonu u predlošku, kliknite na strelicu **Mapa** da biste otvorili mapiranje. Izaberite vezu **Napredni upit i filtriranje** da biste otvorili Power Query.

- Ako koristite podrazumevani predložak stvarnih vrednosti projekta (iz PSA u Fin and Ops), u usluzi Power Query izaberite poslednji **Umetnuti uslov** u odeljku **Primenjeni koraci**. U stavci **Funkcija**, zamenite **USSI** nazivom pravnog lica koje treba koristiti sa integracijom. Dodajte dodatne uslove u stavku **Funkcija** po vašem zahtevu i ažurirajte uslov **else** iz **USMF** u ispravno pravno lice.
- Ako kreirate novi predložak, morate dodati kolonu kako biste podržali međukompanijsko vreme i troškove. Izaberite **Dodaj uslovnu kolonu** i unesite naziv za novu kolonu, kao što je **LegalEntity**. Unesite uslov za kolonu, gde, ako **msdyn\_contractorganizationalunitid.msdyn\_ime** glasi \<organizational unit\>, onda \<enter the legal entity\>; u suprotnom je bez vrednosti.

### <a name="template-mapping-in-data-integration"></a>Mapiranje predložaka u usluzi Data Integration

Sledeće ilustracije prikazuju primer mapiranja zadataka predloška u usluzi Data Integration. Mapiranje prikazuje informacije o terenu koje će se sinhronizovati iz usluge Project Service Automation u Finance.

[![Mapiranje predložaka - stvarni troškovi](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Mapiranje šablona - Transakcione veze](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Uvoz iz pripremne tabele nakon integracije iz usluge Project Service Automation

Periodični proces uvoza iz pripremne tabele mora se pokrenuti nakon sinhronizacije stvarnih podataka iz usluge Project Service Automation u Finance. Ovaj proces će uvoziti projektne transakcije iz pripremne tabele u dnevnik Project Service Automation integracije, gde se primenjuje računovodstvo i uvezene transakcije se mogu knjižiti. Preporučujemo vam da ovaj postupak pokrenete u paketnom režimu; po želji se može podesiti da se pokreće kao periodični paket.

## <a name="update-actuals-from-finance"></a>Ažuriranje stvarnih vrednosti iz usluge Finance

### <a name="template-and-tasks"></a>Predlošci i zadaci

Sledeći predložak i osnovni zadaci se koriste za sinhronizaciju broja vaučera i poreza na promet za objavljene projektne transakcije iz usluge Finance u Project Service Automation:

- **Naziv predloška u usluzi Data integration:** Ažuriranje stvarnih vrednosti projekta (iz Fin and Ops u PSA)
- **Naziv zadataka u projektu:**

    - Stvarne vrednosti 
    - TransactionConnections

### <a name="entity-set"></a>Skup entiteta

| Finance                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Entitet integracije za stvarne vrednosti projekta                   | Stvarne vrednosti                    |
| Entitet integracije za odnose transakcija projekta | Veze transakcija    |

### <a name="entity-flow"></a>Tok entiteta

Stvarnim vrednostima projekta se upravlja u usluzi Project Service Automation i oni se sinhronizuju sa dnevnikom integracije projekta u usluzi Finance. Kada se stvarne vrednosti proknjiže u usluzi Finance, one će se ažurirati u usluzi Project Service Automation brojem vaučera iz usluge Finance. Ako su porezi na promet dodati u Finance, nove stvarne vrednosti poreza kreiraju se u usluzi Project Service Automation.

### <a name="power-query"></a>Power Query

U predlošku za ažuriranje stvarnih vrednosti projekta, morate da koristite Power Query za Excel da biste izvršili ove zadatke:

- Transformišite vrstu transakcije u usluzi Finance u ispravnu vrstu transakcije u usluzi Project Service Automation. Ova transformacija je već definisana u predlošku za ažuriranje stvarnih vrednosti projekta (iz Fin and Ops u PSA).
- Transformišite tip naplate u usluzi Finance u ispravan tip naplate u usluzi Project Service Automation. Ova transformacija je već definisana u predlošku za ažuriranje stvarnih vrednosti projekta (iz Fin and Ops u PSA).

### <a name="template-mapping-in-data-integration"></a>Mapiranje predložaka u usluzi Data Integration

Sledeće ilustracije prikazuju primere mapiranja zadataka predloška u usluzi Data Integration. Mapiranje prikazuje informacije o polju koje će se sinhronizovati iz usluge Finance u Project Service Automation.

[![Mapiranje predložaka - ažuriranje stvarnih troškova](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Mapiranje predložaka - ažuriranje transakcija](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]