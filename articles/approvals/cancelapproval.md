---
title: Otkazivanje odobravanja prethodno odobrenih stavki
description: Ovaj članak sadrži objašnjenja o tome kako menadžer projekta može da otkaže odobravanje prethodno odobrenih stavki vremena, troškova ili korišćenja materijala.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 08c2248a5fcfc9b7569871a76bc09234ffd172c7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930473"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Otkazivanje odobravanja prethodno odobrenih stavki

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Menadžer projekta ili osoba koja vrši odobravanje koja je prethodno odobrila stavke vremena, troškova ili korišćenja materijala može da otkaže odobravanje tih stavki. 

Sledite ove korake da biste otkazali odobravanje prethodno odobrenog vremena, troškova ili stavke korišćenja materijala.

1. Idite na **Projekti** \> **Moj posao** \> **Odobrenja**.
2. Stranica **liste "** Odobrenja" prikazuje sve stavke vremena koje čekaju na odobravanje. Promenite prikaz u Moja **prethodna odobrenja**.
3. Izaberite vreme, trošak ili odobrenja materijala za otkazivanje. Zatim u oknu za radnje izaberite stavku Otkaži **odobravanje**.
4. U okviru za potvrdu poruke koji će se pojaviti kliknite na dugme U **redu** da biste potvrdili operaciju.

> [!IMPORTANT]
> Ne možete otkazati odobravanje prethodno odobrenog vremena, troškova i stavke korišćenja materijala koja je već fakturisana kupcu. Ako pokušate, dobićete poruku u kojoj se navodi da odobravanje ne može biti otkazano jer je već fakturisano. U tom slučaju, odobrenje možete otkazati samo ako se korektivna faktura koristi za izdavanje kompletnog kredita ili povraćaja novca kupcu u originalnoj fakturi.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Uticaj otkazivanja odobravanja prethodno odobrene stavke

Kada se odobrenje otkaže, postoji i operativni i finansijski uticaj.

### <a name="operational-impact"></a>Operativni uticaj

Ako je odobravanje stavke otkazano, zapis odobravanja je označen kao **prosleđen**. Status stavke se menja u **Prosleđeno**. U ovoj fazi, član projektnog tima može da opozove stavku bez podnošenja zahteva za opoziv.

Osoba koja vrši odobravanje može da promeni **vrednosti količine za fakturisanje** **i vrste** naplate, a zatim da odobri stavku još jednom.

### <a name="financial-impact"></a>Finansijski uticaj

Ako je odobravanje stavke otkazano, odgovarajuće stvarne stvari za trošak i prodaju ažuriraju se na sledeći način:

- Polje **Status poravnanja** se ažurira na **Poravnato**.
- Polje **Status naplate** se ažurira na **Otkazano**.

Zatim, stavke storniranja se kreiraju u tabeli Stvarne vrednosti. Da bi sistem kreirao stavke storniranja, kopira vrednosti polja iz originalnih stvarnih vrednosti. Jedine vrednosti koje se ne kopiraju su vrednosti količine. Umesto toga, ove vrednosti se storniraju. Stornirane stvarne vrednosti se kreiraju za stvarne vrednosti **Troškovi** i **Nenaplaćena prodaja**. Polje **Status poravnanja** u storniranim stvarnim vrednostima je podešeno na **Ne može da se poravna**, a polje **Status naplate** na **Otkazano**. Zbog ovih izmena, evidentirana potrošnja za projekat i preostali prihod od projekta više neće uzimati u obzir iznose koje ove stvarne vrednosti predstavljaju.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
