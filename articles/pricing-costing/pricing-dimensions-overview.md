---
title: Pregled dimenzija za određivanje cena
description: Ova tema pruža informacije o dimenzija za određivanje cena u usluzi Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fe2ab3a1b12c00e346e27709d66b5a0cb81a3b56
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898233"
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

Dynamics 365 Project Operations se isporučuje sa podrazumevanim skupom dimenzija za određivanje cena. Ove dimenzije za određivanje cena možete da ih vidite tako što ćete otići na **Project Operations** > **Parametri**. U zapisu parametra, na kartici **Dimenzije za određivanje cena zasnovane na iznosima** proverite da li uloga **msdyn_resourcecategory** i organizaciona jedinica resursa **msdyn_organizationalunit** imaju polja **Primenljivo na prodaju** i **Primenljivo na troškove** podešena na **Da**. Kada su ova polja omogućena, možete da podesite cenu i trošak za svaku kombinaciju uloge i organizacione jedinice.

Ako je potrebno da odredite cenu ili troškove resursa pomoću dodatnih atributa, možete da kreirate prilagođena polja, entitete i dimenzije.

## <a name="pricing-human-resource-time"></a>Određivanje cene vremena ljudskog resursa
Kako organizacija određuje cenu vremena ljudskog resursa je često značajno strateško pitanje koje direktno utiče na profitabilnost organizacije. Sarađujte sa finansijskim timovima i budite mudri kada vaša organizacija bude spremna da utvrdi kako želi da podesi stope naplate i troškova za vreme ljudskog resursa.

Druga pitanja koja se tiču formiranja cena podrazumevaju da li ponovo da koristite polja ili entitete koji trenutno nisu dimenzije za određivanje cena, ali se primenjuju kao dimenzija za određivanje cena u vašoj organizaciji. Polja kao što su **Kategorija transakcije** (**msdyn_transactioncategory**) i **Resurs koji može da se rezerviše** (**bookableresource**) su primeri mogućih dimenzija. 

Razmotrite i da li vaša dimenzija za određivanje cena treba da bude tabela ili skup opcija. Ako predviđate promene vrednosti dimenzije koje će premašiti 10 ili 12, a potrebni su vam dodatni atributi za ove vrednosti, možete da kreirate entitet, a ne skup opcija. Održavanje skupa opcija, kao što je dodavanje ili uklanjanje vrednosti, zahteva administratora ili programera, dok većina korisnika može da dodaje nove redove u tabelu.

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
