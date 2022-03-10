---
title: Podešavanje prilagođenih polja kao dimenzija za određivanje cena
description: Ova tema pruža informacije o tome kako da podesite dimenzije za određivanje cena pomoću prilagođenih polja.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e40f0336d98cd8452642eb582c4d9daf2304ceb2532ef75ce9d03a0fa4bd8e8b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003608"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>Podešavanje prilagođenih polja kao dimenzija za određivanje cena

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Pre nego što počnete, ova tema pretpostavlja da ste dovršili procedure u temama [Kreiranje prilagođenih polja i entiteta](create-custom-fields-entities-pricing-dimensions.md) i [Dodavanje obaveznih prilagođenih polja u podešavanje cena i entitete transakcije](add-custom-fields-price-setup-transactional-entities.md). Ako niste dovršili te procedure, vratite se i dovršite ih, a zatim se vratite na ovu temu. 

Ova tema pruža informacije o podešavanju prilagođenih dimenzija za određivanje cena. Na stranici **Parametri**, na kartici **Dimenzije za određivanje cena zasnovane na iznosima**, prikazuju se zapisi u entitetima dimenzije za određivanje cena. Na mreži se na ovoj kartici podrazumevano nalaze dva reda u mreži:

- **msdyn_resourcecategory** (uloga)
- **msdyn_OrganizationalUnit** (organizaciona jedinica)

> [!IMPORTANT]
> Nemojte brisati ove redove. Međutim, ako vam nisu potrebni, možete da ih učinite neprimenljivim u određenom kontekstu tako što ćete podesiti **Primenljivo na troškove**, **Primenljivo na prodaju** i **Primenljivo na kupovinu** na **Ne**. Podešavanje vrednosti ovih atributa na **Ne** ima isti efekat: polje ne postoji kao dimenzija za određivanje cena.

Da bi polje postalo dimenzija za određivanje cena, mora biti:

- Kreirano kao polje u entitetima **Cena uloge** i **Provizije na cenu uloge**. Da biste saznali kako ovo da uradite, pročitajte članak [Dodavanje prilagođenih polja u podešavanje cena i entitete transakcije](add-custom-fields-price-setup-transactional-entities.md).

- Kreirano kao red u tabeli **Dimenzija za određivanje cena**. Na primer, dodajte redove dimenzije za određivanje cena kao što je prikazano na sledećem grafikonu. 

![Redovi dimenzija za određivanje cena zasnovanih na iznosu.](media/Amt-based-PD.png)

Radno vreme resursa (**msdyn_resourceworkhours**) je dodato kao dimenzija zasnovana na proviziji i da je dodato u mrežu na kartici **Dimenzija za određivanje cena zasnovana na proviziji**.

![Redovi dimenzija za određivanje cena zasnovanih na proviziji.](media/Markup-based-PD.png)


> [!IMPORTANT]
> Bilo kakva promena podataka o dimenzijama za određivanje cena u ovoj tabeli, postojeća ili nova, je prosleđena u poslovnu logiku određivanja cena tek nakon osvežavanja keša. Vreme osvežavanja keša može potrajati do 10 minuta. Iskoristite to vreme da vidite promene podrazumevane logike određivanja cena koje moraju da budu posledica promena podataka o dimenzijama za određivanje cena.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Atributi tabele sa dimenzijama za određivanje cena
Sledeći odeljci pružaju informacije o različitim atributima u tabeli **Dimenzije za određivanje cena**.

### <a name="pricing-dimension-name"></a>Naziv dimenzije za određivanje cena
Ova vrednost bi trebalo da bude ista kao i ime šeme polja koje se dodaje u tabelu **Cena uloge** za prilagođene dimenzije za određivanje cena. Za više informacija o dodavanju polja u tabelu **Cena uloge**, pogledajte članak [Dodavanje prilagođenih polja u podešavanje cena i entitete transakcije](add-custom-fields-price-setup-transactional-entities.md).

### <a name="type-of-dimension"></a>Tip dimenzije
Postoje dva tipa dimenzija za određivanje cena.
  
  - **Dimenzije zasnovane na iznosu**: vrednosti dimenzije iz konteksta unosa se podudaraju sa vrednostima dimenzije u stavci **Cena uloge**, a podrazumevana vrednost cene/troškova se izvodi direktno iz tabele **Cena uloge**.
  - **Dimenzije za određivanje cena zasnovane na proviziji**: to su dimenzije u kojima se koristi sledeći proces od tri koraka za dobijanje cene/troškova:
 
    1. Vrednosti dimenzija koje nisu zasnovane na proviziji iz konteksta unosa podudaraju se sa stavkom Cena uloge da bi dobio osnovnu stopu.
    2. Vrednosti dimenzija iz konteksta unosa se podudaraju sa stavkom **Provizija na cenu uloge** da bi dobio procenat provizije.
    3. Procenat provizije iz drugog koraka se primenjuje na osnovnu stopu dobijenu iz tabele **Cena uloge** u prvom koraku da bi dobio konačnu cenu/troškove.
   
   Sledeća tabela ilustruje izračunavanje provizija na cene.
  
| Uloga        | Organizaciona jedinica    |Radna lokacija      |Standardna pozicija      |Radno vreme resursa      |  Provizija|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|Na lokaciji            |                    |Prekovremeni rad                 |15     |
|             | Contoso India|Lokalno             |                    |Prekovremeni rad                 |10     |
|             | Contoso US   |Lokalno             |                    |Prekovremeni rad                 |20     |


Ako je resurs iz kompanije Contoso India, čija je osnovna stopa 100 USD za rad na lokaciji, a evidentiraju 8 sati redovnog radnog vremena i 2 sata prekovremenog rada u stavci vremena, mehanizam za određivanje cena će koristiti osnovnu stopu od 100 za 8 sati da bi evidentirao 800 USD. Za 2 sata prekovremenog rada, provizija od 15% biće primenjena na osnovnu stopu od 100 za dobijanje jedinične cene od 115 USD i biće evidentirani ukupni troškovi od 230 USD.

### <a name="applicable-to-cost"></a>Primenljivo na cenu 
Ako je ovo podešeno na **Da**, to znači da bi vrednost dimenzije iz konteksta unosa trebalo da se koristi za podudaranje sa stavkama **Cena uloge** i **Provizija na cenu uloge** prilikom preuzimanja stope troškova i stope provizija.

### <a name="applicable-to-sales"></a>Primenljivo na prodaju
Ako je ovo podešeno na **Da**, to znači da bi vrednost dimenzije iz konteksta unosa trebalo da se koristi za podudaranje sa stavkama **Cena uloge** i **Provizija na cenu uloge** prilikom preuzimanja stope naplate i stope provizije.

### <a name="applicable-to-purchase"></a>Primenljivo na kupovinu
Ako je ovo podešeno na **Da**, to znači da bi vrednost dimenzije iz konteksta unosa trebalo da se koristi za podudaranje sa stavkama **Cena uloge** i **Provizija na cenu uloge** prilikom preuzimanja cene kupovine. Scenariji podugovaranja nisu podržani, pa se ovo polje ne koristi. 

### <a name="priority"></a>Prioritet
Podešavanje prioriteta dimenzije pomaže da određivanje cena iznese cenu čak i kada ne može da pronađe tačnu podudarnost između vrednosti ulaznih dimenzija i vrednosti iz tabele **Cena uloge** ili **Provizija na cenu uloge**. U ovom scenariju, se koriste nulte vrednosti za nepodudarne vrednosti dimenzija tako što će težinski faktor dimenzija određivati prema prioritetima.

- **Prioritet cene**: vrednost prioriteta cene dimenzije će ukazati na težinski faktor te dimenzije kada se podudara sa podešavanjem cena koštanja. Vrednost **Prioritet troškova** mora biti jedinstvena za sve dimenzije koje su **primenljive na troškove**.
- **Prioritet prodaje**: vrednost prioriteta prodaje dimenzije će ukazati na težinski faktor te dimenzije kada se podudara sa podešavanjem prodajnih cena ili stopa naplate. Vrednost **prioriteta prodaje** mora biti jedinstvena za sve dimenzije koje su **primenljive na prodaju**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]