---
title: Automatizacija projektne usluge za planiranje procesa planiranje projektnih operacija
description: Ovaj članak pruža pregled promena funkcija za Microsoft Dynamics 365 Project Service Automation Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/07/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 84a40fcc9a8561c4ade0be175b08f701f3196508
ms.sourcegitcommit: 28004d38800782540fa5642d41f8fe0f6e2d9fa5
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/08/2022
ms.locfileid: "9642586"
---
# <a name="project-service-automation-to-project-operations-project-scheduling-conversion-process"></a>Automatizacija projektne usluge za planiranje procesa planiranje projektnih operacija

Nakon uspešne nadogradnje projekta sa Microsoft Dynamics 365 Project Service Automation 3.X Dynamics 365 Project Operations na Lite, uređivanje projektnih zadataka u strukturi analize rada koordinatne mreže zadataka (WBS) nije moguće. Klijenti će moći da pregledaju WBS-ove u mreži za praćenje gde su dodata nova polja da bi pružili sve detalje koji su povezani sa zadatkom. Za projekte u kojima je potrebno uređivanje u WBS možete selektivno da konvertujete projekte koji ispunjavaju uslove u novi Projekat za iskustvo web planiranje.

## <a name="project-conversion-process"></a>Proces konverzije projekta

Da biste konvertovali projekat, sledite ove korake.

1. Otvorite glavnu stranicu projekta i u oknu za radnje izaberite **stavku** Konvertuj.
1. U okviru sa porukom o potvrdi kliknite na dugme U **redu** da biste započeli konverziju projekta. Dešavaju se sledeće radnje:

    1. Na traci sa porukama koja se pojavljuje na glavnoj stranici projekta navodi se: "Plan projekta se konvertuje. Ne možete da menjate projekat dok se konverzija ne dovrši."
    1. Preusmereni ste na listu projekata.

    Nakon završetka konverzije projekta, dešavaju se sledeće radnje:

    1. Dodeljeni menadžer projekta dobija obaveštenje sa desne strane aplikacije.
    1. Traka sa porukama na kojoj se navodi da je konverzija u toku je uklonjena.
    1. Kartica **"** Raspored" prikazuje novo iskustvo sa planiranjem sa projektom za Web. Svaki korisnik koji ima odgovarajuće licence i bezbednosne uloge može da uređuje WBS.
    1. Polje **mašina za planiranje je** ažurirano u Projekat **za Veb**.
    1. Dugme " **Konvertuj** " se uklanja iz okna za radnje.

> [!IMPORTANT]
> Masovna konverzija projekata nije dozvoljena. Svaki pokušaj ažuriranja velikog obima projekata u isto vreme biće ugušen. Ovo ograničenje pomaže da se obezbede visoke performanse za sve kupce.

## <a name="manual-tasks-vs-automatic-tasks"></a>Ručni zadaci u odnosu na automatske zadatke

Kada se okruženje nadogradi sa automatizacije projektne usluge na operacije projekta, svi zadaci u WBS-u se smatraju automatski planiranim. Koncept ručno planiranih zadataka nije dostupan u projektu za Web. Međutim, možete da definišete željeno ponašanje planiranje za projekte [pomoću postavke režima za planiranje](/project-management/scheduling-modes.md) prilikom kreiranja novih projekata.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Ograničene operacije za projekte pre konverzije

Ovaj odeljak prikazuje funkcionalne razlike koje možete očekivati kada projekti nisu konvertovani.

### <a name="copy-project"></a>Kopiraj projekat

Operacija **Kopiranje** je podržana samo u konvertovanim projektima. Nadograđene projekte nije bilo kopirati pre konverzije.

### <a name="move-project"></a>Premesti projekat

Promena datuma početka projekta neće proporcionalno pomeriti početak zadataka ukoliko projekat nije konvertovan.

## <a name="frequently-asked-questions"></a>Najčešća pitanja

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Koje su razlike između konvertovanja projekata i novih projekata koji se kreiraju nakon završetka nadogradnje?

Za projekte koji se konvertuju nakon nadogradnje okruženja biće postavljena zastavica koja nalaže rasporedu da poštuje samo kalendar projekta. Ovo ponašanje se podudara sa ponašanjem u automatizaciji usluge projekta. Međutim, zastavica neće biti postavljena za nove projekte koji su kreirani nakon nadogradnje. Zbog toga će raspored poštovati radno vreme resursa kada su dodeljeni zadatku.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Šta treba da uradim ako projekat ne uspe da se konvertuje?

Ako projekat ne uspe da se konvertuje, prvi korak je da pregledate evidencije grešaka da biste identifikovali sve uobičajene probleme koji su povezani sa WBS-om. Ako evidencije ne ukazuju na određenu grešku na koju možete da preduzmete radnju, obratite se korisničkoj podršci kako bi vaš predmet mogao dodatno da se pregleda.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Kako se rešavaju poslovna zatvaranja u Projektu za web?

Projekat za Web ne poštuje poslovna zatvaranja koja preduzeće definiše na nivou organizacije. Međutim, poštovaće druge vrste slobodnih dana koji su definisani u datom predlošku radnog sata.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Koja su ograničenja projekta za Web?

Pogledajte [članak Kreiranje strukture nervnog sloma rada: Ograničenja projekta](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Da li mogu da očekujem promene u proceni troškova i prodaje?

U retkim slučajevima kada se konture dodeljivanje resursa ponovo izračunaju ili kada padaju na drugoj granici datuma od izvornog projekta, možda ćete videti razlike u proceni prodaje i troškova. U sklopu procesa nadogradnje, od klijenata se očekuje da testiraju reprezentativni set projekata uzoraka kako bi mogli da razumeju sve potencijalne promene rasporeda.
