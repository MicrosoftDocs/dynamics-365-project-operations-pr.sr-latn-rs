---
title: Šta je novo ili promenjeno u izdanju 40 ispravke Project Service Automation verzije 3
description: U ovom članku navedene su funkcije i ispravke koje su dostupne u izdanju 40 ispravke usluge Microsoft Dynamics 365 Project Service Automation verzije 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: dca7f340b8d544b183aa0390ac3c11a38f536ed0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912809"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Šta je novo ili promenjeno u izdanju 40 ispravke Project Service Automation verzije 3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da najavimo najnoviju ispravku za aplikaciju Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Kompatibilna je sa sistemom Dynamics 365 9.x. Da biste se ažurirali na ovo izdanje, posetite stranicu centra administracije za Dynamics 365 mrežna rešenja i instalirajte ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).

U ovom članku date su funkcije koje su nove ili su promenjene u rešenju Project Service Automation u verziji 3, izdanje ispravke 40. Ova verzija ima broj verzije V3.10.61.61 i generalno je dostupna putem samostalnog ažuriranja u februaru 2022.

## <a name="update-release-40"></a>Izdanje ispravke 40

### <a name="features"></a>Funkcije
Prva faza nadogradnje 1 sa Project Service Automation na Project Operations – jednostavnom primenom biće objavljena u februaru 2022. godine za sve klijente. Da biste proverili da li ispunjavate uslove, pogledajte [Nadogradnja sa aplikacije Project Service Automation na uslugu Project Operations](upgrade-project-operations-non-stocked.md). Ako se aplikacija ne pojavi u vašoj instanci u Power Platform centru administracije, obratite se podršci i zatražite da to bude omogućeno za vaša okruženja. Vaš zahtev mora da sadrži listu ID-ova okruženja gde je potrebno omogućiti aplikaciju.

### <a name="bug-fixes"></a>Ispravke grešaka

Popravljeni su sledeći problemi.

**Vreme i trošak**
- Stavka beleške nedostaje kada je stavka vremena odbijena ili otkazana. 

**Prodaja**

- Kada ažurirate procenu cene ili prodaje korišćenjem gotovih dodatnih komponenti, neispravno vam je dozvoljeno da šaljete JSON korisne podatke koji nisu važeći izvan korisničkog interfejsa.
- Kada ažurirate redove ponude pomoću brzog prikaza, dozvoljeno vam je da aktivirate ponude.
