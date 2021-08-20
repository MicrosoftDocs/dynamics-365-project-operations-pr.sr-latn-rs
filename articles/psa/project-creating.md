---
title: Rasporedi projekata
description: Ova tema pruža informacije o tome kako da kreirate raspored.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: 192fbe7f26a2bd060ffe9bc0b1eea50b9431bca4696e3da1d94bf53158e026a6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998433"
---
# <a name="project-schedules"></a>Rasporedi projekata 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Raspored projekta navodi koji posao treba da se završi, koji resursi će obavljati posao i vremenski okvir u kom posao mora da se završi. On odražava sav posao povezan sa završavanjem projekta na vreme. U aplikaciji Dynamics 365 Project Service Automation, kreirate raspored projekata tako što posao delite na upravljive zadatke, procenite vreme koje je potrebno za obavljanje svakog zadatka, podešavate zavisne elemente zadatka, trajanje zadatka i procenite generičke resurse koji će obavljati zadatke. Raspored projekata kreiran je na kartici **Raspored** stranice projekta.
 
## <a name="tasks"></a>Zadaci

Prvi korak u kreiranju projektnog rasporeda je raščlanjivanje posla na upravljive delove. Raspored u aplikaciji PSA podržava sledeće funkcije:

- Osnovni čvor projekta.
- Rezime ili zadaci spremišta
- Zadaci čvora lista

### <a name="project-root-node"></a>Osnovni čvor projekta.

Osnovni čvor projekta je rezime zadatka najvišeg nivoa za projekat. Svi drugi projektni zadaci se kreiraju u okviru njega. Ime osnovnog čvora je uvek podešeno na ime projekta. Aktivnosti, datumi i trajanje osnovnog čvora se rezimiraju na osnovu vrednosti u hijerarhiji ispod njega. Ne možete uređivati svojstva osnovnog čvora. Takođe ne možete izbrisati osnovni čvor.

### <a name="summary-or-container-tasks"></a>Rezime ili zadaci spremišta 

Rezimirani zadaci imaju podzadatke ili zadatke kontejnera ispod sebe. Oni nemaju sopstvene radne aktivnosti ni troškove. Umesto toga, njihove radne aktivnosti i troškovi su zbirna vrednost radnih aktivnosti i troškova njihovih zadataka u kontejneru. Datum početka rezimiranog zadataka je datum početka zadataka u kontejneru, a datum završetka je datum završetka zadataka u kontejneru. Naziv rezimiranog zadatka može se uređivati, ali svojstva zakazivanja (aktivnosti, datumi i trajanje) ne mogu se uređivati. Ako obrišete rezimirani zadatak, brišete i sve njegove zadatke u kontejneru.

### <a name="leaf-node-tasks"></a>Zadaci čvora lista

Zadaci čvora lista predstavljaju najdetaljniji posao na projektu. Oni imaju procenjene aktivnosti, resurse, planirane datume početka i završetka i trajanje.
 
## <a name="creating-a-task-hierarchy"></a>Kreiranje hijerarhije zadataka

Možete da kreirate hijerarhiju zadatka pomoću sledećih opcija:

- Dugme **Dodaj zadatak**
- Dugme **Uvuci zadatak**
- Dugme **Izvuci zadatak**
- Dugmad **Premesti nagore** i **Premesti nadole**
- Pristupačnost i tasterske prečice

### <a name="add-task"></a>Dodavanje zadatka

Dugme **Dodaj zadatak** omogućava kreiranje novog zadatka u hijerarhiji. Ako ne odaberete poziciju, zadatak se umeće na kraju. 

ID rasporeda dodeljuje se svakom zadatku. ID rasporeda predstavlja dubinu i položaj zadatka u hijerarhiji. Koristi šematsko numerisanje. Za zadatke na prvom nivou pod osnovnim čvorom projekta, koristi se šema numerisanja od 1, 2, 3 i tako dalje. Za zadatke ispod prvog nivoa, koristi se šema numerisanja od 1,1; 1,2; 1,3 i tako dalje.

### <a name="indent-task"></a>Uvlačenje zadatka

Kada je zadatak razveden, postaje podređen zadatku koji se nalazi neposredno iznad njega. ID rasporeda zadatka se zatim ponovo izračunava tako da se zasniva na ID-u rasporeda njegovog novog nadređenog elementa i sledi šemu numerisanja. Nadređeni zadatak je sada rezimirani zadatak ili zadatak kontejnera. Stoga postaje zbirna vrednost podređenih zadataka.

### <a name="outdent-task"></a>Izvlačenje zadatka 

Kada se zadatak izvuče, to više nije podređeni zadatak nadređenog zadatka. ID rasporeda se zatim ponovo izračunava tako da odražava ažuriranu dubinu i položaj zadatka u hijerarhiji. Aktivnosti, troškovi i datumi prethodnog nadređenog zadatka se ponovo izračunavaju kako ne bi uključili ovaj zadatak.

### <a name="move-up-and-move-down"></a>Premeštanje nagore i nadole 

Dugmad **Premesti nagore** i **Premesti nadole** menjaju položaj zadatka unutar nadređene hijerarhije. Promene ove vrste ne utiču na aktivnosti, troškove, datume niti trajanje zadatka. Utiču samo na ID rasporeda zadatka. ID rasporeda se ponovo izračunava tako da odražava novi položaj podređenih zadatka u listi nadređenog zadatka.

### <a name="accessibility-and-keyboard-shortcuts"></a>Pristupačnost i tasterske prečice

Mreža **Raspored** je potpuno dostupna i može se koristiti sa čitačima ekrana kao što su Narrator, JAWS ili NVDA. Kroz oblast mreže možete se kretati pomoću tastera sa strelicama (kao u programu Microsoft Excel), možete koristiti taster Tab da biste se kretali kroz interaktivne elemente korisničkog interfejsa, a pomoću tastera sa strelicom nadole, tastera Enter ili razmaknice možete da izaberete i pozovete padajuće menije. Zaglavlja kolona su takođe interaktivna. Možete da sakrijete i prikažete kolone, koristite tastere Tab i strelice da biste se kretali kroz zaglavlja kolona, kao i dugmad za radnje na traci sa alatkama. Pored toga, možete da koristite sledeće prečice na tastaturi:

- **Osveži**: ALT+SHIFT+F5
- **Dodaj**: ALT+SHIFT+Insert
- **Izbriši**: ALT+SHIFT+Delete
- **Pomeri nagore/nadole**: ALT+SHIFT+strelice nagore/nadole
- **Uvuci/izvuci**: ALT_SHIFT+strelice nalevo/nadesno
- **Razvij/skupi hijerarhije**: ALT+SHIFT+tasteri plus/minus

## <a name="task-attributes"></a>Atributi zadatka

Ime zadatka opisuje posao koji mora da se dovrši. U aplikaciji PSA, atributi koji su povezani sa zadatkom opisuju raspored zadatka i njegove potrebe za angažovanjem resursa.

> ![Atributi zadatka.](media/project-2.png)
 
### <a name="schedule-attributes"></a>Zakazivanje atributa

Atributi **Aktivnosti**, **Datum početka**, **Datum završetka** i **Trajanje** definišu raspored za zadatak.

U dodatne atribute rasporeda spadaju:

- **Sati aktivnosti**: Unesite procenu sati potrebnih za ispunjavanje zadatka. 
- **Trajanje**: Navedite broj radnih dana koji su potrebni za dovršavanje zadatka.
- **ID rasporeda** : Ovaj automatski generisan ID koristi se za naručivanje zadataka u hijerarhiji. Zavisni elementi između zadataka upravljaju stvarnim redosledom kojim se zadaci obavljaju.
 
### <a name="staffing-attributes"></a>Atributi zaposlenih

Atributima angažovanja se pristupa u polju **Resursi** u rasporedu. Možete potražiti postojeći resurs ili kliknite na **Kreiraj** i u oknu **Brzo kreiranje** dodajte člana projektnog tima kao novi resurs.

Polja **Uloga**, **Jedinica za obezbeđivanje resursa** i **Naziv pozicije** se koriste za opisivanje potreba za angažovanjem resursa na zadatku. Ovi atributi angažovanja zajedno sa rasporedom zadataka koriste se za pronalaženje dostupnih resursa za obavljanje ovog zadatka.

**Uloga** - Navedite vrstu resursa koji je potreban za izvršavanje zadatka.

**Jedinica za obezbeđivanje resursa** - Navedite jedinicu iz koje treba dodeliti resurse za zadatak. Ovaj atribut utiče na procenu troškova i prodaje za zadatak ako su stope troškovi i naplate za resurs podešene na osnovu jedinica za obezbeđivanje resursa.

**Naziv pozicije** - Unesite prepoznatljivo ime za generički resurs koje služi kao čuvar mesta za resurs koji će na kraju obaviti posao.

Polje **Resursi** sadrži naziv pozicije generičkog resursa ili imenovanog resursa kada ga neko pronađe.

Polje **Kategorija** sadrži vrednosti koje ukazuju na širi tip posla u koji se zadatak može grupisati. Ovo polje ne utiče na zakazivanje niti obezbeđivanje resursa. Koristi se samo za izveštavanje.

### <a name="task-dependencies"></a>Zavisnosti zadatka 

Raspored u aplikaciji PSA možete da koristite za kreiranje odnosa prethodnika između zadataka. Polje **Prethodni zadatak** u okviru stavke **Zadaci** uzima jednu ili više vrednosti kako bi označio zadatke od kojih zadatak zavisi. Kada dodelite prethodne vrednosti zadatku, zadatak možete da pokrenete jedino kada dovršite sve prethodne zadatke. Zbog zavisnih elemenata, planirani datum početka zadatka vraća se na datum kada su prethodni zadaci završeni.

Režim zadatka nema uticaja na ažuriranja koja se obavljaju na datum početka i završetka prethodnih/zavisnih zadataka.

## <a name="task-mode"></a>Režim zadatka 

Režim zadatka određuje zakazivanje zadataka čvora lista. PSA podržava dva režima zadataka za svaki zadatak: automatsko zakazivanje i ručno zakazivanje.

### <a name="auto-scheduling"></a>Automatsko zakazivanje 
 
Kada je režim zadatka podešen na **Automatsko zakazivanje**, mehanizam za zakazivanje zadataka koristi pravila rasporeda za atribute zadataka radi utvrđivanja rasporeda zadatka:

#### <a name="scheduling-rules"></a>Pravila zakazivanja

Ako zadatak čvora lista nema prethodne zadatke, njegov datum početka se podrazumevano podešava na zakazani datum početka projekta. Trajanje zadatka čvora lista se uvek izračunava kao broj radnih dana između njegovog početka i završetka. Kada se zadatak automatski zakazuje, mehanizam za zakazivanje prati ova pravila:

- Datumi početka i završetka zadatka moraju biti radni dani, u skladu sa kalendarom za zakazivanje u okviru projekta. 
- Za bilo koji zadatak koji ima prethodne zadatke, datum početka se podrazumevano podešava na poslednji datum završetka prethodnih zadataka.
- Aktivnosti se izračunavaju pomoću ove formule: Broj ljudi × Trajanje × Sati u uobičajenom radnom danu u kalendaru projekta.

### <a name="manual-scheduling"></a>Ručno planiranje

Ako pravila automatskog zakazivanja ne zadovoljavaju vaše potrebe, možete da podesite režim zadatka na **Ručno zakazano**. Podešavanje zaustavlja mehanizam za zakazivanje, pa ne može da izračuna vrednosti drugih atributa zakazivanja. Bez obzira na režim zadatka, ako za zadatke podesite prethodne zadatke, uvek utičete na datum početka zavisnog zadatka.


[!INCLUDE[footer-include](../includes/footer-banner.md)]