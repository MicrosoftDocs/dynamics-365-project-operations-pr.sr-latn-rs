---
title: Korišćenje kategorije transakcije kao aspekta za određivanje cena
description: Ova tema pruža informacije o tome kako da koristite polje „Kategorija transakcije“ kao dimenzije za određivanje cena.
author: rumant
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ab8093aca9a33bbbaef41c6fc7d33cad930bfadd13b0f7587c3de9032ac0d630
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996138"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Korišćenje kategorije transakcije kao aspekta za određivanje cena


_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_


Ova tema objašnjava kako da koristite polje **Kategorija transakcije** kao dimenzije za određivanje cena. 

## <a name="prerequisites"></a>Preduslovi
Pre nego što dovršite procedure u ovoj temi, morate da imate novo rešenje dimenzije za formiranje cena za organizaciju. Ako ih već niste kreirali, pogledajte [Kreiranje prilagođenih polja i entiteta kao dimenzija za određivanje cena](create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>Dodavanje polja „Kategorija transakcije“ u obrasce i prikaze
Da bi polje **Kategorija transakcije** bilo vidljivo u rešenju dimenzija formiranja cena, morate da dodate polje svim obrascima i prikazima kao entitet.

Sledeća tabela navodi sve gotove obrasce i prikaze po entitetima. Takođe ćete morati da dodate novo polje u sve dodatne obrasce ili prikaze u vašim prilagođenim entitetima.

|  Entity        | Obrasci     |Prikazi        |
| ------------------------------|---------------------------------|----------------------------------|
|  Cena uloge| Informacija |- Aktivne cene kategorija resursa<br> - Vezano za cenu kategorije resursa |
|  Provizija na cenu uloge| Informacija|- Aktivne provizije na cenu uloge<br>- Vezano za proviziju na cenu uloge |
|  Detalj stavke ponude|- Informacije o projektu<br>- Brzo kreiranje projekta| - Aktivni detalj stavke ponude<br>- Kombinovani detalji stavke ponude<br>- Vezano za detalje stavki ponude |
|  Detalj predmeta ugovora za projekat|- Informacije o projektu<br>- Brzo kreiranje projekta|- Kombinovani detalji predmeta ugovora<br>- Aktivni detalji predmeta ugovora<br>- Vezano za detalje predmeta ugovora |
|  Projektni zadatak|- Informacija<br>- Novi obrazac| &nbsp; |
|  Član projektnog tima|- Informacija<br>- Novi obrazac|- Aktivni članovi projektnog tima<br>- Članovi projektnog tima<br>- Vezani članovi projektnog tima |
|  Stavka vremena|- Informacija<br>- Kreiranje stavke vremena|- Moje stavke vremena prema datumu<br>- Moje stavke vremena za ovu sedmicu<br>- Stavke vremena za odobrenje|
|  Stavka u glavnoj knjizi|- Informacija<br>- Brzo kreiranje|- Aktivne stavke u glavnoj knjizi<br>- Vezano za stavku u glavnoj knjizi|
|  Detalj stavke fakture|- Informacija<br>- Brzo kreiranje|- Aktivni detalj stavke fakture<br>- Naplative transakcije fakture<br>- Besplatne transakcije fakture<br>- Vezano za detalje stavki fakture <br>- Nenaplative transakcije fakture|
|  Stvarna vrednost|- Informacija<br>- Aktivne stvarne vrednosti| Vezane stvarne vrednosti |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>Podešavanje polja „Kategorija transakcije“ kao dimenzije određivanja cena

1. Idite na **Podešavanja** > **Parametri**. 
2. Na stranici **Parametri**, na kartici **Dimenzije za određivanje cena zasnovane na iznosima**, potvrdite da li mreža prikazuje zapise u entitetu **Dimenzije za određivanje cena**.
3. Dodajte **Kategorija transakcije** na ovu listu i podesite polja **Primenljivo na troškove** i **Primenjivo na prodaju** na **Da**.
4. U polju **Vrsta dimenzije** izaberite **Zasnovano na iznosu**, a zatim izaberite prioritet za stavku **Kategorija transakcije** jer je povezana sa troškovima i prodajom.


[!INCLUDE[footer-include](../includes/footer-banner.md)]