---
title: Šta je novo u februaru 2022. – Project Operations jednostavna primena
description: Ovaj članak pruža informacije o ispravkama kvaliteta koje su dostupne u izdanju jednostavne primene usluge Project Operations za februar 2022.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1203faa2dd53a8fb82cff0857a1725426ebff19a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922837"
---
# <a name="whats-new-february-2022---project-operations-lite-deployment"></a>Šta je novo u februaru 2022. – Project Operations jednostavna primena

_Odnosi se na: Jednostavna primena – od pogodbe do profakture_

Ovaj članak se odnosi na sledeće komponente i verzije usluge Microsoft Dynamics 365 Project Operations:

- Project Operations u Dataverse okruženju verzije 4.28.0.120

## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

Od ovog izdanja, možete da dodate do 300 članova tima u jedan projekat. Prethodno je ograničenje broja članova tima bilo 150. Za više informacija, pogledajte članak [Ograničenja projekta](../../project-management/create-wbs.md#project-limitations).

## <a name="quality-updates"></a>Ispravke kvaliteta

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Naplata i određivanje cena | 2497369 | Korekcija materijala mora pratiti vrednost datuma u parametrima **Korekcija**. |
| Naplata i određivanje cena | 2498697 | Poboljšana je bezbednosna konfiguracija za **Opoziv stavke vremena**. |
| Naplata i određivanje cena | 2517455 | Radnja **Osvežene transakcije stavke na fakturi** ne sme biti dozvoljena da bude aktivirana više puta istovremeno za istu fakturu. |
| Naplata i određivanje cena | 2517465 | Radnja **Deaktiviranje detalja o redu na fakturi** je blokirana jer nije podržana. |
| Naplata i određivanje cena | 2556660 | Popravljena je provera stupanja na snagu datuma koja se vrši na cenovniku koji je priložen zapisu parametara projekta. |
| Upravljanje mogućnostima za poslovanje | 2369202 | Ispravljena je poslovna logika koja potvrđuje da cenovnici koji imaju preklapajuće datume stupanja na snagu mogu biti priloženi istom projektnom ugovoru. |
| Upravljanje mogućnostima za poslovanje | 2385965 | Ispravili ste ponašanje na kartici **Klijenti** na stranici **Projektni ugovor** kada izaberete **Sačuvaj i zatvori**. |
