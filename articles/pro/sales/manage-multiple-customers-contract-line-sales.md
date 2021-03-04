---
title: Upravljanje većim brojem klijenata u predmetima ugovora zasnovanim na projektu – jednostavno
description: Ova tema pruža informacije o upravljanju većim brojem klijenata na predmetima ugovora zasnovanim na projektu.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f28e7d1363647621f7bd23504aa6d4ea3fc95fc9
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181663"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines---lite"></a>Upravljanje većim brojem klijenata u predmetima ugovora zasnovanim na projektu – jednostavno

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Predmeti ugovora zasnovani na projektu mogu sadržati listu klijenata koji su odgovorni za plaćanje. Ova lista klijenata na predmetu ugovora zasnovanom na projektu može biti ista kao lista klijenata na ugovoru, ali to nije obavezno. Kada se dobije ponuda za projekat i kreira ugovor za projekat, lista klijenata u stavki ponude se kopira u odgovarajući predmet ugovora. Klijenti na ponudi se kopiraju u ugovor.

Kada se fakturiše ugovor o projektu, lista klijenata na predmetu ugovora zasnovanom na projektu ima prioritet nad listom klijenata u ugovoru. Spisak klijenata na ugovoru o projektu koristi se samo za dodelu podrazumevanih vrednosti novim predmetima ugovora.

Svi klijenti za ugovor na kartici **Klijenti** ugovora o projektu podrazumevaju se kao klijenti predmeta ugovora na svim novim predmetima ugovora kreiranim za ugovor o projektu. Nijedan postojeći predmet ugovora neće naslediti nove zapise klijenata ugovora kreirane nakon njih.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Kreiranje, ažuriranje ili brisanje zapisa klijenta iz predmeta ugovora

Možete kreirati, ažurirati ili izbrisati klijenta predmeta ugovora sa kartice Klijenti predmeta ugovora na stranici Predmet ugovora zasnovan na projektu. Kada se novi klijent doda u predmet ugovora zasnovan na projektu, on se takođe dodaje u celokupni ugovor kao klijent ugovora sa podrazumevanim procentom podele naplate od nula procenata. Procenat podele naplate u celokupnom ugovoru kopira se u nove predmete ugovora i u eventualni ugovor o projektu. Međutim, prilikom fakturisanja iz ugovora koristi se procenat podele naplate na nivou predmeta ugovora, a ne procenat podele naplate na ukupnom nivou ugovora.

U nastavku se nalaze polja na zapisu klijenta predmeta **ugovora** za predmet ugovora zasnovan na projektu kako biste imali na umu dok radite sa njim:

| Polje | Lokacija | Opis | Posledični uticaj |
| --- | --- | --- | --- |
| **Poslovni kontakt** | Mreža koja može da se uređuje na kartici **Klijenti ugovora**, **glavni obrazac** i **obrazac za brzo kreiranje** za klijenta ugovora. | Svi aktivni nalozi. Ovo polje se zaključava nakon kreiranja zapisa. Da biste ažurirali polje, izbrišite zapis i napravite novi. Ako ste evidentirali bilo koju stvarnu vrednost, ne možete izbrisati zapis. Međutim, procenat podele naplate možete označiti kao nula za taj nalog. Kada je zapis označen kao nula, to utiče na sve buduće stvarne vrednosti troškova i prihoda koji se pripisuju ili dele ovom klijentu. | Kada odaberete nalog sa glavne liste naloga da biste ga dodali i sačuvali, klijent iz predmeta ugovora se takođe dodaje kao klijent za ugovor. Klijenti predmeta ugovora se koriste kada se generišu fakture. |
| **Procenat deljenja naplate** | Mreža koja može da se uređuje na kartici **Klijenti ugovora**, **glavni obrazac** i **obrazac za brzo kreiranje** za klijenta ugovora. | Ovo polje predstavlja procenat svake nenaplaćene prodajne transakcije koja će biti pripisana ovom klijentu predmeta ugovora. | Klijenti predmeta ugovora i procenti podele naplate koriste se kada se stvarne vrednosti kreiraju nakon odobrenja i kada se generiše faktura. |
| **Ograničenje koje ne sme da se prekorači** | Mreža koja može da se uređuje na kartici **Klijenti ugovora**, **glavni obrazac** i **obrazac za brzo kreiranje** za klijenta ugovora. | Označava da li postoji dogovoreno ograničenje ili gornje ograničenje ukupnog iznosa koji će se fakturisati ovom klijentu za predmet ugovora. | Ograničenje neprekoračenja za klijenta predmeta ugovora koristi se kada se kreiraju stvarne vrednosti i generišu fakture. |
| **Da li je zaokruživanje** | Mreža koja može da se uređuje na kartici **Klijenti ugovora**, **glavni obrazac** i **obrazac za brzo kreiranje** za klijenta predmeta ugovora. | Ovo polje označava da li je ovaj klijent podrazumevani klijent za zaokruživanje za ovaj predmet ugovora zasnovan na projektu. | Kada generišete stvarnu vrednost u skladu sa procentom podele naplate, mogu postojati neke razlike u zaokruživanju. U tom slučaju, razlike u zaokruživanju se pripisuju ovom kupcu. |

## <a name="edit-billing-split-percentages"></a>Uređivanje procenata podele naplate

Procenti podele naplate se mogu uređivati u mreži. Kada procenti podele naplate ne budu iznosili 100 procenata, javiće se greška. Kada uredite procente podele naplate, osvežite stranicu da biste uklonili grešku.

Takođe možete izabrati opciju **Ravnomerno rasporedi** na podformi klijenta predmeta ugovora. Ova radnja ravnomerno raspoređuje podele naplate za sve klijente predmeta ugovora. Ako postoji bilo koji faktor zaokruživanja, on će se dodati klijentu za zaokruživanje. Jedan klijent iz predmeta ugovora uvek je označen kao klijent za **zaokruživanje**, čija zastavica **Zaokruživanje** je postavljena na **Da**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]