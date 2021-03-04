---
title: Obezbeđenje novog okruženja
description: Ova tema pruža informacije o načinu obezbeđenja novog Project Operations okruženja.
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 09af2a7693c45d1d0b9c75420d018cc50d2cc0fa
ms.sourcegitcommit: 04c446746aad97fc3f4c3d441983c586b918a3a6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 12/11/2020
ms.locfileid: "4727807"
---
# <a name="provision-a-new-environment"></a>Obezbeđenje novog okruženja

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Ova tema pruža informacije o načinu da obezbedite novo Dynamics 365 Project Operations okruženje za scenarije zasnovane na resursima/bez zaliha.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Omogućavanje Project Operations automatskog obezbeđivanja u LCS projektu

Koristite sledeće korake da omogućite Project Operations automatizovani tok obezbeđivanja za vaš LCS projekat.

1. Idite na [LCS](https://lcs.dynamics.com/v2) i izaberite pločicu **Pregled upravljanja funkcijama**.
2. Na listi **Funkcija pregleda** izaberite **Project Operations Feature** i izaberite **Omogućena funkcija pregleda** kako bi se omogućila usluga Project Operations.

> [!NOTE]
> Ovaj korak se izvodi samo jednom po LCS projektu.

## <a name="provision-a-project-operations-environment"></a>Obezbeđivanje Project Operations okruženja

1. Otvori novu primenu Dynamics 365 Finance [demo okruženja](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) ili [sandbox/proizvodnog okruženja](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure). 
2. Prođite kroz čarobnjak **Obezbeđivanje okruženja**. 

> [!IMPORTANT]
> Uverite se da je izabrana verzija aplikacije 10.0.13 ili novija.

3. Da biste obezbedili Project Operations, u delu **Napredna podešavanja** izaberite **Common Data Service**. 
4. Omogućite **Common Data Service podešavanje** birajući **Da**, a zatim unesite podatke u obavezna polja:

  - +Ime
  - Region
  - Jezik
  - Valuta
 
5. U polju **Common Data Service predložak**, izaberite **Project Operations** 

6. Izaberite vrstu okruženja za vašu primenu. Probno vreme zasnovano na pretplati omogućiće vam da primenite CDS okruženje na 30 dana. 

![Podešavanja primene](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> Izaberite **Slažem se** da biste prihvatili uslove usluge, a zatim izaberite **Gotovo** da se vratite na podešavanja primene.

![Saglasnost za primenu](./media/2DeploymentConsent.png)

7. Opcionalno – primenite demo podatke na okruženje. Idite na **Napredna podešavanja**, izaberite **Prilagodi konfiguraciju SQL baze podataka** i podesite **Navedite skup podataka za bazu podataka aplikacije** na **Demo**.

8. Popunite preostala obavezna polja u čarobnjaku i potvrdite primenu. Vreme za pripremu okruženja varira u zavisnosti od vrste okruženja. Obezbeđenje može potrajati do šest sati.

  Kada se primena uspešno završi, okruženje će se prikazati kao **Primenjeno**.

9. Da biste potvrdili da se okruženje uspešno primenilo, izaberite **Prijavi se** i prijavite se u okruženje da biste potvrdili.

![Detalji  okruženja](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a>Primenite ispravke na Finance okruženje

Project Operations zahteva Finance okruženje sa verzijom aplikacije **10.0.13 (10.0.569.20009)** ili novijom.

Možda ćete morati da primenite ispravke kvaliteta u svom Finance okruženju da biste dobili ovu verziju.

1. U LCS-u, na stranici **Detalji okruženja**, u odeljku **Dostupne ispravke** izaberite **Prikaži ispravku**.

![Prikaz ispravki](./media/5ViewUpdates.png)

2. Na stranici **Binarna ažuriranja** izaberite **Sačuvaj paket.**

![Sačuvaj paket](./media/6SavePackage.png)

3. Kliknite na **Izaberi sve**, a zatim izaberite **Sačuvaj paket**.

![Pregledajte i sačuvajte ispravke](./media/7ReviewAndSaveUpdates.png)

4. Unesite naziv i opis paketa, a zatim izaberite **Sačuvaj**. U zavisnosti od internet veze, ovaj postupak može potrajati.

![Otpremite paket u biblioteku sredstava](./media/8UploadPackageToAssetsLibrary.png)

5. Kada se paket sačuva, izaberite **Gotovo** i sačuvajte ovaj paket u biblioteci sredstava u vašem LCS projektu.

Čuvanje i potvrđivanje paketa može potrajati oko 15 minuta.

6. Da biste primenili ispravku, idite na stranicu **Detalji okruženja** u LCS-u i izaberite **Održavanje** > **Primeni ispravke**.

![Održavanje okruženja](./media/9MaintainEnvironment.png)

7. Na listi ispravki izaberite paket koji ste kreirali i izaberite **Primeni**.

![Primena ispravki](./media/10ApplyUpdates.png)

Servisiranje okruženja će potrajati neko vreme. Po završetku, okruženje će se vratiti u primenjeno stanje.

![Primenjeno okruženje](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Uspostavite vezu sa dvostrukim upisivanjem 

1. U svom LCS projektu idite na stranicu **Detalji okruženja**.
2. U odeljku **Common Data Service informacije o okruženju**, izaberite **Poveži sa uslugom CDS za aplikacije**.
3. Kada se povezivanje završi, ponovo izaberite **Poveži sa uslugom CDS za aplikacije**. Bićete preusmereni na dvostruko upisivanje u usluzi Finance.

![Povezivanje sa uslugom CDS](./media/12LinktoCDS.png)

4. Izaberite **Primeni rešenje** za pristup entitetima koji će biti mapirani u integraciji.

![Primena rešenja](./media/13ApplySolutions.png)

5. Izaberite oba rešenja, **Dynamics 365 Finance and Operations mapa entiteta za dvostruko pisanje** i **Dynamics 365 Project Operations mape entiteta za dvostruko pisanje**, a zatim izaberite **Primeni**.

![Potvrda rešenja](./media/14ConfirmSolutions.png)

Kada primenite rešenja, entiteti dvostrukog upisivanja se primenjuju na okruženje.

![Primena rešenja](./media/15ApplyingSolutions.png)

Kada se entiteti primene, sva raspoloživa mapiranja se navode u okruženju.

![Mape za dvostruko upisivanje](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Osvežite entitete podataka nakon ispravke

1. U usluzi Finance idite na radni prostor **Upravljanje podacima**.

![Radni prostor za upravljanje podacima](./media/16DataManagement.png)

2. Izaberite pločicu **Parametri radnog okvira**.

![Parametri radnog okvira](./media/17FrameworkParameters.png)

3. Na stranici **Podešavanja entiteta**, izaberite **Osveži listu entiteta**.

![Osveži listu entiteta](./media/18RefreshEntityList.png)

Osvežavanje će trajati približno 20 minuta. Dobićete upozorenje kada se završi.

![Potvrda osvežavanja](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a>Ažuriranje bezbedonosnih podešavanja u usluzi Project Operations za Dataverse

1. Idite na Project Operations u Dataverse okruženju. 
2. Idite na **Podešavanja** > **Bezbednost** > **Bezbednosne uloge**. 
3. Na stranici **Bezbedonosne uloge** sa liste uloga izaberite **korisnik aplikacije za dvostruko upisivanje** i izaberite karticu **Prilagođeni entiteti**.  
4. Proverite da li uloga ima dozvole **Čitanje** i **Priloži u** za:
      
      - **Tip deviznog kursa valute**
      - **Grafikon poslovnih kontakata**
      - **Fiskalni kalendar**
      - **Glavna knjiga**

5. Nakon ažuriranja bezbednosne uloge, idite na **Podešavanja** > **Bezbednost** > **Timovi** i izaberite podrazumevani tim u prikazu timova **Vlasnik lokalnog preduzeća**.
6. Izaberite **Upravljanje ulogama** i proverite da li je bezbednosna privilegija **korisnik aplikacije za dvostruko upisivanje** primenjena na ovaj tim.

## <a name="run-project-operations-dual-write-maps"></a>Pokrenite Project Operations mape dvostrukog upisivanja

1. U svom LCS projektu idite na stranicu **Detalji okruženja**.
2. U odeljku **Common Data Service informacije o okruženju**, izaberite **Poveži sa uslugom CDS za aplikacije.** Kada izaberete vezu, bićete preusmereni na listu entiteta u mapiranjima.
3. Pokrenite mape kao što je opisano u sledećoj tabeli. Uverite se da sledite navedeni redosled.

| **Mapa entiteta** | **Osvežavanje entiteta** | **Početna sinhronizacija** | **Master za početnu sinhronizaciju** | **Preduslovi za pokretanje** | **Početna sinhronizacija preduslova** |
| --- | --- | --- | --- | --- | --- |
| **Uloge projektnih resursa za sva preduzeća (bookableresourcecategories)** | No | Da | Common Data Service | No | Nije primenjivo |
| **Pravna lica (cdm\_preduzeća)** | No | Da | Finance and Operations aplikacije | No | Nije primenjivo |
| **Knjiga (msdyn_ledgers)** | No | Da | Finance and Operations aplikacije | Da | Da, Finance and Operations aplikacije |
| **Project Operations stvarne vrednosti integracije (msdyn\_stvarne vrednosti)** | No | No | Nije primenjivo | Da | No |
| **Predmeti ugovora projekta (salesorderdetails)** | No | No | Nije primenjivo | No | No |
| **Entitet integracije za odnose transakcija projekta (msdyn\_transactionconnections)** | No | No | Nije primenjivo | No | Nije primenjivo |
| **Project Operations kontrolne tačke predmeta ugovora o integraciji (msdyn\_contractlinesscheduleofvalues)** | No | No | Nije primenjivo | No | Nije primenjivo |
| **Project Operations entitet integracije za procene troškova (msdyn\_estimateslines)** | No | No | Nije primenjivo | No | Nije primenjivo |
| **Project Operations entitet izvoza kategorija troškova projekta (msdyn\_expensecategories)** | No | No | Nije primenjivo | No | Nije primenjivo |
| **Project Operations entitet izvoza troškova integracije projekta (msdyn\_expenses)** | Da | No | Nije primenjivo | No | Nije primenjivo |
| **Project Operations entitet integracije za procene sati (msdyn\_resourceassignments)** | Da | No | Nije primenjivo | No | Nije primenjivo |


4. Da biste osvežili entitet, izaberite naziv mape, a zatim izaberite **Osveži entitete**. 


![Osvežavanje mape](./media/20RefreshMapping.png)

5. Kada se osvežavanje završi, pokrenite mapu. Pre nego što omogućite sledeću mapu, proverite da li je mapa u tabeli u stanju **Pokrenuta**. Pokretanje mapa sa većim brojem preduslova može potrajati.

Da biste pokrenuli mapu sa preduslovima, omogućite preklopno dugme **Prikaži povezane mape entiteta**. Ako tabela pokazuje da **Početna sinhronizacija preduslova** ima vrednost **Ne**, proverite da li je zastavica **Početna sinhronizacija** **isključena** u svim mapama preduslova pre nego što je pokrenete.

![Pokretanje mape](./media/21RunMap.png)

6. Potvrdite da su sve mape povezane sa projektom u aktivnom stanju.

![Sve mape su pokrenute](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Primena podataka o konfiguraciji u usluzi CDS za Project Operations (opcionalno)

Ako ste primenili demo podatke na Finance okruženje, pogledajte članak [Podešavanje i primena podataka o konfiguraciji u usluzi Common Data Service za Project Operations](resource-apply-pro-setup-config-data.md) za primenu demo podataka na CDS okruženje.


Vaše Project Operations okruženje je sada obezbeđeno i konfigurisano. 
