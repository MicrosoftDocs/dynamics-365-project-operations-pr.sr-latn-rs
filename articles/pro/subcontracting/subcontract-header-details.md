---
title: Detalji zaglavlja za podugovore
description: Ova tema objašnjava funkcionalnost koja je navedena u zaglavlju podugovora u aplikaciji Project Operations.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 49158af1a430033db3a5db57a840512c45bc17e2
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323658"
---
# <a name="header-details-for-subcontracts"></a>Detalji zaglavlja za podugovore

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Ova tema objašnjava funkcionalnost koja je navedena u zaglavlju u aplikaciji Dynamics 365 Project Operations.

Kako menadžer projekata planira i izvršava projekte, može zaposliti podizvođače i kupovati proizvode i usluge od prodavaca. Kada menadžer projekta treba da kupi proizvode ili usluge, može da sklopi podugovor u okviru aplikacije Project Operations.

Da biste kreirali podugovor, obavite sledeće korake.

1. U oknu za navigaciju izaberite **Podugovori**, i na stranici **Podugovor** izaberite **Novo**.
2. Unesite potrebne informacije, a zatim izaberite **Sačuvaj**.

    Sledeća tabela pruža informacije o poljima na stranici zaglavlja podugovora.

    | **Polje** | **Opis** |
    | --- | --- | 
    | +Ime | Naziv podugovora. |
    | Opis | Kratak opis usluga i proizvoda koji se kupuju u okviru podugovora. |
    | Prodavac | Naziv kompanije od koje se kupuju proizvodi i usluge. Ovaj zapis naloga ima vrstu odnosa **Prodavac** ili **Dobavljač**. |
    | Datum podugovora | Datum kreiranja podugovora. |
    | Razlog statusa | Status podugovora. |
    | Valuta | Valuta u kojoj se kupuju proizvodi i usluge. Vrednost u ovom polju podrazumevano se dobija na osnovu naloga prodavca, ali se može promeniti. Cenovnici projekata koji se koriste za određivanje cena proizvoda i usluga u podugovoru treba da budu u ovoj valuti. Cenovnici u bilo kojoj drugoj valuti ne mogu se pridružiti podugovoru. Troškovi proizvoda i usluga nastali po ovom podugovoru biće evidentirani na projektu u ovoj valuti. |
    | Jedinica ugovaranja | Odeljenje kompanije koja sklapa kupoprodajni ugovor ili podugovor sa prodavcem. |
    | Uslovi plaćanja | Uslovi plaćanja na fakturama dobavljača koji su izdati po ovom podugovoru. Vrednost u ovom polju podrazumevano se dobija na osnovu zapisa prodavca. |
    | Adresa plaćanja | Adresa na koju se šalje uplata na fakturama prodavca. Vrednost u ovom polju podrazumevano se dobija na osnovu zapisa prodavca. |
    | Ime fakturisanja | Ime osobe ili odeljenja u kompaniji prodavca koja će poslati fakturu. Vrednost u ovom polju podrazumevano se dobija na osnovu zapisa naloga prodavca i koristiće se kao naziv primarnog kontakta na fakturama prodavca kreiranim za ovaj podugovor. |
    | Adresa fakturisanja | Adresa koja se koristi na fakturama ovog prodavca. Vrednost u ovom polju podrazumevano se dobija na osnovu zapisa prodavca. Ova adresa se takođe koristi kao adresa fakturisanja na fakturama prodavca napravljenim za ovaj podugovor. |
    | Međuiznos | Ako podugovor nema predmeta, unesite vrednost u ovo polje koja označava međuzbir porudžbina pre oporezivanja. Ako podugovor ima predmete, ovo polje je samo za čitanje. Prikazani iznos je međuzbir iz svih predmeta na podugovoru. |
    | Ukupan porez | Ako podugovor nema predmeta, unesite vrednost u ovo polje koja označava poreza na ovom podugovoru. Ako podugovor ima predmete, ovo polje je samo za čitanje. Prikazani iznos je zbir poreza iz svih predmeta na podugovoru. |
    | Ukupan iznos |  Ovo izračunato polje prikazuje ukupan iznos iz podugovora nakon uključivanja poreza.  |
    | Datum potvrđivanja | Datum potvrđivanja podugovora.  |
    | Podnosilac zahteva | Vrednost u ovom polju podrazumevano je ime korisnika koji kreira podugovor. Ovu vrednost može promeniti autor podugovora da bi označio osobu u čije ime sklapa podugovor.  |
    | Menadžera poslovnog kontakta prodavca | Ime primarnog kontakta sa naloga prodavca. Vrednost u ovom polju podrazumevano se dobija na osnovu zapisa prodavca. Ovu vrednost polja može da promeni korisnik kako bi izabrao drugi kontakt kao menadžera naloga prodavca na podugovoru. Ovaj kontakt može konfigurisati i slati upozorenja putem e -pošte i pregovore o ceni. |


