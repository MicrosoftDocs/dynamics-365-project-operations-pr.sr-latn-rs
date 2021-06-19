---
title: Troškovi i prihod projekta
description: Ova tema pruža informacije o proceni troškova i prihoda projekta.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 48f313b15f788645b88a4d878e3bece419d63126
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009183"
---
# <a name="project-costs-and-revenue"></a>Troškovi i prihod projekta

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Procene projekta pružaju finansijski prikaz za posao koji je procenjen i zakazan u rasporedu projekta. Kartica **Procene** na stranici **Projekti** prikazuje uticaj troškova i prihoda za posao koji planirate. Takođe pruža informacije o mnogim unapred definisanim dimenzijama. 

> ![Kartica sa procenama](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a>Vrednosti troškova i prodajne vrednosti projekta

Cenovnici definišu stope troškova i naplate za projekat. Možete odrediti uticaj troškova i prihoda posla, na osnovu uloga koje su povezane sa nazivom pozicije i imenovanim resursom koji je dodeljen nekom zadatku. Ako postoje zadaci koji nemaju dodele (generičke ili imenovane), ne možete dobiti procene troškova ni prodaje. Vrednosti troškova i prodaje uzimaju u obzir datum koji je definisan u cenovnicima.

### <a name="default-cost-price"></a>Podrazumevana cena koštanja  

Svaki projekat pripada organizaciji. Ova organizacija je prikazana u polju **Jedinica za ugovaranje** u okviru projekta. Cenovnik koji je povezan sa ugovornom jedinicom koristi se za utvrđivanje jedinične cene koštanja. Da biste utvrdili tačne cene koštanja za uloge i to za datum definisan u stavkama procene, pretražite kombinaciju uloge, jedinice i organizacione jedinice u cenovniku troškova. 

Da bi njihove cene koštanja mogle da se izračunaju, svi zadaci moraju biti dodeljeni resursu. Svi nedodeljeni zadaci imaće cenu koštanja od 0,00.

Ako kombinacija uloge, jedinice i organizacione jedinice ne prikazuje cenu koštanja iz cenovnika ugovorne jedinice, sistem ignoriše jedinicu. Umesto toga, traži samo kombinaciju uloge i organizacione jedinice. Ako se nađe cena koštanja, koriste se faktori konverzije da bi je konvertovali u jedinicu koju ste odabrali u stavci procene.

Ako kombinacija uloge i organizacione jedinice ne prikazuje cenu koštanja, sistem ignoriše organizacionu jedinicu. Umesto toga, traži kombinaciju uloge i jedinice da bi podesio podrazumevanu cenu (nakon što se primeni bilo koja konverzija).

Ako sistem ne pronađe cenu za ulogu, cena koštanja u stavci procene se podešava na podrazumevanu vrednost **0,00**. Svi iznosi troškova u stavkama procene troškova za projekat se evidentiraju u valuti ugovorne jedinice.

> [!NOTE]
> Podrazumevano, Microsoft Dynamics 365 skladišti iznose troškova u vašoj osnovnoj valuti. Međutim, iznosi troškova koji su prikazani na kartici **Procene** su u valuti ugovorne jedinice.  

### <a name="default-sales-price"></a>Podrazumevani prodajna cena 

Prodajni cenovnik određuje entitet prodaje uz koji je projekat priložen ili klijent projekta. Kada je entitet prodaje, kao što je mogućnost za poslovanje, ponuda ili ugovor, povezan sa projektom, prodajna cena entiteta prodaje određuje se cenovnikom koji je povezan sa ponudom ili ugovorom. Ako ponuda ili ugovor imaju prilagođeni cenovnik, on će biti podrazumevani cenovnik prodaje za procene projekta. Ako nema veze sa entitetima prodaje, podrazumevani prodajni cenovnik iz parametara koristi se kao podrazumevani prodajni cenovnik projekta koji se podudara sa valutom klijenta koja je definirana za projekat.

Svaka stavka procene ima jedinicu za resurse koja je povezana s njom. Jedinica za obezbeđivanje resursa ukazuje na organizacionu jedinicu iz koje se rezervišu resursi za završetak zadatka. Da biste odredili prodajnu cenu za povezane uloge, potražite kombinaciju uloge, jedinice i jedinice za obezbeđivanje resursa u prodajnom cenovniku. Ako nema dodela za zadatak, prodajna cena zadatka je 0,00.

Ako kombinacija uloge, jedinice i jedinice za obezbeđivanje resursa ne prikazuje prodajnu cenu iz prodajnog cenovnika, sistem ignoriše jedinicu. Umesto toga, traži samo kombinaciju uloge i jedinice za obezbeđivanje resursa. Ako se nađe prodajna cena, koriste se faktori konverzije da bi je konvertovali u jedinicu koju ste odabrali u stavci procene za prodaju. 

Ako kombinacija uloge i jedinice za obezbeđivanje resursa ne prikazuje prodajnu cenu iz prodajnog cenovnika, sistem ignoriše jedinicu za obezbeđivanje resursa. Umesto toga, traži kombinaciju uloge i jedinice da bi podesio podrazumevanu cenu (nakon što se primeni bilo koja konverzija).

Ako sistem ne pronađe cenu za ulogu, prodajna cena u stavci procene se podešava na podrazumevanu vrednost **0,00**.

Kartica **Procene** ima prikaz mreže koji prikazuje stavke procene. Mreža sadrži kolone za jedinicu, ukupnu cenu koštanja i ukupnu prodajnu cenu, kao što je prikazano na sledećoj ilustraciji. 

> ![Prikaz mreže na kartici Procene](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a>Prikaz procena za projekat u vremenu

Prikaz po fazama vremena za projektne procena prikazuje podatke o proceni iz prikaza mreže po vremenskoj osi, u vremenskoj skali koju odaberete. Podaci o proceni su podrazumevano izvedeni u dimenziji **Uloga**.

> ![Prikaz procena za projekat po fazama vremena](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a>Dodela procenjenih aktivnosti na osnovu režima zadatka

U prikazu po fazama vremena, ukupne procenjene aktivnosti za zadatak distribuirate dodeljivanjem broja sati za aktivnosti po jedinici perioda vremena u odabranoj skali vremena. Režim zadatka određuje način dodeljivanja aktivnosti tokom trajanja zadatka. Dve vrste dodele su **Ravnomerna** i **Na osnovu radnog vremena**.

### <a name="work-hours-based-allocation"></a>Dodela na osnovu radnog vremena
 
U režimu zadatka sa automatskim zakazivanjem, dnevni podrazumevani sati za resurse zadatka podešavaju se na punu stopu radnog sata. Ovo ponašanje se primenjuje i kada se aktivnosti dodeljuju podelom po trajanju zadataka u prikazu po fazama vremena. Na primer, ako na vremenskoj skali po **danu** procenite da će zadatak dovršiti jedan resurs, aktivnosti dodeljene po danu neće premašiti radno vreme po danu definisano u kalendaru projekta. Stoga, dodela aktivnosti uvek osigurava da se proceni korišćenje resursa tokom celog dana.

### <a name="even-allocation"></a>Ravnomerna dodela

U režimu ručno zakazanih zadataka, radni sati iz kalendara projekta se ne koriste. Umesto toga, raspored zadatka je zasnovan na unosu korisnika. Za ove zadatke, dodela aktivnosti po jedinici vremenskog perioda u odabranoj vremenskoj skali nema ograničavajuće faktore. Ukupne aktivnosti na zadatku se ravnomerno dele i dodeljuje za svaku jedinicu vremenskog perioda u odabranoj skali vremena. Zato režim zadataka definisan u zadatku određuje distribuciju ili dodelu aktivnosti po jedinici vremenskog perioda u procenama po vremenskim fazama.

## <a name="grouping-and-time-phasing-options"></a>Opcije grupisanja i prikazivanja u vremenu

Prikaz po fazama vremena pokazuje distribuciju procena aktivnosti, troškova i prodaje na dnevnom, sedmičnom, mesečnom ili godišnjem nivou. Podaci o proceni su podrazumevano izvedeni u dimenziji **Uloga**. Međutim, možete koristiti opciju **Grupiši prema** da biste izveli vrednosti za druge dve dimenzije: **Kategorija** i **Resurs**.

U prikazu mreže i prikazu po fazama vremena možete da izaberete koja će se polja prikazivati. Ukupne vrednosti za svaki vremenski blok prikazuju se na dnu projekta. Oni pokazuju ukupne procenjene aktivnosti, troškove i prodaju za dan, nedelju, mesec ili godinu. Podrazumevana cena koštanja i prodajna cena stupaju na snagu određenog datuma. Drugim rečima, oni se menjaju za svaki resurs, na osnovu prikaza po fazama vremena koji odaberete.

## <a name="expense-estimates"></a>Procene troškova

Dugme **Dodajte novu procenu troškova** u prikazu mreže omogućava vam da evidentirate sve troškove koji nastaju u projektu, ali koji nisu direktno povezani sa radnom snagom. Možete zabeležiti procene troškova za određeni zadatak ili za ceo projekat. Odaberite kategorije troškova i okvirni datum kada očekujete da nastanu. Ako povezani cenovnik troškova i cenovnik prodaje imaju podrazumevane cene (ili ako su procenti provizije definisani za kategorije troškova), oni se automatski unose u stavku procene kada dođe do povezivanja.


[!INCLUDE[footer-include](../includes/footer-banner.md)]