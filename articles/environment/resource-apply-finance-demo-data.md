---
title: Primena demo podataka na Finance okruženje koje se hostuje u oblaku
description: Ovaj tema objašnjava kako da primenite demo podatke iz operacija projekta na okruženje Dynamics 365 Finance hostovano u oblaku.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e4ccc7eb02fabdc0476fe454f33bff637ab8b835
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588983"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a>Primena demo podataka na Finance okruženje koje se hostuje u oblaku

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

> [!IMPORTANT]
> Ovaj tema je primenljiv samo Microsoft Dynamics 365 Finance verzija 10.0.13 i može se izvršiti samo na cloud okruženju. Dovršite korake u ovoj temi **PRE NEGO ŠTO** primenite ispravke kvaliteta na okruženje.

1. U svom LCS projektu, otvorite stranicu **Detalji okruženja**. Primetite da sadrži detalje potrebne za povezivanje sa okolinom pomoću protokola udaljene radne površine (RDP).

![Detalji okruženja.](./media/1EnvironmentDetails.png)

Prvi skup istaknutih akreditiva su akreditivi lokalnog naloga i sadrže hipervezu do veze sa udaljenom radnom površinom. Akreditivi uključuju korisničko ime i lozinku administratora okruženja. Drugi skup akreditiva se koristi za prijavljivanje na SQL Server u ovom okruženju.

2. Povežite se udaljeno sa okruženjem koristeći hipervezu u odeljku **Lokalni nalozi** i upotrebite **Akreditivi za lokalni nalog** za potvrdu identiteta.
3. Idite na **Internet Information Services** > **Grupe aplikacija** > **AOSService** i zaustavite uslugu. U ovom trenutku zaustavljate uslugu da biste mogli da nastavite da zamenjujete SQL bazu podataka.

![Zaustavljanje AOS.](./media/2StopAOS.png)

4. Idite na **Usluge** i zaustavite sledeće dve stavke:

- Microsoft Dynamics 365 Unified Operations: Batch Management Service
- Microsoft Dynamics 365 Unified Operations: Data Import Export Framework

![Zaustavljanje usluga.](./media/3StopServices.png)

5. Otvorite Microsoft SQL Server Management Studio. Prijavite se pomoću akreditiva za SQL Server i koristite korisnika axdbadmin i lozinku sa LCS stranice **Detalji okruženja**.

![SQL Server Management Studio.](./media/4SSMS.png)

6. U pregledaču objekata, izaberite **Baze podataka** i pronađite **AXDB**. Bazu podataka ćete zameniti novom bazom podataka koja se nalazi u [centru za preuzimanje](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip). 
7. Kopirajte zip datoteku u VM u koji ste udaljeno povezani i raspakujte zip sadržaj.
8. U programu SQL Server Management Studio kliknite desnim tasterom miša na **AxDB**, a zatim izaberite **Zadaci** > **Vraćanje** > **Baza podataka**.

![Vraćanje baze podataka.](./media/5RestoreDatabase.png)

9. Izaberite **Izvorni uređaj** i dođite do datoteke izvučene iz zip datoteke koju ste kopirali.

![Izvorni uređaji.](./media/6SourceDevice.png)

10. Izaberite **Opcije**, a zatim izaberite **Prepiši postojeću bazu podataka** i **Zatvorite postojeće veze sa odredišnom bazom podataka**. 
11. Izaberite **U redu**.

![Vraćanje podešavanja.](./media/7RestoreSetting.png)

Dobićete potvrdu da je vraćanje AXDB bilo uspešno. Kada dobijete ovu potvrdu, možete da zatvorite SQL Services Management Studio.

12. Vratite se na **Internet Information Services** > **Grupe aplikacija** > **AOSService** i pokrenite uslugu AOSService.
13. Idite na **Usluge** i pokrenite dve usluge koje ste ranije zaustavili.

14. Pronađite alatku AdminUserProvisioning na ovom VM-u. Potražite K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.
15. Pokrenite .ext datoteku koristeći svoju korisničku adresu u polju **Adresa e-pošte**. 
16. Izaberite **Prosledi**.

![Obezbeđivanje korisnika-administratora.](./media/8AdminUserProvisioning.png)

Za ovo je potrebno nekoliko minuta. Trebalo bi da primite poruku sa potvrdom da je korisnik-administrator uspešno ažuriran.

17. Na kraju, pokrenite komandnu liniju kao administrator i pokrenite komandu iisreset

![Resetovanje IIS.](./media/9IISReset.png)

18. Zatvorite sesiju udaljene radne površine i koristite stranicu LCS **Detalji okruženja** da biste se prijavili u okruženje i potvrdili da radi kao što se očekuje.

![Finansije i operacije.](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]