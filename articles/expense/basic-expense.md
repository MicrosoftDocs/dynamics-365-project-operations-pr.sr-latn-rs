---
title: Stavka troška (lagana verzija)
description: Ova tema pruža informacije o tome kako raditi sa stavkom troška u jednostavnoj primeni.
author: stsporen
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 774bf2f8f54d2e314740fbad40ea15ce83d38297
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578357"
---
# <a name="expense-entry-lite"></a>Stavka troška (lagana verzija)

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Osnovno (ili lagano) upravljanje troškovima je sposobnost evidentiranja jednostavnih troškova. Možete evidentirati troškove na projektu, a zatim će ih davalac odobrenja pregledati i odobriti.

Za više informacija o mogućnostima troškova u usluzi Dynamics 365 Project Operations, pogledajte [Pregled troškova](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Obuhvatanje osnovnog troška

Možete pokriti svoje troškove kako biste ih mogli dostaviti davaocu odobrenja.

1. Idite na **Troškovi** i izaberite **Novi**.
2. Na stranici **Novi trošak**, unesite potrebne informacije o troškovima, a zatim izaberite **Sačuvaj**.

## <a name="submit-a-basic-expense"></a>Prosleđivanje osnovnog troška

Kada završite sa evidentiranjem svih troškova i budete li spremni da ih odobrite, morate ih prijaviti.

1. Idite na **Troškovi** i izaberite trošak. Ili izaberite sve troškove pomoću polja za potvrdu u zaglavlju.
2. Izaberite **Prosledi**. Sistem obrađuje odabrane stavke, a zatim kreira zahteve za odobrenje troškova.

## <a name="add-an-attachment"></a>Dodajte prilog

Možda ćete odobravaocu morati da dostavite dodatnu dokumentaciju o svom trošku. U vremensku osu unosa troškova možete priložiti priznanicu. Izaberite **Uredi** i u odeljku **Vremenska osa**, a zatim izaberite ikonu spajalice da biste priložili priznanicu.

## <a name="recall-a-basic-expense"></a>Opoziv osnovnog troška

Kada greškom prosledite trošak, možete ga opozvati. Vreme potrebno za opoziv stavke troška zavisi od faze odobrenja.  Ako davalac odobrenja još nije odobrio stavku, opoziv se može izvršiti odmah. Međutim, ako je stavka već odobrena, od davaoca odobrenja se traži da odobri opoziv i poništi transakcije.

1. Idite na **Troškovi**, a zatim na listi troškova odaberite trošak koji ćete opozvati.
2. Izaberite **Opozovi**. Ako stavka troška još nije odobrena, sistem je odmah opoziva. Ako je stavka troška već odobrena, kreira se zahtev za opoziv da obavesti davaoca odobrenja da želite da stornirate trošak. Davalac odobrenja će zatim potvrditi da se storniranje može izvršiti i stavka će biti vraćena.

## <a name="delete-a-basic-expense"></a>Brisanje osnovnog troška

Troškovi koji još nisu prosleđeni mogu se izbrisati. Da biste izbrisali trošak koji je već prosleđen, prvo ga morate opozvati.

## <a name="see-also"></a>Takođe pogledajte

- [Pregled odobrenja](../approvals/approvals-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]