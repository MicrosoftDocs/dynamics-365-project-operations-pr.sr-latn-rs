---
title: Otkazivanje prethodno odobrenih stavki vremena i troškova
description: Ova tema pruža informacije o tome kako se otkazuje odobreno vreme projekta i transakcija troškova.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bf3d146d2b07723b4d2e6e85eafd6f1b23b8b83f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014763"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>Otkazivanje prethodno odobrenih stavki vremena ili troškova

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

U najnovijoj verziji aplikacije Dynamics 365 Project Service Automation, davaoci odobrenja mogu da otkažu stavke za vreme ili troškove koje su prethodno odobrili.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>Otkazivanje prethodno odobrene stavke vremena ili troškova

Sledite ove korake da biste otkazali stavku vremena ili troškova koju ste prethodno odobrili.

1. Idite na **Projekti** \> **Moj posao** \> **Odobrenja**.
2. Na stranici liste **Odobrenja** promenite prikaz na **Moja prošla odobrenja**. Prikazuje se lista stavki vremena i troškova koje ste prethodno odobrili.
3. Izaberite jednu ili više stavki, a zatim **Otkaži odobrenje**. Dobićete poruku upozorenja.
4. Da biste otkazali odobrenje, izaberite **U redu**.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>Razumevanje uticaja otkazivanja odobrenja stavke vremena ili troškova

Kada se odobrenje otkaže, postoji i operativni i finansijski uticaj.

### <a name="operational-impact"></a>Operativni uticaj

Što se tiče operacija, kada se odobrenje otkaže, status zapisa će biti vraćen na **Radna verzija**, a odobravanje se više ne pojavljuje u prikazu **Moja poslednja odobravanja**. Umesto toga, otkazano odobrenje se pojavljuje u prikazu **Stavke vremena za odobrenje** ili **Stavke troškova za odobrenje**, u zavisnosti od toga da li se radi o stavci vremena ili stavci troškova. Pored toga, status povezane stavke vremena ili troškova se menja u **Prosleđeno**, tako da povezana stavka odgovara odobrenjima koja imaju status **Radna verzija**.

Kao davalac odobrenja, možete da uređujete neka od polja odobravanja koja imaju status **Radna verzija**. Ova polja obuhvataju stavke **Vrsta naplate** i **Naplativi sati za stavke vremena**. Nakon što unesete promene, možete ponovo da odobrite zapis. Druga mogućnost je da odbacite stavku. Ako odbacite odobravanje stavke vremena, status stavke će biti promenjen u **Vraćena**. Ako odbacite odobravanje stavke troškova, status stavke će biti promenjen u **Odbačena**. Sa funkcionalne strane, i vraćene i odbačene stavke se ponašaju isto kao stavka koja ima status **Radna verzija**. Član projektnog tima može da unese sve potrebne promene u stavku, a zatim da je ponovo prosledi na odobravanje ili da u potpunosti izbriše stavku.

### <a name="financial-impact"></a>Finansijski uticaj

Postoji i finansijski uticaj na projekat kada se odobrenje otkaže. Prvo, odgovarajuće stvarne vrednosti troškova i prodaje se ažuriraju na sledeći način:

- Status poravnanja se podešava na **Poravnato**.
- Status naplate se podešava na **Otkazano**.

Zatim, stavke storniranja se kreiraju u tabeli Stvarne vrednosti. Da bi sistem kreirao stavke storniranja, kopira vrednosti polja iz originalnih stvarnih vrednosti. Jedine vrednosti koje se ne kopiraju su vrednosti količine. Umesto toga, ove vrednosti se storniraju. Stornirane stvarne vrednosti se kreiraju za stvarne vrednosti **Troškovi** i **Nenaplaćena prodaja**. Polje **Status poravnanja** u storniranim stvarnim vrednostima je podešeno na **Ne može da se poravna**, a status naplate na **Otkazano**.

Nakon ovih izmena, iznos koji se evidentira kao potrošen za projekat i preostali prihodi od projekta više neće uzimati u obzir iznose koje ove stvarne vrednosti predstavljaju.


[!INCLUDE[footer-include](../includes/footer-banner.md)]