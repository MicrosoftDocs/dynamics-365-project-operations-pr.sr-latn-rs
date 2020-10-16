---
title: Model bezbednosti
description: Ova tema pruža informacije o modelu bezbednosti u usluzi Dynamics 365 Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ffcfa8a9c8e31c5665acd3c3919fa90d36a3f3ca
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896748"
---
# <a name="security-model"></a>Model bezbednosti

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Microsoft Dynamics 365 Project Operations sadrži jedinstveni model bezbednosti koji omogućava poslovni model bezbednosti zasnovan na ulogama koji sarađuje sa Microsoft Office grupama. 


## <a name="security-roles"></a>Bezbednosne uloge
Izložene mogućnosti usluge Project Operations uključuju sledeće uloge:

| Uloga                          | Opis                                                                                                                                                                 | Scope |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Menadžer obuke              | Podržava izveštavanje između projekata.                                                                                                            | Poslovna jedinica              |
| Davalac odobrenja za projekat              | Odobrava vreme i troškove u odnosu na projekat.                                                                                                                              | Poslovna jedinica |
| Administrator naplate projekta | Izrađuje predlog fakture.                                                                                                                                                 | Poslovna jedinica |
| Menadžer projekta               | Izrađuje plan projekta i zahteva resurse.                                                                                                                              | Poslovna jedinica |
| Resurs za projekat              | Članovi tima koji mogu da rezervišu i prijave vreme.                                                                                                          | Poslovna jedinica|
| Menadžer resursa              | Sve funkcije upravljanja resursima, poput ispunjavanja zahteva za resursima i rezervacija, razdvojene su da bi podržale hibridnu konfiguraciju menadžera projekata + menadžera resursa i jedinstvenu i centralizovanu ulogu menadžera resursa. | Poslovna jedinica |


Microsoft Project za veb uključuje sledeće uloge:
| Uloga                          | Opis                                                                                                          | Scope |                                                       
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----|
| Korisnik projekta | Korisnik koji sarađuje u programu Project koji može da kreira sopstvene projekte i pregleda sve projekte koji se dele sa njim.| Korisnik|
| Projektni sistem | Uloga koja se koristi za kontekst aplikacije. Klijenti ne bi trebalo da koriste ovu sistemsku ulogu. | Globalni|

## <a name="security-enforcement"></a>Provođenje bezbednosti
Radnje koje se izvode na nivou projekta izvode se u kontekstu prijavljenog korisnika. To znači da je za kreiranje, otvaranje ili brisanje projekta od korisnika potrebno da ima pristup dostupan u CDS-u. Pristup CDS-u se može odobriti putem bilo kog od mogućih mehanizama uključenih u platformu. Na primer, korisnik sa većim opsegom može pristupiti projektu ili ako je izvršena eksplicitna akcija deljenja projekta koja korisniku odobrava pristup.

Važno je to uzeti u obzir prilikom kreiranja projekata u usluzi Project Operations.

## <a name="modern-group-collaboration-with-project-operations"></a>Savremena grupna saradnja sa uslugom Project Operations
Project za veb i Project Operations podržavaju savremene grupe za saradnju. Korisnici dodati u projekat putem grupe mogu da uređuju plan projekta.

Project za veb automatski dodaje korisnike u grupu po dodeljivanju.

Grupe omogućavaju zajednički rad na dozvolama projekta i pratećim artefaktima za saradnju. Sledeći dijagram prikazuje događaje i promene stanja koji se dešavaju tokom procesa grupnog dodeljivanja.

Usluga Project Operations ne kreira grupu implicitnom akcijom, već samo eksplicitnom akcijom pritiska grupa.

Pretraga članova grupe u dijalogu **Upravljanje grupama** ograničena je na one koji su postavljeni kao deo bezbednosne grupe okruženja. Više informacija potražite u članku [Kontrola korisničkog pristupa okruženjima: bezbednosne grupe i licence](https://docs.microsoft.com/power-platform/admin/control-user-access).

1. Projekat se kreira i njegov vlasnik je korisnik koji ga je kreirao.
2. Vlasnik projekta je obavešten o timu.
3. Tim-vlasnik se mapira u navedenu ili kreiranu Office grupu.
4. Prvobitni vlasnik projekta se dodaje u Office grupu.

## <a name="deployment-recommendation"></a>Preporuka za primenu
Kako se model saradnje Office grupe razvija, funkcionalnost će biti dodavana kako bi se pružala detaljnija kontrola tokom vremena. Klijenti koji danas primenjuju Project Operations podstiču se da se usredsrede na tradicionalni Microsoft Dynamics 365 model bezbednosti.

Za više informacija, pogledajte [Bezbednost u usluzi Common Data Service](https://docs.microsoft.com/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Project Operations i Microsoft Dynamics 365 Finance bezbednost
Usluga Project Operations uključuje sledeće uloge:

- Menadžer projekta
- Računovođa projekta

Više informacija o bezbednosti u usluzi Finance potražite u odeljku [Bezbednost zasnovana na ulogama](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).


