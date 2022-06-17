---
title: Kreiranje i ažuriranje projekta
description: Ovaj članak pruža informacije o ažuriranju projekata Projektnih operacija.
author: ruhercul
ms.date: 10/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dcb822a726f94a7e8e8621dc7a04f9051168d361
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911107"
---
# <a name="create-and-update-a-project"></a>Kreiranje i ažuriranje projekta

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Sledi rezime polja koja se mogu ažurirati na projektu nakon njegovog kreiranja. Ovo takođe uključuje sve primenljive implikacije zasnovane na ovim ispravkama.

## <a name="project-detail-fields"></a>Polja detalja o projektu

- **Naziv**: Naslov projekta.
- **Opis**: Pregled projekta.
- **Klijent**: Preduzeće kojem će projekat biti isporučen.
- **Predložak kalendara**: Radno vreme projekta. Kada se polje promeni, ceo raspored se preračunava.
- **Valuta**: Valuta projekta. Podrazumevana vrednost za ovo polje se zasniva na valuti koja je definisana u jedinici ugovaranja. Kada se ugovorna jedinica ažurira, polje se takođe ažurira.
- **Ugovorna jedinica**: Organizaciona jedinica koja predstavlja grupu ili odeljenje preduzeća koje je prvenstveno odgovorno za povećanje prodaje i upravljanje isporukom posla i usluga klijentu.  Kada organizaciona jedinica menadžera projekta nije definisana, ovo polje se podrazumevano koristi za vrednost definisanu u parametrima projekta.
- **Menadžer projekta**: Član projektnog tima koji ima ovlašćenje da pregleda i odobri stavke vremena i troškove.

## <a name="estimate-fields"></a>Polja za procenu

- **Procenjeni datum početka**: Datum početka projekta. Kada se ovo polje ažurira, svi zadaci na projektu pomeriće svoj početak srazmerno novom datumu početka.
- **Datum završetka**: Datum za kada je planiran završetak projekta.
- **Angažovanje**: Procenjeno angažovanje u projektu. Kada se zadaci dodaju u projekat, ovo polje više nije moguće uređivati.
- **Procenjena cena rada**: Procenjena cena rada na projektu. Kada se cene rada dodaju u projekat, ovo polje više nije moguće uređivati.
- **Procenjeni troškovi**: Procenjeni troškovi projekta. Kada se troškovi dodaju u projekat, ovo polje više nije moguće uređivati.

## <a name="project-actual-fields"></a>Polja stvarnih vrednosti projekta
- **Stvarni početak**: Datum kada je projekat započet.
- **Stvarni završetak**: Biće ažuriran kada se projekat završi.

## <a name="project-status-fields"></a>Polja statusa projekta

- **Sveukupni status projekta**: Sveukupna ispravnost projekta koju obezbeđuje menadžer projekta.
- **Komentari**: Opisivanje trenutne ispravnosti projekta koju je obezbedio menadžer projekta.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
