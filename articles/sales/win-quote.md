---
title: Zatvori ponudu
description: Ova tema pruža informacije o zatvaranju ponuda u usluzi Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2314444dfdbd4d1a2f38c7de55e2070011e51a86f1e074dd6667d54393c641fe
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993438"
---
# <a name="close-a-quote"></a>Zatvori ponudu

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ponuda za projekat može da se zatvori kao ostvarena ili neostvarena. Budući da funkcije Aktiviraj i Revidiraj nisu podržane za ponude u usluzi Microsoft Dynamics 365 Project Operations, možete da zatvorite radnu verziju ponude.

## <a name="close-a-quote-as-won"></a>Zatvaranje ponude kao ostvarene

Zatvaranje ponude za projekat kao ostvarene postaviće status ponude na **Zatvoreno** a razlog statusa na **Ostvareno**. Zatvaranje ponude je pretvara u status samo za čitanje i kreira radnu verziju ugovora za projekat sa svim informacijama iz ponude. Budući da zatvorenu ponudu ne možete ponovo otvoriti, pre nego što zatvorite ponudu, dijalog za potvrdu će potvrditi vaše promene.

Ugovor za projekat kreiran na osnovu ponude za projekat takođe je dostupan u modulu „Upravljanje projektima i računovodstvo“ usluge Project Operations. Ako ugovor za projekat nije mapiran u projekat ni na jednoj od njegovih stavki, ovaj ugovor za projekat postaje dostupan kao neaktivan ugovor za projekat i postaje aktivan čim se projekat preslika na najmanje jedan od njegovih predmeta ugovora.

Ako priložite ponudu uz mogućnost za poslovanje, sve ostale ponude za projekat u mogućnosti za poslovanje automatski se zatvaraju kao neostvarene.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Finansijski uticaj zatvaranja ponude kao ostvarene

Ako postoje stvarni podaci za vreme zabeleženo na projektu dok je još uvek priložen uz radnu verziju ponude, beleže se samo troškovi vremena ili rashoda. Nakon što se ponuda zatvori kao ostvarena, aplikacija će refaktorisati troškove storniranjem starijih stvarnih troškova i ponovnim kreiranjem novih stvarnih troškova. Aplikacija će obraditi ove stvarne troškove na osnovu metode naplate povezanog predmeta ugovora o projektu. Ako se stvarni iznosi troškova odnose na predmet ugovora o vremenu i materijalu, sistem će automatski kreirati odgovarajuće nefakturisane stvarne podatke o prodaji kada se ponuda zatvori i kreira projektni ugovor. Ako se stvarni podaci o troškovima pozivaju na predmet ugovora sa fiksnom cenom, aplikacija će zaustaviti ponovnu obradu stvarnih troškova na osnovu pravila podeljenog obračuna za klijente po ugovoru o projektu.

Sva obrađena trenutna stanja dostupna su u modulu za upravljanje projektom i računovodstvo, a računovođa projekta može ih pregledati, ažurirati i knjižiti u glavnu knjigu. 

## <a name="close-a-quote-as-lost"></a>Zatvaranje ponude kao neostvarene

Zatvaranje ponude za projekat kao neostvarene postaviće status ponude na **Zatvoreno** a razlog statusa na **Neostvareno**. Zatvaranjem ponude ona postaje samo za čitanje. Budući da zatvorenu ponudu ne možete ponovo otvoriti, pre nego što zatvorite ponudu, dijalog za potvrdu će potvrditi vaše promene.

Ako ponuda za projekat koja je zatvorena kao neostvarena ima projekat na koji se poziva bilo koji od njenih predmeta, taj projekat se takođe označava kao zatvoren i sve rezervacije za resurse od tog dana nadalje se otkazuju.

> [!NOTE]
> U usluzi Project Operations, zatvaranje ponude kao ostvarene ili neostvarene neće uticati na status mogućnosti za poslovanje, koja će ostati otvorena sve dok se ručno ne zatvori.


[!INCLUDE[footer-include](../includes/footer-banner.md)]