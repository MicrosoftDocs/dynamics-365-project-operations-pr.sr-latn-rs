---
title: Primena demo podešavanja i podataka o konfiguraciji
description: Ova tema pruža informacije o tome kako da primenite demo podešavanja i podatke o konfiguraciji za Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 33b85115963f3561718b8951e5b518fd34de7723
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083445"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Primenite demo podešavanja i podatke o konfiguraciji za jednostavnu primenu usluge Project Operations – od pogodbe do profakture

_**Jednostavna primena – od pogodbe do profakture_

1. Preuzmite [Paket glavnih podataka](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Idite u fasciklu *ProjOpsDemoDataSetupAndMaster - Integrated CMT* i pokrenite izvršnu datoteku *DataMigrationUtility*.
3. Na 1. stranici Common Data Service čarobnjaka za konfigurisanje migracije (CMT) izaberite **Uvezi podatke** , a zatim izaberite **Nastavi**.

![Migracija konfiguracije](./media/1ConfigurationMigration.png)

4. Na 2. stranici CMT čarobnjaka izaberite **Microsoft 365** kao **Tip primene**.
5. Izaberite polja za potvrdu **Prikaži listu dostupnih organizacija** i **Prikaži napredno**.
6. Izaberite region vašeg zakupca, unesite svoje akreditive, a zatim izaberite **Prijavljivanje**.

![Prijavljivanje u konfiguraciju](./media/2ConfigurationSignin.png)

7. Na stranici 3, sa liste organizacija u zakupcu, izaberite u koju organizaciju želite da uvezete demo podatke, a zatim izaberite **Prijavljivanje**.
8. Na 4. stranici izaberite zip datoteku *MasterAndSetupData* iz raspakovane fascikle *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.

![Komprimovana datoteka](./media/3ZipFile.png)

![Izbor datoteke](./media/4SelectAFile.png)

9. Kada izaberete zip datoteku, izaberite **Uvoz podataka**.

![Uvoz podataka](./media/5ImportData.png)

10. Uvoz će trajati otprilike od dva do deset minuta, u zavisnosti od brzine vaše mreže. Po završetku izađite iz CMT čarobnjaka. 
11. Potražite u svojoj organizaciji podatke za sledećih 20 entiteta:

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
- Detalj o učestalosti fakturisanja
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
