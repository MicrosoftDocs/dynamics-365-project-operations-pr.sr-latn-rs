---
title: Korišćenje kategorije transakcije kao dimenzije određivanja cena
description: Ovaj članak pruža informacije o korišćenju kategorije transakcije kao dimenzije cena.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 1a1c2dc17c2092e5364d90e7efc1f13aee80703e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915753"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Korišćenje kategorije transakcije kao dimenzije određivanja cena

[!include [banner](../includes/psa-now-project-operations.md)]

Ovaj članak prikazuje kako se kategorija transakcije koristi kao dimenzija određivanja cena. Pre nego što počnete, ako još niste kreirali rešenje sa dimenzijama za određivanje cena, moraćete da kreirate novo. Ako već imate rešenje sa dimenzijama za određivanje cena, onda možete da unesete promene u njega. Ako niste kreirali novo rešenje dimenzije cena za vašu organizaciju, dovršite procedure u članku [Kreiranje prilagođenih polja i entiteta](create-custom-fields-entities.md).

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
2. Na stranici **Parametri**, na kartici **Dimenzije za određivanje cena zasnovane na iznosima**, primetićete da mreža na kartici prikazuje zapise u entitetu **Dimenzije za određivanje cena**.
3. Dodajte **Kategorija transakcije** na ovu listu i podesite polja **Primenljivo na troškove** i **Primenjivo na prodaju** na **Da**.
4. U polju **Vrsta dimenzije** izaberite **Zasnovano na iznosu**, a zatim izaberite prioritet za stavku **Kategorija transakcije** koja je povezana sa troškovima i prodajom.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
