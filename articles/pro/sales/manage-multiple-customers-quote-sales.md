---
title: Upravljanje sa više klijenata u ponudama za projekat – jednostavno
description: Ova tema pruža informacije o radu sa ponudama sa više klijenata koji će finansirati projekat. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bdda1a940e733270399d092e543c3982c47174d0
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181653"
---
# <a name="manage-multiple-customers-on-project-quotes---lite"></a>Upravljanje sa više klijenata u ponudama za projekat – jednostavno

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Ponude za projekte podržavaju scenario kada predlog uključuje više klijenata koji će finansirati pogodbu. Na kartici **Rezime** ponude nalazi se polje **Potencijalni klijent** koje identifikuje primarnog klijenta u pogodbi. Drugi klijenti za pogodbu mogu se podesiti na kartici **Klijenti** ponude za projekat.

Svi klijenti ponude na kartici **Klijenti** ponude za projekat podrazumevano su klijenti stavke ponude u svakoj **novoj** stavci ponude zasnovane na projektu kreiranoj za ponudu. Sve postojeće stavke ponude zasnovane na projektu neće naslediti nove zapise klijenata ponude kreirane nakon njih.

Stavke ponude zasnovane na proizvodu se automatski povezuju sa primarnim klijentom koji je ujedno i klijent u polju **Potencijalni klijent** na kartici **Rezime** ponude.

Klijenti ponude i klijenti stavke ponude mogu da se dodaju, ažuriraju ili brišu u bilo kom trenutku pre ostvarenja ponude.

## <a name="concept-of-a-primary-customer"></a>Koncept primarnog klijenta

Klijent naveden na kartici rezimea ponude za projekat kao potencijalni klijent je primarni klijent ponude. Kada pokušate da izbrišete primarnog klijenta sa liste klijenata u ponudi, videćete grešku da primarni zapis klijenta u ponudi ne može da se izbriše.

Primarni klijent ne bi trebalo da se ažurira sa liste klijenata na ponudi. Međutim, na primarnog klijenta možete uticati promenom potencijalnog klijenta na kartici **Rezime** ponude. Kada se ovo polje ažurira na **rezimeu ponude**, novoizabrani potencijalni klijent se dodaje kao novi klijent ponude sa postavljenom zastavicom **Primarni**. Stari potencijalni klijent i dalje će biti klijent na ponudi.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Kreiranje, ažuriranje ili brisanje zapisa klijenta ponude

Klijent ponude može da se kreira, ažurira ili izbriše na kartici **Klijenti ponude** na stranici **Ponuda**. Polja navedena u sledećoj tabeli nalaze se u zapisu klijenta ponude u ponudi za projekat.

| **Polje** | **Lokacija** | **Opis** | **Posledični uticaj** |
| --- | --- | --- | --- |
| Nalog | Mreža podložna uređivanju na kartici **Klijenti ponude** i obrasci **Glavni** i **Brzo kreiranje** za klijenta ponude. | Navodi sve aktivne naloge. Ovo polje se zaključava nakon kreiranja zapisa. Ako želite da ga ažurirate, izbrišite zapis i ponovo ga napravite. Ako ste evidentirali bilo koje stvarne podatke ili ako je zapis klijenta ponude primarni klijent, biće vam dozvoljeno da izbrišete zapis. | Klijenti ponude se kopiraju u klijente stavke ponude kada se kreira stavka ponude. Klijenti ponude se takođe kopiraju u klijente ugovora za projekat kada se ponuda ostvari. |
| Procenat deljenja naplate | Mreža podložna uređivanju na kartici **Klijenti ponude** i obrasci **Glavni** i **Brzo kreiranje** za klijenta ponude. | Predstavlja procenat svake nenaplaćene prodajne transakcije koja će biti pripisana ovom klijentu ponude. | Prekopirano u nove stavke ponude i u klijente ugovora o projektu. |
| Ime ugovora za fakturisanje | Mreža podložna uređivanju na kartici **Klijenti ponude** i obrasci **Glavni** i **Brzo kreiranje** za klijenta ponude. | Ovo je tekstualno polje i trebalo bi da se koristi za identifikaciju osobe za kontakt na fakturi za ovog klijenta. One se podrazumevaju iz povezanog zapisa o poslovnom kontaktu | Kopira se u klijente ugovora o projektu kada se ponuda ostvari i pretvara se u polje Ime ugovora za fakturisanje koje se generiše za ovog klijenta. |
| Ime za fakturisanje | Mreža podložna uređivanju na kartici **Klijenti ponude** i obrasci **Glavni** i **Brzo kreiranje** za klijenta ponude. | Ovo tekstualno polje treba da se koristi za identifikaciju osobe za kontakt na fakturi za ovog klijenta. | Kopira se u klijente ugovora o projektu kada se ponuda ostvari i pretvara se u polje **Ime ugovora za fakturisanje** koje se generiše za ovog klijenta. |
| Uslovi plaćanja | Mreža podložna uređivanju na kartici **Klijenti ponude** i obrasci **Glavni** i **Brzo kreiranje** za klijenta ponude. | Ovo je skup opcija sa vrednostima koje se podrazumevaju iz povezanog zapisa naloga. | Kopira se u klijente ugovora o projektu kada se ponuda ostvari i pretvara se u polje **Ime ugovora za fakturisanje** koje se generiše za ovog klijenta. |
| Da li se zaokružuje | Mreža podložna uređivanju na kartici **Klijenti ponude** i obrasci **Glavni** i **Brzo kreiranje** za klijenta ponude. | Označava da li je ovaj klijent podrazumevani klijent za zaokruživanje za ovu pogodbu. | Kopira se u klijente ugovora o projektu kada se ponuda ostvari. |
| Ograničenje koje ne sme da se prekorači | Mreža podložna uređivanju na kartici **Klijenti ponude** i obrasci **Glavni** i **Brzo kreiranje** za klijenta ponude. | Označava da li postoji ugovoreno ograničenje ili gornje ograničenje ukupnog iznosa koji će se fakturisati ovom klijentu za ovo angažovanje | Kopira se u klijente ugovora o projektu kada se ponuda ostvari. |

## <a name="editing-billing-split-percentages"></a>Uređivanje procenta podele naplate

Procente podele naplate možete da uredite koristeći iskustvo unutrašnjeg uređivanja mreže. Kada procenti podele naplate ne iznose 100%, dolazi do greške. Kada ažurirate procente podele naplate, osvežite stranicu da biste uklonili grešku.

Takođe možete pokušati da izaberete **Ravnomerno rasporedi** na podformi klijenata ponude. Ova radnja dodeljuje podele naplate svim klijentima ponude. Ako postoji bilo koji faktor zaokruživanja, to će se dodati klijentu za zaokruživanje. Jedan od klijenata ponude uvek se označava kao klijent za zaokruživanje. to znači da zapis klijenta ponude ima zastavicu **Zaokruživanje** postavljenu na **Da**. Obično je ovo primarni klijent ponude, ali to se može promeniti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]