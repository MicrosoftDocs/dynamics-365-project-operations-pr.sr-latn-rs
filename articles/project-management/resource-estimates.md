---
title: Finansijske procene vremena resursa na projektima
description: Ova tema pruža informacije o tome kako se izračunavaju finansijske procene za vreme.
author: rumant
manager: Annbe
ms.date: 03/19/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 91156c5cf79af8c66c12b84a6d2b17aa7fe09ed1
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701843"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a>Finansijske procene vremena resursa na projektima

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Finansijske procene za vreme se izračunavaju se na osnovu tri faktora: 

- Tip generičkog ili imenovanog člana tima dodeljen svakom zadatku čvora lista na planu projekta. 
- Vrsta ili složenost posla.
- Širenje angažovanja za dodelu resursa na zadatku. 

Prva dva faktora utiču na jedinični trošak ili stopu naplate dodeljivanja resursa. Jedinični trošak ili stopa naplate dodeljivanja resursa određuju se atributima dodeljenog resursa. Ti atributi uključuju organizacionu jedinicu kojoj resurs pripada i standardnu ulogu resursa. Takođe možete da dodate prilagođene atribute relevantne za vaše poslovanje za resurs, poput standardnog naslova ili nivoa iskustva, i da utiču na jedinične troškove ili obračun zadatka.
Pored atributa resursa, atributi rada, kao što je zadatak, takođe mogu uticati na jediničnu stopu naplate ili stopu troškova zadatka. Na primer, kada su određeni zadaci složeniji, dodeljivanje resursa tim određenim zadacima rezultira većim jediničnim troškovima ili stopom naplate od zadataka koji su manje složeni.   

Treći faktor navodi količinu sati po toj stopi. U slučajevima kada zadatak pokriva dva perioda cena, verovatno je da se troškovi i cena prvog dela dodeljivanja resursa za taj zadatak određuje drugačije od drugog dela zadatka. Procena angažovanja pri svakom dodeljivanju resursa je složena vrednost koja se čuva uz dnevnu raspodelu napora dnevno.

Za detaljna uputstva o tome kako da postavite prilagođene atribute rada i resurse kao aspekte cena i troškova, pogledajte [Pregled aspekata za određivanje cena](../pricing-costing/pricing-dimensions-overview.md).

Finansijska procena za svaku dodelu resursa izračunava se kao **stopa na sat za zadatak pomnožena sa brojem sati.**  Slično proceni angažovanja, finansijska procena troškova i prihoda za svaku dodelu resursa je složena vrednost koja se čuva uz dnevnu raspodelu novčanog iznosa dnevno. 

## <a name="summarizing-financial-estimates-for-time"></a>Rezimiranje finansijskih procena za vreme
Finansijska procena za vreme na zadatku čvora lista predstavlja zbir finansijskih procena svih dodeljivanja resursa za taj zadatak.

Finansijska procena za vreme na rezimeu nadređenog zadatka predstavlja zbir finansijskih procena svih dodeljivanja resursa za taj zadatak. To je procenjena cena rada na projektu. 

![Procene resursa](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Podrazumevana cena koštanja i valuta troškova

Podrazumevana cena koštanja potiče iz cenovnika koji su priloženi ugovornoj jedinici projekta. Valuta cene projekta je uvek valuta ugovorne jedinice projekta. Pri dodeli resursa, finansijska procena troška čuva se u valuti troškova projekta. Ponekad se valuta u kojoj je cena utvrđena u cenovniku razlikuje od valute troškova projekta. U tim slučajevima, aplikacija konvertuje valutu u kojoj je postavljena cena koštanja u valutu projekta. Na mreži **Procene**, sve procene troškova se prikazuju i rezimiraju u valuti troškova projekta. 

## <a name="default-bill-rate-and-sales-currency"></a>Podrazumevana stopa naplate i prodajna valuta

Podrazumevana prodajna cena dolazi iz cenovnika projekta koji su priloženi povezanom ugovoru o projektu ako je pogodba dobijena ili iz povezane ponude za projekat ako je posao još uvek u fazi pretprodaje. Valuta prodajne cene projekta je uvek valuta ponude za projekat ugovora o projektu. Pri dodeli resursa, finansijska procena prodaje čuva se u valuti prodajne cene u projektu. Za razliku od troškova, prodajna cena koja se postavlja u cenovniku nikada se ne može razlikovati od valute prodajne cene u projektu. Ne postoji scenario u kojem je potrebna konverzija valuta. Na mreži **Procene**, sve procene prodaje se prikazuju i rezimiraju u valuti prodajne cene u projektu. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
