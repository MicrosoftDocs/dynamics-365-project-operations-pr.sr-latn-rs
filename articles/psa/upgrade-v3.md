---
title: Činjenice koje treba uzeti u obzir prilikom nadogradnje – Microsoft Dynamics 365 Project Service Automation verzije 2.x ili 1.x na verziju 3.x
description: Ova tema pruža informacije o činjenicama koje morate uzeti u obzir prilikom nadogradnje aplikacije Project Service Automation sa verzije 2.x ili 1.x na verziju 3.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3c51726f71cfd0d4be98982d6a02268d64a70b91
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121730"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>Činjenice koje treba uzeti u obzir prilikom nadogradnje - PSA verzije 2.x ili 1.x na verziju 3.x
[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>Project Service Automation i Field Service
I Dynamics 365 Project Service Automation i Dynamics 365 Field Service koriste Universal Resourcing Scheduling (URS) rešenje za planiranje resursa. Ako u vašoj instanci imate i Project Service Automation i Field Service, trebalo bi da planirate nadogradnju oba rešenja na najnoviju verziju (verziju 3.x za Project Service Automation, verziju 8.x za Field Service). Nadogradnjom aplikacije Project Service Automation ili Field Service ćete instalirati najnoviju verziju rešenja URS, što znači da je neusaglašeno ponašanje moguće ako se i Project Service Automation i Field Service rešenje u istoj instanci ne nadograde na najnoviju verziju.

## <a name="resource-assignments"></a>Dodele resursa
U aplikaciji Project Service Automation verzije 2 i 1, dodeljivanja zadataka su skladištena kao podređeni zadaci (takođe poznati kao zadaci stavke) u **entitetu zadatka** i bili su indirektno povezani sa entitetom **Dodela resursa**. Zadatak stavke je bio vidljiv u iskačućem prozoru za dodelu u okviru strukturne analiza posla (SAP).

![Zadaci stavke u SAP-u u rešenju Project Service Automation u verziji 2 i verziji 1](media/upgrade-line-task-01.png)

U verziji 3 aplikacije Project Service Automation, osnovna šema dodeljivanja resursa koji se mogu rezervisati zadacima je promenjena. Zadatak stavke je zastareo i postoji direktni 1:1 odnos između zadatka u **entitetu zadatka** i člana tima u entitetu **Dodela resursa**. Zadaci koji su dodeljeni članu projektnog tima sada se skladište direktno u entitetu Dodela resursa.  

Ove promene utiču na nadogradnju svih postojećih projekata koji imaju dodele resursa za imenovane resurse koji se mogu rezervisati i generičke resurse u timu projekta. Ova tema obezbeđuje činjenice koje treba uzeti u obzir za projekte prilikom nadogradnje na verziju 3. 

### <a name="tasks-assigned-to-named-resources"></a>Zadaci su dodeljeni imenovanim resursima
Ako koristite osnovni entitet zadatka, zadaci u verziji 2 i 1 dozvoljavaju članovima tima da prikazuju ulogu koja nije njihova podrazumevana definisana uloga. Na primer, Dunja Nikolić, kojoj je podrazumevano dodeljena uloga menadžera programima, može biti dodeljen zadatku sa ulogom programera. U verziji 3, uloga imenovanog člana tima je uvek podrazumevana, tako da svaki zadatak koji je dodeljen Dunji Nikolić koristi njenu podrazumevanu ulogu menadžera programa.

Ako ste dodelili resurs zadatku van njegove podrazumevane uloge u verziji 2 i 1, kada izvršite nadogradnju, imenovanom resursu će biti dodeljena podrazumevana uloga za sve dodele zadataka, bez obzira na dodelu uloge u verziji 2. Ovo će dovesti do razlika u izračunatim procenama u verziji 2 ili 1 u odnosu na verziju 3 zato što se procene izračunavaju na osnovu uloge resursa, a ne dodele zadatka stavke. Na primer, u verziji 2, dva zadatka je dodeljeno Pavlu Kneževiću. Uloga u zadatku stavke za 1. zadatak je programer, a za 2. zadatak menadžer programa. Pavle Knežević ima podrazumevanu ulogu menadžera programa.

![Više uloga je dodeljeno jednom resursu](media/upgrade-multiple-roles-02.png)

S obzirom na to da se uloge programera i menadžera programa razlikuju, procene troškova i prodaje su sledeće:

![Procene troškova za uloge resursa](media/upggrade-cost-estimates-03.png)

![Procene prodaje za uloge resursa](media/upgrade-sales-estimates-04.png)

Kada izvršite nadogradnju na verziju 3, zadaci stavke se zamenjuju dodelama resursa u zadatku člana tima resursa koji se može rezervisati. Dodela će koristiti podrazumevanu ulogu resursa koji se može rezervisati. Na sledećem grafikonu, Pavle Knežević koji ima ulogu menadžera programa, jeste resurs.

![Dodele resursa](media/resource-assignment-v2-05.png)

Pošto su procene zasnovane na podrazumevanoj ulozi za resurs, mogu se promeniti procene prodaje i troškova. Imajte na umu da na sledećem grafikonu više nećete videti ulogu **Programer** jer je sada uzeta iz podrazumevane uloge resursa koji može da se rezerviše.

![Procena troškova za podrazumevane uloge](media/resource-assignment-cost-estimate-06.png)
![Procena troškova za podrazumevane uloge](media/resource-assignment-sales-estimate-07.png)

Nakon nadogradnje, možete da uredite ulogu člana tima tako da bude nešto drugo od dodeljene podrazumevane uloge. Međutim, ako promenite ulogu člana tima, ona će biti promenjena u svim dodeljenim zadacima zato što članovima tima više nije dozvoljeno dodeljivati više uloga u verziji 3.

![Ažuriranje uloge resursa](media/resource-role-assignment-08.png)

Ovo važi i za zadatke stavke koji su bili dodeljeni imenovanim resursima kada promenite organizacionu jedinicu resursa od podrazumevane vrednosti u drugu organizacionu jedinicu. Kada se završi nadogradnja na verziju 3, dodela će koristiti podrazumevanu organizacionu jedinicu resursa umesto one koja je podešena u zadatku stavke.

### <a name="tasks-assigned-to-generic-resources"></a>Zadatak je dodeljen generičkim resursima
U verziji 2 i 1, možete da podesite ulogu i organizacionu jedinicu za zadatak, a zatim da koristite funkciju **Generiši tim** da biste generisali generičke resurse na osnovu atributa koji su podešeni za zadatak. U verziji 3 možete kreirati generičke članove sa ulogom i organizacionom jedinicom, a zatim dodeliti članove tima zadacima.

U verziji 2 i 1, projekti sa generičkim resursima mogu da imaju dva statusa ili njihovu kombinaciju na nivou zadatka. Na primer, možete da imate sledeće scenarije:

- Zadaci sa podešenim ulogama i skupom organizacionih jedinica, ali bez povezane dodele resursa su generisani.
- Zadaci sa dodelama generičkih članova tima koji su dodeljeni kreiranjem generičkog resursa pomoću funkcije **Generiši tim**.

Pre nego što započnete nadogradnju, preporučujemo da ponovo generišete tim za svaki projekat koji ima zadatke dodeljene generičkim resursima ili za koje tek treba da se pokrene proces generičkog tima.

Za zadatke koji su dodeljeni generičkim članovima tima koji su generisani pomoću funkcije **Generiši tim**, nadogradnja će ostaviti generički resurs u timu i ostaviće dodelu tom generičkom članu tima. Preporučujemo da nakon nadogradnje generišete potrebu za resursom za generičkog člana tima, ali pre nego što rezervišete ili prosledite zahtev za resurs. To će sačuvati sve dodele organizacione jedinice za generičke članove tima koji se razlikuju od ugovorne organizacione jedinice projekta.

Na primer, u projektu Š, ugovorna organizaciona jedinica je Contoso US. U projektnom planu, zadaci testiranja u fazi implementacije su dodeljeni ulozi Tehnički konsultant, a dodeljena organizaciona jedinica je Contoso India.

![Dodela organizacije u fazi implementacije](media/org-unit-assignment-09.png)

Nakon faze implementacije, zadatak testiranja integracije se dodeljuje ulozi Tehnički konsultant, ali se organizacija podešava na Contoso US.  

![Dodela zadatka testiranja integracije u organizaciji](media/org-unit-generate-team-10.png)

Kada generišete tim za projekat, dva generička člana tima se kreiraju zbog različitih organizacionih jedinica za zadatak. 1. tehnički konsultant biće dodeljen zadacima kompanije Contoso India, a 2. tehnički konsultant će imati zadatke kompanije Contoso US.  

![Generički članovi tima su generisani](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> U aplikaciji Project Service Automation u verzijama 2 i 1, član tima ne održava organizacionu jedinicu, koja se održava u zadatku stavke.

![Zadaci stavke za verziju 2 i verziju 1 u rešenju Project Service Automation](media/line-tasks-12.png)

Organizacionu jedinicu možete videti u prikazu predviđanja. 

![Procene organizacionih jedinica](media/org-unit-estimates-view-13.png)
 
Kada se nadogradnja dovrši, organizaciona jedinica u zadatku stavke koja odgovara generičkom članu tima dodaje se tom članu, a zadatak stavke će biti uklonjen. Zbog ovoga preporučujemo da pre nadogradnje generišete ili ponovo generišete tim za svaki projekat koji sadrži generičke resurse.

Za zadatke koji su dodeljeni ulozi sa organizacionom jedinicom koja se razlikuje od organizacione jedinice projekta za ugovaranje, a tim nije generisan, nadogradnja će kreirati generičkog člana tima za ulogu, ali će koristiti ugovornu jedinicu projekta za organizacionu jedinicu člana tima. Ako se vratimo na primer projekta Š, to znači da je ugovorna organizaciona jedinica Contoso US i da su zadaci testiranja projektnog plana u okviru faze implementacije dodeljeni ulozi Tehnički konsultant, a da je organizaciona jedinica dodeljena kompaniji Contoso India. Zadatak testiranja integracije, koji je dovršen nakon faze implementacije, dodeljen je ulozi Tehnički konsultant. Organizaciona jedinica Contoso US i tim nisu generisani. Nadogradnja će kreirati jednog generičkog člana tima, tehničkog konsultanta koji ima dodeljene sate za sva tri zadatka, kao i organizacionu jedinicu Contoso US, ugovornu organizacionu jedinicu projekta.   
 
Promena podrazumevanih vrednosti različitih organizacionih jedinica za obezbeđivanje resursa za članove tima koji nisu generisani je razlog zbog kojeg preporučujemo da pre nadogradnje generišete ili ponovo generišete tim za svaki projekat koji sadrži generičke resurse, kako se dodele organizacionih jedinica ne bi izgubile.
