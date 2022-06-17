---
title: Kreirajte i primenite uslove zadržavanja plaćanja prodavca
description: Ovaj članak pruža informacije o tome kako da podesite i održite uslove zadržavanja za uplate dobavljačima.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 2cd18375d93e503ac532cb3839c691231ea46681
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916765"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Kreirajte i primenite uslove zadržavanja plaćanja prodavca

[!include [banner](../includes/banner.md)] 

Postavljanje uslova zadržavanja za plaćanja prodavaca za projekat korisno je kada vaša organizacija želi da zadrži deo uplata izvršenih prodavcu. Na primer, kada želite da zadržite plaćanje prodavcu dok isporučeni proizvodi ne ispune vaša očekivanja. Uslovi zadržavanja za plaćanja prodavaca mogu se odrediti kada pregovarate o ugovoru prodavca.

## <a name="create-vendor-payment-retention-terms"></a>Kreirajte uslove zadržavanja plaćanja prodavca

Možete da unesete procenat plaćanja prodavca za zadržavanje i procenat prethodno zadržanih iznosa koji će se osloboditi. Iznosi se automatski zadržavaju na fakturama prodavaca sve dok ugovor ne dostigne određeni status završenosti. Nakon što postavite uslove zadržavanja, možete ih primeniti na bilo koji projekat tog prodavca.

Koristite sledeće korake za postavljanje i održavanje uslova zadržavanja za plaćanja prodavca. 

1. Idite na **Upravljanje projektima i računovodstvo** > **Zadržavanje** > **Uslovi zadržavanja za plaćanja prodavaca**.
2. Izaberite **Novo** da biste dodali novi uslov zadržavanja za prodavce. Vrednost **ID pravila** za novi uslov se automatski unosi. 
3. Unesite kratak opis u polje **Opis**, a na brzoj kartici **Uslovi** izaberite **Dodaj liniju** da biste uneli vrednosti uslova za sledeće:

   - **Procenat isporučenih jedinica**: Unesite procenat završetka za uslov. Iznosi se automatski zadržavaju na fakturama prodavaca sve dok faza dovršetka projekta ne bude ista kao navedeni procenat. Na primer, ako unesete 50,00, iznosi se zadržavaju sve dok projekat ne bude završen 50 odsto.
   - **Procenat za zadržavanje**: Unesite procenat iznosa fakture dobavljača koji će se zadržati. Na primer, ako unesete 10,00, tada se zadržava 10 procenata iznosa na fakturi dobavljača sve dok projekat ne dostigne procenat završetka kako je postavljeno u polje **Procenat isporučenih jedinica**.
   - **Procenat za oslobađanje**: Izaberite **Dodaj liniju** da biste uneli procenat svih prethodno zadržanih iznosa koji će se osloboditi za izabrani nivo završetka projekta.

> [!NOTE]
> Ako imate više od jedne kontrolne tačke za različite nivoe završetka projekta, unesite zasebnu liniju uslova zadržavanja za prodavca za svako pravilo zadržavanja. Svaka linija može navoditi različiti procenat zadržavanja i drugačiji procenat izdavanja za svaki naznačeni nivo završetka projekta.

Nakon što kreirate uslove zadržavanja za prodavca, možete ih primeniti na projekat.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Primenite uslove zadržavanja za prodavca na projekat

1. Idite na **Upravljanje projektima i računovodstvo** > **Projekti** > **Svi projekti** i otvorite projekat sa stranice liste projekata.
2. Na brzoj kartici **Ugovori sa prodavcima** izaberite **Dodaj liniju**.
3. U polju **Kôd poslovnog kontakta** izaberite jednu od sledećih opcija: 

   - **Tabela**: Uslovi zadržavanja za prodavce se primenjuju na jednog prodavca.
   - **Grupa** – Uslovi zadržavanja za prodavce važe za sve prodavce u grupi.
   - **Sve**: Uslovi zadržavanja za prodavce se primenjuju na sve prodavce.

4. U **polju Dobavljač/grupa prodavaca**, izaberite prodavca ili grupu prodavaca na koje se primenjuju uslovi zadržavanja za prodavce. Ako ste izabrali **Sve** u prethodnom koraku, ovo polje nije dostupno.
5. U polju **Uslovi zadržavanja za prodavce** izaberite uslove zadržavanja koje ste kreirali u prethodnom postupku.
6. Ako projekat takođe ima uslove za plaćanje nakon uplate (PWP) za prodavca, unesite procenat praga za projekat u polje **Procenat PWP praga**.

Uslovi zadržavanja za prodavce se takođe prikazuju na porudžbenicama koje kreirate za prodavca.


[!INCLUDE[footer-include](../includes/footer-banner.md)]