---
title: Šta je novo ili promenjeno u izdanju 37 ispravke za Project Service Automation verzije 3
description: U ovom članku navedene su funkcije i ispravke koje su dostupne u izdanju 37 ispravke usluge Microsoft Dynamics 365 Project Service Automation verzije 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: bdbb125b4f41bb9970f5bd8a01cf0bb863c34738
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922515"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Šta je novo ili promenjeno u izdanju 37 ispravke za Project Service Automation verzije 3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da najavimo najnoviju ispravku za aplikaciju Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Kompatibilna je sa sistemom Dynamics 365 9.x. Da biste se ažurirali na ovo izdanje, posetite stranicu centra administracije za Dynamics 365 mrežna rešenja i instalirajte ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).

U ovom članku date su funkcije koje su nove ili su promenjene u izdanju ispravke 37 u rešenju Project Service Automation u verziji 3. Ova verzija ima broj V3.10.58.120 i opšte je dostupna kroz samostalnu ispravku u novembru 2021.

## <a name="update-release-37"></a>Izdanje ispravke 37

### <a name="bug-fixes"></a>Ispravke grešaka

Popravljeni su sledeći problemi.

**Vreme i trošak**
- Korisnici ne mogu da brišu unos vremena tako što će obrisati ćeliju.
- Prikaz **Moje neuspelo odobrenje** sadrži samo odobrenja projekata sa statusom **Poslato**.

**Upravljanje projektima**
- Korisnici dobijaju grešku u izuzetku bez reference prilikom otvaranja projekta u programskom dodatku Microsoft za računare ako je naziv pozicije člana projektnog tima prazan.
- Ne postoji dugme **Sačuvaj** na stranici **Projektni zadatak** tako da korisnici ne mogu da sačuvaju promene na zapisima projekta.
- Korisnici ne mogu da izbrišu projekat koji ima zadatak povezan sa ponudom sa statusom **Osvojeno**.

**Prodaja**
- Polje **Valuta** na stranici **Projekat** se ažurira tako da se podudara sa primenjenom valutom predloška.
- Cena se nepravilno izračunava za zadatke koji imaju više valuta.
