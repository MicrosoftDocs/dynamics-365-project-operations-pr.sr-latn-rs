---
title: Podesite stope naplate za rad
description: Ova tema pruža informacije o tome kako postaviti stope naplate za rad u usluzi Project Operations.
author: rumant
manager: Annbe
ms.date: 10/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 501458510efca6434a51577aacd1f09d1a4faa25
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180727"
---
# <a name="set-up-labor-bill-rates"></a>Podesite stope naplate za rad

**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha

Svaki cenovnik ima skup cena uloga ili stopa rada koje stupaju na snagu za kontekst i efektivnost datuma navedenih u zaglavlju cenovnika. Stope naplate za vreme u usluzi Dynamics 365 Project Operations mogu se postaviti u samo jednoj valuti, koja je valuta u zaglavlju cenovnika.

1. Da biste postavili stope naplate za rad za prodajni cenovnik, napravite cenovnik na osnovu zaglavlja cenovnika. 
2. Na kartici **Uloga cena**, u podmreži odaberite **+ Nova cena uloge**. 
3. U oknu **Brzo kreiranje** unesite kombinaciju uloge i organizacione jedinice za koju treba da podesite stopu naplate.

   Sledeća tabela uključuje polja na kartici **Opšti podaci** i oknu **Brzo kreiranje** linije cena za ulogu koju treba imati na umu dok kreirate cene uloga na prodajnom cenovniku:

    | Polje | Lokacija | Opis | Posledični uticaj |
    | --- | --- | --- | --- |
    | Uloga | Kartica **Opšti podaci** i okno **Brzo kreiranje** | Izaberite ulogu za koju postavljate stopu naplate. | Uloga na dolaznoj proceni ili trenutnom stanju će se podudarati sa ovom linijom kako bi se zadala stopa naplate uloge. |
    | Preduzeće koje određuje resurse | Kartica **Opšti podaci** i okno **Brzo kreiranje** | Izaberite kompaniju ili pravno lice od kojeg potiče uloga. Na primer, programer iz kompanije Fabrikam India ili programer iz kompanije Fabrikam USA. | Preduzeće koje određuje resurse na dolaznoj proceni ili trenutnom stanju će se podudarati sa ovom linijom kako bi se zadala stopa naplate uloge. |
    | Jedinica za određivanje resursa | Kartica **Opšti podaci** i okno **Brzo kreiranje** | Izaberite organizacionu jedinicu ili odeljenje kompanije odakle potiče uloga. Na primer, programer iz odeljenja za robotiku kompanije Fabrikam Indija ili programer iz odeljenja softvera kompanije Fabrikam SAD. | Jedinica koja određuje resurse na dolaznoj proceni ili trenutnom stanju će se podudarati sa ovom linijom kako bi se zadala stopa naplate uloge. |
    | Cena | Kartica **Opšti podaci** i okno **Brzo kreiranje** | Postavite stopu naplate za ulogu, preduzeće koje određuje resurse i kombinaciju jedinica za obezbeđivanje resursa. Na primer, programer iz kompanije Fabrikam India ima stopu naplate 100 USD ili programer kompanije Fabrikam USA ima stopu naplate 150 USD. | Ova cena je podrazumevana stopa naplate za cenu po jedinici dolazne procene ili stvarne linije za klasu transakcije vreme. |
    | Valuta | Kartica **Opšti podaci** i okno **Brzo kreiranje**| Vrednost valute podrazumevano potiče iz valute iz zaglavlja cenovnika prodaje. Na prodajnom cenovniku, valuta se ne može zameniti. | Ova valuta je podrazumevana valute za cenu po jedinici dolazne stvarne prodaje za klasu transakcije Vreme. |
    | Raspored jedinica | Kartica **Opšti podaci** i okno **Brzo kreiranje** | Raspored jedinica podrazumevano ima vrednost Vreme i ne može se promeniti u entitetu cene uloga jer se koristi ekspresna stopa po jedinicama vremena. | Nema posledičnog uticaja za ovo polje. |
    | Jedinica | Kartica **Opšti podaci** i okno **Brzo kreiranje** | Jedinična vrednost podrazumevano potiče iz polja **Jedinica vremena** u zaglavlju cenovnika prodaje. Ali, vrednost se može zameniti. Na primer, programer iz kompanije Fabrikam India ima stopu naplate 1000 USD po **danu u Indiji**. Programer iz kompanije Fabrikam USA ima stopu naplate od 1500 USD po **danu u SAD**. | Kada se jedinična cena podrazumeva iz dolazne procene ili stvarne linije, sistem koristi sistem jedinica i konverziju u osnovne jedinice za izračunavanje jedinične cene. Na primer, procena je za posao od 10 **dana u Indiji** za programera iz Indije, a jedinica, dan u Indiji se definiše kao 10 sati. Kada određuje cenu te linije procene, aplikacija izračunava jediničnu cenu na proceni kao 1000 USD/10 sati = 100 USD na sat. |

## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Prenesite cene ili postavite stope naplate za resurse iz drugih organizacionih jedinica ili odeljenja 

Projektne kompanije često koriste zaposlene iz različitih pravnih lica i različitih odeljenja unutar pravnog lica za rad na projektima. Projekte može izvršiti jedno pravno lice ili odeljenje, ali zaposleni ili konsultanti koji rade na projektima mogu poticati iz istog pravnog lica i odeljenja ili iz nekog drugog. Projekat bi takođe mogao da se sastoji od kombinacije ljudi iz različitih pravnih lica i odeljenja. U programu Project Operations pravno lice koje je vlasnik projekta je **Preduzeće-vlasnik**, a odeljenje koje je vlasnik isporuke je **Jedinica ugovaranja**. Sva ostala pravna lica koja pružaju resurse su **Preduzeća koja određuju resurse**, a odeljenja koja pružaju resurse su **Jedinice za određivanje resursa**. Zbog razlika u troškovima radne snage u različitim geografskim područjima i na tržištima rada širom sveta, stope naplate za rad takođe su različito postavljene za različite geografske regije.

Na primer, programeru iz odeljenja za robotiku kompanije Fabrikam India, koji radi na američkom projektu, naplaćuje se stopa od 100 USD na sat. Programeru iz odeljenja za robotiku kompanije Fabrikam US, koji radi na američkom projektu, naplaćuje se stopa od 150 USD na sat. 

### <a name="example-set-up-a-bill-rate"></a>Primer: Podesite stopu naplate 

1. Kreirajte prodajni cenovnik pod nazivom *Fabrikam US stope naplate* i odredite datum stupanja na snagu.
2. U prodajni cenovnik unesite sledeće informacije o ceni:

    | Uloga | Preduzeće koje obezbeđuje resurse | Jedinica za određivanje resursa | Stopa naplate |
    | --- | --- | --- | --- |
    | Projektant | Fabrikam India | Fabrikam India - Robotics | $100 |
    | Projektant | Fabrikam Philippines | Fabrikam Philippines - Robotics | 90 USD |
    | Projektant | Fabrikam US | Fabrikam US - Robotics | 150 USD |

3. Priložite prodajni cenovnik, **Fabrikam US stope naplate** projektnom cenovniku projektnog ugovora ili na određeni nalog.
