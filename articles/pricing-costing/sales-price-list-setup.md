---
title: Podešavanje prodajnog cenovnika
description: Ova tema pruža informacije o radu sa prodajnim cenovnicima za određivanje cena proizvoda u projektu.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d2c797b72666123eb0a18d2d0c1df9fe3d207f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083635"
---
# <a name="sales-price-list-setup"></a>Podešavanje prodajnog cenovnika

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Za projektne ponude i ugovore, cenovnik projekta ima različit obrazac za zamenu cena u odnosu na cenovnik proizvoda. U stavci ponude zasnovanoj na katalogu proizvoda možete da zamenite cenu za uloge i kategorije direktno u stavci ponude, jer svaka stavka ponude ukazuje na tačno jednu stavku kataloga. Međutim, u stavci ponude zasnovanoj na projektu ne možete da zamenite cenu za uloge i kategorije direktno u stavci ponude. Cenovnik projekata možete koristiti za rad sa dva različita obrasca zamene.

> [!NOTE]
> Preporučujemo da imate poseban cenovnik za resurse projekta i stavke kataloga, zbog razlika u ponašanju između njih kada zamenite cene.

Svaki od sledećih entiteta može imati jednu ili više pridruženih cenovnika prodaje za cenu projekata:

- Klijent (poslovni kontakt) 
- Mogućnost za poslovanje 
- Ponuda 
- Ugovor za projekat

Povezivanje ovih entiteta sa cenovnikom je naznačeno cenovnikom projekta. Možete da povežete neke cenovnike sa entitetima prodaje Klijent, Mogućnost za poslovanje, Ponuda i Ugovor o projektu.

Podrazumevani cenovnik projekta se ne unosi automatski u zapis klijenta. Međutim, cenovnik projekta možete ručno priložiti zapisu klijenta. Ipak, trebalo bi ručno da priložite cenovnik projekta samo kada imate prilagođeni ugovor o određivanju cena sa klijentom. 

Kada je cenovnik projekta priložen entitetu prodaje, proveravaju se sledeće informacije:

- Da li cenovnik ima kontekst **prodaje**. 
- Da li se valuta cenovnika podudara sa valutom klijenta. 

U ugovoru o projektu se koristi sledeći redosled prioriteta da bi se automatski podesili povezani cenovnici projekta:

1. Ponuda
2. Mogućnost za poslovanje
3. Klijent 
4. Globalna podešavanja 

Kada se cenovnik projekta unese podrazumevano, sistem proverava da li se valuta podudara sa valutom klijenta i da li podrazumevani cenovnici koji su uneti imaju kontekst **prodaje**.

Možete da povežete više cenovnika projekta sa entitetima Klijent, Mogućnost za poslovanje, Ponuda i Ugovor o projektu. Ova mogućnost podržava podrazumevane cene za određeni datum za dugoročni ugovor o projektu, gde možete da zahtevate više od jednog cenovnika kako biste u obzir uzeli izmene cena do kojih dolazi zbog inflacije. Međutim, ako se za cenovnike koje povežete sa entitetom Klijent, Mogućnost za poslovanje, Ponuda ili Ugovor o projektu preklapaju datumi stupanja na snagu, podrazumevane cene mogu biti netačne. Zbog toga bi trebalo da proverite da cenovnici projekata sa datumima stupanja na snagu koji se preklapaju nisu povezani sa tim entitetima.
