---
title: Sinhronizacija kapaciteta resursa
description: Ovaj članak pruža informacije o tome kako da sinhronizujete kapacitet resursa u kalendarima i projektima.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2b684833ffae83b7cedfc73ee96a8aa8ddd4ec57
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920721"
---
# <a name="synchronize-resource-capacity"></a>Sinhronizacija kapaciteta resursa

[!include [banner](../includes/banner.md)]

Procesi za sinhronizaciju resursa garantuju da će se informacije za kalendar i osnovni kalendar slivati u planiranje resursa projekta. Ako se kalendar promeni, procesi izvršavaju potrebna ažuriranja rasporeda resursa projekta. Procesi takođe pomažu u poboljšanju performansi, jer su informacije o resursima kalendara unapred sinhronizovane. Stoga se ažuriranja podataka o rasporedu resursa dešavaju brže. Preporučujemo da procese planirate kao pakete umesto kao jedan po jedan. U suprotnom, postoji rizik da će neko zaboraviti sve datume kada su informacije poslednji put sinhronizovane. Ako se ne koriste svi datumi, mogu se pojaviti praznine tokom sinhronizacije datuma.

![Sinhronizacija kalendara.](./media/projectresourcing04-1024x471.jpg)

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

[![Proces sinhronizacije.](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]