---
title: Upravljanje cenovnicima projekata u ponudama za projekat
description: Ova tema pruža informacije o radu sa cenovnicima za projekat u ponudama. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4013d2e8cc0d2329f824a17484ee6f4a054a390e
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083503"
---
# <a name="manage-project-price-lists-on-project-quotes-sales"></a>Upravljanje cenovnicima projekata u ponudama za projekat (Prodaja)

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Ponude za projekte su dizajnirane da podržavaju više efektivnih prodajnih cenovnika. Uz Dynamics 365 Project Operations, dodaje se novi pridruženi entitet pod nazivom **Cenovnici za projekat**. Ovaj entitet ima relaciju „1 prema više“ sa ponudom za projekat.

Cenovnici projekata se koriste za određivanje transakcija vremena i troškova na projektu. Kada ponuda ima jedan ili više cenovnika projekata, ovi cenovnici se koriste za procene cene vremena i troškova i stvarne vrednosti koje su povezane sa ponudom preko stavke ponude.

Kada na ponudi za projekat ne postoje cenovnici projekata, dobićete poruku upozorenja. U poruci se navodi da pošto ne postoje cenovnici projekata, neće biti određena cena za procenjeni i stvarni rad i troškove na projektu. Umesto toga, imaće nultu (0) cenu za vrednosti prodaje.

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Pridružite ili razdvojite cenovnik projekta u ponudi za projekat

Da biste kreirali ili izabrali određeni cenovnik za procenu rada i troškova zasnovanih na projektu, izvršite sledeće korake.

1. U ponudi, izaberite karticu **Cenovnik za projekat** i u podformi izaberite **+ Dodaj novi cenovnik za projekat**.
2. Na stranici Brzo kreiranje, izaberite cenovnik. Padajuća lista prikazuje sve cenovnike kojima je kontekst podešen na **Prodaja** a valuta se podudara sa valutom na ponudi.
4. Unesite opis za povezivanje cenovnika projekta i izaberite stavku **Sačuvaj i zatvori**.

Povezivanje cenovnika projekta je kreirano.

Ovaj postupak možete ponoviti ako treba da dodate više od jednog cenovnika projekta u ponudu za projekat. Više cenovnika projekta kreirajte samo ako imate različite datume stupanja na snagu za svaki od povezanih cenovnika projekata.

> [!NOTE]
> Project Operations ne podržava preklapanje datuma stupanja na snagu cenovnika za projekat. Ako postoji više cenovnika projekta za transakciju sa datim datumom, cena te transakcije biće podrazumevano nula (0).
Da biste uklonili povezivanje cenovnika projekta, izaberite cenovnik projekta, a zatim izaberite **Izbriši cenovnik projekta za ponudu**. Cenovnik se uklanja iz cenovnika projekta za ponudu, ali sam cenovnik se ne briše. Briše se samo povezivanje sa ponudom.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Podešavanje podrazumevanih cenovnika projekta u ponudi

Cenovnici projekta se mogu podesiti na podrazumevane vrednosti u ponudi projekta. Ova postavka obezbeđuje da sve ponude u vašoj organizaciji uvek počinju sa standardnim cenovnikom za taj cenovni period.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Podešavanje podrazumevanih cenovnika projekta za organizaciju

1. Idite na **Podešavanja** > **Opšti podaci** > **Parametri**.
2. Na stranici liste **Aktivni parametri** pronađite zapis i dvaput kliknite da biste ga otvorili. 
3. Na stranici **Parametri** , izaberite karticu **Cenovnik**. Videćete da se prikazuje lista podrazumevanih cenovnika. Ovo je lista standardnih troškova i prodajnih cenovnika. Ako imate ovde povezan prodajni cenovnik za svaku valutu u kojoj prodajete, obezbediće se da ovaj prodajni cenovnik bude podrazumevan za bilo koju ponudu koju kreirate za klijente koji obavljaju transakcije u toj valuti.

### <a name="set-up-customer-specific-project-price-lists"></a>Podešavanje cenovnika projekta specifičnog za klijenta

Cenovnici projekata specifični za klijenta takođe se mogu podesiti kada ste sa svojim klijentima dogovorili glavni ugovor o cenama.

Da biste podesili cenovnik projekta specifičan za klijenta, izvršite sledeće korake.

1. U oblasti **Prodaja** , izaberite **Klijenti**.
2. U listi aktivnih poslovnih kontakata, odaberite i otvorite zapis klijenta za kojeg imate poseban cenovnik.
3. Na kartici **Cenovnik projekta** možete kreirati novo povezivanje cenovnika da biste dobili cenovnik projekta koji je specifičan za ovog klijenta.

## <a name="create-custom-pricing-on-a-project-quote"></a>Kreiranje prilagođenog određivanja cena u ponudi za projekat

Kada imate organizacione i korisničke podrazumevane cenovnike projekata, vaše ponude za projekte automatski će se kreirati sa tim povezivanjima cenovnika projekata. Međutim, u određenim slučajevima, možda ćete morati da kreirate prilagođene cene za određenu ponudu za projekat. 

1. U delu **Ponuda za projekat** , na kartici **Cenovnik projekta** , u podformi verifikujte da nije izabran nijedan određeni zapis o cenovniku.
2. Izaberite **Kreiranje prilagođenih cena**. Ovim ćete napraviti kopije svih standardnih cenovnika koji su trenutno povezani sa ponudom i povezati ove kopije sa ponudom. Ukloniće se postojeća povezivanja sa standardnim cenovnicima. Tada prodavac može započeti uređivanje cena na ovim kopijama. Ove promenjene cene će se primenjivati samo na ovu ponudu za projekat.
