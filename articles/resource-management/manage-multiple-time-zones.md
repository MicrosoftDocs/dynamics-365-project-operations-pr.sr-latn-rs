---
title: Upravljanje vremenskim zonama
description: Kada se projekat kreira, njegova vremenska zona zasniva se na vremenskoj zoni definisanoj u predlošku radnog sata koji se primenjuje.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27f58f0dacc3404119a719547ad374629c740740
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083518"
---
# <a name="manage-time-zones"></a>Upravljanje vremenskim zonama

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_


## <a name="projects"></a>Projekti

Kada se projekat kreira, njegova vremenska zona se zasniva na vremenskoj zoni definisanoj u predlošku radnog sata koji se primenjuje. Na obrascu **Projekat** , datumi su uvek relativni u odnosu na vremensku zonu korisnika koji je prijavljen na svakoj kartici, osim kartice **Zadatak**. Kada pregledate strukturne analize posla, datumi će se uvek prikazivati u vremenskoj zoni projekta.

## <a name="tasks"></a>Zadaci

Kada se zadatak kreira, vreme početka, vreme završetka i broj sati na dan kontrolišu se radnim vremenom projekta. Na primer, ako se zadatak kreira sa projektom čija je vremenska zona -8 PST i ima radno vreme od 9:00 do 17:00 od ponedeljka do petka, svaki zadatak kreiran bez dodele poštovaće vreme početka i vreme završetka kalendara projekta.

## <a name="manage-resources-with-time-zones"></a>Upravljanje resursima pomoću vremenskih zona

Za tačne i predvidljive rezultate prilikom upotrebe **produženja rezervacije** , postoje dva ključna preduslova koja moraju biti ispunjena:  

- Korisnik mora da konfiguriše vremensku zonu svog uređaja tako da odgovara vremenskoj zoni definisanoj u sistemskim **podešavanjima personalizacije**.
 
  ![Podešavanja vremenske zone u operativnom sistemu Windows 10](media/reconcile-assignments-03.png)

  ![Podešavanja vremenske zone u podešavanjima personalizacije](media/reconcile-assignments-04.png)
 
- Resurs koji može da se rezerviše mora imati najmanje jedan minut radnog vremena koji se preklapa sa konturama koje se koriste za definisanje traženog dodatka. Na primer, sledeći resursi sa radnim vremenom koje pada između 9:00 i 19:00. 

  ![Poređenje kontura resursa](media/reconcile-assignments-05.png)

Sledeća tabela prikazuje:

- Predložak kalendara projekta
- Resurs A: ovaj resurs ima isti kalendar i nalazi se u istoj vremenskoj zoni kao i projekat. Početno vreme rezervacije će biti u 9:00.
- Resurs B: Ovaj resurs se nalazi u drugoj vremenskoj zoni u odnosu na projekat i počinje u 7:00 u svojoj vremenskoj zoni. Međutim, rezervacije će početi u 9:00, jer je to najranije vreme početka konture zadatka.
- Resursi C i D: Resursi se nalaze u različitim vremenskim zonama, različitim međusobno i u odnosu na projekat, a njihove rezervacije započinju najranije od odgovarajućeg raspoloživog vremena početka.

|Entitet  |Kalendar  |
|-|-|
|Predložak kalendara projekta   | ![kalendar projekta](media/reconcile-assignments-06.png) |
|Resurs A  | ![Kalendar resursa A](media/reconcile-assignments-06.png) |
|Resurs B  |  ![Kalendar resursa B](media/reconcile-assignments-07.png) |
|Resurs C  |  ![Kalendar resursa C](media/reconcile-assignments-08.png) |
|Resurs D  | ![Kalendar resursa D](media/reconcile-assignments-09.png)  |
 
Kada odete na prikaz **Usaglašavanje** , prikazuju se dodele resursa i pridruženi nedostaci rezervacija.

![Prikaz usklađivanja pre produžetka](media/reconcile-assignments-10.png)

Kada se za svaki resurs koristi funkcija proširenog rezervisanja, rezervacije se uspešno produžavaju za svaki resurs, jer se radno vreme svakog resursa preklapa sa konturama nedostatka.

![Prikaz usklađivanja nakon produženja rezervacije](media/reconcile-assignments-11.png) 

Primetite da bolji uvid u detalje rezervacije pokazuje razlike u vremenu početka rezervacija. Rezervacije počinju ne ranije od vremena početka konture dodele i ne ranije od raspoloživog vremena početka resursa.

![Nove rezervacije resursa na tabeli rasporeda](media/reconcile-assignments-12.png)
