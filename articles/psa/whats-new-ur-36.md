---
title: Šta je novo ili promenjeno u izdanju 36 ispravke Project Service Automation verzije 3
description: U ovoj temi navedene su funkcije i ispravke koje su dostupne u izdanju 36 ispravke usluge Microsoft Dynamics 365 Project Service Automation verzije 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
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
ms.openlocfilehash: 108c75598dc7dd3dd0cdb9ce68e30423d051a4cf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586683"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Šta je novo ili promenjeno u izdanju 36 ispravke Project Service Automation verzije 3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da najavimo najnoviju ispravku za aplikaciju Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Kompatibilna je sa sistemom Dynamics 365 9.x. Da biste se ažurirali na ovo izdanje, posetite stranicu centra administracije za Dynamics 365 mrežna rešenja i instalirajte ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).

U ovoj temi navedene su funkcije koje su nove ili su promenjene u rešenju Project Service Automation u verziji 3, izdanje ispravke 36. Ova verzija ima broj verzije V3.10.57.152 i opšte je dostupna putem samo-ispravke u oktobru 2021. godine.

## <a name="update-release-36"></a>Izdanje ispravke 36

### <a name="bug-fixes"></a>Ispravke grešaka

Popravljeni su sledeći problemi.

**Opšte**
- Naziv polja **Podrazumevani predložak radnih časova** pogrešno je preveden na stranici **Parametri projekta**.
- Dodatne komponente za asinhronizaciju ne upravljaju ispravno sa izuzecima vezanim za **SharedVariableService**.

**Vreme i trošak**
- Kada stavke u glavnoj knjizi nedostaju ili korisnik nema odgovarajuće privilegije za čitanje stavki u glavnoj knjizi, dolazi do greške pri otkazivanju odobrenja projekta.
- Korisnici ne mogu da otkažu odobrenje ako stavka troškova ili vremena ima više od jednog pridruženog odobrenja projekta.
- **Odsustvo** i **Godišnji odmor** su pogrešno prevedeni za kineski jezik u pretrazi na stranici za brzo kreiranje **Stavka vremena**.

**Upravljanje resursima**
- Korisnik ne može tražiti resurse u **Pomoćniku za zakazivanje** kada je režim prikaza podešen na **Dan**, **Nedelja** ili **Mesec**.
- Generičkim resursima je pogrešno dozvoljeno da imaju prazna imena radnih mesta. 
- Zatvaranje ugovora kao neostvarenog ne otkazuje buduće rezervacije.

**Prodaja**
- Kada okruženje ima veliku količinu proizvoda, performanse se smanjuju u tabeli **Procena materijala**.
- Prilikom kreiranja projekta iz predloška, valuta projekta nije podrazumevana za odgovarajuću ugovornu jedinicu odgovarajućeg vođe projekta.
- Stvarni iznosi ne odgovaraju uvek onome što se se nalazi u dospelom projektu, ili iznosi postaju negativni u specifičnim scenarijima opoziva.
- Do greške dolazi kada projekat koji ste kreirali iz predloška projekta povežete sa predmetom ugovora.
- Korisnici mogu da obrišu predmet ugovora sa kontrolnim tačkama, **Spremno za fakturisanje** i **Faktura je napravljena**. Ovo ne bi trebalo dozvoliti.
- Kada se procene uvezu iz projekta, mogućnost naplate detalja stavke ponude je pogrešno podešena kada je za stavku ponude omogućena naplata zasnovana na zadacima.
- Kada dodate kontrolnu tačku u naplati po fiksnoj ceni, ta kontrolna tačka se ne odražava u podmreži kontrolnih tačaka sve dok se stranica ne osveži.
- Izuzetak nulte reference generiše se kada kreirate ugovor o projektu sa nazivom ponude koji je bez vrednosti.
- Zadaci u ručnom režimu u kojima se valuta projekta razlikuje od valute izvora dovode do pogrešnih procena cene.
- Korisnici ne mogu da se sete transakcije koja je uspešno ispravljena korektivnom fakturom.
- Deaktivirane kategorije transakcija pojavljuju se u mreži **Procene troškova**.



