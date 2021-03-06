---
title: Ispunjavanje generičkih zahteva za resursima
description: Ova tema pruža informacije o rezervisanju imenovanih resursa u skladu sa potrebama za generičkim resursima.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 76dd47fa2451b5cb61298ff332d77bae646a288a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897603"
---
# <a name="generic-resource-requirement-fulfillment"></a>Ispunjavanje generičkih zahteva za resursima

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Možete rezervisati imenovani resurs da biste zamenili generički resurs za kojim postoji potreba.

1. Na stranici **Projekti**, izaberite karticu **Tim**.
2. Na listi izaberite generički resurs za kojim postoji potreba, a zatim izaberite **Rezerviši**. Ili otvorite potrebu za resursom, a zatim izaberite **Rezerviši**.
3. Na stranici **Pomoćnik za zakazivanje** izaberite imenovani resurs koji ćete rezervisati za projektni tim, a zatim izaberite **Rezerviši**.

Kada se rezervacija dovrši i ispuni je imenovani resurs, generički resurs se zamenjuje imenovanim resursom.

Dodele u rasporedu se ažuriraju i imenovanim resursom.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Popunjavanje generičkog resursa većim brojem imenovanih resursa
Ispunjavanje zahteva za generički resurs sa više imenovanih resursa je slično dodeljivanju jednog imenovanog resursa. Na primer, postoji zadatak sa trajanjem od pet dana i 120 sati truda. Ovaj zadatak ne može da dovrši jedan resurs koji radi sa tipičnim osmočasovnim radnim danom u sedmici od pet radnih dana. 

Zahtev je za 120 sati inženjeringa robotike u toku pet dana, što je 24 časa dnevno.

Ovo je primer kada je potrebno više imenovanih resursa za ispunjavanje generičkog zahteva za resurse. Biće potrebno da rezervišete više resursa da biste ispunili taj zahtev.

Glavna razlika u ovom scenariju je to što generički resurs ostaje u timu koji je dodeljen zadatku, a rezervisani imenovani članovi tima resursa nisu dodeljeni kao deo pozicije. Menadžer projekta može po potrebi da dodeli posao imenovanim resursima. Prikaz **Usaglašenost** može da pomogne menadžeru projekta da podeli rezervacije više resursa na zadatke za dodeljivanje. Ovo se ne radi automatski jer u svakom scenariju komplikovanijem od običnog primera datog iznad, na primer kada imate skup zadataka koji sačinjavaju zahtev ili kada sistem mora da pretpostavi kako menadžer projekta namerava da dodeli resurse. Pošto sistem ne može da razume nameru, pretpostavke će se verovatno razlikovati od predviđenih, pa će doći do netačnog ili nepredvidivog rezultata. Predvidiv ishod je da generički resurs ostaje dodeljen dok menadžer projekta namerno ne kreira dodele, uz pomoć prikaza **Usaglašenost**.


