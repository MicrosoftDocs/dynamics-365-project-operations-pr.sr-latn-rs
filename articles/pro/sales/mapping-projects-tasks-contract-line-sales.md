---
title: Mapiranje projekata i zadataka na predmet ugovora zasnovan na projektu – jednostavno
description: Ova tema pruža informacije o dodavanju i uklanjanju projekata i zadataka u predmet ugovora.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ce99e6f770c5eb39e5f2740a861721cf3d210ac9743bbd9d2a1e1a7236f368c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989748"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line"></a>Mapiranje projekata i zadataka na predmet ugovora zasnovanog na projektu 

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture, Project Operations za scenarije zasnovane na resursima / bez zaliha_

U predmetima ugovora zasnovanim na projektu, možete mapirati određene zadatke u projektu na predmet ugovora.

Kada mapirate određene zadatke na predmet ugovora, način naplate, opcije naplativosti, ograničenja koja se ne prelaze i klijenti definisani na predmetu ugovora biće primenljivi samo na te određene zadatke.

Ako imate scenario u kojem je jedna faza projekta, na primer faza prototipa, fiksna cena, a sve ostale faze su vreme i materijal, moći ćete da pridružite fazu prototipa i sve povezane podređene zadatke predmetu ugovora za tu fazu metodom obračuna sa fiksnom cenom.

Sve ostale faze u strukturnoj analizi posla na projektu (SAP) mogu se povezati sa predmetom ugovora zasnovanom na vremenu i materijalu.

## <a name="associate-tasks-to-project-based-contract-lines"></a>Povezivanje zadataka sa predmetima ugovora zasnovanim na projektu

Zadaci se mogu povezati sa predmetima ugovora sa kartice **Naplativi zadaci** na stranici **Predmet ugovora** ili sa kartice **Obračun zadataka** na stranici **Projekat**.

### <a name="from-the-contract-line-page"></a>Sa stranice Predmet ugovora

Dovršite sledeće korake za pridruživanje projektnih zadataka predmetu ugovora sa kartice **Naplativi zadaci** na stranici **Predmet ugovora**.

1. Na kartici **Opšti podaci** predmeta ugovora zasnovanog na projektu, proverite da li je polje **Projekat** popunjeno.
2. U polju **Uključeni zadaci** izaberite polje **Samo izabrani zadaci**.
3. Sačuvajte promene. Obrazac će se osvežiti i kartica **Naplativi zadaci** će biti vidljiva.
4. Izaberite karticu **Naplativi zadaci** i u podformi izaberite **Dodaj zadatak iz predmeta ugovora**.
5. Na stranici **Zadaci iz predmeta ugovora**, u padajućoj listi **Zadaci**, izaberite zadatak. 
6. Unesite informacije u polje **Vrsta obračuna**, a zatim izaberite **Sačuvaj i zatvori**. Izabrani zadatak je povezan sa predmetom ugovora.

> [!NOTE]
> Ovo nije najoptimalnije iskustvo za pridruživanje projektnih zadataka predmetima ugovora. Svaki projekat će morati ručno da se poveže u ovom iskustvu. Poželjni način je sa kartice **Obračun zadataka** na stranici **Projekat**.

### <a name="from-the-project-page"></a>Sa stranice projekta

Ovo je optimalna metoda za povezivanje zadataka sa predmetima ugovora. Možete izabrati više zadataka i povezati sve njih i njihove podređene zadatke sa izabranim predmetom ugovora. Dovršite sledeće korake da biste zadatke povezali sa predmetom ugovora sa stranice **Projekat**.

1. Na kartici **Opšti podaci** predmeta ugovora zasnovanog na projektu, proverite da li je polje **Projekat** popunjeno.
2. U polju **Uključeni zadaci** izaberite **Samo izabrani zadaci**.
3. Sačuvajte predmet ugovora zasnovan na projektu. Obrazac će se osvežiti i kartica **Naplativi zadaci** će biti vidljiva. Ovo je samo u svrhu verifikacije.
4. Na kartici **Opšti podaci** predmeta ugovora zasnovanog na projektu, u polju **Projekat** izaberite vezu ka projektu.
5. Na stranici **Projekat** izaberite karticu **Podešavanje naplate za zadatak**.
6. Postoje dve mreže. Jedna mreža se odnosi na predmete ugovora koji se primenjuju na ceo projekat. Druga mreža se odnosi na podešavanje obračuna za određeni zadatak. U drugoj mreži izaberite jedan ili više zadataka, a zatim izaberite **Pridruženi predmeti ugovora**.
7. Na stranici dijaloga koja se otvori, izaberite predmet ugovora iz padajućeg menija.
8. Koristite padajući meni **Tip naplate** da biste zadatke označili kao naplative ili nenaplative.
9. Označite polje za potvrdu da biste naznačili da li bi povezivanje trebalo da uključuje i podređene zadatke izabranih zadataka. Označavanje polja će takođe povezati podređene zadatke izabranih zadataka sa predmetom ugovora.
10. Izaberite **U redu** da biste zatvorili dijalog.

## <a name="unassociate-tasks-from-project-based-contract-lines"></a>Nepovezani zadaci iz predmeta ugovora zasnovanih na projektu

### <a name="from-the-contract-line-page"></a>Sa stranice predmeta ugovora

Dovršite sledeće korake za raskinete vezu projektnih zadataka sa predmetom ugovora na kartici **Naplativi zadaci** na stranici **Predmet ugovora**.

1. Na kartici **Naplativi zadaci**, izaberite **Izbriši zadatak predmeta ugovora**.
2. Poruka upozorenja ukazuje da uklanjanje ovog povezivanja može dovesti do poništavanja stvarnih podataka prethodno zabeleženih u zadatku. Izaberite **U redu** u dijalogu da biste uklonili vezu između zadatka i predmeta ugovora zasnovanog na projektu. 

> [!NOTE]
> Ovo ne briše zadatak iz projekta. Umesto toga, uklanja povezivanje zadataka iz predmeta ugovora zasnovanog na projektu.

### <a name="from-the-project-page"></a>Sa stranice projekta

Ovo je optimalnije iskustvo za raskidanje veze zadataka sa predmetima ugovora. Možete izabrati više zadataka i raskinuti vezu za sve njih i njihove podređene zadatke sa izabranim predmetom ugovora. Dovršite sledeće korake da biste raskinuli vezu zadataka sa predmetom ugovora.

1. Na kartici **Opšti podaci** predmeta ugovora zasnovanog na projektu, u polju **Projekat** kliknite na vezu ka projektu.
2. Na stranici **Projekat** izaberite karticu **Podešavanje naplate za zadatak**.
3. Na stranici postoje dve mreže. Jedna mreža se odnosi na predmete ugovora koji se primenjuju na ceo projekat, a druga se odnosi na podešavanje obračuna specifičnih za zadatak. U drugoj mreži izaberite jedan ili više zadataka, a zatim izaberite **Prekini vezu sa predmetima ugovora**.
4. Na stranici dijaloga koja se otvori, izaberite predmet ugovora iz padajućeg menija.
5. Označite polje za potvrdu da biste naznačili da li bi povezivanje uklonilo i podređene zadatke izabranih zadataka. Označavanje polja će takođe raskinuti vezu podređenih zadataka izabranih zadataka sa predmetom ugovora.
6. Izaberite **U redu**. Poruka upozorenja ukazuje da uklanjanje ovog povezivanja može dovesti do poništavanja stvarnih podataka prethodno zabeleženih u zadatku. Izaberite **U redu** u dijalogu upozorenja da biste uklonili vezu između zadatka i predmeta ugovora zasnovanog na projektu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
