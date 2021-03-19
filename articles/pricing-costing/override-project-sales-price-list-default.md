---
title: Izmena prodajnih cenovnika za projekat
description: Ova tema pruža informacije o kreiranju prilagođenih prodajnih cenovnika.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17a86e89f626cef720fe3c8db0cbd8d6a2a3ddd5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275555"
---
# <a name="override-project-sales-price-lists"></a>Izmena prodajnih cenovnika za projekat

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

## <a name="customer-specific-project-price-lists"></a>Cenovnici projekata specifični za klijenta

Ugovori o cenama specifični za klijenta mogu se postaviti kao cenovnici projekata u zapisu poslovnog kontakta u usluzi Dynamics 365 Project Operations.

Da biste postavili cenovnik projekata specifičan za klijenta, u oblasti **Prodaja**, dođite do zapisa o poslovnom kontaktu.

1. Otvorite stranicu liste **Poslovni kontakti**.
2. Pronađite i dvaput kliknite na zapis klijenta da biste otvorili stranicu sa detaljima o **poslovnom kontaktu**.
3. Na kartici **Cenovnici projekta** izaberite **+ Novi cenovnik projekta**.
4. Na stranici **Novi cenovnik projekta**, iz padajuće liste izaberite cenovnik. Uključeni su samo cenovnici kojima je kontekst postavljen na **Prodaja** i čija valuta se podudara sa valutom poslovnog kontakta.
5. Imenujte povezivanje, a zatim izaberite **Sačuvaj**. Kreiraće se cenovnik projekta specifičan za klijenta. Ovaj cenovnik će se koristiti za podrazumevane cene za projekat u ponudama ili ugovorima za projekat kreiranim za ovog klijenta kada datum kreiranja ponude ili ugovora za projekat spada u datum efektivnosti cenovnika.

## <a name="custom-pricing-on-project-quotes"></a>Prilagođeno određivanje cena u ponudama za projekat

U ponudama za projekat, možete imati cene projekata koje počinju sa podrazumevanim standardnim cenovnikom koji dobija podrazumevane vrednosti od klijenta ili iz parametara projekta.

Kada vam je potrebno prilagođeno određivanje cena za posao u vezi sa projektom za određenu ponudu, to možete dobiti iz entiteta povezanog sa cenovnicima projekata.

Dovršite sledeće korake da biste postavili cene projekata specifične za ponudu.

1. Otvorite ponudu za projekat i izaberite karticu **Cenovnici projekta**.
2. U podformi izaberite **Kreiraj prilagođene cene**.

Svi cenovnici projekta koji su priloženi uz ponudu kopiraju se u nove cenovnike. Nazivi novih cenovnika odražavaju naziv ponude sa obeležjem datuma i vremena kada su ovi cenovnici kreirani.

Možete da koristite svaki od tih cenovnika i ažurirate cene rada (cena uloge) i cene troškova (cena kategorije). Ove cene će se primenjivati samo na ovu ponudu za projekat.

## <a name="price-lists-on-a-project-contract"></a>Cenovnici u ugovoru za projekat

U ugovoru za projekat, određivanje cena za projekat se uvek podrazumeva iz prilagođenog cenovnika sa nazivom ugovora i obeležjem datuma i vremena kreiranja koji se dodaje nazivu. To je tačno da li je ugovor kreiran kada je ponuda dobijena ili je ugovor kreiran ispočetka. Ako je potrebno, možete ukloniti ovo povezivanje sa prilagođenim cenovnikom i umesto toga pridružiti standardni cenovnik ugovoru o projektu.

Kada standardni cenovnik pridružite cenovnicima projekta u ponudi ili ugovoru, sve promene cena u cenovniku uticaće na sve ponude i ugovore koji koriste taj cenovnik.


[!INCLUDE[footer-include](../includes/footer-banner.md)]