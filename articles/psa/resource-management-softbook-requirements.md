---
title: Potrebe za uslovnim rezervisanjem
description: Ovaj članak pruža informacije o tome kako da rezervišete resurse prema potrebama za uslovnim rezervisanjem.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 8192047639823bc594803d6d10759be28f6db3ed
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928955"
---
# <a name="soft-book-requirements"></a>Potrebe za uslovnim rezervisanjem

[!include [banner](../includes/psa-now-project-operations.md)]

Potreba za resursom može se fiksno rezervisati. Fiksna rezervacija kreira predlog koji troši kapacitet resursa. Predlog se zatim vraća podnosiocu zahteva na odobrenje. Uslovno rezervisanje privremeno dodaje resurs u projektni tim i ima drugačiji status u tabeli rasporeda, ali ne troši kapacitet resursa. Da biste uslovno rezervisali resurs iz tabele rasporeda, podesite polje **Status rezervacije** na **Uslovna**.

![Status rezervacije je podešen na Uslovna.](media/Resource-Management-image77.png)

Kada kartica **Tim** ima prikaz **Imenovani članovi tima**, resurs se pojavljuje tamo. Uslovno rezervisani sati se evidentiraju u koloni **Uslovno rezervisani sati**.

![Uslovno rezervisani sati u prikazu Imenovani članovi tima.](media/Resource-Management-image78.png)

Uslovno rezervisani članovi tima mogu biti dodeljeni zadacima.

![Uslovno rezervisan član tima je dodeljen zadatku.](media/Resource-Management-image79.png)

Na kartici **Usaglašenost** nisu prikazane rezervacije uslovno rezervisanog resursa jer kartica **Usaglašenost** uzima u obzir samo fiksne rezervacije.

![Uslovno rezervisan resurs bez rezervacija na kartici Usaglašenost.](media/Resource-Management-image80.png)

> [!NOTE]
> Ne možete uslovno da rezervišete resurs iz potrebe koja je generisana od generičkog člana tima.

Na tabeli rasporeda upotrebljava se drugačija boja za uslovne rezervacije resursa.

![Uslovne rezervacije u tabeli rasporeda.](media/Resource-Management-image81.png)

Da biste uslovnu rezervaciju pretvorili u fiksnu, u tabeli rasporeda kliknite desnim tasterom miša na uslovna rezervacija, a zatim izaberite **Promeni status** \> **Fiksna rezervacija** \> **Fiksna**.

![Promena statusa rezervacije u Fiksna.](media/Resource-Management-image82.png)

Rezervacija je promenjena i status se menja u tabeli rasporeda. Pošto je status rezervacije sada **Fiksna**, resurs je prikazan kao rezervisan, a njegov kapacitet i dostupnost su prilagođeni.

Možete upotrebiti isti metod da otkažete fiksnu rezervaciju ili uslovnu rezervaciju u tabeli rasporeda.

Da biste pretvorili resurs koji je uslovno rezervisan u fiksno rezervisan na kartici projekta **Tim**, izaberite resurs, a zatim izaberite **Potvrdi**.

![Komanda za potvrdu.](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
