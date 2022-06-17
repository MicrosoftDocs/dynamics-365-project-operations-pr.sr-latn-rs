---
title: Upravljanje cenovnicima projekata u ugovorima za projekat
description: Ovaj članak pruža informacije o upravljanju cenovnicima projekta u ugovorima o projektu.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 23b9e6f9bc3e4bc3fb03de62064644dd58da34c7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926195"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Upravljanje cenovnicima projekata u ugovorima za projekat

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Ugovori za projekat u usluzi Dynamics 365 Project Operations osmišljeni su tako da podržavaju više efektivnih prodajnih cenovnika na ugovoru. U usluzi Project Operations postoji novi pridruženi entitet koji se zove **Cenovnici projekta**. Taj entitet ima relaciju „jedan prema više“ sa ugovorom za projekat.

Cenovnici projekata se koriste za određivanje vremena, materijala i transakcija troškova na projektu. Kada ugovor ima jedan ili više cenovnika projekata, ti cenovnici se koriste za određivanje cene za vreme, materijal, procenu troškova i trenutno stanje projekata koji su povezani sa ugovorom preko predmeta ugovora.

Kada na ugovoru o projektu ne postoje cenovnici za projekat, videćete poruku upozorenja da ne postoje cenovnici za projekat, a cena za vaše procene, stvarni rad na projektu, materijal i evidentirane troškove neće biti određena. Neće biti navedene vrednosti cena prodaje.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Povezivanje ili prekidanje veze cenovnika projekta na ugovoru o projektu

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a>Napravite ili povežite određeni cenovnik za procenu rada, materijala i troškova zasnovanih na projektu

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

Cenovnik projekta može se postaviti kao zadati cenovnik projekta. Ovo podešavanje obezbeđuje da svi ugovori u vašoj organizaciji uvek započinju standardnim cenovnikom projekata za taj period cena.

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
