---
title: Kupujte neskladišteni materijal koristeći fakturu dobavljača na čekanju
description: Ova tema objašnjava kako da snimite fakture dobavljača na čekanju.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ce9f244eaa549742aeb55024ca9ef4d82cde1bd4a5b9c7f8c762cf72e0da83f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009053"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Kupujte neskladišteni materijal koristeći fakturu dobavljača na čekanju

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Kako kompanija nabavlja ne-zalihe materijala za projekat, troškovi se mogu odmah evidentirati u odnosu na projekat. 

Na primer, Contoso Robotics US izvodi projekat obnove opreme i potrebne su softverske licence. Ove licence se nabavljaju od nezavisnog dobavljača.  Koristeći Dynamics 365 Finance, službenik za dugovanja evidentira dokument fakture dobavljača na čekanju i pripisuje troškove licence direktno projektu obnove opreme. 

> [!IMPORTANT]
> Pre nego što upotrebite funkcionalnost opisanu u ovoj temi, pregledajte i primenite potrebne konfiguracije. Za više informacija pogledajte [Omogućite neskladišteni materijal i fakture dobavljača na čekanju](configure-materials-nonstocked.md). 

## <a name="post-a-project-related-pending-vendor-invoice"></a>Pošaljite fakturu dobavljača na čekanju u vezi sa projektom 

Fakture dobavljača na čekanju mogu se evidentirati na stranici **Fakture dobavljača na čekanju** (**Dugovanja** > **Fakture** > **Fakture dobavljača na čekanju**). Dovršite sledeće korake da biste knjižili fakturu dobavljača na čekanju u vezi sa projektom:

1. Idite na **Dugovanja** > **Fakture** i izaberite **Novo**. 
2. U polju **Račun fakture** izaberite dobavljača i u polje **Broj** unesite identifikaciju računa dobavljača.
3. Dodajte red na fakturu dobavljača i u polje **Broj predmeta** izaberite artikal na zalihama kupljen od dobavljača. 

    > [!NOTE]
    > Redovi faktura dobavljača koji se zasnivaju na kategoriji nabavke ne mogu se evidentirati u projektu. 
    
5. Dodajte kupljenu količinu. Sistem će popuniti jediničnu cenu na osnovu konfiguracije cene zaliha na zalihama. 
6. Potvrdite ukupan iznos i ostale potrebne detalje na liniji.
7. Na liniji detalji, na kartici **Projekat** odaberite ID projekta na koji će se snimati ova stavka.
8. Po želji odaberite broj aktivnosti i ažurirajte kategoriju projekta i svojstvo linije.
9. Pošaljite fakturu dobavljača na čekanju. Kada je faktura knjižena, sistem beleži:
    
    - Iznos bilansa dobavljača.
    - Iznos poreza na promet.
    - Troškovi projekta evidentiraju se na račun integracije nabavki.
    - Stvarna transakcija projekta u Dataverse. Ova transakcija se dalje obrađuje pomoću [Project Operations dnevnika integracije](../project-accounting/project-operations-integration-journal.md). Objavljivanjem ovog dnevnika premešta se iznos sa računa integracije nabavki na račun troškova projekta.
