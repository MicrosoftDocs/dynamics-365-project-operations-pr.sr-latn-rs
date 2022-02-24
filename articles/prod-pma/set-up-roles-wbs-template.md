---
title: Podesite uloge na predlošcima strukturne analiza posla
description: Ova tema pruža informacije o postavljanju informacija o ulogama na predlošcima strukturne analize posla.
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
ms.openlocfilehash: 143f1094c653fb7ac0e026b7875aa162a3eb83f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083560"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Podesite uloge na predlošcima strukturne analiza posla

[!include [banner](../includes/banner.md)]

Menadžeri projekata mogu postaviti predloške strukturne analize posla (WBS) koje mogu primeniti kada kreiraju WBS za nove projekte. Menadžeri projekata mogu da dodaju uloge kada kreiraju predložak. Koristite sledeći postupak za dodeljivanje uloge SAP predlošku.

1. Izaberite **Upravljanje projektima i računovodstvo** > **Podešavanje** > **Projekti** > **Predlošci strukturne analize posla**.
2. Izaberite **Detalji** za izabrani SAP predložak.
3. Izaberite zadatak sa liste, a zatim u polju **Uloga** izaberite ulogu koju želite da dodelite zadatku.

## <a name="work-with-a-wbs"></a>Rad sa SAP

Možete da kreirate novi SAP ili da ga kopirate iz postojećeg SAP predloška. Menadžer projekata može lako da upravlja resursima dodeljujući uloge novim zadacima na SAP-u. Uloge se mogu zameniti nakon sticanja resursa ili nakon identifikacije potvrđenog resursa za rad na zadatku. Ova fleksibilnost omogućava menadžerima projekata da izvršavaju sledeće zadatke:

- Identifikujte broj resursa potrebnih za SAP radne pakete.
- Procenite troškove projekta.
- Odredite preliminarni budžet.
- Procenite trajanje aktivnosti na osnovu uloga i resursa.
- Razvijte neke planove upravljanja projektom na osnovu dostupnih informacija o projektu.

Dodatne opcije su dodate u SAP radi boljeg korišćenja funkcionalnosti resursa.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opcija</th>
<th>Opis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Dodele resursa</td>
<td>Pogledajte dodeljene resurse, datume, broj sati i vrstu rezervacije za zadatke na SAP-u.</td>
</tr>
<tr class="even">
<td>Automatsko generisanje tima</td>
<td>Automatski dodajte planirane resurse pomoću uloga povezanih sa zadatkom. Finance automatski predlaže planirane resurse korišćenjem analize odluka sa više kriterijuma, zasnovane na ulogama. Kada se uloge i zalaganje (u satima) postave za zadatke u SAP-u i kada se objavi struktura, izaberite <strong>Automatski generiši tim</strong>. Potreban broj planiranih resursa dodaje se SAP-u i na karticu <strong>Zakazivanje projekata i timova</strong>.</td>
</tr>
<tr class="odd">
<td>Resurs (padajuća lista)</td>
<td>Na stranici <strong>Pokretanje dodele resursa</strong>, možete odabrati resurse za fiksno rezervisanje ili uslovno rezervisanje, na osnovu navedenog trajanja. Možete prilagoditi postavke prikaza da biste videli i postavili trajanje aktivnosti resursa. Možete izabrati i dodeliti resurse na nivou radnog paketa koristeći sledeće opcije:
<ul>
<li><strong>Prihvati</strong> – Potvrdite promene resursa koji je dodeljen zadatku.</li>
<li><strong>Otkaži</strong> – Otkažite promene resursa koji je dodeljen zadatku.</li>
<li><strong>Dodeli automatski</strong> – Dostupni resurs sa osobljem koji ima odgovarajuću ulogu automatski se bira i dodeljuje izabranom zadatku.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Na stranici **Svi projekti** izaberite projekat **Nadogradnja XYZ faza 2**.
2. Izaberite **Plan** > **Aktivnosti** > **Strukturna analiza posla**.
3. Izaberite **Novo** da biste dodali sledeće aktivnosti prvog nivoa u SAP:

    - Pokretanje
    - Planiranje
    - Izvršavanje
    - Nadgledanje i kontrola
    - Zatvaranje

4. Podesite datume i zalaganje (u satima), kao što je prikazano na sledećoj ilustraciji.

    [![Određivanje datuma i zalaganja](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Izaberite red zadatka **Pokretanje**, a zatim u polju **Uloga** izaberite **Viši menadžer projekta**.
6. Izaberite **Objavi**.
7. Na istoj liniji, u polju **Resurs** izaberite **Danijel Goldšmit**, a zatim izaberite **Prihvati**.
8. Izaberite red zadatka **Planiranje**, a zatim u polju **Uloga** izaberite **Poslovni analitičar**.
9. Izaberite **Objavi**, a zatim izaberite **Automatski generiši tim**.
10. U okviru poruke koji se prikaže, izaberite **Da**.
11. U polju **Resurs** proverite da li je vrednost **Poslovni analitičar 1**.
12. Za resurs **Poslovni analitičar 1**, otvorite pronalaženje i izaberite **Pokreni dodelu resursa**. Zatim izaberite radnika za zadatak.
13. Izaberite **Uslovno dodeljivanje** &gt; **Puni kapacitet**.

    > [!NOTE] 
    > Nećete dobiti upozorenje da je navedeni resurs sada 2, jer broj resursa ostaje 1.

14. Na stranici **Strukturna analiza posla** potvrdite dodeljivanje resursa na SAP-u, a zatim izaberite **Sačuvaj**.
