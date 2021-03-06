---
title: Kreiranje i potvrda dnevnika sa ispravkama
description: Ova tema pruža informacije o tome kako da kreirate i potvrdite dnevnik sa ispravkama.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 274f99527804b0db81b26201a22eb5a8cbe86c9a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896973"
---
# <a name="create-and-confirm-correction-journals"></a>Kreiranje i potvrda dnevnika sa ispravkama

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

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


