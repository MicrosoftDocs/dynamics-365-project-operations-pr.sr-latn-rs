---
title: Upravljanje predračunom zasnovanim na projektu
description: Ovaj članak pruža informacije o načinu upravljanja i rada sa fakturama zasnovanim na predračunima za projekat.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 31822947a4fbb60218ce1c3c9415a60491f6d8fa
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932129"
---
# <a name="manage-a-proforma-project-based-invoice"></a>Upravljanje predračunom zasnovanim na projektu

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

U usluzi Dynamics 365 Project Operations, profakture se prave kao dodatak fakturama u usluzi Dynamics 365 Sales. Međutim, postoje mnoge razlike u procesu fakturisanja između usluga Sales i Project Operations kada je reč o fakturisanju. Na primer, nije moguće kreirati novu fakturu na stranici **Lista faktura** u usluzi Project Operations, ali to je moguće učiniti u usluzi Sales. Ove razlike i proširenja postoje za podršku procesima fakturisanja za projekte koji se razlikuju od tipične fakture za narudžbenicu.

> [!IMPORTANT]
> Zbog tih razlika, nemojte razmenjivati fakture između usluga Sales i Project Operations.

## <a name="invoice-header"></a>Zaglavlje fakture

Sledeće informacije su dostupne u zaglavlju predračuna u usluzi Project Operations.

| Polje | Lokacija | Opis |
| --- | --- | --- | 
| **ID fakture** | Kartica **Rezime** | ID koji se automatski generiše prilikom kreiranja predračuna. Polje samo začitanje koje je zaključano za uređivanje. Ovo polje se koristi kao referenca za svaki predračun. |
| **Ime** | Kartica **Rezime** | Podrazumevano postavljeno na ime projektnog ugovora. To polje možete uređivati. | 
| **Valuta** | Kartica **Rezime** | Podrazumevano podešeno na valutu projektnog ugovora. Polje samo začitanje koje je zaključano za uređivanje. |
| **Cenovnik** | Kartica **Rezime** | Podrazumevano podešeno na cenovnik projektnog ugovora. Polje samo začitanje koje je zaključano za uređivanje. | 
| **Mogućnost za poslovanje** | Kartica **Rezime** | Referenca na povezanu mogućnost za poslovanje. Polje samo začitanje koje je zaključano za uređivanje. | 
| **Ugovor** | Kartica **Rezime** | Referenca na povezani ugovor za projekat. Polje samo začitanje koje je zaključano za uređivanje. | 
| **Klijent** | Kartica **Rezime** | Referenca na povezani ugovor za projekat. Polje samo začitanje koje je zaključano za uređivanje. |
| **Opis** | Kartica **Rezime** | Tekstualno polje koje opisuje fakturu. To polje možete uređivati. | 
| **Adresa fakturisanja** i srodna polja | **Kartica Rezime** | Podrazumevane vrednosti postavlja klijent ugovora za projekat. To polje možete uređivati.  | 
| **Status** | Kartica **Rezime** | Postavlja sledeće opcije: **Aktivno**, **Zatvoreno**, **Plaćeno** i **Otkazano**, a to se može uređivati. Nepodržani statusi za Project Operations uključuju **Zatvoreno** i **Otkazano**. </br> Status je podešen na **Aktivno** kada se kreira faktura. </br>Status treba postaviti na **Plaćeno** tek nakon potvrde fakture.  | 
| **Status fakture projekta** | Kartica **Rezime** | Postavlja sledeće opcije: **Radna verzija**, **Pregleda se** i **Potvrđeno**, a to se može uređivati. U statusima **Radna verzija** i **Pregleda se**, faktura se može uređivati. Faktura se ne može uređivati nakon potvrde. | 
| **Detaljan iznos** | Kartica **Rezime** | Zbir iznosa na svim stavkama faktura nakon avansnih uplata i odbitaka. Polje samo začitanje koje je zaključano za uređivanje.  Ovo polje se koristi za izračunavanje konačnog iznosa. | 
| **Popust (%)** | Kartica **Rezime** | Ovo polje možete urediti da biste uneli procenat popusta. Project Operations funkcionalnost ne podržava ovo polje. Ovo je nepodržano polje.|  
| **Iznos popusta** | Kartica **Rezime** | Ovo polje možete urediti da biste uneli iznos popusta. Project Operations funkcionalnost ne podržava ovo polje. Ovo je nepodržano polje. |  
| **Cena pre transporta** | **Kartica Rezime** | Ukupan iznos fakture nakon primene popusta. Polje samo začitanje koje je zaključano za uređivanje. Ovo polje se koristi za izračunavanje konačnog iznosa.  | 
| **Iznos troškova prevoza** | Kartica **Rezime** | Ovo polje možete urediti da biste uneli cenu transporta. Project Operations funkcionalnost ne podržava ovo polje. Ovo je nepodržano polje. |
| **Ukupni porez** | Kartica **Rezime** | Ukupan porez iz svih stavki fakture na fakturi. Polje samo začitanje koje je zaključano za uređivanje. | 
| **Ukupan iznos** | Kartica **Rezime** | Zbir iznosa nakon popusta i poreza. Zbir je iznos koji klijent treba da plati. | 

## <a name="project-based-invoice-lines"></a>Predmeti ugovora zasnovani na projektu

U usluzi Project Operations, uvek postoji jedna stavka fakture za svaki predmet ugovora o projektu. Stavka fakture se kreira čak i ako nema stvarnih vrednosti. Sledeće informacije su dostupne u stavki predračuna.

| Polje | Lokacija | Opis | 
| --- | --- | --- |
| **ID fakture** | Kartica **Opšti podaci** | Referenca na ID fakture. Polje samo začitanje koje je zaključano za uređivanje. Veza sa ID-om fakture može se koristiti za povratak u zaglavlje fakture. | 
| **Ime** | Kartica **Opšti podaci** | Naziv stavke fakture koji je podrazumevano postavljen iz naziva predmeta ugovora. To polje možete uređivati. |
| **Project** | Kartica **Opšti podaci** | Projekat na odgovarajućem predmetu ugovora o projektu. Polje samo začitanje koje je zaključano za uređivanje. Veza do projekta može se koristiti za navigaciju do projekta. | 
| **Način naplate** | Kartica **Opšti podaci** | Način plaćanja na odgovarajućem predmetu ugovora o projektu. Polje samo začitanje koje je zaključano za uređivanje. |
| **Iznos predmeta ugovora** | Kartica **Opšti podaci** | Iznos ugovora na povezanom predmetu ugovora za projekat. Polje samo začitanje koje je zaključano za uređivanje. | 
| **Fakturisano do datuma** | Kartica **Opšti podaci** | Zbir iznosa na svim detaljima stavki ove fakture. Polje samo začitanje koje je zaključano za uređivanje. | 
| **Iznos** | Kartica **Opšti podaci** | Zbir iznosa na svim detaljima naplativih stavki ove fakture. Polje samo začitanje koje je zaključano za uređivanje. Ovo polje se koristi za izračunavanje konačnog iznosa zaglavlja fakture. | 
| **Porez** | Kartica **Opšti podaci** | Zbir iznosa poreza na svim detaljima stavki ove fakture. Polje samo začitanje koje je zaključano za uređivanje. Ovo polje se koristi za izračunavanje konačnog iznosa poreza zaglavlja fakture. | 
| **Prošireni iznos** | Kartica **Opšti podaci** | Zbir ukupnih iznosa (**porez + iznosi**) na svim detaljima naplativih stavki ove fakture. Polje samo začitanje koje je zaključano za uređivanje. Ovo polje se koristi za izračunavanje konačnog iznosa zaglavlja fakture. |

## <a name="invoice-line-details"></a>Detalji stavki fakture

Svaka stavka fakture u fakturi za projekat sadrži detalje stavke fakture. Ovi detalji stavke su povezani sa nenaplaćenim stvarnim vrednostima prodaje i kontrolnim tačkama koje se odnose na predmet ugovora na koji se poziva stavka fakture. Sve ove transakcije su obeležene sa **Spremno za fakturisanje**.

Za red **Faktura za vreme i materijal**, detalji stavke fakture se grupišu u **Naplativo**, **Ne naplaćuje se** i **Besplatno** na stranici **Red fakture**. Detalji **naplative stavke fakture** se sabiraju u ukupnu vrednost stavke fakture. **Besplatno** i **Nenaplative stvarne vrednosti** se ne sabiraju u ukupnu vrednost stavke fakture.

Za red **Faktura sa fiksnom cenom**, detalji stavke fakture kreiraju se iz kontrolnih tačaka koje su označene kao **Spremno za fakturisanje** na odgovarajućem predmetu ugovora. Kada se kreira detalj stavke fakture iz kontrolne tačke, status naplate na kontrolnoj tački se ažurira na **Faktura kreirana za klijenta**.

### <a name="edit-invoice-line-details"></a>Uređivanje detalja stavki fakture

Sledeća polja su dostupna na detaljima stavke fakture koji su podržani stvarnim vrednostima nenaplaćene prodaje.

| Polje | Opis |
| --- | --- | 
| **Stavka fakture** | Referenca na **ID stavke fakture**. Ovo polje je samo za čitanje i zaključano za uređivanje. Ova veza se može koristiti za povratak u zaglavlje fakture. | 
| **Opis** | Opis detalja stavke fakture. Podrazumevano postavljeno iz polja **Interni komentari** na **Stavka vremena** i iz polja **Opis** na **Unos troškova**. To polje možete uređivati.| 
| **Spoljni opis** | Opis detalja stavke fakture. Podrazumevano postavljeno iz polja **Spoljni komentari** na **Stavka vremena** i iz polja **Opis** na **Unos troškova**. To polje možete uređivati. Ovaj opis se može koristiti za određivanje šta treba da bude na odštampanoj fakturi koja će biti poslata klijentu. U usluzi Project Operations, predračun nema svu potrebnu funkcionalnost za konfigurisanje podešavanja štampanja za fakturu. | 
| **Datum početka** | To je polje samo za čitanje koje je podrazumevano podešeno iz stvarnog izvora. |
| **Project** | To je polje samo za čitanje koje je podrazumevano podešeno iz stvarnog izvora za projekat na povezanom predmetu ugovora. |  
| **Zadatak** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. |
| **Kategorija transakcije** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. | 
| **Uloga** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. |  
| **Resurs koji može da se rezerviše** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. | 
| **Preduzeće koje određuje resurse** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. | 
| **Jedinica za određivanje resursa** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. | 
| **Količina** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. |  
| **Raspored jedinica** | Za detalje stavke fakture za vreme, ovo se uvek postavlja na vreme i ne može se uređivati. Za troškove je ovo podrazumevano postavljeno iz stvarnih vrednosti troškova izvora. Polje samo začitanje koje je zaključano za uređivanje. | 
| **Jedinica** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. |  
| **Cena** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. |
| **Valuta** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. | 
| **Iznos** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. | 
| **Porez** | Podrazumevano postavljeno iz stvarne vrednosti izvora. To polje možete uređivati.| 
| **Prošireni iznos** | Izračunato polje, izračunava se kao **Iznos + porez**. Polje samo začitanje koje je zaključano za uređivanje. | 
| **Tip naplate** | Podrazumevano postavljeno iz stvarne vrednosti izvora. To polje možete uređivati. Izbor **Naplativo** dodaje stavku u ukupan iznos fakture. **Besplatno** i **Nenaplativo** će ga izuzeti iz ukupne vrednosti stavke fakture.| 
| **Izaberite proizvod** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. |
| **Proizvod** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. | 
| **Naziv proizvoda** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. |  
| **Ručno dodat opis** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. |
| **Tip transakcije** | To je polje samo za čitanje koje je podrazumevano podešeno iz stvarnog izvora u polje **Naplaćena prodaja**. |  
| **Klasa transakcije** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. | 

Sledeća polja su dostupna na detaljima stavke fakture koji su podržani kontrolnom tačkom.

| Polje | Opis |
| --- | --- | 
| **Stavka fakture** | Referenca na **ID stavke fakture**. Polje samo začitanje koje je zaključano za uređivanje. Veza se može koristiti za povratak u zaglavlje fakture.  | 
| **Opis** | Opis detalja stavke fakture. Podrazumevano postavljeno iz opisa kontrolne tačke izvora. | 
|**Spoljni opis** | Opis detalja stavke fakture koja je podrazumevano postavljena iz opisa kontrolne tačke izvora. Ovo polje se može koristiti za određivanje šta treba da bude na odštampanoj fakturi koja će biti poslata klijentu. Predračun u usluzi Project Operations nema svu potrebnu funkcionalnost za konfigurisanje podešavanja štampanja za fakturu. | 
| **Datum početka** | Podrazumevano postavljeno iz datuma **Kontrolna tačka** u kontrolnoj tački izvora. Polje samo začitanje koje je zaključano za uređivanje. | 
| **Project** | Podrazumevano postavljeno iz kontrolne tačke izvora. Polje samo začitanje koje je zaključano za uređivanje. |
| **Zadatak** | Podrazumevano postavljeno iz kontrolne tačke izvora. Polje samo začitanje koje je zaključano za uređivanje. | 
| **Kategorija transakcije** | Polje samo začitanje koje je zaključano za uređivanje. |
| **Uloga** | Polje samo začitanje koje je zaključano za uređivanje. | 
| **Resurs koji može da se rezerviše** | Polje samo začitanje koje je zaključano za uređivanje. | 
| **Jedinica za određivanje resursa** | Polje samo začitanje koje je zaključano za uređivanje. | 
| **Raspored jedinica** | Polje samo začitanje koje je zaključano za uređivanje. | 
| **Jedinica** | Polje samo začitanje koje je zaključano za uređivanje. | 
| **Cena** | Podrazumevano postavljeno iz iznosa na kontrolnoj tački izvora. Polje samo začitanje koje je zaključano za uređivanje. |
| **Valuta** | Podrazumevano postavljeno iz kontrolne tačke izvora. Polje samo začitanje koje je zaključano za uređivanje. |
| **Iznos** | Podrazumevano postavljeno iz iznosa na kontrolnoj tački izvora. Polje samo začitanje koje je zaključano za uređivanje. | 
| **Porez** | Podrazumevano postavljeno iz iznosa poreza na kontrolnoj tački izvora. Polje samo začitanje koje je zaključano za uređivanje. |
| **Prošireni iznos** | Podrazumevano postavljeno iz proširenog iznosa poreza na kontrolnoj tački izvora. To polje možete uređivati. | 
| **Tip naplate** | Uvek podrazumevano postavljeno na **Naplativo**. Polje samo začitanje koje je zaključano za uređivanje. |
| **Tip transakcije** | Podrazumevano postavljeno iz kontrolne tačke izvora. Polje samo začitanje koje je zaključano za uređivanje. | 
| **Klasa transakcije** | Podrazumevano postavljeno iz kontrolne tačke izvora. Polje samo začitanje koje je zaključano za uređivanje. | 

## <a name="refresh-invoice-transactions"></a>Osvežavanje transakcija za fakture

Ako imate stvarne vrednosti koje su stigle nakon kreiranja fakture, možete ih uključiti u fakturu.

1. U **Prikazu zaostalih naplata**, označite podatke kao **Spremni za fakturisanje**.   
2. Otvorite radnu verziju predračuna i na traci **Radnje** izaberite **Osvežite transakcije u stavci fakture**.

  Detalji stavke fakture se kreiraju za sve stvarne podatke čiji datum je istekao i označeni su kao **Spremno za fakturisanje**, ali nisu uključeni u fakturu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
