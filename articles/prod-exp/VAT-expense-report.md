---
title: Povraćaj PDV-a
description: Ova tema objašnjava kako da vratite povraćaj sredstava za transakcije poreza na dodatu vrednost (PDV).
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1be96521cdb486dd5a702cded615d3e1015b364
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083622"
---
# <a name="vat-recovery"></a>Povraćaj PDV-a 

[!include [banner](../includes/banner.md)]

Da bi primila povraćaj sredstava za prihvatljive transakcije poreza na dodatu vrednost (PDV), kompanija ili organizacija mora identifikovati, prikupiti, verifikovati i dostaviti tačne informacije. Ovaj proces uključuje više zadataka i, u zavisnosti od veličine vašeg preduzeća, može uključivati nekoliko zaposlenih ili uloga.

Da biste povratili PDV koristeći Upravljanje troškovima, morate ispuniti sledeće preduslove:

- Šifre poreza se moraju kreirati za zemlje/regione koji su raspoređeni u kategorije troškova.
- Grupa poreza na promet se mora kreirati za svaku šifru poreza.
- Šifra poreza na promet proizvoda se mora kreirati za svaku grupu poreza na promet.

Nakon ispunjavanja preduslova, zaposleni moraju izvršiti sledeće korake za traženje povrata za transakcije sa PDV-om.

1. U izveštaju o troškovima unesite poreske informacije o transakcijama kreditnim karticama da biste identifikovali prihvatljiv povraćaj PDV-a.
2. Proverite da li su sve poreske informacije kompletne, a zatim proknjižite izveštaj o troškovima.
3. Obradite troškove koji ispunjavaju uslove za međunarodni povraćaj PDV-a.
4. Pošaljite podatke o povraćaju PDV-a nezavisnom dobavljaču da podnesu međunarodne prijave za povraćaj.
5. Obradite troškove za povraćaj domaćeg PDV.

Sledeći odeljci pružaju primere koji pokazuju kako zaposleni u kompaniji Contoso završavaju svaki korak.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>U izveštaju o troškovima unesite poreske informacije o transakcijama kreditnim karticama da biste identifikovali prihvatljiv povraćaj PDV-a

Radmila, predstavnica prodaje kompanije Contoso sa sedištem u Sjedinjenim Državama, nedavno se vratila sa prodajnog putovanja u Ujedinjeno Kraljevstvo. Tokom putovanja, napravila je neke lične troškove za obroke sa kreditne kartice. Radmila sada mora da sačini izveštaj o troškovima kako bi uskladila troškove.

Kada Radmila unese informacije u izveštaj o troškovima, ona bira **Ujedinjeno Kraljevstvo** u polju **Zemlja/region** na stranici **Uređivanje izveštaja o troškovima**. Lista grupa poreza na promet se zatim filtrira tako da prikazuje samo grupe koje se odnose na Ujedinjeno Kraljevstvo. Radmila bira grupu poreza na promet **Ujedinjeno Kraljevstvo 001** , a zatim bira grupu poreza na promet proizvoda **Obroci**. Zatim, ona dodaje novu transakciju za smeštaj. Budući da u Ujedinjenom Kraljevstvu postoji samo jedna grupa poreza na promet i jedna grupa poreza na promet predmeta, ove informacije se automatski popunjavaju u Radmilinom izveštaju o troškovima.

Prema smernicama kompanije Contoso, svi troškovi moraju imati odgovarajuću priznanicu. Stoga, kada Radmila sačuva izveštaj o troškovima, ona dobija poruku u kojoj se navodi da mora priložiti priznanicu za svaku transakciju koju je navela u svom izveštaju o troškovima. Radmila potvrđuje da je svom izveštaju o troškovima priložila digitalnu sliku svake priznanice o transakciji, a zatim svoj izveštaj podnosi na odobrenje. Zatim šalje papirne priznanice pozadinskom timu za obradu. Ovaj tim će poslati podatke o povraćaju PDV nezavisnom dobavljaču koji podnosi međunarodne prijave za povraćaj PDV za Contoso.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Proverite da li su sve poreske informacije kompletne, a zatim proknjižite izveštaj o troškovima

Ana, koordinator za obaveze za Contoso, mora uneti sve poreske informacije koje nedostaju u izveštaju o troškovima pre nego što izveštaj može biti proknjižen. Ona otvara stranicu **Detalji izveštaja o troškovima** i vidi Radmilin izveštaj o troškovima. Ana zatim otvara izveštaj o troškovima da bi videla detalje transakcija. Ona vidi da Radmila nije unela grupu poreza na promet proizvoda za jednu od transakcija. Pošto te informacije nisu navedene, Ana ne može da proknjiži izveštaj o troškovima. Stoga, Ana gleda stranicu **Poreske konfiguracije** u odeljku Upravljanje troškovima i pronalazi odgovarajuću grupu poreza na promet stavki za zemlju/region i vrstu transakcije. Ana sada može da proknjiži izveštaj o troškovima u glavnu knjigu.

Kada Ana objavi izveštaj o troškovima, kreira se radna stavka za povraćaj PDV. Ova radna stavka se dodeljuje članu pozadinskog tima za obradu. Ana dobija poruku koja potvrđuje da je knjiženje bilo uspešno. U ovoj poruci se navodi i broj transakcija PDV koje su identifikovane za povraćaj.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Obrada troškova koji ispunjavaju uslove za međunarodni povraćaj PDV

Arni, član tima kompanije Contoso za pozadinsku obradu, odgovoran je za potvrdu da su sve potrebne informacije za povraćaj PDV uključene u izveštaje o troškovima. On otvara stranicu **Povraćaj poreza na troškove** i bira izveštaj o troškovima koji je Radmila podnela. Arni proverava da li su priložene svi potrebne priznanice i da li su unete tačne šifre poreza na promet i poreza na promet proizvoda.

Kada Arni dobije papirne priznanice od Radmile, on ih verifikuje u odnosu na digitalne priznanice, a zatim menja status izveštaja o troškovima u **Spremni za povraćaj**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>Pošaljite podatke o povraćaju PDV-a nezavisnom dobavljaču da podnesu međunarodne prijave za povraćaj

Kada Arni bude spreman da pošalje podatke izveštaja o troškovima nezavisnom dobavljaču koji će podneti povraćaj PDV, on otvara stranicu **Povraćaj poreza na troškove**. On filtrira stranicu tako da prikazuje samo izveštaje o troškovima koji su označeni kao **Spremni za povraćaj**. Arni zatim bira **Datoteka** &gt; **Izvezi u Excel**. Informacije o PDV iz izveštaja o troškovima izvoze se u Microsoft Excel radni list. Arni prosleđuje taj radni list nezavisnom dobavljaču i uključuje poruku u kojoj se navodi da su papirne priznanice poslate po kuriru.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Obrada troškove za povraćaj domaćeg PDV

Arni mora da potvrdi da su transakcije izveštaja o troškovima prihvatljive za povraćaj PDV i da su digitalne priznanice priložene uz izveštaje. Da bi započeo da obrađuje prihvatljive troškove za domaći povraćaj, Arni otvara stranicu **Povraćaj poreza na troškove** i bira izveštaj o troškovima koji zahteva verifikaciju. On proverava da li su priznanice na ime preduzeća umesto na zaposlenog. Za povraćaj PDV-a, priznanice moraju biti na ime kompanije. Arni zatim potvrđuje da je primenjena tačna grupa zakona o porezu na prodaju i zakoni o porezu na promet.

Kada Arni dobije papirne priznanice, on menja status izveštaja o troškovima u **Spremno za povraćaj**. Tada može podneti prijavu za povraćaj odgovarajućem poreskom organu. U tom slučaju, odgovarajuća poreska uprava u Sjedinjenim Državama je Služba unutrašnjih prihoda (IRS).
