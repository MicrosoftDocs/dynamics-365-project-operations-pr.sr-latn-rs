---
title: Osoblje projekta sa radnicima po ugovoru i podizvođačima
description: Ova tema objašnjenja o tome kako zahtevi projekta mogu da se koriste pomoću radnika po ugovoru ili kapaciteta podizvođačima u korporaciji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a0efea80484dfca0a9dae8404837c3376dfecaed
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574659"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Osoblje projekta sa radnicima po ugovoru i podizvođačima

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Generički članovi projektnog tima mogu biti zaposleni ili radnici po ugovoru. Kada koristite projekat sa radnicima po ugovoru, možete da ograničite opcije osoblja na određene radnike po ugovoru koji su dodeljeni redu podizvođače. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Traženje zahteva resursa osoblja sa radnicima po ugovoru koji pripadaju određenom redu podizvođači

Da biste tražili i zahtevali resurse osoblja sa radnicima po ugovoru koji pripadaju određenom redu podizvođači, sledite ove korake:

1. Kreirajte generički član projektnog tima koji upućuje na red podizvođači i podizvođači.
2. Generiši zahtev resursa za ovog generičkog člana projektnog tima pomoću dugmeta **Generisaj** zahtev na podmrežnoj mreži članova projektnog tima.
3. Izaberite red člana tima, a zatim kliknite na dugme **"Knjiga** " u podmrežnoj mreži. 
4. Ovo otvara tablu rasporeda sa kontekstom zahteva. Zajedno sa drugim atributima kao što su polja datuma, uloge i organizacione jedinice, filteri table rasporeda se takođe automatski popunjavaju poljima dobavljača, podizvođača i reda podizvođača iz zahteva resursa.
5. Sistem traži resurse koji zadovoljavaju kriterijume filtera i navodi ih. 
6. Izaberite jedan od filtriranog resursa i rezervišite resurs za zahtev. 
7. Član projektnog tima se kreira i ažurira referencama reda podizvođačima i podizvođačima. Idite na **"Procene projekta"** i izaberite **stavku Ažuriraj** cene da biste videli ažurirane troškove dodele resursa. 

> [!NOTE]
> Ažuriranje člana projektnog tima referencom podizvođačem i redom podizvođače možda neće uvek biti moguće tokom rezervisanja ako je resurs dodeljen u više redova podizvođače. Ako sistem ne može da ažurira člana projektnog tima podizvođačom i redom podizvođača, otvorite zapis člana projektnog tima i ručno ažurirajte ova polja tako da procena finansijskih troškova tačno odražava trošak podizvođača.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Traženje i zahtevi resursa osoblja kod bilo kog radnika po ugovoru

Da biste tražili i zahtevali resurse osoblja sa bilo kojim radnikom po ugovoru, sledite ove korake:

1. Kreirajte generičkog člana projektnog tima.
2. Generiši zahtev resursa za ovog generičkog člana projektnog tima pomoću dugmeta **Generisaj** zahtev na podmrežnoj mreži članova projektnog tima.
3. Izaberite red člana tima, a zatim kliknite na dugme **"Knjiga** " u podmrežnoj mreži. 
4. Ovo otvara tablu rasporeda sa kontekstom zahteva. Zajedno sa drugim atributima kao što su polja datuma, uloge i organizacione jedinice, filteri table rasporeda se takođe automatski popunjavaju poljima dobavljača, podizvođača i reda podizvođača iz zahteva resursa. Pošto u zahtevu nisu popunjene vrednosti podizvođača ili reda podizvođača, ovi atributi će biti prazni u oknu sa filterima.
5. Sistem traži resurse koji zadovoljavaju kriterijume filtera i navodi ih.
6. Ažurirajte polje Vrsta **radnika u** oknu sa filterima na Radnik po ugovoru **da biste** ograničili pretragu na radnike po ugovoru. Ažurirajte **dobavljača** u oknu sa filterima da biste izabrali dobavljača da biste ograničili pretragu da biste pokazali samo radnike po ugovoru koji pripadaju određenom preduzeću dobavljača.
7. Izaberite radnika po ugovoru sa liste i rezervišite resurs za zahtev.
8. Kreira se član projektnog tima. Međutim, član projektnog tima se ne ažurira ni sa jednim redom podizvođače ili podizvođačem i zato dodela resursa neće biti skupa korišćenjem cena podizvođače. Ručno ažurirajte člana projektnog tima redom podizvođač i idite na **"Procene projekta"** i izaberite **stavku Ažuriraj cene** da biste videli ažurirane troškove dodele resursa.

> [!NOTE]
> Članovi projektnog tima koji **imaju tip radnika** **kao radnika** po ugovoru, ali nemaju referencu podizvođaca, označeni su **zastavicom kao nevažeći** u **koordinatnoj mreži članova projektnog** tima. Ako postoje članovi projektnog tima sa ovim statusom, otvorite zapis člana projektnog tima i ručno ažurirajte polja reda podizvođača i podizvođača tako da procena finansijskih troškova tačno odražava trošak podizvođača na **kartici "Procene** ". 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
