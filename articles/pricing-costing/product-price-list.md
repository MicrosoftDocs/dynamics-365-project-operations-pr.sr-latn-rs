---
title: Cenovnici proizvoda
description: Ova tema pruža informacije o cenovnicima u kataloškim cenama koji se koriste za ponude za projekat i ugovore.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 504aa90bfb478207059b5e2894a3990f9a4a5e9e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083648"
---
# <a name="product-price-lists"></a>Cenovnici proizvoda

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Entiteti Cenovnici i Stavka cenovnika podržavaju cene u katalogu proizvoda. Ova funkcionalnost se u najvećoj meri koristi u stavkama zasnovanim na katalogu u projektnim ponudama i projektnim ugovorima.

Za stavke zasnovane na projektu, ugovor predstavlja pogodbu nakon što je odobren. Budući da proces pregovaranja obično prethodi odobrenju, cene koje su priložene uz ponudu uvek se kopiraju takve kakve jesu u novi cenovnik i prilažu uz ugovor. Ovaj novi cenovnik ne može se menjati izvan okvira ugovora. Ovo ograničenje pomaže u zaštiti ugovorene cenovne karte od bilo kakvih promena cena u glavnom cenovniku.

Proizvodi treba da budu podešeni tako da u katalogu proizvoda imaju podrazumevane troškove i cenovnike. Koristite cenovnik, standardnu cenu i trenutnu cenu da biste konfigurisali podrazumevanu cenu i cenovnik. Podrazumevane cene na listi koriste se u stavci ponude ili predmetu ugovora o projektu samo kada sistem ne može da pronađe stavku cenovnika za taj proizvod u cenovniku proizvoda za ponudu ili ugovor o projektu.

Cena koštanja stavki kataloga proizvoda može se menjati između ponuda. Ova mogućnost je važna, jer ako ne pratite tačno troškove, ne možete da odredite operativni profit od projektnih angažmanima. Standardna cena proizvoda se podrazumevano koristi kao cena koštanja. Međutim, podrazumevana cena koštanja može se ažurirati u stavci ponude ako za tu ponudu postoji drugačija cena.

## <a name="price-list-items"></a>Stavke cenovnika

Možete da dodate proizvode iz kataloga proizvoda u različite cenovnike. Stavke cenovnika za proizvode uvek upućuju na određenu jedinicu. Cene proizvoda u stavkama cenovnika se mogu konfigurisati kao iznos valute. Alternativno, mogu se konfigurisati kao funkcija cenovnika, trenutne cene ili standardne cene.

PSA podržava različite opcije zaokruživanja kada su cene konfigurisane kao funkcija cenovnika, standardne cene ili trenutne cene. Pored toga što možete iskoristiti više metoda određivanja cena i mogućnosti zaokruživanja, liste popusta možete povezati sa stavkama cenovnika. 

Kada kreirate novi prilagođeni cenovnik za ponudu, izborom stavke **Kreiranje prilagođenih cena** na stranici **Ponuda za projekat** , pravi se kopija cenovnika i polje **Entitet** u zaglavlju novog cenovnika se podešava na **Prodajni entitet**. Naziv novog cenovnika se dodaje uz naziv ponude i vremensku oznaku. Takođe možete da koristite ime novog cenovnika i naziv ponude u prilagođenim tokovima posla da pokrenete dodatni pregled i odobrenja za ponude koje koriste prilagođene cene.

 
## <a name="default-product-price-list"></a>Podrazumevani cenovnik proizvoda
Svaki zapis klijenta ima polje **Podrazumevani cenovnik** , gde možete odrediti cenovnik koji odgovara valuti klijenta. Podrazumevana vrednost se ne unosi u ovo polje automatski. Kada postoji prilagođeni ugovor o cenama sa određenim klijentom, ovo polje možete koristiti da biste povezali cenovnik sa tim klijentom.

Entiteti Mogućnost za poslovanje, Ponuda i Ugovor o projektu koriste sledeći redosled za unošenje podrazumevanih cenovnika proizvoda. Isti redosled se koristi za cenovnike projekata.

1.  Ponuda
2.  Mogućnost za poslovanje
3.  Klijent
4.  Globalna podešavanja 

Polje **Proizvod** u stavci ponude podrazumevano navodi sve aktivne proizvode u cenovniku proizvoda za ponudu. Ako proizvod nije aktiviran ili je radna verzija proizvoda, on nije naveden, čak i ako je u cenovniku. 

Stavke kataloga proizvoda dodaju se kao stavke fakture na prvoj fakturi koja je kreirana za ugovor o projektu. U radnoj verziji fakture te stavke fakture mogu se izbrisati. U tom slučaju, stavke će se pojaviti na narednoj fakturi dok se ne fakturišu ili dok se faktura ne pošalje klijentu. Ne možete fakturisati delimičnu količinu stavke fakture za proizvod. Kada se fakturišu stavke proizvoda iz projektnog ugovora, kreiraju se stvarne vrednosti. Međutim, ove stvarne vrednosti nisu povezane sa srodnim entitetom projekta. Drugim rečima, predmeti ugovora zasnovani na proizvodima ne zavise ni od kakve upotrebe zasnovane na projektu. Potrošnja materijala za projekte se ne prati.
