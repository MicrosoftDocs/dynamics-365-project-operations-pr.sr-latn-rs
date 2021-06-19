---
title: Upravljanje procenama prihoda
description: U ovoj temi se pružaju informacije o tome kako da radite sa procenama prihoda za projekte.
author: sigitac
ms.date: 11/04/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e3cbaff18d8bd4d6f6a7577bba25b3e843b1757e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013864"
---
# <a name="manage-revenue-estimates"></a>Upravljanje procenama prihoda

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Možete da kreirate, izračunate, objavite, stornirate ili eliminišete procene prihoda. To možete učiniti ručno ili periodičnim procesom. U ovoj temi se pružaju informacije o tome kako da radite sa procenama prihoda za projekte.

### <a name="manage-revenue-estimates-manually"></a>Ručno upravljanje procenama prihoda

Na projektu sa procenom prihoda sa fiksnom cenom ili stranici **Upit za procenu** (**Upravljanje projektima i računovodstvo** > **Izveštaji i upiti** > **Procene upita i izveštaja**), izaberite **Procene**.

### <a name="manage-revenue-estimates-using-a-periodic-process"></a>Upravljanje procenama prihoda koristeći periodični proces

Idite na **Upravljanje projektima i računovodstvo** > **Periodično** > **Procene** i izaberite odgovarajući postupak.

## <a name="create-a-revenue-estimate"></a>Kreiranje procene prihoda

Dovršite sledeće korake kako biste kreirali procenu prihoda. 

1. Idite na **Upravljanje projektima i računovodstvo** > **Periodično** > **Procene**.
2. Izaberite **Novo**. Na stranici **Kreiranje procene**, izaberite sledeće parametre:

   - **Kôd perioda**: ovaj kôd određuje koliko često se objavljuju procene.
   - **Datum procene**: datum obrade procene.
   - **Kontinuirano**: izaberite ovo polje za potvrdu da biste kreirali procene samo ako su procene objavljene u prethodnom periodu ili ako procena predstavlja prvu procenu koja je kreirana. Ako ovo nije izabrano, procene se kreiraju čak i ako procene nisu objavljene u prethodnom periodu.
   - **Metod troškova za dovršetak**: definišite kako da procenite preostali rad na projektu. Za više informacija pogledajte [Metode troška za dovršetak](cost-complete-methods.md).
   - **Metod dovršetka**: izaberite metod dovršetka između sledećih opcija:
     - **Automatski**: procenat dovršenja izračunava se automatski i na osnovu linija troškova uključenih u izračunavanje. Predložak troškova definiše linije troškova koje su uključene.
     - **Ručno**: procenat dovršenja jednak je procentu dovršenja poslednje procene. Nakon što kreirate procenu, možete da promenite **Ručno izračunavanje** na stranici **Procene**.
     - **Iz predloška troškova**: kombinacija automatskih i ručnih metoda. Ova opcija se postavlja automatski ili ručno, u zavisnosti od podrazumevane vrednosti u predlošku troškova.
   - **Model predviđanja**: izaberite model predviđanja za procenu.
   - **Štampajte listu procena**: kreirajte i prikažite listu procena. Lista sadrži status trenutne funkcije. Sva upozorenja o proceni možete da odštampate na izveštaju. Sledeći uslovi dovode do toga da se upozorenja pojavljuju na listi procena:
     - Procenat dovršenja veći od 100 procenata.
     - Procenat dovršenja manji od nula procenata.
     - Negativan iznos u koloni **Do dovršetka**.
     - Procena bez odgovarajućeg ugovornog iznosa.
     - Procena bez priložene procene troškova.
   - **Prikaži evidenciju sa informacijama**: izaberite ovu opciju da biste dobili poruku koja sadrži informacije o procenjenim projektima koji su obrađeni prilikom izvršavanja posla.


## <a name="post-wip-or-accruals"></a>Knjiženje WIP-a ili prirasta

Nakon ocenjivanja procene, one se održavaju, smanjuju ili povećavaju. Tada možete proknjižiti WIP kada radite sa principom procene **Dovršenja ugovora** ili knjižite priraste kada radite sa principom procene **Procenat dovršenja**.
  
Status perioda procene se menja iz **Kreirano** u **Proknjiženo**.

## <a name="reverse-wip-or-accruals"></a>Storniranje WIP ili prirasta

Koristite opciju storniranja za kreditiranje već proknjiženih WIP-ova ili prirasta, a zatim kreirajte procene za period.

> [!NOTE]
> Da biste stornirali period koji je između ostalih perioda, stornirajte neophodne periode procene, a zatim ih ponovo proknjižite. Pošto svi naredni periodi zavise od procena iz prethodnog perioda, nemojte preskakati nijedan period.

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a>Otklonite projekat procene i završite projekat

Završni korak u procesu procene je uklanjanje projekta procene i završetak projekta sa fiksnom cenom kada procenat dovršenja dostigne 100 procenata.

Sledeće se dešava kada pokrenete eliminaciju:

- Za projekat sa fiksnom cenom sa završenim ugovorom, vrednosti WIP-a se brišu sa konta bilansa i knjiže na konta dobiti i gubitka.
- Za projekat sa fiksnom cenom sa procentom dovršenja, obračunska vremenska razgraničenja uklanjaju se sa konta dobiti i gubitka.

Procena menja status u **Eliminisano**.

> [!NOTE]
> U posebnim slučajevima, procenat može da premaši 100 procenata. Kada se to desi, smanjite procenat dovršenja pomoću **Metode podešavanja troška za dovršenja na nulu** da biste dostigli 100 posto.

## <a name="reverse-elimination"></a>Eliminacija storniranjem

1. Idite na **Upravljanje projektima i računovodstvo** > **Periodično** > **Procene** > **Eliminacija storniranjem**. 
2. Na oknu Radnja, na kartici **Proces**, u grupi **Uspostavljanje**, izaberite **Procena**. 
3. Izaberite **Eliminacija storniranjem**.

Koristite ovu stranicu za storniranje svih eliminacija sa navedenim datumom procene i sa statusom procene **Eliminisan**. Status transakcije se menja nakon što izaberete odgovarajuća polja.

Ovo takođe automatski menja status projekta u **U procesu** ako je faza projekta postavljena na dovršeno. Procenjeni status projektnog perioda se vraća na **Proknjiženo**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]