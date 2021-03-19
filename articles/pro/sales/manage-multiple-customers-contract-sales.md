---
title: Upravljanje sa više klijenata na ugovorima za projekat – jednostavno
description: Ova tema pruža informacije o upravljanju većim brojem klijenata na ugovorima zasnovanim na projektu.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c9804c77cc0931352b026f15fd764f43361757f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273170"
---
# <a name="manage-multiple-customers-on-project-contracts---lite"></a>Upravljanje sa više klijenata na ugovorima za projekat – jednostavno

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Ugovori za projekat u usluzi Dynamics 365 Project Operations podržavaju scenario kada ugovor obuhvata više klijenata koji finansiraju pogodbu. Kartica **Rezime** na stranici **Ugovor o projektu** uključuje polje **Klijent**. Ovo polje identifikuje primarnog klijenta pogodbe. Drugi klijenti za pogodbu mogu se podesiti na kartici **Klijenti** na stranici **Ugovor o projektu**.

Svi klijenti za ugovor navedeni u ugovoru za projekat podrazumevaju se kao klijenti predmeta ugovora na svim novim predmetima ugovora zasnovanim na projektu koji su kreirani za ugovor o projektu. Postojeći predmeti ugovora zasnovani na projektu ne nasleđuju nove klijente za ugovor dok se kreiraju novi zapisi.

Predmeti ugovora zasnovani na proizvodu automatski se povezuju sa primarnim klijentom.

Klijenti ugovora i klijenti predmeta ugovora mogu se dodati, ažurirati ili izbrisati u bilo kom trenutku pre dobijanja ugovora.

## <a name="primary-customer"></a>Primarni klijent

Klijent naveden na kartici **Rezime** ugovora za projekat kao potencijalni klijent je primarni klijent ugovora. Kada pokušate da izbrišete primarnog klijenta sa liste klijenata na ugovoru, dobićete poruku o grešci da zapis primarnog klijenta na ugovoru ne možete izbrisati.

Primarni klijent se ne može ažurirati sa liste klijenata za ugovor. Umesto toga, promenite potencijalnog klijenta na kartici **Rezime** ugovora. Kada se ovo polje ažurira na stranici **Rezime ugovora**, novi klijent se dodaje kao novi klijent za ugovor sa podešenom zastavicom **Primarni**. Prethodni primarni klijent će i dalje će biti klijent za ugovor.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Kreiranje, ažuriranje ili brisanje zapisa klijenta za ugovor

Klijent za ugovor može biti kreiran, ažuriran ili izbrisan iz kartice **Klijenti** na stranici **Ugovor o projektu**. Polja u sledećoj tabeli nalaze se u zapisu klijenta za ugovor na ugovoru za projekat i to treba da imate na umu dok radite sa ugovorom.

| Polje | Lokacija | Opis | Posledični uticaj |
| --- | --- | --- | --- |
| **Poslovni kontakt** | Mreža koja može da se uređuje na kartici **Klijenti ugovora**, **glavni obrazac** i **obrazac za brzo kreiranje** za klijenta za ugovor. | Navodi sve aktivne naloge. Ovo polje se zaključava nakon kreiranja zapisa. Da biste ažurirali poslovni kontakt, izbrišite zapis i napravite novi. Ako ste evidentirali bilo koje stvarne podatke ili ako je zapis klijenta za ugovor primarni klijent, ne možete izbrisati zapis. | Klijenti za ugovor se kopiraju kao klijenti iz predmeta ugovora kada se kreira predmet ugovora. |
| **Procenat deljenja naplate** | Mreža koja može da se uređuje na kartici **Klijenti ugovora**, **glavni obrazac** i **obrazac za brzo kreiranje** za klijenta za ugovor. | Predstavlja procenat svake nenaplaćene prodajne transakcije koja će biti pripisana ovom klijentu predmeta ugovora. | Prekopirano na nove predmete ugovora i na klijente predmeta ugovora za projekat na novim predmetima ugovora za projekat. |
| **Ime ugovora za fakturisanje** | Mreža koja može da se uređuje na kartici **Klijenti ugovora**, **glavni obrazac** i **obrazac za brzo kreiranje** za klijenta za ugovor. | Ovo tekstualno polje treba da se koristi za identifikaciju osobe za kontakt na fakturi za ovog klijenta. Ovo polje dobija podrazumevanu vrednost iz odgovarajućeg zapisa poslovnog kontakta. | Prekopirano u polje **Ime kontakta za fakturisanje** na fakturi koji se generiše za ovog klijenta. |
| **Ime fakturisanja** | Mreža koja može da se uređuje na kartici **Klijenti ugovora**, **glavni obrazac** i **obrazac za brzo kreiranje** za klijenta za ugovor | Ovo tekstualno polje treba da se koristi za identifikaciju osobe za kontakt na fakturi za ovog klijenta. Ovo polje dobija podrazumevanu vrednost iz odgovarajućeg zapisa poslovnog kontakta. | Prekopirano u polje **Ime kontakta za fakturisanje** na fakturi koji se generiše za ovog klijenta. |
| **Uslovi isplate** | Mreža koja može da se uređuje na kartici **Klijenti ugovora**, **glavni obrazac** i **obrazac za brzo kreiranje** za klijenta za ugovor. | Vrednosti se podrazumevano dobijaju iz odgovarajućeg zapisa poslovnog kontakta. | Prekopirano u polje **Ime kontakta za fakturisanje** na fakturi koji se generiše za ovog klijenta. |
| **Da li je zaokruživanje** | Mreža koja može da se uređuje na kartici **Klijenti ugovora**, **glavni obrazac** i **obrazac za brzo kreiranje** za klijenta za ugovor. | Označava da li je ovaj klijent podrazumevani klijent za zaokruživanje za ovu pogodbu. Na ugovoru za projekat može biti samo jedan klijent za zaokruživanje. | Kada deljenje troškova i nenaplaćene količine dovede do razlike u zaokruživanju, ta razlika se primenjuje na stvarnu vrednost koja se mapira na ovog klijenta. |
| **Ograničenje koje ne sme da se prekorači** | Mreža koja može da se uređuje na kartici **Klijenti ugovora**, **glavni obrazac** i **obrazac za brzo kreiranje** za klijenta za ugovor | Označava da li postoji dogovoreno ograničenje ili gornje ograničenje ukupnog iznosa koji će se fakturisati ovom klijentu za ovo angažovanje. | Podešavanje **Ograničenje koje ne sme da se prekorači** na nivou klijenta za ugovor ocenjivaće se u **stvarnim vrednostima nenaplaćene prodaje** koji upućuju na ovog klijenta za ugovor. |

## <a name="edit-billing-split-percentages"></a>Uređivanje procenata podele naplate

Procenti podele naplate se mogu uređivati pomoću iskustva direktnog uređivanja u mreži. Kada procenti podele naplate ne budu iznosili 100 procenata, dobićete grešku. Kada uredite procente podele naplate, osvežite stranicu da biste odbacili grešku.

Takođe možete izabrati **Ravnomerno raspoređivanje** na podformi **Klijenti za ugovor** da biste ravnomerno rasporedili podelu naplate na sve klijente za ugovor. Ako postoji faktor zaokruživanja, on će se dodati klijentu za zaokruživanje. Jedan od klijenata za ugovor je uvek označen kao klijent za **zaokruživanje**, što znači da je u zapisu klijenta za ugovor zastavica zaokruživanja postavljena na **Da**. To je obično primarni klijent za ugovor, ali to se može promeniti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]