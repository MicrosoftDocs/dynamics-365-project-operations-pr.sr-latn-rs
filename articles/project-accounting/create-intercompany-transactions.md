---
title: Kreiranje transakcija među preduzećima
description: Ova tema pruža informacije o tome kako da kreirate transakcije među preduzećima.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0e396f0d08fd166e7acd6f8ec8f32353a7679dd8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013368"
---
# <a name="create-intercompany-transactions"></a>Kreiranje transakcija među preduzećima

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Transakcije među preduzećima su transakcije radnog vremena i troškova iz projektnog ugovora koje pripadaju jednom preduzeću ili organizacionoj jedinici, dok su resursi iz projektnog ugovora deo drugog preduzeća ili organizacione jedinice.

Kada se odobri transakcija među preduzećima, kreiraju se sledeće stvarne transakcije

| **Tip transakcije** | **Primenjeni cenovnik** | **Valuta transakcije** |
| --- | --- | --- |
| Cena | Cenovnik koštanja za ugovornu jedinicu | Valuta u cenovniku |
| Nenaplaćena prodaja. Oni su kreirani samo za stvarne podatke koji su povezani sa predmetom ugovora sa tipom naplate, vremenom i materijalom. | Prodajni cenovnik ugovornog projekta | Valuta ugovora |
| Troškovi jedinice za obezbeđivanje resursa | Cenovnik koštanja za jedinicu za određivanje resursa | Valuta u cenovniku |
| Prodaja između jedinica unutar organizacije | Cenovnik koštanja za ugovornu jedinicu | Valuta u cenovniku |

**Organizaciona jedinica** pokreće cenu, troškove jedinice za određivanje resursa i određivanje cena prodajne transakcije jedinice unutar organizacije i valutu. Ovo je važno imati na umu prilikom donošenja odluke o strukturiranju preduzeća i organizacionih jedinica u vašoj implementaciji.

Kada kreirate mogućnost za poslovanje, ponudu, ugovor za projekat i evidenciju projekata, sistem proverava da li se valuta ugovorne jedinice poklapa sa računovodstvenom valutom ugovornog preduzeća. Kada nisu iste, nije moguće kreirati ove zapise. Valuta organizacione jedinice se definiše u usluzi Dynamics 365 Project Operations tako što ćete otići u **Dataverse** > **Podešavanja** > **Organizacione jedinice**. Računovodstvena valuta preduzeća se definiše u usluzi Dynamics 365 Finance tako što ćete otići u **Glavna knjiga** > **Podešavanje glavne knjige** > **Knjiga**. Valuta se sinhronizuje sa vašim Dataverse okruženjem pomoću mape dvostrukog upisivanja u knjige.

Sistem u sledećim situacijama kreira troškove jedinice za određivanje resursa i stvarne prodajne vrednosti između preduzeća:

  - Kada se jedinica za resurse razlikuje od jedinice za ugovaranje
  - Kada se preduzeće za resurse razlikuje od preduzeća za ugovaranje

Međutim, samo će transakcije koje imaju drugo preduzeće za resurse koja se razlikuje od preduzeća za ugovaranje biti prenete u Dynamics 365 Finance okruženje za dodatno računovodstvo.

Računovodstvo stvarnih podataka o projektu evidentira se u Project Operations dnevniku integracije u usluzi Finance. Sistem kreira sledeće stavke u glavnoj knjizi.

| **Tip transakcije** | **Pravno lice** | **Kreira transakciju projekta prilikom knjiženja** | **Podrazumevane vrednosti finansijskih dimenzija potiču iz** | **Podrazumevana grupa za naplatu poreza na promet i grupa za porez na promet stavki na računu** |
| --- | --- | --- | --- | --- |
| Cena | Ne dodaje se u dnevnik integracije | Nije primenjivo | Nije primenjivo | Nije primenjivo |
| Nenaplaćena prodaja | Dnevnik integracije pravnih lica koja se zadužuju | Da | Project | **Grupa za naplatu poreza na promet**: na osnovu **klijenta ugovora** <br/> **Grupa za porez na promet stavki na računu**: iz kategorije projekta trenutnog pravnog lica na stavci u glavnoj knjizi |
| Troškovi jedinice za obezbeđivanje resursa | Dnevnik integracije pravnih lica koja pozajmljuju | No | Klijent između preduzeća | **Grupa za naplatu poreza na promet**: na osnovu **klijenta između preduzeća** <br/> **Grupa za porez na promet stavki na računu**: iz kategorije projekta trenutnog pravnog lica na stavci u glavnoj knjizi |
| Prodaja između organizacija | Dnevnik integracije pravnih lica koja pozajmljuju | No | Klijent između preduzeća | **Grupa za naplatu poreza na promet**: na osnovu **klijenta između preduzeća** <br/> **Grupa za porez na promet stavki na računu**: iz kategorije projekta trenutnog pravnog lica na stavci u glavnoj knjizi |

### <a name="example-intercompany-transactions"></a>Primer: transakcije između preduzeća

Jovanka Nikolić, programerka koja je zaposlena u preduzeću GBPM evidentira 10 sati rada za USPM Adventure Works projekat, kog je odobrio projektni menadžer. Troškovi programera u preduzeću GBPM su 88 GBP na sat. GBPM će naplatiti USPM 120 USD po satu programera. USPM će klijentu Adventure Works, naplatiti 200 USD za posao koji je obavio GBPM resurs. Još informacija potražite u članku [Konfigurisanje fakturisanja između preduzeća](configure-intercompany-invoicing.md).

1. U usluzi Project Operations, idite na **Resursi**, pa sa liste izaberite **Jovanka Nikolić**. Na kartici **Planiranje**, u polju **Preduzeće** izaberite **GBPM**.
2. Idite na **Prodaja** > **Klijenti**, i izaberite **Novo** da biste kreirali novi zapis klijenta za Adventure Works.
    1. Podesite preduzeće na **USPM**.
    2. Postavite **Tip odnosa** na **Klijent**.
    3. Izaberite **Grupa klijenata 10 – domaći**.
    4. Podesite valutu na **USD**.
    5. Sačuvajte zapis.
3. Idite na **Prodaja** > **Ugovori o projektu** i kreirajte novi projektni ugovor za preduzeće Adventure Works.
    1. Podesite kompaniju-vlasnika na **USPM**, a ugovornu jedinicu na **Contoso Robotics US**.
    2. Izaberite Adventure Works kao klijenta.
    3. Izaberite cenovnik proizvoda i sačuvajte zapis.
    4. Na kartici **Predmeti ugovora** kreirajte novi predmet ugovora. Podesite bilo koje ime i izaberite **Vreme i materijali** kao način naplate.
    5. Kreirajte novi projekat i povežite ga sa ovim predmetom ugovora.
4. Prijavite se kao resurs, **Jovanka Nikolić**. Idite na **Projekti** > **Stavke vremena**, i kreirajte stavku vremena za Adventure Works projekat.
5. Prijavite se kao menadžer projekta. Idite na **Projekti** > **Odobrenja** i odobrite transakciju stavke vremena koju je evidentirala Jovanka Nikolić.
6. Idite do projekta Adventure Works i izaberite **Srodno** > **Stvarni podaci**. Kreiraju se sledeće transakcije stvarnih podataka.

| **Tip transakcije** | **Cena** | **Valuta transakcije** | **Iznos** |
| --- | --- | --- | --- |
| Cena | 120 | USD | 1200 |
| Nenaplaćena prodaja | 200 | USD | 2000 |
| Troškovi jedinice za obezbeđivanje resursa | 88 | GBP | 880 |
| Prodaja između organizacionih jedinica | 120 | USD | 1200 |

7. Prijavite se kao računovođa preduzeća USPM. Otvorite instancu Finance usluge Project Operations i izaberite preduzeće **USPM**. 
8. Idite na **Upravljanje projektima i računovodstvo** > **Periodično** > **Project Operations u usluzi Customer Engagement** > **Uvoz iz pripreme** i izaberite da pokrenete periodični proces. Ovaj periodični proces će se popuniti u Project Operations dnevniku integracije.
9. Idite na **Upravljanje projektima i računovodstvo** > **Dnevnici** > **Project Operations dnevnik integracije** i pregledajte stavke u glavnoj knjizi. Sistem kreira sledeću stavku.

    | **Tip transakcije** | **Cena** | **Valuta transakcije** | **Iznos** |
    | --- | --- | --- | --- |
    | Nenaplaćena prodaja | 200 | USD | 2000 |

    Ako je sistem podešen za ostvarivanje prihoda za ovaj projekat, objavljuje se sledeće:

    - Zaduženje: projekat – WIP prodajna vrednost 200 USD
    - Odobrenje: projekat – ostvareni prihod 200 USD

    Ova nefakturisana prodaja je sada spremna za fakturisanje. Faktura za klijenta Adventure Works može biti finansijski objavljena kada je to potrebno.

10. Prijavite se kao računovođa preduzeća **GBPM**. Otvorite instancu Finance usluge Project Operations i otvorite preduzeće, **GBPM**. 
11. Idite na **Upravljanje projektima i računovodstvo** > **Periodično** > **Integracija projektnih operacija** > **Uvoz iz pripremne tabele** i pokrenite periodični postupak za popunjavanje dnevnika Project Operations integracije.
12. Idite na **Upravljanje projektima i računovodstvo** > **Dnevnici** > **Project Operations dnevnik integracije** i pregledajte stavke. Sistem kreira sledeće stavke.

    | **Tip transakcije** | **Cena** | **Valuta transakcije** | **Iznos** |
    | --- | --- | --- | --- |
    | Troškovi jedinice za obezbeđivanje resursa | 88 | GBP | 880 |
    | Prodaja između organizacionih jedinica | 120 | USD | 1200 |

    Objavljivanje ovih zapisa rezultiraće sledećim transakcijama vaučera:

    - Zaduženje: trošak projekta gbp
    - Odobrenje: raspodela zarada 88 GBP

    Ako je sistem podešen za ostvarivanje prihoda između preduzeća, objavljuje se sledeće:

    - Zaduženje: projekat – WIP prodajna vrednost 120 USD
    - Odobrenje: projekat – ostvareni prihod 120 USD

    Sistem je sada spreman da kreira internu fakturu klijentu između preduzeća.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
