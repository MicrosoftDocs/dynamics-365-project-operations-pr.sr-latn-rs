---
title: Upravljanje cenovnicima projekata u ponudi
description: Ova tema pruža informacije o entitetu cenovnika projekta.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8cfabf98f1a38823c777b6e388fbbb65d02877e3cd433069dd3845c292f2b277
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003923"
---
# <a name="manage-project-price-lists-on-a-quote"></a>Upravljanje cenovnicima projekata u ponudi

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Dynamics 365 Project Operations proširuje entitet cenovnika u sistemu Dynamics 365 Sales. 

## <a name="key-entities"></a>Ključni entiteti

Cenovnik sadrži informacije koje obezbeđuje četiri različita entiteta:

- **Cenovnik**: ovaj entitet skladišti informacije o kontekstu, valuti, datumu stupanja na snagu i jedinici vremena za vreme određivanja cena. Kontekst prikazuje da li su u cenovniku izražene stope troškova ili prodajne stope. 
- **Valuta**: ovaj entitet skladišti valutu cena u cenovniku. 
- **Datum**: ovaj entitet se koristi kada sistem pokuša da unese podrazumevanu cenu za transakciju. Izabran je cenovnik sa datumom stupanja na snagu koji obuhvata datum transakcije. Ako se pronađe više od jednog cenovnika, koji su na snazi na datum transakcije i koji su priloženi sa povezanom ponudom, ugovorom ili organizacionom jedinicom, onda nijedna cena nije podešena kao podrazumevana. 
- **Vreme**: ovaj entitet skladišti jedinicu vremena za koju su izražene cene, kao što cene po danu ili satu. 

Entitet cenovnika ima tri povezane tabele u kojima se skladište cene:

  - **Cena uloge**: ova tabela skladišti cenu za kombinaciju uloge i vrednosti organizacione jedinice i koristi se za podešavanje cena zasnovanih na ulogama za ljudske resurse.
  - **Cena kategorije transakcije**: ova tabela skladišti cene po kategoriji transakcije i koristi se za podešavanje cena po kategorijama troškova.
  - **Stavka cenovnika**: ova tabela skladišti cene za proizvode u katalogu.
 
Cenovnik je cenovna karta. Cenovna karta je kombinacija entiteta cenovnika i srodnih redova u tabelama Cena uloge, Cena kategorije transakcije i Stavke cenovnika.

## <a name="resource-roles"></a>Uloge resursa

Termin *Uloga resursa* odnosi se na skup veština, kompetencija i certifikacije koje osoba mora imati da bi mogla da obavlja određeni skup zadataka u projektu.

Vreme ljudskih resursa se nudi na osnovu uloge koju resurs ima na određenom projektu. Za vreme ljudskih resursa, troškovi i naplata se zasnivaju na ulozi resursa. Vreme može biti izraženo cenom u bilo kojoj jedinici u grupi jedinica **Vreme**.

**Vreme** grupe jedinica kreira se kada instalirate Project Operations. Podrazumevana jedinica je **Čas**. Ne možete izbrisati, preimenovati niti urediti atribute grupe jedinica **Vreme** niti **Čas**. Međutim, možete da dodate druge jedinice u grupu jedinica **Vreme**. Ako pokušate da izbrišete grupu jedinica **Vreme** ili jedinicu **Čas**, možete uzrokovati otkazivanja poslovne logike.
 
## <a name="transaction-categories-and-expense-categories"></a>Kategorije transakcija i troškova

Troškove putovanja i drugi troškovi koje ostvaruju projektni konsultanti se naplaćuju klijentu. Određivanje cena kategorija troškova se završava pomoću cenovnika. Avionski i hotelski troškovi, kao i troškovi iznajmljivanja automobila su primeri kategorija troškova. Svaka stavka cenovnika za troškove određuje cenu za određenu kategoriju troškova. Sledeće tri metode se koriste za određivanje kategorija troškova:

- **Po ceni**: iznos troškova se naplaćuje klijentu, a provizija se ne naplaćuje.
- **Procenat provizije**: procenat u odnosu na stvarnu vrednost troškova se naplaćuje klijentu. 
- **Cena po jedinici**: cena naplate se podešava za svaku jedinicu kategorije troškova. Iznos koji se naplaćuje klijentu se izračunava na osnovu broja jedinica troškova koje konsultant prijavi. Kilometraža koristi metod određivanja cena po jedinici. Na primer, kategorija troškova za kilometražu može se konfigurisati za 30 američkih dolara (USD) dnevno ili 2 USD po milji. Kada konsultant prijavi kilometražu za projekat, taj iznos za naplatu se izračunava na osnovu broja milja koji je prijavio konsultant.
 
## <a name="project-sales-pricing-and-overrides"></a>Formiranje cena i njihova zamena za prodaju u okviru projekta

Za projektne ponude i ugovore, cenovnik projekta ima različit obrazac za zamenu cena u odnosu na cenovnik proizvoda. U stavci ponude zasnovanoj na katalogu proizvoda možete da zamenite cenu za uloge i kategorije direktno u stavci ponude, jer svaka stavka ponude ukazuje na tačno jednu stavku kataloga. Međutim, u stavci ponude zasnovanoj na projektu ne možete da zamenite cenu za uloge i kategorije direktno u stavci ponude. Koristite cenovnik projekta da biste podržali dva različita obrasca zamene.

> [!NOTE]
> Preporučujemo da imate poseban cenovnik za resurse projekta i stavke kataloga, zbog razlika u ponašanju između njih kada zamenite cene.

Svaki od sledećih entiteta može imati jednu ili više pridruženih cenovnika prodaje za cenu projekata:

- Klijent (poslovni kontakt) 
- Mogućnost za poslovanje 
- Ponuda 
- Ugovor za projekat

Povezivanje ovih entiteta sa cenovnikom je naznačeno cenovnikom projekta. Možete da povežete neke cenovnike sa entitetima prodaje Klijent, Mogućnost za poslovanje, Ponuda i Ugovor o projektu.

Podrazumevani cenovnik projekta se ne unosi automatski u zapis klijenta. Međutim, cenovnik projekta možete ručno priložiti zapisu klijenta. Ipak, trebalo bi ručno da priložite cenovnik projekta samo kada imate prilagođeni ugovor o određivanju cena sa klijentom. 

Kada je cenovnik projekta priložen entitetu prodaje, proveravaju se sledeće informacije:

- Da li cenovnik ima kontekst **prodaje**. 
- Da li se valuta cenovnika podudara sa valutom klijenta. 

U ugovoru o projektu, koristi sledeći redosled prioriteta da bi automatski podesio povezane cenovnike projekta:

1. Ponuda
2. Mogućnost za poslovanje
3. Klijent 
4. Globalna podešavanja 

Kada se cenovnik projekta unese podrazumevano, sistem proverava da li se valuta podudara sa valutom klijenta i da li podrazumevani cenovnici koji su uneti imaju kontekst **prodaje**.

Možete da povežete više cenovnika projekta sa entitetima Klijent, Mogućnost za poslovanje, Ponuda i Ugovor o projektu. Ova mogućnost podržava podrazumevane cene za određeni datum za dugoročni ugovor o projektu, gde možete da zahtevate više od jednog cenovnika kako biste u obzir uzeli izmene cena do kojih dolazi zbog inflacije. Međutim, ako se za cenovnike koje povežete sa entitetom Klijent, Mogućnost za poslovanje, Ponuda ili Ugovor o projektu preklapaju datumi stupanja na snagu, podrazumevane cene mogu biti netačne. Zbog toga bi trebalo da proverite da cenovnici projekata sa datumima stupanja na snagu koji se preklapaju nisu povezani sa tim entitetima.

### <a name="deal-specific-price-overrides"></a>Zamene cena za određenu pogodbu

Možete kreirati zamene cena za određenu pogodbu za željene cene u cenovnicima projekata koje se podrazumevano unose za ponudu ili ugovor o projektu.

Ugovor o projektu uvek podrazumevano dobija kopiju glavnog cenovnika prodaje umesto direktne veze do njega. Ovo ponašanje garantuje da se sporazumi o cenama koji su napravljeni sa klijentom za izjave o radu ne menjaju ako se promeni glavni cenovnik.

Međutim, u ponudi možete koristiti glavni cenovnik. Druga mogućnost je da kopirate glavni cenovnik i uredite ga tako da kreirate prilagođeni cenovnik koji se primenjuje samo na tu ponudu. Da biste kreirali novi cenovnik koji je specifičan za ponudu, na stranici **Ponuda** izaberite **Kreiraj prilagođene cene**. Cenovniku projekta specifičan za pogodbu možete da pristupite samo iz ponude. 

Kada kreirate prilagođeni cenovnik projekta, biće kopirane samo komponente projekta cenovnika. Drugim rečima, novi cenovnik kreiran kao kopija postojećeg cenovnika projekta koji je priložen uz ponudu i ovaj novi cenovnik imaju samo povezane cene uloga i cene kategorija transakcija.
  
## <a name="tracking-costs"></a>Praćenje troškova

Project Operations prati troškove korišćenja vremena ljudskih resursa za projekte. Takođe prati druge troškove koji su ostvareni u toku projekta, kao što su putni troškovi.

Kao i kod stopa naplate, stope troškova za ljudske resurse se takođe podešavaju korišćenjem cenovnika. Evo glavnih razlika u ponašanju cenovnika troškova i cenovnika prodaje:

- Stopa troškova resursa se ne može zameniti za određeni projekat, ugovor ili ponudu. Međutim, stope naplate mogu se zameniti na osnovu pogodbe, ukoliko dođe do izmena specifičnih za prirodu pogodbe. 

- Sledeća porudžbina se koristi za rešavanje problema sa cenovnikom troškova:

    1. Cenovnik troškova koji je priložen organizacionoj jedinici.
    2. Cenovnik troškova koji je priložen Project Operations parametrima. S obzirom na to da se cenovnici troškova u mnogim različitim valutama mogu priložiti uz parametre, završava se podudaranje valute ugovorne organizacione jedinice projekta, ugovora ili ponude sa valutom cenovnika troškova.
    3. Kada su u pitanju troškovi, metodi formiranja cena „Provizija preko troškova“ i „Po ceni“ ne primenjuju se na cenovnike troškova. Čak i ako se ovi metodi određivanja cena koriste u stavkama cenovnika troškova da bi se podesili troškovi za kategoriju transakcije, sistem ih zanemaruje i ne unosi se podrazumevana cena koštanja.


[!INCLUDE[footer-include](../includes/footer-banner.md)]