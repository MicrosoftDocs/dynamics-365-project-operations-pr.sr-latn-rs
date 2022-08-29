---
title: Sinhronizovanje statusa projekta da bi se sprečila stavka protiv zatvorenih projekata
description: Ovaj članak sadrži objašnjenja o tome kako da sinhronizujete status projekta da biste sprečili ulazak u neaktivne ili zatvorene projekte.
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
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Sinhronizovanje statusa projekta da bi se sprečila stavka protiv zatvorenih projekata

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

## <a name="scenario"></a>Scenario

Contoso sa korporacijom Microsoft za scenarije Dynamics 365 Project Operations koji nisu snabdeveni resursima. U sklopu normalnih poslovnih aktivnosti, projekti mogu biti završeni ili stavljeni na čekanje. Projekat možete aktivirati da biste se uverili da se ne generišu troškovi ili fakture.

## <a name="solution"></a>Rešenje

### <a name="prerequisites"></a>Preduslovi

-   Microsoft Dynamics 365 Finansije 10.0.29 ili novije moraju biti instalirane.
-   Dual Write map 1.0.0.3 za projekte V2 (msdyn\_ projekti) mora biti instalirana ili ručno konfigurisana kao što je opisano u nastavku.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Kreiranje ažurirane verzije integracije projektnih operacija Projekti V2 mapa za dvostruko pisanje

Da biste ažurirali mapu dvostrukog pisanja projekta Projekti V2:

1. Idite na radni **prostor za upravljanje** podacima i izaberite **dual-write**.
2. Izaberite pločicu **"Dva** pisanja".
3. Iz kolone mape T **tabele** pronađite i izaberite **projekat V2 (msdyn projekti\_), a zatim** kliknite na dugme Zaustavi.
4. Izaberite ime mape da biste otvorili mapu, a zatim izaberite **[Nijedno]**.
5. U dijalogu Izbor kolone izaberite status projekta statecode **, \[a zatim\]** kliknite na dugme U redu. Možete da upišete **stanje** u vrednost filtera da biste suzili listu.
6.  Kliknite **na dugme Dodaj ili uredi transformaciju** u koloni **tipa** mape da biste uredili transformaciju.
7.  Iz tipa **transformacije** izaberite **Mapu vrednosti**.
8.  Izaberite **opciju Dodaj mapiranje vrednosti**, a zatim dodajte sledeće tastere **i** **vrednosti**:

   Taster       | Vrednost 
   ----------|-------
   InProcess | 0     
   Dovršeno | 1     

![Snimak ekrana koji prikazuje mapiranje dva pisanja](media/projectstage-dw-mapping.png)

9. Izaberite **Sačuvaj**.
10. Sa vrha stranice Dual-write **> Projects V2 (msdyn_projects)** izaberite stavku Sačuvaj **kao**.
11. Iz **tabele "** Dodaj" u **Polju programa Publisher** izaberite **PODRAZUMEVANI IZDAVAČ CDS-a**.
12. Postavite **polje** Verzija na 1.0.0.3.
13. Otkucajte opis, a **zatim** kliknite na dugme **Sačuvaj**.
14. Sa vrha stranice **Dual-write > Projects V2 (msdyn_projects)** **izaberite stavku Pokreni** da biste pokrenuli mapu, a zatim sekect **Da** ako budete upitani da potvrdite pre nego što pokrenete. 

### <a name="close-a-newly-completed-project"></a>Zatvaranje novozavršenog projekta

Dynamics 365 Finance polje faze projekta za **razlikovanje projekata u toku** ili **završenom**.**·** **Završeni** projekti ne mogu da nanose troškove niti da budu fakturisani kupcima.

1. Otvorite projekat za deaktiviranje.
2. Na glavnoj traci izaberite stavku **Deaktiviši**.

> [!NOTE]
> Možete da deaktivirate ili zatvorite projekat jer će se obojica ponašati isto u kontekstu finansija.

3. U okviru Finansije otvorite stranicu **Lista svih projekata**.
4. Potvrdite da se deaktivirani projekat ne pojavljuje na listi.
5. U prikazu **filtera** projekata iznad liste promenite vrednost iz Aktivno **u** **Sve**.
6. Sada ćete videti deaktivirani projekat.

Ako pokušate da evidentiraje vreme ili troškove u odnosu na ovaj projekat u programu Finansije, ne bi trebalo da vidite projekat za izbor. Ako ručno unesete broj projekta o trošku, videćete poruku poput "Završena faza projekta ne dozvoljava snimanje u projektu". Fakturisanje i druge funkcije naplate treba da budu onemogućene jer će biti u kontekstu zatvorenog projekta.

