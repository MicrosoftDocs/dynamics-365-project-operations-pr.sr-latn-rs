---
title: Zakažite projekat sa strukturnom analizom posla
description: Kako da planirate projekat sa strukturnom analizom posla u aplikaciji Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cf12cc3bcf061e1daffafb248cfd76809c6444ec
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149830"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a>Planirajte projekat sa strukturnom analizom posla (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Raspored projekta navodi koji posao treba da se obavi, koji resursi će izvršiti posao i vremenski okvir u kom posao treba da se dovrši. Raspored projekta odražava sav posao povezan sa završavanjem projekta na vreme. Jedan od prvih koraka u početnoj fazi projekta je da se napravi raspored projekta. Da biste uspostavili raspored projekta, potrebno je da kreirate strukturnu analizu posla.  
  
 Kreiranje projektne strukture sa strukturnom analizom posla koja vam pomaže da:  
  
- Podelite posao u zadatke kojima je lako upravljati  
  
- Procenite vreme potrebno za dovršenje zadatka  
  
- Podesite zavisnosti i trajanje zadatka  
  
- Odredite uloge koje su potrebne za dovršavanje svakog zadatka  
  
  Raspored projekta strukturnoj analizi posla ima poznati izgled i osećaj, dovršite sa interaktivnim gantogramom.  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a>Kreiranje strukturne analize posla za projekat  
 Kreiranje strukturne analize posla za predstavljanje redosled zadataka u projektu Strukturna analiza posla uključuje zadatke, zahteve za svaki zadatak i informacije o prihodima i troškovima. U strukturnu analizu posla možete dodati:  
  
-   Redosled zadataka u hijerarhiji  
  
-   Druge zadatke, ako ih ima, koji moraju biti dovršeni pre nego što možete pokrenuti zadatak  
  
-   Početni datum, datum prestanka i trajanje zadatka  
  
-   Broj časova potrebnih za zadatak  
  
-   Sve potrebne veštine i obrazovanje za radnike  
  
-   Zaposleni koji su postavljeni na zadatak  
  
-   Procenjeni prihod i troškovi  
  
## <a name="task-types"></a>Tipovi zadatka  
Videćete sledeće vrste zadataka prilikom kreiranja strukturne analize posla:  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| **Osnovni čvor projekta**. | Sažetak najvišeg nivoa za zadatak projekta. Svi drugi projektni zadaci se kreiraju u okviru njega. Ime osnovnog zadatka je ime projekta. Trud, datumi i trajanje korenskog čvora se zasnivaju na vrednostima hijerarhije ispod njega. Nije moguće urediti svojstva korenskog čvora ili izbrišite korenski čvor. | 
| **Rezime ili zadaci spremišta** | Zadatak sažetka je zadatak koji ima podzadatke. Zadatak sažetka nema samostalni trud ili trošak. Njegov trud i trošak su zbirne vrednosti njegovih podzadataka. Možete promeniti ime zadatka sažetka ali ne možete promeniti trud, datume ili vreme trajanja, zato što se oni automatski izračunavaju. Brisanjem zadatka sažetka briše zadatak i sve njegove podzadatke.|  
| **Zadaci čvora lista** | Zadatak čvor lista predstavlja najdetaljniji posao na projektu. Sadrži procenjeni trud, planirani broj resursa, planirane datume početka i završetka i trajanje.|

  
## <a name="task-hierarchy"></a>Hijerarhija zadataka  
 Imate sledeće opcije prilikom kreiranja hijerarhije zadataka:  
  
- **Dodaj zadatak**.   Možete da dodate zadatak u položaj koji odaberete u hijerarhiji zadataka. Ako ne odaberete položaj, novi zadatak se pojavljuje na kraju.  
  
- **Uvlačenje zadatka**.   Uvlačenjem zadatka ga činite podređenim zadatku direktno iznad njega.  
  
- **Izvlačenje zadatka**.   Izvucite zadatak da biste ga učinili tako da nije više podzadatak njegovog prvobitno nadređenog zadatka.  
  
- **Premesti nagore i Premesti nadole**.   Pomeranje zadataka nagore i nadole u hijerarhiji njegovog nadređenog zadatka. Premeštanje zadatka nagore ili nadole nema uticaja na njegov trud, trošak, datume ili trajanje.  
  
## <a name="task-attributes"></a>Atributi zadatka  
 Ime zadatka opisuje posao koji treba da se dovrši. Koristite različite atribute zadatka da biste opisali raspored i zahteve zaposlenih na zadatku.  
  
### <a name="schedule-attributes"></a>Zakazivanje atributa

 - Vrednosti koje dodelite za **Časove truda**, **Broj resursa**, **Datum Početka**, **Datum Završetka**, i **Trajanje** za određivanje rasporeda zadataka. 
 - **Trud** je procena časova potrebnih za dovršavanje zadatka.
 - **Broj resursa** je procena koja menadžera projekta stavlja u zadatak kako bi se pronašao najbolji mogući raspored. 
 - **Trajanje** (u danima) označava broj radnih dana koji će biti potrebni za dovršavanje zadatka.  
  
### <a name="staffing-attributes"></a>Atributi zaposlenih

 - **Uloga**, **Resursa organizacione jedinice**, **Broj resursa**, i **Resursa** za opisivanje zahteva zaposlenima za zadatak. 
 - **Uloga** opisuje vrstu resursa potrebnog za obavljanje zadatka. 
 - **Resurs organizacione jedinice** označava organizacionu jedinicu iz koje su ljudski resursi za taj zadatak; ovo takođe utiče na troškove i procenu prodaje zadatka, pošto se ovo računa za određivanje cene prodaje po jedinici za resurse. 
 - **Resursi** sadrže generičke resurse ili nazvane resurse kada je jedan pronađen.  
  
## <a name="task-dependencies"></a>Zavisnosti zadatka  
 Možete da kreirate prethodne odnose između jednog ili više zadataka u strukturnoj analizi posla. Možete postaviti jednu ili više vrednosti za polje prethodnik na zadacima da biste ukazali na zadatke od kojih će zavisiti. Kada dodelite prethodnu vrednost zadatku, zadatak možete da pokrenete jedino kada dovršite sve prethodne zadatke. Podešavanje ove zavisnosti zadatka dovešće do ponovnog preračunavanja datuma planirane početka zadatka kao najnoviji kraj svih njegovih prethodnika. Povezani uticaj prethodnika na raspored nije ograničen režimom zadatka definisanog u zadatku.  
  
## <a name="task-mode"></a>Režim zadatka  
 Režim zadatka je jedna od važnih činilaca koji određuju zakazivanje zadataka čvora lista. Postoje dva režima zadataka za svaki zadatak: režim automatskog zakazivanja i režim ručnog zakazivanja.  
  
-   **Automatsko zakazivanje**.   Kada podesite režim zadatka na Automatsko zakazivanje, mehanizam za zakazivanje zadataka koristi pravila o praćenju atributa zadataka radi utvrđivanja rasporeda za zadatak:  
  
    -   Prethodni zadaci  
  
    -   Angažovanje  
  
    -   Broj resursa  
  
    -   Datume početka i završetka  
  
-   **Pravila planiranja**.   Datum početka zadatka čvora lista koji nema prethodnih zadataka podrazumevano je zakazan za početak projekta. Trajanje zadatka čvora lista se uvek izračunava kao broj radnih dana između njegovog početka i završetka. Kada se zadatak automatski zakazuje, mehanizam za planiranje prati pravila ispod:  
  
    -   Datumi početka i završetka zadatka uvek moraju biti radni dani u skladu sa kalendarom za planiranje projekta  
  
    -   Datum početka zadatka koji ima prethodne zadatke je podrazumevano poslednji datum završetka prethodnih zadataka  
  
    -   Trud = Broj osoba * Trajanje * časova u standardnom radnom danu kalendara projekta  
  
-   **Ručno planiranje**.   U nekim slučajevima, možda ćete želeti da odstupite od ovih pravila. U ovim slučajevima, možete postaviti režim zadataka na ručno zakazivanje zadataka. Zaustavlja mehanizam za planiranje iz izračunavanja vrednosti za druge atribute zakazivanja. Podešavanje prethodnih zadataka na zadatke uvek utiče na datum početka zavisnog zadatka.  
  
## <a name="create-a-work-breakdown-structure"></a>Kreiranje strukturne analize posla  
  
1.  Idite na **Project Service > Projekti**.  
  
2.  Kliknite na projekat na kome želite da radite.  
  
3.  Na traci u vrhu ekrana izaberite strelicu nadole pored naziva projekta, a zatim kliknite na Strukturnu analizu posla.  
  
4.  Da biste dodali zadatak, kliknite na dugme **Dodaj Zadatak**. Popunite polja za zadatak, a zatim kliknite na **Sačuvaj**.  
  
5.  Nastavite dodavanje zadataka dok se ne završi strukturna analiza posla. Prilikom kreiranja strukturne analize posla, možete uraditi sledeće da biste organizovali svoje zadatke:  
  
    -   Izaberite zadatak i kliknite na dugme **Uvuci** da biste ga premestili u drugi zadatak ili Izvuci da biste premestili izvan nivoa.  
  
    -   Izaberite zadatak i kliknite na dugme **Premesti nagore** ili **Premesti nadole** da biste ga premestili nagore ili nadole na listi.  
  
    -   Kliknite na dugme **Sakrij gantogram** da biste sakrili gantogram i kliknite na dugme **Prikaži gantogram** da biste ga ponovo prikazali.  
  
    -   Izaberite drugi period vremena za gantogram u opciji **Vremenska skala**.  
  
6.  Da biste dodali uloge koje ste naveli u vašu strukturnu analizu posla za članove tima vašeg projekta, kliknite na dugme **Generisanje tima za projekat**.  
  
7.  Kliknite na dugme **Sačuvaj** u donjem desnom uglu ekrana kada završite sa unošenjem izmena.  
  
### <a name="see-also"></a>Takođe pogledajte  
 [Vodič za menadžera projekta](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]