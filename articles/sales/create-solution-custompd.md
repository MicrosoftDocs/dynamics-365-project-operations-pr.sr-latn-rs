---
title: Kreiranje rešenja za prilagođene dimenzije određivanja cena
description: Ova tema pruža informacije o tome kako da kreirate rešenja za prilagođene dimenzije određivanja cena.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441501dff23d16960381b3f9fb4b2cceba2b3ba5
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514019"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Kreiranje rešenja za prilagođene dimenzije određivanja cena

 _**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_ 

>[!IMPORTANT]
>Sve promene prilagođenih dimenzija cene treba da budu u zasebnom rešenju. Ova važna najbolja praksa omogućava fleksibilnost za ažuriranje ili uklanjanje promena po potrebi, pomaže pri ponovnoj upotrebi posla i olakšava prilagođavanje ovih promena drugim instancama. Nakon što unesete sve potrebne promene, izvezite ovo rešenje kao **Kompletno** rešenje, pa ga uvezete u druge instance da biste ga ponovo koristili.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Kreiranje rešenja za prilagođene dimenzije određivanja cena

1.  Izaberite **Podešavanja** > **Rešenja**, a zatim izaberite **Novo**.
2.  Imenujte rešenje, *<your organization name> dimenzije za određivanje cena*.
3. Unesite preostale potrebne informacije, a zatim izaberite **Sačuvaj**.

  ![Kreiranje rešenja za prilagođene dimenzije za određivanje cena](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Dodajte sve zahtevane entitete i srodne komponente u rešenje za dimenzije cene

Dodajte sledeće Project Service entitete u svoje rešenje za određivanje cena da biste uneli važne promene u šemi u rešenju za određivanje cena. Nakon što završite ovaj postupak, entiteti će prepoznati nove dimenzije za određivanje cena.

1.  Izaberite **Podešavanja** > **Rešenja**, a zatim kliknite dvaput na **<*naziv vaše organizacije*> dimenzije za određivanje cena**.
2.  U levom oknu za navigaciju istraživača rešenja izaberite **Dodaj postojeće** > **Entiteti**.
3.  U dijalogu **Komponente rešenja** izaberite sledeće entitete:
 
   - **Stvarna vrednost**
   - **Resurs koji može da se rezerviše**
   - **Stavka procene**
   - **Projektni zadatak**
   - **Detalj stavke fakture**
   - **Stavka u glavnoj knjizi**
   - **Detalj predmeta ugovora za projekat**
   - **Član projektnog tima**
   - **Detalj stavke ponude**
   - **Provizija na cenu uloge**
   - **Cena uloge**
   - **Stavka vremena**
 
   ![Dodavanje rešenja sa prilagođenom dimenzijom određivanja cena postojećim entitetima](./media/Existing-entities-to-PD-solution.png)
 
 4. Za svaki entitet, pregledajte komponente koje se dodaju i konačnu listu sredstava entiteta za svaki entitet. 

   >[!NOTE]
   > Uključite sve obrasce i prikaze za svaki od izabranih entiteta.

  ![Dodati entiteti](./media/solution-component-selection.png)


5.  Kada se od vas zatraži da uključite bilo koji zavisni entitet za izabrane entitete, izaberite **Ne, ne uključuj obavezne komponente.**

    ![Uključivanje zavisnih entiteta](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]