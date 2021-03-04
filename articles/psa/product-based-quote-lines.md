---
title: Stavke ponuda zasnovane na proizvodu
description: Ova tema pruža informacije o stavkama ponuda zasnovanim na proizvodu.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a5b52e74994a40b20353d85d1d9bcd59d435cd0b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151270"
---
# <a name="product-based-quote-lines"></a>Stavke ponuda zasnovane na proizvodu

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Možete kreirati stavke ponude zasnovane na proizvodu u aplikaciji Dynamics 365 Project Service Automation. To mogu da budu stavke za unos ili stavke iz kataloga proizvoda.

## <a name="product-catalog"></a>Katalog proizvoda

Proizvodi u Dynamics 365 katalogu proizvoda imaju podrazumevanu jedinicu i grupu jedinica. Ako nekoliko proizvoda deli isti skup atributa, možete da kreirate grupu proizvoda koja takođe ima te atribute. Svi proizvodi iz jedne grupe proizvoda nasljeđuju isti skup atributa.

Na primer, kompanija prodaje licence za pretplatu na razni softver. Sav softver za pretplatu ima sledeća dva atributa:

- Broj korisnika 
- Trajanje pretplate (u mesecima)

Dobar način za održavanje ove vrste kataloga je kreiranje grupe proizvoda pod imenom **Softver za pretplatu** i sa atributima **Broj korisnika** i **Trajanje pretplate**. Zatim možete dodati pojedinačne proizvode, kao što su **Dynamics 365 Sales** ili **Dynamics 365 Field Service** u grupu proizvoda **Softver za pretplatu**.

## <a name="adding-product-catalog-items-to-a-project-quote"></a>Dodavanje stavki iz kataloga proizvoda u ponudu za projekat

Stranica sa ponudom za projekat i stranica ugovora imaju odeljke za dve vrste stavki: stavke zasnovane na projektu i stavke zasnovane na proizvodu. Za stavke zasnovane na proizvodu, Dynamics 365 se koristi za dodavanje stavki iz kataloga proizvoda u ponudu. Padajuća lista u okviru stavke ponude ili predmeta ugovora za projekat uključuje sve proizvode i jedinice u cenovniku proizvoda koji je priložen uz ponudu ili ugovor o projektu. Takođe možete da dodate proizvode koji nisu deo cenovnika proizvoda ponude.

Pored toga, možete odabrati proizvode iz drugih cenovnika ili možete odabrati proizvode direktno iz kataloga proizvoda. Kada izaberete proizvode direktno iz kataloga proizvoda, koristi se podrazumevani cenovnik tog proizvoda da biste dobili prodajnu cenu proizvoda. Ako podrazumevani cenovnik nije podešen, cena se podešava na 0 (nula).

Ako se stavka ponude temelji na katalogu proizvoda, možete izmeniti prodajnu cenu direktno u stavci ponude. Imajte na umu da stavka ponude u sistemu Dynamics 365 ima polje **Određivanje cena**. Dostupne su dve vrednosti:

- Izmena načina određivanja cena  
- Koristi podrazumevane cene

Ako ovo polje podesite na **Izmena načina određivanja cena**, Dynamics 365 ne podešava podrazumevanu cenu. Morate da unesete cenu proizvoda u stavku ponude. Ako ovo polje podesite na **Koristi podrazumevane cene**, Dynamics 365 koristi podrazumevane prodajne cene i zaključava polje radi sprečavanja uređivanja.

Nakon što instalirate PSA, podrazumevane prodajne cene se unose u stavke zasnovane na proizvodima u okviru ponude. Polje **Određivanje cena** se tada podešava na **Izmeni način određivanja cena** tako da možete da uredite podrazumevanu cenu u stavkama ponude.

> ![Podešavanje izmene načina određivanja cena](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>Količinski faktori proizvoda

PSA koristi količinske faktore da podrži prodaju proizvoda zasnovanih na pretplati. Za proizvode zasnovane na pretplati, količina u stavci ponude ili predmetu ugovora o projektu izražena je kao broj korisničkih meseci.

Obično se cena softvera za pretplatu čuva u katalogu kao cena po korisniku mesečno. Međutim, umesto toga možete koristiti opise drugih perioda. Tokom procesa prodaje, cena u stavci ponude je obično cena po korisniku, mesečno, do koje se došlo pregovorima i popustima od strane IT agenta prodaje. Svaka pogodba ima različit broj korisnika i različit broj meseci pretplate. Količina koja se koristi za izračunavanje količine stavke ponude je proizvod broja korisnika i broja meseci pretplate.

Da bi podržao ovu vrstu prodaje, PSA je uveo koncept faktora količine. Količinski faktori se oslanjaju na atribute proizvoda u sistemu Dynamics 365. Kada konfigurišete određene osobine proizvoda, PSA vam omogućava da označite podskup tih svojstava ili sva svojstva kao faktore količine.

PSA potvrđuje da se kao faktori količine označavaju samo numerička svojstva ili svojstva proizvoda koja imaju numerički tip podataka. Kada se proizvod za koji su konfigurisani faktori količine doda u stavku ponude, polje **Količina** u stavci ponude postaje polje samo za čitanje. Nakon što unesete vrednosti za svojstva proizvoda koja su količinski faktori, PSA izračunava količinu stavke ponude.

Na primer, Dynamics 365 može imati sledeća svojstva: 

- **Br. korisnika** - Broj korisnika 
- **Br. meseci** - Broj meseci pretplate
- **SKU proizvoda** 

Svojstva **Br. korisnika** i **Br. meseci** se mogu označiti kao faktori količine, uređivanjem svojstava u stavci proizvoda. 

> ![Označavanje broja korisnika i broja meseci kao faktora kvaliteta](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]