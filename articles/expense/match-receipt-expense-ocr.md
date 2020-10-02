---
title: Podudaranje priznanice sa troškom koristeći OCR
description: Ova tema pruža informacije o obradi priznanica pomoću optičkog prepoznavanja znakova (OCR).
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 02c1bafbe907a657689b610ae792f88085320903
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897018"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a>Podudaranje priznanice sa troškom koristeći OCR

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Unos troškova je poboljšan uvođenjem obradu priznanica putem optičkog prepoznavanja znakova (OCR). Ova funkcionalnost je dizajnirana da poboljša korisničko iskustvo prilikom kreiranja izveštaja o troškovima.

## <a name="key-features"></a>Ključne funkcije

- Sistem izdvaja ime trgovca, datum i ukupan iznos sa priznanice.
- Sistem će pokušati da uskladi nevezane priznanice sa nevezanim transakcijama troškova.
- Iz priznanica možete da kreirate ručno unete transakcije troškova.

## <a name="attach-receipts-to-an-expense-report"></a>Priložite priznanice uz izveštaj o troškovima

Da biste automatski priložili priznanice koje uključuju transakcije kreditnom karticom kada se kreira izveštaj o troškovima, izvršite sledeće korake.

  1. Otvorite radni prostor **Upravljanje troškovima**.
  2. Na kartici **Priznanice** proverite da li postoje nepriložene priznanice. Takođe možete da otpremite priznanice na karticu **Priznanice**.
  3. Na kartici **Troškovi** proverite da li postoje nepriloženi troškovi. Obično ih administrator troškova uvozi od dobavljača kreditne kartice.
  4. Izaberite **Novi izveštaj o troškovima**. Obratite pažnju da i sada možete da uključite troškove i priznanice kada kreirate izveštaj o troškovima. Ako dodate i troškove i račune, aktiviraće se automatsko upoređivanje priznanice i troškova.

## <a name="create-or-match-receipts-to-an-expense-report"></a>Kreirajte ili uporedite priznanice sa izveštajem o troškovima
Da biste stvorili trošak ili uporedili trošak sa priznanice, izvršite sledeće korake.

  1. Na izveštaju o troškovima, na kartici **Priznanice**, priložite priznanicu izborom stavke **Dodaj priznanice**.
  2. Ispod otpremljene slike priznanice videćete opcije **Kreiraj** i **Uporedi**.

      - Izaberite **Kreiraj** da biste kreirali ručno unete transakcije troškova i popunili vrednosti koje su izdvojene iz priznanice.
      - Ako izaberete **Uporedi**, sistem pokušava da postojeći trošak uskladi sa priznanicom.

## <a name="installation"></a>Instalacija

Da biste koristili ove napredne mogućnosti troškova, instalirajte programski dodatak Usluga upravljanja troškovima za Microsoft Dynamics 365 Finance i uključite funkcije u vašoj instanci. Programskom dodatku možete pristupiti iz svog projekta u usluzi Microsoft Dynamics Lifecycle Services (LCS).

1. Prijavite se na LCS i otvorite željeno okruženje.
2. Idi na stavku **Svi detalji**.
3. Izaberite **Održavanje** ili se pomerite nadole do brze kartice **Programski dodaci za životnu sredinu**.
4. Izaberite stavku **Instalirajte novi programski dodatak**.
5. Izaberite stavku **Usluga upravljanja troškovima**.
6. Sledite uputstva za instalaciju i prihvatite odredbe i uslove.
7. Izaberite **Instaliraj**.

U radnom prostoru **Upravljanje funkcijama** uključite sledeće funkcije:

- Ponovno osmišljeni izveštaji o troškovima
- Automatsko podudaranje i kreiranje troškova iz priznanice

Kada uključite ove funkcije, dešavaju se sledeće radnje:

- Postojeći radni prostor **Upravljanje troškovima** se zamenjuje novim radnim prostorom.
- Dodata je nova stavka menija za vidljivost polja troškova.
- Još uvek možete otvoriti prethodnu stranicu **Izveštaji o troškovima** odlaskom na **Upravljanje troškovima > Moji troškovi > Izveštaji o troškovima**.
- Tokovi posla i sva odobrenja vas i dalje vode na postojeću stranicu sa izveštajima o troškovima.
- Priznanice će se obrađivati putem Microsoft Azure Cognitive Services, a metapodaci će biti izdvojeni i dodati.
- Dodata je opcija koja vam omogućava da napravite izveštaj o troškovima koji uključuje odgovarajuće nepriložene priznanice.
- Opcija koja se dodaje izveštajima o troškovima omogućava vam da kreirate liniju troškova iz priznanica ili pokušate da uporedite postojeću priznanicu sa postojećom linijom troškova.

## <a name="frequently-asked-questions"></a>Najčešća pitanja

**Da li Microsoft koristi moje podatke za svoje modele?**

Ne, Microsoft je izgradio opšti model mašinskog učenja za uslugu obrade priznanica. Ovaj model se ne zasniva na priznanicama koje otpremite.

**Gde je ova funkcija dostupna i obrađena?**

Trenutno su podržane Sjedinjene Države.

**Gde odlaze moje priznanice?**

Finansije će kontaktirati Cognitive Services da bi izvukli podatke sa terena. Cognitive Services će zadržati kopiju vaše priznanice i do 24 sata dok traje obrada. Po završetku obrade, Cognitive Services će ukloniti priznanicu. Priznanice se i dalje čuvaju u Finansijama.

Za više informacija pogledajte [Omogućite razumevanje priznanice sa novom sposobnošću prepoznavanja obrazaca](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).
