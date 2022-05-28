---
title: Korišćenje kategorija nabavki sa izlaznim porudžbinama projekta i neobrađenim fakturama dobavljača
description: Ovaj tema opisuje kako se konfigurišu kategorije nabavki koje se mogu koristiti sa izlaznim porudžbinama projekta i neobrađenim fakturama dobavljača.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ee68d7906cb0c887c19a32363ec7fda547cb74bd
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613364"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Korišćenje kategorija nabavki sa izlaznim porudžbinama projekta i neobrađenim fakturama dobavljača

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Profesionalci za nabavku mogu kreirati i održavati kataloge artikala i usluga koji se mogu koristiti u izlaznim porudžbinama projekta i neobrađenim fakturama dobavljača. [Katalozi nabavki](/dynamics365/supply-chain/procurement/procurement-catalogs) vam daju jednostavan način da kategorizujete nabavke bez potrebe da konfigurišete i koristite katalog izdatih proizvoda. Svaka kategorija nabavke može biti mapirana u kategoriju projekta za transakcije vremena, troškova ili artikala. Nakon knjiženja neobrađene fakture dobavljača koja koristi kategoriju nabavke, sistem će kreirati stvarne vremenske, troškove ili materijalne projektne stavke, transakcije projekta i stavke podnaslova.

## <a name="minimum-version-requirements"></a>Minimalni zahtevi za verziju

Sledeće verzije su potrebne za korišćenje kategorija nabavki sa izlaznim porudžbinama projekta za Microsoft scenarije Dynamics 365 Project Operations zasnovane na zalihama/resursima:

- Verzija rešenja Dataverse za projektne operacije 4.41.0.45 ili novija
- Okruženje za finansije i operacije verzija 10.0.26 ili novija

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Pokrenite mape dvostrukog pisanja za podršku kategoriji nabavki

Uverite se da mapiranje za integraciju **projektnih operacija integracija reda dobavljača projekta izvoz entitet msdyn\_ projectvendorinvoiceline koristi** verziju 1.0.0.4 ili noviju.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Omogućavanje ključa funkcije za kategorije nabavki

Sledite ove korake da biste omogućili funkcionalnost korišćenja kategorija nabavki sa izlaznim porudžbinama projekta.

1. U Dynamics 365 Finance otvorite radni prostor **za upravljanje** funkcijama.
1. Na listi funkcija pronađite kategorije Korišćenje nabavki **u operacijama projekta za funkciju scenarija zasnovanih na resursima/scenarijima koji nisu snabdeveni**, a zatim izaberite stavku **Omogući**.

> [!IMPORTANT]
> Kao preduslov morate **omogućiti i opciju Omogući fakture dobavljača na čekanju u operacijama projekta za opciju scenarija zasnovanih na resursima/nefakturisanih scenarija**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Mapiranje kategorija projekta u hijerarhiji kategorije Nabavke

Sledite ove korake da biste mapirali kategorije projekata u kategorije nabavki u **hijerarhiji kategorije** nabavke:

1. Idite u kategorije **nabavki i nabavki \>**.
1. Izaberite **uredi hijerarhiju kategorija**.
1. Izaberite željeni kvrga za hijerarhiju kategorije, a zatim na kartici Dodeljivanje **kategorija projekta povežite kvrgu sa kategorijom projekta iz kategorije** Vreme **, Trošak**ili**,,Projekat **artikla" (odnosno kategorija** Podrazumevano vreme **ili** Podrazumevani troškovi **).**
1. Izaberite **Sačuvaj**.
1. Zatvorite stranicu.

> [!NOTE]
> Mapiranje kategorije nabavke u kategoriju projekta je opcionalno. Ako kategorija nabavke nije mapirana, **·** **sistem će koristiti vrednost koja je postavljena u polju Artikal u odeljku Podrazumevane vrednosti kategorije projekta** na **kartici "Operacije projekta 365** **kupaca" na stranici "Upravljanje projektima i računovodstvenim parametrima**".
