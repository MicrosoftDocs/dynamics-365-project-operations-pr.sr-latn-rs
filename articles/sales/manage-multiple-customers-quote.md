---
title: Upravljanje sa više klijenata u ponudama za projekat
description: Ova tema pruža informacije o radu sa ponudama koje uključuju više klijenata koji će finansirati projekat.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8b1d9284c063e34e34ec6525072a1f8f860116b6
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908544"
---
# <a name="manage-multiple-customers-on-project-quotes"></a>Upravljanje sa više klijenata u ponudama za projekat

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Ponude za projekte podržavaju scenario kada predlog uključuje više klijenata koji će finansirati pogodbu. Na kartici **Rezime** ponude nalazi se polje **Potencijalni klijent**, koje identifikuje primarnog klijenta u pogodbi. Drugi klijenti za pogodbu mogu se podesiti na kartici **Klijenti** ponude za projekat.

Svi klijenti ponude na kartici **Klijenti** ponude za projekat podrazumevano su klijenti stavke ponude u svakoj **novoj** stavci ponude zasnovane na projektu kreiranoj za ponudu. Sve postojeće stavke ponude zasnovane na projektu neće naslediti nove zapise klijenata ponude kreirane nakon njih.

Klijenti ponude i klijenti stavke ponude mogu da se dodaju, ažuriraju ili brišu u bilo kom trenutku pre ostvarenja ponude. Važeći klijent u ponudi mora biti podešen kao klijent u preduzeću-vlasniku ili pravnom licu na stranici **Klijenti**. Pravna lica se podešavaju u modulu **Upravljanje projektima i računovodstvo** usluge Dynamics 365 Project Operations i dostupna su kao kompanije u modulima **Projektna prodaja i isporuka** usluge Project Operations.

## <a name="concept-of-a-primary-customer"></a>Koncept primarnog klijenta

Klijent naveden na kartici **Rezime** ponude za projekat kao potencijalni klijent je primarni klijent ponude. Ako pokušate da izbrišete primarnog klijenta sa liste klijenata u ponudi, dobićete grešku da primarni zapis klijenta u ponudi ne može da se izbriše.

Primarni klijent ne bi trebalo da se ažurira sa liste klijenata na ponudi. Međutim, na primarnog klijenta možete uticati promenom potencijalnog klijenta na kartici **Rezime** ponude. Kada se ovo polje ažurira na **rezimeu ponude**, novoizabrani potencijalni klijent se dodaje kao novi klijent ponude sa postavljenom zastavicom **Primarni**. Stari potencijalni klijent i dalje će biti klijent na ponudi.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Kreiranje, ažuriranje ili brisanje zapisa klijenta ponude

Klijent ponude može da se kreira, ažurira ili izbriše na kartici **Klijenti ponude** na stranici **Ponuda**. Polja navedena u sledećoj tabeli nalaze se u zapisu klijenta ponude u ponudi za projekat.

| **Polje** | **Lokacija** | **Relevantnost, svrha i smernice** | **Posledični uticaj** |
| --- | --- | --- | --- |
| Nalog | Mreža podložna uređivanju na kartici **Klijenti ponude** i obrasci **Glavni** i **Brzo kreiranje** za klijenta ponude. | Navodi sve aktivne naloge. Ovo polje se zaključava nakon kreiranja zapisa. Ako želite da ga ažurirate, izbrišite zapis i ponovo ga napravite. Ako ste evidentirali bilo koje stvarne podatke ili ako je zapis klijenta ponude primarni klijent, biće vam dozvoljeno da izbrišete zapis. | Klijenti ponude se kopiraju u klijente stavke ponude kada se kreira stavka ponude. Klijenti ponude se takođe kopiraju u klijente ugovora za projekat kada se ponuda ostvari. |
| Procenat deljenja naplate | Mreža podložna uređivanju na kartici **Klijenti ponude** i obrasci **Glavni** i **Brzo kreiranje** za klijenta ponude. | Predstavlja procenat svake nenaplaćene prodajne transakcije koja će biti pripisana ovom klijentu ponude. | Prekopirano u novokreirane stavke ponude i za projektovanje klijenata ugovora. |
| Ime ugovora za fakturisanje | Mreža podložna uređivanju na kartici **Klijenti ponude** i obrasci **Glavni** i **Brzo kreiranje** za klijenta ponude. | Ovo je tekstualno polje i trebalo bi da se koristi za identifikaciju osobe za kontakt na fakturi za ovog klijenta. One se podrazumevaju iz povezanog zapisa o poslovnom kontaktu | Kopira se u klijente ugovora o projektu kada se ponuda ostvari i pretvara se u polje Ime ugovora za fakturisanje koje se generiše za ovog klijenta. |
| Ime za fakturisanje | Mreža podložna uređivanju na kartici **Klijenti ponude** i obrasci **Glavni** i **Brzo kreiranje** za klijenta ponude. | Ovo tekstualno polje treba da se koristi za identifikaciju osobe za kontakt na fakturi za ovog klijenta. | Kopira se u klijente ugovora o projektu kada se ponuda ostvari i pretvara se u polje **Ime ugovora za fakturisanje** koje se generiše za ovog klijenta. |
| Uslovi plaćanja | Mreža podložna uređivanju na kartici **Klijenti ponude** i obrasci **Glavni** i **Brzo kreiranje** za klijenta ponude. | Ovo je skup opcija sa vrednostima koje se podrazumevaju iz povezanog zapisa naloga. | Kopira se u klijente ugovora o projektu kada se ponuda ostvari i pretvara se u polje **Ime ugovora za fakturisanje** koje se generiše za ovog klijenta. |
| Da li se zaokružuje | Mreža podložna uređivanju na kartici **Klijenti ponude** i obrasci **Glavni** i **Brzo kreiranje** za klijenta ponude. | Označava da li je ovaj klijent podrazumevani klijent za zaokruživanje za ovu pogodbu. | Kopira se u klijente ugovora o projektu kada se ponuda ostvari. |
| Preduzeće-vlasnik | Mreža podložna uređivanju na kartici **Klijenti ponude** i obrasci **Glavni** i **Brzo kreiranje** za klijenta ponude. | Pravno lice čiji je klijent podešen u modulu **Upravljanje projektima i računovodstvo**. Ovo polje je samo za čitanje i postavljeno je za preduzeće-vlasnika same ponude. Lista klijenata koje treba dodati u polju **Poslovni kontakt** već je filtrirana u listu iz preduzeća-vlasnika u modulu **Upravljanje projektima i računovodstvo** usluge Project Operations. | Preduzeće-vlasnik se izjednačava sa konceptom pravnog lica u modulu **Upravljanje projektima i računovodstvo** usluge Project Operations. Svi troškovi i prihodi koji se ostvaruju od ovog projekta evidentiraju se u glavnoj knjizi preduzeća-vlasnika. |
| Ograničenje koje ne sme da se prekorači | Mreža podložna uređivanju na kartici **Klijenti ponude** i obrasci **Glavni** i **Brzo kreiranje** za klijenta ponude. | Označava da li postoji ugovoreno ograničenje ili gornje ograničenje ukupnog iznosa koji će se fakturisati ovom klijentu za ovo angažovanje. | Kopira se u klijente ugovora o projektu kada se ponuda ostvari. |

## <a name="editing-billing-split-percentages"></a>Uređivanje procenta podele naplate

Procente podele naplate možete da uredite koristeći iskustvo unutrašnjeg uređivanja mreže. Kada procenti podele naplate ne iznose 100%, dolazi do greške. Kada ažurirate procente podele naplate, osvežite stranicu da biste uklonili grešku.

Takođe možete pokušati da izaberete opciju **Ravnomerno rasporedi** na podformi klijenata ponude. Ova radnja dodeljuje podele naplate svim klijentima ponude. Ako postoji bilo koji faktor zaokruživanja, to će se dodati klijentu za zaokruživanje. Jedan od klijenata ponude uvek se označava kao klijent za zaokruživanje. to znači da zapis klijenta ponude ima zastavicu **Zaokruživanje** postavljenu na **Da**. Obično je ovo primarni klijent ponude, ali to se može promeniti.