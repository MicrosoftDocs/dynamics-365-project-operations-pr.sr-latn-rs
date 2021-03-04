---
title: Šta je novo ili promenjeno u izdanju 16 ispravke Project Service Automation verzije 3
description: U ovoj temi date su funkcije i ispravke koje su dostupne u izdanju 16 ispravke za Project Service Automation verzije 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 882ee6c25e5d88db22e051254c7fd82dc787ab73
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143650"
---
# <a name="project-service-automation-update-release-16-v3"></a>Project Service Automation izdanje ispravke 16, u verziji 3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti.  Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x. Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku. Za još informacija pogledajte članak [Instaliranje i ispravka željenog rešenja](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).
U ovoj temi date su funkcije i ispravke koje su nove ili su promenjene u rešenju PSA u verziji 3, izdanje ispravke 16. Ova verzija ima broj verzije V3.10.6.34 i opšte je dostupna putem samo-ispravke u januaru 2020. godine.


## <a name="update-release-16"></a>Izdanje ispravke 16

### <a name="bug-fixes"></a>Ispravke grešaka

-   Vreme i trošak

    -   Ispravljeno: Korisnici koji pokušavaju da proslede izbrisane unose vremena i troška za odobrenje će sada primati relevantne poruke o grešci.

-   Upravljanje projektima

    -   Ispravljeno: jedinice za obezbeđivanje resursa definisanih za članove tima u šablonima se poštuju, a predlošci se primenjuju na novi projekat.

    -   Ispravljeno: poboljšano rukovanje ponovnim dodeljivanjem vlasništva nad zapisima.

    -   Ispravljeno: projekte koji su u procesu kopiranja neće biti dozvoljeno kopirati dok se ne završe sve operacije kopiranja.

-   Upravljanje resursima

    -   Ispravljeno: Produži rezervacije sada ispravno upravlja kratkim trajanjima i više ne kreira nula časova za produžene rezervacije.

    -   Ispravljeno: prikaz sravnjenja se sada prikazuje kada je vremenska zona projekta +5:30 GMT, a vremenska zona klijenta je drugačija.

-   Sales

    -   Ispravljeno: kada se ukloni projekat mapiran na predmetu ugovora i mapira se novi projekat, stvarni zapisi o novom projektu nisu bili preispitivani na osnovu pravila za obračun i cena definisanih na liniji ugovora. Ovo je ispravljeno u ovom izdanju. Cene i stvarni zapisi projekta koji je skoro mapiran će biti opozvani, pa ponovo kreirani ispravno na osnovu pravila o cenama i naplatama iz predmeta ugovora. Kao posledica ovoga, stvarni zapisi o projektu koji nije mapiran će takođe biti ponovo procenjeni, pa ponovo kreirani.

    -   Fiksno: dodata je dodatna provera u stavku procene, u polje **Iznos**, kako bi se osiguralo da se nulte vrednosti ne zadržavaju.

    -   Fiksno: kada se na projektu ažurira trenutno stanje, u glavni obrazac projekta se dodaje dugme za osvežavanje kako bi se korisnicima omogućilo da ponovo sinhronizuju trenutno stanje.

    -   Fiksno: kada korisnici nadograde sa 2.X na 3.X, dozvoljavaju se projekti čija je vrednost za naziv projekta NULL.



[!INCLUDE[footer-include](../includes/footer-banner.md)]