---
title: Kreirajte modele predviđanja za budžete projekata
description: Ova tema opisuje kako kreirati model predviđanja za preostale budžete.
author: Yowelle
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: c4467bc1c687b028f1cce8280c3cf0b5ef492b6fd1a024d49f001ce5ff8a34cb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986013"
---
# <a name="create-forecast-models-for-project-budgets"></a>Kreirajte modele predviđanja za budžete projekata 

[!include [banner](../includes/banner.md)]

Ova tema opisuje kako kreirati model predviđanja za preostale budžete. Projekat koji podleže budžetskoj kontroli koristi dve vrste budžeta: originalni i preostali. Kada kreirate budžet projekta, morate navesti modele predviđanja prvobitnog i preostalog budžeta koji su kreirani na stranici **Modeli predviđanja**. Budžeti projekata zasnovani na navedenim modelima kreiraju se kada dodelite budžet projekta.

> [!NOTE]
> Model prognoze koji se koristi za kontrolu budžeta ne može da ima podmodel ili da se koristi kao podmodel.

1. Izaberite **Upravljanje projektima i računovodstvo** > **Podešavanje** > **Prognoze**  > **Modeli predviđanja**.
2. Izaberite **Novo** da biste kreirali novi model prognoze, a zatim unesite ID broja modela i ime za novi model. 
3. Podesite opciju **Zaustavljeno** na **Da** kako bi se sprečile bilo kakve promene linija predviđanja za model prognoze. 
4. Ako linije predviđanja sa kojima je model povezan treba da generišu predviđanja novčanog toka u glavnoj knjizi, postavite **Uključi u predviđanja novčanog toka** na **Da.** 
5. Da biste koristili datum projekta kao datum fakture, podesite **Datum fakture prognoze** na **Da**. 
6. U polju **Tip budžeta** izaberite jedan od sledećih tipova modela:

   - **Originalni budžet**: Koristite originalne iznose budžeta koji su prosleđeni pri kreiranju i odobravanju početnog budžeta.
   - **Preostali budžet**: Koristite preostale iznose budžeta tokom trajanja projekta. Stanja u ovom modelu predviđanja smanjuju se stvarnim transakcijama, a povećavaju ili smanjuju revizijama budžeta.
   - **Prenos**: Koristite prenosne iznose budžeta za projekat. Prenos je opcioni postupak koji se može pokrenuti radi prenosa neiskorišćenih iznosa budžeta iz jedne fiskalne godine u drugu.

7. Po potrebi podesite sledeće opcije:

   - Da biste koristili datum projekta kao datum fakture, omogućite **Datum fakture prognoze**.
   - Omogućite **Prognoza pomoću WIP-a** za predviđanje na osnovu posla u toku (WIP), a zatim odaberite tip WIP-a. 
   - Možete zadržati podrazumevani **Tip budžeta** kao **Nijedan** ili unesite novi tip. Tip budžeta ne može se promeniti nakon što promenite zapis.     
    > [!NOTE]
    > Ako promenite podrazumevani tip budžeta, sve ostale opcije postaće nedostupne za ažuriranja i ne možete ponovo koristiti ovaj model predviđanja. 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]