---
title: Kako da „uslovno rezervišete“ resurse u aplikaciji u verziji 2.x?
description: U ovom članku opisano je kako da uslovno rezervišete članove projektnog tima uz pomoć programa Project Service.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: d7eb9e3baea3c3f696845905a2522940d14bba8a8d42917f8fe1b90c7c443747
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993933"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a>Kako da „uslovno rezervišem“ resurse u veb aplikaciji (aplikacija Project Service u verziji v2.x)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Uslovno možete da rasporedite ili „uslovno rezervišete“ resurs u projektni tim kako biste prikazali da nameravate da dodelite resurs projektu. Uslovne rezervacije ne troše dostupni kapacitet resursa. Uslovno rezervisani članovi tima ne mogu biti dodeljeni projektnim zadacima. Samo resursi koji imaju status Fiksno rezervisani i tip primene Primenjeno mogu biti dodeljeni zadacima (pod pretpostavkom da imaju dovoljno fiksno rezervisanih radnih časova da pokriju angažovanje za dodelu).

Uslovno rezervisani članovi tima se prikazuju u koordinatnoj mreži Član tima sa uslovno rezervisanim časovima prikazanim u koloni Uslovno rezervisanje. Prikazuju se i na tabeli rasporeda. Ponovo, oni ne označavaju nikakvo korišćenje kapaciteta, jer uslovno rezervisanje ne koristi kapacitet resursa.

Postoje tri načina da uslovno rezervišete člana tima za projekat pomoću programa Project Service u verziji 2.x. Možete uslovno da rezervišete sa tabelom rasporeda, da koristite funkciju Održavanje rezervacija ili da kreirate generički resurs. Ovi načini su opisani u nastavku.

## <a name="soft-book-with-the-schedule-board"></a>Uslovno rezervisanje sa tabelom rasporeda

Da biste uslovno rezervisali pomoću tabele rasporeda, pratite ovu proceduru: 
1. Otvorite tabelu rasporeda.
2. Izaberite karticu Projekat na dnu table Zahtevi za rezervaciju u okviru table rasporeda.
3. Pronađite projekat za koji želite da uslovno rezervišete resurs. Ako imate više projekata, kliknite na zaglavlje kolone Projekat, a zatim pronađite svoj projekat pomoću filtera.
4. Kliknite na projekat, a zatim ga prevucite na koordinatnu mrežu vremena resursa.
5. To otvara tablu Kreiranje rezervacije resursa sa desne strane. Podesite datume početka i završetka, izaberite Status rezervacije kao Uslovna i podesite časove. 
6. Kliknite na Rezerviši.
7. Natrag na projektu, resurs će se sada prikazivati kao član tima sa uslovno rezervisanim časovima u koloni Uslovno rezervisanje.

Imajte na umu da ne možete da ih dodelite zadacima u strukturnoj analizi posla (SAP) jer resursi moraju da budu fiksno rezervisani za tim da bi bili dodeljeni.

## <a name="soft-book-using-the-maintain-bookings-feature"></a>Uslovno rezervisanje korišćenjem funkcije Održavanje rezervacija

Da biste uslovno rezervisali pomoću Održavanja rezervacija, pratite ovu proceduru:
1. Sa mreže člana tima, kliknite na Novi.
2. Izaberite resurs koji je moguće rezervisati, ulogu, od/do.
3. Izaberite način dodele koji nije Nijedno:
- Puni kapacitet
- Kapacitet u procentima
- Ravnomerno raspoređivanje po satima
- Početno opterećenje po časovima
4. Kliknite na dugme Sačuvaj. Videćete resurs na mreži tima, a njegove časove označene kao Fiksni.
5. Održite rezervacije resursa klikom na Održavanje rezervacija.
6. Kada se otvori tabela rasporeda, razvijte resurs da biste prikazali njegove rezervacije. Videćete rezervaciju označenu kao „Fiksna“.
7. Kliknite desnim tasterom miša na rezervaciju, u okviru opcije „Promena statusa“, izaberite „Uslovno rezerviši“ i zatim „Uslovno“. Status rezervacije je sada „Uslovno“.
8. Nakon zatvaranja tabele rasporeda, videćete da su časovi za resurs promenjeni iz „Fiksni“ u „Uslovni“ na mreži člana tima.
Imajte u vidu da ako fiksno rezervišete resurs za tim, a zatim mu dodelite zadatke u SAP-u, kada koristite održavanje rezervacija da biste promenili status iz „Fiksna“ u „Uslovna“, uklonićete dodele iz zadataka za taj resurs, jer samo fiksno rezervisani resursi mogu biti dodeljeni zadacima.

## <a name="soft-book-by-creating-a-generic-resource"></a>Uslovno rezervisanje kreiranjem generičkog resursa

Uslovno rezervisanje možete da kreirate generisanjem generičkog člana tima, ispunjavanjem sa tabelom rasporeda ili Zahtevom za resurs i promenom tipa tokom rezervacije.
To možete da uradite pomoću sledeće procedure:

1. U SAP-u projekta dodelite uloge zadacima za koje želite da generišete generičke članove tima.
2. Kliknite na Generisanje projektnog tima.
3. Na mreži člana projektnog tima izaberite generički resurs i kliknite na dugme „Rezerviši“.
4. Na tabeli rasporeda, izaberite resurs koji želite da rezervišete.
5. Na tabli „Kreiranje rezervacije resursa“ tabele rasporeda, promenite Status rezervacije na „Uslovna“.
6. Kliknite na dugme „Rezerviši“ i „Rezerviši i izađi“.

Nakon zatvaranja tabele rasporeda, videćete da je izabrani resurs dodat u tim sa uslovno rezervisanim, kao i sa dodeljenim časovima. Videćete i da generički resurs ostaje u timu kao indikator da su zadaci dodeljeni članu tima koji je uslovno rezervisan.

Kada budete spremni da promenite resurs uslovno rezervisanog člana tima u fiksno rezervisanog člana tima kako biste mogli da mu dodeljujete zadatke, postupite na sledeći način:

1. Izaberite taj resurs i kliknite na dugme „Održavanje rezervacija“.
2. Kada se otvori tabela rasporeda, razvijte resurs da biste prikazali njegove rezervacije. Videćete da je rezervacija označena kao „Uslovna“.
3. Kliknite desnim tasterom miša na rezervaciju, u okviru opcije „Promena statusa“, izaberite „Fiksno rezerviši“ i zatim „Fiksno“. Status rezervacije je sada „Fiksna“.
4. Nakon zatvaranja tabele rasporeda, videćete da su časovi za resurs promenjeni iz „Uslovni“ u „Fiksni“ na mreži člana tima. Sada možete da dodelite resurs zadacima (ukoliko postoji usklađenost između fiksno rezervisanih časova i časova angažovanja zadatka za dodelu). Imajte u vidu da ako ste pratili korake ispunjenja generičkog resursa u stavci br. 3 iznad, kada promenite status uslovno rezervisanog resursa u fiksno rezervisani, generički član tima se uklanja iz tima.


[!INCLUDE[footer-include](../includes/footer-banner.md)]