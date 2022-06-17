---
title: Tipovi faza projekata
description: Ovaj članak pruža informacije o fazama projekta.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 8d772acce152b08c7986739ac557818e6f97d0fe
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919077"
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
