---
title: Plaćanje prilikom plaćanja uplatama dobavljača
description: Ova tema objašnjava kako se koristi scenario plaćanja prilikom plaćanja (PWP).
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
# <a name="pay-when-paid-vendor-payments"></a>Plaćanje prilikom plaćanja uplatama dobavljača

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ova tema objašnjava kako se koristi scenario plaćanja prilikom plaćanja (PWP).

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Kreiranje izlazne porudžbine koja ima PWP uslove

Kada proknjižite fakturu od dobavljača, ako dobavljač podleže odredbama PWP, ti uslovi se prikazuju u redovima izlazne porudžbine (PO). Da biste kreirali porudžbenicu koja sadrži uslove za PWP, sledite ove korake.

1. U Microsoft Dynamics 365 Finance sledite jedan od ovih koraka:

    - Idite na **Nabavka i poreklo** \> **Porudžbenice** \> **Sve porudžbenice**. U oknu radnji, izaberite **Novo**. U dijalogu **Kreiranje izlazne porudžbine** izaberite dobavljača za koga su podešeni PWP uslovi za projekat, unesite druge potrebne informacije, a zatim kliknite na dugme U **redu**.
    - Idite na **Upravljanje projektima i računovodstvo** \> **Projekti** \> **Svi projekti**. U oknu za radnje, na kartici **Upravljanje** izaberite stavku Zadatak **stavke**. Izaberite izlaznu porudžbinu. Izaberite dobavljača za koje su U projektu podešeni PWP uslovi, a zatim kliknite na dugme U **redu**.

2. Na stranici **Izlazna porudžbina**, na brzoj kartici **Redovi izlazne porudžbine** izaberite stavku Dodaj **red da biste** kreirali red izlazne porudžbine.
3. Izaberite broj artikla ili kategoriju nabavke i unesite ostale potrebne detalje. Pregledajte detalje reda PO za dobavljača.

    Opcija **Plati nakon plaćanja** je automatski izabrana, a vrednost u **Procenat praga za PWP** se automatski kopira iz polja **Procenat praga za PWP** na stranici **Projekti**.

4. Ako ne želite da primenite uslove za PWP na prodavca za liniju porudžbenice, obrišite opciju **Plati nakon plaćanja**. U ovom slučaju, polje **procenta PWP praga** za PO red biće vraćeno na **0** (nula).
5. Na stranici Izlazna porudžbina **, u oknu za radnje, na kartici Nabavka** **izaberite stavku Potvrdi da** **biste potvrdili izlaznu porudžbinu.**
6. U oknu za radnje, na kartici Faktura **izaberite** stavku Faktura **da** biste generisali fakturu za izlaznu porudžbinu.

## <a name="create-a-project-invoice-proposal"></a>Kreiranje predloga fakture projekta

Predlozi za projektnu fakturu se koriste za kreiranje projektne fakture za kupca. U PWP scenariju, uplate dobavljača zavise od plaćanja kupaca u skladu sa PWP postavkama. Međutim, postoje opcije koje vam omogućava da uplate bez plaćanja kupca oslobodite onako kako zahtevate. Da biste kreirali fakturu projekta za kupca, sledite ove korake.

1. U aplikacijama za angažovanje klijenata idite **na Project** \> **Projects** i izaberite projekat.
2. Na kartici **"Stvarne** datoteke" izaberite stvarni red koji generiše PO koji ima vrstu transakcije **"Nekontrolisana** prodaja". Zatim izaberite opciju **Spremno za fakturu**.
3. Idite na **ugovor** \> **o projektu** \> **prodaje** i izaberite ugovor o projektu.
4. U oknu za radnje izaberite stavku Faktura **da** biste generisali fakturu kupca.
5. U oblasti "Finansije" idite na prozor **Upravljanje projektima i računovodstvo** \> **Periodični** \> **uvoz iz pripremne tabele** i kliknite na dugme U **redu** da biste generisali nalog za integraciju operacija projekta.
6. Idite na **predlog projektnog menadžmenta** \> **i knjigovodstvenih** \> **faktura projekta** i **izaberite stavku Proknjiži** da biste proknjižili predlog fakture koji je generisan za projekat.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Ažurirajte uplatu klijenta i platite prodavcu

Kada dobavljač dovrši svoj rad na projektu i pošalje vam fakturu, morate pregledati status projekta i fakture kupaca da biste utvrdili da li su ispunjeni uslovi PWP projekta. Ako su ispunjeni uslovi za PWP za dobavljača, možete da odredite koje redove na fakturi dobavljača treba da platite na osnovu uplata klijenata za projekat. Ako odlučite da platite prodavcu iako uslovi za PWP nisu ispunjeni, možete zameniti uslove za PWP na stranici **Faktura prodavca sa plaćanjem nakon uplate**.

1. U okviru Finansije idite na **Project management i knjigovodstvene** \> **·** \> **projekte** Svi projekti i izaberite projekat.
2. U oknu za radnje izaberite **stavku Kontrola**, a zatim izaberite **fakture dobavljača** da biste prikaželi sve fakture dobavljača koje su generisane za projekat.
3. Na stranici **Faktura prodavca sa plaćanjem nakon uplate**, u polje za pretragu unesite vrednosti da biste pronašli fakturu dobavljača koju želite da pregledate, a zatim izaberite **Pretraga**.
4. Izaberite opciju **Plati kada se** plati da biste prikazali samo PWP fakture.
5. Na brzoj **kartici Redovi fakture** dobavljača izaberite redove koje želite da oslobodite za plaćanje.
6. Izaberite uplatu **dobavljača za izdavanje**. Opcija **Plaćanje posle uplate** se briše, a vrednost polja **Spremno za plaćanje** se menja u **Da**.
