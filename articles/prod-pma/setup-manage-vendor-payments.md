---
title: Podesite i koristite plaćanja prodavcima nakon izvršene naplate
description: Ova tema objašnjava kako kreirati uslove za plaćanje nakon izvršene naplate (PWP) tako da možete puštati delimične uplate dobavljača na osnovu plaćanja klijenata.
author: RadhikaRS
ms.date: 03/30/2020
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
ms.openlocfilehash: 71f7b1db58c0d6aacc4f47920e5ad39dbb35ec51
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683930"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Podesite i koristite plaćanja prodavcima nakon izvršene naplate

[!include [banner](../includes/banner.md)]

Kada odobrite dobavljača da radi kao podizvođač, možda ćete želeti da zadržite plaćanje dobavljaču sve dok vam klijent ne plati za projekat. Da biste podržali ovaj scenario, možete da postavite uslove za plaćanje nakon izvršene naplate (PWP) kada sa dobavljačem postavljate porudžbenicu (PO).

Na primer, kada klijent plati iznos na fakturi projekta, možete pustiti deo ili ceo iznos fakture prodavca. Samo podesite uslove za PWP koji određuju da će prodavac biti plaćen nakon što od klijenta primite procenat odgovarajuće uplate. Ako primite delimičnu uplatu od klijenta, možete ručno da pustite neke od povezanih faktura prodavca na plaćanje.

Sledeći primer opisuje postupak kada se koriste uslove za PWP.

## <a name="example"></a>Primer

Vaša organizacija pristaje da klijentu obezbedi 100 računara na kojima je instaliran softver, po ceni od 150,00 američkih dolara (USD) po računaru. Zatim unajmite prodavca da vam obezbedi računare na kojima je instaliran softver. Prema ugovoru, klijent mora da odobri kvalitet računara pre nego što plati vašoj organizaciji. Politika vaše organizacije je zadržavanje plaćanja prodavcima dok vam klijent ne plati. Stoga ste projekat postavili tako da ima procenat PWP od 100 procenata.

Prodavac vam šalje 100 računara na kojima je instaliran softver, zajedno sa fakturom na 10.000,00 USD. Budući da su za vaš projekat postavljeni uslovi za PWP, ne plaćate prodavcu po prijemu računara. Umesto toga, računare šaljete klijentu, zajedno sa fakturom na 15.000,00. Klijent pregleda računare i odobrava puni iznos fakture projekta.

Nakon što od klijenta primite celokupnu uplatu, prodavcu plaćate 10.000,00, puni iznos fakture prodavca.

## <a name="set-up-pwp-terms-for-a-project"></a>Postavite uslove za PWP za projekat

Kada postavljate uslove za PWP za projekat, morate odrediti, u procentima, minimalni iznos koji vam klijent mora platiti za projekat pre nego što platite prodavcu. Iznos praga se automatski izračunava na fakturama klijenta za projekat. Sledite ove korake da biste postavili procenat praga za uslove za PWP.

1. Idite na **Upravljanje projektima i računovodstvo** \> **Projekti** \> **Svi projekti**.
2. Pronađite i otvorite projekat za koji želite da postavite uslove za PWP.
3. Na brzoj kartici **Ugovori sa prodavcima** izaberite **Dodaj liniju**.
3. U polju **Kôd poslovnog kontakta** izaberite jednu od sledećih opcija:

    - **Tabela** – Uslovi za PWP se primenjuju na jednog prodavca.
    - **Grupa** – Uslovi za PWP važe za sve prodavce u grupi.
    - **Sve** - Uslovi za PWP važe za sve prodavce.

4. Ako ste izabrali **Tabela** ili **Grupa** u prethodnom koraku, u polju **Prodavac/grupa prodavaca** izaberite prodavca ili grupu prodavaca na koje se odnose uslovi za PWP. Ako ste izabrali **Sve** u prethodnom koraku, polje **Prodavac/grupa prodavaca** se ne može uređivati.
5. Ako su uslovi zadržavanja prodavaca postavljeni za prodavca u projektu, u polju **Uslovi zadržavanja prodavaca** izaberite ID pravila za uslove zadržavanja.
6. U polje **Procenat PWP praga** unesite procenat praga za projekat. Procenat koji unesete za projekat definiše minimalni iznos koji vam klijent mora platiti pre nego što platite prodavcu.

## <a name="create-a-po-that-has-pwp-terms"></a>Napravite PO koji sadrži uslove za PWP

Kada knjižite fakturu od prodavca, ako je dobavljač podložan uslovima za PWP, ti uslovi su prikazani na linijama porudžbenice. Da biste kreirali porudžbenicu koja sadrži uslove za PWP, sledite ove korake.

1. Idite na **Nabavka i poreklo** \> **Porudžbenice** \> **Sve porudžbenice**.
2. U oknu radnji, izaberite **Novo**. Zatim, u dijalogu **Kreirajte porudžbenicu** unesite potrebne informacije i izaberite **U redu**.

    Alternativno, otvorite postojeću porudžbenicu na stranici liste **Sve porudžbenice**.

4. Na stranici **Porudžbenica**, na brzoj kartici **Redovi porudžbenica** pregledajte detalje o liniji porudžbenice za prodavca. Opcija **Plati nakon plaćanja** je automatski izabrana, a vrednost u **Procenat praga za PWP** se automatski kopira iz polja **Procenat praga za PWP** na stranici **Projekti**.
6. Ako ne želite da primenite uslove za PWP na prodavca za liniju porudžbenice, obrišite opciju **Plati nakon plaćanja**. U ovom slučaju, polje **Procenat praga za PWP** za liniju porudžbenice biće vraćeno na 0 (nulu).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Ažurirajte uplatu klijenta i platite prodavcu

Kada prodavac dovrši svoj posao na projektu i pošalje vam fakturu, morate pregledati status projekta i fakture klijenata da biste utvrdili da li su uslovi za PWP ispunjeni za projekat. Ako su ispunjeni uslovi za PWP za dobavljača, možete da odredite koje redove na fakturi dobavljača treba da platite na osnovu uplata klijenata za projekat. Ako odlučite da platite prodavcu iako uslovi za PWP nisu ispunjeni, možete zameniti uslove za PWP na stranici **Faktura prodavca sa plaćanjem nakon uplate**.

1. Idite na **Upravljanje projektima i računovodstvo** \> **Upiti i izveštaji** \> **Upiti o zadržavanju** \> **Faktura prodavca sa plaćanjem nakon uplate**.
2. Na stranici **Faktura prodavca sa plaćanjem nakon uplate**, u polje za pretragu unesite vrednosti da biste pronašli fakturu dobavljača koju želite da pregledate, a zatim izaberite **Pretraga**.
3. Na brzoj kartici **Redovi faktura prodavaca** izaberite redove koje želite da promenite.
4. Ako su ispunjeni uslovi za **Plaćanje nakon uplate** za stavku fakture, izaberite **Pusti uplatu prodavca**. Opcija **Plaćanje posle uplate** se briše, a vrednost polja **Spremno za plaćanje** se menja u **Da**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]