---
title: Šta je novo ili promenjeno u izdanju 18 ispravke za Project Service Automation verzije 3
description: U ovom članku date su funkcije i ispravke koje su dostupne u izdanju 18 ispravke za Project Service Automation verzije 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: e8d423c550d9aa09c9cbb7d4f7c277c43bbe10ae
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918881"
---
# <a name="project-service-automation-update-release-18-v3"></a>Project Service Automation izdanje ispravke 18, u verziji 3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x. Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).

U ovom članku date su funkcije koje su nove ili su promenjene u rešenju Project Service Automation u verziji 3, izdanje ispravke 18. Broj izrade ove verzije je V3.10.8.12 i uglavnom je dostupna putem samostalnog ažuriranja u aprilu 2020. godine.

## <a name="update-release-18"></a>Izdanje ispravke 18

### <a name="bug-fixes"></a>Ispravke grešaka

**Vreme i trošak**

- Popravljeno: tokovi **Opoziv**, **Zahtev** i **Otkaži odobrenje** izbacuju izuzetke sa nejasnim porukama o greškama.
- Popravljeno: Kada **Otkaži odobrenje** ne uspe za trošak, ne izbacuje se relevantna greška izuzetka.
- Popravljeno: Mreža stavke vremena pogrešno obrađuje neradne dane u Australiji nakon prebacivanja letnjeg vremena (DST) u oktobru.
- Popravljeno: Nepravilna logika podrazumevanih vrednosti sprečava podnošenje troškova.
- Popravljeno: Kada odobrenje stavke vremena ne uspe, odobrenje ostaje u statusu **Na čekanju**.
- Popravljeno: SQL greške pri masovnim odobrenjima (zastoj / istek vremena).
- Popravljeno: Značajni problemi sa performansama u korisničkom iskustvu izazvani ažuriranjem članova tima prilikom odobravanja unosa vremena.

**Upravljanje projektima**

- Popravljeno: Obaveštenje o vremenskoj zoni premešteno je sa prikaza **Sravnjenje** na glavni obrazac **Projekat**.
- Popravljeno: Predložak kalendara nema ispravne podrazumevane vrednosti kada se otvori novi obrazac projekta.
- Popravljeno: Za Chromium pregledače, korisnici ne mogu lako da izaberu prethodne zadatke koje će izbrisati.
- Popravljeno: Kreiranje ili kopiranje **projekta iz praznog predloška** preuzima nepovezane dodele.
- Popravljeno: U specifičnim rubnim slučajevima, kreiranje novog zadatka iz mreže zadataka dovodi do stvaranja duplikata zapisa.
- Popravljeno: U ručnom režimu korisnici ne mogu da ažuriraju datume početka zadatka da budu kasniji od sačuvanog trenutnog datuma.

**Upravljanje resursima**

- Popravljeno: Red podzbira u prikazu **Sravnjenje** pogrešno izračunava odstupanje rezervacija nakon produženja rezervacije.
- Popravljeno: Prikaz **Sravnjenje** pogrešno prikazuje dodeljene resurse kada resurs koji je moguće rezervisati ima kalendar koji se ne podudara sa kalendarom projekta.

**Sales**

- Popravljeno: Kada se stavke vremena ponovo odobre (**Odobri > Otkaži >** Ponovo odobri), kreira se duplikat nenaplative stvarne vrednosti.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
