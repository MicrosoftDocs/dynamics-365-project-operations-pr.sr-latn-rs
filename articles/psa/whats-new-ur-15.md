---
title: Šta je novo ili promenjeno u izdanju 15 ispravke Project Service Automation verzije 3
description: Ovaj članak pruža informacije o tome šta je novo u izdanju za ažuriranje automatizacije usluge projekta Release 15, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: b87cae2cd8913457c2931d1661a57509d1398d29
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915661"
---
# <a name="project-service-automation-update-release-15-v3"></a>Project Service Automation izdanje ispravke 15, u verziji 3

[!include [banner](../includes/psa-now-project-operations.md)]

Sa zadovoljstvo najavljujemo najnoviju ispravku za aplikaciju Dynamics 365 Project Service Automation (PSA). Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x. Da biste ažurirali ovo izdanje, posetite centar za administraciju za Dynamics 365 online i idite do stranice sa rešenjima kako biste instalirali ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).

Ovaj članak navodi funkcije i ispravke koje su nove ili promenjene za PSA V3, Izdanje za ažuriranje 15. Ova verzija ima broj verzije V3.10.5.28 i opšte je dostupna putem samo-ispravke u januaru 2020. godine.

## <a name="update-release-15"></a>Izdanje ispravke 15 

### <a name="enhancements"></a>Poboljšanja

- Upravljanje projektima

### <a name="bug-fixes"></a>Ispravke grešaka

- Vreme i trošak

  - Ispravljeno: dodavanje rukovanja greškom prilikom učitavanja u prikazu usklađivanja.
  - Ispravljeno: čvorište resursa za projekat: preimenovanje stavke **Iznos** radi smanjenja dvosmislenosti.
  - Ispravljeno: podešavanje prikaza **Kopiranje kolona za stavku vremena** tako da obuhvata tip.
  - Ispravljeno: uređivanje trajanja stavke vremena u prikazu mreže korišćenjem decimalnih brojeva rezultira nepoznatom greškom kod nekih brojeva.

- Upravljanje projektima

  - Ispravljeno: padajući meni za **Korišćenje u prikazu praćenja** se sada proširuje na osnovu širine opcija.
  - Ispravljeno: kada upravljate projektima u vremenskoj zoni +13, proračuni zadataka mogu prikazati netačne rezultate.
  - Ispravljeno: **Vreme završetka člana tima** je ispravljeno kada se koristi kalendar od 24 sata.
  - Ispravljeno: ponovo aktiviran **BPF** u glavnom obrascu **msdyn_project**.
  - Ispravljeno: izračunavanje zadataka više ne ignoriše jedan dan.
  - Ispravljeno: novi baner obaveštenja je dodat u obrazac projekta kada se vremenska zona razlikuje između korisnika i projekata.

- Sales

  - Ispravljeno: pronalaženje kategorije procene troškova može da se koristi za filtriranje duplikata.
  - Ispravljeno: kôd u **PluginDomain.ExecuteInTryCatchBlock(..)** više ne sakriva poreklo izuzetka.
  - Ispravljeno: više se ne dobija poruka o grešci u stavci **Pronalaženje projekta** u obrascu **Stavka ponude** kada ima preko 1000 projekata.
  - Ispravljeno: Mreža **Procene** za procene cene rada i cene troškova sada prikazuje ispravan simbol valute.
  - Ispravljeno: nakon što organizacija ažurira PSA sa izdanja ispravke 14 na izdanje ispravke 15, kartica **Raspored** se više ne pojavljuje kao prazna u obrascu **Projekat**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
