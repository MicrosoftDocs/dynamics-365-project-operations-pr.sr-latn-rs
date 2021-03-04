---
title: Masovne ispravke trenutnog stanja kreiranog odobrenim stavkama vremena i troška
description: Ova tema objašnjava kako administrator može da izvrši pojedinačne ili masovne ispravke prethodno odobrenih stavki vremena ili troška ukoliko naplata nije potpuna.
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 063c4d017f5904f09c3c239bfa432a128872e4d7
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144970"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a>Masovne ispravke trenutnog stanja kreiranog odobrenim stavkama vremena i troška

[!include [banner](../includes/psa-now-project-operations.md)]

Povremeno se može pogrešno uneti stavka vremena ili troška. Na primer, konsultant može da odabere pogrešan datum prilikom kreiranja stavke vremena ili može da prenese brojeve prilikom unosa troška. Ako konsultant ne može da obavi ažuriranja prosleđenih stavki, administrator može direktno da ispravi stavku za projekat.

Da biste dovršili procedure u ovoj temi, trebaće vam dozvole administratora.

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

Na primer, na sledećoj slici postoje dve stavke čija je količina 8,00 a koje imaju zaduženja navedena u koloni Iznos. Uz to, postoje dve stavke čija je količina -8,00 koje prikazuju zadužene iznose u koloni Iznos. Ove ispravke svode količinu na nulu.

![Lista vezanog prikaza stvarnih vrednosti](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a>Ispravne odobrene stavke troškova

Obavite sledeće korake da biste ispravili jednu stavku troškova ili više njih. 

1. U oblasti **Prodaja** u levom oknu za navigaciju, u okviru **Transakcije**, izaberite **Odobreni troškovi**.

2. Na listi **Odobreni troškovi** izaberite projekat koji želite da ispravite, a zatim izaberite **Ispravi stavke**. Kreira se novi dnevnik ispravki sa dodeljenom vrstom **Ispravka troška**. 

3. Na stranici **Novi dnevnik** unesite **Opis** za ispravku a na kartici **Ispravka troška**, u odeljku **Nove vrednosti za troškove**, izaberite polja podataka koja želite da ispravite za odabrane stavke troška. Na primer, možete da dodelite trošak drugom **Projektu** ili da ispravite stavku **Kategorija troška**, **Datum troška** ili **Resurs koji može da se rezerviše**.

4. Izaberite **Pregled**. U dijalogu izaberite **U redu**. 

5. Proverite ispravke na kartici **Stavke u glavnoj knjizi**. Možete videti listu originalnog trenutnog stanja koje je povezano sa izabranim stavkama troškova koje su opozvane i sa ispravljenim odgovarajućim stavkama koje su kreirane.

6. Ako su ispravljene vrednosti prema očekivanju, izaberite **Potvrdi**. U dijalogu izaberite **U redu.** Ako se vrednosti ne prikazuju kako se očekuje, izaberite **Otkaži** da biste se vratili na listu **Odobreni troškovi**. Ponovite korake od 2 do 5. 

> [!NOTE]
> Ispravljene stvarne vrednosti imaće iste vrednosti koje ste izabrali u odeljku **Nove vrednosti za troškove**.

7. Nakon što potvrdite dnevnik ispravki, vratite se na projekat ili projekte koje ste ažurirali da biste pogledali svoje izmene.  

8. Na stranici projekta, na kartici **Aktuelno**, pregledajte **Vezani prikaz stvarnih vrednosti**. Navedene su izvorne stavke i ispravljene stavke. Sledeća slika prikazuje izvorne iznose stavke troška i odgovarajuće ispravljene iznose stavke troška. 

![Trošak_stvarna vrednost](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)
