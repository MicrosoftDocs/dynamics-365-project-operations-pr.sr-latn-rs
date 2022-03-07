---
title: Pregled režima upravljanja resursima
description: U ovoj temi date su informacije o funkciji upravljanja resursima u usluzi Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: 41265534661e51565bf31105ef69cec9b3b181c3
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 07/07/2021
ms.locfileid: "6367908"
---
# <a name="resource-management-modes-overview"></a>Pregled režima upravljanja resursima

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_


Dynamics 365 Project Operations podržava dva režima kako biste izvršavali ukupan tok rezervacije. Režim upravljanja definisan je kao parametar projekta i može se izmeniti ako vaše poslovanje treba promeniti.    

## <a name="central-mode"></a>Centralni režim
Za organizacije koje centralizuju dodeljivanje resursa projektima, centralni režim pruža način da menadžeri projekata mogu da definišu zahteve za resursima na nivou projekta. Ispunjavanje zahteva za resursima delegira se menadžeru resursa. Menadžeri projekata mogu prihvatiti ili odbiti resurse koje predloži menadžer resursa.

![Centralni režim](./media/resource-management-central.png)

Da biste upravljali resursima u centralnom režimu, pogledajte:

- [Dodeljivanje generičkih resursa koji se mogu rezervisati zadatku i generisanje potreba za resursima](/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezervisanje imenovanih resursa iz potrebe za resursima](/dynamics365/project-service/book-named-resource)
- [Prosleđivanje zahteva za resursom](/dynamics365/project-service/submit-resource-request)
- [Ispunjavanje zahteva za resursima](/dynamics365/project-service/resource-management-fulfill-requests)
- [Prihvatanje ili odbacivanje predloženog resursa projekta u zahtevu za resurs](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hibridni režim
Za organizacije kojima je potrebna fleksibilnost u raspodeli resursa, hibridni režim omogućava menadžerima projekata i menadžerima resursa mogućnost da rezervišu resurse.

![Hibridni režim](./media/resource-management-hybrid.png)

Pored podržanog procesa centralnog režima, pogledajte sledeće teme da biste upravljali svim ostalim podržanim tokovima rezervacija u hibridnom režimu:

Rezervisanje resursa direktno u projektu:
- [Rezervisanje imenovanih resursa koje je moguće rezervisati za projektni tim i dodeljivanje zadataka](/dynamics365/project-service/assign-named-bookable-resource)

Rezervisanje resursa iz zahteva za resursima:
- [Dodeljivanje generičkih resursa koji se mogu rezervisati zadatku i generisanje potreba za resursima](/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezervisanje imenovanih resursa iz potrebe za resursima](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]