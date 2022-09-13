---
title: Kopiranje ugovora za projekat
description: Ovaj članak pruža informacije o kopiranju projektnih ugovora u projektne operacije.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8fa17bbd5738e4bc6330c728a3418a2be6828eef
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410184"
---
# <a name="copy-project-contracts"></a>Kopiranje ugovora za projekat

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Možete lako kreirati nove projektne ugovore kopiranjem postojećih ugovora na jedan od dva načina: 

  - Na stranici liste **Ugovori o projektima** izaberite ugovor za projekat, a zatim izaberite **Kopiraj**.
  - Na stranici detalja **Ugovori za projekat** izaberite **Kopiraj**.

Otvoriće se stranica dijaloga na kojoj možete izabrati parametre kopiranog ugovora. Sledeća polja su uključena u dijalog. U zavisnosti od izabranih vrednosti u ovom dijalogu, postupak kopiranja se može promeniti.

| **Polje** | **Opis** | **Posledični uticaj** |
| --- | --- | --- |
| Tema | Unesite temu ciljnog ugovora. Kada se stranica dijaloga otvori, sistem će podesiti ovo polje na naziv izvornog ugovora sa dodatim sufiksom **-kopija**. | Nema posledičnog uticaja za ovo polje. |
| Klijent | Upućivanje na zapis o kompaniji klijenta ili poslovnom kontaktu. Kada se dijalog otvori, sistem će postaviti ovo polje na poslovni kontakt u izvornom ugovoru. | Ovo polje je primarni klijent u ugovoru. |
| Jedinica ugovaranja | Organizaciona jedinica koja je odgovorna za isporuku projekata povezanih sa ovom pogodbom. Kada se stranica dijaloga otvori, sistem će je postaviti na jedinicu ugovaranja izvornog ugovora. | Jedinica ugovaranja je odeljenje preduzeća koje će izvršavati projekte nakon zaključenja pogodbe. Svaka jedinica ugovaranja ima valutu. Ova valuta se koristi za izveštavanje o procenjenim i stvarnim troškovima nastalim tokom projekta. |
| Valuta | Valuta u kojoj se obavljaju transakcije u pogodbi. Kada se stranica dijaloga otvori, sistem će postaviti polje na valutu izvornog ugovora. Nije moguće promeniti valutu. Ako jeste, polje **Kopiraj cene** je uvek postavljeno na **Ne** jer cenovnici u izvornom ugovoru više nisu relevantni. | Valuta se koristi za podrazumevani cenovnik, za izradu finansijske procene na ugovoru i za fakturisanje klijentu kada se pogodba ostvari. |
| Zahtevani datum isporuke | Datum isporuke koji je klijent zahtevao. | Ovaj datum se koristi kao datum završetka prilikom kreiranja datuma fakturisanja prema određenoj učestalosti. |
| Kopiranje određivanja cene | Ukazuje na to da li određivanje cene na ugovoru treba kopirati iz izvornog ugovora. | Ako je polje podešeno na **Da**, reference na cenovnik projekta i cenovnik proizvoda se kopiraju iz izvornog u ciljni ugovor. Ako je izabrano **Ne**, cenovnici se podrazumevano postavljaju na osnovu najnovijih cenovnika u parametrima poslovnog kontakta ili projekta. |

Kada na stranici dijaloga izaberete **U redu**, sistem kreira kopiju ugovora na osnovu izabranih parametara. Otvoriće se novi ugovor.

Sledeće informacije se ne kopiraju iz **izvornog** u **ciljni ugovor**:

  - Rasporedi za fakturisanje
  - Ugovor i klijenti predmeta ugovora
  - Referenca projekta u predmetima ugovora zasnovanih na projektu
  - Informacije o budžetu klijenta

Budući da su ove informacije vrlo specifične za svaki ugovor, ta polja i zapisi se ne kopiraju. Kopiraju se predmeti ugovora za projekte i proizvode, procene detalja predmeta ugovora i vrednosti koje ne smeju da premaše vrednost na nivou ugovora. Podrazumevane vrednosti cena i stopa troškova zavise od izbora u polju **Kopiranje određivanja cena** na stranici dijaloga **Kopiranje parametara**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
