---
title: Matična stranica za dimenzije određivanja cena i obračuna troškova
description: Ova tema obezbeđuje pregled dimenzija za određivanje cena.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 515a2e2e518614884b414ca43702e8bfea2c6919
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083621"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Matična stranica za dimenzije određivanja cena i obračuna troškova

Na dimenzije koje se koriste za određivanje cena i troškova rada u projektnim organizacijama utiču sledeći atributi:

- Ljudi koji rade posao sličan svom iskustvu, ulozi ili geografskoj lokaciji
- Posao koji treba obaviti, sličan po složenosti ili dobu dana

S obzirom na tipičnu prirodu ovih atributa posla i ljudi koji su potrebni za obavljanje posla, postoje dve vrste vrednosti dimenzija cene koje su dostupne u usluzi Project Service Automation: 

- **Skupovi opcija** – Atributi koji predstavljaju fiksna nabrajanja za skup vrednosti.
- **Vrednosti zasnovane na entitetima** – Atributi koji mogu imati različit skup vrednosti koje su konačne, ali se vremenom mogu menjati.

## <a name="pricing-dimensions"></a>Dimenzije za određivanje cena

PSA obavlja isporuku pomoću podrazumevanog skup dimenzija za određivanje cena. Možete da ih vidite tako što ćete otići na **Project Service** > **Parametri**. U zapisu parametra, na kartici **Dimenzije za određivanje cena zasnovane na iznosima** proverite da li uloga **msdyn_resourcecategory** i organizaciona jedinica resursa **msdyn_organizationalunit** imaju polja **Primenljivo na prodaju** i **Primenljivo na troškove** podešena na **Da**. Ovo će vam omogućiti podešavanje cene i troška za svaku kombinaciju uloge i organizacione jedinice.

![Snimak ekrana Project Service parametara sa markiranom stavkom „Primenljivo na prodaju“](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Ako ste koristili unapred definisana polja uloge i organizacionih jedinica kao dimenzije za određivanje cena pre verzije 3 aplikacije PSA, neće biti nikakvih primetnih promena. Možete da nastavite da koristite Project Service kao i obično. 

Ako je potrebno da odredite cenu ili troškove resursa pomoću dodatnih atributa, možete da kreirate prilagođena polja, entitete i dimenzije. Da biste dobili više informacija, pogledajte sledeće teme, ali imajte na umu da morate da dovršite procedure po dolenavedenom redosledu:

- [Kreiranje prilagođenih polja i entiteta](create-custom-fields-entities.md)
- [Dodavanje prilagođenih polja u podešavanje cena i entitete transakcije](field-references.md)
- [Podešavanje prilagođenih polja kao dimenzija za određivanje cena ](set-up-pricing-dimensions.md)
- [Ažuriranje atributa dodatnih komponenti tako da uključuju nove dimenzije za određivanje cena](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Određivanje cene vremena ljudskog resursa
Kako organizacija određuje cenu vremena ljudskog resursa je često značajno strateško pitanje koje direktno utiče na profitabilnost organizacije. Sarađujte sa finansijskim timovima i budite mudri kada vaša organizacija bude spremna da utvrdi kako želi da podesi stope naplate i troškova za vreme ljudskog resursa.

Druga pitanja koja se tiču formiranja cena podrazumevaju da li ponovo da koristite polja ili entitete koji trenutno nisu dimenzije za određivanje cena, ali se primenjuju kao dimenzija za određivanje cena u vašoj organizaciji. Polja kao što su **Kategorija transakcije** ( **msdyn_transactioncategory** ) i **Resurs koji može da se rezerviše** ( **bookableresource** ) su primeri mogućih dimenzija. 

Razmotrite i da li vaša dimenzija za određivanje cena treba da bude tabela ili skup opcija. Ako predviđate promene vrednosti dimenzije koje će premašiti 10 ili 12, a potrebni su vam dodatni atributi za ove vrednosti, bolje je da kreirate entitet nego skup opcija. Održavanje skupa opcija, kao što je dodavanje ili uklanjanje vrednosti, zahteva administratora ili programera, dok većina poslovnih korisnika može da dodaje nove redove u tabelu.

Sledeći primer prikazuje kursne stope koje su podešene na osnovu uloge i organizacione jedinice resursa kome pripada resurs. Stope troškova se obično zasnivaju na grupi ličnih dohodaka zaposlenih i organizacionoj jedinici kojoj pripadaju. U ovom primeru, tabele sa stopama naplate i stopama troškova će izgledati ovako:

**Primeri stopa naplate**

| Uloga        | Organizaciona jedinica    |Jedinica      |Cena      |Valuta  |
| ------------|-------------|----------|----------:|----------|
| Programer   | Contoso US  |Hour | 200|USD     |
| Programer   | Contoso India |Hour|   112|USD     |


**Primeri stopa troškova**

| Grupa ličnih dohodaka     | Organizaciona jedinica    |Jedinica      |Cena      |Valuta  |
| ----------------|-------------|----------|----------:|----------|
| Moje preduzeće_Prva grupa ličnih dohodaka | Contoso US  |Hour | 145|USD     |
| Moje preduzeće_druga grupa ličnih dohodaka | Contoso India |Hour|   67|USD     |
