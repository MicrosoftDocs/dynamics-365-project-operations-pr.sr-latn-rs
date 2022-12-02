---
title: Šta je novo u februaru 2021. – Project Operations jednostavna primena
description: Ovaj članak pruža informacije o ispravkama kvaliteta dostupnim u izdanju jednostavne primene usluge Project Operations za februar 2021.
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 329bc31ad4c0958fe60e73b257e6b4c262bb60f9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914051"
---
# <a name="whats-new-february-2021---project-operations-lite-deployment"></a>Šta je novo u februaru 2021. – Project Operations jednostavna primena

Ovaj članak se odnosi na sledeće komponente i verzije usluge Dynamics 365 Project Operations:

  - Project Operations u Dataverse okruženju verzije 4.7.0.95

## <a name="quality-updates"></a>Ispravke kvaliteta

| **Oblast funkcija** | **Referentni broj** | **Ispravka kvaliteta** |
| --- | --- | --- |
| **Naplata i određivanje cena** | 2053736 | Detalji stavke fakture sada su dostupni ako odete na **Faktura** > **Srodne informacije**. |
| **Naplata i određivanje cena** | 2122613 | Radnje **Aktiviraj** i **Deaktiviraj** su uklonjene iz entiteta veze **cenovnika**. |
| **Naplata i određivanje cena** | 2128606 | Rešen je problem sa **ullReferenceException** u dodatnoj komponenti **GetEstimatesForProject**. |
| **Primena i konfiguracija** | 2140569 | Projektno rešenje ne sme da se instalira u okruženje Dataverse Teams. |
| **Primena i konfiguracija** | 2086991 | Ograničeno prilagođavanje lokalizacije veb-resursa. |
| **Upravljanje mogućnostima za poslovanje** | 2136794 | Prikažite tačnu poruku o grešci kada proces **Potvrdi fakturu** ili **Označi fakturu kao plaćenu** ne uspe. |
| **Upravljanje mogućnostima za poslovanje** | 2146376 | Ispravljen iznos poreza u stvarnom nenaplativom iznosu se kreira na osnovu potvrde fakture. |
| **Planiranje i praćenje projekta** | 2099879 | Primena Dataverse okruženja mora da kreira podrazumevanu kategoriju transakcija sa statičkim ID-om, a ne da nasumično generiše jedan po okruženju. |
| **Planiranje i praćenje projekta** | 2128577 | Ispravljene su Project Service privilegije korisnika za ažuriranje kategorije transakcije u dodeli resursa. |
| **Planiranje i praćenje projekta** | 2164035 | Rešeni su problemi sa funkcijom **Kopiraj projekat**. |
| **Stavka vremena** | 2129161 | Primenjuju se stroža ograničenja kako bi se osiguralo da korisnici ne mogu promeniti i ažurirati unos vremena koji je poslat ili odobren. |
| **Stavka vremena** | 2103572 | Odobrenje vremena za unose vremena koji se ne odnose na projekat ne sme tražiti ulogu odobravaoca projekta. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]