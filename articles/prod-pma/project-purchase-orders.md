---
title: Porudžbenice za projekat
description: Ovaj članak opisuje razne metode pomoću kojih možete da kreirate porudžbenice za projekat. Način koji koristite zavisi od svrhe porudžbenice i od toga kada se kupljene stavke koriste i naplaćuju projektu.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd891aec5bcab66c5801a5d9ca8abbbf632d662d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083568"
---
# <a name="purchase-orders-for-a-project"></a>Porudžbenice za projekat

[!include [banner](../includes/banner.md)]

Ovaj članak opisuje razne metode pomoću kojih možete da kreirate porudžbenice za projekat. Način koji koristite zavisi od svrhe porudžbenice i od toga kada se kupljene stavke koriste i naplaćuju projektu.

### <a name="methods-for-creating-a-purchase-order"></a>Metode za kreiranje porudžbenice

Možete da koristite jedan od sledećih metoda za kreiranje porudžbenice u upravljanju projektima i računovodstvu. Svrha porudžbenice određuje kada se porudžbenica koristi i, stoga, kada se stavke naplaćuju projektu.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Metod</th>
<th>Svrha</th>
<th>Potrošnja stavki</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kreirajte porudžbenicu direktno iz projekta.</td>
<td>Ovu metodu koristite za kupovinu stavki od spoljnog prodavca za potrošnju na projektu. Porudžbenicu možete kreirati na dva načina:
<ul>
<li>Iz samog projekta. U ovom slučaju, projekat je već definisan za porudžbenicu.</li>
<li>Navigacijom do porudžbenice za projekat. Morate izabrati prodavca i projekat za koji ćete kreirati porudžbenicu.</li>
</ul></td>
<td>Stavke se koriste kada se faktura dobavljača ažurira.</td>
</tr>
<tr class="even">
<td>Kreirajte porudžbenicu direktno iz ulazne porudžbine.</td>
<td>Koristite ovaj metod za kupovinu stavki kada kreirate ulaznu porudžbinu iz projekta.</td>
<td>Stavke se koriste kada se porudžbenica fakturiše klijentu.</td>
</tr>
<tr class="odd">
<td>Kreirajte porudžbenicu na osnovu zahteva za stavku.</td>
<td>Koristite ovaj metod za kupovinu stavki kada kreirate zahtev za stavku iz projekta.</td>
<td>Stavke se koriste kada se ažurira otpremnica zahteva.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Kada ažurirate fakturu dobavljača ili otpremnicu, od vas će se zatražiti da ažurirate otpremnicu prema zahtevu za stavku.

Za više informacija pogledajte [Prijem stavki po porudžbenici iz zahteva za stavku](tasks/receive-items-purchase-order-item-requirement.md).
