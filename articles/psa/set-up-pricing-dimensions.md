---
title: Podešavanje prilagođenih polja kao dimenzija za određivanje cena
description: Ova tema pruža informacije o podešavanju prilagođenih dimenzija za određivanje cena.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: cce3a3fe6aef247380f6284f58d49337f969c38c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008328"
---
# <a name="setting-up-custom-fields-as-pricing-dimensions"></a>Podešavanje prilagođenih polja kao dimenzija za određivanje cena 

[!include [banner](../includes/psa-now-project-operations.md)]

Pre nego što počnete, ova tema pretpostavlja da ste dovršili procedure u temama [Kreiranje prilagođenih polja i entiteta](create-custom-fields-entities.md) i [Dodavanje prilagođenih polja u podešavanje cena i entitete transakcije](field-references.md). Ako niste dovršili te procedure, vratite se i dovršite ih, a zatim se vratite na ovu temu. 

Ova tema pruža informacije o podešavanju prilagođenih dimenzija za određivanje cena. Na stranici **Parametri** u Project Service veb-interfejsu, kartica **Dimenzije za određivanje cena zasnovane na iznosima** prikazuje zapise u entitetima dimenzija za određivanje cena. Project Service instalacija podrazumevano kreira 2 reda u mreži na ovoj kartici:

- **msdyn_resourcecategory** (uloga)
- **msdyn_OrganizationalUnit** (organizaciona jedinica)

> [!IMPORTANT]
> Nemojte brisati ove redove. Međutim, ako vam nisu potrebni, možete da ih učinite neprimenljivim u određenom kontekstu tako što ćete podesiti **Primenljivo na troškove**, **Primenljivo na prodaju** i **Primenljivo na kupovinu** na **Ne**. Podešavanje vrednosti ovih atributa na **Ne** ima isti efekat: polje ne postoji kao dimenzija za određivanje cena.

Da bi polje postalo dimenzija za određivanje cena, mora biti:

- Kreirano kao polje u entitetima **Cena uloge** i **Provizije na cenu uloge**. Da biste saznali kako ovo da uradite, pročitajte članak [Dodavanje prilagođenih polja u podešavanje cena i entitete transakcije](field-references.md).
- Kreirano kao red u tabeli **Dimenzija za određivanje cena**. Na primer, dodajte redove dimenzije za određivanje cena kao što je prikazano na sledećem grafikonu. 

![Redovi dimenzija za određivanje cena zasnovanih na iznosu](media/Amt-based-PD.png)

Obratite pažnju na to da je radno vreme resursa (**msdyn_resourceworkhours**) dodato kao dimenzija zasnovana na proviziji i da je dodato u mrežu na kartici **Dimenzija za određivanje cena zasnovana na proviziji**.

![Redovi dimenzija za određivanje cena zasnovanih na proviziji](media/Markup-based-PD.png)

> [!IMPORTANT]
> Bilo kakva promena podataka o dimenzijama za određivanje cena u ovoj tabeli, postojeća ili nova, je prosleđena u Project Service poslovnu logiku određivanja cena tek nakon osvežavanja keša. Vreme osvežavanja keša može potrajati do 10 minuta. Iskoristite to vreme da vidite promene podrazumevane logike određivanja cena koje moraju da budu posledica promena podataka o dimenzijama za određivanje cena.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Atributi tabele sa dimenzijama za određivanje cena
Sledeći odeljci pružaju informacije o različitim atributima u tabeli **Dimenzije za određivanje cena**.

### <a name="pricing-dimension-name"></a>Naziv dimenzije za određivanje cena
Ova vrednost bi trebalo da bude ista kao i ime šeme polja koje se dodaje u tabelu **Cena uloge** za prilagođene dimenzije za određivanje cena. Za više informacija o dodavanju polja u tabelu **Cena uloge**, pogledajte članak [Dodavanje prilagođenih polja u podešavanje cena i entitete transakcije](field-references.md).

### <a name="type-of-dimension"></a>Tip dimenzije
Postoje dva tipa dimenzija za određivanje cena.
  
  - **Dimenzije zasnovane na iznosu**: vrednosti dimenzije iz konteksta unosa se podudaraju sa vrednostima dimenzije u stavci **Cena uloge**, a podrazumevana vrednost cene/troškova se izvodi direktno iz tabele **Cena uloge**.
  - **Dimenzije za određivanje cena zasnovane na proviziji**: to su dimenzije u kojima će Project Service usvojiti sledeći proces od 3 koraka za dobijanje cene/troškova
 
    1. Project Service podudara vrednosti dimenzija koje nisu zasnovane na proviziji iz konteksta unosa sa stavkom Cena uloge da bi dobio osnovnu stopu.
    2. Project Service podudara sve vrednosti dimenzija iz konteksta unosa sa stavkom **Provizija na cenu uloge** da bi dobio procenat provizije.
    3. Project Service primenjuje procenat provizije iz drugog koraka na osnovnu stopu dobijenu iz tabele **Cena uloge** u prvom koraku da bi dobio konačnu cenu/troškove.
   
   Sledeća tabela ilustruje izračunavanje provizija na cene.
  
| Uloga        | Organizaciona jedinica    |Radna lokacija      |Standardna pozicija      |Radno vreme resursa      |  Provizija|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|Na lokaciji            |                    |Prekovremeni rad                 |15     |
|             | Contoso India|Lokalno             |                    |Prekovremeni rad                 |10     |
|             | Contoso US   |Lokalno             |                    |Prekovremeni rad                 |20     |


Ako je resurs iz kompanije Contoso India, čija je osnovna stopa 100 USD za rad na lokaciji, a evidentiraju 8 sati redovnog radnog vremena i 2 sata prekovremenog rada u stavci vremena, Project Service sistem za određivanje cena će koristiti osnovnu stopu od 100 za 8 sati da bi evidentirao 800 USD. Za 2 sata prekovremenog rada, provizija od 15% biće primenjena na osnovnu stopu od 100 za dobijanje jedinične cene od 115 USD i biće evidentirani ukupni troškovi od 230 USD.

### <a name="applicable-to-cost"></a>Primenljivo na cenu 
Ako je ovo podešeno na **Da**, to znači da bi vrednost dimenzije iz konteksta unosa trebalo da se koristi za podudaranje sa stavkama **Cena uloge** i **Provizija na cenu uloge** prilikom preuzimanja stope troškova i stope provizija.

### <a name="applicable-to-sales"></a>Primenljivo na prodaju
Ako je ovo podešeno na **Da**, to znači da bi vrednost dimenzije iz konteksta unosa trebalo da se koristi za podudaranje sa stavkama **Cena uloge** i **Provizija na cenu uloge** prilikom preuzimanja stope naplate i stope provizije.

### <a name="applicable-to-purchase"></a>Primenljivo na kupovinu
Ako je ovo podešeno na **Da**, to znači da bi vrednost dimenzije iz konteksta unosa trebalo da se koristi za podudaranje sa stavkama **Cena uloge** i **Provizija na cenu uloge** prilikom preuzimanja cene kupovine. Trenutno Project Service ne podržava scenarije podizvođača, tako da se ovo polje ne koristi. 

### <a name="priority"></a>Prioritet
Podešavanje prioriteta dimenzije pomaže da Project Service određivanje cena iznese cenu čak i kada ne može da pronađe tačnu podudarnost između vrednosti ulaznih dimenzija i vrednosti iz tabele **Cena uloge** ili **Provizija na cenu uloge**. U ovom scenariju, Project Service će koristiti nulte vrednosti za nepodudarne vrednosti dimenzija tako što će težinski faktor dimenzija određivati prema prioritetima.

- **Prioritet cene**: vrednost prioriteta cene dimenzije će ukazati na težinski faktor te dimenzije kada se podudara sa podešavanjem cena koštanja. Vrednost **Prioritet troškova** mora biti jedinstvena za sve dimenzije koje su **primenljive na troškove**.
- **Prioritet prodaje**: vrednost prioriteta prodaje dimenzije će ukazati na težinski faktor te dimenzije kada se podudara sa podešavanjem prodajnih cena ili stopa naplate. Vrednost **prioriteta prodaje** mora biti jedinstvena za sve dimenzije koje su **primenljive na prodaju**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]