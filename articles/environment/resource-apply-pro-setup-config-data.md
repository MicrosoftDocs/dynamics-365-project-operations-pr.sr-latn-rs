---
title: Podešavanje i primena podataka o konfiguraciji u usluzi Common Data Service za Project Operations
description: Ova tema pruža informacije o tome kako da podesite i primenite podatke o konfiguraciji u usluzi Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e72b88a4dae1eb89859fdfd55f6d5e6ee5befcd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083453"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a>Podešavanje i primena podataka o konfiguraciji u usluzi Common Data Service za Project Operations

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

## <a name="install-setup-and-configuration-data"></a>Podaci o podešavanju i konfiguraciji instaliranja

1. Preuzmite, deblokirajte i raspakujte [Paket podataka za podešavanje i konfiguraciju](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).
2. Idite u fasciklu sa raspakovanim sadržajem i pokrenite izvršnu datoteku *DataMigrationUtility*.
3. Na 1. stranici Common Data Service čarobnjaka za konfigurisanje migracije (CMT) izaberite **Uvezi podatke** , a zatim izaberite **Nastavi**.

![Migracija konfiguracije](./media/1ConfigurationMigration.png)

4. Na 2. stranici CMT čarobnjaka izaberite **Microsoft 365** kao **Tip primene**.
5. Izaberite polja za potvrdu **Prikaži listu dostupnih organizacija** i **Prikaži napredno**.
6. Izaberite region vašeg zakupca, unesite svoje akreditive, pa izaberite **Prijavljivanje**.

![Prijavljivanje u konfiguraciju](./media/2ConfigurationSignin.png)

7. Na 3. stranici, sa liste organizacija u zakupcu, izaberite u koju organizaciju želite da uvezete demo podatke, a zatim izaberite **Prijavljivanje**.
8. Na 4. stranici, izaberite zip datoteku *SampleSetupAndConfigData* iz raspakovane fascikle.

![Izbor zip datoteke](./media/3ZipFile.png)

![Izbor datoteke](./media/4SelectAFile.png)

9. Kada izaberete zip datoteku, izaberite **Uvoz podataka**.

![Uvezi podatke](./media/5ImportData.png)

10. Uvoz će trajati otprilike od dva do deset minuta, u zavisnosti od brzine vaše mreže. Po završetku uvoza, izađite iz CMT čarobnjaka. 
11. Potražite u svojoj organizaciji podatke za sledećih 19 entiteta:

  - Valuta
  - Organizaciona jedinica
  - Kontakt
  - Poreska grupa
  - Grupa klijenata
  - Jedinica
  - Grupa jedinica
  - Cenovnik
  - Cenovnik parametara projekta
  - Učestalost fakturisanja
  - Kategorija resursa koji može da se rezerviše
  - Kategorija transakcije
  - Kategorija troška
  - Cena uloge
  - Cena kategorije transakcije
  - Karakteristika
  - Resurs koji može da se rezerviše
  - Povezivanje kategorije resursa koji može da se rezerviše
  - Karakteristika resursa koji može da se rezerviše

![Kompletan uvoz](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Ažuriranje Project Operations konfiguracije

1. Idite u CE okruženje. Možete ga pronaći ako otvorite [Power Platform centar administracije](https://admin.powerplatform.microsoft.com/environments), izaberete okruženje, a zatim izaberete **Otvoreno okruženje**. 

![Otvoreno okruženje](./media/7OpenEnvironment.png)

2. Idite na **Projekti** > **Resursi** , a zatim izaberite **Novo** da biste kreirali resurs koji može da se rezerviše za vašeg korisnika.

![Resursi koji mogu da se rezervišu](./media/8BookableResources.png)

3. Na kartici **Opšti podaci** izaberite svog administratora. Proverite da li se vremenska zona podudara sa onom u kojoj se nalazite. 

![Novi resurs koji može da se rezerviše](./media/9NewBookableResource.png)

4. Na kartici **Zakazivanje** , u polju **Kompanija** odaberite kompaniju **USPM** , a zatim izaberite **Sačuvaj**. 

![Kartica „Zakazivanje“](./media/10SchedulingTab.png)

5. Izaberite karticu **Radno vreme**.  

![Radno vreme](./media/11WorkHours.png)

6. Dvaput kliknite bilo koju vrednost u kalendaru i izaberite **Uređivanje** > **Svi događaji u seriji**. 

![Kalendar posla](./media/12WorkCalendar.png)

7. Promenite radno vreme u radni dan od osam (8) sati, obeležite vikende kao neradne dane i uverite se da vremenska zona odgovara vašoj. 
8. Izaberite stavku **Sačuvaj i zatvori**.

![Ažuriranje kalendara](./media/13UpdateCalendar.png)

9. Idite na **Podešavanja** > **Predlošci kalendara** i izaberite **Novi**.
 
 ![Predlošci kalendara](./media/14CalendarTemplates.png)
 
 10. Unesite naziv, izaberite resurs šablona koji ste kreirali, a zatim izaberite **Sačuvaj**. 
 
 ![Čuvanje predloška kalendara](./media/15SaveCalendarTemplate.png)
 
 11. Idite na **Parametri** i dvaput kliknite na zapis. 
 
 ![Parametri projekta](./media/16ProjectParameters.png)
 
12. Ažurirajte sledeća polja:

 - **Podrazumevana kompanija** : USPM
 - **Podrazumevana organizaciona jedinica** : Contoso Robotics Global
 - **Učestalost fakturisanja** : Sedmi i poslednji dan
 - **Predložak radnog vremena** : Promenite na predložak koji ste kreirali.

13. Izaberite stavku **Sačuvaj**. 

![Ažurirani parametri projekta](./media/17UpdatedProjectParameters.png)
