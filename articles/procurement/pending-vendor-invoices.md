---
title: Kupovima neskladištenog materijala ili kategorija nabavke koristeći fakturu dobavljača na čekanju
description: Ovaj članak objašnjava kako da snimite fakture dobavljača na čekanju.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1c05755f6759e90e031a11261f15a2c4b6b716e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922009"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Kupovima neskladištenog materijala ili kategorija nabavke koristeći fakturu dobavljača na čekanju

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Kako kompanija nabavlja materijal koji nije na zalihama ili kategorije nabavke za projekat, troškovi se mogu odmah evidentirati u odnosu na projekat. 

Na primer, preduzeće Contoso Robotics US izvodi projekat obnove opreme i potrebne su mu softverske licence. Ove licence se nabavljaju od nezavisnog dobavljača.  Koristeći Dynamics 365 Finance, službenik za dugovanja evidentira dokument fakture dobavljača na čekanju i pripisuje troškove licence direktno projektu obnove opreme. 

> [!IMPORTANT]
> Pre nego što upotrebite funkcionalnost opisanu u ovom članku, pregledajte i primenite potrebne konfiguracije. Više informacija potražite u članku [Omogućavanje materijala koji nisu na zalihama i faktura dobavljača na čekanju](configure-materials-nonstocked.md) i [Korišćenje kategorija nabavki sa porudžbenicama projekta i fakturama dobavljača na čekanju](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Pošaljite fakturu dobavljača na čekanju u vezi sa projektom 

Fakture dobavljača na čekanju mogu se evidentirati na stranici **Fakture dobavljača na čekanju** (**Dugovanja** > **Fakture** > **Fakture dobavljača na čekanju**). Dovršite sledeće korake da biste knjižili fakturu dobavljača na čekanju u vezi sa projektom:

1. Idite na **Dugovanja** > **Fakture** i izaberite **Novo**. 
1. U polju **Račun fakture** izaberite dobavljača, a zatim u polje **Broj** unesite identifikaciju računa dobavljača.
1. Dodajte red na fakturu dobavljača, a zatim u polje **Broj predmeta** izaberite artikal na zalihama koji je kupljen od dobavljača. Druga mogućnost je da u polju **Kategorija nabavke** izaberete kategoriju nabavke koja je kupljena od dobavljača.   
1. Dodajte količinu koja je kupljena. Sistem popunjava jediničnu cenu na osnovu konfiguracije cene zaliha na zalihama. 
1. Potvrdite ukupan iznos i ostale potrebne detalje na liniji.
1. Na detaljima reda, na kartici **Projekat** odaberite ID projekta na koji će se snimati ova stavka.
1. Opciono: Izaberite broj aktivnosti i ažurirajte kategoriju projekta i svojstvo linije.
1. Proknjižite fakturu dobavljača na čekanju. Kada se faktura knjiži, sistem evidentira sledeće informacije:
    
    - Iznos bilansa dobavljača.
    - Iznos poreza na promet.
    - Troškovi projekta evidentiraju se na račun integracije nabavki.
    - Transakcija stvarnih troškova projekta u usluzi Dataverse.  Ova transakcija se dalje obrađuje pomoću [Project Operations dnevnika integracije](../project-accounting/project-operations-integration-journal.md). Objavljivanjem ovog dnevnika premešta se iznos sa računa integracije nabavki na račun troškova projekta. 
    - Kupovine koje se klijentu projekta obračunavaju korišćenjem metode obračuna vremena i materijala. Osim toga, za kupovine u usluzi Dataverse kreiraju se transakcije nenaplaćene prodaje. Cenovnik proizvoda u usluzi Dataverse koristi se za prodajne cene i iznose za transakcije nenaplaćene prodaje.
