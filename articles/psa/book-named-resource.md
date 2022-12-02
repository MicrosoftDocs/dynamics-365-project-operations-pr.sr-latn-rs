---
title: Rezervisanje imenovanih resursa iz potrebe za resursima
description: Ovaj članak pruža informacije o rezervisanju imenovanih resursa u skladu sa potrebama za generičkim resursima.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 9598490da1905227e517da8ba90f8ffd1df88566
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916259"
---
# <a name="book-named-resources-from-resource-requirements"></a>Rezervisanje imenovanih resursa iz potrebe za resursima

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Možete rezervisati imenovani resurs da biste zamenili generički resurs za kojim postoji potreba.

1. U aplikaciji Project Service Automation (PSA), na stranici **Projekti** kliknite na karticu **Tim**.
2. Sa liste izaberite generički resurs za kojim postoji potreba, a zatim kliknite na **Rezerviši**. Ili otvorite potrebu za resursom, a zatim kliknite na **Rezerviši**.


![Rezervisanje generičkog člana tima.](media/RM-how-to-14.png)


3. Na stranici **Pomoćnik za zakazivanje** izaberite imenovani resurs koji ćete rezervisati za projektni tim, a zatim kliknite na **Rezerviši**.

![Rezervisanje generičkog člana tima pomoću pomoćnika za zakazivanje.](media/RM-how-to-15.png)

Kada se rezervacija dovrši i ispuni je imenovani resurs, generički resurs se zamenjuje imenovanim resursom.

![Imenovani član tima koji zamenjuje generičkog člana tima.](media/RM-how-to-16.png)

Dodele u rasporedu se ažuriraju i imenovanim resursom.

![Imenovani član tima dodeljen projektnim zadacima.](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Popunjavanje generičkog resursa većim brojem imenovanih resursa
Ispunjavanje zahteva za generički resurs sa više imenovanih resursa je slično dodeljivanju jednog imenovanog resursa. Na primer, postoji zadatak sa trajanjem od pet dana i 120 sati truda. Ovaj zadatak ne može da dovrši jedan resurs koji radi sa tipičnim osmočasovnim radnim danom u sedmici od pet radnih dana. 

![Zadatak koji treba 120 sati truda tokom perioda od pet dana.](media/RM-how-to-21.png)

Zahtev je za 120 sati inženjeringa robotike u toku pet dana, što je 24 časa dnevno.

![Zahtev po danu.](media/RM-how-to-22.png)

Ovo je primer kada je potrebno više imenovanih resursa za ispunjavanje generičkog zahteva za resurse. Biće potrebno da rezervišete više resursa da biste ispunili taj zahtev.

![Rezervisanje više resursa radi ispunjavanja zahteva.](media/RM-how-to-23.png)

Glavna razlika u ovom scenariju je to što generički resurs ostaje u timu koji je dodeljen zadatku, a rezervisani imenovani članovi tima resursa nisu dodeljeni kao deo pozicije. Menadžer projekta može po potrebi da dodeli posao imenovanim resursima. Prikaz **Usaglašenost** može da pomogne menadžeru projekta da podeli rezervacije više resursa na zadatke za dodeljivanje. Ovo se ne radi automatski jer u svakom scenariju komplikovanijem od običnog primera datog iznad, na primer kada imate skup zadataka koji sačinjavaju zahtev, sistem mora da pretpostavi kako menadžer projekta namerava da dodeli resurse. Pošto sistem ne može da razume nameru, postoje šanse da će se pretpostavke razlikovati od predviđenih, pa će doći do netačnog ili nepredvidivog rezultata. Predvidiv ishod je da generički resurs ostaje dodeljen dok menadžer projekta namerno ne kreira dodele, uz pomoć prikaza **Usaglašenost**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
