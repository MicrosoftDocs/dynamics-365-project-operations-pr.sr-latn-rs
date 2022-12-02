---
title: Proces konverzije sa aplikacije Project Service Automation na Project Operations planiranje projekta
description: Ovaj članak pruža pregled promena funkcija iz usluge Microsoft Dynamics 365 Project Service Automation u Dynamics 365 Project Operations.
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
# <a name="project-service-automation-to-project-operations-project-scheduling-conversion-process"></a>Proces konverzije sa aplikacije Project Service Automation na Project Operations planiranje projekta

Nakon uspešne nadogradnje projekta sa usluge Microsoft Dynamics 365 Project Service Automation 3.X na Dynamics 365 Project Operations jednostavnu primenu, uređivanje projektnih zadataka u strukturnoj analizi posla (WBS) matrice koordinatne mreže zadatka nije moguće. Klijenti će moći da pregledaju WBS-ove u matrici koordinatne mreže za praćenje gde su dodata nova polja da bi pružili sve detalje koji su povezani sa zadatkom. Za projekte u kojima je potrebno uređivanje WBS-a, možete selektivno da konvertujete projekte koji ispunjavaju uslove u novo Project for the web iskustvo planiranja.

## <a name="project-conversion-process"></a>Proces konverzije projekta

Da biste konvertovali projekat, pratite ove korake:

1. Otvorite glavnu stranicu projekta i u oknu Radnja izaberite **Konvertuj**.
1. U okviru sa porukom o potvrdi kliknite na dugme **U redu** da biste započeli konverziju projekta. Dešavaju se sledeće radnje:

    1. Na traci sa porukama koja se pojavljuje na glavnoj stranici projekta navodi se: „Raspored projekta se konvertuje. Ne možete da unosite promene u projekat dok se konverzija ne dovrši.“
    1. Preusmereni ste na listu projekata.

    Nakon završetka konverzije projekta, dešavaju se sledeće radnje:

    1. Dodeljeni menadžer projekta dobija obaveštenje sa desne strane aplikacije.
    1. Traka sa porukama na kojoj se navodi da je konverzija u toku se uklanja.
    1. Kartica **Raspored** prikazuje novo iskustvo sa uslugom Project for the web. Svaki korisnik koji ima odgovarajuće licence i bezbednosne uloge može da uređuje WBS.
    1. Polje **Mehanizam planiranja** je ažurirano u **Project for the web**.
    1. Dugme **Konvertuj** se uklanja iz okna Radnje.

> [!IMPORTANT]
> Masovna konverzija projekata nije dozvoljena. Svaki pokušaj ažuriranja velikog obima projekata u isto vreme biće prigušen. Ovo ograničenje pomaže da se obezbede visoke performanse za sve klijente.

## <a name="manual-tasks-vs-automatic-tasks"></a>Ručni zadaci u odnosu na automatske zadatke

Kada se okruženje nadogradi sa Project Service Automation na Project Operations, svi zadaci u WBS-u se smatraju automatski planiranim. Koncept ručno planiranih zadataka nije dostupan u rešenju Project for the web. Međutim, možete da definišete željeno ponašanje planiranja za projekte pomoću postavke [režima za planiranje](/project-management/scheduling-modes.md) prilikom kreiranja novih projekata.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Ograničene operacije za projekte pre konverzije

Ovaj odeljak prikazuje funkcionalne razlike koje možete očekivati kada projekti nisu konvertovani.

### <a name="copy-project"></a>Kopiranje projekta

Operacija **Kopiranje** je podržana samo u konvertovanim projektima. Nadograđene projekte nije moguće kopirati pre konverzije.

### <a name="move-project"></a>Premeštanje projekta

Promena datuma početka projekta neće proporcionalno pomeriti početak zadataka ukoliko projekat nije konvertovan.

## <a name="frequently-asked-questions"></a>Najčešća pitanja

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Koje su razlike između konvertovanih projekata i novih projekata koji se kreiraju nakon završetka nadogradnje?

Za projekte koji se konvertuju nakon nadogradnje okruženja, biće postavljena zastavica koja nalaže da raspored poštuje samo kalendar projekta. Ovo ponašanje se podudara sa ponašanjem u rešenju Project Service Automation. Međutim, zastavica neće biti postavljena za nove projekte koji su kreirani nakon nadogradnje. Zbog toga će raspored poštovati radno vreme resursa kada su dodeljeni zadatku.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Šta treba da uradim ako projekat ne uspe da se konvertuje?

Ako projekat ne uspe da se konvertuje, prvi korak je da pregledate evidencije grešaka da biste identifikovali sve uobičajene probleme koji su povezani sa WBS-om. Ako evidencije ne ukazuju na određenu grešku za koju možete da preduzmete radnju, obratite se korisničkoj podršci kako bi dalje pregledali vaš predmet.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Kako se rešavaju prekidi poslovnih aktivnosti u rešenju Project for the web?

Project for the web ne poštuje prekide poslovnih aktivnosti koje preduzeće definiše na nivou organizacije. Međutim, poštovaće druge vrste slobodnih dana koji su definisani u datom predlošku radnih sati.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Koja su ograničenja programa Project for the web?

Pogledajte [Kreiranje strukturne analize posla: ograničenja projekta](/project-management/create-wbs#project-limitations.md)

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Da li mogu da očekujem promene u proceni troškova i prodaje?

U retkim slučajevima kada se konture dodele resursa ponovo izračunaju ili kada padaju na drugoj granici datuma od izvornog projekta, možda ćete videti razlike u proceni prodaje i troškova. U sklopu procesa nadogradnje, od klijenata se očekuje da testiraju reprezentativni set primera projekata kako bi mogli da razumeju sve potencijalne promene rasporeda.
