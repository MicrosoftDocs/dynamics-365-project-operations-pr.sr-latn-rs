---
title: Parametri integracije usluge Project Service Automation
description: Ova tema objašnjava kako da konfigurišete način unosa podrazumevanih podataka prilikom integracije usluge Microsoft Dynamics 365 for Project Service Automation sa uslugom Microsoft Dynamics 365 Finance.
author: ruhercul
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: b8faba1d799e360e58d47a02dc8b46e09fa0d393
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270920"
---
# <a name="project-service-automation-integration-parameters"></a>Parametri integracije usluge Project Service Automation

[!include[banner](../includes/banner.md)]

Na stranici **Parametri integracije usluge Project Service Automation** možete da konfigurišete način unosa podrazumevanih podataka prilikom integracije usluge Dynamics 365 Project Service Automation sa uslugom Dynamics 365 Finance. Da bi se projekti uspešno sinhronizovali iz usluge Project Service Automation u Finance, morate podesiti sledeća polja.

Da biste otvorili stranicu **Parametri integracije usluge Project Service Automation**, idite na **Upravljanje projektima i računovodstvo** \> **Podešavanje** \> **Parametri integracije usluge Dynamics 365 for Project Service Automation**. 

> [!NOTE]
> - Integracija projektnih zadataka, kategorije transakcija troškova, procene sati, procene troškova i zaključavanje funkcionalnosti dostupni su u verziji 8.0.
> - Integracija stvarnih podataka dostupna je u verziji 8.0.1 ili novijoj.


| KArtica                    | Polje                | Opis |
|------------------------|----------------------|-------------|
| Opšte                | Podrazumevani tip projekta | Izaberite podrazumevani tip projekta. Kada se projekti sinhronizuju iz usluge Project Service Automation, ova vrednost se koristi ako u šablonu integracije niste naveli podrazumevanu vrednost. Tokom sinhronizacije, polje **Tip projekta** novih projekata postavljeno je na ovu vrednost. Međutim, vrednost se može ažurirati kada se predmeti ugovora o projektu sinhronizuju iz usluge Project Service Automation. |
|                        | Kategorija vremena        | Izaberite kategoriju vremena podrazumevanog zapisa. Ova vrednost se koristi kada se procene sati sinhronizuju iz usluge Project Service Automation. Kada se procene sati i aktuelne vrednosti sata sinhronizuju iz Project Service Automation, polje **Kategorija** novih predviđanja vremena za projekat u usluzi Finance postavljeno je na ovu vrednost. |
|                        | Kategorija naknade         | Izaberite kategoriju podrazumevane naknade. Ova vrednost se koristi kada se aktuelni podaci o naknadama sinhronizuju iz usluge Project Service Automation. Kada se aktuelni podaci o naknadama sinhronizuju iz usluge Project Service Automation, polje **Kategorija** novih predviđanja naknade u usluzi Finance se postavlja na ovu vrednost. |
| Podrazumevane vrednosti grupe projekata | Tip projekta         | Kliknite na **Novo** da biste dodali red u kome možete da odaberete tip projekta za koji ćete postaviti podrazumevanu grupu projekata. Određeni tip projekta može se odabrati samo jednom u konfiguraciji. |
|                        | Grupa projekata        | Izaberite podrazumevanu grupu projekata za izabrani tip projekta. Kada se novi projekti sinhronizuju iz usluge Project Service Automation, polje **Grupa projekata** se postavlja na podrazumevanu vrednost za tip projekta ako niste naveli podrazumevanu vrednost u predlošku za integraciju. |
| Podrazumevane vrste naplate  | Tip naplate         | Kliknite na **Novo** da biste dodali red u kome možete da odaberete vrstu naplate za koju ćete postaviti podrazumevano svojstvo reda. Određena vrsta naplate se može izabrati samo jednom u konfiguraciji. |
|                        | Svojstvo reda        | Izaberite podrazumevano svojstvo reda za izabranu vrstu naplate. Kada se nove procene sati, nove procene troškova ili nove stvarne vrednosti sinhronizuju iz usluge Project Service Automation, polje **Svojstvo linije** se postavlja na podrazumevanu vrednost za vrstu naplate. |
| Zaključavanje funkcionalnosti  | Nije primenjivo       | Izaberite funkcionalnost koju ćete onemogućiti u usluzi Finance za projekte i ugovore koji potiču iz usluge Project Service Automation. Na primer, možete da isključite mogućnost uređivanja ugovora i projekata, kreiranja strukturne analize posla i unosa vremenskih rasporeda u Finance. Polja koja se odnose na računovodstvo i dalje će biti omogućena, čak i ako postanu nedostupna podešavanjem parametra. Podrazumevano je omogućena sva funkcionalnost. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]