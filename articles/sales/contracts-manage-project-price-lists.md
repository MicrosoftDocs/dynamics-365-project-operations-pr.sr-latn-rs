---
title: Upravljanje cenovnicima projekata u ugovorima za projekat
description: Ova tema pruža informacije o upravljanju cenovnicima za projekat na ugovorima za projekat.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2cfac6eda64d1d8e578115bba07942a7d786328f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278615"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Upravljanje cenovnicima projekata u ugovorima za projekat

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Ugovori za projekat u usluzi Dynamics 365 Project Operations osmišljeni su tako da podržavaju više efektivnih prodajnih cenovnika na ugovoru. U usluzi Project Operations postoji novi pridruženi entitet koji se zove **Cenovnici projekta**. Taj entitet ima relaciju „jedan prema više“ sa ugovorom za projekat.

Cenovnici projekata se koriste za određivanje transakcija vremena i troškova na projektu. Kada ugovor ima jedan ili više cenovnika projekata, ovi cenovnici se koriste za određivanje cene za stavke vremena i troškova, kao i za trenutno stanje na projektima koji su povezani sa ugovorom preko predmeta ugovora.

Kada u ugovoru za projekat ne postoje cenovnici projekta, videćete poruku upozorenja da ne postoje cenovnici projekta, pa cene za vaše procene, stvarni rad na projektu i troškove neće biti određene. Neće biti navedene vrednosti cena prodaje.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Povezivanje ili prekidanje veze cenovnika projekta na ugovoru o projektu

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-and-expenses"></a>Napravite ili pridružite određeni cenovnik za procenu rada i troškova zasnovanih na projektu

1. U ugovoru za projekat, izaberite karticu **Cenovnici projekta**.
2. U podformi izaberite **+ Dodaj novi cenovnik projekta**.
3. Na klizaču **Brzo kreiranje**, izaberite cenovnik. 

  Padajuća lista prikazuje sve cenovnike kojima je kontekst postavljen na **Prodaja**, pri čemu se valuta na cenovniku podudara sa valutom iz ugovora.
  
4. Unesite opis veze sa cenovnikom projekta, izaberite **Sačuvaj**, a zatim zatvorite klizač **Brzo kreiranje**.

   Povezivanje cenovnika projekta je kreirano.
   
5. Ponovite korake 1-4 da biste ugovoru za projekat pridružili više od jednog cenovnika projekta. Više cenovnika projekta kreirajte samo ako imate različitu efektivnost datuma na svakom povezanom cenovniku projekta.

> [!NOTE]
> Project Operations ne podržava preklapanje datumske efektivnosti cenovnika projekta. Ako postoji više cenovnika projekta za transakciju sa datim datumom, cena te transakcije biće podrazumevano postavljena na nulu.

### <a name="remove-a-project-price-list-association"></a>Uklanjanje veze cenovnika projekta

- Izaberite cenovnik projekta, a zatim izaberite **Izbriši cenovnik ugovora za projekat** na podformi. 

  Cenovnik se uklanja iz cenovnika projekta na ugovoru. Sam cenovnik neće biti izbrisan. Biće izbrisana samo veza sa ugovorom.

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>Podešavanje automatskog postavljanja cenovnika projekta na ugovoru

Cenovnik projekta se može postaviti kao podrazumevana lista na ugovoru za projekat. Ovo podešavanje može da pomogne da svi ugovori u vašoj organizaciji uvek započinju standardnim cenovnikom za taj cenovni period.

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>Podešavanje organizacionog postavljanja za cenovnike projekta

1. Idite na **Podešavanja** > **Opšti podaci**, a zatim izaberite **Parametri**.
2. Na stranici liste **Aktivni parametri**, izaberite i dvaput kliknite na zapis da biste ga otvorili. Dok dvaput kliknete, pazite da ne kliknete na vrednost polja koja je hiperveza. 
3. Na stranici **Aktivni parametri**, izaberite karticu **Cenovnik**. Podforma prikazuje listu zadatih cenovnika. Ovo je lista standardnih troškova i prodajnih cenovnika. Ako imate cenovnik **prodaje** koji je ovde povezan za svaku valutu u kojoj prodajete, to obezbeđuje da cenovnik prodaje bude podrazumevan za bilo koji ugovor koji kreirate za klijente koji obavljaju transakcije u toj valuti.

### <a name="set-up-a-customer-specific-project-price-list"></a>Podešavanje cenovnika projekta specifičnog za klijenta

Takođe možete da podesite cenovnike projekta specifične za klijenta kada uspostavite glavni ugovor o cenama sa svojim klijentima.

1. Idite na stavku **Prodaja** > **Klijenti**.
2. Sa liste aktivnih naloga izaberite klijenta za kojeg imate poseban cenovnik.
3. Izaberite zapis klijenta da biste ga otvorili, a zatim izaberite karticu **Cenovnici projekta**. Podforma prikazuje listu cenovnika projekata specifičnih za ovog klijenta. 
4. Kreirajte novu vezu cenovnika ovde da biste dobili cenovnik projekta specifičan za ovog klijenta.

## <a name="custom-pricing-on-a-project-contract"></a>Prilagođeno određivanje cena na ugovoru za projekat

Kada uspostavite organizacione i podrazumevane cenovnike projekta specifične za vaše klijente, automatski vaši ugovori za projekat će se automatski kreirati sa vezama na cenovnike projekta. Međutim, cenovnici projekta na ugovoru o projektu se uvek kopiraju sa datumom i nazivom ugovora koji im je dodat. Menadžeri naloga i projekata mogu tada započeti uređivanje cena na ovim primercima. Ove promenjene cene će se primenjivati samo na ovaj ugovor za projekat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]