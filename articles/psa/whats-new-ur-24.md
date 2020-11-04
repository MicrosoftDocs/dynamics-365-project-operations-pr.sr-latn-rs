---
title: Šta je novo ili promenjeno u izdanju 24 ispravke Project Service Automation verzije 3
description: U ovoj temi date su funkcije i ispravke koje su dostupne u izdanju 24 ispravke za Project Service Automation verzije 3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6c8348e65307f63a251f97bf1ea17578e7026da8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083532"
---
# <a name="project-service-automation-update-release-24-v3"></a>Project Service Automation izdanje 24 ispravke verzije 3

Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x. Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

U ovoj temi date su funkcije i ispravke koje su nove ili promenjene u rešenju Project Service Automation u verziji 3, izdanje ispravke 24. Ova verzija ima broj V3.10.42.43 i opšte je dostupna putem samostalne ispravke objavljene oktobra 2020.

## <a name="update-release-24"></a>Izdanje ispravke 24

### <a name="bug-fixes"></a>Ispravke grešaka

**Sales**

Popravljeni su sledeći problemi:

- Problem prilikom postavljanja podrazumevanog cenovnika proizvoda.
- Performanse ostvarene ponude su spore zbog ugrađenog cenovnika i kopija zapisa cena uloga.
- **Ugovor o projektu / čvorište za prodaju** > **Stavka predmeta proizvoda / količina stavke porudžbine** automatski se zaokružuje na najbliži celi broj.
- Podignite sistemske privilegije prilikom čitanja cenovnika.
- Kopirajte polja adrese klijenta **address1_freighttermscode** i **address1_shippingmethodcode** za ponudu/porudžbinu. 


**Vreme i trošak**

Popravljeni su sledeći problemi:

- **Mreža stavke vremena** ne podržava vremensko ponašanje **Samo datum**.
- **Stavka vremena** se ne osvežava automatski. Potrebno je ručno osvežavanje.
- Nije moguće uvesti stavke vremena iz zadatka kada postoji pauza (0 sati) u dodelama resursa.
- Kada kreirate stavku vremena, podesite da početak bude isti kao **msdyn_date**.
- Ponovo omogućite grupno uređivanje za unos vremena.

**Upravljanje resursima**

Popravljeni su sledeći problemi:

- Pokušaj ažuriranja statusa jednodnevne rezervacije bez zahteva dovešće do izuzetka „null-ref“.
- Greška pri učitavanju **prikaza usaglašenosti**.


**Upravljanje projektima**

Popravljeni su sledeći problemi:

- U **Rasporedu projekta** , pri promeni iz **Ručno** u **Automatski** , automatsko čuvanje se ne dovršava.
- Troškovi troškova ne bi trebalo da se računaju prema odstupanju u odnosu na **Mreža za praćenje projekata**.
- Nedosledno ponašanje za kolone **Oznaka procene** tokom učitavanja u odnosu na promenu tipa **Vremenska faza**.
- Stvarni troškovi projekta možda neće odražavati ukupne iznose iz **stvarnih vrednosti**.
- **Predviđeni datum završetka** na kartici **Rezime** se ne podudara sa **SAP rasporedom**.
- **Ažuriranje stvarnih sati** pri izvlačenju ne radi ispravno.
- Menadžer projekta izvan osnovne **poslovne jedinice** ne može da kreira projekat.
- Promene u zadatku ili kategoriji **procena troškova** ne ostaju sačuvane.
- **Kopija ugovora** kopira rasporede faktura i status pokretanja.
- Dugme **Osveži stvarne vrednosti** pogrešno izračunava rezimirane zadatke.
- Dodatak za Microsoft Project: Ispravljena je greška reference „null“ ako bilo koji član tima ima praznu jedinicu za obezbeđivanje resursa.

