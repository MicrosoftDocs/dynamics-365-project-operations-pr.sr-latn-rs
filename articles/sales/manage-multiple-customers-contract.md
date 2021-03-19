---
title: Upravljanje sa više klijenata na ugovorima za projekat
description: Ova tema pruža informacije o načinu upravljanja većim brojem klijenata na projektnom ugovoru.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dda8bc58c00082a9ef3835ea293003c63013983f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277985"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Upravljanje sa više klijenata na ugovorima za projekat

Ova tema pruža informacije o načinu upravljanja većim brojem klijenata na projektnom ugovoru. Projektni ugovor možete koristiti kada je za finansiranje pogodbe potreban sporazumni ugovor za više klijenata. Na stranici **Projektni ugovor**, kartica **Rezime** sadrži informacije o primarnom klijentu za pogodbu. Ostali klijenti koji učestvuju u pogodbi mogu biti dodati na kartici **Klijenti**.

Svi klijenti ugovora na kartici **Klijenti** projektnog ugovora podrazumevaju se kao klijenti predmeta ugovora na svim novim predmetima ugovora zasnovanim na projektu kreiranim za projektni ugovor. Svi postojeći predmeti ugovora zasnovani na projektu ne nasleđuju zapise novih klijenata ugovora koji se kreiraju kasnije.

Možete da dodajete, ažurirate ili brišete klijente ugovora i predmeta ugovora u bilo kom trenutku pre dobijanja ugovora. Klijent na projektnom ugovoru mora biti konfigurisan kao klijent u vlasničkom preduzeću ili pravnom licu na stranici **Klijenti**. Pravna lica se konfigurišu u modulu **Upravljanje projektima i računovodstvo** usluge Dynamics 365 Project Operations i dostupni su kao preduzeća u modulima **Projektna prodaja** i **Isporuka** usluge Project Operations.

## <a name="primary-customers"></a>Primarni klijenti

Potencijalni klijent naveden na kartici **Rezime** projektnog ugovora je primarni klijent ugovora. Ne možete da ažurirate primarnog klijenta sa liste klijenata ugovora. Ako pokušate da izbrišete primarnog klijenta sa liste klijenata na ugovoru, pojaviće se poruka o grešci koja navodi da zapis primarnog klijenta na ugovoru nije moguće izbrisati. Umesto toga, promenite klijenta u polju **Potencijalni klijent** kartici **Rezime** projektnog ugovora. Kada ažurirate ovo polje, novoizabrani klijent se dodaje kao novi klijent ugovora sa zastavicom **Primarno** podešenom na **Da**. Prethodni primarni klijent je i dalje klijent na ugovoru, ali više nije primarni klijent.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Kreiranje, ažuriranje ili brisanje zapisa klijenta za ugovor

Možete da kreirate, ažurirate ili brišete klijenta na ugovoru iz kartice **Klijenti ugovora** na stranici **Ugovor**. Sledeća polja su uključena u zasip klijenta ugovora projektnog ugovora.

| **Polje** | **Lokacija** | **Opis** | 
| --- | --- | --- | 
| Nalog | Mreža koja može da se uređuje na kartici **Klijenti ugovora**, kao i glavni obrazac i obrazac za brzo kreiranje za klijenta ugovora. | Navodi sve aktivne naloge. Ovo polje se zaključava nakon kreiranja zapisa. Da biste ažurirali zapis, morate da izbrišete zapis, a zatim kreirate novi. Ako ste evidentirali bilo koje stvarne podatke ili ako je zapis klijenta za ugovor primarni klijent, ne možete izbrisati zapis. Kada kreirate predmet ugovora, klijenti ugovora se kopiraju kao klijenti predmeta ugovora. |
| Procenat deljenja naplate | Mreža koja može da se uređuje na kartici **Klijenti ugovora**, kao i glavni obrazac i obrazac za brzo kreiranje za klijenta ugovora. | Predstavlja procenat svake nefakturisane prodajne transakcije koja je pripisana ovom klijentu predmeta ugovora. Kada se kreiraju novi predmeti ugovora na projektu, procenat podele naplate se kopira u nove predmete ugovora koji su kreirani i u klijente predmeta ugovora. |
| Ime ugovora za fakturisanje | Mreža koja može da se uređuje na kartici **Klijenti ugovora**, kao i glavni obrazac i obrazac za brzo kreiranje za klijenta ugovora. | Ovo tekstualno polje treba koristiti za identifikaciju kontakt osobe za fakturu za klijenta. Podrazumevana vrednost se dobija iz odgovarajućeg zapisa poslovnog kontakta. Ime kontakta se kopira u **Ime kontakta za fakturisanje** na fakturi koji se generiše za klijenta. |
| Ime fakturisanja | Mreža koja može da se uređuje na kartici **Klijenti ugovora**, kao i glavni obrazac i obrazac za brzo kreiranje za klijenta ugovora. | Koristite ovo polje za identifikaciju kontakt osobe za fakturu za klijenta. Podrazumevana vrednost se dobija iz odgovarajućeg zapisa poslovnog kontakta. Ime se kopira u polje **Ime kontakta za fakturisanje** na fakturi koji se generiše za klijenta. |
| Uslovi plaćanja | Mreža koja može da se uređuje na kartici **Klijenti ugovora**, kao i glavni obrazac i obrazac za brzo kreiranje za klijent iz ugovora. | Podrazumevana vrednost se dobija iz odgovarajućeg zapisa poslovnog kontakta. Uslovi se kopiraju u **Ime kontakta za fakturisanje** na fakturi koji se generiše za klijenta. |
| Preduzeće-vlasnik | Mreža koja može da se uređuje na kartici **Klijenti projektnog ugovora**, kao i glavni obrazac i obrazac za brzo kreiranje za klijenta projektnog ugovora. | Pravno lice u kome je klijent konfigurisan u modulu **Upravljanje projektima i računovodstvo**. Ovo polje je samo za čitanje i postavljeno je na vlasničko preduzeće projektnog ugovora.</br>Lista klijenata koje treba dodati u polju **Poslovni kontakt** već je filtrirana u listu iz preduzeća-vlasnika u modulu **Upravljanje projektima i računovodstvo** usluge Project Operations. Vlasničko preduzeće je jednako pravnom licu u modulu **Upravljanje projektima i računovodstvo** usluge Project Operations. Svi troškovi i prihodi koji proizlaze iz ovog projekta evidentirani su u glavnoj knjizi vlasničkog preduzeća. |
| Da li je zaokruživanje | Mreža koja može da se uređuje na kartici **Klijenti ugovora**, kao i glavni obrazac i obrazac za brzo kreiranje za klijenta ugovora. | Označava da li je klijent podrazumevani klijent za zaokruživanje pogodbe. Na ugovoru za projekat može biti samo jedan klijent za zaokruživanje. Kada deljenje troškova i nefakturisane količine dovede do razlike u zaokruživanju, ta razlika se primenjuje na stvarnu vrednost koja se mapira na ovog klijenta. |
| Ograničenje koje ne sme da se prekorači | Mreža koja može da se uređuje na kartici **Klijenti ugovora**, kao i glavni obrazac i obrazac za brzo kreiranje za klijenta ugovora. | Označava da li postoji dogovoreno ograničenje ili gornje ograničenje ukupnog iznosa koji će se fakturisati ovom klijentu za angažovanje. Podešavanje Ograničenje koje ne sme da se prekorači na nivou klijenta ugovora ocenjuje se na osnovu stvarnih vrednostima nenaplaćene prodaje koji upućuju na klijenta ugovora. |

## <a name="edit-billing-split-percentages"></a>Uređivanje procenata podele naplate

Možete da uređujte procente podele naplate uređivanjem na mreži. Kada procenti podele naplate ne budu iznosili 100 procenata, dolazi do greške. Kada uredite procente podele naplate, osvežite stranicu **Projektni ugovor** da biste uklonili grešku.

Takođe možete izabrati opciju **Ravnomerno rasporedi** na podformi klijenata projektnog ugovora. Podele naplate su ravnomerno raspoređene svim klijentima na predmetu projektnog ugovora. Ako postoji bilo koji faktor zaokruživanja, on će se dodati klijentu za zaokruživanje. Jedan od klijenata ugovora uvek ima zastavicu **Zaokruživanje** postavljenu na **Da**. Taj klijent je klijent za zaokruživanje. Obično je klijent za zaokruživanje takođe primarni klijent ugovora, ali to nije obavezno.


[!INCLUDE[footer-include](../includes/footer-banner.md)]