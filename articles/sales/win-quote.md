---
title: Zatvaranje ponuda zasnovanih na projektu
description: Ovaj članak pruža informacije o zatvaranju ponuda u usluzi Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7b35417d4258a1e837fdf7a61bbcc303ec04a900
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824235"
---
# <a name="close-project-based-quotes"></a>Zatvaranje ponuda zasnovanih na projektu

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ponuda projekta može biti zatvorena kao osvojena **ili** izgubljena **·**. 

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
