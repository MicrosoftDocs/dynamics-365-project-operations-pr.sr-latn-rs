---
title: Šta je novo u martu 2022. – Project Operations jednostavna primena
description: Ovaj članak pruža informacije o ispravkama kvaliteta koje su dostupne u izdanju jednostavne primene usluge Project Operations za mart 2022.
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

Ovaj članak se odnosi na sledeće komponente i verzije usluge Microsoft Dynamics 365 Project Operations:

- Project Operations u Dataverse okruženju verzije 4.30.0.99

## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

- Podugovaranje: Kreiranje faktura dobavljača i odgovarajuća iskustva

## <a name="quality-updates"></a>Ispravke kvaliteta

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Vreme i trošak | 2388011 | Prikažite komentare odbijanja osobama koje prosleđuju stavke vremena tokom masovnog odobravanja. |
| Planiranje i praćenje projekta | 2495294 | Detalji projekta ne smeju da se uređuju na stranici **Detalji zadatka**. |
| Naplata i određivanje cena | 2499605 | Kontrolne tačke ugovora koje su keširane na osnovu kontrolnih tačaka ponude netačno su označene samo za čitanje. |
| Planiranje i praćenje projekta | 2506050 | Skup operacija ostaje na čekanju jedan sat ako nema promene za čuvanje. Skup se zatim lažno označava kao **Neuspešno**, dok bi trebalo odmah da bude dovršen. |
| Naplata i određivanje cena | 2507401 | Podrazumevane jedinice ugovora se nepravilno unose u projekte zbog pogrešnog keširanja. |
| Naplata i određivanje cena | 2541660 | **Provera valjanosti kreiranja ulaznih porudžbina** u dvostrukom upisivanju treba da bude samo za porudžbine zasnovane na projektu. |
| Naplata i određivanje cena | 2552745 | Porez se ne deli između klijenata koji su podesili pravila za podelu obračuna. |
| Naplata i određivanje cena | 2558859 | Poboljšane poruke o greškama prilikom podešavanja dimenzija za određivanje cena. |
| Naplata i određivanje cena | 2558933 | **Uvoz iz procena za projekat** ne uspeva kada se **msdyn\_project** doda kao dimenzija za određivanje cena. |
| Naplata i određivanje cena | 2559101 | Brisanje parametara projekta nije blokirano i dovodi do problema. |
| Upravljanje mogućnostima za poslovanje | 2570390 | Dodatna komponenta za dvostruko upisivanje primorava da tip naloga na ponudama, porudžbinama i mogućnostima za poslovanje bude **Klijent**, čak i kada taj tip naloga nije ispravan. |
| Naplata i određivanje cena | 2586097 | Stvarne vrednosti podeljenih naplaćenih troškova se ne storniraju kada se projekat ukloni iz predmeta ugovora za projekat. |
| Naplata i određivanje cena | 2589619 | Porez na ručno uneti materijal se propagira na stvarne vrednosti nenaplaćene prodaje i fakturu. |
| Upravljanje mogućnostima za poslovanje | 2594015 | Nije moguće zatvoriti ponudu kao osvojenu za klijente koji imaju **Net60** uslove plaćanja. |
| Planiranje i praćenje projekta | 2595841 | U rešenju Project for the Web, korisnici dobijaju poruku o grešci da nedostaje **msdyn\_actualstart** kada kreiraju novi zahtev za resursom. |
| Vreme i trošak | 2602511 | Polje **Odbio** za stavke vremena prikazuje **Sistem** umesto imenovanog korisnika kao osobe koja je odbila. |
| Vreme i trošak | 2602528 | Osoba koja vrši odobravanje projekta može da odobri vreme na projektima u kojima nije navedena kao osoba koja vrši odobravanje. |
| Naplata i određivanje cena | 2608550 | Korektivna faktura se može potvrditi čak i ako nema promena u originalnoj. |

## <a name="removed-and-deprecated-features"></a>Uklonjene i zastarele funkcije

Članak [Uklonjene ili zastarele funkcije u rešenju Project Operations](../../whats-new/removed-depreciated-features-project.md) opisuje funkcije koje su uklonjene ili zastarele za rešenje Dynamics 365 Project Operations.

- Uklonjena funkcija više nije dostupna u proizvodu.
- Zastarela funkcija nije u aktivnom razvoju i možda će biti uklonjena u budućoj ispravci.

Najava zastarevanja će se pojaviti u članku [Uklonjene ili zastarele funkcije u rešenju Project Operations](../../whats-new/removed-depreciated-features-project.md) 12 meseci pre nego što bilo koja funkcija bude uklonjena iz proizvoda.
