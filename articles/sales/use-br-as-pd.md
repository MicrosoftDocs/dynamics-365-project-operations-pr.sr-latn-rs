---
title: Korišćenje resursa koji može da se rezerviše kao aspekta za određivanje cena
description: Ova tema pruža informacije o tome kako da koristite resurs koji se može rezervisati kao dimenzije za određivanje cena.
author: Rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: dcd01d80236f0218bc6fa3a1fe1389f8314f3c9b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598644"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>Korišćenje resursa koji može da se rezerviše kao aspekta za određivanje cena

 _**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_ 

Ova tema pruža informacije o tome kako da koristite resurs koji se može rezervisati kao dimenzije za određivanje cena. Ako je vaša strategija određivanja cena podešena tako da svaki resurs koji možete rezervirati mora da ima određenu cenu ili stopu troškova, koristite resurs koji možete rezervirati kao dimenziju formiranja cena.

## <a name="prerequisites"></a>Preduslovi
Pre nego što dovršite procedure u ovoj temi, morate da imate novo rešenje dimenzije za formiranje cena za organizaciju. Ako ih već niste kreirali, pogledajte [Kreiranje prilagođenih polja i entiteta](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>Dodavanje polja Resurs koji se može rezervisati u obrasce i prikaze
Da bi polje **Resurs koji se može rezervisati** bilo vidljivo u rešenju dimenzija formiranja cena, morate da dodate polje svim obrascima i prikazima kao entitet.

Sledeća tabela navodi sve gotove obrasce i prikaze po entitetima. Takođe ćete morati da dodate novo polje u sve dodatne obrasce ili prikaze u vašim prilagođenim entitetima.

|   Entity        | Obrasci   |Prikazi        |
| ------------------------------|---------------------------------|----------------------------------|
|  Cena uloge| Informacija | - Aktivne cene kategorija resursa<br> - Vezano za cenu kategorije resursa |
|  Provizija na cenu uloge| Informacija| - Aktivne provizije na cenu uloge<br>- Vezano za proviziju na cenu uloge |
|  Detalj stavke ponude| - Informacije o projektu<br>- Brzo kreiranje projekta| - Aktivni detalj stavke ponude<br>- Kombinovani detalji stavke ponude<br>- Vezano za detalje stavki ponude |
|  Detalj predmeta ugovora za projekat| - Informacije o projektu<br>- Brzo kreiranje projekta| - Kombinovani detalji predmeta ugovora<br>- Aktivni detalji predmeta ugovora<br>- Vezano za detalje predmeta ugovora |
|  Projektni zadatak| - Informacija<br>- Novi obrazac| &nbsp; |
|  Član projektnog tima| - Informacija<br>- Novi obrazac| - Aktivni članovi projektnog tima<br>- Članovi projektnog tima<br>- Vezani članovi projektnog tima |
|  Stavka vremena| - Informacija<br>- Kreiranje stavke vremena| - Moje stavke vremena prema datumu<br>- Moje stavke vremena za ovu sedmicu<br>- Stavke vremena za odobrenje|
|  Stavka u glavnoj knjizi| - Informacija<br>- Brzo kreiranje| - Aktivne stavke u glavnoj knjizi<br>- Vezano za stavku u glavnoj knjizi |
|  Detalj stavke fakture| - Informacija<br>- Brzo kreiranje| - Aktivni detalj stavke fakture<br>- Naplative transakcije fakture<br>- Besplatne transakcije fakture<br>- Vezano za detalje stavki fakture <br>- Nenaplative transakcije fakture|
|  Stvarna vrednost| - Informacija<br>- Aktivne stvarne vrednosti| Vezane stvarne vrednosti |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>Podešavanje resursa koji se može rezervisati kao dimenzije za određivanje cena
Da biste podesili resurs koji se može rezervisati kao dimenzije za određivanje cena, pratite ove korake:

1. Idite na **Podešavanja** > **Parametri**. 
2. Na stranici **Parametar**, na kartici **Dimenzije za određivanje cena zasnovane na iznosima**, potvrdite da li mreža prikazuje zapise u entitetu **Dimenzije za određivanje cena**. 
2. Dodajte **Resurs koji se može rezervisati** na ovu listu dimenzija za određivanje cena kao **msdyn_bookableresource**. 
3. U **Primenljivo na troškove** i **Primenljivo na prodaju**, izaberite vrednost.
4. U **Vrsta dimenzije**, izaberite **Zasnovano na iznosu**. 
5. Izaberite prioritet za troškove i prodaju za resurs koji se može rezervisati. Tipično, resurs koji se može rezervisati ima najveći prioritet kada je uključen kao dimenzija formiranja cena. Podesite prioritet na **1** (ili **0** u zavisnosti od toga kako računate prioritet) kako biste osigurali ovo ponašanje.

## <a name="set-up-pricing-dimension-field-names"></a>Podešavanje imena polja za dimenziju određivanja cena

Kada se ime polja dimenzije za određivanje cena u tabeli **Cena uloge** razlikuje od naziva polja u bilo kom drugom entitetu gde se koristi podrazumevano određivanje cena, zapis dimenzije za određivanje cena mora da bude upoznat sa različitim nazivima.  

Za resurs koji može da se rezerviše, entitet **Članova projektnog tima** ima malo drugačiji naziv polja od onoga kako se zove u entitetu **Cena uloge**: 

 - Entitet **Članovi projektnog tima** = **msdyn_bookableresourceid**
 - Entitet **Cena uloge** = **msdyn_bookableresource**

Zapis dimenzije za određivanje cena za **msydn_bookableresource** mora da bude obavešten o ovoj razlici.

1. Dvaput kliknite na red u mreži **Dimenzije za određivanje cena** da biste otvorili stranicu dimenzije polja **msdyn_bookableresource**.
2. Na stranici dimenzije, na kartici **Povezano** izaberite **Nazivi polja dimenzija za određivanje cena**.

  ![Kartica Imena polja dimenzija za određivanje cena.](media/PD-fieldname.png)

3. U vezanom prikazu koji se otvara izaberite **Dodaj novi naziv polja dimenzije za određivanje cena**.

  ![Dodavanje novih imena polja dimenzije za određivanje cena.](media/Add-NewPD-fieldname.png)

  Ovako otvarate stranicu **Novo ime polja dimenzije za određivanje cena** za **msdyn_bookableresource**. 

4. U stranici **Novi naziv polja dimenzije za određivanje cene**, dodajte **msdyn_projectteam** u **Logički naziv entiteta**.
5. Dodajte **msdyn_bookableresourceid** u **Naziv polja**.

 ![Obrazac za novo ime polja dimenzije za određivanje cena.](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]