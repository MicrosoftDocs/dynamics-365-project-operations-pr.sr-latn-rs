---
title: Pregled dimenzija za određivanje cena
description: Ova tema pruža informacije o dimenzijama za određivanje cena u usluzi Dynamics 365 Project Operations.
author: rumant
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 4b3b71c0b64a24f6914c70c4383eee654e7d4947ececaf9b4e6394f45a081a4c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001988"
---
# <a name="pricing-dimensions-overview"></a>Pregled dimenzija za određivanje cena

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Dimenzije koje se koriste u ljudskim resursima za podešavanje cena i troškova spadaju u dve kategorije:

- Ljudi
- Planirani rad

Zbog toga postoje dve vrste vrednosti dimenzija za određivanje cena koje su dostupne:

- **Skupovi opcija**: Dimenzije koje predstavljaju fiksna nabrajanja za skup vrednosti.
- **Vrednosti zasnovane na entitetima**: Dimenzije koje mogu biti različit skup vrednosti.

## <a name="pricing-dimensions"></a>Dimenzije za određivanje cena

Dynamics 365 Project Operations obavlja isporuku pomoću podrazumevanog skupa dimenzija za određivanje cena. Ove dimenzije za određivanje cena možete da ih vidite tako što ćete otići na **Project Operations** > **Parametri**. U zapisu parametra, na kartici **Dimenzije za određivanje cena zasnovane na iznosima** proverite da li uloga **msdyn_resourcecategory** i organizaciona jedinica resursa **msdyn_organizationalunit** imaju polja **Primenljivo na prodaju** i **Primenljivo na troškove** podešena na **Da**. Kada su ova polja omogućena, možete da podesite cenu i trošak za svaku kombinaciju uloge i organizacione jedinice.

![Snimak ekrana Project Service parametara sa markiranom stavkom „Primenljivo na prodaju“.](media/PS-OOB-parameters.png)

Ako je potrebno da odredite cenu ili troškove resursa pomoću dodatnih atributa, možete da kreirate prilagođena polja, entitete i dimenzije. Pogledajte sledeći odeljak za više informacija. 
  
  > [!NOTE]
  > Postupci moraju biti završeni kako bi bili navedeni.

1. [Kreiranje rešenja za prilagođene dimenzije određivanja cena](../sales/create-solution-custompd.md)
2. [Kreiranje prilagođenih polja i entiteta](create-custom-fields-entities-pricing-dimensions.md)
3. [Dodavanje prilagođenih polja u podešavanje cena i entitete transakcije ](add-custom-fields-price-setup-transactional-entities.md)
4. [Podešavanje prilagođenih polja kao dimenzija za određivanje cena ](set-up-custom-fields-pricing-dimensions.md)
5. [Ažuriranje atributa dodatnih komponenti tako da uključuju nove dimenzije za određivanje cena](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a>Određivanje cene vremena ljudskog resursa
Kako organizacija određuje cenu vremena ljudskog resursa je često značajno strateško pitanje koje direktno utiče na profitabilnost organizacije. Sarađujte sa finansijskim timovima i budite mudri kada vaša organizacija bude spremna da utvrdi kako želi da podesi stope naplate i troškova za vreme ljudskog resursa.

Druga pitanja koja se tiču formiranja cena podrazumevaju da li ponovo da koristite polja ili entitete koji trenutno nisu dimenzije za određivanje cena, ali se primenjuju kao dimenzija za određivanje cena u vašoj organizaciji. Polja kao što su **Kategorija transakcije** (**msdyn_transactioncategory**) i **Resurs koji može da se rezerviše** (**bookableresource**) su primeri mogućih dimenzija. 

Razmotrite i da li vaša dimenzija za određivanje cena treba da bude tabela ili skup opcija. Ako predviđate promene vrednosti dimenzije koje će premašiti 10 ili 12, a potrebni su vam dodatni atributi za ove vrednosti, možete da kreirate entitet, a ne skup opcija. Održavanje skupa opcija, kao što je dodavanje ili uklanjanje vrednosti, zahteva administratora ili programera, dok većina korisnika može da dodaje nove redove u tabelu.

Sledeći primer prikazuje kursne stope koje su podešene na osnovu uloge i organizacione jedinice resursa kome pripada resurs. Stope troškova se obično zasnivaju na grupi ličnih dohodaka zaposlenih i organizacionoj jedinici kojoj pripadaju. U ovom primeru, tabele sa stopama naplate i stopama troškova će izgledati ovako:

**Primeri stopa naplate**

| Uloga        | Organizaciona jedinica    |Jedinica      |Cena      |Valuta  |
| ------------|-------------|----------|----------:|----------|
| Programer   | Contoso US  |Sat | 200|USD rešenje     |
| Programer   | Contoso India |Sat|   112|USD rešenje     |


**Primeri stopa troškova**

| Grupa ličnih dohodaka     | Organizaciona jedinica    |Jedinica      |Cena      |Valuta  |
| ----------------|-------------|----------|----------:|----------|
| Moje preduzeće_Prva grupa ličnih dohodaka | Contoso US  |Sat | 145|USD rešenje     |
| Moje preduzeće_druga grupa ličnih dohodaka | Contoso India |Sat|   67|USD rešenje     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]