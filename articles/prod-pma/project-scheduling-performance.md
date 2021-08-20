---
title: Performanse planiranja resursa za projekat
description: Ova tema pruža informacije o tome kako poboljšati performanse planiranja resursa za veliki broj projekata.
author: Yowelle
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 9dc638a7b2d8e0db45b5acfa5cc9512f356f8b2635028748a1e2c3230605c154
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007298"
---
# <a name="project-resource-scheduling-performance"></a>Performanse planiranja resursa za projekat

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Problemi sa učinkom koji se odnose na planiranje resursa mogu se pojaviti kada broj projekata dostigne više hiljada. Da bi se poboljšale performanse planiranja resursa, dostupna je funkcija koja omogućava korisnicima da smanje vreme potrebno za pokretanje obrasca dostupnosti resursa. Konkretno, ovo uklanja postupak zbirne sinhronizacije kapaciteta resursa i koristi tabelu **ResProjectResource** za ubrzanje pretraživanja resursa. Imajte na umu da se tabela **ResRollup** više neće koristiti.

> [!IMPORTANT]
> Ako postoji zavisnost ili postupka zbirne sinhronizacije kapaciteta resursa ili tabele **ResProjectResource**, nemojte koristiti ovu funkciju.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Omogućite poboljšanje performansi planiranja resursa
Da biste omogućili poboljšanje performansi planiranja resursa, izvršite sledeće korake.

1. Idite na **Upravljanje funkcijama** > **Sve**, a na listi funkcija pronađite **Omogući funkciju poboljšanja performansi planiranja resursa projekta**.
2. Izaberite dugme **Omogući odmah**.

> [!NOTE]
> Ako ne možete da pronađete funkciju na listi, izaberite **Proveri da li ima ažuriranja** da biste osvežili listu.

3. Osvežite pregledač, a zatim idite na **Upravljanje projektima i računovodstvo** > **Periodično** > **Resursi projekta** > **Sinhronizujte kapacitet kalendara resursa u svim kompanijama**.
4. Podesite **Uklonite postojeće evidencije o kapacitetu** na **Da** da biste uklonili prethodne podatke. Ako želite da generišete inkrementalne podatke, podesite ga na **Ne**.
5. U polju **Šifra perioda**, izaberite period u kojem treba generisati podatke. Ako izaberete šifru perioda, datumi početka i završetka ne moraju biti definisani.
6. Ako ostavite polje **Šifra perioda** prazno, odaberite određene datume početka i završetka da biste generisali podatke.
7. Izaberite **U redu**.

 > [!NOTE]
 > Ovo će distribuirati opšte podatke u tabeli **ResCalendarCapacity** u svim kompanijama u vašem okruženju, tako da grupni posao treba pokrenuti samo u jednom pravnom licu. Podaci u ovom grupnom poslu potrebni su za izračunavanje kapaciteta resursa kroz pridruženi kalendar.

8. Idite na **Upravljanje projektima i računovodstvo** > **Periodično** > **Resursi projekta** > **Popunite projektne resurse u svim kompanijama**, a zatim izaberite **U redu**. Ovo je skripta za nadogradnju podataka za opšte podatke u tabelama **ResProjectResource**, **ResCalendarDateTimeRange** i **ResEffectiveDateTimeRange**. Vrednosti za polje **PSAPRojSchedRole.RootActivity** takođe se ažuriraju. Ako se ovo ne pokrene, primićete upozorenje kada pokušate da izvršite operacije planiranja resursa.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Isključite poboljšanje performansi planiranja resursa

1. Idite na **Upravljanje funkcijama** > **Sve**, pa potražite **Omogući funkciju poboljšanja performansi planiranja resursa projekta**.
2. Izaberite funkciju, a zatim odaberite dugme **Onemogući**.
3. Osvežite pregledač.
4. Idite na **Upravljanje projektima i računovodstvo** > **Periodično** > **Sinhronizacija kapaciteta** > **Sinhronizuj zbirne vrednosti kapaciteta resursa**.
5. Na stranici **Zbirna sinhronizacija kapaciteta** podesite **Ukloni postojeće evidencije o kapacitetu** na **Da** kako biste uklonili prethodne podatke. Ako želite da generišete inkrementalne podatke, podesite ga na **Ne**.
6. U polju **Šifra perioda**, izaberite period u kojem treba generisati podatke. Ako izaberete šifru perioda, datumi početka i završetka ne moraju biti definisani.
7. Ako ostavite polje **Šifra perioda** prazno, odaberite određene datume početka i završetka da biste generisali podatke.
8. Izaberite **U redu**.

> [!NOTE]
> Ovo će distribuirati opšte podatke u tabeli **ResRollup** u svim kompanijama u vašem okruženju, tako da grupni posao treba pokrenuti samo u jednom pravnom licu. Ovaj grupni posao potreban je svim prikazima **Dostupnost resursa**. Ako se ovaj grupni posao ne pokrene, **ResRollup** podaci će se generisati u hodu, što može potrajati.


[!INCLUDE[footer-include](../includes/footer-banner.md)]