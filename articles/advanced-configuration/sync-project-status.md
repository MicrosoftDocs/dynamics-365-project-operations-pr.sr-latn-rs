---
title: Sinhronizovanje statusa projekta radi sprečavanja ulaska u zatvorene projekte
description: Ovaj članak objašnjava kako da sinhronizujete status projekta da biste sprečili unos u neaktivne ili zatvorene projekte.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348128"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Sinhronizovanje statusa projekta radi sprečavanja ulaska u zatvorene projekte

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

## <a name="scenario"></a>Scenario

Contoso je objavljen sa rešenjem Microsoft Dynamics 365 Project Operations za scenarije resursa/bez zaliha. U sklopu normalnih poslovnih aktivnosti, projekti mogu biti završeni ili stavljeni na čekanje. Projekat možete deaktivirati da biste se uverili da se ne generišu troškovi ili fakture.

## <a name="solution"></a>Rešenje

### <a name="prerequisites"></a>Preduslovi

-   Microsoft Dynamics 365 Finance 10.0.29 ili noviji mora biti instaliran.
-   Mapa dvostrukog upisivanja 1.0.0.3 za projekte V2 (msdyn\_projects) mora biti instalirana ili ručnog konfigurisana kao što je opisano ispod.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Kreiranje ažurirane verzije integracije Project Operations projekta V2 mape za dvostruko upisivanje

Da biste ažurirali mapu dvostrukog upisivanja za Project Operations projekte V2:

1. Uđite u radni prostor **Upravljanje podacima** i izaberite **Dvostruko upisivanje**.
2. Izaberite pločicu **Dvostruko upisivanje**.
3. iz kolone T **Mapa tabele**, pronađite i izaberite **Projekat V2 (msdyn\_projects**), a zatim izaberite Zaustavi.
4. Izaberite naziv mape da biste otvorili mapu, a zatim izaberite **[Nijedno]**.
5. U dijalogu Izbor kolone izaberite **statecode \[Status projekta\]**, a zatim kliknite na U redu. Možete da unesete **Status** u vrednost filtera da biste suzili listu.
6.  Izaberite **Dodaj ili uredi transformaciju** u koloni **tip mape** da biste uredili transformaciju.
7.  Iz **Tipa transformacije** izaberite **ValueMap**.
8.  Izaberite **Dodaj mapiranje vrednosti**, a zatim dodajte sledeće **Tasteri** i **Vrednosti**:

   Taster       | Vrednost 
   ----------|-------
   InProcess | 0     
   Dovršeno | 1     

![Snimak ekrana koji prikazuje mapiranje dvostrukog upisivanja](media/projectstage-dw-mapping.png)

9. Izaberite **Sačuvaj**.
10. Sa vrha stranice **Dvostruko upisivanje > Projekti V2 (msdyn_projects)**, izaberite **Sačuvaj kao**.
11. Iz opcije **Dodavanje tabele**, u polju **Objavljivač** izaberite **Podrazumevani CDS izdavač**.
12. Postavite polje **Verzija** na 1.0.0.3.
13. Unesite **Opis**, a zatim izaberite **Sačuvaj**.
14. Sa vrha stranice **Dvostruko upisivanje > Projekti V2 (msdyn_projects)** izaberite **Pokreni** da biste pokrenuli mapu, a zatim izaberite **Da** ako budete upitani da potvrdite pre nego što pokrenete. 

### <a name="close-a-newly-completed-project"></a>Zatvaranje novozavršenog projekta

Dynamics 365 Finance koristi polje **faza u projektu** da napravi razliku između projekata koji su **u toku** ili **završeni**. **Završeni** projekti ne mogu da nanose troškove niti da budu fakturisani klijentima.

1. Otvorite projekat za deaktiviranje.
2. Sa trake, izaberite **Deaktiviraj**.

> [!NOTE]
> Možete da deaktivirate ili zatvorite projekat jer će se oboje ponašati isto u kontekstu finansija.

3. U okviru Finansija otvorite stranicu **Lista svih projekata**.
4. Potvrdite da se deaktivirani projekat ne pojavljuje na listi.
5. U filteru **prikaži projekte** iznad liste promenite vrednost iz **Aktivno** u **Svi**.
6. Sada ćete videti deaktivirani projekat.

Ako pokušate da evidentirate vreme ili troškove za ovaj projekat u Finansijama, ne bi trebalo da vidite projekat za izbor. Ako ručno unesete broj projekta na trošku, videćete poruku poput „Završena faza projekta ne dozvoljava evidentiranje u projektu“. Fakturisanje i druge funkcije naplate treba da budu onemogućene jer će biti u kontekstu zatvorenog projekta.

