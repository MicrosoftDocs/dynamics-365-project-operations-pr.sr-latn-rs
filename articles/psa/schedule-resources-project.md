---
title: Planirajte resurse za projekat
description: Kako da planirate resurse za projekat u aplikaciji Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: e39c95386eb2dd31fb54878bc203bd94931274de
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150460"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Planiranje resursa za projekat (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Možete da proverite dostupnost resursa da biste dobili ukupan prikaz toga koliko su rezervisani resursi ili možete filtrirati prikaz prema veštinama, timu, lokaciji i ostalim opcijama.  
  
Tabla rasporeda prikazuje listu resursa i njihovu dostupnost. Izaberite režim prikaza za prikazivanje dostupnosti prema **Satima**, **Danima**, **Nedelji** ili **Mesecu**.  
  
Pre nego što možete da koristite tabelu rasporeda, važno je da je podesite. Više informacija potražite u odeljku [Konfigurišite tablu rasporeda (Field Service ili Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).
  
Ako koristite stariju verziju, za dostupnost resursa pogledajte [Prikaz dostupnosti resursa](../psa/view-resource-availability.md).  

> [!IMPORTANT]
>  Da biste koristili funkcionalnost rezervacije tabele rasporeda, geografsko kodiranje i usluge za lokaciju, potrebno je da uključite mape.  
> 
> 1. U glavnom meniju izaberite **Planiranje resursa** > **Administracija**.  
> 2. Kliknite na **Parametri planiranja**.  
> 3. Otvorite zapis i pomerite se nadole do odeljka **Resource Scheduling Optimization**.  
> 4. U polju **Povezivanje sa mapama** odaberite **Da**.  
> 5. Prihvatite uslove i sačuvajte zapis.  
> 6. U glavnom meniju izaberite **Project Service** > **Tabela rasporeda**. Odavde, postoji nekoliko načina da ručno zakažete zahtev za rezervaciju. Izaberite metod koji funkcioniše za vas.
  
## <a name="find-available-resources"></a>Pronađite dostupne resurse

1.  Na listi **Zahtev za rezervaciju** kliknite desnim tasterom miša na nezakazanu rezervaciju i izaberite jedno od sledećeg:  
  
- Odaberite **Pronađi dostupnost – Trenutni resursi** da biste pronašli dostupan resurs sa liste na tabli rasporeda.  
- Odaberite **Pronađi dostupnost – Svi resursi**, da biste pronašli dostupan resurs u resursima u sistemu  
   > [!NOTE]
   >  Kada to uradite, filteri će prikazati opcije za izabrani zahtev za rezervaciju.  
  
2. Kada vidite dostupni termin, kliknite desnim tasterom miša na vremenski interval na tabeli rasporeda i odaberite **Rezerviši ovde**. Ili prevucite i ispustite zahtev rezervacije na dostupan vremenski interval.  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>Rezervišite resurs pomoću dnevnog prikaza i pronađite ko nema dovoljno rezervacija
  
1.  Na tabeli rasporeda, izaberite **Režim prikaza**, a zatim izaberite **Dani**.  
  
    Ovo prikazuje prikaza koordinatne mreže koliko je sati resurs rezervisan po danu i kojim danima je slobodan.  
  
2.  Kliknite na ime resursa koji želite da rezervišete, a zatim izaberite **Rezerviši**.  
  
3.  U dijalogu **Rezervacija resursa (kreiranje)** izaberite projekat za koji želite da rezervišete resurs za zajedno sa metodom rezervacije i vremenima početka i završetka.  
  
4.  Kada završite, izaberite **Rezerviši**.  
  
## <a name="view-to-the-schedule-board"></a>Prikaz tabele rasporeda
  
1.  Izaberite nezakazani zahtev za rezervaciju sa liste na dnu.  
  
2.  Prevucite zahtev za rezervaciju na dostupni resurs/vremenski interval na tabli rasporeda.  
  
3.  Kada završite, izaberite **Rezerviši**.  
  
### <a name="additional-resources"></a>Dodatni resursi  
 [Vodič za menadžera resursa](../psa/resource-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]