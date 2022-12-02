---
title: Kreiranje prilagođenih rešenja za dimenzije cene
description: U ovom članku se objašnjava kako se kreira prilagođeno rešenje prilikom kreiranja prilagođenih dimenzija cene.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 0df6728634b169c8a1a128aba1555d79fee5719f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929047"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Kreiranje prilagođenih rešenja za dimenzije cene

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> Sve promene prilagođenih dimenzija cene treba da budu u zasebnom rešenju. Ova važna najbolja praksa pruža fleksibilnost u budućnosti za ažuriranje ili uklanjanje promena po potrebi, pomoći će pri ponovnoj upotrebi posla i olakšava prilagođavanje ovih promena drugoj instanci. Kada unesete sve potrebne promene, izvezite ovo rešenje kao **Kompletno rešenje** i uvezite ga u druge instance da biste ponovo koristili podešavanje za određivanje cena.

1. Izaberite **Podešavanja** > **Rešenja**, a zatim izaberite **Novo**. 
2. Imenujte rešenje, **\<your organization name> dimenzije za određivanje cena**, unesite preostale zahtevane informacije, a zatim izaberite **Sačuvaj**.

> ![Kreiranje prilagođenog rešenja za dimenzije za određivanje cena.](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Dodajte sve zahtevane entitete i srodne komponente u rešenje za dimenzije cene
Moraćete da dodate sledeće Project Service entitete u rešenje za određivanje cena. Dovršite korake u ovoj proceduri da biste napravili neke važne promene šema u rešenju za određivanje cena, tako da entiteti postanu svesni novih dimenzija cene.

1. Izaberite **Podešavanja** > **Rešenja**, a zatim dvaput kliknite na **\<your organization name> dimenzije za određivanje cena**. 
2. U levom oknu za navigaciju istraživača rešenja izaberite **Dodaj postojeće** > **Entiteti**.
3. U dijalogu **Komponente rešenja** izaberite sledeće entitete:

- Stvarna vrednost
- Resurs koji može da se rezerviše
- Stavka procene
- Projektni zadatak
- Detalj stavke fakture
- Stavka u glavnoj knjizi
- Detalj predmeta ugovora za projekat
- Član projektnog tima
- Detalj stavke ponude
- Provizija na cenu uloge
- Cena uloge 
- Stavka vremena 

> ![Dodavanje postojećih entiteta u rešenje za dimenzije određivanja cena.](media/Existing-entities-to-PD-solution.png)

> ![Izaberite komponente rešenja.](media/Dimension-Components.png)

> [!NOTE]
> Obavezno uključite sve obrasce i prikaze za svaki od izabranih entiteta.

4. Kada se od vas zatraži da uključite zavisne entitete za izabrane entitete, izaberite **Ne**.

> ![Nemojte da uključujete sve povezane komponente.](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
