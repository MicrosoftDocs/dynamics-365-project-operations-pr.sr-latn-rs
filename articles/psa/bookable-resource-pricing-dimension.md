---
title: Korišćenje resursa koji se može rezervisati kao dimenzije za određivanje cena
description: Ova tema pruža informacije o korišćenju resursa koji se može rezervisati kao dimenzije za određivanje cena.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: c551673708ae2d965979136e92326be98252304a601964c1fbc52a329c592712
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988983"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>Korišćenje resursa koji se može rezervisati kao dimenzije za određivanje cena

[!include [banner](../includes/psa-now-project-operations.md)]

Ova tema pruža informacije o korišćenju resursa koji se može rezervisati kao dimenzije za određivanje cena. Pre nego što počnete, ako još niste kreirali rešenje sa dimenzijama za određivanje cena, moraćete da kreirate novo. Ako već imate rešenje sa dimenzijama za određivanje cena, onda možete da unesete promene u njega. Ako niste kreirali novo rešenje sa dimenzijama za određivanje cena za organizaciju, dovršite procedure u temi [Kreiranje prilagođenih polja i entiteta](create-custom-fields-entities.md).

## <a name="add-bookable-resource-to-forms-and-views"></a>Dodavanje resursa koji se može rezervisati u obrasce i prikaze
Da bi polja bila vidljiva u korisničkom interfejsu u rešenju za dimenziju određivanja cena, moraćete da prođete kroz sve obrasce i prikaze ključnih Project Service entiteta i dodate ta polja u obrasce i prikaze tih entiteta.
Sledeća tabela predstavlja sveobuhvatnu listu unapred definisanih obrazaca i prikaza koji su navedeni prema entitetu, a koji će morati da se ažuriraju. Ako postoje dodatni prikazi ili obrasci u okviru prilagođavanja za ove entitete, dodajte nova polja i u njih.
Otvorite istraživač rešenja za rešenje za dimenzije određivanja cena i zatim kliknite na **Objavi sva prilagođavanja**.


|   Entitet        | Obrasci   |Prikazi        |
| ------------------------------|---------------------------------|----------------------------------|
|  Cena uloge|• Informacije |• Aktivne cene kategorija resursa<br> • Vezani prikaz cena kategorija resursa|
|  Provizija na cenu uloge|• Informacije|• Aktivne provizije na cenu uloge<br>• Vezani prikaz provizija na cenu uloge|
|  Detalj stavke ponude|• Informacije o projektu<br>• Brzo kreiranje projekta|• Aktivni detalj stavke ponude<br>• Kombinovani detalji stavke ponude<br>• Vezani prikaz detalja stavki ponude|
|  Detalj predmeta ugovora za projekat|• Informacije o projektu<br>• Brzo kreiranje projekta|• Kombinovani detalji predmeta ugovora<br>• Aktivni detalji predmeta ugovora<br>• Vezani prikaz detalja predmeta ugovora|
|  Projektni zadatak|• Informacije<br>• Novi obrazac||
|  Član projektnog tima|• Informacije<br>• Novi obrazac|• Aktivni članovi projektnog tima<br>• Članovi projektnog tima<br>• Vezani prikaz članova projektnog tima|
|  Stavka vremena|• Informacije<br>• Kreiranje stavke vremena|• Moje stavke vremena prema datumu<br>• Moje stavke vremena za ovu sedmicu<br>• Stavke vremena za odobrenje|
|  Stavka u glavnoj knjizi|• Informacije<br>• Brzo kreiranje|• Aktivne stavke u glavnoj knjizi<br>• Vezani prikaz stavki u glavnoj knjizi|
|  Detalj stavke fakture|• Informacije<br>• Brzo kreiranje|• Aktivni detalji stavke fakture<br>• Naplative transakcije fakture<br>• Besplatne transakcije fakture<br>• Vezani prikaz detalja stavki fakture<br>• Nenaplative transakcije fakture|
|  Stvarno|• Informacije<br>• Aktivne stvarne vrednosti|• Vezani prikaz stvarnih vrednosti|

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>Podešavanje resursa koji se može rezervisati kao dimenzije za određivanje cena

1. U veb interfejsu idite na **Project Service** > **Podešavanja** > **Parametri**. Na stranici **Parametar**, na kartici **Dimenzije za određivanje cena zasnovane na iznosima**, primetićete da mreža na kartici prikazuje zapise u entitetu dimenzija za određivanje cena. 
2. Dodajte **Resurs koji se može rezervisati** na ovu listu dimenzija za određivanje cena kao **msdyn_bookableresource**. 
3. Naznačite kontekst u kome resurs koji može da se rezerviše funkcioniše kao dimenzija za određivanje cena i podesite vrednosti **Primenljivo na troškove** i **Primenljivo na prodaju**.
4. U polju **Vrsta dimenzije** izaberite **Zasnovano na iznosu**. 
5. Izaberite prioritet za troškove i prodaju za resurs koji se može rezervisati. Obično, kada ga uvrstite kao dimenziju za određivanje cena, resurs koji može da se rezerviše ima najviši prioritet, pa će njegovo podešavanje na **1** (ili **0**, zavisno od toga kako računate prioritet) obezbediti takvo ponašanje.

## <a name="set-up-pricing-dimension-field-names"></a>Podešavanje imena polja za dimenziju određivanja cena

Kada se ime polja dimenzije za određivanje cena u tabeli **Cena uloge** razlikuje od imena polja u bilo kom drugom entitetu koji gde je potrebno da podrazumevano određivanje cena funkcioniše, zapis dimenzije za određivanje cena mora da bude upoznat sa različitim imenima.    
Za resurs koji može da se rezerviše, entitet **Članovi projektnog tima** ima malo drugačije ime polja (**msdyn_bookableresourceid**) od onoga kako se zove u entitetu **Cena uloge** (**msdyn_bookableresource**). Zapis dimenzije za određivanje cena za **msydn_bookableresource** mora da bude svestan toga. 
1. Da biste to uradili, dvaput kliknite na red u mreži **Dimenzije za određivanje cena** da biste otvorili stranicu dimenzije polja **msdyn_bookableresource**.
2. Na stranici dimenzije, na kartici **Povezano** kliknite na **Imena polja dimenzija za određivanje cena**.

 ![Kartica Imena polja dimenzija za određivanje cena.](media/PD-fieldname.png)

4. U vezanom prikazu koji se otvara kliknite na **Dodaj novo ime polja dimenzije za određivanje cena**.

 ![Dodavanje novih imena polja dimenzije za određivanje cena.](media/Add-NewPD-fieldname.png)


Ovako otvarate stranicu **Novo ime polja dimenzije za određivanje cena** za **msdyn_bookableresource**. 

5. Dodajte **msdyn_projectteam** u polje **Logičko ime entiteta** i **msdyn_bookableresourceid** u polje **Ime polja**. Sačuvajte zapis.

 ![Obrazac za novo ime polja dimenzije za određivanje cena.](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]