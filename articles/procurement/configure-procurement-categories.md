---
title: Korišćenje kategorija nabavke sa porudžbenicama projekta i fakturama dobavljača na čekanju
description: U ovom članku opisano je kako da konfigurišite kategorije nabavki koje mogu da se koriste sa porudžbenicama projekta i fakturama dobavljača na čekanju.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f71c6bfcd183613471a4cc10e16a5a54571fac31
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028627"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Korišćenje kategorija nabavke sa porudžbenicama projekta i fakturama dobavljača na čekanju

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Profesionalci za nabavku mogu kreirati i održavati kataloge artikala i usluga koji se mogu koristiti u porudžbenicama na projektu i neobrađenim fakturama dobavljača. [Katalozi za nabavku](/dynamics365/supply-chain/procurement/procurement-catalogs) vam daju jednostavan način da kategorizujete nabavke bez potrebe da konfigurišete i koristite objavljeni katalog proizvoda. Svaka kategorija nabavke može biti mapirana u kategoriju projekta za transakcije vremena, troškova ili artikala. Nakon knjiženja neobrađene fakture dobavljača koja koristi kategoriju nabavke, sistem će kreirati stvarne vrednosti za vreme, troškove ili materijale na projektu, transakcije projekta i stavke u knjizi analitike.

## <a name="minimum-version-requirements"></a>Minimalni zahtevi verzije

Sledeće verzije su potrebne za korišćenje kategorija nabavki sa porudžbenicama projekta za Microsoft Dynamics 365 Project Operations bez zaliha/zasnovane na resursa:

- Rešenje Project Operations Dataverse u verziji 4.41.0.45 ili novije
- Okruženje za finansije i operacije u verziji 10.0.26 ili novijoj

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Pokrenite mape dvostrukog upisivanja za podršku kategoriji nabavke

Uverite se da je mapiranje za **Project Operations entitet izvoza reda fakture prodavca (msdyn\_projectvendorinvoicelines)** koristi verziju 1.0.0.4 ili noviju.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Omogućavanje ključa funkcije za kategorije nabavki

Pratite ove korake da biste omogućili funkcionalnost korišćenja kategorija nabavki sa porudžbenicama na projektu.

1. U Dynamics 365 Finance, otvorite radni prostor **Upravljanje funkcijama**.
1. Na listi funkcija pronađite funkciju **Koristi kategorije nabavke u Project Operations za resurs/scenarije koji nisu zasnovani na zalihama**, a zatim izaberite **Omogući**.

> [!IMPORTANT]
> Kao preduslov, morate da omogućite i funkciju **Omogućite fakture dobavljača na čekanju u Project Operations za resurs/scenarije koji nisu zasnovani na zalihama**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Mapiranje kategorija projekta u hijerarhiji kategorije nabavke

Pratite ove korake da biste mapirali kategorije projekata u kategorije nabavki u hijerarhiji **Kategorije nabavke**:

1. Idite u **Nabavka i poreklo \> Kategorije nabavke**.
1. Izaberite **Uredi hijerarhiju kategorija**.
1. Izaberite željeni čvor hijerarhije kategorija, a zatim na kartici **Dodela kategorija projekta** povežite oglas sa kategorijom projekta iz kategorije **Vreme**,  **Trošak** ili **Projekat artikla** (to jest, **Podrazumevano vreme** ili **Podrazumevani troškovi**).
1. Izaberite **Sačuvaj**.
1. Zatvorite stranicu.

> [!NOTE]
> Mapiranje kategorije nabavke u kategoriju projekta je opciono. Ako Kategorija nabavke nije mapirana, sistem će koristiti vrednost koja je postavljena u polju **Artikal** u odeljku **Podrazumevane kategorije projekata** na kartici **Project Operations u usluzi Dynamics 365 Customer Engagement** na stranici **Parametri upravljanja projektom i računovodstvo**.
