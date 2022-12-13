---
title: Zatvaranje ponuda za projekat
description: Ovaj članak pruža informacije o zatvaranju ponude u usluzi Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4335fa5467640af840c0f68a648c9b8a6864d834
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 12/05/2022
ms.locfileid: "9826193"
---
# <a name="close-project-quotes"></a>Zatvaranje ponuda za projekat

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Ponuda za projekat može da se zatvori kao ostvarena ili neostvarena. Radna verzija ponude može da se zatvori jer Microsoft Dynamics 365 Project Operations ne podržava operacije Aktiviraj i Revidiraj za ponude.

## <a name="close-a-quote-as-won"></a>Zatvaranje ponude kao ostvarene

Kada zatvorite ponudu za projekat kao Dobijenu, status se podešava na Zatvoreno, a razlog statusa je Dobijeno. Zatvaranje ponude je postavlja ponudu za projekat u status samo za čitanje i kreira radnu verziju ugovora za projekat koja sadrži sve informacije iz ponude. Budući da zatvorena ponuda ne može ponovo da se otvori, dijalog za potvrdu će potvrditi vaše promene.

Ako priložite ponudu uz mogućnost za poslovanje, sve ostale ponude za projekat u mogućnosti za poslovanje automatski se zatvaraju kao neostvarene.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Finansijski uticaj zatvaranja ponude kao ostvarene

Ako postoje stvarni podaci o vremenu na projektu, dok je on još uvek priložen uz radnu verziju ponude, evidentiraju se samo troškovi vremena ili troškovi. Nakon što se ponuda zatvori kao ostvarena, aplikacija će refaktorisati troškove storniranjem starijih stvarnih troškova i ponovnim kreiranjem novih stvarnih troškova. Aplikacija će obraditi ove stvarne troškove na osnovu metode naplate povezanog predmeta ugovora o projektu. Ako se stvarni podaci o troškovima odnose na predmet ugovora za vreme i materijal, odgovarajuće nenaplaćene stvarne prodajne vrednosti kreiraju se kada se ponuda zatvori i kreira projektni ugovor. Ako se stvarni podaci o troškovima odnose na predmet ugovora sa fiksnom cenom, aplikacija će zaustaviti ponovnu obradu stvarnih troškova koji se zasnivaju na pravilima deljene naplate za klijente ugovora o projektu.

## <a name="closing-a-quote-as-lost"></a>Zatvaranje ponude kao izgubljene

Kada zatvorite ponudu za projekat kao Neostvarenu, status se podešava na Zatvoreno, a razlog statusa je Neostvareno. Zatvaranje ponude postavlja ponudu za projekat u režim samo za čitanje. Budući da zatvorenu ponudu ne možete ponovo otvoriti, pre nego što zatvorite ponudu, dijalog za potvrdu će potvrditi vaše promene.

Ako se ponuda projekta koja je zatvorena kao Neostvarena odnosi na projekat u bilo kom redu, taj projekat je takođe označen kao Zatvoren. Sve rezervacije resursa od tog dana nadalje otkazuju se.

> [!NOTE]
> U usluzi Project Operations, zatvaranje ponude kao ostvarene ili neostvarene neće uticati na status mogućnosti za poslovanje, koja će ostati otvorena sve dok se ručno ne zatvori.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
