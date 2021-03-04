---
title: Faze projekta
description: Ova tema pruža informacije o fazama projekta koje su dostupne u usluzi Microsoft Dynamics Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: aa3d692a46165b01eafbd7619578cead8dd912d6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127490"
---
# <a name="project-stages"></a>Faze projekta

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Faze projekta se dizajniraju tako da odražavaju status projekta tokom njegovog napretka. Prilagođavanja se mogu koristiti za automatsko ažuriranje faza sa tokovima poslovnih procesa, Power Automate ili proširenja dodatnih komponenti.

Sledeće faze su definisane u podrazumevanom toku poslovnog procesa:

- Novi
- Ponuda
- Plan
- Isporuka
- Dovršite
- Zatvaranje 

## <a name="new"></a>Novi

Kada kreirate projekat, faza projekta se podešava na **Novo**. Ako je projekat kreiran iz predloška, možda će imati raspored, procenu i podatke o timu. U suprotnom, to je skica projekta, a preostale komponente moraju biti unete.

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