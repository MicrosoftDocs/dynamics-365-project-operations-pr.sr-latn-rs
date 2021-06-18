---
title: Mapiranje projekata i zadataka na stavku ponude zasnovane na projektu
description: Ova tema pruža informacije o tome kako da mapirate projekte i zadatke u predmet zadatka zasnovanog na projektu.
author: rumant
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d1c98d6a903393a0afc0e94d7f9859d55b9dc1f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994603"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a>Mapiranje projekata i zadataka na stavku ponude zasnovane na projektu

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

U stavkama ponude zasnovane na projektu možete mapirati određene zadatke projekta koji je već povezan sa stavkom ponude.

Kada mapirate zadatke u stavku ponude, sledeće stavke koje ste definisali u stavci ponude primenjivaće se samo na te zadatke:

- Način naplate
- Opcije naplativosti
- Ograničenja koja ne smeju da se prekorače
- Klijenti

Na primer, možda imate projekat gde je jedna faza fiksna cena, a sve ostale faze su vreme i materijali. U tom slučaju, prvu fazu i sve njene podređene zadatke možete povezati sa stavkom ponude za tu fazu metodom obračuna sa fiksnom cenom. Zatim možete povezati sve ostale faze sa stavkom ponude zasnovanom na vremenu i materijalima.

## <a name="associate-tasks-to-project-based-quote-lines"></a>Povezivanje zadataka sa stavkama ponude zasnovanim na projektu

Zadatke možete povezati sa stavkama ponude sa sledećih lokacija:

- Stranica **Projekat** > kartica **Obračun zadataka** (optimalno)
- Stranica **Stavka ponude** > kartica **Zadaci koji se naplaćuju** 

### <a name="from-the-project-page"></a>Sa stranice Projekat

Stranica **Projekat** pruža optimalno iskustvo za povezivanje zadataka sa stavkama ponude. Ovu stranicu možete koristiti za izbor više zadataka i povezivanje svih njih, kao i njihovih podređenih zadataka, u izabranu stavku ponude.

1. Na kartici **Opšti podaci** stavke ponude zasnovane na projektu, proverite da li je polje **Projekat** popunjeno.
2. U polju **Uključeni zadaci** izaberite **Samo izabrani zadaci**.
3. Sačuvajte stavku ponude zasnovanu na projektu. Kada se obrazac osveži, prikazaće se kartica **Zadaci koji se naplaćuju**.
4. Na kartici **Opšti podaci** izaberite vezu za polje **Projekat**.
5. Na stranici **Projekat** izaberite karticu **Obračun zadataka**.
6. U drugoj mreži, koja se odnosi na podešavanje obračuna za određeni zadatak, izaberite jedan ili više zadataka, a zatim izaberite **Povezivanje stavki ponude**.
7. Na stranici dijaloga koja se pojavi, izaberite stavku ponude koja prikazuje stavke ponude zasnovane na projektu u ponudi.
8. U polju **Tip obračuna**, naznačite da li su ovi zadaci naplativi ili nenaplativi.
9. Označite polje za potvrdu da biste naznačili da li povezivanje treba da sadrži podređene zadatke izabranih zadataka. Ako označite to polje, povezaćete podređene zadatke izabranih zadataka sa stavkom ponude.
10. Izaberite **U redu** da biste zatvorili dijalog.

### <a name="from-the-quote-line-page"></a>Sa stranice Stavka ponude

Projektne zadatke možete povezati sa stavkama ponude sa kartice **Zadaci koji se naplaćuju** na stranici **Ponuda**.

>[!NOTE]
>Optimalno mesto za povezivanje projektnih zadataka sa stavkama ponude je na kartici **Obračun zadataka** na stranici **Projekat**. Ako povežete zadatke sa kartice **Zadaci koji se naplaćuju** na stranici **Stavka ponude**, svaki projekat morate ručno povezati.

1. Na kartici **Opšti podaci** stavke ponude zasnovane na projektu, proverite da li je izabran projekat u polju **Projekat**.
2. U polju **Uključeni zadaci** izaberite **Samo izabrani zadaci**.
3. Sačuvajte stavku ponude zasnovanu na projektu. Kada se obrazac osveži, prikazaće se kartica **Zadaci koji se naplaćuju**.
4. Na kartici **Zadaci koji se naplaćuju**, izaberite **Dodaj zadatak stavke ponude**.
5. Na stranici **Zadatak stavke ponude**, u polju **Zadaci** izaberite zadatak i u polju **Tip obračuna** izaberite **Sačuvaj**. 
6. Zatvorite stranicu. Izabrani zadatak je sada povezan sa stavkom ponude.

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a>Prekidanje veze zadataka sa stavkama ponude zasnovanim na projektu

### <a name="from-the-project-page"></a>Sa stranice Projekat

Ovaj metod pruža optimalno iskustvo za prekidanje veze zadataka sa stavkama ponude. Možete izabrati više zadataka i prekinuti vezu svih njih, kao i njihovih podređenih zadataka, sa izabranom stavkom ponude.

1. Na kartici **Opšti podaci** stavke ponude zasnovane na projektu, u polju **Projekat** izaberite vezu ka projektu.
2. Na stranici **Projekat** izaberite karticu **Obračun zadataka**.
3. U drugoj mreži, koja se odnosi na podešavanje obračuna za određeni zadatak, izaberite jedan ili više zadataka, a zatim izaberite **Prekidanje veze sa stavkama ponude**.
4. Na stranici dijaloga koja se pojavi, izaberite stavku ponude.
5. Označite polje za potvrdu da biste naznačili da li povezivanje treba takođe da se ukloni iz podređenih zadataka izabranih zadataka. Ako označite to polje, prekinućete vezu podređenih zadataka izabranih zadataka sa stavkom ponude.
6. Izaberite **U redu**. Poruka upozorenja vas obaveštava da ako uklonite ovo povezivanje, sve stvarne vrednosti prethodno evidentirane u zadatku mogu da se opozovu. 
7. Izaberite **U redu** da bi se nastavilo i uklanjalo povezivanje između zadatka i stavke ponude zasnovane na projektu.

### <a name="from-the-quote-line-page"></a>Sa stranice Stavka ponude

Vezu projektnih zadataka sa stavkama ponude takođe možete prekinuti sa kartice **Zadaci koji se naplaćuju** na stranici **Ponuda**.

1. Na kartici **Zadaci koji se naplaćuju**, izaberite **Izbriši zadatak stavke ponude**.
2. Izaberite **U redu**. Poruka upozorenja vas obaveštava da ako uklonite ovo povezivanje, sve stvarne vrednosti prethodno evidentirane u zadatku mogu da se opozovu. 
3. Izaberite **U redu** da bi se nastavilo i uklanjalo povezivanje između zadatka i stavke ponude zasnovane na projektu.

>[!NOTE]
> Ovaj postupak ne briše zadatak iz projekta. Samo uklanja povezivanje zadatka sa stavke ponude zasnovane na projektu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]