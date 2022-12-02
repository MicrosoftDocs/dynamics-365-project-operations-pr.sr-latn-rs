---
title: Upravljanje cenovnikom za kupovinu i cenovnikom dobavljača u usluzi Project Operations
description: Ovaj članak pruža informacije koje će vam pomoći da kreirate i održavate podatke o dobavljačima i cenovnike za kupovinu za podugovaranje.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3cd883fed8a59f1c54c39e2d051b9748833ba692
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261905"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Upravljanje cenovnikom za kupovinu i cenovnikom dobavljača u usluzi Project Operations


_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

## <a name="vendors-in-project-operations"></a>Dobavljači u usluzi Project Operations

U usluzi Microsoft Dynamics 365 Project Operations, poslovni kontakti dobavljača imaju tip odnosa **Prodavac** ili **Dobavljač**. Možete da izaberete samo zapis poslovnog kontakta koji ima jedan od ovih tipova odnosa kao dobavljač na podugovoru.

Možete povezati jedan ili više cenovnika za kupovinu sa podacima o dobavljaču. Međutim, svaki cenovnik za kupovinu koji je povezan sa zapisom dobavljača treba da ima različite periode važenja. Usluga Project Operations ne podržava preklapanje perioda važenja za cenovnike za kupovinu.

Podrazumevano se sledeća polja i koncepti u zapisu dobavljača koriste za sve podugovore koji su kreirani za dobavljača:

- Uslovi plaćanja
- Kontakt za fakturisanje
- Primarni kontakt

    > [!NOTE]
    > Podrazumevano se primarni kontakt dobavljača koristi kao menadžer poslovnog kontakta dobavljača za podugovor.

- Valuta
- Aktuelni cenovnici za kupovinu

## <a name="purchase-price-lists-in-project-operations"></a>Cenovnici za kupovinu u usluzi Project Operations

Cenovnik u kojem je polje **Kontekst** podešeno na **Kupovina** smatra se cenovnikom za kupovinu. Cenovnici za kupovinu mogu se definisati tako da predstavljaju katalog otkupnih cena za vreme, troškove i materijale. Cenovnici za kupovinu podsećaju na kupovne cenovnike i cenovnike troškova u usluzi Project Operations. Sledeći koncepti se primenjuju na cenovnike za kupovinu na isti način na koji se primenjuju na na kupovne cenovnike i cenovnike troškova:

- **Period važenja** – Cenovnici za kupovinu imaju period važenja. Period važenja predstavljaju polja datuma početka i datuma završetka na svakom cenovniku. Vreme između datuma početka i datuma završetka je period važenja.
- **Valuta** – Valuta u zaglavlju cenovnika se koristi kao valuta u kojoj su izražene cene za kupovinu za rad, kategorije troškova i proizvoda u katalogu.
- **Podrazumevana jedinica vremena** – Podrazumevana jedinica vremena izražava cene rada za kupovine. Polje vremenske jedinice na cenovniku se koristi samo za podrazumevane vrednosti. Ta vrednost se može promeniti u pojedinačnim redovima cena za ulogu.

Cenovnici za kupovinu mogu se pridružiti evidenciji dobavljača kao prilozi koji su poznati kao cenovnici projekata. Ovi cenovnici se koriste za unos podrazumevanih cena za stavke podugovora. Podrazumevano, kada je više cenovnika za kupovinu povezano sa zapisom dobavljača, najnoviji cenovnik se koristi za podugovore koji se kreiraju za dobavljača. Samo cenovnici u kojima je polje **Kontekst** podešeno na **Kupovina** mogu se priložiti evidenciji dobavljača.

### <a name="subcontract-specific-purchase-price-lists"></a>Cenovnici za kupovinu specifični za podugovore

Cenovnici za kupovinu takođe se mogu se pridružiti podugovorima kao prilozi koji su poznati kao cenovnici projekata. Ovi cenovnici se koriste za unos podrazumevanih cena za stavke podugovora. Podrazumevano, kada je više proizvodnih cenovnika priloženo podugovoru, svaki mora da ima različit period važenja. Usluga Project Operations ne podržava preklapanje perioda važenja za cenovnike za kupovinu. Samo cenovnici u kojima je polje **Kontekst** podešeno na **Kupovina** mogu se priložiti podugovorima.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
