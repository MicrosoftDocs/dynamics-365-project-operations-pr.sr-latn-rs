---
title: Sinhronizacija kapaciteta resursa
description: Ova tema pruža informacije o tome kako sinhronizovati kapacitet resursa u kalendarima i projektima.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6b63ccb5b0f04dedb8a942e22d6e1993204dc20
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288589"
---
# <a name="synchronize-resource-capacity"></a>Sinhronizacija kapaciteta resursa

[!include [banner](../includes/banner.md)]

Procesi za sinhronizaciju resursa garantuju da će se informacije za kalendar i osnovni kalendar slivati u planiranje resursa projekta. Ako se kalendar promeni, procesi izvršavaju potrebna ažuriranja rasporeda resursa projekta. Procesi takođe pomažu u poboljšanju performansi, jer su informacije o resursima kalendara unapred sinhronizovane. Stoga se ažuriranja podataka o rasporedu resursa dešavaju brže. Preporučujemo da procese planirate kao pakete umesto kao jedan po jedan. U suprotnom, postoji rizik da će neko zaboraviti sve datume kada su informacije poslednji put sinhronizovane. Ako se ne koriste svi datumi, mogu se pojaviti praznine tokom sinhronizacije datuma.

![Sinhronizacija kalendara](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Sinhronizacija zbirnih vrednosti kapaciteta resursa

Proces sinhronizacije je dizajniran da sinhronizuje sve informacije kalendara resursa. Ove informacije uključuju osnovne informacije o kalendaru o svim promenama u tabeli kapaciteta kalendara resursa projekta. Ako se u projekat dodaju novi resursi, sinhronizacija garantuje dostupnost ažuriranih informacija kalendara. Ova sinhronizacija se može izvršiti u bilo kom trenutku.

Preporučujemo da koristite paket. Opcije su dostupne tokom sinhronizacije rezervacija kapaciteta.

1. Izaberite **Upravljanje projektima i računovodstvo** &gt; **Periodično** &gt; **Sinhronizacija kapaciteta** &gt; **Sinhronizuj zbirne vrednosti kapaciteta resursa**.
2. Podesite opcije u sledećoj tabeli.

    | Opcija      | Opis |
    |-------------|-------------|
    | Šifra perioda | Opcionalno izaberite šifru intervala datuma glavne knjige da biste postavili datume početka i završetka procesa sinhronizacije za zbirne vrednosti kapaciteta resursa. |
    | Datum početka  | Unesite datum početka procesa sinhronizacije za zbirne vrednosti kapaciteta resursa. |
    | Datum završetka    | Unesite datum završetka procesa sinhronizacije za zbirne vrednosti kapaciteta resursa. |

[![Proces sinhronizacije](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]