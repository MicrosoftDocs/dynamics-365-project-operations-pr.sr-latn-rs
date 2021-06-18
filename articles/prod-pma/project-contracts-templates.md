---
title: Sinhronizovanje projektnih ugovora i projekata direktno iz usluge Project Service Automation sa uslugom Finance
description: Ova tema opisuje predložak i osnovne zadatke koji se koriste za sinhronizaciju ugovora o projektu i projekta direktno iz usluge Microsoft Dynamics 365 Project Service Automation u Dynamics 365 Finance.
author: Yowelle
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 2f5fa0143c903f08b3937426805cb43d5d6109e3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999823"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance"></a>Sinhronizovanje projektnih ugovora i projekata direktno iz usluge Project Service Automation sa uslugom Finance 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Ova tema opisuje predložak i osnovne zadatke koji se koriste za sinhronizaciju ugovora o projektu i projekta direktno iz usluge Dynamics 365 Project Service Automation u Dynamics 365 Finance.

> [!NOTE] 
> Ako koristite Enterprise Edition 7.3.0, morate instalirati KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Tok podataka iz usluge Project Service Automation u Finance

> [!NOTE]
> Pre nego što budete mogli da koristite rešenje za integraciju usluge Project Service Automation sa uslugom Finance, trebalo bi da ste upoznati sa funkcijom integracije podataka u sistemu Dynamics 365.

Rešenje za integraciju iz usluge Project Service Automation u Finance koristi funkciju integracije podataka za sinhronizaciju podataka u svim instancama usluga Project Service Automation i Finance. Predložak integracije koji je dostupan sa funkcijom Integracija podataka omogućava tok podataka o ugovorima za projekte, projekte, predmete ugovora o projektu i kontrolne tačke predmeta ugovora o projektu iz usluge Project Service Automation u Finance.

Sledeća ilustracija prikazuje kako se podaci sinhronizuju između usluga Project Service Automation i Finance.

[![Tok podataka za integraciju usluge Project Service Automation sa uslugom Finance](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Predlošci i zadaci

Da biste pristupili dostupnim predlošcima, u Microsoft Power Apps centru administracije izaberite **Projekti**, a zatim u gornjem desnom uglu izaberite **Novi projekat** za izbor javnih predložaka.

Sledeći predlošci i osnovni zadaci koji se koriste za sinhronizaciju ugovora o projektu i projekata iz usluge Project Service Automation u Finance:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Integrisanje sa uslugom Dynamics 365 Project Service Automation verzije 2.x
- **Naziv predloška u integraciji podataka:** Projekti i ugovori (Project Service Automation u Finance)
- **Naziv zadataka u projektu:**

    - Ugovori za projekat: Project Service Automation u Finance
    - Projekti: Project Service Automation u Finance
    - Predmeti ugovora za projekat: Project Service Automation u Finance
    - Kontrolne tačke predmeta ugovora za projekat: Project Service Automation u Finance
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Integrisanje sa uslugom Dynamics 365 Project Service Automation verzije 3.x
Došlo je do promene šeme u usluzi Project Service Automation koja utiče na predložak kontrolne tačke predmeta ugovora o projektu, a za integraciju usluge Project Service Automation verzije 3.x sa sistemom Dynamics 365 potrebno je da koristite predložak verzije 2.

- **Naziv predloška u integraciji podataka:** Projekti i ugovori (Project Service Automation 3.x u Finance), v2
- **Naziv zadataka u projektu:**

    - Ugovori za projekat: Project Service Automation u Finance
    - Projekti: Project Service Automation u Finance
    - Predmeti ugovora za projekat: Project Service Automation u Finance
    - Kontrolne tačke predmeta ugovora za projekat: Project Service Automation u Finance

Da bi moglo da dođe do sinhronizacije ugovora o projektu i projekata, morate sinhronizovati naloge.

## <a name="entity-set"></a>Skup entiteta

| Project Service Automation       | Finance                                                |
|----------------------------------|--------------------------------------------------------|
| Porudžbine                           | Entitet integracije za ugovor o projektu                |
| Projekti                         | Entitet integracije za projekat                         |
| Stavke porudžbine                      | Entitet integracije za predmet ugovora o projektu           |
| Kontrolne tačke predmeta ugovora o projektu | Entitet integracije za kontrolnu tačku predmeta ugovora o projektu |

## <a name="entity-flow"></a>Tok entiteta

Ugovorima o projektu se upravlja u usluzi Project Service Automation i oni se sinhronizuju sa uslugom Finance kao ugovori o projektu. Kao deo predloška za integraciju, možete da postavite izvor integracije u usluzi Finance za ugovor o projektu.

Vremenom i materijalom i projektima sa fiksnom cenom upravlja se u usluzi Project Service Automation i sinhronizuju sa uslugom Finance kao projekti. Kao deo integracije predloška, možete da podesite izvor integracije za projekat u usluzi Finance. Trenutno su podržani samo vreme, materijal i projekti sa fiksnom cenom.


Predmetima ugovora o projektu se upravlja u usluzi Project Service Automation i oni se sinhronizuju sa uslugom Finance kao pravilima naplate po ugovoru o projektu. Ako se način naplate razlikuje od podrazumevanog tipa projekta, sinhronizacija ažurira tip projekta za projekat predmeta ugovora i grupu projekata.

Kontrolnim tačkama predmeta ugovora o projektu se upravlja u usluzi Project Service Automation i oni se sinhronizuju sa uslugom Finance kao kontrolne tačke pravila naplate po ugovoru o projektu.

## <a name="project-service-automation-to-finance-integration-solution"></a>Rešenje za integraciju usluge Project Service Automation sa uslugom Finance

Polje **ID ugovora o projektu** je dostupno na stranici **Ugovori o projektu**. Ovo polje je učinjeno prirodnim i jedinstvenim ključem za podršku integraciji.

Kada se kreira novi ugovor o projektu, ako vrednost **ID ugovora o projektu** već ne postoji, ona se automatski generiše pomoću niza brojeva. Vrednost se sastoji od reči **ORD** praćene rastućim nizom brojeva, a zatim sufiksom od šest znakova. Evo primera: **ORD-01022-Z4M9Q0**.

Polje **Broj projekta** je dostupno na stranici **Projekti**. Ovo polje je učinjeno prirodnim i jedinstvenim ključem za podršku integraciji.

Kada se kreira novi projekat, ako vrednost **Broj projekta** već ne postoji, ona se automatski generiše pomoću niza brojeva. Vrednost se sastoji od reči **PRJ** praćene rastućim nizom brojeva, a zatim sufiksom od šest znakova. Evo primera: **PRJ-01049-CCNID0**.

Kada se primeni rešenje integracije usluge Project Service Automation sa Finance, skripta za nadogradnju postavlja polje **ID ugovora o projektu** za postojeće ugovore o projektu i polje **Broj projekta** za postojeće projekte u usluzi Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Preduslovi i podešavanje mapiranja

- Da bi moglo da dođe do sinhronizacije ugovora o projektu i projekata, morate sinhronizovati naloge.
- U svom skupu veza dodajte mapiranje polja ključa za integraciju za **msdyn\_organizationalunits** u **msdyn\_name \[Name\]**. Možda ćete prvo morati da dodate projekat u skup veza. Za više informacija, pogledajte [Integrisanje podataka u Common Data Service za aplikacije](/powerapps/administrator/data-integrator).
- U svom skupu veza, dodajte mapiranje polja ključa za integraciju za **msdyn\_projects** u **msdynce\_projectnumber \[Project Number\]**. Možda ćete prvo morati da dodate projekat u skup veza. Za više informacija, pogledajte [Integrisanje podataka u Common Data Service za aplikacije](/powerapps/administrator/data-integrator).
- **SourceDataID** za ugovore o projektu i projekte mogu se ažurirati na drugu vrednost ili ukloniti iz mapiranja. Podrazumevana vrednost predloška je **Project Service Automation**.
- Mapiranje **Uslovi plaćanja** se mora ažurirati tako da odražava važeće uslove plaćanja u usluzi Finance. Takođe možete da uklonite mapiranje iz projektnog zadatka. Mapa podrazumevanih vrednosti ima podrazumevane vrednosti za demo podatke. Sledeća tabela prikazuje vrednosti u usluzi Project Service Automation.

    | Vrednost | Opis   |
    |-------|---------------|
    | 1     | Neto 30        |
    | 2     | 2% 10, neto 30 |
    | 3     | Neto 45        |
    | 4     | Neto 60        |

## <a name="power-query"></a>Power Query

Koristite Microsoft Power Query for Excel za filtriranje podataka ako su ispunjeni sledeći uslovi:

- Imate ulazne porudžbine u usluzi Dynamics 365 Sales.
- Imate više organizacionih jedinica u usluzi Project Service Automation i te organizacione jedinice biće mapirane u više pravnih lica u usluzi Finance.

Ako morate da koristite Power Query, sledite ove smernice:

- Predložak Projekti i ugovori (iz PSA u Fin and Ops) ima podrazumevani filter koji uključuje samo ulazne porudžbine tipa **Radni predmet (msdyn\_ordertype = 192350001)**. Ovaj filter vam garantuje da se ugovori o projektu neće kreirati za ulazne porudžbine u usluzi Finance. Ako kreirate sopstveni obrazac, morate dodati ovaj filter.
- Napravite Power Query filter koji uključuje samo ugovorne organizacije koje treba sinhronizovati sa pravnim licem skupa integracionih veza. Na primer, projektni ugovori koje imate sa organizacionom jedinicom ugovora Contoso US bi trebalo da se sinhronizuju sa pravnim licem USSI, ali projektni ugovori koje imate sa organizacionom jedinicom ugovora Contoso Global treba sinhronizovati sa pravnim licem USMF. Ako ne dodate ovaj filter u mapiranje zadataka, svi ugovori o projektu biće sinhronizovani sa pravnim licem koje je definisano za skup veza, bez obzira na organizacionu jedinicu ugovora.

## <a name="template-mapping-in-data-integration"></a>Mapiranje predložaka u usluzi Data Integration

> [!NOTE] 
> Polja **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** i **AddressZipCode** nisu uključena u podrazumevano mapiranje za ugovore o projektu. Mapiranja možete dodati ako želite da se ovi podaci sinhronizuju za ugovore o projektu.
>
> Polja **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** i **ProjectType** nisu uključena u podrazumevano mapiranje za projekte. Mapiranja možete dodati ako želite da se ovi podaci sinhronizuju za projekte.

Sledeće ilustracije prikazuju primere mapiranja zadataka predloška u usluzi Data Integration. Mapiranje prikazuje informacije o terenu koje će se sinhronizovati iz usluge Project Service Automation u Finance.

[![Mapiranje predloška projektnog ugovora](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Mapiranje predloška projekta](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Mapiranje predloška predmeta ugovora](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Mapiranje predloška kontrolne tačke predmeta ugovora](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Mapiranje kontrolnih tačaka predmeta ugovora o projektu u projektima i ugovorima (iz PSA 3.x u Dynamics) – predložak verzije 2:

[![Mapiranje kontrolne tačke predmeta ugovora sa predloškom verzije dva](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]