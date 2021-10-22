---
title: Podesite odlaganje obaveza prema dobavljaču
description: Ova tema objašnjava kako da podesite odlaganje plaćanja dobavljaču.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9511da6212aafbf5b173efc6eb1ceaacbc8264a2
ms.sourcegitcommit: 098ea345ecfaf4445520094c32f5511b67e7953c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594624"
---
# <a name="set-up-vendor-retention"></a>Podesite odlaganje obaveza prema dobavljaču

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ova tema opruža informacije o tome kako da podesite odlaganje plaćanja dobavljaču.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>Podesite račun za odlaganje plaćanja dobavljaču u glavnoj knjizi

1. U usluzi Dynamics 365 Finance idite na **Glavnu knjigu** > **Podešavanje knjiženja** > **Računi za automatske transakcije**.
2. Dodavanje nove stavke.
3. U polju **Vrsta knjiženja**, izaberite **Odlaganje plaćanja dobavljaču**.
4. Izaberite glavni račun za knjiženje odlaganja plaćanja dobavljaču.

## <a name="create-vendor-retention-terms"></a>Kreirajte uslove odlaganja plaćanja dobavljaču

Koristite stranicu **Uslovi odlaganja plaćanja dobavljaču** za podešavanje i održavanje uslova odlaganja plaćanja dobavljaču. Unesite procenat plaćanja dobavljaču koji treba odložiti i procenat prethodno zadržanih iznosa koje treba isplatiti. Iznosi se automatski zadržavaju na fakturama prodavaca sve dok ugovor ne dostigne određeni status završenosti. Nakon što su za dobavljača podešeni uslovi odlaganja, možete da ih primenite na bilo koji projekat na kome dobavljač radi.

1. U odeljku „Finansije“ idite na **Upravljanje projektima i računovodstvo** > **Podešavanja** > **Odlaganje** > **Uslovi odlaganja plaćanja dobavljača**.
2. Izaberite **Novo** da biste dodali novi uslov zadržavanja za prodavce. Vrednost u polju **ID pravila** za novi termin se automatski unosi. 
3. U polju **Opis** unesite opisni naziv za novi termin.
4. Na kartici **Uslovi** izaberite **Dodaj stavku** da biste uneli uslove odlaganja plaćanja dobavljačima.
5. U polje **Procenat isporučenih jedinica** unesite procenat dovršenosti pravila. Iznosi se automatski zadržavaju na fakturama dobavljača sve dok faza završetka projekta nije jednaka procentu koji unesete. Na primer, ako unesete 50,00, iznosi se zadržavaju sve dok projekat ne bude završen 50 odsto.
6. U polje **Procenat za odlaganje** unesite procenat iznosa fakture dobavljača koji treba odložiti. Na primer, ako unesete 10,00 u ovo polje, 10 procenata iznosa na fakturama dobavljača se zadržava sve dok projekat ne dostigne procenat završetka koji izaberete u polju **Procenat isporučenih jedinica**.
7. U polju **Procenat za isplatu** unesite procenat prethodno zadržanih iznosa za isplatu na izabranom nivou završetka projekta.

> [!NOTE]
> Ako imate više od jedne kontrolne tačke za različite nivoe završetka projekta, unesite zasebnu stavku uslova odlaganja plaćanja dobavljaču za svako pravilo zadržavanja. U svakoj stavci može da se navede različit procenat za odlaganje i različit procenat za isplatu za svaki određeni nivo završetka projekta.

## <a name="set-up-a-vendor-agreement-for-the-project"></a>Podesite ugovor sa dobavljačem za projekat

Podesite uslove odlaganja plaćanja dobavljaču koji se primenjuju na projekat. Uslovi zadržavanja za prodavce se takođe prikazuju na porudžbenicama koje kreirate za prodavca.

1. U odeljku „Finansije“ idite na **Upravljanje projektima i računovodstvo** > **Projekti** > **Svi projekti**. 
2. Izaberite projekat, a zatim oknu sa radnjama izaberite **Projektna grupa** > **Ugovori sa dobavljačima**.
3. Na stranici **Ugovori sa dobavljačima** dodajte novi red.
4. U polju **Kôd poslovnog kontakta** izaberite jednu od sledećih opcija:
   - **Tabela**: Uslovi zadržavanja za prodavce se primenjuju na jednog prodavca.
   - **Grupa** – Uslovi zadržavanja za prodavce važe za sve prodavce u grupi.
   - **Sve**: Uslovi zadržavanja za prodavce se primenjuju na sve prodavce.
5. U polju **Dobavljač/grupa dobavljača**, izaberite dobavljača ili grupu dobavljača na koje se primenjuju uslovi odlaganja plaćanja dobavljačima. Ako ste izabrali **Sve** u prethodnom koraku, ovo polje nije dostupno.
6. U polju **Uslovi odlaganja plaćanja dobavljaču** izaberite ID pravila za uslove odlaganja koji će se primeniti na ovog dobavljača.

