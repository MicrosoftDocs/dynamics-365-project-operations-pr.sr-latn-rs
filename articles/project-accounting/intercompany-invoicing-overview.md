---
title: Pregled internog fakturisanja u okviru preduzeća
description: Ova tema pruža informacije i primere o internom fakturisanju između preduzeća za projekte.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3ad75089de1a2f99646f7aba213e199a2bec347d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287345"
---
# <a name="intercompany-invoicing-overview"></a>Pregled internog fakturisanja u okviru preduzeća

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Vaša organizacija može imati više odeljenja, podružnica i drugih pravnih lica koja međusobno prenose proizvode i usluge za projekte. Pravno lice koje pruža uslugu ili daje proizvod naziva se *pravno lice koje pozajmljuje*. Pravno lice koje prima uslugu ili proizvod naziva se *pravno lice koje se zadužuje*.

Sledeća ilustracija prikazuje tipični scenario kada dva pravna lica, Contoso Robotics USA (pravno lice koje se zadužuje) i Contoso Robotics UK (pravno lice koje pozajmljuje) dele resurse kako bi isporučili projekat klijentu, Adventure works. Za ovaj scenario, Contoso Robotics USA po ugovoru treba da isporuči posao preduzeću Adventure Works.

![Interno fakturisanje u okviru preduzeća](./media/IntercompanyScenario.png) 

Dynamics 365 Project Operations koristi sledeći tok za obradu transakcija između preduzeća:

1. Resursi pravnog lica koje daje pozajmice evidentiraju transakcije vremena ili troškova između preduzeća prema vremenu i trošku rezervacije u osnovu na projekte pravnog lica koje se zadužuje.
2. Troškovi vremena i troškova evidentiraju se u preduzeću koje pozajmljuje korišćenjem jediničnog cenovnika troškova preduzeća koje se zadužuje.
3. Nenaplaćene prodajne transakcije između preduzeća evidentiraju se u kompaniji koja pozajmljuje korišćenjem jediničnog cenovnika troškova preduzeća koje se zadužuje.
4. Nefakturisani prihod se evidentira u preduzeću koje se zadužuje koristeći cenovnik prodajnih cena po ugovoru o projektu. Klijentu možete naplatiti kada se evidentira nefakturisani prihod. Klijent ne mora da čeka dok se obrada faktura između preduzeća ne završi.
5. Fakture klijenata između preduzeća se kreiraju periodično u preduzeću koje pozajmljuje. Fakture se kreiraju ručno ili korišćenjem periodičnog automatizovanog procesa. Za svako pravno lice koje se zadužuje možete kreirati pojedinačnu fakturu ili zasebne fakture mogu biti kreirane projektom.
6. Kada se faktura klijenta između preduzeća knjiži u pravnom licu koje pozajmljuje, u pravnom licu koje se zadužuje kreira se odgovarajuća faktura dobavljača na čekanju. Troškovi na fakturi dobavljača na čekanju evidentiraće se u potknjizi projekta kada se faktura proknjiži.

Sledeći dijagram ilustruje fakturisanje između preduzeća koje se odnosi na računovodstvene događaje i očekivana knjiženja u glavnu knjigu.

![Tok između preduzeća](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Dodatni resursi

- [Konfigurisanje internog fakturisanja u okviru preduzeća](configure-intercompany-invoicing.md)
- [Evidentiranje transakcija u okviru preduzeća](create-intercompany-transactions.md)
- [Kreiranje internih faktura klijenta i dobavljača u okviru preduzeća](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]