---
title: Šta je novo u martu 2022. – Project Operations jednostavna primena
description: Ovaj članak pruža informacije o kvalitetnim ispravkama koje su dostupne u izdanju primene lite operacija projekta u martu 2022.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 321d59568bfd33bb00a1500afe514fbecf9a0250
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934245"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>Šta je novo u martu 2022. – Project Operations jednostavna primena

_Odnosi se na: Jednostavna primena – od pogodbe do profakture_

Ovaj članak se odnosi na sledeće komponente i verzije korporacije Microsoft Dynamics 365 Project Operations:

- Operacije projekta u verziji Dataverse okruženja 4.30.0.99

## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

- Podizvođači: Kreiranje faktura dobavljača i odgovarajuća iskustva

## <a name="quality-updates"></a>Ispravke kvaliteta

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Vreme i trošak | 2388011 | Prikažite komentare odbijanja prosleđenim stavkama vremena tokom masovnog odobravanja. |
| Planiranje i praćenje projekta | 2495294 | Detalji projekta ne smeju da se uređuju na stranici **sa detaljima zadatka**. |
| Naplata i određivanje cena | 2499605 | Prekretnice ugovora koje su nastale od prekretnica navoda netačno su označene samo za čitanje. |
| Planiranje i praćenje projekta | 2506050 | Skup operacija ostaje na čekanju jedan sat ako nema promene za čuvanje. Skup je zatim lažno označen kao "Neuspešno **·**", dok bi trebalo odmah da bude dovršen. |
| Naplata i određivanje cena | 2507401 | Podrazumevane jedinice ugovora se nepravilno unose u projekte zbog neispravnog keširanja. |
| Naplata i određivanje cena | 2541660 | **Provera valjanosti kreiranja ulaznih porudžbina** u dvostrukom upisivanju treba da bude samo za porudžbine zasnovane na projektu. |
| Naplata i određivanje cena | 2552745 | Porez se ne deli između kupaca koji su podesili pravila podele naplate. |
| Naplata i određivanje cena | 2558859 | Poboljšane poruke o greškama prilikom podešavanje dimenzija cena. |
| Naplata i određivanje cena | 2558933 | **Uvoz iz procene projekta** ne uspe **kada se msdyn\_** projekat doda kao dimenzija cena. |
| Naplata i određivanje cena | 2559101 | Brisanje parametara projekta nije blokirano i dovodi do problema. |
| Upravljanje mogućnostima za poslovanje | 2570390 | Dodatna komponenta za dvostruko pisanje primorava tip naloga na navodnicima, porudžbinama i prilikama da bude "Kupac **·**", čak i kada taj tip naloga nije ispravan. |
| Naplata i određivanje cena | 2586097 | Razdeljeni troškovi fakturisanih se ne obrću kada se projekat ukloni iz reda ugovora o projektu. |
| Naplata i određivanje cena | 2589619 | Porez na materijal za upis se širi na neželjene aktuele prodaje i fakturu. |
| Upravljanje mogućnostima za poslovanje | 2594015 | Nije moguće zatvoriti citat kao što je osvojeno za kupce koji imaju Net60 **uslove** plaćanja. |
| Planiranje i praćenje projekta | 2595841 | U projektu za Web korisnici dobijaju poruku o grešci o msdyn **actualstart-u \_ koji nedostaje** kada kreiraju novi zahtev za resurs. |
| Vreme i trošak | 2602511 | Polje **"Odbijeno** " za stavke vremena prikazuje **sistem** umesto imenovanog korisnika kao odbijača. |
| Vreme i trošak | 2602528 | Osoba koja vrši odobravanje projekta može da odobri vreme na projektima u kojima nisu navedeni kao osoba koja vrši odobravanje. |
| Naplata i određivanje cena | 2608550 | Korektivna faktura se može potvrditi čak i ako nema promena u originalu. |

## <a name="removed-and-deprecated-features"></a>Uklonjene i neodobrene funkcije

Uklonjene [ili zastarele funkcije u članku "Operacije](../../whats-new/removed-depreciated-features-project.md) projekta" opisuju funkcije koje su uklonjene ili zastarele za Dynamics 365 Project Operations.

- Uklonjena funkcija više nije dostupna u proizvodu.
- Zastarela funkcija nije u aktivnom razvoju i može biti uklonjena u budućoj ispravci.

Najava amortizacije će se pojaviti u funkcijama " [Uklonjeno" ili "Zastarelo" u članku "Operacije](../../whats-new/removed-depreciated-features-project.md) projekta" 12 meseci pre nego što bilo koja funkcija bude uklonjena iz proizvoda.
