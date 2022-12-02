---
title: Osoblje projekta sa radnicima po ugovoru i podizvođačima
description: Ovaj članak sadrži objašnjenja o tome kako zahtevi projekta mogu da se koriste pomoću kapaciteta radnika po ugovoru ili podugovora u usluzi Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 30e16efeed93ab4568eac57fb3ed46067a08524d
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522453"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Osoblje projekta sa radnicima po ugovoru i podizvođačima

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Generički članovi projektnog tima mogu biti zaposleni ili radnici po ugovoru. Kada koristite projekat sa radnicima po ugovoru, možete da ograničite opcije popune osoblja na određene radnike po ugovoru koji su dodeljeni predmetu podugovora. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Pretraga zahteva za resurse osoblja sa radnicima po ugovoru koji pripadaju određenom predmetu podugovora

Da biste pretraživali i dodelili zahteve za resurse osoblja sa radnicima po ugovoru koji pripadaju određenom predmetu podugovora, pratite ove korake:

1. Kreiranje generičkog člana projektnog tima koji upućuje na podugovor i predmet podugovora.
2. Generišite zahtev za resurs za ovog generičkog člana projektnog tima pomoću dugmeta **Generiši zahtev** na podmreži članova projektnog tima.
3. Izaberite red člana tima, a zatim izaberite dugme **Rezerviši** u podmreži. 
4. Ovo otvara Tablu rasporeda sa kontekstom zahteva. Zajedno sa drugim atributima kao što su polja datuma, uloge i organizacione jedinice, filteri Table rasporeda se takođe automatski popunjavaju poljima dobavljača, podugovora i predmeta podugovora iz zahteva za resursom.
5. Sistem traži resurse koji zadovoljavaju kriterijume filtera i navodi ih. 
6. Izaberite jedan od filtriranog resursa i rezervišite resurs za zahtev. 
7. Član projektnog tima se kreira i ažurira sa referencama na podugovor i predmet podugovora. Idite na **Procene projekta** i izaberite **Ažuriraj cene** da biste videli ažuriranu cenu dodele resursa. 

> [!NOTE]
> Ažuriranje člana projektnog tima referencom ka podugovoru i predmetu podugovora možda neće uvek biti moguće tokom rezervisanja ako je resurs dodeljen u više predmeta podugovora. Ako sistem ne može da ažurira člana projektnog tima podugovorom i predmetom podugovora, otvorite zapis člana projektnog tima i ručno ažurirajte ova polja tako da procena finansijskih troškova tačno odražava trošak podugovarača.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Pretraga i zahtevi za popunu resursa osoblja kod bilo kog radnika po ugovoru

Da biste pretraživali i popunili resurse osoblja kod bilo kog radnika po ugovoru, pratite ove korake:

1. Kreiranje generičkog člana projektnog tima.
2. Generišite zahtev za resurs za ovog generičkog člana projektnog tima pomoću dugmeta **Generiši zahtev** na podmreži članova projektnog tima.
3. Izaberite red člana tima, a zatim izaberite dugme **Rezerviši** u podmreži. 
4. Ovo otvara Tablu rasporeda sa kontekstom zahteva. Zajedno sa drugim atributima kao što su polja datuma, uloge i organizacione jedinice, filteri Table rasporeda se takođe automatski popunjavaju poljima dobavljača, podugovora i predmeta podugovora iz zahteva za resursom. Pošto u zahtevu nisu popunjene vrednosti podugovora ili predmeta podugovora, ovi atributi će biti prazni u oknu sa filterima.
5. Sistem traži resurse koji zadovoljavaju kriterijume filtera i navodi ih.
6. Ažurirajte polje **Vrsta radnika** u oknu sa filterima na **Radnik po ugovoru** da biste ograničili pretragu na radnike po ugovoru. Ažurirajte **Dobavljača** u oknu sa filterima da biste izabrali dobavljača kako biste ograničili pretragu tako da pokazuje samo radnike po ugovoru koji pripadaju određenom preduzeću dobavljača.
7. Izaberite radnika po ugovoru sa liste i rezervišite resurs za zahtev.
8. Kreira se člana projektnog tima. Međutim, član projektnog tima se ne ažurira ni sa jednim podugovorom ili predmetom podugovora i zato neće biti obračunata cena dodele resursa korišćenjem cena podugovaranja. Ručno ažurirajte člana projektnog tima predmetom podugovora i idite na **Procene projekta** i izaberite **Ažuriraj cene** da biste videli ažurirane cene dodele resursa.

> [!NOTE]
> Članovi projektnog tima koji imaju **Tip radnika** kao **Radnik po ugovoru**, ali nemaju referencu podugovora, označeni su zastavicom kao **Nevažeći** u matrici koordinatne mreže **Članovi projektnog tima**. Ako postoje neki članovi projektnog tima sa ovim statusom, otvorite zapis člana projektnog tima i ručno ažurirajte polja podugovora i predmeta podugovora tako da procena finansijskih troškova tačno odražava trošak podugovarača na kartici **Procene**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
