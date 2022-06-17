---
title: Podešavanje prodajnog cenovnika
description: Ovaj članak pruža informacije o prodajnim cenama za cene projekata.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1892607ac121e23a05cd45bc05d4e23ea84690b4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923067"
---
# <a name="set-up-a-sales-price-list"></a>Podešavanje prodajnog cenovnika

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]