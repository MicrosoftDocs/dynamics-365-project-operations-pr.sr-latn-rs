---
title: Formiranje cena za katalog proizvoda
description: Ova tema pruža informacije o tome kako funkcionišu cene u katalogu proizvoda u aplikaciji Dynamics 365 Project Service Automation (PSA).
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
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
ms.openlocfilehash: 6cf50a09226bd6fdb803fd1fd379fec80838be75
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600667"
---
# <a name="product-catalog-pricing"></a>Formiranje cena za katalog proizvoda 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Entiteti Cenovnici i Stavka cenovnika podržavaju cene u katalogu proizvoda. Ova funkcionalnost se u najvećoj meri koristi u stavkama zasnovanim na katalogu u projektnim ponudama i projektnim ugovorima.

Za stavke zasnovane na projektu, ugovor predstavlja pogodbu nakon što je odobren. Budući da proces pregovaranja obično prethodi odobrenju, cene koje su priložene uz ponudu uvek se kopiraju takve kakve jesu u novi cenovnik i prilažu uz ugovor. Ovaj novi cenovnik ne može se menjati izvan okvira ugovora. Ovo ograničenje pomaže u zaštiti ugovorene cenovne karte od bilo kakvih promena cena u glavnom cenovniku.

Proizvodi treba da budu podešeni tako da u katalogu proizvoda imaju podrazumevane troškove i cenovnike. Morate da koristite cene na listi, standardnu cenu i trenutnu cenu da biste konfigurisali podrazumevanu cenu i cene na listi. Podrazumevane cene na listi koriste se u stavci ponude ili predmetu ugovora o projektu samo kada sistem ne može da pronađe stavku cenovnika za taj proizvod u cenovniku proizvoda za ponudu ili ugovor o projektu.

Cena koštanja stavki kataloga proizvoda može se menjati između ponuda. Ova mogućnost je važna, jer ako ne pratite tačno troškove, ne možete da odredite operativni profit od projektnih angažmanima. Standardna cena proizvoda se podrazumevano koristi kao cena koštanja. Međutim, podrazumevana cena koštanja može se ažurirati u stavci ponude ako za tu ponudu postoji drugačija cena.

## <a name="price-list-items"></a>Stavke cenovnika

Možete da dodate proizvode iz kataloga proizvoda u različite cenovnike. Stavke cenovnika za proizvode uvek upućuju na određenu jedinicu. Cene proizvoda u stavkama cenovnika se mogu konfigurisati kao iznos valute. Alternativno, mogu se konfigurisati kao funkcija cenovnika, trenutne cene ili standardne cene.

PSA podržava različite opcije zaokruživanja kada su cene konfigurisane kao funkcija cenovnika, standardne cene ili trenutne cene. Pored toga što možete iskoristiti više metoda određivanja cena i mogućnosti zaokruživanja, liste popusta možete povezati sa stavkama cenovnika. 

> ![Dodavanje proizvoda iz kataloga u različite cenovnike.](media/basic-guide-16.png)

Kada kreirate novi prilagođeni cenovnik za ponudu, izborom **Kreiranje prilagođenih cena** na stranici **Ponuda za projekat**, PSA pravi kopiju cenovnika i polje **Entitet** u zaglavlju novog cenovnika podešava na **Prodajni entitet**. Naziv novog cenovnika se dodaje uz naziv ponude i vremensku oznaku. Takođe možete da koristite ime novog cenovnika i naziv ponude u prilagođenim tokovima posla da pokrenete dodatni pregled i odobrenja za ponude koje koriste prilagođene cene.

 
## <a name="default-product-price-list"></a>Podrazumevani cenovnik proizvoda
Svaki zapis klijenta ima polje **Podrazumevani cenovnik**, gde možete odrediti cenovnik koji odgovara valuti klijenta. U aplikaciji PSA, podrazumevana vrednost se automatski ne unosi u ovo polje. Kada postoji prilagođeni ugovor o cenama sa određenim klijentom, ovo polje možete koristiti da biste povezali cenovnik sa tim klijentom.

Entiteti Mogućnost za poslovanje, Ponuda i Ugovor o projektu koriste sledeći redosled za unošenje podrazumevanih cenovnika proizvoda. Isti redosled se koristi za cenovnike projekata.

1.  Ponuda
2.  Mogućnost za poslovanje
3.  Klijent
4.  Globalna podešavanja za PSA

Polje **Proizvod** u stavci ponude podrazumevano navodi sve aktivne proizvode u cenovniku proizvoda za ponudu. Ako proizvod nije aktiviran ili je radna verzija proizvoda, on nije naveden, čak i ako je u cenovniku. 

Stavke kataloga proizvoda dodaju se kao stavke fakture na prvoj fakturi koja je kreirana za ugovor o projektu. U radnoj verziji fakture te stavke fakture mogu se izbrisati. U tom slučaju, stavke će se pojaviti na narednoj fakturi dok se ne fakturišu ili dok se faktura ne pošalje klijentu. U aplikaciji PSA ne možete fakturisati delimičnu količinu stavke fakture za proizvod. Kada se fakturišu stavke proizvoda iz projektnog ugovora, kreiraju se stvarne vrednosti. Međutim, ove stvarne vrednosti nisu povezane sa srodnim entitetom projekta. Drugim rečima, predmeti ugovora zasnovani na proizvodima ne zavise ni od kakve upotrebe zasnovane na projektu. PSA ne prati potrošnju materijala za projekte.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
