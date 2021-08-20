---
title: Kreiranje projektnog tima
description: Ova tema pruža informacije o tome kako da kreirate i upravljate projektnim timovima.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ab8ae045852a75a7a39a4eccfa86a114a34273581c98631975bcbfac5a7a343
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005813"
---
# <a name="create-a-project-team"></a>Kreiranje projektnog tima

[!include [banner](../includes/banner.md)]

Da bi koristio uloge koje su prethodno postavljene u projektu, menadžer projekta mora povezati uloge sa projektom. Za projekat se može dodeliti više uloga. Da bi se sprečila zabuna, ove uloge se automatski označavaju tokom rezervacije. Na primer, ako menadžer projekta zahteva tri softverska inženjera, automatski se generišu tri uloge softverskog inženjera koje imaju oznake **softverski inženjer 1**, **softverski inženjer 2** i **softverski inženjer 3**. Ako su karakteristike uloge prethodno postavljene za ulogu, one se primenjuju kao filter tokom pretraživanja resursa. Dodatne karakteristike se mogu dodati po potrebi za dalje preciziranje pretrage.

Postavke prikaza takođe se mogu prilagoditi kako bi se dobio bolji prikaz dostupnosti resursa. Postoje opcije za prikazivanje raspoloživosti po satima, dnevno, nedeljno, mesečno, kvartalno i godišnje. Takođe postoji opcija za prikaz raspoloživog i preostalog kapaciteta resursa. Ova opcija je korisna za upravljanje vremenom kada procenjujete dostupno vreme za aktivnosti ili dostupnost resursa.

Menadžer projekta može odabrati ulogu na stranici, a zatim, ako postoji dostupan resurs koji odgovara zahtevima, izaberite da rezervišete resurs za popunjavanje uloge. Imajte na umu da resursi u ovom trenutku ne moraju biti rezervisani u fazi planiranja. Kada kreirate SAP, možete zameniti uloge resursima osoblja za projekat. Ako se uloge zamene resursima osoblja u SAP-u, podešavanje resursa automatski ažurira spisak i raspored projektnog tima.

[![Spisak projektnog tima koji uključuje i uloge i stvarne resurse.](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Menadžer projekta ima razne mogućnosti za rezervaciju resursa za projekat, kao što su **Preostali kapacitet**, **Pun kapacitet**, **Procenat kapaciteta** i **Navedite radno vreme**. Ove opcije rezervacije mogu se otkazati u bilo kom trenutku ako se promene dodeljivanja resursa. Podržane su dve vrste rezervacija:

- **Fiksna rezervacija** – Rezervacija resursa je odobrena i potvrđena za rad na angažovanju tokom određenog vremena.
- **Uslovna rezervacija** – Rezervacije resursa su uslovno podešene za rad na angažovanju tokom određenog vremena.

Sledeća procedura objašnjava kako da kreirate projektni tim.

## <a name="create-a-project-team"></a>Kreiranje projektnog tima

1. Na stranici liste **Svi projekti** izaberite projekat, a zatim izaberite **Uredi**.
2. Na kartici **Projektni tim i raspoređivanje**, u polje **Datum završetka rasporeda** unesite datum početka rasporeda uvećan za jedan mesec. Na primer, ako je datum početka rasporeda 24. jun 2017. (24.6.2017), Unesite **24.07.2017**.
3. Izaberite **Dodaj**.
4. U oknu **Dodavanje uloga u projekat**, u polju **Uloga** izaberite **Viši menadžer projekta**.
5. Izaberite **Potrebne kompetencije**.
6. Na stranici **Odaberite karakteristike**, karakteristike koje ste prethodno postavili za ulogu višeg menadžera projekta su podrazumevano izabrane. Izaberite **U redu**.
7. Na stranici **Dodavanje uloge projektu**, u polju **Broj resursa** unesite **1**.
8. U polju **Resurs**, pregled prikazuje sve resurse koji imaju potrebne kompetencije. Izaberite **Danijel Goldšmit**, a zatim izaberite **Kreiraj**.
9. Na stranici **Projekat** izaberite **Dodaj**.
10. U oknu **Dodavanje uloga u projekat**, u polju **Uloga** izaberite **Član tima**. U polje **Broj resursa** unesite **5**.
11. Izaberite **Kreiraj**.
12. Na stranici **Projekti**, izaberite **Popuni resurs**.

## <a name="monitor-project-teams"></a>Nadgledajte projektne timove
1. Na stranici **Svi projekti**, izaberite vezu **ID projekta** za projekat **Nadogradnja XYZ faza 2**.
2. Na brzoj kartici **Projektni tim i zakazivanje**, uverite se da su navedeni resursi projekta tačni.


[!INCLUDE[footer-include](../includes/footer-banner.md)]