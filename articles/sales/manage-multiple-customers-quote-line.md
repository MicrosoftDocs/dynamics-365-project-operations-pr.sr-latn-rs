---
title: Upravljanje sa više klijenata u stavkama ponude zasnovane na projektu
description: Ova tema pruža informacije o tome kako da upravljate sa više klijenata u stavkama ponude zasnovane na projektu.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 48336af0ad522e9d6aa68fa82ffa7921f09662d4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118580"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines"></a>Upravljanje sa više klijenata u stavkama ponude zasnovane na projektu

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Stavke ponude zasnovane na projektu podržavaju scenarije gde svaka stavka ponude ima listu klijenata koji je plaćaju. Ova lista klijenata na stavci ponude zasnovane na projektu može biti ista kao lista klijenata na ponudi. Možete i da promenite listu klijenata da bude drugačija. Da bi se kreirao eventualni ugovor za projekat kada se ostvari ponuda za projekat, lista klijenata na stavci ponude zasnovane na projektu se kopira u odgovarajući predmet ugovora zasnovan na projektu. Klijenti na osnovu ponude zasnovane na projektu kopiraju se u ugovor za projekat.

Kada fakturišete eventualni ugovor za projekat, lista klijenata u predmetu ugovora zasnovanog na projektu ima prioritet nad listom u ugovoru za projekat. Lista klijenata na ugovoru za projekat se koristi samo za podrazumevana podešavanja na novim predmetima ugovora za projekat.

Svi klijenti ponude na kartici **Klijenti** ponude za projekat podrazumevano su klijenti stavke ponude u svakoj novoj stavci ponude zasnovane na projektu kreiranoj za ponudu za projekat. Sve postojeće stavke ponude zasnovane na projektu ne nasleđuju nove zapise klijenata ponude kreirane nakon njih.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Kreiranje, ažuriranje ili brisanje zapisa klijenta stavke ponude

Možete da kreirate, ažurirate ili izbrišete klijenta stavke ponude na kartici **Klijenti stavke ponude** na stranici **Stavka ponude zasnovana na projektu**. Kada dodate novog klijenta na stavci ponude zasnovane na projektu, klijent se takođe dodaje u ukupnu ponudu kao klijent ponude, sa podrazumevanim procentom podele naplate na ukupnoj ponudi od 0%. Procenat podele naplate na celokupnoj ponudi kopira se u nove redove ponuda i na eventualni ugovor za projekat. Međutim, kada fakturišete iz ugovora, koristi se procenat podele naplate na nivou stavke ponude, a ne procenat podele naplate na ukupnom nivou ugovora. 

Sledeća tabela prikazuje polja u zapisu klijenta stavke ponude u stavci ponude zasnovane na projektu.

| Polje | Lokacija | Opis i smernice | Posledični uticaj |
| --- | --- | --- | --- |
| **Poslovni kontakt** | Mreža za uređivanje na kartici **Klijenti stavke ponude**, glavni obrazac i obrazac za brzo kreiranje za klijenta na stavci ponude. | Navodi sve aktivne naloge. Ovo polje se zaključava nakon kreiranja zapisa. Ako treba da ažurirate polje, izbrišite i ponovo napravite zapis. Ako ste evidentirali bilo koju stvarnu vrednost, ne možete izbrisati zapis. | Kada odaberete poslovni kontakt sa glavne liste poslovnih kontakata koji želite da dodate, klijent na stavci ponude se takođe dodaje kao klijent na ponudi. Klijenti na stavkama ponude kopiraju se u klijente na predmetima ugovora kada se ponuda ostvari. |
| **Procenat deljenja naplate** | Mreža za uređivanje na kartici **Klijenti stavke ponude**, glavni obrazac i obrazac za brzo kreiranje za klijenta na stavci ponude. | Predstavlja procenat svake nenaplaćene prodajne transakcije koja će biti pripisana ovom klijentu stavke ponude. | Kopira se u klijente predmeta ugovora za projekat. |
| **Ograničenje koje ne sme da se prekorači** | Mreža za uređivanje na kartici **Klijenti stavke ponude**, glavni obrazac i obrazac za brzo kreiranje za klijenta na stavci ponude. | Označava da li postoji ugovoreno ograničenje ili gornje ograničenje ukupnog iznosa koji će se fakturisati ovom klijentu za ovu stavku ponude. | Kopira se u klijente predmeta ugovora o projektu kada se ponuda ostvari. |
| **Preduzeće-vlasnik** | Mreža za uređivanje na kartici **Klijenti stavke ponude**, glavni obrazac i obrazac za brzo kreiranje za klijenta na stavci ponude, | Pravno lice u kojem je klijent podešen u modulu **Upravljanje projektima i računovodstvo**. Ovo polje je samo za čitanje i postavljeno je za preduzeće-vlasnika same ponude. Lista klijenata koje treba dodati u polju **Poslovni kontakt** već je filtrirana u listu iz preduzeća-vlasnika u modulu **Upravljanje projektima i računovodstvo** usluge Project Operations. | Preduzeće-vlasnik se izjednačava sa pojmom pravnog lica. Svi troškovi i prihodi koji nastaju od ovog projekta evidentiraju se u glavnoj knjizi preduzeća-vlasnika. |
| **Da li se zaokružuje** | Mreža za uređivanje na kartici **Klijenti stavke ponude**, glavni obrazac i obrazac za brzo kreiranje za klijenta na stavci ponude. | Označava da li je ovaj klijent podrazumevani klijent za zaokruživanje za ovu stavku ponude zasnovane na projektu. | Kopira se u klijente ugovora o projektu kada se ponuda ostvari. |

## <a name="edit-billing-split-percentages"></a>Uređivanje procenata podele naplate

Procente podele naplate možete urediti iznutra. Kada procenti podele naplate ne iznose 100%, dolazi do greške. Kada uređujete procente podele naplate, osvežite stranicu stavke ponude da biste uklonili grešku.

Koristite radnju ravnomerne raspodele na podformi klijenata stavke ponude da biste dodelili podele naplate svim klijentima stavke ponude. Ako postoji faktor zaokruživanja, to će se dodati klijentu za zaokruživanje. Jedan od klijenata stavke ponude uvek je označen kao klijent za zaokruživanje, što znači da je u zapisu klijenta stavke ponude zastavica za zaokruživanje podešena na **Da**. 
