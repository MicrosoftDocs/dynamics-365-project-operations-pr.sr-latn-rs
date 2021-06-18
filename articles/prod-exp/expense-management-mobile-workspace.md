---
title: Mobilni radni prostor za upravljanje troškovima
description: Ova tema pruža informacije o mobilnom radnom prostoru za upravljanje troškovima. Ovaj radni prostor omogućava korisnicima da nađu i otpreme priznanicu, kako bi kasnije mogli da je prilože u izveštaju o troškovima. Korisnici takođe mogu brzo da kreiraju liniju troškova koristeći priloženu priznanicu i kreiraju izveštaje o troškovima i upravljaju njima.
author: suvaidya
ms.date: 12/01/2017
ms.topic: article
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 7eccf5cd234df6ca4fc4c83b581f6c4c22b3396f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993658"
---
# <a name="expense-management-mobile-workspace"></a>Mobilni radni prostor za upravljanje troškovima

Ova tema pruža informacije o mobilnom radnom prostoru za **Upravljanje troškovima**. Ovaj radni prostor omogućava korisnicima da nađu i otpreme priznanicu, kako bi kasnije mogli da je prilože u izveštaju o troškovima. Korisnici takođe mogu brzo da kreiraju liniju troškova koristeći priloženu priznanicu i kreiraju izveštaje o troškovima i upravljaju njima. Pored toga, davaoci odobrenja mogu da koriste mobilni radni prostor za **Upravljanje troškovima** za pregled izveštaja o troškovima koji su im dodeljeni i odobravanje ili odbijanje tih izveštaja o troškovima.


Ovaj mobilni radni prostor je namenjen za upotrebu zajedno sa Dynamics 365 Unified Ops aplikacijom za mobilne uređaje.


## <a name="overview"></a>Pregled

Mnoge organizacije zahtevaju da se kopija priznanice priloži uz izveštaj o troškovima povezanim sa putovanjem ili poslovnim odnosom koji zaposleni podnosi na nadoknadu. Mobilni radni prostor za **Upravljanje troškovima** omogućava korisnicima da brzo kreiraju nove linije troškova na mobilnom uređaju po svom izboru, koristeći priloženu fotografiju priznanice. Takođe, korisnici mogu snimiti fotografiju priznanice, a zatim da je kasnije prilože u izveštaju o troškovima. Zaposleni takođe mogu da kreiraju izveštaje o troškovima i upravljaju njima, i da ih, zatim, podnesu na odobrenje i nadoknadu pomoću mobilnog uređaja.


Konkretno, mobilni radni prostor za **Upravljanje troškovima** omogućava korisnicima da izvršavaju ove zadatke:

- Fotografišite priznanicu i otpremite ga u Dynamics 365 Finance. Ovu fotografiju možete kasnije da priložite izveštaju o troškovima.
- Otpremite datoteku kao snimljenu priznanicu. Ovu datoteku možete kasnije da priložite izveštaju o troškovima.
- Napravite novu liniju troškova koristeći priloženu priznanicu. Zatim možete kasnije dodati stavku u izveštaj o troškovima i predati je na odobrenje i nadoknadu.

Takođe možete da koristite ove funkcije:

- Kreirajte novi izveštaj o troškovima.
- Transakcije kreditnim karticama i druge prethodno stvorene troškove priložite u izveštaju o troškovima.
- Napravite nove troškove za izveštaj o troškovima.
- Priložite priznanicu uz bilo koji trošak za izveštaj o troškovima, bilo fotografisanjem priznanice ili učitavanjem datoteke kao snimljene potvrde.
- U zavisnosti od politike troškova kompanije, dodajte listu gostiju na trošak.
- U zavisnosti od politike troškova kompanije, podelite troškove.
- Podnesite izveštaj o troškovima na odobrenje i nadoknadu.
- Odobrite ili odbijte izveštaje o troškovima za koje ste dodeljeni davalac odobrenja.

## <a name="prerequisites"></a>Preduslovi
Preduslovi se razlikuju, na osnovu verzije koja je primenjena za vašu organizaciju.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Preduslovi ako koristite Dynamics 365 Finance 
Ako je u vašoj organizaciji primenjena aplikacija Finance, administrator sistema mora da objavi mobilni radni prostor za **Upravljanje troškovima**. Za uputstva pogledajte [Objavljivanje mobilnih radnih prostora](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Preduslovi ako koristite verziju 1611 sa ispravkom 3 platforme ili novijom
Ako je za vašu organizaciju primenjena verzija 1611 sa ispravkom 3 platforme ili novijom, administrator sistema mora da ispuni sledeće preduslove. 

<table>
<thead>
<tr class="header">
<th>Preduslov</th>
<th>Uloga</th>
<th>Opis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Primena KB 4019015.</td>
<td>Administrator sistema</td>
<td>KB 4019015 je hitna ispravka za X++ ispravku ili metapodatke koja sadrži mobilni radni prostor za <strong>Upravljanje troškovima</strong>. Da bi primenio KB 4019015, administrator sistema mora slediti ove korake.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#download-the-hotfix-from-lcs">Preuzmite hitnu ispravku za metapodatke iz usluge Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#install-the-metadata-hotfix-package">Instalirajte hitnu ispravku za metapodatke</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Kreirajte paket koji se može primeniti</a> koji sadrži modele <strong>ApplicationSuite</strong> i <strong>ExpenseMobile</strong>, a zatim otpremni paket koji se može primeniti na LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Primenite paket koji se može primeniti</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Objavite mobilni radni prostor za <strong>Upravljanje troškovima</strong>.</td>
<td>Administrator sistema</td>
<td>Pogledajte <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Objavljivanje mobilnog radnog prostora</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Preuzmite i instalirajte Dynamics 365 for Operations aplikaciju za mobilne uređaje
Preuzmite i instalirajte Dynamics 365 Unified Ops aplikaciju za mobilne uređaje:

- [Za Android telefone](https://go.microsoft.com/fwlink/?linkid=850662)
- [Za iPhone uređaje](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Prijavite se u aplikaciju za mobilne uređaje
1. Pokrenite aplikaciju na mobilnom uređaju.
2. Unesite svoj Dynamics 365 URL.
4. Kada se prvi put prijavite, od vas će se zatražiti korisničko ime i lozinka. Unesite akreditive.
5. Kada se prijavite, prikazuju se dostupni radni prostori za vašu kompaniju. Imajte na umu da ako administrator sistema kasnije objavi novi radni prostor, moraćete da osvežite listu mobilnih radnih prostora.


[![Povucite da osvežite](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Snimite priznanicu pomoću mobilnog radnog prostora za Upravljanje troškovima

1. Na mobilnom uređaju otvorite radni prostor za **Upravljanje troškovima**.
2. Izaberite **Snimite priznanicu**.
3. Izaberite **Snimite fotografiju** ili **Odaberite sliku**.
4. Pratite jedan od sledećih koraka:

    - Ako ste izabrali **Snimite fotografiju**, pratite ove korake:

        1. Bićete preusmereni na kameru na svom mobilnom uređaju, tako da možete da fotografišete priznanicu. Kada završite sa fotografisanjem, izaberite **U redu** da biste prihvatili fotografiju.
        2. Opcionalno: unesite naziv fotografije i unesite beleške.

    - Ako ste izabrali **Odaberite sliku**, pratite ove korake:

        1. Izaberite sliku sa liste.
        2. Opcionalno: unesite naziv slike i unesite beleške.

5. Izaberite **Gotovo**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Brzo snimite troškove pomoću mobilnog radnog prostora za Upravljanje troškovima
1. Na mobilnom uređaju otvorite radni prostor za **Upravljanje troškovima**.
2. Izaberite **Brzi unos troškova**.
3. Izaberite kategoriju troška. Videćete listu kategorija troškova koje su učitane u vašu aplikaciju za korišćenje van mreže. Podrazumevano se učitava 50 stavki, ali programer može promeniti ovaj broj. Za više informacija, programeri bi trebalo da pogledaju članak [Mobilna platforma](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Ako vaša kategorija nije na listi, izaberite **Pretraga** da biste obavili pretragu na mreži. Pretražujte po kategoriji troška ili se prebacite na pretragu po vrsti troška.
4. Unesite datum transakcije troška.
5. Opcionalno: unesite trgovca za trošak.
6. Unesite iznos troška.
7. Izaberite valutu troška. Videćete listu šifara valuta koje su učitane u vašu aplikaciju za korišćenje van mreže. Podrazumevano se učitava 400 valuta, ali programer može promeniti ovaj broj. Za više informacija, programeri bi trebalo da pogledaju članak [Mobilna platforma](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Ako vaša valuta nije na listi, izaberite **Pretraga** da biste obavili pretragu na mreži. Pretražujte po valuti ili se prebacite na pretragu po nazivu.
8. Izaberite **Snimite fotografiju** ili **Odaberite sliku**.
9. Pratite jedan od sledećih koraka:

    - Ako ste izabrali **Snimite fotografiju**, bićete preusmereni na kameru na svom mobilnom uređaju, tako da možete da fotografišete priznanicu. Kada završite sa fotografisanjem, izaberite **U redu** da biste prihvatili fotografiju.
    - Ako ste izabrali **Odaberite sliku**, izaberite sliku sa liste.

10. Izaberite **Gotovo**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Odobrite izveštaj o troškovima pomoću mobilnog radnog prostora za upravljanje troškovima (ako koristite ispravku iz jula 2017)
1. Na mobilnom uređaju otvorite radni prostor za **Upravljanje troškovima**.
2. **Odobrenja troškova** prikazuje broj izveštaja o troškovima koji su vam dodeljeni na odobrenje. Broj se ažurira otprilike svakih 30 minuta. Izaberite **Odobrenja troškova**.

    Prikazuje se lista izveštaja o troškovima koji su vam dodeljeni na odobrenje.
    
3. Izaberite izveštaj o troškovima da biste videli detalje o troškovima za njega.
4. Izaberite trošak da biste videli detalje za njega. Podaci koji se prikazuju kao trošak uključuju sve detalje o priznanici, gostu i detaljima.
5. Vratite se na stranicu **Izveštaj o troškovima**, izaberite da biste odobrili ili odbili izveštaj o troškovima.
6. Unesite komentare uz odobrenje.
7. Izaberite **Gotovo**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Kreirajte novi izveštaj o troškovima i podnesite ga na odobrenje pomoću mobilnog radnog prostora za upravljanje troškovima (ako koristite ispravku iz jula 2017)
1. Na mobilnom uređaju otvorite radni prostor za **Upravljanje troškovima**.
2. Izaberite **Unos troškova**.
3. Izaberite **Novi izveštaj** ili izaberite postojeći izveštaj o troškovima na listi.
4. Za nove izveštaje o troškovima unesite svrhu i sve dodatne dostupne informacije. Ove informacije se razlikuju, u zavisnosti od toga na koji način je upravljanje troškovima konfigurisano za vašu kompaniju.
5. Izaberite **Gotovo**.
6. Izaberite **Priloži** da biste u izveštaj o troškovima dodali postojeće troškove, poput transakcija kreditnom karticom.
7. Izaberite jedan ili više troškova na listi.
8. Izaberite **Gotovo**.
9. Da biste dodali novi trošak izveštaju o troškovima, izaberite **Novi trošak**.
10. Izaberite kategoriju troška. Videćete listu kategorija troškova koje su učitane u vašu aplikaciju za korišćenje van mreže. Podrazumevano se učitava 50 stavki, ali programer može promeniti ovaj broj. Za više informacija, programeri bi trebalo da pogledaju članak [Mobilna platforma](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Ako vaša kategorija nije na listi, izaberite **Pretraga** da biste obavili pretragu na mreži. Pretražujte po kategoriji troška ili se prebacite na pretragu po vrsti troška.
11. Opcionalno: unesite trgovca za trošak.
12. Unesite datum transakcije troška.
13. Unesite iznos troška.
14. Izaberite valutu troška. Videćete listu šifara valuta koje su učitane u vašu aplikaciju za korišćenje van mreže. Podrazumevano se učitava 400 valuta, ali programer može promeniti ovaj broj. Za više informacija, programeri bi trebalo da pogledaju članak [Mobilna platforma](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Ako vaša valuta nije na listi, izaberite **Pretraga** da biste obavili pretragu na mreži. Pretražujte po valuti ili se prebacite na pretragu po nazivu.
15. Izaberite **Gotovo**.
16. Da biste dodali više detalja trošku, izaberite **Dodajte više detalja**. Dostupna polja zavise od konfiguracije upravljanja troškovima vaše kompanije.
17. Ako politika kompanije zahteva potvrdu o trošku, izaberite **Priznanice**, a zatim sledite ove korake:

    1. Izaberite **Snimite priznanicu** ili **Priložite priznanicu**.
    2. Pratite jedan od sledećih koraka:

        - Ako ste izabrali **Snimite priznanicu**, pratite ove korake:

            1. Izaberite **Snimite fotografiju** ili **Odaberite sliku**.
            2. Pratite jedan od sledećih koraka:

                - Ako ste izabrali **Snimite fotografiju**, pratite ove korake:

                    1. Bićete preusmereni na kameru na svom mobilnom uređaju, tako da možete da fotografišete priznanicu. Kada završite sa fotografisanjem, izaberite **U redu** da biste prihvatili fotografiju.
                    2. Opcionalno: unesite naziv fotografije i unesite beleške.

                - Ako ste izabrali **Odaberite sliku**, pratite ove korake:

                    1. Izaberite sliku sa liste.
                    2. Opcionalno: unesite naziv slike i unesite beleške.

            3.  Izaberite **Gotovo**.

        - Ako ste izabrali **Priložite priznanicu**, pratite ove korake:

            1.  Izaberite jednu ili više slika na listi.
            2.  Izaberite **Gotovo**.

    3. Izaberite dugme **Nazad** za povratak na detalje o troškovima.

18. Ako politika kompanije zahteva gosta za trošak, izaberite **Gosti**, a zatim sledite ove korake:

    1. Izaberite **Gost**, **Prethodni gosti** ili **Saradnici**.
    2. Pratite jedan od sledećih koraka:

        - Ako ste izabrali **Gost**, pratite ove korake:

            1. Unesite ime za gosta.
            2. Opcionalno: unesite organizaciju i/ili zemlju gosta.
            3. Opcionalno: unesite poziciju za gosta.
            4. Izaberite **Gotovo**.

        - Ako ste izabrali **Prethodni gosti**, pratite ove korake:

            1. Izaberite jednog ili više prethodnih gostiju na listi. Videćete listu prethodnih gostiju koje ste dodali u prethodne izveštaje o troškovima koji su učitani u vašu aplikaciju za korišćenje van mreže. Podrazumevano se učitava 50 stavki, ali programer može promeniti ovaj broj. Za više informacija, programeri bi trebalo da pogledaju članak [Mobilna platforma](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Ako vaš prethodni gost nije na listi, izaberite **Pretraga** da biste obavili pretragu na mreži. Pretražujte po imenu ili pređite na pretragu po organizaciji, zemlji ili poziciji.
            2. Izaberite **Gotovo**.

        - Ako ste izabrali **Saradnici**, pratite ove korake:

            1. Izaberite jednog ili više saradnika na listi. Videćete listu saradnika koji su učitani u vašu aplikaciju za korišćenje van mreže. Podrazumevano se učitava 50 stavki, ali programer može promeniti ovaj broj. Za više informacija, programeri bi trebalo da pogledaju članak [Mobilna platforma](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Ako vaš saradnik nije na listi, izaberite **Pretraga** da biste obavili pretragu na mreži. Pretražujte po imenu ili pređite na pretragu po kompaniji ili poziciji.
            2. Izaberite **Gotovo**.

    3. Izaberite dugme **Nazad** za povratak na detalje o troškovima.

19. Ako politika kompanije zahteva podelu troška, izaberite **Podela**, a zatim sledite ove korake:

    1. Izaberite prvi datum za podelu.
    2. Izaberite **Dodajte podelu**.
    3. Izaberite potkategoriju podele troška. Videćete listu potkategorija troškova koje su učitane u vašu aplikaciju za korišćenje van mreže. Podrazumevano se učitava 50 stavki, ali programer može promeniti ovaj broj. Za više informacija, programeri bi trebalo da pogledaju članak [Mobilna platforma](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Ako vaša potkategorija nije na listi, izaberite **Pretraga** da biste obavili pretragu na mreži. Pretražite prema nazivu potkategorije troškova.
    4. Unesite iznos transakcije za podelu.
    5. Izmenite datum transakcije ako je potrebno.
    6. Izaberite **Gotovo**.
    7. Ponavljajte prethodne korake dok ne završite sa dodavanjem svih stavki za izabrani datum.
    8. Za dodatne dane možete odabrati **Kopiraj na sledeći dan** da biste kopirali detalje na sledeći dan. Možete i da izaberete datum za podelu, a zatim da dodate podele kao što ste to učinili za prvi datum.
    9. Nakon što završite sa podelom troškova, izaberite dugme **Nazad** za povratak na detalje o troškovima.

20. Izaberite dugme **Nazad** za povratak na stranicu **Izveštaj o troškovima**.
21. Ponavljajte prethodne korake dok ne završite sa dodavanjem svih troškova.
22. Izaberite **Prosledi**.
23. Unesite komentare za davaoca odobrenja.
24. Izaberite **Gotovo**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]