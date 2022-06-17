---
title: Parametri integracije usluge Project Service Automation
description: Ovaj članak sadrži objašnjenja o tome kako da konfigurišete način na koji se podrazumevani podaci unose kada se integrišete Microsoft Dynamics 365 for Project Service Automation Microsoft Dynamics sa 365 Finansija.
author: ruhercul
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: a4abeb2960981196ed1d7c453e7daa0558e326ef
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932313"
---
# <a name="project-service-automation-integration-parameters"></a>Parametri integracije usluge Project Service Automation

[!include[banner](../includes/banner.md)]

Na stranici **"Parametri integracije za automatizaciju usluge projekta**" možete da konfigurišete način na koji se podrazumevani podaci unose kada se integrišete Dynamics 365 Project Service Automation sa Dynamics 365 Finance. Da bi se projekti uspešno sinhronizovali iz usluge Project Service Automation u Finance, morate podesiti sledeća polja.

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