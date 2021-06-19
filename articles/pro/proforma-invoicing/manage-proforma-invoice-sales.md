---
title: Upravljanje predračunom za projekat
description: Ova tema pruža informacije o načinu rada sa predračunima u projektu.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dc069d7007bdc58140a33c7a2ebae7ef9d1e84ff
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003873"
---
# <a name="manage-a-proforma-project-invoice"></a>Upravljanje predračunom za projekat 

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

U usluzi Dynamics 365 Project Operations, profakture se prave kao dodatak fakturama u usluzi Dynamics 365 Sales. Međutim, postoje mnoge razlike u procesu fakturisanja između usluga Sales i Project Operations kada je reč o fakturisanju. Na primer, nije moguće kreirati novu fakturu na stranici **Lista faktura** u usluzi Project Operations, ali to je moguće učiniti u usluzi Sales. Ove razlike i proširenja postoje za podršku procesima fakturisanja za projekte koji se razlikuju od tipične fakture za narudžbenicu.

> [!IMPORTANT]
> Zbog tih razlika, nemojte razmenjivati fakture između usluga Sales i Project Operations.

## <a name="invoice-header"></a>Zaglavlje fakture

Sledeće informacije su dostupne u zaglavlju predračuna u usluzi Project Operations.

| Polje | Lokacija | Opis | Posledični uticaj |
| --- | --- | --- | --- |
| **ID fakture** | Kartica **Rezime** | ID koji se automatski generiše prilikom kreiranja predračuna. Polje samo začitanje koje je zaključano za uređivanje. | Ovo polje se koristi kao referenca za svaki predračun. |
| **Ime** | Kartica **Rezime** | Podrazumevano postavljeno na ime projektnog ugovora. Korisnik može da uređuje ovo polje. | &nbsp;  |
| **Valuta** | Kartica **Rezime** | Podrazumevano podešeno na valutu projektnog ugovora. Polje samo začitanje koje je zaključano za uređivanje. |&nbsp; |
| **Cenovnik** | Kartica **Rezime** | Podrazumevano podešeno na cenovnik projektnog ugovora. Polje samo začitanje koje je zaključano za uređivanje. | &nbsp; |
| **Mogućnost za poslovanje** | Kartica **Rezime** | Referenca na povezanu mogućnost za poslovanje. Polje samo začitanje koje je zaključano za uređivanje. | &nbsp;  |
| **Ugovor** | Kartica **Rezime** | Referenca na povezani ugovor za projekat. Polje samo začitanje koje je zaključano za uređivanje. | &nbsp; |
| **Klijent** | Kartica **Rezime** | Referenca na povezani ugovor za projekat. Polje samo začitanje koje je zaključano za uređivanje. |&nbsp;  |
| **Opis** | Kartica **Rezime** | Tekstualno polje koje opisuje fakturu. Korisnik može da uređuje ovo polje. | &nbsp; |
| **Adresa fakturisanja** i srodna polja | **Kartica Rezime** | Podrazumevane vrednosti postavlja klijent ugovora za projekat. Korisnik može da uređuje ovo polje.  | &nbsp; |
| **Status** | Kartica **Rezime** | Postavlja sledeće opcije: **Aktivno**, **Zatvoreno**, **Plaćeno** i **Otkazano**, a korisnik može da ih uređuje. | Nepodržani statusi za Project Operations uključuju **Zatvoreno** i **Otkazano**. </br> Status je podešen na **Aktivno** kada se kreira faktura. </br>Status treba postaviti na **Plaćeno** tek nakon potvrde fakture. |
| **Status fakture projekta** | Kartica **Rezime** | Postavlja sledeće opcije: **Radna verzija**, **Pregleda se** i **Potvrđeno**, a korisnik može da ih uređuje. | U statusima **Radna verzija** i **Pregleda se**, faktura se može uređivati. Faktura se ne može uređivati nakon potvrde. |
| **Detaljan iznos** | Kartica **Rezime** | Zbir iznosa na svim stavkama faktura nakon avansnih uplata i odbitaka. Polje samo začitanje koje je zaključano za uređivanje. | Ovo polje se koristi za izračunavanje konačnog iznosa. |
| **Popust (%)** | Kartica **Rezime** | Ovo polje možete urediti da biste uneli procenat popusta. Project Operations funkcionalnost ne podržava ovo polje. | Ovo je nepodržano polje. |
| **Iznos popusta** | Kartica **Rezime** | Ovo polje možete urediti da biste uneli iznos popusta. Project Operations funkcionalnost ne podržava ovo polje. | Ovo je nepodržano polje. |
| **Cena pre transporta** | **Kartica Rezime** | Ukupan iznos fakture nakon primene popusta. Polje samo začitanje koje je zaključano za uređivanje. | Ovo polje se koristi za izračunavanje konačnog iznosa. |
| **Iznos troškova prevoza** | Kartica **Rezime** | Ovo polje možete urediti da biste uneli cenu transporta. Project Operations funkcionalnost ne podržava ovo polje. | Ovo je nepodržano polje. |
| **Ukupni porez** | Kartica **Rezime** | Ukupan porez iz svih stavki fakture na fakturi. Polje samo začitanje koje je zaključano za uređivanje. | Nijedno. |
| **Ukupan iznos** | Kartica **Rezime** | Zbir iznosa nakon popusta i poreza. | Zbir je iznos koji klijent treba da plati. |
## <a name="project-based-invoice-lines"></a>Predmeti ugovora zasnovani na projektu

U usluzi Project Operations, uvek postoji jedna stavka fakture za svaki predmet ugovora o projektu. Stavka fakture se kreira čak i ako nema stvarnih vrednosti. Sledeće informacije su dostupne u stavki predračuna.

| Polje | Lokacija | Opis | Posledični uticaj |
| --- | --- | --- | --- |
| **ID fakture** | Kartica **Opšti podaci** | Referenca na ID fakture. Polje samo začitanje koje je zaključano za uređivanje. | Veza sa ID-om fakture može se koristiti za povratak u zaglavlje fakture. |
| **Ime** | Kartica **Opšti podaci** | Naziv stavke fakture koji je podrazumevano postavljen iz naziva predmeta ugovora. Korisnik može da uređuje ovo polje. | &nbsp; |
| **Project** | Kartica **Opšti podaci** | Projekat na odgovarajućem predmetu ugovora o projektu. Polje samo začitanje koje je zaključano za uređivanje. | Veza do projekta može se koristiti za navigaciju do projekta. |
| **Način naplate** | Kartica **Opšti podaci** | Način plaćanja na odgovarajućem predmetu ugovora o projektu. Polje samo začitanje koje je zaključano za uređivanje. | &nbsp; |
| **Iznos predmeta ugovora** | Kartica **Opšti podaci** | Iznos ugovora na povezanom predmetu ugovora za projekat. Polje samo začitanje koje je zaključano za uređivanje. | &nbsp; |
| **Fakturisano do datuma** | Kartica **Opšti podaci** | Zbir iznosa na svim detaljima stavki ove fakture. Polje samo začitanje koje je zaključano za uređivanje. | &nbsp; |
| **Iznos** | Kartica **Opšti podaci** | Zbir iznosa na svim detaljima naplativih stavki ove fakture. Polje samo začitanje koje je zaključano za uređivanje. | Ovo polje se koristi za izračunavanje konačnog iznosa zaglavlja fakture. |
| **Porez** | Kartica **Opšti podaci** | Zbir iznosa poreza na svim detaljima stavki ove fakture. Polje samo začitanje koje je zaključano za uređivanje. | Ovo polje se koristi za izračunavanje konačnog iznosa poreza zaglavlja fakture. |
| **Prošireni iznos** | Kartica **Opšti podaci** | Zbir ukupnih iznosa (**porez + iznosi**) na svim detaljima naplativih stavki ove fakture. Polje samo začitanje koje je zaključano za uređivanje. | Ovo polje se koristi za izračunavanje konačnog iznosa zaglavlja fakture. |


## <a name="invoice-line-details"></a>Detalji stavki fakture

Svaka stavka fakture u fakturi za projekat sadrži detalje stavke fakture. Ovi detalji stavke su povezani sa nenaplaćenim stvarnim vrednostima prodaje i kontrolnim tačkama koje se odnose na predmet ugovora na koji se poziva stavka fakture. Sve ove transakcije su obeležene sa **Spremno za fakturisanje**.

Za red **Faktura za vreme i materijal**, detalji stavke fakture se grupišu u **Naplativo**, **Ne naplaćuje se** i **Besplatno** na stranici **Red fakture**. Detalji **naplative stavke fakture** se sabiraju u ukupnu vrednost stavke fakture. Stavke **Besplatno** i **Nenaplativa stvarna vrednost** se ne sabiraju sa ukupnim brojem redova fakture.

Za red **Faktura sa fiksnom cenom**, detalji stavke fakture kreiraju se iz kontrolnih tačaka koje su označene kao **Spremno za fakturisanje** na odgovarajućem predmetu ugovora. Kada se kreira detalj stavke fakture iz kontrolne tačke, status naplate na kontrolnoj tački se ažurira na **Faktura kreirana za klijenta**.

### <a name="edit-invoice-line-details"></a>Uređivanje detalja stavki fakture

Sledeća polja su dostupna na detaljima stavke fakture koji su podržani stvarnim vrednostima nenaplaćene prodaje:

| Polje | Opis | Posledični uticaj |
| --- | --- | --- |
| **Stavka fakture** | Referenca na **ID stavke fakture**. Polje je samo za čitanje, zaključano za uređivanje. | Ova veza se može koristiti za povratak u zaglavlje fakture. |
| **Opis** | Opis detalja stavke fakture. Podrazumevano postavljeno iz polja **Interni komentari** na **Stavka vremena** i iz polja **Opis** na **Unos troškova**. Korisnik može da uređuje ovo polje.| &nbsp; |
| **Spoljni opis** | Opis detalja stavke fakture. Podrazumevano postavljeno iz polja **Spoljni komentari** na **Stavka vremena** i iz polja **Opis** na **Unos troškova**. Korisnik može da uređuje ovo polje. | Ovaj opis se može koristiti za određivanje šta treba da bude na odštampanoj fakturi koja će biti poslata klijentu. U usluzi Project Operations, predračun nema svu potrebnu funkcionalnost za konfigurisanje podešavanja štampanja za fakturu. |
| **Datum početka** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. | Ovo polje se može urediti na novom detalju stavke fakture koji nije podržan stvarnom vrednošću izvora. |
| **Project** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. | Podrazumevano podešeno na projekat za povezanu stavku ugovora. |
| **Zadatak** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. | Ovo polje se može urediti na novom detalju stavke fakture koji nije podržan stvarnom vrednošću izvora. Padajuća lista prikazuje sve zadatke koji su povezani sa odgovarajućim predmetom ugovora za projekat.  |
| **Kategorija transakcije** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. | Ovo polje se može urediti na novom detalju stavke fakture koji nije podržan stvarnom vrednošću izvora. |
| **Uloga** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. | Ovo polje se može urediti na novom detalju stavke fakture koji nije podržan stvarnom vrednošću izvora. |
| **Resurs koji može da se rezerviše** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. | Ovo polje se može urediti na novom detalju stavke fakture koji nije podržan stvarnom vrednošću izvora. |
| **Jedinica za određivanje resursa** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. | Ovo polje se može urediti na novom detalju stavke fakture koji nije podržan stvarnom vrednošću izvora. |
| **Količina** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. | Ovo polje se može urediti na novom detalju stavke fakture koji nije podržan stvarnom vrednošću izvora. |
| **Raspored jedinica** | Za detalje stavke fakture za vreme, ovo se uvek postavlja na vreme i ne može se uređivati. Za troškove je ovo podrazumevano postavljeno iz stvarnih vrednosti troškova izvora. Polje samo začitanje koje je zaključano za uređivanje. | Podrazumevano postavljeno na **vreme** na novom detalju stavke fakture koji nije podržan stvarnom vrednošću. |
| **Jedinica** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. | Ovo polje se može urediti na novom detalju stavke fakture koji nije podržan stvarnom vrednošću izvora |
| **Cena** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. | Ovo polje se može urediti na novom detalju stavke fakture koji nije podržan stvarnom vrednošću izvora. Ako nije uneta vrednost, ona se podrazumevano postavlja nakon komande **Sačuvaj**. |
| **Valuta** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. | Podrazumevano postavljeno iz zaglavlja fakture prilikom kreiranja novog detalja fakture bez podrške stvarne vrednosti.  Polje samo začitanje koje je zaključano za uređivanje. |
| **Iznos** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. | Izračunava se kao **Količina \* Cena** prilikom kreiranja novog detalja na fakturi bez podrške stvarne vrednosti. Izračunava se nakon komande **Sačuvaj**. Polje samo začitanje koje je zaključano za uređivanje. |
| **Porez** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Korisnik može da uređuje ovo polje | Korisnik može da uređuje polje prilikom kreiranja novog detalja stavke fakture bez podrške stvarne vrednosti. |
| **Prošireni iznos** | Izračunato polje, izračunava se kao **Iznos + porez**. Polje samo začitanje koje je zaključano za uređivanje. | &nbsp; |
| **Tip naplate** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Korisnik može da uređuje ovo polje. | Izbor **Naplativo** dodaje stavku u ukupan iznos fakture. **Besplatno** i **Nenaplativo** će ga izuzeti iz ukupne vrednosti stavke fakture. |
| **Izaberite proizvod** | Podrazumevano podešeno iz stvarnog izvora, ovo je polje samo za čitanje. | Kada kreirate novi detalj stavke fakture bez podržane stvarne vrednosti, ovo polje se može urediti. |
| **Proizvod** | Podrazumevano podešeno iz stvarnog izvora, ovo je polje samo za čitanje. | Kada kreirate novi detalj stavke fakture bez podržane stvarne vrednosti, ovo polje se može urediti ako se polje **Izaberite proizvod** postavi na **Postojeći proizvod**. |
| **Naziv proizvoda** | Podrazumevano podešeno iz stvarnog izvora, ovo je polje samo za čitanje. | Na novom detalju stavke fakture, gde je ID proizvoda izabran iz kataloga, ovo polje se postavlja na naziv proizvoda. Za ručno dodat proizvod, polje se postavlja na ručno upisan naziv. |
| **Ručno dodat opis** | Podrazumevano podešeno iz stvarnog izvora, ovo je polje samo za čitanje. | Kada kreirate novi detalj stavke fakture bez podržane stvarne vrednosti, možete dodati ručno upisan opis za proizvod. |
| **Tip transakcije** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. | Podrazumevano se postavlja na **Naplaćena prodaja** i zaključava prilikom kreiranja novog **Detalja stavke fakture** bez podrške stvarne vrednosti.  |
| **Klasa transakcije** | Podrazumevano postavljeno iz stvarne vrednosti izvora. Polje samo začitanje koje je zaključano za uređivanje. | Podrazumevano podešeno na osnovu toga da li korisnik odlučuje da kreira detalj **Vreme**, **Trošak**, **Materijal** ili **Nadoknada** stavke fakture, istovremeno kreirajući i novi **Detalj stavke fakture** bez podržane stvarne vrednosti. Zaključano za uređivanje. |

Sledeća polja su dostupna na detaljima stavke fakture koji su podržani kontrolnom tačkom:

| Polje | Opis | Posledični uticaj |
| --- | --- | --- |
| **Stavka fakture** | Referenca na **ID stavke fakture**. Polje samo začitanje koje je zaključano za uređivanje. | Veza se može koristiti za povratak u zaglavlje fakture. |
| **Opis** | Opis detalja stavke fakture. Podrazumevano postavljeno iz opisa kontrolne tačke izvora. | &nbsp; |
|**Spoljni opis** | Opis detalja stavke fakture koja je podrazumevano postavljena iz opisa kontrolne tačke izvora. | Ovo polje se može koristiti za određivanje šta treba da bude na odštampanoj fakturi koja će biti poslata klijentu. Predračun u usluzi Project Operations nema svu potrebnu funkcionalnost za konfigurisanje podešavanja štampanja za fakturu. |
| **Datum početka** | Podrazumevano postavljeno iz datuma **Kontrolna tačka** u kontrolnoj tački izvora. Polje samo začitanje koje je zaključano za uređivanje. | &nbsp; |
| **Project** | Podrazumevano postavljeno iz kontrolne tačke izvora. Polje samo začitanje koje je zaključano za uređivanje. | &nbsp; |
| **Zadatak** | Podrazumevano postavljeno iz kontrolne tačke izvora. Polje samo začitanje koje je zaključano za uređivanje. | &nbsp; |
| **Kategorija transakcije** | Polje samo začitanje koje je zaključano za uređivanje. | &nbsp; |
| **Uloga** | Polje samo začitanje koje je zaključano za uređivanje. | &nbsp; |
| **Resurs koji može da se rezerviše** | Polje samo začitanje koje je zaključano za uređivanje. | &nbsp; |
| **Jedinica za određivanje resursa** | Polje samo začitanje koje je zaključano za uređivanje. | &nbsp; |
| **Raspored jedinica** | Polje samo začitanje koje je zaključano za uređivanje. | &nbsp; |
| **Jedinica** | Polje samo začitanje koje je zaključano za uređivanje. | &nbsp; |
| **Cena** | Podrazumevano postavljeno iz iznosa na kontrolnoj tački izvora. Polje samo začitanje koje je zaključano za uređivanje. | &nbsp; |
| **Valuta** | Podrazumevano postavljeno iz kontrolne tačke izvora. Polje samo začitanje koje je zaključano za uređivanje. |&nbsp; |
| **Iznos** | Podrazumevano postavljeno iz iznosa na kontrolnoj tački izvora. Polje samo začitanje koje je zaključano za uređivanje. | &nbsp; |
| **Porez** | Podrazumevano postavljeno iz iznosa poreza na kontrolnoj tački izvora. Polje samo začitanje koje je zaključano za uređivanje. | &nbsp; |
| **Prošireni iznos** | Podrazumevano postavljeno iz proširenog iznosa poreza na kontrolnoj tački izvora. Korisnik može da uređuje ovo polje | &nbsp; |
| **Tip naplate** | Uvek podrazumevano postavljeno na **Naplativo**. Polje samo začitanje koje je zaključano za uređivanje. | &nbsp; |
| **Tip transakcije** | Podrazumevano postavljeno iz kontrolne tačke izvora. Polje samo začitanje koje je zaključano za uređivanje. | &nbsp; |
| **Klasa transakcije** | Podrazumevano postavljeno iz kontrolne tačke izvora. Polje samo začitanje koje je zaključano za uređivanje. | &nbsp; |

### <a name="create-new-invoice-line-details"></a>Kreiranje novih detalja stavke fakture

Na stavkama fakture za vreme i materijal možete kreirati nove detalje stavke fakture. Ovi detalji stavke fakture nisu podržane stvarnom vrednošću. Na stavki fakture za vremena i stavki fakture za materijal, možete da izaberete **Novo** da biste kreirali novi detalj stavke fakture za klase transakcija koje su uključene u predmet ugovora.

## <a name="refresh-invoice-transactions"></a>Osvežavanje transakcija za fakture

Ako imate stvarne vrednosti koje su stigle nakon kreiranja fakture, možete ih uključiti u fakturu.

1. U **Prikazu zaostalih naplata**, označite podatke kao **Spremni za fakturisanje**.   
2. Otvorite radni verziju predračuna i na traci **Radnje** kliknite na **Osvežavanje transakcija stavki fakture**.

  Ovo kreira detalje o stavki fakture za sve stvarne vrednosti čiji datum je istekao i označene su kao **Spremno za fakturisanje**; ali nisu uključene u fakturu.

## <a name="product-based-invoice-lines"></a>Stavke fakture zasnovane na proizvodu

U usluzi Project Operations možete kreirati stavke fakture za proizvode koji se ne odnose na bilo koji projekat ili za sve projekte, zajedno sa stavkama faktura zasnovanih na projektu. Ove stavke faktura kreiraju se kao predmeti ugovora zasnovani na proizvodu i nakon što se označe kao spremni za fakturisanje, dodaju se kao stavke faktura zasnovane na proizvodu.

Kada dodate stavke faktura zasnovane na proizvodu, one se više ne mogu menjati. One se, međutim, mogu izbrisati iz radne verzije predračuna.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
