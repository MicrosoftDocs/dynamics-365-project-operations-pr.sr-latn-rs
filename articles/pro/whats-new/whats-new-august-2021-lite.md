---
title: Šta je novo u avgustu 2021. – Project Operations jednostavna primena
description: Ovaj članak pruža informacije o ispravkama kvaliteta dostupnim u izdanju usluge Project Operations jednostavna primena za avgust 2021. godine.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 84318a26d97355fe56794e1d1532576cde4af661
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922055"
---
# <a name="whats-new-august-2021---project-operations-lite-deployment"></a>Šta je novo u avgustu 2021. – Project Operations jednostavna primena

_Odnosi se na: Jednostavna primena – od pogodbe do profakture_

Ovaj članak se odnosi na sledeće komponente i verzije usluge Dynamics 365 Project Operations:

  - Project Operations u Dataverse okruženju verzije 4.13.0.152

## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

Sledeće funkcije su uključene u ovom izdanju:

- **Skupovi odobrenja**: Skupovi odobrenja grupišu zahteve za odobrenje vremena, troškova ili korišćenje materijala u manje podskupove operacija. Ovo grupisanje omogućava da se odobrenja obrađuju prema određenom redosledu po projektu i omogućava ponovni pokušaj i sekvenciranje. Grupisanje zahteva poboljšava pouzdanost i mogućnost praćenja obrade odobrenja za velike brojeve odobrenja. Za više informacija, pogledajte [Skupovi odobrenja](../../approvals/approval-sets.md).

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-on-dataverse"></a>Project Operations u usluzi Dataverse

| **Oblast funkcija** | **Referentni broj** | **Ispravka kvaliteta** |
| --- | --- | --- |
| Naplata i određivanje cena | 2295625 | Naziv kontrolne tačke mora se kopirati iz rasporeda faktura u detalje stavke fakture. |
| Naplata i određivanje cena | 2316323 | Za popust ne treba da postoji mogućnosti uređivanja na predračunu u aplikaciji Project Operations za scenarije zasnovane na resursima. |
| Upravljanje mogućnostima za poslovanje | 2338619 | Poslovna pravila za stavke **Mogućnost za poslovanje** i **Ponuda** moraju se pozivati samo na stranicama. |
| Upravljanje resursima | 2316523 | Korišćenje stavke **Poslati zahtev** iz zahteva resursa koji ima priloženu ulogu ne bi trebalo da prikaže grešku. |
| Upravljanje resursima | 2326885 | Kreiranje zahteva za resursima kroz projekat ne bi trebalo da prikaže grešku. |
| Vreme i trošak | 2335584 | Zastareli tokovi zadataka u unosu vremena. |
| Vreme i trošak | 2336884 | Dugme za unos vremena **Kopiraj sedmicu** mora raditi ne samo za trenutnog korisnika. |
