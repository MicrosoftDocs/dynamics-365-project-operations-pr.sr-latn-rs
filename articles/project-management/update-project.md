---
title: Ažuriranje projekta
description: Ova tema pruža informacije o ažuriranju projekata u usluzi Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: b0ec03a2c4dd7bc833b22b7a93fed810b4998a2788f4ff40234e3dd163bd9eb6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000908"
---
# <a name="update-a-project"></a>Ažuriranje projekta

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

U nastavku se nalazi rezime polja koja se mogu ažurirati u projektu nakon kreiranja i sve primenljive implikacije ažuriranja.

## <a name="project-detail-fields"></a>Polja detalja o projektu

- **Naziv**: Naslov projekta.
- **Opis**: Pregled projekta.
- **Klijent**: Preduzeće kojem će projekat biti isporučen.
- **Predložak kalendara**: Radno vreme projekta. Kada se polje promeni, ceo raspored se preračunava.
- **Valuta**: Valuta projekta. Ovo polje se podrazumevano zasniva na valuti definisanoj u ugovornoj jedinici. Kada se ugovorna jedinica ažurira, polje se takođe ažurira.
- **Ugovorna jedinica**: Organizaciona jedinica koja predstavlja grupu ili odeljenje preduzeća koje je prvenstveno odgovorno za povećanje prodaje i upravljanje isporukom posla i usluga klijentu. 
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