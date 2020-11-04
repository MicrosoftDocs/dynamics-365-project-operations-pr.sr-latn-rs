---
title: Zatvaranje ponuda
description: Ova tema pruža informacije o zatvaranju ponude u usluzi Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083501"
---
# <a name="close-quotes"></a>Zatvaranje ponuda 

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Ponuda za projekat može da se zatvori kao ostvarena ili neostvarena. Budući da operacije Aktiviranje i Revizija nisu podržane u ponudama u usluzi Microsoft Dynamics 365 Project Operations, možete zatvoriti radnu verziju ponude.

## <a name="close-a-quote-as-won"></a>Zatvaranje ponude kao ostvarene

Zatvaranje ponude za projekat kao ostvarene zatvoriće ponudu sa statusom postavljenim na Zatvoreno i razlogom statusa postavljenim na Ostvareno. Zatvaranje ponude je postavlja ponudu za projekat u status samo za čitanje i kreira radnu verziju ugovora za projekat koja sadrži sve informacije iz ponude. Postoji dijalog za potvrdu pre nego što se promene izvrše, jer se zatvorena ponuda ne može ponovo otvoriti i promene su nepovratne.

Ako priložite ponudu uz mogućnost za poslovanje, sve ostale ponude za projekat u mogućnosti za poslovanje automatski se zatvaraju kao neostvarene.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Finansijski uticaj zatvaranja ponude kao ostvarene

Ako postoje stvarni podaci za vreme zabeleženo na projektu dok je još uvek priložen uz radnu verziju ponude, beleže se samo troškovi vremena ili rashoda. Nakon što se ponuda zatvori kao ostvarena, aplikacija će refaktorisati troškove storniranjem starijih stvarnih troškova i ponovnim kreiranjem novih stvarnih troškova. Aplikacija će obraditi ove stvarne troškove na osnovu metode naplate povezanog predmeta ugovora o projektu. Ako se stvarni iznosi troškova odnose na predmet ugovora o vremenu i materijalu, sistem će automatski kreirati odgovarajuće nefakturisane stvarne podatke o prodaji kada se ponuda zatvori i kreira projektni ugovor. Ako se stvarni podaci o troškovima pozivaju na predmet ugovora sa fiksnom cenom, aplikacija će zaustaviti ponovnu obradu stvarnih troškova na osnovu pravila podeljenog obračuna za klijente po ugovoru o projektu.

## <a name="closing-a-quote-as-lost"></a>Zatvaranje ponude kao neostvarene:

Zatvaranje ponude za projekat kao neostvarene postaviće status ponude na Zatvoreno a razlog statusa na Neostvareno. Zatvaranje ponude postavlja ponudu za projekat u režim samo za čitanje. Budući da zatvorenu ponudu ne možete ponovo otvoriti, pre nego što zatvorite ponudu, dijalog za potvrdu će potvrditi vaše promene.

Ako ponuda za projekat koja je zatvorena kao neostvarena ima projekat na koji se poziva bilo koji od njenih predmeta, taj projekat se takođe označava kao zatvoren i sve rezervacije za resurse od tog dana nadalje se otkazuju.

> [!NOTE]
> U usluzi Project Operations, zatvaranje ponude kao ostvarene ili neostvarene neće uticati na status mogućnosti za poslovanje, koja će ostati otvorena sve dok se ručno ne zatvori.
