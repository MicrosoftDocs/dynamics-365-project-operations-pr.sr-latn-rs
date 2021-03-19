---
title: Pregled preostalog fakturiranja za projekte i ugovore o projektima
description: Ova tema pruža informacije o tome kako pregledati preostalo vreme, troškove i proizvode i kako ih označiti kao spremne za fakturiranje.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: bdeeb100614cda78d0ba536310bb6b411c863b71
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282800"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>Pregled preostalog fakturiranja za projekte i ugovore o projektima

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Kada transakcija bude bila spremna za kreiranje i obradu fakture, transakcija treba biti obeležena kao **Spremno za fakturiranje**. Ova tema opisuje vrste transakcija koje se mogu kreirati.

## <a name="review-the-time-and-material-billing-backlog"></a>Pregled preostale naplate vremena i materijala

Kada se stavka vremena i troškova prosledi i odobri za projekt, PSA kreira stvarnu vrednost projekta. Ako se kombinacija projekta i klase transakcije mapiraju u predmet ugovora za projekat zasnovan na vremenu i materijalu, kada se stavka odobri, kreiraju se dve stvarne vrednosti:

- Stvarna vrednost troškova 
- Stvarna vrednost nenaplaćene prodaje

Stvarne vrednosti nenaplaćene prodaje predstavljaju preostalu naplatu i njihov status naplate mora biti podešen na **Spremno za fakturisanje**. Kada se kreira faktura za projekat, stvarne vrednosti nenaplaćene prodaje označene kao **Spremno za fakturisanje** kopiraju se kao detalji stavke fakture.

Da biste pregledali preostale naplate za vreme i materijale, idite na **Prodaja** \> **Naplata** \> **Preostala naplata vremena i materijala**. Odaberite sve stvarne vrednosti nenaplaćene prodaje koje su spremne za fakturisanje, a zatim izaberite **Spremno za fakturisanje**. Status naplate ovih stvarnih vrednosti je promenjen u **Spremno za fakturisanje**.

![Preostala naplata vremena i materijala](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>Pregled preostale naplate za proizvod

U aplikaciji PSA, kada projektni ugovor ima predmete ugovora zasnovane na proizvodima, ti predmeti se uzimaju u obzir za fakturisanje svaki put kada se kreira faktura za projektni ugovor. Svaki proizvod koji ima predmete ugovora obeležene kao **Spremno za fakturisanje** kopira se u fakturu projekta kao stavke fakture za projekat.

Da biste pregledali preostalu naplatu za proizvod, idite na **Prodaja** \> **Naplata** \> **Preostala naplata za proizvod**. Odaberite sve predmete ugovora zasnovane na proizvodima koji su spremni za fakturisanje, a zatim izaberite **Spremno za fakturisanje**. Status naplate ovih stavki je promenjen u **Spremno za fakturisanje**.

![Preostala naplata za proizvod](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>Preged kontrolnih tačaka naplate u ugovorima sa fiksnom cenom

Svaki predmet ugovora za projekat koji koristi način naplate fiksne cene mora definisati kontrolne tačke u ugovoru. Ove kontrolne tačke u ugovoru mogu se fakturisati samo ako su označene kao **Spremno za fakturisanje**. 

Da biste pregledali kontrolne tačke naplate, idite na **Prodaja** \> **Naplata** \> **Kontrolne tačke sa fiksnom cenom**. Odaberite kontrolne tačke koje su spremne za fakturisanje, a zatim izaberite **Spremno za fakturisanje**. Status naplate ovih kontrolnih tačaka je promenjen u **Spremno za fakturisanje**.

![Kontrolne tačke sa fiksnom cenom](media/FPBacklog.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]