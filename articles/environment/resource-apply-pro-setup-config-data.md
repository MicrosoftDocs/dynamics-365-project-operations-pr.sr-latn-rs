---
title: Podešavanje i primena podataka o konfiguraciji u usluzi Common Data Service
description: Ova tema pruža informacije o tome kako da podesite i primenite podatke o konfiguraciji u usluzi Project Operations.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6fb91de30a2414fa7dd8dba47b28cf4824948565
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594733"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Podešavanje i primena podataka o konfiguraciji u usluzi Common Data Service 

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_



## <a name="prerequisites"></a>Preduslovi

Pre nego što počnete da konfigurišete podatke u usluzi Common Data Service (CDS), moraju biti ispunjeni sledeći preduslovi:

1.  Obezbeđivanje CDS okruženja i okruženja Dynamics 365 Finance za projektne operacije.
2.  Informacije o pravnom licu Dynamics 365 Finance se dele u CDS okruženje. To znači da entitet **Kompanija** u CDS-u ima sledeće evidencije preduzeća:
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Podaci o podešavanju i konfiguraciji instaliranja

1. Preuzmite, deblokirajte i raspakujte [Paket podataka za podešavanje i konfiguraciju](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).
2. Idite u fasciklu sa raspakovanim sadržajem i pokrenite izvršnu datoteku *DataMigrationUtility*.
3. Na 1. stranici Common Data Service čarobnjaka za konfigurisanje migracije (CMT) izaberite **Uvezi podatke**, a zatim izaberite **Nastavi**.

![Migracija konfiguracije.](./media/1ConfigurationMigration.png)

4. Na 2. stranici CMT čarobnjaka izaberite **Microsoft 365** kao **Tip primene**.
5. Izaberite polja za potvrdu **Prikaži listu dostupnih organizacija** i **Prikaži napredno**.
6. Izaberite region vašeg zakupca, unesite svoje akreditive, pa izaberite **Prijavljivanje**.

![Prijavljivanje u konfiguraciju.](./media/2ConfigurationSignin.png)

7. Na 3. stranici, sa liste organizacija u zakupcu, izaberite u koju organizaciju želite da uvezete demo podatke, a zatim izaberite **Prijavljivanje**.
8. Na 4. stranici, izaberite zip datoteku *SampleSetupAndConfigData* iz raspakovane fascikle.

![Izbor zip datoteke.](./media/3ZipFile.png)

![Izaberite datoteku.](./media/4SelectAFile.png)

9. Kada izaberete zip datoteku, izaberite **Uvoz podataka**.

![Uvezi podatke.](./media/5ImportData.png)

10. Uvoz će trajati otprilike od dva do deset minuta, u zavisnosti od brzine vaše mreže. Po završetku uvoza, izađite iz CMT čarobnjaka. 
11. Potražite u svojoj organizaciji podatke za sledećih 26 entiteta:

  - Valuta
  - Grafikon poslovnih kontakata
  - Fiskalni kalendar
  - Vrste deviznih kurseva valuta
  - Dan za plaćanje
  - Raspored plaćanja
  - Uslovi plaćanja
  - Organizaciona jedinica
  - Kontakt
  - Poreska grupa
  - Grupa klijenata
  - Grupa prodavaca
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

![Kompletan uvoz.](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Ažuriranje Project Operations konfiguracije

1. Idite u CE okruženje. Možete ga pronaći ako otvorite [Power Platform centar administracije](https://admin.powerplatform.microsoft.com/environments), izaberete okruženje, a zatim izaberete **Otvoreno okruženje**. 

![Otvoreno okruženje.](./media/7OpenEnvironment.png)

2. Idite na **Projekti** > **Resursi**, a zatim izaberite **Novo** da biste kreirali resurs koji može da se rezerviše za vašeg korisnika.

![resursi koji mogu da se rezervišu.](./media/8BookableResources.png)

3. Na kartici **Opšti podaci** izaberite svog administratora. Proverite da li se vremenska zona podudara sa onom u kojoj se nalazite. 

![Novi resurs koji može da se rezerviše.](./media/9NewBookableResource.png)

4. Na kartici **Zakazivanje**, u polju **Kompanija** odaberite kompaniju **USPM**, a zatim izaberite **Sačuvaj**. 

![Kartica „Zakazivanje“.](./media/10SchedulingTab.png)

5. Izaberite karticu **Radno vreme**.  

![Radno vreme.](./media/11WorkHours.png)

6. Dvaput kliknite bilo koju vrednost u kalendaru i izaberite **Uređivanje** > **Svi događaji u seriji**. 

![Kalendar posla.](./media/12WorkCalendar.png)

7. Promenite radno vreme u radni dan od osam (8) sati, obeležite vikende kao neradne dane i uverite se da vremenska zona odgovara vašoj. 
8. Izaberite stavku **Sačuvaj i zatvori**.

![Ažuriranje kalendara.](./media/13UpdateCalendar.png)

9. Idite na **Podešavanja** > **Predlošci kalendara** i izaberite **Novi**.
 
 ![Predlošci kalendara.](./media/14CalendarTemplates.png)
 
 10. Unesite naziv, izaberite resurs šablona koji ste kreirali, a zatim izaberite **Sačuvaj**. 
 
 ![Čuvanje predloška kalendara.](./media/15SaveCalendarTemplate.png)
 
 11. Idite na **Parametri** i dvaput kliknite na zapis. 
 
 ![Parametri projekta.](./media/16ProjectParameters.png)
 
12. Ažurirajte sledeća polja:

 - **Podrazumevana kompanija**: USPM
 - **Podrazumevana organizaciona jedinica**: Contoso Robotics Global
 - **Učestalost fakturisanja**: Sedmi i poslednji dan
 - **Predložak radnog vremena**: Promenite na predložak koji ste kreirali.

13. Izaberite stavku **Sačuvaj**. 

![Ažurirani parametri projekta.](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
