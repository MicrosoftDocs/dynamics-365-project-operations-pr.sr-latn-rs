---
title: Konfigurisanje internog fakturisanja između preduzeća
description: Ova tema pruža informacije i primere o konfigurisanju internog fakturisanja između preduzeća za projekte.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 09bbd1bf640cc86b16afb8c2b824329b92f833df836e9313491d57a2f1646440
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994068"
---
# <a name="configure-intercompany-invoicing"></a>Konfigurisanje internog fakturisanja između preduzeća

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Dovršite sledeće korake da biste podesili fakturisanje između preduzeća za projekte u usluzi Dynamics 365 Project Operations. Transakcije među preduzećima su transakcije radnog vremena i troškova iz projektnog ugovora koje pripadaju jednom preduzeću ili organizacionoj jedinici, dok su resursi iz projektnog ugovora deo drugog preduzeća ili organizacione jedinice.

## <a name="example-configure-intercompany-invoicing"></a>Primer: konfigurisanje internog fakturisanja između preduzeća

U sledećem primeru, Contoso Robotics USA (USPM) je pravno lice koje se zadužuje i Contoso Robotics UK (GBPM) je pravno lice koje daje pozajmice. 

1. **Konfigurišite računovodstvo između preduzeća između pravnih lica**. Svaki par pravnih lica koja se zadužuju i pozajmljuju mora biti konfigurisan na stranici glavne knjige [Računovodstvo između preduzeća](/dynamics365/finance/general-ledger/intercompany-accounting-setup).
    
    1. U usluzi Dynamics 365 Finance, idite na **Glavna knjiga** > **Podešavanje knjiženja** > **Računovodstvo između preduzeća**. Kreirajte zapis sa sledećim informacijama:

        - **Izvorno preduzeće** = **GBPM**
        - **Odredišno preduzeće** = **USPM**

2. **Konfigurišite trgovački odnos između pravnih lica**. Zapis klijenta koji predstavlja pravno lice koje se zadužuje mora biti kreirano u pravnom licu koje pozajmljuje. Zapis dobavljača koji predstavlja pravno lice koje pozajmljuje mora biti kreirano u pravnom licu koje se zadužuje.

     1. U usluzi Finance, izaberite pravno lice **GBPM**.
     2. Idite na **Potraživanja** > **Klijent** > **Svi klijenti**. Kreirajte novi zapis za pravno lice, **USPM**.
     3. Razvijte **Naziv**, filtrirajte zapise prema kategoriji **Tip** i izaberite **Pravna lica**. 
     4. Pronađite i izaberite evidenciju klijenata za **Contoso Robotics USA (USPM)**.
     5. Izaberite **Koristi podudaranje**. 
     6. Izaberite grupu klijenata **50 - Međukompanijski klijenti** a zatim sačuvajte zapis.
     7. Izaberite pravno lice **USPM**.
     8. Idite na **Dugovanja** > **Dobavljači** > **Svi dobavljači**. Kreirajte novi zapis za pravno lice, **GBPM**.
     9. Razvijte **Naziv**, filtrirajte zapise prema kategoriji **Tip**, pa izaberite **Pravna lica**. 
     10. Pronađite i izaberite evidenciju klijenata za **Contoso Robotics UK (GBPM)**.
     11. Izaberite **Koristi podudaranje**, izaberite grupu dobavljača, a zatim sačuvajte zapis.
     12. U evidenciji dobavljača izaberite **Opšti podaci** > **Podesi** > **Između preduzeća**.
     13. Na kartici **Trgovinski odnos**, podesite **Aktivno** na **Da**.
     14. Podesite **Kompanija klijent** na **GBPM** a u **Zapis mog naloga**, izaberite evidenciju klijenata koju ste kreirali ranije u proceduri.

3. **Konfigurišite podešavanja između preduzeća u upravljanju projektima i računovodstvenim parametrima**. 

    1. Izaberite pravno lice **USPM** i idite u **Upravljanje projektima i računovodstvo** > **Podešavanje** > **Upravljanje projektom i računovodstveni parametri**.
    2. Na kartici **Između preduzeća** izaberite kategoriju nabavke kako biste se podudarali sa fakturama dobavljača koje se automatski generišu.
    3. U okviru opcije **Podrazumevana kategorija**, izaberite **Resursi između preduzeća**.
    4. Izaberite pravno lice **GBPM** i idite u **Upravljanje projektima i računovodstvo** > **Podešavanje** > **Upravljanje projektom i računovodstveni parametri**.
    5. Na kartici **Između preduzeća** izaberite podrazumevanu kategoriju projekta za svaki tip transakcije. Kategorije projekata se koriste za konfiguraciju poreza kada fakturisana kategorija u međukompanijskim transakcijama postoji samo u pravnom licu zajmoprimcu. Možete odabrati da akumulirate prihod za međukompanijske transakcije. Do obračunavanja dolazi kada se transakcije knjiže kroz Project Operations dnevnik integracije u pravnom licu koje pozajmljuje. Dnevnik se poništava kada se knjiži interna faktura između preduzeća.
    6. U okviru grupe **Kada resursi pozajmljuju**, izaberite **...** > **Novo**. 
    7. U mreži unesite ili izaberite sledeće informacije:

          - **Pravno lice koje se zadužuje** = **USPM**
          - **Ostvarivanje prihoda** = **Da**
          - **Podrazumevana kategorija vremenskog rasporeda** = **Podrazumevano – sat**
          - **Podrazumevana kategorija troškova** = **Podrazumevano – trošak**

4. **Podesite poslovne kontakte za troškove i prihode između preduzeća u podešavanju knjiženja knjige**. Konto za prihode između preduzeća se kreditira kada se interna faktura klijenta između preduzeća knjiži u entitetu pravnog lica koje pozajmljuje. Konto za trošak između preduzeća se zadužuje kada se odgovarajuća faktura dobavljača na čekanju knjiži u entitetu pravnog lica koje se zadužuje. Ova konta su podešena u odgovarajućim pravnim licima. 
      
     1. U usluzi Finance, izaberite pravno lice koje se zadužuje **USPM**. 
     2. Idite na **Upravljanje projektima i računovodstvo** > **Podešavanje** > **Knjiženje** > **Podešavanje knjiženja knjige**. 
     3. Na kartici **Konta troškova**, u **Tipu konta glavne knjige**, izaberite **Troškovi između preduzeća**. Kreirajte novi zapis sa sledećim informacijama:
      
        - **Pravno lice koje pozajmljuje** = **GBPM**
        - **Glavni nalog** = izaberite glavni konto za troškove između preduzeća. Ovo podešavanje je obavezno. Postavka se koristi za međukompanijske tokove u finansijama, ali ne i za interkompanijske tokove povezane sa projektima. Ovaj izbor nema uticaja nizvodno. 
        
     4. Izaberite pravno lice koje pozajmljuje **GBPM**. 
     5. Idite na **Upravljanje projektima i računovodstvo** > **Podešavanje** > **Knjiženje** > **Podešavanje knjiženja knjige**. 
     6. Na kartici **Konta prihoda**, u **Tipu konta glavne knjige**, izaberite **Prihodi između preduzeća**. Kreirajte novi zapis sa sledećim informacijama:

        - **Pravno lice koje se zadužuje** = **USPM**
        - **Glavni konto** = izaberite glavni konto za prihod između preduzeća. Ovo podešavanje je obavezno. Postavka se koristi za međukompanijske tokove u finansijama, ali ne i za interkompanijske tokove povezane sa projektima. Ovaj izbor nema uticaja nizvodno. 

5. **Podešavanje cena za prenos za rad**. Cene prenosa između preduzeća su konfigurisane u usluzi Project Operations na platformi Dataverse. Konfigurišite [stope troškova rada](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity) i [stope naplate za rad](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions) za interno fakturisanje između preduzeća. Formiranje cena za prenos nije podržan za transakcije troškova između preduzeća. Prodajna jedinična cena između organizacija će uvek biti podešena na istu vrednost kao cena koštanja jedinice za resurse.

      Troškovi resursa za programere u Contoso Robotics UK je 88 GBP na sat. Contoso Robotics UK će naplatiti Contoso Robotics USA 120 USD za svaki sat koji je ovaj resurs radio na američkim projektima. Contoso Robotics USA će klijentu Adventure Works 200 USD za posao koji je obavio Contoso Robotics UK resurs za programere.

      1. U usluzi Project Operations na platformi Dataverse, idite na **Prodaja** > **Cenovnici**. Napravite novi cenovnik troškova pod nazivom **Contoso Robotics UK stope troškova.** 
      2. U cenovniku koštanja kreirajte zapis sa sledećim informacijama:
         - **Uloga** = **Programer**
         - **Trošak** = **88 GBP**
      3. Idite na **Podešavanja** > **Organizacione jedinice** i priložite ovaj cenovnik uz **Contoso Robotics UK** organizacionu jedinicu.
      4. Idite na **Prodaja** > **Cenovnici**. Napravite novi cenovnik troškova pod nazivom **Contoso Robotics USA stope troškova**. 
      5. U cenovniku koštanja kreirajte zapis sa sledećim informacijama:
          - **Uloga** = **Programer**
          - **Resursna kompanija** = **Contoso Robotics UK**
          - **Trošak** = **120 USD**
      6. Idite na **Podešavanja** > **Organizacione jedinice** i priložite **Contoso Robotics USA stope cena** uz **Contoso Robotics USA** organizacionu jedinicu.
      7. Idite na **Prodaja** > **Cenovnici**. Kreirajte prodajni cenovnik pod nazivom **Stope naplate za Adventure Works**. 
      8. U prodajnom cenovniku kreirajte zapis sa sledećim informacijama:
          - **Uloga** = **Programer**
          - **Resursna kompanija** = **Contoso Robotics UK**
          - **Stopa naplate** = **200 USD**
      9. Idite na **Prodaja** > **Projektni ugovori** i priložite cenovnik za **Adventure Works stope naplate** cenovniku ugovora o projektu za Adventure Works projekat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
