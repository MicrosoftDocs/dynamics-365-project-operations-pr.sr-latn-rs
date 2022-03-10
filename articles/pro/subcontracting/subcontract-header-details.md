---
title: Detalji zaglavlja za podugovore
description: Ova tema objašnjava funkcionalnost koja je navedena u zaglavlju podugovora u aplikaciji Project Operations.
author: rumant
ms.date: 09/14/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ee863d31b45e7de962488fe804202ddfe580eb04
ms.sourcegitcommit: 083e3d219cd5126eecb74debb1b70b361680b1f6
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/18/2021
ms.locfileid: "7501343"
---
# <a name="header-details-for-subcontracts"></a>Detalji zaglavlja za podugovore

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Ova tema objašnjava funkcionalnost koja je navedena u zaglavlju u aplikaciji Dynamics 365 Project Operations.

Kako menadžer projekata planira i izvršava projekte, može zaposliti podizvođače i kupovati proizvode i usluge od prodavaca. Kada menadžer projekta treba da kupi proizvode ili usluge, može da sklopi podugovor u okviru aplikacije Project Operations.

Da biste kreirali podugovor, obavite sledeće korake.

1. U oknu za navigaciju izaberite **Podugovori**, i na stranici **Podugovor** izaberite **Novo**.
2. Unesite potrebne informacije, a zatim izaberite **Sačuvaj**.

    Sledeća tabela pruža informacije o poljima na stranici **zaglavlja podugovora**.

    | Polje | Opis |Funkcionalni uticaj |
    |---|------|---| 
    | +Ime | Naziv podugovora. | Na svim padajućim listama podugovora, naziv podugovora naveden je u prvoj koloni kako bi vam pomogao da identifikujete podugovor. | 
    | Opis | Kratak opis usluga i proizvoda koji se kupuju u okviru podugovora. | Ništa |
    | Prodavac | Naziv kompanije od koje se kupuju proizvodi i usluge. Ovaj zapis naloga ima vrstu odnosa **Prodavac** ili **Dobavljač**. | Na osnovu izabranog dobavljača, podrazumevane vrednosti se automatski unose za sledeća polja:<br/> **• Valuta** </br> **• Cenovnici** </br> **• Uslovi plaćanja**</br> **• Adresa plaćanja**</br> **• Adresa za fakturisanje**</br> **• Ime za fakturisanje** </br>**• Menadžer poslovnog kontakta dobavljača**|
    | Datum podugovora | Datum kada je kreiran podugovor. | Datum podugovora se koristi za izbor ispravnog cenovnika za nabavku, bilo iz cenovnika koji su priloženi povezanom dobavljaču ili iz parametara projekta. |
    | Razlog statusa | Status podugovora. | Status određuje gde se podugovor nalazi u poslovnom procesu i da li se može urediti. <br/>Vrednosti uključuju:<br>• **Nacrt**: Podugovor može da se uređuje. Možete da uređujete samo podugovore sa statusom **Nacrt**.<br/>• **Potvrđeno**: Pregovori sa dobavljačem su završeni i podugovor je odobren za isporuku. <br/>• **Zatvoreno**: Isporuka za podugovor je završena.<br/>• **Otkazano**: Podugovor je otkazan i isporuka nije planirana.  | 
    | Valuta | Valuta u kojoj se kupuju proizvodi i usluge. Podrazumevana vrednost se automatski unosi iz poslovnog kontakta dobavljača, ali se može promeniti. | Valuta podugovora se koristi za izbor cenovnika za nabavku, bilo iz cenovnika koji su priloženi povezanom dobavljaču ili iz parametara projekta. Cenovnici u drugoj valuti ne mogu se povezati sa podugovorom. Cene vremena, troškova i materijala koje resursi dobavljača isporučuju po ovom podugovoru su evidentirane u ovoj valuti na projektu. Nakon što se sačuva zapis podugovora, valuta na podugovoru se ne može promeniti.|
    | Jedinica ugovaranja | Odeljenje kompanije koja sklapa kupoprodajni ugovor ili podugovor sa prodavcem. | Ništa |
    | Uslovi plaćanja | Uslovi plaćanja na fakturama dobavljača koje su izdate po ovom podugovoru. Podrazumevana vrednost se automatski unosi iz zapisa poslovnog kontakta dobavljača. | Uslovi plaćanja iz podugovora kopiraju se na sve fakture dobavljača koje su povezane sa ovim podugovorom. Uslovi plaćanja se mogu ažurirati ako podugovor ima status **Nacrt**. | 
    | Adresa plaćanja | Adresa dobavljača kojem treba poslati uplate. Podrazumevana vrednost se automatski unosi iz zapisa poslovnog kontakta dobavljača. | Adresa za plaćanje iz podugovora kopira se kao adresa za plaćanje na sve fakture dobavljača koje su kreirane za ovaj podugovor. Adresa za plaćanje se može ažurirati ako podugovor ima status **Nacrt**.|
    | Ime fakturisanja | Ime osobe ili odeljenja u kompaniji prodavca koja će poslati fakturu. Podrazumevana vrednost se automatski unosi iz zapisa poslovnog kontakta dobavljača. | Vrednost **Ime za fakturisanje** iz podugovora kopira se na sve fakture dobavljača koje su povezane sa ovim podugovorom. Ovo polje se može ažurirati ako podugovor ima status **Nacrt**.|
    | Adresa fakturisanja | Adresa koja se koristi na fakturama dobavljača. Podrazumevana vrednost se automatski unosi iz zapisa poslovnog kontakta dobavljača. | Ova adresa je adresa „pošiljaoca fakture“ na fakturama dobavljača koje su kreirane za ovaj podugovor. |
    | Međuiznos | Ako podugovor nema stavke, unesite međuzbir narudžbine pre oporezivanja. Ako podugovor ima predmete, ovo polje je samo za čitanje. Iznos koji je prikazan je međuzbir iz svih stavki na podugovoru. | Ništa |
    | Ukupan porez | Ako podugovor nema stavke, unesite ukupan iznos poreza na podugovoru. Ako podugovor ima predmete, ovo polje je samo za čitanje. Iznos koji je prikazan je zbir iznosa poreza za sve stavke na podugovoru. | Ništa |
    | Ukupan iznos | Ovo izračunato polje prikazuje ukupan iznos iz podugovora nakon uključivanja poreza. | Ništa |
    | Datum potvrđivanja | Datum kada je podugovor potvrđen. | Ništa |
    | Podnosilac zahteva | Podrazumevano, ovo polje je podešeno na ime korisnika koji kreira podugovor. Međutim, tvorac podugovora može promeniti vrednost kako bi naznačio osobu u čije ime kreira podugovor. | Ništa |
    | Menadžera poslovnog kontakta prodavca | Ime primarnog kontakta sa naloga prodavca. Podrazumevana vrednost se automatski unosi iz zapisa poslovnog kontakta dobavljača. Možete izabrati drugi kontakt za menadžera poslovnog kontakta dobavljača podugovora. | Možete da podesite upozorenja putem e-pošte za obaveštavanje kontakta o promenama u podugovoru kao rezultat pregovora o ceni. |
