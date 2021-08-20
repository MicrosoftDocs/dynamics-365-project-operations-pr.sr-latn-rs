---
title: Tipovi faza projekata
description: Ova tema pruža informacije o stvarnim fazama projekta.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e4f50d12b4f0bf1586d0a5702bcd38b891590bffe0d3f9661d7f5d170877b54e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996903"
---
# <a name="project-stage-types"></a>Tipovi faza projekata 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Faze projekta se dizajniraju tako da odražavaju status projekta tokom njegovog napretka. Prilagođavanja se mogu koristiti za automatsko ažuriranje faza sa tokovima poslovnih procesa, Power Automate ili proširenja dodatnih komponenti.

Sledeće faze su definisane u podrazumevanom toku poslovnog procesa:

- Novi
- Ponuda
- Plan
- Isporuka
- Dovršeno
- Zatvori 

## <a name="new"></a>Novo

Kada kreirate projekat, faza projekta se podešava na **Novo**. Ako je projekat kreiran iz predloška, možda će imati raspored, procenu i podatke o timu. U suprotnom, to je samo skica projekta, a preostale komponente moraju biti unete.

## <a name="quote"></a>Ponuda

Kada povežete projekat sa ponudom ili ga kreirate iz ponude, faza projekta se podešava na **Ponuda**, a procenjeni datum početka i završetka se ažuriraju. Dok je projekat je u fazi **ponude**, kartica **Prodaja** na stranici **Entitet projekta** prikazuje detalje ponude.

## <a name="plan"></a>Plan

Kada vam bude odobrena ponuda povezana sa projektom i kada se projekat prebaci u fazu **ugovora**, faza projekta se ažurira na **Plan**. Dok je projekat u fazi **plana**, na stranici **Entitet projekta** se prikazuju detalji ugovora.

## <a name="deliver"></a>Isporuka

Kada je projektni plan završen, a vi ste spremni za početak projekta, menadžer projekta treba da ažurira fazu projekta na **Isporuka** da bi pokazao da je projekat započet.

## <a name="complete"></a>Dovršeno 

Kada je posao za projekat završen, menadžer projekta može da ažurira fazu na **Dovršeno**. Ažuriranjem faze projekta na **Dovršeno**, menadžer projekta pokazuje da je posao završen 100%, ali da je projekat i dalje otvoren tako da se mogu evidentirati bilo kakve stavke vremena ili troškova na čekanju.

## <a name="close"></a>Zatvori

Kada se sve transakcije evidentiraju za projekat, menadžer projekta može da ažurira fazu na **Zatvoreno**. U tom trenutku ne mogu se evidentirati nikakve transakcije i projekt se podešava na „samo za čitanje“.


[!INCLUDE[footer-include](../includes/footer-banner.md)]