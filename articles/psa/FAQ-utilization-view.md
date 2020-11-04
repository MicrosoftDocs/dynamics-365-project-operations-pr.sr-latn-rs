---
title: Prikaz naplative ukupne iskorišćenosti resursa
description: Ova tema pruža informacije o prikazu ukupne iskorišćenosti resursa.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 6daa6cfa1c6a237d8a1685123f7c1a6926418bfe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083602"
---
# <a name="view-chargeable-utilization-for-resources"></a>Prikaz naplative ukupne iskorišćenosti resursa
 
**Prikaz ukupne iskorišćenosti** na stranici **Ukupna iskorišćenost resursa u aplikaciji Project Service** prikazuje naplativu ukupnu iskorišćenost svakog resursa koji može da se rezerviše. Pošto je prikaz zasnovan na tabeli rasporeda, pronaćićete dosta istih funkcija.

> ![Snimak ekrana prikaza ukupne iskorišćenosti](media/FAQ-utilization-1.png)
 

Izračunavanje naplative ukupne iskorišćenosti funkcioniše na sledeći način:

   Naplativa ukupna iskorišćenost = (naplativi stvarni sati) / (kapacitet resursa).

Ćelije predstavljaju izračunatu naplativu ukupnu iskorišćenost za izabrani period (dani, sedmice ili meseci).

Boje u svakoj ćeliji prikazuju naplativu ukupnu iskorišćenost za resurs u poređenju sa njegovom ciljnom naplativom ukupnom iskorišćenošću. 

Ciljna ukupna iskorišćenost može biti podešena za podrazumevanu ulogu resursa ili za samog pojedinačnog resursa. Izračunavanje prvo gleda pojedinca za cilj, a zatim podrazumevanu ulogu resursa.

## <a name="set-target-on-a-resource"></a>Podešavanje cilja za resurs

1. Idite na **Resursi** \> **Resursi**. 
2. Izaberite resurs da biste otvorili zapis. 
3. Na kartici **Project Service** možete podesiti ciljnu ukupnu iskorišćenost resursa.

> ![Snimak ekrana korišćenja kartice Project Service za podešavanje ciljne ukupne iskorišćenosti](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>Podešavanje ciljne ukupne iskorišćenosti za ulogu

1. Idite na **Resursi** \> **Uloge resursa**. 
2. Izaberite ulogu i otvorite zapis. 
3. Podesite ciljnu ukupnu iskorišćenost za ulogu.

> ![Snimak ekrana korišćenja uloga resursa za podešavanje ciljne ukupne iskorišćenosti](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>Izračunavanje naplative ukupne iskorišćenosti resursa

Da biste izračunali naplativu ukupnu iskorišćenost za resurs, potrebno je da ispunite neke preduslove. 

### <a name="set-default-role-for-individual-resource"></a>Podešavanje podrazumevane uloge za pojedinačni resurs

Prvo, ciljna ukupna iskorišćenost mora biti podešena za ulogu pojedinačnog resursa ili za ulogu resursa. Ako koristite uloge resursa za ciljeve, svaki pojedinačni resurs mora da ima podrazumevanu ulogu. 

1. Da biste to podesili, idite na stavku **Resursi** \> **Resursi**. 
2. Izaberite resurs, otvorite zapis, a zatim izaberite karticu **Project Service**. 
3. U mreži **Uloga resursa** , uverite se da postoji jedna uloga za resurs, a **Je podrazumevano** podešeno na **Da**.
 
### <a name="change-billing-type-for-resource-role"></a>Promena tipa naplate za ulogu resursa

Uloge resursa moraju biti podešene tako da imaju tip naplate **Naplativ**. 

1. Idite na **Resursi** \> **Uloge resursa**. 
2. Otvorite zapis koji želite da ažurirate, a zatim podesite podrazumevani tip naplate na **Naplativo**.

### <a name="set-working-hours-for-resource-role"></a>Podešavanje radnog vremena za ulogu resursa
 
Resurs mora da ima radno vreme za izračunavanje kapaciteta. 

1. Idite na **Resursi** \> **Resursi**. 
2. Izaberite resurs da biste otvorili zapis, a zatim izaberite **Prikaži radno vreme**. 
3. Možete masovno da ispravite listu resursa primenom **predloška za radno vreme** sa prikaza **liste resursa**.

## <a name="troubleshooting-chargeable-actual-hours"></a>Rešavanje problema sa naplativim stvarnim satima

Izvor naplativih stvarnih sati je entitet **Stvarne vrednosti**. Stvarne vrednosti čiji je tip naplate **Naplativo** su obuhvaćene u izračunavanje i zato morate da imate projekte u kojima su stvarne vrednosti naplative.

Ako ne vidite naplativu ukupnu iskorišćenost, evo nekih stvari koje možete da proverite:

- Resurs ima radne časove koji su definisani za kapacitet.
- Resurs ima pojedinačno definisani cilj ukupne iskorišćenosti ili mu je dodeljena podrazumevana uloga. Za ulogu je definisan cilj ukupne iskorišćenosti.
- Stvarne vrednosti imaju tip naplate **Naplativo** za period za koji očekujete izračunavanje ukupne iskorišćenosti. Proverite sledeće stvari ako vidite stvarne vrednosti čiji tipovi naplate nisu naplativi:

  - Uloga korišćena za stvarne troškove ima podrazumevani tip naplate koji se razlikuje od tipa „Naplativo“.
  - Uloge za predmet ugovora za projekat koji podržava projekat je podešena na nenaplativo.
  - Projekat nema povezani predmet ugovora.

