---
title: Ponude – ključni koncepti
description: Ovaj članak pruža informacije o ponudama za projekat i ponudama za prodaju koje su dostupne u operacijama projekta.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c0598b9ec276741f1f62e0cfc1717a3fd622cd7c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912533"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Koncepti jedinstveni za ponude zasnovane na projektu

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

U usluzi Dynamics 365 Project Operations postoje dve vrste ponuda – za projekte i za prodaju. Ova dva tipa ponuda se razlikuju na sledeće načine:

- **Mreže za stavke**: u ponudi za prodaju postoji samo jedna mreža za stavke. U ponudi za projekat postoje dve mreže za stavke. Jedna mreža je za projektne linije, a druga za proizvodne linije.
- **Aktivacija i revizije** : ponude za prodaju podržavaju aktivaciju i revizije. Ovi procesi nisu podržani u ponudi za projekat.
- **Priložene ponude**: ponudi za prodaju možete priložiti više porudžbina. U ponudu za projekat možete da priložite samo jedan ugovor o projektu.
- **Osvajanje ponude**: kada osvojite ponudu za prodaju, srodna prilika može ostati otvorena. Kada vam odobre ponudu za projekat, biće zatvorena povezana mogućnost za poslovanje.
- **Polja i koncepti**: ponuda za prodaju ne sadrži neka polja i koncepte koji su obuhvaćeni u ponudi za projekat. U polja spadaju **Ugovorna jedinica**, **Menadžer za poslovne kontakte** i **Ime kontakta za fakturisanje**.  
- **Tip**: Ponude za prodaju i ponude za projekte identifikuje i polje zasnovano na skupu opcija pod nazivom **Tip**. Za ponudu za prodaju, ovo polje ima vrednost **Zasnovano na stavci**. Za ponudu za projekat, ima vrednost **Zasnovano na radu**.

Ovaj članak je fokusiran na detalje projektne ponude.

Ponuda za projekat u aplikaciji Project Operations može da ima više stavki predmeta ili stavki ponude. U stvari, ponuda za projekat ima dve mreže za stavke predmeta. Jedna mreža je namenjena stavkama zasnovanim na projektu i omogućava detaljne procene. Druga mreža je namenjena stavkama zasnovanim na proizvodu i koristi jednostavnu jediničnu cenu i pristup zasnovan na količini.

- **Zasnovano na projektu**: iznos (ponuđena vrednost) utvrđuje se nakon procene količine posla. Možete proceniti rad na visokom nivou, direktno kao detalje reda ispod svake stavke ponude, ili na osnovu osnovanih procena, koristeći projekat i projektni plan. Stavke ponude zasnovane na projektu se nalaze samo u ponudama zasnovanim na projektu koje se kreiraju pomoću aplikacije Project Operations. Ovaj tip stavke ponude je prilagođeni obrazac ručno dodatih stavki ponude koje su dostupne u sistemu Microsoft Dynamics 365 Sales.

- **Zasnovano na proizvodu**: ponuđena vrednost se određuje na osnovu količine prodatih jedinica i prodajne cene. Proizvod u stavci zasnovanoj na proizvodu može doći iz kataloga proizvoda u Prodaji ili može biti proizvod koji definišete. Ovaj tip stavke ponude je takođe dostupan u ponudama zasnovanim na projektu koje se kreiraju pomoću aplikacije Project Operations.

Iznos u ponudi je zbirna vrednost svih stavki zasnovanih na proizvodu i stavki zasnovanih na projektu.

> [!NOTE]
> Ponude i stavke ponuda nisu potrebne u aplikaciji Project Operations. Proces projekta možete započeti ugovorom o projektu (prodat projekat). Međutim, uvek je potrebna mogućnost za poslovanje, bez obzira na to da li ste započeli ponudom ili ugovorom o projektu.

## <a name="project-based-quote-lines"></a>Stavke ponude zasnovane na projektu

Stavka ponude zasnovana na projektu u aplikaciji Project Operations ima sledeće načine naplate:

- Vreme i materijal
- Fiksna cena

### <a name="time-and-material"></a>Vreme i materijal

Način naplate vremena i materijala je zasnovan na utrošku. Kada izaberete ovaj način naplate, klijentu se fakturiše tokom ostvarivanja troškova projekta. Učestalost kreiranja fakture je periodična i zasnovana na datumu. Tokom procesa prodaje, ponuđena vrednost komponente vremena i materijala klijentu daje samo procenu konačnih troškova. Prodavac se ne obavezuje da će dovršiti projekat sa tačnom ponuđenom vrednošću. Komponente vremena i materijala povećavaju rizik klijenta. Klijenti će možda želeti da ispregovaraju dodatne odrednice u vezi sa iznosom koji ne sme da se premaši da bi umanjili rizik. Project Operations ne podržava podešavanje odrednica u vezi sa iznosom koji ne sme da se premaši.

### <a name="fixed-price"></a>Fiksna cena

Način naplate Fiksna cena omogućava prodavcu da se obaveže da će projekat isporučiti klijentu po fiksnoj ceni. Klijentu se naplaćuje ponuđena vrednost stavke ponude sa fiksnom cenom, bez obzira na troškove koje prodavac ostvaruje prilikom isporuke te stavke ponude. Vrednost stavke ponude sa fiksnom cenom se naplaćuje na jedan od sledećih načina: 

- Kao objedinjena suma iznosa na početku ili kraju projekta ili kada se dođe do kontrolne tačke u projektu. 
- Na jednake rate fiksne vrednosti u stavci ponude. Njihova učestalost je zasnovana na određenom datumu. Ove rate su poznate kao periodične kontrolne tačke.
- U ratama sa monetarnom vrednošću koja je usklađena sa napretkom posla ili specifičnim kontrolnim tačkama koje ispunjavate za projekat. U ovom slučaju, vrednost svake rate može da se razlikuje, ali iznos svih rata mora da bude fiksna vrednost u stavci ponude.

Project Operations podržava sve tri vrste rasporeda fakturisanja za stavke ponude sa fiksnom cenom.

## <a name="transaction-classification"></a>Klasifikacija transakcije

Organizacije koje pružaju profesionalne usluge obično daju ponude klijentima i fakturišu klijentima po klasifikaciji troškova. Troškovi su predstavljeni sledećim klasifikacijama transakcija:

- **Vreme**: ova klasifikacija predstavlja troškove rada ili vremena ljudskih resursa na projektu.
- **Trošak**: ova klasifikacija predstavlja sve ostale vrste troškova na projektu. Pošto troškovi mogu da budu široko klasifikovani, većina organizacija kreira podkategorije, poput putnih troškova, troškova iznajmljivanja automobila, hotelskih troškova ili kancelarijskih zaliha.
- **Naknada**: ova klasifikacija predstavlja razne dodatne troškove, kazne i druge stavke koje se naplaćuju klijentu. 
- **Porez**: ova klasifikacija predstavlja iznose poreza koje korisnici dodaju dok unose troškove.
- **Stvarna transakcija**: ova klasifikacija predstavlja stvarne vrednosti iz stavki proizvoda na potvrđenoj fakturi za projekat.
- **Kontrolna tačka**: ovu klasifikaciju koristi logika naplate fiksne cene.

Neke od ovih klasifikacija transakcija mogu da se povežu sa svakom stavkom ponude. Kada vam odobre ponudu, mapiranje između klasifikacije transakcije i stavke ponude se prenosi u predmet ugovora.
  
Na primer, ponuda može da sadrži sledeće dve stavke ponude: 

- Konsultantski posao koji koristi metod naplate vremena i materijala u kom se mogu primenjivati klasifikacije transakcija prema vremenu i nadoknadi. Na primer, sve transakcije vremena i naknade za primer projekta **Dynamics AX implementacija** se fakturišu klijentu na osnovu utrošenog vremena i materijala. 
- Srodni putni troškovi koji koriste način naplate Fiksna cena. Na primer, svi putni troškovi za primer projekta **Dynamics AX implementacija** se fakturišu po fiksnoj monetarnoj vrednosti.

> [!NOTE]
> Kombinacija klasifikacija projekta i transakcije **Vreme**, **Troškovi** i **Naknada** povezana sa stavkom ponude ili predmetom ugovora mora biti jedinstvena. Ako je ista kombinacija klase projekta i transakcije povezana sa više od jednog predmeta ugovora ili stavki ponude, Project Operations neće raditi ispravno.

## <a name="billing-types"></a>Tipovi naplate

Polje **Vrsta naplate** definiše koncept naplativosti. To je skup opcija koji ima sledeće moguće vrednosti:

- **Naplativo**: troškovi koje je akumulirala ova uloga/kategorija su direktni troškovi koji dovodi do izvršenje projekta, a klijent će platiti za ovaj posao. Plaćanje se može administrirati kao aranžman zasnovan na vremenu i materijalu ili aranžman sa fiksnom cenom. Međutim, zaposleni koji utroši ovo vreme dobiće odgovarajući kredit za naplativu ukupnu iskorišćenost.
- **Nenaplativo**: troškovi koje akumulira ova uloga/kategorija se smatraju direktnim troškovima koji dovode do izvršenje projekta, čak i ako klijent ne shvata ovu činjenicu i ne želi da plati za ovaj posao. Zaposleni koji utroši ovo vreme neće dobiti kredit u formi naplative ukupne iskorišćenosti rada.
- **Besplatno**: troškovi koje akumulira ova uloga/kategorija se smatraju direktnim troškovima koji dovodi do izvršenje projekta, a klijent shvata ovu činjenicu. Zaposleni koji utroši ovo vreme će dobiti kredit za naplativu ukupnu iskorišćenost rada. Međutim, ovi troškovi se ne naplaćuju klijentu.
- **Nije dostupno**: troškovi koji se akumuliraju na internim projektima i ne zahtevaju praćenje prihoda se prate pomoću ove opcije.

## <a name="invoice-schedule"></a>Raspored za fakturisanje

Raspored za fakturisanje predstavlja niz datuma kada se fakturišu troškovi za projekat. Opcionalno možete da kreirate raspored za fakturisanje u stavci ponude u aplikaciji. Svaka stavka ponude može imati svoj raspored za fakturisanje. Da biste kreirali raspored za fakturisanje, morate obezbediti sledeće vrednosti atributa:

- Datum početka naplate 
- Datum isporuke koji predstavlja datum završetka naplate za projekat
- Učestalost fakturisanja

Koriste se ove tri vrednosti atributa za generisanje uslovni skup datuma za uspostavljanje fakturisanja.

## <a name="invoice-frequency"></a>Učestalost fakturisanja

Učestalost fakturisanja je entitet koji skladišti vrednosti atributa koje pomažu da se izrazi učestalost kreiranja fakture. Sledeći atributi izražavaju ili definišu entitet učestalosti fakturisanja:

- **Period**: mesečni, dvonedeljni i sedmični periodi su podržani. 
- **Broj pokretanja u toku perioda:/** - za sedmične i dvonedeljne periode možete definisati samo jedno pokretanje po periodu. Za mesečne periode možete definisati između jednog i četiri pokretanja po periodu. 
- **Dani pokretanja**: dani kada treba pokrenuti fakturisanje. Ovaj atribut možete da konfigurišete na dva načina:
  - **Radnim danima**: na primer, možete da navedete da se fakturisanje pokreće svakog ponedeljka ili svakog drugog ponedeljka. Klijenti koji moraju da podese pokretanje fakturisanja radnim danom možda preferiraju ovakvu vrstu konfiguracije. 
  - **Kalendarski dani**: na primer, možete navesti da se fakturisanje pokreće sedmog i dvadesetprvog dana svakog meseca. Neke organizacije možda preferiraju ovakvu vrstu konfiguracije, jer garantuje da se fakturisanje pokreće po fiksnom rasporedu svakog meseca.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Raspored za fakturisanje za stavku ponude sa fiksnom cenom

Za stavku ponude sa fiksnom cenom možete koristiti mrežu **Raspored fakturisanja** da biste kreirali kontrolne tačke naplate koje su jednake vrednošću u stavci ponude.

- Da biste kreirali kontrolne tačke za naplatu koje su podjednako podeljene, izaberite učestalost fakturisanja, unesite datum početka naplate u stavku ponude i izaberite **Zahtevani datum završetka** za ponudu u odeljku **Rezime** zaglavlja ponude. Zatim izaberite **Generisanje periodičnih kontrolnih tačaka** da biste kreirali podjednako podeljene kontrolne tačke zasnovane na izabranoj učestalosti fakturisanja. 
- Da biste kreirali kontrolnu tačku naplate objedinjene sume, kreirajte kontrolnu tačku, a zatim unesite vrednost stavke ponude kao iznos za kontrolnu tačku.
- Da biste kreirali kontrolne tačke za naplatu koje su zasnovane na specifičnim zadacima u planu projekta, kreirajte kontrolnu tačku i mapirajte je na element rasporeda projekta u korisničkom interfejsu za naplatu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
