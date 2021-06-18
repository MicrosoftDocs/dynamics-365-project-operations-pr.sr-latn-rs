---
title: Kopiranje ponuda zasnovanih na projektu
description: Ova tema pruža informacije o načinu kopiranja ponuda zasnovanih na projektu u usluzi Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4e9009391d33c5dd5988ae65e13ca1ca1ec398bc
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999103"
---
# <a name="copy-project-based-quotes"></a>Kopiranje ponuda zasnovanih na projektu

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Možete lako kreirati novu ponudu za projekat kopiranjem postojeće. 

- Da biste kopirali ponudu za projekat, na stranici liste **Ponude za projekat** ili stranici detalja **ponude za projekat**, izaberite ponudu za projekat koju želite da kopirate, a zatim izaberite **Kopiraj**.

To će otvoriti stranicu dijaloga na kojoj možete uneti parametre kopije. Sledeća tabela navodi polja koja su uključena u stranicu dijaloga. U zavisnosti od izabranih vrednosti, postupak kopiranja se može promeniti.

| **Polje** | **Opis** | **Posledični uticaj** |
| --- | --- | --- |
| Tema | Unesite odgovarajuću temu ili naziv ciljne ponude. Kada se dijalog otvori, sistem će ga podesiti na temu izvorne ponude sa dodatim sufiksom **-kopija**. | |
| Potencijalni klijent | Upućivanje na zapis o kompaniji klijenta ili poslovnom kontaktu. Kada se dijalog otvori, sistem će ga postaviti na poslovni kontakt u izvornoj ponudi. | Ovo polje je primarni klijent u ponudi. |
| Jedinica ugovaranja | Organizaciona jedinica koja je odgovorna za isporuku projekata povezanih sa ovom pogodbom.
Kada se dijalog otvori, sistem će ga postaviti na jedinicu ugovaranja u izvornoj ponudi. | Jedinica ugovaranja je odeljenje preduzeća koje će izvršiti projekte nakon zaključenja pogodbe. Svaka jedinica ugovaranja ima valutu. Valuta se koristi za izveštavanje o procenjenim i stvarnim troškovima nastalim tokom izvršenja projekta. |
| Valuta | Ovo je valuta u kojoj se obavljaju transakcije u pogodbi. Kada se dijalog otvori, sistem će ga postaviti na valutu izvorne ponude. Ovo se može izmeniti, a ako je to promena, polje **Kopiraj određivanje cena** je uvek postavljeno na **Ne**. To je zato što cenovnici na izvornoj ponudi više nisu relevantni. | Valuta se koristi za podrazumevani cenovnik, za izradu finansijske procene na ponudi i na kraju za fakturisanje klijentu kada se pogodba ostvari. |
| Zahtevani datum isporuke | Ovo je datum isporuke koji zahteva klijent. | Ovo se koristi kao datum završetka prilikom kreiranja datuma fakturisanja duž određene frekvencije. |
| Kopiranje određivanja cene | Vrednost Da/Ne ukazuje na to da li bi se određivanje cene na ponudi moralo kopirati iz izvorne ponude. | Ako je izabrano **Da**, reference na cenovnik projekta i cenovnik proizvoda se kopiraju iz izvorne ponude u ciljnu ponudu. Ako je izabrano **Ne**, cenovnici se podrazumevano postavljaju na osnovu najnovijih cenovnika koji su postavljeni u parametrima poslovnog kontakta ili projekta. |

Kada na stranici dijaloga izaberete **U redu**, sistem kreira kopiju ponude za projekat na osnovu parametara izabranih u dijalogu. Otvara se nova ponuda za projekat. 

> [!NOTE]
> Sledeće informacije se ne kopiraju iz izvorne u ciljnu ponudu:
>
> - Rasporedi za fakturisanje
> - Ponuda i klijenti stavke ponude
> - Referenca projekta na stavkama ponude zasnovane na projektu – Informacije o budžetu klijenta
>
>Budući da su ove informacije vrlo specifične za svaku ponudu, ta polja i zapisi se ne kopiraju. Kopiraju se stavke ponude za projekte i proizvode, procene detalja stavki ponude i vrednosti koje ne smeju da premaše vrednost na nivou ponude. Podrazumevane vrednosti cena i stopa troškova zavise od opcije **Kopiranje određivanja cena** izabrane na stranici dijaloga **Kopiranje parametara**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]