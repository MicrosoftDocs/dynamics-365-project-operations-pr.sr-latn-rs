---
title: Primena demo podešavanja i podataka o konfiguraciji – jednostavno
description: Ova tema pruža informacije o tome kako da primenite demo podešavanja i podatke o konfiguraciji za Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7729b4a9ef5f498b78af298f7233d7dd45434bb3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997168"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Primena demo podešavanja i podataka o konfiguraciji za Project Operations – jednostavno 

_**Jednostavna primena – od pogodbe do profakture_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>Preduslovi

Pre nego što započnete konfiguraciju, morate imati Common Data Service (CDS) okruženje predviđeno za Dynamics 365 Project Operations.


## <a name="instructions"></a>Uputstva

1. Preuzmite [Paket glavnih podataka](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
2. Dođite do fascikle *ProjOpsSampleSetupData - CE only CMT* i pokrenite izvršnu datoteku *DataMigrationUtility*.
3. Na 1. stranici Common Data Service čarobnjaka za konfigurisanje migracije (CMT) izaberite **Uvezi podatke**, a zatim izaberite **Nastavi**.

    ![Migracija konfiguracije](./media/1ConfigurationMigration.png)

4. Na 2. stranici CMT čarobnjaka izaberite **Microsoft 365** kao **Tip primene**.
5. Izaberite polja za potvrdu **Prikaži listu dostupnih organizacija** i **Prikaži napredno**.
6. Izaberite region vašeg zakupca, unesite svoje akreditive, a zatim izaberite **Prijavljivanje**.

   ![Prijavljivanje u konfiguraciju](./media/2ConfigurationSignin.png)

7. Na stranici 3, sa liste organizacija u zakupcu, izaberite u koju organizaciju želite da uvezete demo podatke, a zatim izaberite **Prijavljivanje**.
8. Na stranici 4 izaberite zip datoteku, *SampleSetupAndConfigData* iz raspakovane fascikle, *ProjOpsSampleSetupData - CE only CMT*.

   ![Komprimovana datoteka](./media/3ZipFile.png)

   ![Izaberite datoteku](./media/4SelectAFile.png)

9. Kada izaberete zip datoteku, izaberite **Uvoz podataka**.

   ![Uvoz podataka](./media/5ImportData.png)

10. Uvoz će trajati otprilike od dva do deset minuta, u zavisnosti od brzine vaše mreže. Po završetku izađite iz CMT čarobnjaka. 
11. Potražite u svojoj organizaciji podatke za sledećih 18 entiteta:

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

    ![Kompletan uvoz](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
