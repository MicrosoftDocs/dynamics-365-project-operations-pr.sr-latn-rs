---
title: Kopiranje mogućnosti za projekat
description: Ovaj članak pruža informacije o kopiranju mogućnosti za poslovanje zasnovanih na projektu u usluzi Project Operations.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0fe29918e14a944de7277639f752ad53513a7589
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 12/05/2022
ms.locfileid: "9826146"
---
# <a name="copy-project-opportunities"></a>Kopiranje mogućnosti za projekat

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_


Projektne mogućnosti za poslovanje se lako mogu kopirati da bi se stvorile nove projektne mogućnosti za poslovanje. 

1. Idite na stranicu **Projektne mogućnosti za poslovanje** i izaberite mogućnosti za poslovanje sa liste. Ili otvorite stranicu sa detaljima određene mogućnosti za poslovanje. 
2. Na bilo kojoj stranici izaberite **Kopiraj**. Otvoriće se stranica dijaloga koja sadrži sledeće informacije o polju. U zavisnosti od izabranih vrednosti u ovom dijalogu, postupak kopiranja se može promeniti.

    | **Polje** | **Opis** | **Posledični uticaj** |
    | --- | --- | --- |
    | Tema | Unesite relevantnu temu ciljne mogućnosti za poslovanje. Kada se dijalog otvori, sistem će ga podesiti na temu izvorne mogućnosti za poslovanje sa dodatim sufiksom **kopija**. | Nema posledičnog uticaja za ovo polje. |
    | Nalog | Upućivanja na zapis o kompaniji klijenta ili poslovnom kontaktu. Kada se dijalog otvori, sistem će ga postaviti na poslovni kontakt u izvornoj mogućnosti za poslovanje. | Ovo polje je primarni klijent u mogućnosti za poslovanje. |
    | Jedinica ugovaranja | Organizaciona jedinica koja je odgovorna za isporuku projekata povezanih sa ovom pogodbom. Kada se dijalog otvori, sistem će ga postaviti na jedinicu ugovaranja u izvornoj mogućnosti za poslovanje. | Jedinica ugovaranja je odeljenje preduzeća koje će izvršiti projekte nakon zaključenja pogodbe. Svaka ugovorna jedinica ima valutu i ona se koristi za izveštavanje o procenjenim i stvarnim troškovima nastalim tokom projekta. |
    | Valuta | Valuta u kojoj se obavljaju transakcije u pogodbi. Kada se stranica dijaloga otvori, sistem će ga postaviti na valutu u izvornoj mogućnosti za poslovanje. | Valuta se koristi za zadavanje podrazumevanog cenovnika i izradu finansijskih procena na ponudi. Na kraju, valuta se koristi za fakturisanje klijenta kada je pogodba dobijena. |
    | Kopiranje određivanja cene | Vrednost Da/Ne koja pokazuje da li treba kopirati cene za mogućnost za poslovanje iz izvorne mogućnosti za poslovanje. | Ako je **Da** izabrano, cenovnici se kopiraju iz izvorne u ciljnu mogućnost za poslovanje. Ako je izabrano **Ne**, cenovnici se podrazumevano postavljaju na osnovu najnovijih cenovnika koji su postavljeni. |

3. Izaberite **U redu**. Sistem kreira kopiju projektne mogućnosti za poslovanje na osnovu odabranih parametara i nova projektna mogućnost za poslovanje se otvara.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
