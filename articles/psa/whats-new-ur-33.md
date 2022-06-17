---
title: Šta je novo ili promenjeno u izdanju 33 ispravke usluge Project Service Automation verzije 3
description: Ovaj članak navodi funkcije i ispravke koje su dostupne u izdanju za ažuriranje automatizacije usluge projekta Release 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.reviewer: johnmichalak
ms.openlocfilehash: d9c282e8b95b111ce71fb441e4dbb2d04f904e0f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915433"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Šta je novo ili promenjeno u izdanju 33 ispravke usluge Project Service Automation verzije 3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da najavimo najnoviju ispravku za aplikaciju Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Kompatibilna je sa sistemom Dynamics 365 9.x. Da biste se ažurirali na ovo izdanje, posetite stranicu centra administracije za Dynamics 365 mrežna rešenja i instalirajte ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).

Ovaj članak navodi funkcije i ispravke koje su nove ili promenjene za V3 za automatizaciju projektne usluge, izdanje za ažuriranje 33. Ova verzija ima broj verzije 3.10.54.98 i opšte je dostupna putem samostalnog ažuriranja u julu 2021.

## <a name="update-release-33"></a>Izdanje ispravke 33

### <a name="bug-fixes"></a>Ispravke grešaka

**Vreme i trošak**

Popravljeni su sledeći problemi:

- Dva zaključana polja, **msdyn_description** i **msdyn_externaldescription** mogu se uređivati nakon prosleđivanja.
- Poruka o grešci se javlja ako se kreira trošak koji nije povezan sa projektom.
- Kada se kreira stavka vremena, uloga resursa je podrazumevano neaktivna.
- Stavke u glavnoj knjizi povezane sa opozvanim i izbrisanim troškovima se ne brišu.
- Na **obrascu za brzo kreiranje stavke vremena**, ažurirajte prikaz **Lista projektnih zadataka** da biste podrazumevano prikazani datum promenili u datum početka zadatka.
- Kada kreirate unos vremena sa kartice **Povezano** resursa koji može da se rezerviše, stavka vremena se pogrešno kreira za prijavljenog korisnika umesto za nadređeni resurs koji može da se rezerviše.
- Nova polja se dodaju u dijalog **Grupno odobravanje MDD**.

**Planiranje projekta**

Popravljeni su sledeći problemi:
- Spore performanse kreiranja projekata kada se predlošci radnog vremena projekta primenjuju sa složenim kalendarima.
- Kada je datum početka veći od datuma završetka, na predlošku projekta kopiranja prikazuje se greška zbog razlika u vremenskoj komponenti svakog polja.

**Upravljanje resursima**

Popravljeni su sledeći problemi:
- U upitu o ukupnoj iskorišćenosti resursa koristi se netačan parametar, a XML dovodi do netačnih rezultata filtera na mreži **Ukupna iskorišćenost resursa**.
- Potvrda **Produžetak rezervacija** prikazuje netačan datum završetka za rezervacije.

**Prodaja**

Popravljeni su sledeći problemi:
- Poruka o grešci se javlja ako se kreira cena kategorije sa vrednostima koje nedostaju.
- Javlja se poruka o grešci ako se kreira kontrolna tačka predmeta ugovora bez stavke porudžbine.
