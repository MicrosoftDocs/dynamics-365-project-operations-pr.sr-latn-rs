---
title: Cenovnici proizvoda
description: Ova tema pruža informacije o cenovnicima u kataloškim cenama koji se koriste za ponude za projekat i ugovore.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8bfd4eaa6f4bcbbdf398683a25a3b0079cfedd535ef32d383993883607f7ef5a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999243"
---
# <a name="product-price-lists"></a>Cenovnici proizvoda

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

 U usluzi Project Operations, **cenovnici proizvoda** i povezani entiteti stavke cenovnika podržavaju funkcionalnost određivanja cena proizvoda prema ponudi zasnovanoj na proizvodima i predmetima ugovora. Za proizvode koji se koriste na projektima, koriste se zapisi stavki cenovnika za cenovnike projekata. 

Proizvodi treba da budu podešeni tako da u katalogu proizvoda imaju podrazumevane troškove i cenovnike. Koristite cenovnik, standardnu cenu i trenutnu cenu da biste konfigurisali podrazumevanu cenu i cenovnik. Podrazumevane cene na listi koriste se u stavci ponude ili predmetu ugovora o projektu samo kada sistem ne može da pronađe stavku cenovnika za taj proizvod u cenovniku proizvoda za ponudu ili ugovor o projektu.

Cena koštanja stavki kataloga proizvoda može se menjati između ponuda. Ova mogućnost je važna, jer ako ne pratite tačno troškove, ne možete da odredite operativni profit od projektnih angažmanima. Standardna cena proizvoda se podrazumevano koristi kao cena koštanja. Međutim, podrazumevana cena koštanja može se ažurirati u stavci ponude ako za tu ponudu postoji drugačija cena.

## <a name="price-list-items"></a>Stavke cenovnika

Možete da dodate proizvode iz kataloga proizvoda u različite cenovnike. Stavke cenovnika za proizvode uvek upućuju na određenu jedinicu. Cene proizvoda u stavkama cenovnika se mogu konfigurisati kao iznos valute. Alternativno, mogu se konfigurisati kao funkcija cenovnika, trenutne cene ili standardne cene.

Funkcionalnost određivanja cena podržava različite opcije zaokruživanja kada su cene proizvoda konfigurisane kao funkcija cenovnika, standardna cena ili trenutna cena. Pored toga što možete iskoristiti više metoda određivanja cena i mogućnosti zaokruživanja, liste popusta možete povezati sa stavkama cenovnika. 

 
## <a name="default-product-price-list"></a>Podrazumevani cenovnik proizvoda
Svaki zapis klijenta ima polje **Podrazumevani cenovnik**, gde možete odrediti cenovnik koji odgovara valuti klijenta. Podrazumevana vrednost se ne unosi u ovo polje automatski. Kada postoji prilagođeni ugovor o cenama sa određenim klijentom, ovo polje možete koristiti da biste povezali cenovnik sa tim klijentom.

Entiteti Mogućnost za poslovanje, Ponuda i Ugovor o projektu koriste sledeći redosled za unošenje podrazumevanih cenovnika proizvoda. Isti redosled se koristi za cenovnike projekata.

1.  Ponuda
2.  Mogućnost za poslovanje
3.  Klijent
4.  Globalna podešavanja 

Polje **Proizvod** u stavci ponude podrazumevano navodi sve aktivne proizvode u cenovniku proizvoda za ponudu. Ako proizvod nije aktiviran ili je radna verzija proizvoda, on nije naveden, čak i ako je u cenovniku. 

Stavke kataloga proizvoda dodaju se kao stavke fakture na prvoj fakturi koja je kreirana za ugovor o projektu. U radnoj verziji fakture te stavke fakture mogu se izbrisati. U tom slučaju, stavke će se pojaviti na narednoj fakturi dok se ne fakturišu ili dok se faktura ne pošalje klijentu. Ne možete fakturisati delimičnu količinu stavke fakture za proizvod. Kada se fakturišu stavke proizvoda iz projektnog ugovora, kreiraju se stvarne vrednosti. Međutim, ove stvarne vrednosti nisu povezane sa srodnim entitetom projekta. Drugim rečima, predmeti ugovora zasnovani na proizvodima ne zavise ni od kakve upotrebe zasnovane na projektu. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
