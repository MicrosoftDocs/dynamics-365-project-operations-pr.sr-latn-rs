---
title: Obrada priznanica za troškove
description: Ova tema pruža informacije o obradi priznanica pomoću optičkog prepoznavanja znakova (OCR). Ova funkcija je dizajnirana da poboljša korisničko iskustvo prilikom kreiranja izveštaja o troškovima u usluzi Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 31c08ea264e6caec3217f4b424275495f39123e3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083738"
---
# <a name="expense-receipt-processing"></a>Obrada priznanica za troškove

[!include [banner](../includes/banner.md)]

Unos troškova je poboljšan uvođenjem obradu priznanica putem optičkog prepoznavanja znakova (OCR). Ova funkcija je dizajnirana da poboljša korisničko iskustvo prilikom kreiranja izveštaja o troškovima.

## <a name="key-features"></a>Ključne funkcije

- Sa priznanice se izdvajaju ime trgovca, datum i ukupan iznos.
- Funkcija pokušava da uskladi nevezane priznanice sa nevezanim transakcijama troškova.
- Korisnici iz priznanica mogu da kreiraju ručno unete transakcije troškova.

## <a name="usage-examples"></a>Primeri upotrebe

Da biste automatski priložili priznanice koje uključuju transakcije kreditnom karticom kada se kreira izveštaj o troškovima, izvršite sledeće korake:

  1. Otvorite radni prostor **Upravljanje troškovima**.
  2. Na kartici **Priznanice** proverite da li postoje nepriložene priznanice. Takođe možete da otpremite priznanice na karticu **Priznanice**.
  3. Na kartici **Troškovi** proverite da li postoje nepriloženi troškovi. Obično ih administrator troškova uvozi od dobavljača kreditne kartice.
  4. Izaberite **Novi izveštaj o troškovima**. Obratite pažnju da i sada možete da uključite troškove i priznanice kada kreirate izveštaj o troškovima. Ako dodate i troškove i račune, aktiviraće se automatsko upoređivanje priznanice i troškova.

Da biste stvorili trošak ili uporedili trošak sa priznanice, izvršite sledeće korake:

  1. Na izveštaju o troškovima, na kartici **Priznanice** , priložite priznanicu izborom stavke **Dodaj priznanice**.
  2. Ispod otpremljene slike priznanice videćete opcije **Kreiraj** i **Uporedi**.

      - Izaberite **Kreiraj** da biste kreirali ručno unete transakcije troškova i popunili vrednosti koje su izdvojene iz priznanice.
      - Ako izaberete **Uporedi** , sistem pokušava da postojeći trošak uskladi sa priznanicom.

## <a name="installation"></a>Instalacija

Ova funkcija radi u kombinaciji sa funkcijom **Redizajnirani izveštaji o troškovima** koja vam pomaže da pojednostavite iskustvo sa troškovima. Ova funkcija je dostupna samo za okruženja 2. nivoa i viših, a to su Sandbox i Proizvodnja.

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

Za više informacija o redizajniranoj funkciji izveštaja o troškovima pogledajte [Redizajnirani izveštaji o troškovima](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Najčešća pitanja

**Da li Microsoft koristi moje podatke za svoje modele?**

Ne, Microsoft je izgradio opšti model mašinskog učenja za uslugu obrade priznanica. Ovaj model se ne zasniva na priznanicama koje otpremite.

**Gde je ova funkcija dostupna i obrađena?**

Trenutno su podržane Sjedinjene Države.

**Gde odlaze moje priznanice?**

Finansije će kontaktirati Cognitive Services da bi izvukli podatke sa terena. Cognitive Services će zadržati kopiju vaše priznanice i do 24 sata dok traje obrada. Po završetku obrade, Cognitive Services će ukloniti priznanicu. Priznanice se i dalje čuvaju u Finansijama.

Za više informacija pogledajte [Omogućite razumevanje priznanice sa novom sposobnošću prepoznavanja obrazaca](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).
