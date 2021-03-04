---
title: Redizajnirani izveštaji o troškovima
description: Ova tema pruža informacije o redizajniranom i ponovo osmišljenom iskustvu za unos izveštaja o troškovima u usluzi Microsoft Dynamics 365 Finance. Novo iskustvo pojednostavljuje postupak popunjavanja izveštaja o troškovima i smanjuje vreme koje je potrebno za to.
author: ryansandness
manager: AnnBe
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: d076c0a596940cb08433f7ee57dea54903f6078f
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960264"
---
# <a name="redesigned-expense-reports"></a>Redizajnirani izveštaji o troškovima

Unos izveštaja o troškovima redizajniran je kako bi se pojednostavio postupak dovršavanja izveštaja o troškovima i smanjilo vreme potrebno za popunu izveštaja. Evo glavnih komponenti novog iskustva sa troškovima:

- Novi radni prostor za upravljanje troškovima koji vam omogućava pristup troškovima vašeg delegata.
- Novo iskustvo podudaranja priznanica kako bi se bolje prikazale priznanice na nivou zaglavlja i pojednostavio postupak povezivanja računa sa stavkama troškova.
- Nova mreža samo za čitanje koja vam omogućava da vidite mnogo više stavki troškova i dodatne kolone podataka. Sada možete videti sve razdvojene i podeljene stavke, zajedno sa nadređenim troškovima.
- Pojednostavljeno okno za uređivanje troškova.
- Redizajnirane poruke o greškama, upozorenjima i smernicama obezbeđuju da imate tačan kontekst i razumevanje problema i kako se to može rešiti. Microsoft je uklonio mnoge poruke koje su se pojavile pre nego što su korisnici imali priliku da izvrše svoje zadatke i reše probleme, poput nepotpune poruke o detaljima.
- Nova stranica koja specificira koja polja su obavezna za vašu organizaciju, koja su neobavezna i koja polja ne treba snimati. Ova stranica pomaže u smanjenju broja polja koja korisnici moraju postaviti.
- Novi izgled i utisak za izveštaje o troškovima, tako da izveštaji više ne izgledaju kao da su dizajnirani za računovođe.

Da biste uključili novo iskustvo, koristite radni prostor **Upravljanje funkcijama** da biste uključili funkciju **Redizajnirani izveštaji o troškovima**. Kada uključite ovu funkciju, dešavaju se sledeće radnje:

- Postojeći radni prostor za troškove se zamenjuje novim radnim prostorom.
- Dodata je nova stavka menija za vidljivost polja troškova.
- Ne uklanjaju se postojeće stavke menija za izveštaje o troškovima (postojeća stranica) ili polja izveštaja o troškovima.
- Tokovi posla i sva odobrenja vas i dalje vode na postojeću stranicu sa izveštajima o troškovima.

## <a name="getting-started-video-for-new-users"></a>Video sa prvim koracima za nove korisnike

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

Video [Iskustvo troškova u usluzi Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) (prikazan gore) uključen je u [Finance and Operations plejlistu](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) dostupnu na YouTube-u.

## <a name="new-features"></a>Nove funkcije

| Nova funkcija | Opis |
|---|----|
| Vidljivost polja troškova | Nova stranica za podešavanje omogućava vam da odredite koja polja treba da budu onemogućena za organizaciju, koja polja treba da budu obavezna i koja se polja preporučuju. |
| Obavezna polja | Nova jednostavna konfiguracija omogućava vam da napravite neka polja obavezna bez upotrebe okvira smernica. |
| Opcionalna polja | Dodata je druga stranica za opcionalna polja. Na taj način se zaposleni neće osećati kao da moraju da postave polja, ali polja su i dalje lako dostupna. |
| Dodajte nepriložene priznanice | Mogućnost dodavanja nepriloženih priznanica u izveštaj o troškovima vidljivija je iz radnog prostora i u izveštaju o troškovima. |
| Poboljšana razmena poruka | Postoji bolja vidljivost stavki troškova koje sadrže upozorenja ili greške. |
| Smanjivanje broja poruka na traci sa porukama| Smanjen je broj Infolog poruka i učinjen je napor da se u mnogim slučajevima spreči pojavljivanje dupliranih poruka. |
| Grupisane zajedničke radnje | Interfejs je očišćen dodavanjem novog dugmeta radnji za većinu uobičajenih radnji na nivou stavke i dodatkom dugmeta sa tri tačke (...) za zaglavlje i druge manje učestale radnje. |
| Novi radni prostor za povećanje vidljivosti | Novi radni prostor objedinjuje funkcije i veze koje korisnicima omogućavaju prelazak na različita područja. |
| Dodavanje postojećih troškova i priznanica tokom kreiranja troškova | Kada kreirate izveštaje o troškovima, možete da dodate sve ili izabrane troškove i priznanice. |
| Kalkulator deviznih kurseva | Dodat je kalkulator deviznih kurseva koji vam omogućava izračunavanje deviznog kursa za viševalutne transakcije iz svog džepa. |
| Sačuvajte i dodajte nove stavke troškova | Dugmad **Sačuvaj** i **Novo** su dostupna kada se unose novi troškovi, što vam pomaže da brzo unesete stavke troškova. |
| Bolja vidljivost na podeljene i razvrstane stavke | Razvrstane i podeljene stavke dodaju se direktno na listu troškova radi veće vidljivosti i pomoći će vam da lako utvrdite da li postoje greške sa smernicama ili druge greške. |
| Prikažite priznanice tokom razvrstavanja | Možete prikazivati priznanice tokom razvrstavanja. |

Početno izdanje se fokusira na scenarije unosa troškova. Svaki prikaz izveštaja o troškovima ili scenario odobravanja i dalje će koristiti postojeću stranicu za unos troškova.

Sledeće funkcije su prisutne na postojećoj stranici, ali još uvek nisu na novoj. Te funkcije će biti ponovo predstavljene tokom sledećih nekoliko izdanja:

- Odobrenja
- Odobrenja za dugovanja i mogućnost uređivanja računovodstva
- Više ulaznih tačaka
- Integracija zahteva za putovanje
- Entitet podataka za vidljivost polja troškova
- Stavka za dnevnice
- Tok posla na nivou stavke
- Prelazna podrška davaocu odobrenja
- Napredno razvrstavanje
