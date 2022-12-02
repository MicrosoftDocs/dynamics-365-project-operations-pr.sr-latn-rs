---
title: Plaćanje prodavcima nakon izvršene naplate
description: Ova tema objašnjava kako se koristi scenario plaćanja nakon izvršene naplate (PWP).
author: mukumarm
ms.date: 08/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: mukumarm
ms.openlocfilehash: d1fe8d92663b31b22dc405fc1f3e06d976e6c5dc
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525391"
---
# <a name="pay-when-paid-vendor-payments"></a>Plaćanje prodavcima nakon izvršene naplate

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ova tema objašnjava kako se koristi scenario plaćanja nakon izvršene naplate (PWP).

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Kreiranje porudžbenice koja ima PWP uslove

Kada knjižite fakturu od prodavca, ako je dobavljač podložan uslovima za PWP, ti uslovi su prikazani na linijama porudžbenice (PO). Da biste kreirali porudžbenicu koja sadrži uslove za PWP, sledite ove korake.

1. U usluzi Microsoft Dynamics 365 Finance, pratite jedan od ovih koraka:

    - Idite na **Nabavka i poreklo** \> **Porudžbenice** \> **Sve porudžbenice**. U oknu radnji, izaberite **Novo**. U dijalogu **Kreiranje porudžbenice** izaberite dobavljača za koga su podešeni PWP uslovi za projekat, unesite druge potrebne informacije, a zatim izaberite **U redu**.
    - Idite na **Upravljanje projektima i računovodstvo** \> **Projekti** \> **Svi projekti**. U oknu Radnji na kartici **Upravljanje** izaberite **Zadatak stavke**. Izaberite porudžbenicu. Izaberite prodavca za kog su PWP uslovi konfigurisani u projektu, pa izaberite **U redu**.

2. Na stranici **Porudžbenica**, na brzoj kartici **Redovi na porudžbenici** izaberite **Dodaj red** da biste kreirali red porudžbenice.
3. Izaberite broj artikla ili kategoriju nabavke i unesite ostale potrebne detalje. Pregledajte detalje reda PO za dobavljača.

    Opcija **Plati nakon plaćanja** je automatski izabrana, a vrednost u **Procenat praga za PWP** se automatski kopira iz polja **Procenat praga za PWP** na stranici **Projekti**.

4. Ako ne želite da primenite uslove za PWP na prodavca za liniju porudžbenice, obrišite opciju **Plati nakon plaćanja**. U ovom slučaju, polje **Procenat praga za PWP** za red porudžbenice biće vraćeno na **0** (nulu).
5. Na stranici **Porudžbenica**, u oknu radnji na kartici **Nabavka** izaberite **Potvrdi** da biste potvrdili porudžbenicu.
6. U oknu radnji, na kartici **Faktura** izaberite **Faktura** da biste generisali fakturu za porudžbenicu.

## <a name="create-a-project-invoice-proposal"></a>Kreiranje predloga za fakture za projekat

Predlozi za fakture projekta se koriste za kreiranje faktura projekta za klijenta. U PWP scenariju, plaćanja prodavcima zavise od plaćanja klijenata u skladu sa PWP postavkama. Međutim, postoje opcije koje vam omogućavaju da realizujete uplate bez plaćanja klijenta kako zahtevate. Da biste kreirali fakturu za projekat za klijenta, pratite ove korake.

1. U Customer Engagement aplikacijama, idite na stavku **Projekti** \> **Projekti** i izaberite projekat.
2. Na kartici **Stvarne vrednosti** izaberite stvarni red kog generiše porudžbenica i koji ima tip transakcije **Nenaplaćena prodaja**. Zatim izaberite **Spremno za fakturisanje**.
3. Idite na **Prodaja** \> **Prodaja** \> **Projektni ugovor**, pa izaberite projektni ugovor.
4. Na oknu radnji izaberite **Faktura** da biste generisali fakturu za klijenta.
5. U Finansijama, idite na **Upravljanje projektima i računovodstvo** \> **Periodično** \> **Uvoz iz pripremne tabele** i izaberite **U redu** da biste generisali dnevnika Project Operations integracije.
6. Idite na **Upravljanje projektom i računovodstvo** \> **Fakture za projekat** \> **Predlog fakture za projekat** i **Proknjiži** da biste proknjižili predlog fakture koji je generisan za projekat.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Ažurirajte uplatu klijenta i platite prodavcu

Kada prodavac dovrši svoj posao na projektu i pošalje vam fakturu, morate pregledati status projekta i fakture klijenata da biste utvrdili da li su uslovi za PWP ispunjeni za projekat. Ako su ispunjeni uslovi za PWP za dobavljača, možete da odredite koje redove na fakturi dobavljača treba da platite na osnovu uplata klijenata za projekat. Ako odlučite da platite prodavcu iako uslovi za PWP nisu ispunjeni, možete zameniti uslove za PWP na stranici **Faktura prodavca sa plaćanjem nakon uplate**.

1. U odeljku „Finansije“ idite na **Upravljanje projektima i računovodstvo** \> **Projekti** \> **Svi projekti** i izaberite projekat.
2. U oknu Radnje izaberite **Kontrola**, a zatim izaberite **Fakture dobavljača** da biste prikazali sve fakture dobavljača koje su generisane za projekat.
3. Na stranici **Faktura prodavca sa plaćanjem nakon uplate**, u polje za pretragu unesite vrednosti da biste pronašli fakturu dobavljača koju želite da pregledate, a zatim izaberite **Pretraga**.
4. Izaberite opciju **Plati kada vam plate** da biste prikazali samo PWP fakture.
5. Na brzoj kartici **Redovi faktura prodavaca** izaberite redove koje želite da pustite za plaćanje.
6. Izaberite **Pusti uplatu za dobavljača**. Opcija **Plaćanje posle uplate** se briše, a vrednost polja **Spremno za plaćanje** se menja u **Da**.
