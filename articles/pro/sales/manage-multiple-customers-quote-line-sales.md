---
title: Upravljanje većim brojem klijenata u stavkama ponude zasnovane na projektu – jednostavno
description: Ova tema opisuje kako se upravlja sa više klijenata u stavkama ponuda zasnovanim na projektu.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d015e9107741fd496f7d3639731f33fcdcc9b9bdd5f501c9ad2617e37a707f35
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001718"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines---lite"></a>Upravljanje većim brojem klijenata u stavkama ponude zasnovane na projektu – jednostavno

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Stavke ponude zasnovane na projektu podržavaju scenarije gde svaka stavka ponude ima listu klijenata koji je plaćaju. Ova lista klijenata na stavci ponude zasnovane na projektu može biti ista kao lista klijenata na ponudi. Možete i da promenite listu klijenata da bude drugačija. Kada se ostvari ponuda za projekat, lista klijenata na stavci ponude zasnovane na projektu se kopira u odgovarajući predmet ugovora zasnovan na projektu da bi se kreirao eventualni ugovor o projektu. Klijenti na osnovu ponude zasnovane na projektu kopiraju se u ugovor za projekat.

Kada fakturišete eventualni ugovor za projekat, lista klijenata u predmetu ugovora zasnovanog na projektu ima prioritet nad listom u ugovoru za projekat. Lista klijenata na projektnom ugovoru koristi se samo za podrazumevana podešavanja na novim predmetima ugovora o projektu.

Svi klijenti ponude na kartici **Klijenti** ponude za projekat podrazumevano su klijenti stavke ponude u svakoj novoj stavci ponude zasnovane na projektu kreiranoj za ponudu za projekat. Sve postojeće stavke ponude zasnovane na projektu ne nasleđuju nove zapise klijenata ponude kreirane nakon njih.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Kreiranje, ažuriranje ili brisanje zapisa klijenta stavke ponude

Možete da kreirate, ažurirate ili izbrišete klijenta stavke ponude na kartici **Klijenti stavke ponude** na stranici **Stavka ponude zasnovana na projektu**. Kada dodate novog klijenta na stavci ponude zasnovane na projektu, klijent se takođe dodaje u ukupnu ponudu kao klijent ponude, sa podrazumevanim procentom podele naplate na ukupnoj ponudi od 0%. Procenat podele naplate na celokupnoj ponudi kopira se u nove redove ponuda i na eventualni ugovor za projekat. Međutim, prilikom fakturisanja iz ugovora koristi se procenat podele naplate na nivou stavke ponude, a ne procenat podele naplate na ukupnom nivou ugovora. 

Sledeća tabela prikazuje polja u zapisu klijenta stavke ponude u stavci ponude zasnovane na projektu.

| Polje | Lokacija | Opis i smernice | Posledični uticaj |
| --- | --- | --- | --- |
| **Poslovni kontakt** | Mreža za uređivanje na kartici **Klijenti stavke ponude**, glavni obrazac i obrasci za brzo kreiranje za klijenta na stavci ponude. | Navodi sve aktivne naloge. Ovo polje se zaključava nakon kreiranja zapisa. Ako treba da ažurirate polje, izbrišite i ponovo napravite zapis. Ako ste evidentirali bilo koju stvarnu vrednost, ne možete izbrisati zapis. | Kada odaberete poslovni kontakt sa glavne liste poslovnih kontakata koji želite da dodate, klijent na stavci ponude se takođe dodaje kao klijent na ponudi kada ga sačuvate. Kada se ponuda ostvari, klijenti na stavkama ponude kopiraju se u klijente na predmetima ugovora. |
| **Procenat deljenja naplate** | Mreža za uređivanje na kartici **Klijenti stavke ponude**, glavni obrazac i obrasci za brzo kreiranje za klijenta na stavci ponude. | Predstavlja procenat svake nenaplaćene prodajne transakcije koja će biti pripisana ovom klijentu stavke ponude. | Kopira se u klijente predmeta ugovora za projekat. |
| **Ograničenje koje ne sme da se prekorači** | Mreža za uređivanje na kartici **Klijenti stavke ponude**, glavni obrazac i obrasci za brzo kreiranje za klijenta na stavci ponude. | Označava da li postoji ugovoreno ograničenje ili gornje ograničenje ukupnog iznosa koji će se fakturisati ovom klijentu za ovu stavku ponude. | Kopira se u klijente predmeta ugovora o projektu kada se ponuda ostvari. |
| **Da li se zaokružuje** | Mreža za uređivanje na kartici **Klijenti stavke ponude**, glavni obrazac i obrasci za brzo kreiranje za klijenta na stavci ponude. | Označava da li je ovaj klijent podrazumevani klijent za zaokruživanje za ovu stavku ponude zasnovane na projektu. | Kopira se u klijente ugovora o projektu kada se ponuda ostvari. |

## <a name="edit-billing-split-percentages"></a>Uređivanje procenata podele naplate

Procente podele naplate možete urediti iznutra. Kada procenti podele naplate ne iznose 100%, dolazi do greške. Kada uređujete procente podele naplate, osvežite stranicu stavke ponude da biste uklonili grešku.

Koristite radnju ravnomerne raspodele na podformi klijenata stavke ponude da biste dodelili podele naplate svim klijentima stavke ponude. Ako postoji faktor zaokruživanja, to će se dodati klijentu za zaokruživanje. Jedan od klijenata stavke ponude uvek je označen kao klijent za zaokruživanje, što znači da je u zapisu klijenta stavke ponude zastavica za zaokruživanje podešena na **Da**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]