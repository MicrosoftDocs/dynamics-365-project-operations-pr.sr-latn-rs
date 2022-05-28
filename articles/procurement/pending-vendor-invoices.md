---
title: Nabavka nefakturisanih materijala ili kategorija nabavki pomoću neobrađene fakture dobavljača
description: Ova tema objašnjava kako da snimite fakture dobavljača na čekanju.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e81f7a54e304ae6fc9a9f2637124579b6e7b54e9
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612674"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Nabavka nefakturisanih materijala ili kategorija nabavki pomoću neobrađene fakture dobavljača

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Kako preduzeće nabavlja nenapuštene materijale ili kategorije nabavki za projekat, troškovi se mogu odmah zabeležiti u odnosu na projekat. 

Na primer, preduzeće Contoso Robotics US izvodi projekat obnove opreme i potrebne su mu softverske licence. Ove licence se nabavljaju od nezavisnog dobavljača.  Koristeći Dynamics 365 Finance, službenik koji plaća račune zapisuje dokument fakture dobavljača na čekanju i pripisuje troškove licenciranja direktno u odnosu na projekat obnavljanja opreme. 

> [!IMPORTANT]
> Pre nego što upotrebite funkcionalnost opisanu u ovoj temi, pregledajte i primenite potrebne konfiguracije. Više informacija potražite u članku Omogućavanje [nefakturisanih materijala i neobrađenih faktura dobavljača](configure-materials-nonstocked.md)[i Korišćenje kategorija nabavki sa izlaznim porudžbinama projekta i neobrađenim fakturama dobavljača](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Pošaljite fakturu dobavljača na čekanju u vezi sa projektom 

Fakture dobavljača na čekanju mogu se evidentirati na stranici **Fakture dobavljača na čekanju** (**Dugovanja** > **Fakture** > **Fakture dobavljača na čekanju**). Dovršite sledeće korake da biste knjižili fakturu dobavljača na čekanju u vezi sa projektom:

1. Idite na fakture **za plaćanje** > **i izaberite** stavku **Novo**. 
1. U polje **Konto fakture** izaberite dobavljača, a zatim u polje Broj **unesite** identifikaciju fakture dobavljača.
1. Dodajte red u fakturu dobavljača, a zatim u **polju Broj artikla** izaberite nefakturisan artikal koji je nabavljen od dobavljača. Druga mogućnost je da u polju **Kategorija nabavke** izaberete kategoriju nabavke koja je kupljena od dobavljača.   
1. Dodajte nabavljenu količinu. Sistem popunjava jediničnu cenu na osnovu konfiguracije cena artikla koja nije snabdevena. 
1. Potvrdite ukupan iznos i ostale potrebne detalje na liniji.
1. U detaljima reda, na kartici **Projekat** izaberite ID projekta na koji će ova stavka biti zapisana.
1. Opcionalno: Izaberite broj aktivnosti i ažurirajte kategoriju projekta i svojstvo reda.
1. Proknjižite fakturu dobavljača na čekanju. Kada proknjižite fakturu, sistem zapisuje sledeće informacije:
    
    - Iznos bilansa dobavljača.
    - Iznos poreza na promet.
    - Troškovi projekta evidentiraju se na račun integracije nabavki.
    - Transakcija stvarnih troškova projekta u usluzi Dataverse.  Ova transakcija se dalje obrađuje pomoću [Project Operations dnevnika integracije](../project-accounting/project-operations-integration-journal.md). Objavljivanjem ovog dnevnika premešta se iznos sa računa integracije nabavki na račun troškova projekta. 
    - Kupovine koje se klijentu projekta obračunavaju korišćenjem metode obračuna vremena i materijala. Osim toga, za kupovine u usluzi Dataverse kreiraju se transakcije nenaplaćene prodaje. Cenovnik proizvoda u usluzi Dataverse koristi se za prodajne cene i iznose za transakcije nenaplaćene prodaje.
