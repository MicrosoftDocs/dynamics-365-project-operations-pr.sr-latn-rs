---
title: Šta je novo ili promenjeno u izdanju 21 ispravke za Project Service Automation u verziji 3
description: U ovoj temi date su funkcije i ispravke koje su dostupne u izdanju 21 ispravke za Project Service Automation u verziji 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 799be481c365e82e8ffb59ba242e30378644008b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126725"
---
# <a name="project-service-automation-update-release-21-v3"></a>Project Service Automation izdanje ispravke 21, u verziji 3

Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x. Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

U ovoj temi date su funkcije koje su nove ili su promenjene u izdanju 21 ispravke za Project Service Automation u verziji 3. Broj izrade ove verzije je V 3.10.32.50 i uglavnom je dostupna putem samostalnog ažuriranja u junu 2020. godine.

## <a name="update-release-21"></a>Izdanje ispravke 21

### <a name="bug-fixes"></a>Ispravke grešaka

**Vreme i trošak**

Popravljeni su sledeći problemi:

- Prilikom hostovanja **Kontrole mreže stavke vremena** na kontrolnoj tabli, mreža ne koristi punu širinu kontejnera mreže kontrolne table.
- Za određene vremenske zone, kontrola mreže **Stavka vremena** ne prikazuje zapise.
- Stavke vremena koje su posle 21:00 pojavljuju se pogrešnog dana.
- Korisnici ne mogu da pošalju troškove ako kategorija troškova, **Potrebna je priznanica za troškove** nema vrednost.

**Upravljanje resursima**

Popravljeni su sledeći problemi:

- Neaktivne rezervacije se prikazuju u prikazu **Sravnjenje**.
- Nedostaje validacija generičkog resursa kako bi se osiguralo da postoji važeći status rezervacije.

**Upravljanje projektima**

Popravljeni su sledeći problemi:

- Mreže obrasca za **Projekat** (**Dodela resursa**, **Zadatak**, prikaz **Sravnjenje**, **Procene troškova**) se mogu uređivati čak i kada projekat nije aktivan.
- Duplirani klijenti se ne mogu objediniti sa klijentima koji su povezani sa potvrđenim ugovorima za projekat.
- Kada se doda resurs koji nema važeći kalendar, sistem ne vraća poruku o grešci prilagođenu korisniku.
- Dugme **Dodaj zadatak** na mreži zadataka je omogućeno kada je projekat povezan na **programski dodataka za Microsoft Project**.
- Napor nekontrolisano raste kada je zadatak sa kategorijom dodeljen resursu sa ulogom za koju je definisana cena koštanja.

**Sales**

Uneta su sledeća poboljšanja:

- **Učestalost fakturisanja** i **Početak naplate** su preseljeni na karticu **Raspored fakturisanja**.

Popravljeni su sledeći problemi:

- **Ukupna prodajna cena** je nula (0) za **Kategoriju**, mada **Uloga** ima ukupnu prodajnu cenu koja nije nula.
- Klijenti ne mogu da menjaju vrednost polja **Status fakture** na **Spremno za fakturisanje** kada neki drugi prilagođeni proces ažurira dodatno polje.
- Dugme **Osveži stavke fakture** može da kreira više dupliranih stavki ako se više puta izaberu.
- Dugme **Ažuriraj cene** ne radi na podformi **Cene uloga** u obrascu **Brzi prikaz**.
- Logika **Rešenje prodajnog cenovnika** nepravilno rukuje vremenskim zonama, što rezultira pogrešnim odabirom cenovnika.
- **Ukupni stvarni trošak** projekta se može isključiti jednim delom nakon što se odobri jedna stavka vremena.
- Logika **Rešenje cena** ne daje poruku o grešci prilagođenu korisniku ako **Vraćena cena uloge** nema vrednosti u poljima **'Primarna jedinica'** i **'Cena u osnovnoj jedinici'**.
