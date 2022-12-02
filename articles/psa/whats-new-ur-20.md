---
title: Šta je novo ili promenjeno u Project Service Automation izdanju ispravke 20 u verziji 3
description: U ovom članku date su funkcije i ispravke koje su dostupne u Project Service Automation izdanju ispravke 20 u verziji 3
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 7265f4999ee9c584450efcf444621c00acd65920
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913085"
---
# <a name="project-service-automation-update-release-20-v3"></a>Project Service Automation izdanje ispravke 20, u verziji 3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x. Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).

U ovom članku date su funkcije koje su nove ili su promenjene u rešenju Project Service Automation u verziji 3, izdanje ispravke 20. Broj izrade ove verzije je V 3.10.31.37 i uglavnom je dostupna putem samostalnog ažuriranja u junu 2020. godine.

## <a name="update-release-20"></a>Izdanje ispravke 20

### <a name="bug-fixes"></a>Ispravke grešaka

**Upravljanje projektima**

Popravljeni su sledeći problemi:

- Uvoz članova projektnog tima metodom raspodele koja zahteva sate rezultira nejasnom porukom o grešci kada su navedeni sati nula.
- Korisnici dobijaju pogrešnu grešku kada je u polje **Opis** unet maksimalan broj znakova za projektni zadatak.
- Stranica **preuzimanja Microsoft Dynamics 365 Project Service Automation programskog dodatka** preusmerava se na stranicu za preuzimanje na engleskom kada su podešavanja jezika korisnika postavljena na japanski.
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
