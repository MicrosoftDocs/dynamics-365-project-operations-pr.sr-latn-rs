---
title: Šta je novo ili promenjeno u izdanju 32 ispravke usluge Project Service Automation verzije 3
description: U ovoj temi navedene su funkcije i ispravke koje su dostupne u izdanju 32 ispravke usluge Project Service Automation verzije 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 023e51e834060a35d2d7e3469d34297192e38ba11c12a2c4f57424213aba44ba
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994878"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Šta je novo ili promenjeno u izdanju 32 ispravke usluge Project Service Automation verzije 3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da najavimo najnoviju ispravku za aplikaciju Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Kompatibilna je sa sistemom Dynamics 365 9.x. Da biste se ažurirali na ovo izdanje, posetite stranicu centra administracije za Dynamics 365 mrežna rešenja i instalirajte ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).

U ovoj temi navedene su funkcije koje su nove ili promenjene u izdanju 32 ispravke usluge Project Service Automation verzije 3. Ova verzija ima broj verzije 3.10.53.108 i opšte je dostupna putem samostalnog ažuriranja u junu 2021.

## <a name="update-release-32"></a>Izdanje ispravke 32

### <a name="bug-fixes"></a>Ispravke grešaka

#### <a name="general"></a>Opšte

- Kada glavna nadogradnja ne uspe, treba blokirati samo glavne ulazne tačke aplikacije kako bi se osiguralo da deljeni entiteti i dalje budu dostupni.

#### <a name="time-and-expense"></a>Vreme i trošak

Popravljeni su sledeći problemi:

- **TimeEntriesImportFromResourceAssignment** ne održava vremena početka i završetka isečaka konture dodele resursa.
- Kada izaberete **Otvori stavku** na mreži **Stavka vremena**, možda ćete biti sprečeni da izaberete druge obrasce.
- Dok uvozite zadatke u stavke vremena, upit klijentskog koda može da generiše dugu URL adresu koja ne uspeva u upitu.
- U mreži **Stavka vremena**, kada se vrednost izbriše iz ćelije, fokus ne ostaje u mreži.
- Dugme **Odbaci** je uklonjeno iz prikaza **Odobrenja obrade** za moderna odobrenja.
- Na stabilnost i performanse grupnog odobravanja stavke vremena utiču zastoji i neuspeh u odgovarajućem rukovanju prilagođavanjima koja su povezana sa entitetom **Stavka vremena**.

#### <a name="project-planning"></a>Planiranje projekta

- Izuzetak nulte reference se generiše kada ažurirate projekat koji ima nultu vrednost u polju **Jedinica ugovaranja**.
- **Osveži ukupne vrednosti projekata** pogrešno izračunava preostali trošak i preostalu prodaju u projektu.
- Prekomerni proračuni cena utiču na performanse povezane sa ažuriranjima na konturama dodele resursa.

#### <a name="resource-management"></a>Upravljanje resursima

Sledeći problem je ispravljen:

- Kada je kapacitet kalendara resursa koji može da se rezerviše veći od 1, Project Service Automation pogrešno prepoznaje kapacitet kao 0 (nula). Stoga se u prikazu rasporeda javlja beskonačna petlja.

#### <a name="sales"></a>Prodaja

Popravljeni su sledeći problemi:

- Kada se kreira stavka u glavnoj knjizi koja ima prilagođeni tip transakcije, javlja se sledeći izuzetak nulte reference: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.
- Uloge i kategorije koje su deaktivirane pre kopiranja ponude ne bi trebalo dodavati ulogama koje se naplaćuju i kategorijama novokopirane ponude.
- Datum dokumenta i datum obračuna nisu usklađeni sa datumom početka koji je naveden u detaljima stavke fakture koja se kreira direktno na radnoj verziji fakture.
- Izuzeci od nulte reference se generišu u scenarijima koji su povezani sa deaktivacijom uloga i kategorija pre kopiranja ponude.
- Radnja **Ažuriranje cena** na stranici **Projekti** ne ažurira procene troškova i procene materijala.