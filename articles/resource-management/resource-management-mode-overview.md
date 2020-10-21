---
title: Pregled režima upravljanja resursima
description: Ova tema pruža informacije o funkcionalnosti upravljanja resursima u usluzi Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: cf79185c8c84c55fbae55f9cfc1b17840e072b49
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930108"
---
# <a name="resource-management-modes-overview"></a>Pregled režima upravljanja resursima

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_


Dynamics 365 Project Operations podržava dva režima kako biste izvršili ukupan tok rezervacije. Režim upravljanja definisan je kao parametar projekta i može se izmeniti ako vaše poslovanje treba promeniti.    

## <a name="central-mode"></a>Centralni režim
Za organizacije koje centralizuju dodeljivanje resursa projektima, centralni režim pruža način da menadžeri projekata mogu da definišu zahteve za resursima na nivou projekta. Ispunjavanje zahteva za resursima delegira se menadžeru resursa. Menadžeri projekata mogu prihvatiti ili odbiti resurse koje predloži menadžer resursa.

![Centralni režim](./media/resource-management-central.png)

Da biste upravljali resursima u centralnom režimu, pogledajte:

- [Dodeljivanje generičkih resursa koji se mogu rezervisati zadatku i generisanje potreba za resursima](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezervisanje imenovanih resursa iz potrebe za resursima](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [Prosleđivanje zahteva za resursom](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [Ispunjavanje zahteva za resursima](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [Prihvatanje ili odbacivanje predloženog resursa projekta u zahtevu za resurs](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hibridni režim
Za organizacije kojima je potrebna fleksibilnost u raspodeli resursa, hibridni režim omogućava menadžerima projekata i menadžerima resursa mogućnost da rezervišu resurse.

![Hibridni režim](./media/resource-management-hybrid.png)

Pored podržanog procesa centralnog režima, pogledajte sledeće teme da biste upravljali svim ostalim podržanim tokovima rezervacija u hibridnom režimu:

Rezervisanje resursa direktno u projektu:
- [Rezervisanje imenovanih resursa koje je moguće rezervisati za projektni tim i dodeljivanje zadataka](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

Rezervisanje resursa iz zahteva za resursima:
- [Dodeljivanje generičkih resursa koji se mogu rezervisati zadatku i generisanje potreba za resursima](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezervisanje imenovanih resursa iz potrebe za resursima](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
