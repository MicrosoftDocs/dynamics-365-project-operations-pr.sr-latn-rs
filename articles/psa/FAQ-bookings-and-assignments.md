---
title: Rezervacije resursa i kako su one povezane sa dodelom zadataka
description: Ova tema pruža informacije o tome kako upravljati imenovanim resursima, rezervacijama resursa i dodelama zadataka, kao i kakav je njihov međusobni odnos.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 83b1bf39c71275f2e8e4ec20082f711154696586
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286220"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a>Rezervacije resursa i kako su one povezane sa dodelom zadataka

[!include [banner](../includes/psa-now-project-operations.md)]

Imenovani resursi mogu biti rezervisani za projektni tim i dodeljeni projektnim zadacima na dva načina:

- Resurs može biti direktno rezervisan za projekat, a zatim dodeljen projektnim zadacima.
- Zadaci mogu biti dodeljeni generičkom resursu, koji se zatim koriste za pronalaženje i zamenu generičkog resursa imenovanim resursom. 

U oba slučaja, čim rezervisanja resursa rezerviše kapacitet resursa.

Menadžer projekta koji planira projekat je vlasnik plana i rasporeda projekta. Korišćenjem generičkog resursa za dodelu, a zatim generisanjem zahteva za resurs iz njega, menadžer projekta može da rezerviše resurse za projekat pomoću skica navedenih u planu projekta. On može da rezerviše resurse za projekat, a zatim da im dodeljuje zadatke. Međutim, ne postoji nijedan način da uskladi skice rezervacije sa skicama zadataka. Rezervacije ne utiču na raspored projekta.

Uzmite za primer složeni projekat sa više zadataka koji se preklapaju na kojima više resursa istog tipa moraju istovremeno da rade. Ako je resursu zadata kontura koja se razlikuje od konture skupa njihovih dodela, teško je izmeniti zadatke kako bi se uklopili u konturu rezervacija za njihove izolovane zadatke i njihove prvobitne konture.

U primeru u nastavku, ukupno angažovanje potrebno za isti resurs iz skupa od četiri zadatka je 62 sata tokom dvonedeljnog perioda, a postoji određena kontura. Ako je resurs Branko rezervisan za 62 radna sata tokom te iste dve sedmice, ali sa drugom konturom, zahtev i rezervacije su usklađeni.

| **Konture zadatka**    | **Ukupno časova** | pon 6/4 | uto 6/5 | sre 6/6 | čet 6/7 | pet 6/8 | sub 6/9 | ne 6/10 | pon 6/11 | uto 6/12 | sre 6/13 | čet 6/14 | pet 6/15 |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Zadatak 1               | 24              | 8      | 8      | 4      |        |        |        |         |         |         | 4       |         |         |
| Zadatak 2               | 16              |        |        | 4      | 4      |        |        |         | 8       |         |         |         |         |
| Zadatak 3               | 10.              |        |        |        |        | 4      |        |         |         | 4       |         | 2       |         |
| Zadatak 4               | 12              |        |        |        |        |        |        |         |         |         | 4       |         | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| **Zbirovi**           | 62              | 8      | 8      | 8      | 4      | 4      |        |         | 8       | 4       | 8       | 2       | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a>Brankova dostupnost
| **Rezervacija   resursa** | **Ukupno časova** | pon 6/4 | uto 6/5 | sre 6/6 | čet 6/7 | pet 6/8 | sub 6/9 | ne 6/10 | pon 6/11 | uto 6/12 | sre 6/13 | čet 6/14 | pet 6/15 |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Branko                    | 62              | 4      | 4      | 8      | 8      | 8      |        |         | 4       | 4       | 8       | 8       | 6.       |

Međutim,ne postoji sistematski način da dodeljujete konturu rezervisanih sati zadacima iz dana u dana. Ako je menadžer projekta spreman da promeni raspored projekta kako bi izašao u susret dostupnosti resursa, moraće da ukloni dodelu i da revidira sve zadatke kako bi odgovaraju konturama rezervacije.

U slučaju kada je organizacija zadatak planiranja dala i menadžeru projekta i menadžeru resursa, menadžera projekta postavlja raspored, što obuhvata i konturisanje potrebnog posla. Ne bi trebalo da menadžer resursa može da utiče na raspored bez znanja menadžera projekta promenom kontura angažovanja prilikom rezervacije stvarnih resursa. Ako menadžer resursa ispunjava nešto drugo, a ne šta je menadžer projekta zahtevao, oni moraju da postignu dogovor o potrebnim promenama u rasporedu projekta.

Budući da rezervacije i dodele nisu čvrsto povezane, moguće je rezervisati konture koje se razlikuju od kontura zadatka ili promeniti dodele kako bi se dobile okolnosti u kojima rezervacije i dodele nisu usklađene.

**Prikaz usklađenosti** menadžeru projekta dozvoljava da vidi rezervacije i dodele za svakog člana projektnog tima. Prikaz koristi boje i senčenje za prikazivanje gde postoji nepodudaranje između rezervacija i dodela za članove tima. Na osnovu ovih informacija, menadžer projekta može da preduzima korektivne radnje. On može da proširi rezervaciju resursa za predmete u kojima postoje dodele, a nema rezervacija, ili može da otkaže rezervacije tako gde su resursi rezervisani, ali imaju nema dodele.

> [!NOTE]
> Ako premestite zadatak koji ste sami skicirali, te skice ostaju. Konture se ponovo generišu u skladu sa kalendarom projekta kako bi odrazile promene u radnom vremenu i praznicima. To je tako projektovano jer sistem ne zna nameru prvobitne skice i ne može da utvrdi da li ima smisla zadržati tu skicu u novom vremenskom periodu. Pošto rezervacije i dodele nisu povezane, rezervacije zadržavaju prvobitne skice rezervacije. U tom slučaju, moraćete da otkažete i ponovo rezervišete za konturu nove dodele.



[!INCLUDE[footer-include](../includes/footer-banner.md)]