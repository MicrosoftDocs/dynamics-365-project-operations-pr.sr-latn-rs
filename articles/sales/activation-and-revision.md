---
title: Aktiviranje i korigovanje ponude za projekat
description: Ovaj članak pruža informacije o aktiviranju i reviziji ponuda u usluzi Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e71102078832ac7d5f8e5edb40cc484df927eda4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410396"
---
# <a name="activate-and-revise-a-project-quote"></a>Aktiviranje i korigovanje ponude za projekat

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Mogućnosti aktivacije i revizije vam pomažu da pratite kreiranje verzija za ponude zasnovane na projektu tokom faza procene i pregovora. Kada se aktivira radna verzija ponude, ona postaje samo za čitanje.

Mogućnosti aktivacije i revizije vam omogućavaju da izvršite sledeće zadatke:

- Realizujte ili izgubite ponude tek nakon aktivacije.
- Revidirajte ponudu da biste uneli promene u postojeću ponudu ili kreirali novu verziju.

> [!NOTE]
> Nakon što funkcija za aktiviranje i reviziju ponuda bude omogućena, ne možete je onemogućiti.

Da biste uključili mogućnost aktiviranja i revidiranja ponuda zasnovanih na projektu, sledite ove korake.

1. Idite na **Postavke** \> **Parametri**.
1. Otvori zapis **Parametri**.
1. U oknu radnji, na kartici **Kontrola funkcija** izaberite dugme **Omogući aktivaciju i reviziju ponuda**.
1. U dijalogu za potvrdu izaberite **U redu**.
1. Nakon nekoliko trenutaka osvežite pregledač. Mogućnosti aktivacije i revizije sada bi trebalo da budu dostupne. Znaćete da su ove mogućnosti omogućene ako se dugme **Omogući aktivaciju i reviziju za ponude** više ne pojavljuje u oknu radnji.

## <a name="activating-a-quote"></a>Aktiviranje ponude

Nakon što je funkcija aktiviranja i revizije ponuda omogućena, dugmad **Zatvori ponudu kao ostvarenu** i **Zatvori ponudu kao izgubljenu** u oknu radnji neće biti dostupne za radne verzije ponude za projekat. One su dostupne tek nakon aktiviranja ponude.

Aktivacija predstavlja fazu u procesu davanja ponuda kada želite da sprečite više promena u ponudi. U ovoj fazi, ponuda se šalje na internu reviziju ili klijentu.

Dugmad **Zatvori ponudu kao ostvarenu** i **Zatvori ponudu kao izgubljenu** u oknu radnji dostupna su za aktivirane ponude. U zavisnosti od ishoda interne ili revizije klijenta, možete koristiti jedno od ovih dugmadi da biste zatvorili aktiviranu ponudu. Možete pregovarati i menjati aktivirane ponude izborom opcije **Koriguj ponudu**.

## <a name="revising-a-quote"></a>Korigovanje ponude

Ako morate da menjate aktiviranu ponudu, izaberite **Koriguj ponudu**. Ponuda je zatvorena, a koristi se šifra razloga **izmenjeno**. Zatim se kreira nova ponuda koja ima isti ID i broj revizije uvećan za jedan. Svi detalji iz originalne ponude se kopiraju u novu ponudu. Nova ponuda je u statusu radne verzije i može se uređivati po potrebi.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
