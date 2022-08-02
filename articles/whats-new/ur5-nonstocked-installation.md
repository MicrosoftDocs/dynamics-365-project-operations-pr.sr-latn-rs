---
title: Ažuriranje usluge Project Operations u Finance okruženju
description: Ovaj članak pruža informacije o tome kako da ažurirate operacije projekta u Dynamics 365 Finance okruženju.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: aedfd815521054d58944496500aa03a27be9267b
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/18/2022
ms.locfileid: "9030052"
---
# <a name="update-project-operations-in-your-finance-environment"></a>Ažuriranje usluge Project Operations u Finance okruženju

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_


Ovaj članak pruža informacije o tome kako da ažurirate Dynamics 365 Project Operations Dynamics 365 Finance okruženju. Postoje tri procedure potrebne za ažuriranje usluge Project Operations na ispravku 5 (Microsoft Dynamics CRM 2011 Update Rollup 5):

- [Uvoz paketa u projekat pregleda](#import)
- [Primena ispravke](#apply)
- [Ažuriranje Dataverse okruženja](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>Uvoz paketa u LCS projekat

1. Prijavite se na [Lifecycle Services (LCS)](https://lcs.dynamics.com/) kao vlasnik projekta ili menadžer okruženja.
2. Sa liste projekata odaberite LCS projekat.
3. Na stranici **Projekat** u grupi **Okruženja** otvorite okruženje koje želite da ažurirate.
4. Proverite da li je okruženje pokrenuto. Ako nije pokrenuto, pokrenite okruženje.
5. U odeljku **Novo izdanje** pod **Dostupne ispravke** izaberite **Prikaži ispravku** za 10.0.15.

![Dugme „Prikaži ispravku“.](media/view-update.png)

6. Na stranici **Binarna ažuriranja** izaberite **Sačuvaj paket**.
7. Na stranici **Pregled i čuvanje ispravki** izaberite **Sačuvaj paket**.
8. U oknu **Čuvanje paketa u biblioteci sredstava** koji se otvori unesite naziv paketa, a zatim izaberite **Sačuvaj paket**.
9. Kada LCS završi čuvanje paketa, dugme **Gotovo** će biti omogućeno. Izaberite **Gotovo**. LCS će verifikovati paket. Verifikacija može trajati nekoliko minuta, najviše do sat vremena.


## <a name="apply-the-package-update"></a><a name="apply"></a>Primena ispravke paketa

1. U usluzi LCS, na stranici **Detalji okruženja** izaberite **Održavaj** > **Primeni ispravke**.
2. Na listi izaberite paket koji ste ranije sačuvali, a zatim izaberite **Primeni**.
3. Izaberite **Da** da biste potvrdili da želite da primenite paket.

![Potvrdite izbor u dijalogu „Primena paketa“.](media/confirm-package-deployment.png)

4. Izaberite **Da** da biste potvrdili da želite da ažurirate aplikaciju.

![Potvrdite izbor u dijalogu „Ažuriranje aplikacije“.](media/confirm-application-update.png)

Pokrenuće se primena i ažuriranje aplikacije. 

Na stranici **Detalji okruženja**, u gornjem desnom uglu, status okruženja će se ažurirati na **Servisiranje**. Za otprilike dva sata ažuriranje će biti gotovo. Informacije o izdanju aplikacije će se ažurirati na **Microsoft Dynamics 365 for Finance and Operations 10.0.15** a status okruženja će se ažurirati na **Primenjeno**.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Ažuriranje Dataverse okruženja

1. Prijavite se u [Power Platform centar administracije](https://admin.powerplatform.com/).
2. Na listi pronađite i otvorite okruženje koje ste koristili za instaliranje usluge Project Operations.
3. Na stranici **Okruženja** izaberite **Resurs** > **Dynamics 365 aplikacije**.
4. Na listi pronađite **Microsoft Dynamics 365 Project Operations** i u koloni **Status** izaberite **Dostupna ispravka**.
5. Označite polje za potvrdu **Slažem se sa uslovima korišćenja usluge**, a zatim izaberite **Ažuriraj**. Biće instalirana najnovija verzija rešenja.

Po završetku instalacije imaćete instaliranu verziju 4.5.0.134.

## <a name="configure-new-features"></a>Konfigurisanje novih funkcija

### <a name="enable-dual-write-mapping"></a>Omogućavanje mapiranja dvostrukog upisivanja

Nakon što dovršite ažuriranje Finance i Dataverse okruženja, možete omogućiti potrebna mapiranja dvostrukog upisivanja. Obavite sledeće procedure da biste omogućili mapiranje dvostrukog upisivanja.

- [Ažuriranje bezbedonosnih podešavanja u Customer Engagement okruženju](#security)
- [Osvežavanje entiteta podataka](#refresh)
- [Ažuriranje i pokretanje mapiranja dvostrukog upisivanja](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>Ažuriranje bezbedonosnih podešavanja u Dataverse okruženju

Sledeće ispravke bezbednosnih privilegija za entitete su potrebne kao deo ažuriranja na Microsoft Dynamics CRM 2011 Update Rollup 5.

1. U okruženju Dataverse idite na **Podešavanja** i u grupi **Sistem** izaberite **Bezbednost**.

![Podešavanja Dataverse okruženja.](media/Picture21.png)

2. Izaberite **Bezbednosne uloge**.
3. Sa liste uloga izaberite **korisnik aplikacije za dvostruko upisivanje** i izaberite karticu **Prilagođeni entiteti**. 
4. Proverite da li uloga ima dozvole **Čitanje** i **Priloži u** za:

      - **Tip deviznog kursa valute**
      - **Grafikon poslovnih kontakata** 
      - **Fiskalni kalendar** 
      - **Glavna knjiga**

5. Nakon ažuriranja bezbednosne uloge, idite na **Podešavanja** > **Bezbednost** > **Timovi**. Proverite da li je uloga **korisnik aplikacije za dvostruko upisivanje** primenjena na tim. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>Osvežavanje entiteta podataka iz ispravke

1. U Finance okruženju otvorite radni prostor **Upravljanje podacima**, a zatim otvorite stranicu **Parametri okvira**.
2. Na kartici **Podešavanja entiteta** izaberite **Osveži listu entiteta**.
3. Izaberite **Zatvori** da biste potvrdili osvežavanje entiteta.

 > [!NOTE]
 > Ovaj postupak će se završiti za oko 20 minuta. Bićete obavešteni kada se osvežavanje završi.

### <a name="update-dual-write-mappings"></a><a name="run"></a>Ažuriranje mapiranja dvostrukog upisivanja

1. U radnom prostoru **Upravljanje podacima** izaberite **Dvostruko upisivanje**.
2. Izaberite **Primeni rešenja**, izaberite oba rešenja sa liste, a zatim izaberite **Primeni**.
3. Na stranici **Dvostruko upisivanje** izaberite sledeće mape tabela, a zatim izaberite **Zaustavi**.

    - **Project Operations stvarne vrednosti integracije (msdyn_actuals)**
    - **Project Operations integracija kategorija troškova projekata (msdyn_expensecategories)**
    - **Entitet za izvoz troškova projekata za Project Operations stvarne vrednosti integracije (msdyn_expenses)**

4. Na stranici **Verzija mape tabele** primenite novu verziju mape na svaki od tri entiteta.
5. Na stranici **Dvostruko upisivanje** izaberite „Pokreni“ da biste ponovo pokrenuli mape.
6. Na listi mapa odaberite mapu **Glavna knjiga (msdyn_ledgers)** sa svim preduslovima i označite polje za potvrdu **Početna sinhronizacija**. 
7. U polju Master **za početnu sinhronizaciju izaberite** aplikacije "Finansije **" i "Operacije", a zatim** izaberite stavku **Pokreni**.
 
 ![Sinhronizacija mape glavne knjige.](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]