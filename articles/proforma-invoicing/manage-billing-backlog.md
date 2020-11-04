---
title: Upravljanje zaostalim naplatama
description: Ova tema pruža informacije o tome kako da prikažete i radite sa zaostalim naplatama u usluzi Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ec77f3911a460b96414a61bc44ea254f1b7da660
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088083"
---
# <a name="manage-the-billing-backlog"></a>Upravljanje zaostalim naplatama

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Dynamics 365 Project Operations ima dva namenska prikaza koji će vam pomoći da radite sa zaostalim naplatama i upravljate njima. To su **Kontrolne tačke sa fiksnom cenom** i **Zaostale naplate vremena i materijala**. Da biste izabrali prikaz, u oblasti **Prodaja** u usluzi Project Operations, na levoj navigacionoj stranici izaberite **Naplata**. Veze zaostalih naplata se čuvaju tamo.

## <a name="fixed-price-milestones"></a>Kontrolne tačke fiksne cene

Ovaj prikaz navodi sve kontrolne tačke sa fiksnom cenom u svim predmetima projektnih ugovora u sistemu. Jednu ili više kontrolnih tačaka možete označiti kao **Spremno za fakturisanje** ili **Nije spremno za fakturisanje** iz ovog prikaza. Kada obeležite kontrolnu tačku kao **Spremno za fakturisanje** , ona postaje dostupna za radnu verziju fakture.

Kada predmeti ugovora sa više klijenata imaju način naplate sa fiksnom cenom, stvara se jedna kontrolna tačka za svakog kupca na predmetu ugovora. Korisnik kreira kontrolnu tačku i ona se interno deli na zapise o kontrolnim tačkama specifične za klijenta, u skladu sa podelom procenata naplate definisanom za svakog klijenta u predmetu ugovora. U prikazu **Kontrolne tačke fiksne cene** videćete pojedinačne zapise kontrolnih tačaka specifične za klijenta. Svaki od ovih zapisa kontrolnih tačaka može se označiti kao **Spremno za fakturisanje** nezavisno od ovog prikaza. Kada se jedna ili više povezanih kontrolnih tačaka razdvoji kao **Spremno za fakturisanje** , zaglavlje se pomera u status **U toku** iz **Nije započeto**. Kada su fakturisane sve podele kontrolnih tačaka, status kontrolne tačke zaglavlja postaje **Završeno**.

Kontrolna tačka u radnoj verziji fakture prikazana je u ovom prikazu sa statusom naplate **Kreirana je faktura za klijenta**. Kada se potvrdi radna verzija fakture, status naplate na ovom zapisu ažurira se na **Faktura je proknjižena**. Ažuriranje ove vrednosti statusa pomoću prilagođenog koda se ne preporučuje. Project Operations neće pravilno funkcionisati ako se ove vrednosti statusa ažuriraju prilagođenim kodom.

## <a name="time-and-material-billing-backlog"></a>Neizvršavanje naplate vremena i materijala

U ovom prikazu su navedene svi nenaplaćeni stvarni iznosi prodaje koji nisu fakturisani u svim projektnim ugovorima u sistemu. Jedan ili više nenaplaćenih stvarnih iznosa prodaje možete označiti kao **Spremno za fakturisanje** ili **Nije spremno za fakturisanje** iz ovog prikaza. Označavanje nenaplaćenog stvarnog iznosa prodaje kao **Spremno za fakturisanje** omogućava stavljanje fakture u radnu verziju.

Nenaplaćeni stvarni iznosi prodaje koji imaju status **Ne treba da pređe** za **Nije uspelo** ne mogu da se označe kao **Spremno za fakturisanje**. Ako ove stvarne iznose treba označiti kao takve, resetujte status na drugim stvarnim iznosima na predmetu ugovora koji su prosleđeni, a zatim procenite status **Ne treba da pređe**.

U slučaju predmeta ugovora sa više klijenata koje imaju način naplate za vreme i materijal, kada se odobre vreme i troškovi, za svakog klijenta na predmetu ugovora kreira se nenaplaćeni stvarni iznos prodaje prema podeli procenta naplate definisanoj za svakog klijenta na predmetu ugovora. U prikazu **Zaostale naplate vremena i materijala** videćete ove pojedinačne nenaplaćene stvarne troškove prodaje specifične za kupca. Svaki od ovih zapisa nenaplaćenih stvarnih troškova prodaje može se označiti kao **Spremno za fakturisanje** nezavisno od ovog prikaza.

Nenaplaćeni stvarni iznos prodaje u radnoj verziji fakture prikazan je u ovom prikazu sa **Statusom naplate** koji ima vrednost **Kreirana je faktura za klijenta**. Kada se potvrdi radna verzija fakture, status naplate na ovom zapisu ažurira se na **Faktura za klijenta je proknjižena**. Ažuriranje ove vrednosti statusa kada je u ovom statusu pomoću prilagođenog koda se ne preporučuje. Project Operations neće pravilno funkcionisati kada se ove vrednosti statusa ažuriraju prilagođenim kodom.
