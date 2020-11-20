---
title: Korišćenje kategorije transakcije kao dimenzije određivanja cena
description: Ova tema pruža informacije o korišćenju kategorije transakcije kao dimenzije za određivanje cena.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 0019571a1d37d3b6a503e7221db3c3b51365c236
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083664"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Korišćenje kategorije transakcije kao dimenzije određivanja cena
Ova tema pokazuje kako da koristite kategorije transakcije kao dimenzije za određivanje cena. Pre nego što počnete, ako još niste kreirali rešenje sa dimenzijama za određivanje cena, moraćete da kreirate novo. Ako već imate rešenje sa dimenzijama za određivanje cena, onda možete da unesete promene u njega. Ako niste kreirali novo rešenje sa dimenzijama za određivanje cena za organizaciju, dovršite procedure u temi [Kreiranje prilagođenih polja i entiteta](create-custom-fields-entities.md).

## <a name="add-transaction-category-to-forms-and-views"></a>Dodavanje kategorije transakcije u obrasce i prikaze
Da bi kategorija transakcije bila vidljiva u korisničkom interfejsu u rešenju za dimenziju određivanja cena, moraćete da prođete kroz sve obrasce i prikaze ključnih entiteta i dodate ta polja u obrasce i prikaze tih entiteta.
Sledeća tabela predstavlja sveobuhvatnu listu unapred definisanih obrazaca i prikaza koji su navedeni prema entitetu, a koji će morati da se ažuriraju pomoću novih polja. Ako postoje dodatni prikazi ili obrasci u okviru prilagođavanja za ove entitete, dodajte nova polja i u njih.

|  Entitet        | Obrasci     |Prikazi        |
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

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>Podešavanje kategorije transakcije kao dimenzije određivanja cena

1. U veb interfejsu idite na **Project Service** > **Podešavanja** > **Parametri**. 
2. Na stranici **Parametri** , na kartici **Dimenzije za određivanje cena zasnovane na iznosima** , primetićete da mreža na kartici prikazuje zapise u entitetu **Dimenzije za određivanje cena**.
3. Dodajte **Kategorija transakcije** na ovu listu i podesite polja **Primenljivo na troškove** i **Primenjivo na prodaju** na **Da**.
4. U polju **Vrsta dimenzije** izaberite **Zasnovano na iznosu** , a zatim izaberite prioritet za stavku **Kategorija transakcije** koja je povezana sa troškovima i prodajom.