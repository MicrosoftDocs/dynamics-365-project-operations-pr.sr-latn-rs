---
title: Šta je novo ili promenjeno u Project Service Automation izdanju ispravke 20 u verziji 3
description: U ovoj temi date su funkcije i ispravke koje su dostupne u Project Service Automation izdanju ispravke 20 u verziji 3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: ee3be43da401af405ab329b9b5a724a2e95c0219
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147130"
---
# <a name="project-service-automation-update-release-20-v3"></a>Project Service Automation izdanje ispravke 20, u verziji 3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x. Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

U ovoj temi date su funkcije koje su nove ili su promenjene u rešenju Project Service Automation u verziji 3, izdanje ispravke 20. Broj izrade ove verzije je V 3.10.31.37 i uglavnom je dostupna putem samostalnog ažuriranja u junu 2020. godine.

## <a name="update-release-20"></a>Izdanje ispravke 20

### <a name="bug-fixes"></a>Ispravke grešaka

**Upravljanje projektima**

Popravljeni su sledeći problemi:

- Uvoz članova projektnog tima metodom raspodele koja zahteva sate rezultira nejasnom porukom o grešci kada su navedeni sati nula.
- Korisnici dobijaju pogrešnu grešku kada je u polje **Opis** unet maksimalan broj znakova za projektni zadatak.
- Stranica **Preuzimanje Microsoft Dynamics 365 Project Service Automation programskog dodatka** se preusmerava na englesku stranicu za preuzimanje kada su podešavanja jezika korisnika podešene na japanski.
- Kada dođe do greške na serveru, oznaka sinhronizacije na kartici **Raspored** obrasca **Projekti** ponekad ostaje.
- Suvišna ažuriranja zadataka se šalju serveru kada je zadatak izmenjen.

**Sales**

Popravljeni su sledeći problemi:

- Na obrascu **Ugovor**, dvostruki klik na **Kreiraj fakturu** kreira dve fakture za jedan stvarni zapis.
- U rešenju Internet Explorer 11,korisnici ne mogu da kreiraju stavke troškova.
- Storniranje troškova i storniranje nefakturisanih stvarnih podataka o prodaji nisu povezani.
- Dugme **Osveži stvarne troškove** na obrascu **Projekat** ne osvežava stavku **Stvarni sati za zadatak**.
- Dodatna komponenta **PreValidateProjectTeamMemberCreate** može da kreira duplirane generičke resurse koji mogu da se rezervišu kada je atribut **msdyn_isgenericresourceprojectscoped** podešen na **Netačno**.
- **Ponovo izračunaj** briše naplative troškove detalja ponude zasnovane na proizvodu i detalje predmeta ugovora.
- U određenim scenarijima dodatna komponenta **PostEstimateLineUpdate** prikazuje grešku izuzetka nedefinisane reference.
- Trajanje vremenske faze na **Grafikonu analize profitabilnosti** se ne podudara se sa trajanjem troškova u detaljima linije ponude sa fiksnom cenom na ponudi.
- Vrednosti za jedinicu i grupu jedinica ne postaju ispravno podrazumevano za kategorije troškova u obrascima **Detalji o predmetu ugovora** i **Detalji stavke ponude**.
- Liste **Cena koštanja po jedinici za organizaciju** dozvoljavaju preklapanje efikasnosti datuma.
- Korisnicima nije dozvoljeno da menjaju **OrgUnit** kada tip porudžbine nije zasnovan na radu jer će dovesti do greške izuzetka nepostojeće reference.
- Pri pokušaju kretanja iz obrasca **Detalji stavke ponude** natrag na karticu **Ponuda**, obrazac se osvežava i prikazuje karticu **Rezime**.
