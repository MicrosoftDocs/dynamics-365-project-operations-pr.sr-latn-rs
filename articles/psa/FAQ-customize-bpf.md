---
title: Kako prilagođavate tok poslovnog procesa za faze projekta?
description: Pregled načina prilagođavanja toka poslovnog procesa za faze projekta.
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 15540f524fb8fca8f69a2249f783289ba683cad7dabbf58ecbf620d147e5d491
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002978"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>Kako prilagođavate tok poslovnog procesa za faze projekta?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

Postoji poznato ograničenje u ranijim verzijama aplikacije Project Service da imena faza u toku poslovnog procesa za faze projekta moraju biti potpuno ista sa očekivanim engleskim imenima (**Quote**, **Plan**, **Close**). U suprotnom, poslovna logika, koja se oslanja na englesko ime faze, ne radi kako je očekivano. Zato ne vidite da su poznate radnje, kao što su **Prebaci proces** ili **Uredi proces** dostupne u obrascu projekta, a prilagođavanje toka poslovnog procesa se ne podstiče. 

Ovo ograničenje je otklonjeno u verziji 2.4.5.48 i novijim. U ovom članku data su predložena zaobilazna rešenja ukoliko morate da prilagodite podrazumevani tok poslovnog procesa za starije verzije.  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>Poslovna logika zahteva potpuno podudaranje sa engleskim imenima faze

Tok poslovnog procesa za faze projekta sadrži poslovnu logiku koja upravlja sledećim ponašanjima u aplikaciji:
- Kada je projekat povezan sa ponudom, kôd postavlja tok poslovnog procesa na fazu **Quote**.
- Kada je projekat povezan sa kontaktom, kôd postavlja tok poslovnog procesa na fazu **Plan**.
- Kada je tok poslovnog procesa napredovao do faze **Close**, zapis projekat se deaktivira. Kada je projekat deaktiviran, obrazac projekta i strukturna analiza posla (SAP) su podešeni na samo za čitanje, rezervacije imenovanog resursa se ukidaju i svi povezani cenovnici se deaktiviraju.

Ova poslovna logika se oslanja imena na engleskom jeziku za faze projekta. Ova zavisnost od imena na engleskom jeziku predstavlja glavni razlog zašto se ne podstiče prilagođavanje toka poslovnog procesa za faze projekta, kao i zašto ne vidite uobičajene radnje toka poslovnog procesa kao što su **Prebaci proces** ili **Uredi proces** u entitetu Projekat.

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>Šta se događa ako se imena faza ne podudaraju sa imenima na engleskom?

U aplikaciji Project Service, verzija 1.x na platformi 8.2, kada se imena faza u toku poslovnog procesa ne podudaraju tačno sa engleskim imenima za faze, preskače se poslovna logika koja podešava pravi fazu za ponude ili ugovore ili koja zatvara projekat. Neće se prikazivati poruke o grešci. Zbog toga deluje da možete da prilagodite tok poslovnog procesa za faze projekta. Međutim, nećete videti da ijedan automatski proces funkcioniše za ponude, ugovore i zatvaranje projekta.

U aplikaciji Project Service, verzija 2.4.4.30 ili ranija na platformi 9.0, došlo je do značajne arhitektonske promene tokova poslovnih procesa, što je zahtevalo ponovno pisanje poslovne logike toka poslovnog procesa. Kao posledica toga, ako se imena faze procesa ne podudaraju sa očekivanim imenima na engleskom jeziku, primićete poruku o grešci. 

Stoga, ako želite da prilagodite tok poslovnog procesa za faze projekta za entitet projekta, možete samo da dodate potpuno nove faze u podrazumevani tok poslovnog procesa za entitet projekta zadržavajući faze **Ponuda**, **Plan** i **Zatvori** nepromenjene. Ovo ograničenje osigurava da ne dobijate greške od poslovne logike koja očekuje imena na engleskom jeziku u toku poslovnog procesa.

U verziji 2.4.5.48 ili novijoj, poslovna logika opisana u ovom članku je uklonjena iz podrazumevanog toka poslovnog procesa za entitet projekta. Nadogradnja na tu verziju ili kasniju će vam omogućiti da prilagodite ili zamenite podrazumevani tok poslovnog procesa sopstvenim. 

## <a name="workarounds-for-earlier-versions"></a>Zaobilazna rešenja za ranije verzije

Ako nadogradnja ne predstavlja opciju, možete da prilagodite tok poslovnog procesa za faze projekta za entitet projekta na jedan od ova dva načina:

1. Dodajte dodatne faze podrazumevanoj konfiguraciji istovremeno zadržavajući engleska imena faza za opcije **Quote**, **Plan** i **Close**.


![Snimak ekrana za dodavanje faza podrazumevanoj konfiguraciji.](media/FAQ-Customize-BPF-1.png)
 
2. Kreirajte sopstveni tok poslovnog procesa i neka on bude vaš primarni tok poslovnog procesa za entitet projekta, što vam omogućava da imate bilo koja imena faze po želji. Međutim, ako želite da koristite iste standardne faze projekta **Quote**, **Plan** i **Close**, potrebno je da izvršite još neka prilagođavanja koja se pokreću na osnovu vaših prilagođenih imena za faze. Složenija logika se nalazi u zatvaranju projekta, koju i dalje možete da pokrećete prostim deaktiviranjem zapisa projekta.

![BPF prilagođavanje.](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>Dodatna razmatranja za aplikaciju Project Service, verzija 2.4.4.30 ili ranije na platformi 9.0

U aplikaciji Project Service 2.4.4.30 ili ranijoj na platformi 9.0, sa prilagođenim tokom poslovnog procesa, polje **Ime faze** u entitetu Projekat kojeg koristi grafikon **Projekata prema fazi** i prikaz liste projekta se neće ispravljati, jer su povezani sa tokom poslovnog procesa za podrazumevane faze projekta. Ovaj problem možete da rešite sa sledećim koracima:

- Dodajte prilagođeno polje da biste pribeležili trenutnu fazu toka poslovnog procesa koja se ažurira kako korisnik prilazi kroz prilagođeni tok poslovnog procesa.

- Izmenite grafikon **Projekat prema fazi** kako biste radili sa prilagođenim poljem umesto sa podrazumevanom konfiguracijom.

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>Koraci za kreiranje sopstvenog toka poslovnog procesa za entitet projekta

Postupite na sledeći način da biste kreirali sopstveni tok poslovnog procesa za entitet projekta:

1. Idite na stavku **Podešavanja** > **Centar za procese**. Nemojte da kopirate tok poslovnog projekta za faze projekta jer to kopira i poslovnu logiku aplikacije Project Service.

  ![Kreiraj proces.](media/FAQ-Customize-BPF-3.png)

2. Koristite dizajner procesa za kreiranje željenih imena za faze. Ako želite istu funkcionalnost kao podrazumevane faze za stavke **Quote**, **Plan** i **Close**, moraćete da je kreirate na osnovu imena za faze prilagođenog toka poslovnog procesa.

   ![Snimak ekrana dizajnera procesa koji se koristi za prilagođavanje BPF.](media/FAQ-Customize-BPF-4.png) 

3. U dizajneru procesa, kliknite na stavku **Redosled toka procesa** kako bi prilagođeni tok poslovnog procesa postao primarni tok poslovnog procesa za entitet projekta njegovim premeštanjem iznad toka poslovnog procesa za faze projekta na vrh liste.


   [Snimak ekrana korišćenja Redosleda toka procesa](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>Sledeći koraci se primenjuju na aplikaciju Project Service 2.4.4.30 ili raniju na platformi 9.0

4. Dodajte novo prilagođeno polje u entitet projekta da biste pribeležili prilagođene faze u svom prilagođenom toku poslovnog procesa. Potrebno je da dodate poslovnu logiku (dodatnu komponentu/tok posla) da biste ispravili ovo polje kada se ispravlja faza u prilagođenom toku poslovnog procesa.

   ![Snimak ekrana za prilagođavanje entiteta Projekat.](media/FAQ-Customize-BPF-6-720.png)

5. Izmenite grafikon **Projekat prema fazi** da biste koristili novo prilagođeno polje za faze.

   ![Snimak ekrana korišćenja grafikona Projekat prema fazi.](media/FAQ-Customize-BPF-7-720.png)

6. Izmenite sve prikaze za entitet Projekat da biste obuhvatili novo prilagođeno polje za faze.

   ![Snimak ekrana izmene prikaza u entitetu Projekat.](media/FAQ-Customize-BPF-8-720.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]