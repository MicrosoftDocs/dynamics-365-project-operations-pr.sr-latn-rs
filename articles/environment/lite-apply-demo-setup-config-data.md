---
title: Primena demo podešavanja i podataka o konfiguraciji – jednostavno
description: Ovaj članak pruža informacije o tome kako da primenite demo podešavanja i podatke o konfiguraciji za Project Operations.
author: sigitac
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8ac8c910ce2d91fa47df08e8fb6efb723c0dc5fa
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811043"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Primena demo podešavanja i podataka o konfiguraciji za Project Operations – jednostavno 

_**Jednostavna primena – od pogodbe do profakture_



## <a name="prerequisites"></a>Preduslovi

Pre nego što započnete konfiguraciju, morate imati Dataverse okruženje predviđeno za Dynamics 365 Project Operations.


## <a name="instructions"></a>Uputstva

1. Preuzmite instalacioni [paket podataka](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
1. Dođite do fascikle *ProjOpsSampleSetupData - CE only CMT* i pokrenite izvršnu datoteku *DataMigrationUtility*.
1. Na 1. stranici Common Data Service čarobnjaka za konfigurisanje migracije (CMT) izaberite **Uvezi podatke**, a zatim izaberite **Nastavi**.

    ![Migracija konfiguracije.](./media/1ConfigurationMigration.png)

1. Na 2. stranici CMT čarobnjaka izaberite **Microsoft 365** kao **Tip primene**.
1. Izaberite polja za potvrdu **Prikaži listu dostupnih organizacija** i **Prikaži napredno**.
1. Izaberite region vašeg zakupca, unesite svoje akreditive, a zatim izaberite **Prijavljivanje**.

   ![Prijavljivanje u konfiguraciju.](./media/2ConfigurationSignin.png)

1. Na stranici 3, sa liste organizacija u zakupcu, izaberite u koju organizaciju želite da uvezete demo podatke, a zatim izaberite **Prijavljivanje**.
1. Na stranici 4 izaberite zip datoteku, *SampleSetupAndConfigData* iz raspakovane fascikle, *ProjOpsSampleSetupData - CE only CMT*.

   ![Komprimovana datoteka.](./media/3ZipFile.png)

   ![Izaberite datoteku.](./media/4SelectAFile.png)

1. Kada izaberete zip datoteku, izaberite **Uvoz podataka**.

   ![Uvoz podataka.](./media/5ImportData.png)

1. Uvoz će trajati otprilike od dva do deset minuta, u zavisnosti od brzine vaše mreže. Po završetku izađite iz CMT čarobnjaka. 
1. Potražite u svojoj organizaciji podatke za sledećih 18 entiteta:

    -   Valuta
    -   Nalog
    -   Organizaciona jedinica
    -   Kontakt
    -   Jedinica
    -   Grupa jedinica
    -   Cenovnik
    -   Cenovnik parametara projekta 
    -   Učestalost fakturisanja
    -   Kategorija resursa koji može da se rezerviše
    -   Kategorija transakcije
    -   Kategorija troška
    -   Cena uloge
    -   Cena kategorije transakcije
    -   Karakteristika
    -   Resurs koji može da se rezerviše
    -   Povezivanje kategorije resursa koji može da se rezerviše
    -   Karakteristika resursa koji može da se rezerviše

    ![Kompletan uvoz.](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
