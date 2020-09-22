---
title: Prodajne procene i projekti
description: Ova tema pruža informacije o tome kako iskoristiti raspored i procene u procesu prodaje.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: eb5ab6a1-fdff-490e-9c2a-19aef493de11
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 4431c1c894a01bfecc132575d8981ebc9fe50b51
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755144"
---
# <a name="sales-estimates-and-projects"></a>Prodajne procene i projekti

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Tokom procesa prodaje možete kreirati procene prodaje povezujući projekat s prodajnom ponudom. Na ovaj način, može da dođe do determinističke procene tokom procesa prodaje, kako bi se iskoristile prednosti zakazivanja projekata i procene. Ako prodaja prođe, raspored koji je korišćen za procenu prodaje može se koristiti kao osnova za dalje preciziranje projektnog plana.

## <a name="linking-a-project-to-a-quote-line"></a>Povezivanje projekta sa stavkom ponude

Kada kreirate stavku ponude zasnovanu na projektu, možete da kreirate novi projekat ili povežete postojeći projekat na stranici **Stavka projekta**. 

> ![Obrazac stavke ponude](media/project-8.png)
 
Kada kreirate novi projekat iz detalja stavke ponude, možete iskoristiti predloške projekta. Predlošci projekata su modeli projekata koji predstavljaju standardne planove projekata i finansijske procene tipične za organizaciju. Takođe mogu predstavljati kopije projektnih planova i procena iz prošlih projekata.

> ![Detalji stavke ponude](media/project-9.png)
  
Kada kreirate projekat iz ponude, projekat se automatski povezuje sa stavkom ponude.

## <a name="components-of-estimates-in-a-project"></a>Komponente procena u projektu

Raspored vam omogućava da podelite posao na zadatke, održavate hijerarhiju zadataka, odredite koji su resursi potrebni za obavljanje zadatka i dodelite procenu potrebnih aktivnosti za obavljanje zadatka.

Možete definisati radne aktivnosti i procene rasporeda pomoću polja na kartici **Raspored** u okviru stranice **Projekat**. Pošto je cenovnik povezan sa projektom, finansijske procene se izračunavaju korišćenjem cene koštanja i prodajne cene koje su definisane u cenovniku.

## <a name="importing-estimates-from-a-project-into-a-quote"></a>Uvoz procena iz projekta u ponudu

Nakon što definišete procene projekta, možete ih uvesti u stavku ponude. Na stranici **Detalji stavke ponude** izaberite **Uvoz iz procena** na traci da biste rezimirali procene projekta prema vrsti transakcije, ulozi ili nivou zadatka.
