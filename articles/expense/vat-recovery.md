---
title: Povraćaj PDV u upravljanju troškovima
description: Ova tema objašnjava kako da dobijete povraćaj sredstava za prihvatljive transakcije poreza na dodatu vrednost (PDV).
author: suvaidya
ms.date: 10/10/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 64e9f4091fdf40cc702e83a165fe0a5be5043359348210bbe4afcd8a18055133
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999378"
---
# <a name="vat-recovery-in-expense-management"></a>Povraćaj PDV u upravljanju troškovima

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Da bi primila povraćaj sredstava za prihvatljive transakcije poreza na dodatu vrednost (PDV), kompanija ili organizacija mora identifikovati, prikupiti, verifikovati i dostaviti tačne informacije. Ovaj proces uključuje više zadataka i, u zavisnosti od veličine vašeg preduzeća, može uključivati nekoliko zaposlenih ili uloga.

Da biste povratili PDV u modulu **Upravljanje troškovima**, morate se ispuniti sledeće preduslove:

- Šifre poreza se moraju kreirati za zemlje/regione koji su raspoređeni u kategorije troškova.
- Grupa poreza na promet se mora kreirati za svaku šifru poreza.
- Šifra poreza na promet proizvoda se mora kreirati za svaku grupu poreza na promet.

Nakon ispunjavanja preduslova, moraju se izvršiti sledeći koraci za traženje povraćaja za transakcije sa PDV-om.

1. U izveštaju o troškovima unesite poreske informacije o transakcijama kreditnim karticama da biste identifikovali prihvatljiv povraćaj PDV-a.
2. Proverite da li su sve poreske informacije kompletne, a zatim proknjižite izveštaj o troškovima.
3. Obradite troškove koji ispunjavaju uslove za međunarodni povraćaj PDV-a.
4. Pošaljite podatke o povraćaju PDV-a nezavisnom dobavljaču da podnesu međunarodne prijave za povraćaj.
5. Obradite troškove za povraćaj domaćeg PDV.

Sledeći odeljci pružaju primere koji pokazuju kako zaposleni u kompaniji Contoso završavaju svaki korak.

## <a name="enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Unesite poreske informacije o transakcijama kreditnim karticama da biste identifikovali prihvatljiv povraćaj PDV-a

Radmila, predstavnik Contoso prodaje sa sedištem u Sjedinjenim Državama, nedavno se vratila sa prodajnog putovanja u Ujedinjeno Kraljevstvo. Tokom putovanja, Radmila je napravila neke lične troškove za obroke sa kreditne kartice. Radmila sada mora da sačini izveštaj o troškovima kako bi uskladila troškove.

Kada Radmila unese informacije u izveštaj o troškovima, ona bira **Ujedinjeno Kraljevstvo** u polju **Zemlja/region** na stranici **Uređivanje izveštaja o troškovima**. Lista grupa poreza na promet se zatim filtrira tako da prikazuje samo grupe koje se odnose na Ujedinjeno Kraljevstvo. Radmila bira grupu poreza na promet **Ujedinjeno Kraljevstvo 001**, a zatim bira grupu poreza na promet proizvoda **Obroci**. Zatim, Radmila dodaje novu transakciju za smeštaj. Budući da u Ujedinjenom Kraljevstvu postoji samo jedna grupa poreza na promet i jedna grupa poreza na promet proizvoda, ove informacije se automatski popunjavaju u Radmilinom izveštaju o troškovima.

Prema smernicama kompanije Contoso, svi troškovi moraju imati odgovarajući račun. Stoga, kada Radmila sačuva izveštaj o troškovima, ona dobija poruku u kojoj se navodi da mora priložiti priznanicu za svaku transakciju koju je navela u svom izveštaju o troškovima. Radmila potvrđuje da je svom izveštaju o troškovima priložila digitalnu sliku svake priznanice o transakciji, a zatim svoj izveštaj podnosi na odobrenje. Zatim šalje papirne priznanice pozadinskom timu za obradu. Ovaj tim će poslati podatke o povraćaju PDV nezavisnom dobavljaču koji podnosi međunarodne prijave za povraćaj PDV za kompaniju Contoso.

## <a name="verify-tax-information-and-post-an-expense-report"></a>Potvrđivanje poreske informacije i knjiženje izveštaja o troškovima

Da bi Ana, koordinatorka za dugovanja za Contoso, mogla da objavi izveštaj o troškovima, ona mora da unese sve informacije o porezu koje joj nedostaju. Ona otvara stranicu **Detalji izveštaja o troškovima** i vidi Radmilin izveštaj o troškovima. Ana zatim otvara izveštaj o troškovima da bi videla detalje transakcija. Ona vidi da Radmila nije unela grupu poreza na promet proizvoda za jednu od transakcija. Pošto te informacije nisu navedene, Ana ne može da proknjiži izveštaj o troškovima. Stoga, ona pregleda stranicu **Konfiguracije poreza** u upravljanju troškovima i pronalazi odgovarajuću grupu poreza na promet proizvoda za zemlju/region i tip transakcije. Ana sada može da proknjiži izveštaj o troškovima u glavnu knjigu.

Kada Ana objavi izveštaj o troškovima, kreira se radna stavka za povraćaj PDV. Ova radna stavka se dodeljuje članu pozadinskog tima za obradu. Ana dobija poruku koja potvrđuje da je knjiženje bilo uspešno. U ovoj poruci se navodi i broj transakcija PDV koje su identifikovane za povraćaj.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Obrada troškova koji ispunjavaju uslove za međunarodni povraćaj PDV

Arni, član Contoso tima za obradu u pozadini, odgovoran je za potvrdu da su sve potrebne informacije za povraćaj PDV uključene u izveštaje o troškovima. On otvara stranicu **Povraćaj poreza na troškove** i bira izveštaj o troškovima koji je Radmila podnela. Arni zatim proverava da li su priložene svi potrebne priznanice i da li su unete tačne šifre poreza na promet i poreza na promet proizvoda.

Kada Arni dobije papirne priznanice od Radmile, on ih verifikuje u odnosu na digitalne priznanice, a zatim menja status izveštaja o troškovima u **Spremni za povraćaj**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor"></a>Slanje podataka o povraćaju PDV nezavisnom dobavljaču

Kada Arni bude spreman da pošalje podatke izveštaja o troškovima nezavisnom dobavljaču koji će podneti povraćaj PDV, on otvara stranicu **Povraćaj poreza na troškove**. On filtrira stranicu tako da prikazuje samo izveštaje o troškovima koji su označeni kao **Spremni za povraćaj**. Arni zatim bira **Datoteka** &gt; **Izvezi u Excel**. Informacije o PDV iz izveštaja o troškovima izvoze se u Microsoft Excel radni list. Arni prosleđuje taj radni list nezavisnom dobavljaču i uključuje poruku u kojoj se navodi da su papirne priznanice poslate po kuriru.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Obrada troškove za povraćaj domaćeg PDV

Arni mora da potvrdi da su transakcije izveštaja o troškovima prihvatljive za povraćaj PDV i da su digitalne priznanice priložene uz izveštaje. Da bi započeo da obrađuje prihvatljive troškove za domaći povraćaj, Arni otvara stranicu **Povraćaj poreza na troškove** i bira izveštaj o troškovima koji zahteva verifikaciju. On proverava da li su priznanice na ime preduzeća umesto na zaposlenog. (Za povraćaj PDV, priznanice moraju da budu na ime preduzeća.) Arni zatim proverava da li su unete tačne šifre poreza na promet i poreza na promet proizvoda.

Kada Arni dobije papirne priznanice, on menja status izveštaja o troškovima u **Spremno za povraćaj**. Tada može podneti prijavu za povraćaj odgovarajućem poreskom organu. U tom slučaju, odgovarajuća poreska uprava u Sjedinjenim Državama je Služba unutrašnjih prihoda (IRS).


[!INCLUDE[footer-include](../includes/footer-banner.md)]