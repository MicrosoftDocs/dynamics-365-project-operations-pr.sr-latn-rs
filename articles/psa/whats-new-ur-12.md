---
title: Šta je novo ili promenjeno u izdanju 12 ispravke Project Service Automation verzije 3
description: U ovoj temi date su informacije o tome šta je novo u izdanju ispravke 12 za Project Service Automation u verziji 3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: 62c3a0c5cfbecb568faef570da309c20afd86de9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083541"
---
# <a name="project-service-automation-update-release-12-v3"></a>Project Service Automation izdanje ispravke 12, u verziji 3
Sa zadovoljstvo najavljujemo najnoviju ispravku za aplikaciju Dynamics 365 Project Service Automation (PSA). Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x. Da biste ažurirali ovo izdanje, posetite centar za administraciju za Dynamics 365 online i idite do stranice sa rešenjima kako biste instalirali ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

U ovoj temi date su funkcije koje su nove ili su promenjene u rešenju Project Service Automation u verziji 3, izdanje ispravke 12. Ova verzija ima broj verzije V3.10.2.34 i opšte je dostupna putem samo-ispravke u oktobru 2019. godine.

## <a name="update-release-12"></a>Izdanje ispravke 12

### <a name="bug-fixes"></a>Ispravke grešaka

- Vreme i trošak

    - Ispravljeno: Poruke o greškama za stavku vremena su ispravljene sa relevantnijim kontekstom.
    - Ispravljeno: Mreža stavke vremena i raspored ispravno prikazuju vertikalnu traku za listanje kada je to potrebno.
    - Ispravljeno: nije moguće odobriti prosleđene stavke troškova i vremena.
    - Ispravljeno: poruka dijaloga potvrde otkazivanja odobrenja je ispravljena i odražava status odobrenja kada se promeni iz **Odobreno** u **Prosleđeno**.
    - Ispravljeno: polja **Cena** , **Jedinica** i **Količina** su sada zaključana u zapisu troška nakon što je odobren.

- Upravljanje projektima

    - Ispravljeno: radnja **Novo** na glavnom obrascu **Član tima** je uklonjena.
    - Ispravljeno: dodele resursa su ispravljene kako bi se uzele u obzir greške u nepreciznom zaokruživanju, koje dovode do pomeranja datuma završetka zadatka.
    - Ispravljeno: u mreži zadataka korisniku će se prikazati relevantne greške na strani servera.
    - Ispravljeno: ime člana tima sada se prikazuje u zadatku birača osoba umesto naziva položaja.

- Upravljanje resursima

    - Ispravljeno: detalji o zahtevima za resursima za projekte kreirane iz predloška sada koriste kalendar projekata.
    - Ispravljeno: veštine i kompetencije sada podrazumevano potiču iz osnovnih podataka uloge u zahtev za resursom koji je kreiran za tu ulogu.

- Sales

    - Ispravljeno: duplirani ID-ovi objekta pronađeni na glavnom obrascu **Ugovor**.
    - Ispravljeno: logika je ispravljena kako bi kartica **Analiza ponude** bila vidljiva tako da prikazuje podešavanje metapodataka kartice.
    - Ispravljeno: računovodstveni datum na stvarnom zapisu sada potiče od datuma unosa vremena/troška, a ne od datuma odobrenja.
