---
title: Režimi planiranja
description: Ova tema pruža informacije o režimima planiranja.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 508ff1df8f7e31066712fab6f8871dfdb107a43b
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116724"
---
# <a name="scheduling-modes"></a>Režimi planiranja

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_


Dynamics 365 Project Operations pruža mogućnost organizacijama da definišu kako upravljaju promenama ključnih promenljivih u zadacima unutar strukture raspodele rada. Na osnovu specifičnih potreba organizacije, projekt menadžeri mogu da izvrše promene u načinu raspoređivanja kada se projekat kreira.

U Project Operations dostupna su tri načina raspoređivanja:

  - Fiksno trajanje (ovo je podrazumevani režim)
  - Fiksno angažovanje (*Rad*)
  - Fiksne jedinice

Vrednosti na koje utiče definicija određenog režima rasporeda određuju se sledećom formulom:

  Angažovanje = Trajanje x Jedinice

Kada definišete režim zakazivanja projekta, postavljate jednu od ovih vrednosti, koje se potom ne mogu promeniti. Držanje ove vrednosti kao konstante stavlja prioritet na tu vrednost, što obaveštava sistem da je ne menja kada se promene druge dve vrednosti. Sledeća tabela pruža informacije o uticajima izbora određenog režima.

| **U ovom zadatku**             | **Ako revidirate jedinice**   | **Ako revidirate trajanje** | **Ako revidirate napor**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| Zadatak sa fiksnim jedinicama     | Trajanje je preračunato. | Napor se preračunava.    | Trajanje je preračunato. |
| Zadatak fiksnog angažovanja    | Trajanje je preračunato. | Jedinice se preračunavaju.    | Trajanje je preračunato. |
| Zadatak fiksnog trajanja  | Napor se preračunava.   | Napor se preračunava.    | Jedinice se preračunavaju.   |

Za više informacija o implikacijama datog režima pogledajte [Promenite tip zadatka za tačnije raspoređivanje](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72). U temi se pojam **Posao** koristi umesto **Napor**.

## <a name="change-the-organizations-scheduling-mode"></a>Promenite režim zakazivanja organizacije

Dovršite sledeće korake da biste definisali režim zakazivanja organizacije.

1. Idite na **Podešavanja** \> **Opšta** \> **Parametri**, a zatim izaberite parametar projekta. 
2. Na stranici **Parametri projekta** izaberite podrazumevani režim zakazivanja za organizaciju, a zatim definišite sposobnost da menadžer projekta zameni postavku prilikom kreiranja novog projekta.

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>Promenite postavku režima zakazivanja na projektu

Ako organizacija dozvoli menadžeru projekta da zameni zadati režim raspoređivanja, menadžer projekta može to promeniti kada kreira novi projekat. Međutim, nakon što je projekat sačuvan, režim zakazivanja ne može se promeniti.

## <a name="copied-projects"></a>Kopirani projekti

Budući da se projekat kreira kada se preduzme akcija kopiranja, menadžer projekta ne može da postavi režim zakazivanja. Odredišni projekat će se uvek podrazumevati za režim definisan na organizacionom nivou.

## <a name="copied-tasks"></a>Kopirani zadaci

Kada se zadatak kopira iz jednog projekta u drugi, zadatak nasleđuje režim rasporeda odredišnog projekta.
