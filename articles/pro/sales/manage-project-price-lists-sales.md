---
title: Upravljanje cenovnicima projekata u ponudama za projekat
description: Ovaj članak pruža informacije o radu sa cenovnicima projekta u ponudama.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6902d22c7bd4b422466c924ee6473146b036caa5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929967"
---
# <a name="manage-project-price-lists-on-project-quotes"></a>Upravljanje cenovnicima projekata u ponudama za projekat 

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Ponude za projekte su dizajnirane da podržavaju više efektivnih prodajnih cenovnika. Uz Dynamics 365 Project Operations, dodaje se novi povezani entitet pod nazivom **Cenovnici projekata**. Ovaj entitet ima relaciju „1 prema više“ sa ponudom za projekat.

Cenovnici projekata se koriste za određivanje vremena, materijala i transakcija troškova na projektu. Kada ponuda ima jedan ili više cenovnika projekata, ovi cenovnici se koriste za određivanje cene vremena, materijala, procena troškova i trenutnog stanja projekata koji su povezani sa ponudom preko stavke ponude.

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
3. Na stranici **Parametri**, izaberite karticu **Cenovnik**. Videćete da se prikazuje lista podrazumevanih cenovnika. Ovo je lista standardnih troškova i prodajnih cenovnika. Ako imate ovde povezan prodajni cenovnik za svaku valutu u kojoj prodajete, obezbediće se da ovaj prodajni cenovnik bude podrazumevan za bilo koju ponudu koju kreirate za klijente koji obavljaju transakcije u toj valuti.

### <a name="set-up-customer-specific-project-price-lists"></a>Podešavanje cenovnika projekta specifičnog za klijenta

Cenovnici projekata specifični za klijenta takođe se mogu podesiti kada ste sa svojim klijentima dogovorili glavni ugovor o cenama.

Da biste podesili cenovnik projekta specifičan za klijenta, izvršite sledeće korake.

1. U oblasti **Prodaja**, izaberite **Klijenti**.
2. U listi aktivnih poslovnih kontakata, odaberite i otvorite zapis klijenta za kojeg imate poseban cenovnik.
3. Na kartici **Cenovnik projekta** možete kreirati novo povezivanje cenovnika da biste dobili cenovnik projekta koji je specifičan za ovog klijenta.

## <a name="create-custom-pricing-on-a-project-quote"></a>Kreiranje prilagođenog određivanja cena u ponudi za projekat

Kada imate organizacione i korisničke podrazumevane cenovnike projekata, vaše ponude za projekte automatski će se kreirati sa tim povezivanjima cenovnika projekata. Međutim, u određenim slučajevima, možda ćete morati da kreirate prilagođene cene za određenu ponudu za projekat. 

1. U delu **Ponuda za projekat**, na kartici **Cenovnik projekta**, u podformi verifikujte da nije izabran nijedan određeni zapis o cenovniku.
2. Izaberite **Kreiranje prilagođenih cena**. Ovim ćete napraviti kopije svih standardnih cenovnika koji su trenutno povezani sa ponudom i povezati ove kopije sa ponudom. Ukloniće se postojeća povezivanja sa standardnim cenovnicima. Tada prodavac može započeti uređivanje cena na ovim kopijama. Ove promenjene cene će se primenjivati samo na ovu ponudu za projekat.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
