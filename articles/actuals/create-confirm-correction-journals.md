---
title: Kreiranje i potvrda dnevnika sa ispravkama
description: Ovaj članak pruža informacije o tome kako da kreirate i potvrdite dnevnik sa ispravkama.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 70886aa5a3060fa58461ce215e4de3b7286093e3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928081"
---
# <a name="create-and-confirm-correction-journals"></a>Kreiranje i potvrda dnevnika sa ispravkama

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Povremeno se može pogrešno uneti stavka vremena ili troška. Na primer, konsultant može da odabere pogrešan datum kada kreira stavke vremena ili može da izaberete pogrešan projekat prilikom unosa troška. Ako konsultant ne može da ažurira prosleđene stavke, administrator usluga u pozadini može direktno da ispravi stvarne vrednosti za projekat.

## <a name="correct-approved-time-entries"></a>Ispravne odobrene stavke vremena     

Obavite sledeće korake da biste ispravili pojedinačne ili višestruke stavke za projekat.

1. U oblasti **Prodaja** izaberite **Transakcije**, a zatim izaberite **Odobreno vreme**. 

2. Na listi **Odobreno vreme** pronađite i izaberite jednu odobrenu stavku vremena ili više njih da biste ih ispravili. Možete koristiti filter da biste pronašli povezane stavke. Na primer, možete da filtrirate ID projekta i da izaberete sve odobrene stavke vremena sa tim ID-om projekta.

3. Izaberite **Ispravi stavke**. Novi dnevnik ispravki se automatski kreira, sa dodeljenom vrstom **Ispravka vremena**. Stake koje ste izabrali se dodaju u glavnu knjigu. 

4. Na stranici **Nova glavna knjiga** unesite **Opis** za vaš dnevnik ispravki, a zatim izaberite karticu **Ispravke stavki vremena**.  

5. U odeljku **Nove vrednosti za stavke vremena** po potrebi ažurirajte polja ispravnim informacijama. Na primer, možete da promenite dodeljeni projekat ili resurs koji je moguće rezervisati.

6. Izaberite **Pregled**. U dijalogu izaberite **U redu**. Na kartici **Stavke u glavnoj knjizi** možete videti listu originalnog trenutnog stanja koje je povezano sa izabranim stavkama vremena koje su opozvane i sa ispravljenim odgovarajućim stavkama koje su kreirane. Ako je potrebno da se izvrše dodatne ispravke, ponovite korake 5 i 6. 

    > [!NOTE]
    > Sve ispravljene stvarne vrednosti imaće iste vrednosti koje ste izabrali u odeljku **Nove vrednosti za stavke vremena**.

7. Ako se ispravke pojave kako se očekuje, izaberite **Potvrdi**. U dijalogu izaberite **U redu**.

8. Vratite se na oblast **Prodaja**, izaberite **Projekti**, a zatim otvorite projekat za koji ste upravo ažurirali stavke vremena. 

9. Na stranici **Projekti**, na kartici **Stvarne vrednosti**, pogledajte promene koje ste izvršili. 

    > [!NOTE]
    > Ako kartica **Aktuelno** nije vidljiva, izaberite **Povezano** > **Stvarne vrednosti**.  

10. Na listi **Vezani prikaz stvarnih vrednosti** možete videti da su originalne stavke vremena koje su opozvane i dalje navedene, kao što su navedene i odgovarajuće ispravljene stavke vremena. 

 
## <a name="correct-approved-expense-entries"></a>Ispravne odobrene stavke troškova

Obavite sledeće korake da biste ispravili jednu stavku troškova ili više njih. 

1. U oblasti **Prodaja** u levom oknu za navigaciju, u okviru **Transakcije**, izaberite **Odobreni troškovi**.

2. Na listi **Odobreni troškovi** izaberite projekat koji želite da ispravite, a zatim izaberite **Ispravi stavke**. Kreira se novi dnevnik ispravki sa dodeljenom vrstom **Ispravka troška**. 

3. Na stranici **Novi dnevnik** unesite **Opis** za ispravku a na kartici **Ispravka troška**, u odeljku **Nove vrednosti za troškove**, izaberite polja podataka koja želite da ispravite za odabrane stavke troška. Na primer, možete da dodelite trošak drugom **Projektu** ili da ispravite stavku **Kategorija troška**, **Datum troška** ili **Resurs koji može da se rezerviše**.

4. Izaberite **Pregled**. U dijalogu izaberite **U redu**. 

5. Proverite ispravke na kartici **Stavke u glavnoj knjizi**. Možete videti listu originalnog trenutnog stanja koje je povezano sa izabranim stavkama troškova koje su opozvane i sa ispravljenim odgovarajućim stavkama koje su kreirane.

6. Ako su ispravljene vrednosti prema očekivanju, izaberite **Potvrdi**. U dijalogu izaberite **U redu.** Ako se vrednosti ne prikazuju kako se očekuje, izaberite **Otkaži** da biste se vratili na listu **Odobreni troškovi**. Ponovite korake od 2 do 5. 

7. Nakon što potvrdite dnevnik ispravki, vratite se na projekat ili projekte koje ste ažurirali da biste pogledali svoje izmene.

8. Na stranici projekta, na kartici **Aktuelno**, pregledajte listu **Vezani prikaz stvarnih vrednosti**. Navedene su izvorne stavke i ispravljene stavke.


## <a name="correct-approved-material-usage-logs"></a>Ispravljanje evidencija odobrenog korišćenja materijala

Obavite sledeće korake da biste ispravili najmanje jednu stavku korišćenja materijala.

1. U oblasti **Prodaja** u levom oknu za navigaciju, u okviru **Transakcije**, izaberite **Stvarne vrednosti**.

2. Na listi **Stvarne vrednosti** koristite filtere kolona da biste izabrali klasu transakcija **Materijal**, tako da se prikazuju samo stvarne vrednosti za materijale. Koristite druge filtere kolona da biste dodatno ograničili prikazane stvarne vrednosti. Nakon što pronađete željeni skup stvarnih vrednosti, izaberite stvarne vrednosti, a zatim izaberite stavku **Ispravni unosi**. Novi dnevnik ispravki se automatski kreira, a dodeljuje se tip **Ispravka materijala**.

3. Na stranici **Nova glavna knjiga**, u polju **Opis**, unesite opis za ispravku. Zatim, na kartici **Korekcija materijala**, u odeljku **Nove vrednosti za materijale** izaberite polja podataka koja želite da ispravite za izabrane redove materijala. Na primer, možete da dodelite materijal drugom projektu ili da ispravite proizvod, datum materijala ili podugovor.

4. Izaberite **Pregled**. Zatim, u dijalogu izaberite **U redu**.

5. Na kartici **Stavke u glavnoj knjizi** proverite ispravke. Možete videti listu originalnih stvarnih vrednosti koje su povezane sa izabranim stavkama materijala koje su opozvane i sa ispravljenim odgovarajućim stavkama koje su kreirane.

6. Ako su ispravljene vrednosti prema očekivanju, izaberite **Potvrdi**. Zatim, u dijalogu izaberite **U redu**. Ako vrednosti nisu kako se očekuje, izaberite **Otkaži** da biste se vratili na listu **Stvarne vrednosti**. Zatim ponovite korake od 2 do 5.

7. Nakon što potvrdite dnevnik ispravki, vratite se na projekat ili projekte koje ste ažurirali da biste pogledali svoje izmene.

8. Na stranici projekta, na kartici **Aktuelno**, pregledajte listu **Vezani prikaz stvarnih vrednosti**. Navedene su izvorne stavke i ispravljene stavke.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
