---
title: Upravljanje podugovorima u aplikaciji Project Operations
description: Ova tema pruža pregled procesa upravljanja podizvođačima od početka do kraja u usluzi Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994248"
---
# <a name="subcontract-management-in-project-operations"></a>Upravljanje podugovorima u aplikaciji Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Podugovaranje u usluzi Microsoft Dynamics 365 Project Operations podržava sledeće tokove poslovnih procesa.

![Tok procesa podugovaranja](../media/SubcontractingProcessFlow.png)

Evo detaljnog opisa procesa podugovaranja.

1. Rukovodilac projekta sklapa podugovor sa dobavljačem. Podrazumevano se cenovnici koji su priloženi evidenciji dobavljača koriste za podugovor. Račun dobavljača ima vrstu odnosa **Dobavljač** ili **Dobavljač**.
2. Rukovodilac projekta može da raščlani sve kupovine i stavi ih kao stavke u podugovoru. Stavke podugovora mogu da budu vezane za vreme, troškove ili proizvode. Klasa transakcije koja je izabrana za svaku stavku podugovora određuje čemu ta stavka služi.
3. Menadžer poslovnog kontakta dobavljača i rukovodilac projekta mogu da ponavljaju podugovor. Cene mogu da se prilagode u cenovnicima za kupovinu koji su priloženi podugovoru.
4. U ovom trenutku ili kasnije u toku procesa, ako se stavka podugovora odnosi na vreme, menadžer poslovnog kontakta dobavljača povezuje kontakte sa svakom stavkom podugovora. Ovo povezivanje pruža informacije rukovodiocu projekta koji radi na podugovoru. Kada je kontakt povezan sa stavkom podugovora, sistem automatski kreira resurs koji može da se rezerviše od kontakta, ako resurs koji može da se rezerviše već ne postoji.
5. Način naplate na svakoj stavci podugovora može da bude **Fiksna cena** ili **Vreme i materijal**. Za stavke podugovora sa fiksnom cenom možete da podesite raspored faktura na osnovu kontrolnih tačaka.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
