---
title: Šta je novo ili promenjeno u izdanju 26 ispravke Project Service Automation verzije 3
description: U ovoj temi su navedene funkcije i ispravke koje su dostupne u izdanju ispravke 26 za Project Service Automation verzije 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 135f017533705e165230ac994d217ad7c58bab10
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280415"
---
# <a name="project-service-automation-update-release-26-v3"></a>Project Service Automation izdanje ispravke 26, u verziji 3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x. Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

U ovoj temi date su funkcije koje su nove ili su promenjene u rešenju Project Service Automation u verziji 3, izdanje ispravke 26. Ova verzija ima broj verzije V3.10.44.59 i generalno je dostupna putem samostalnog ažuriranja u decembru 2020.

## <a name="update-release-26"></a>Izdanje ispravke 26

### <a name="bug-fixes"></a>Ispravke grešaka

**Vreme i trošak**

Popravljeni su sledeći problemi:

- Korisnici mogu da promene zadatak na stavci vremena koja je odobrena/podneta.
- Greška „Referenca objekta nije podešena“ prilikom čuvanja stavke vremena.
- Uvoz stavke vremena iz dodeljivanja resursa kreira stavke vremena sa netačnim vrednostima datuma i vremena.
- Kada su instalirane aplikacije Project Service Automation i Field Service, dugme **Novo** se prikazuje dva puta na komandnoj traci za stavke vremena u aplikaciji Field Service.
- Ćelije **Dozvoli ažuriranja jedinice** i **grupe jedinica** sada rade u mreži **Procene troškova**.
- Obrazac **Ažuriraj uređivanje stavke vremena** uključuje **Vremensku osu**.
- Odobrenje vremena za stavke vremena koje se ne odnose na projekat blokiraju sistem prilikom pretrage za ulogu odobravaoca projekta.

**Upravljanje resursima**

Popravljeni su sledeći problemi:

- Dodata je validacija u dodatnoj komponenti **PostProjectCreate** za proveru primarnog zahteva pre njegovog kreiranja.
- Obrazac za brzo kreiranje **Član projektnog tima** daje izuzetak prazne reference ako se polja uklone iz obrasca.
- Generiranje zahteva za 12 sati tokom 1 godine neće uspeti.
- Poboljšana poruka o grešci za izuzetak prazne reference tokom kreiranja zahteva za resursom.

**Upravljanje projektima**

Popravljeni su sledeći problemi:

- Poboljšana validacija za odgovor na izuzetak prazne reference generisane u dodatnoj komponenti **PreProjectUpdate**.
- Projekti objavljeni u programskom dodatku za računare usluge Microsoft Project brišu neraspoređene zadatke.
- Dodata je nova validacija kada referenca projekta zadatka nije važeća zbog izuzetka prazne reference u dodatnoj komponenti **PreValidateProjectTaskUpdate**.
- Mreža člana tima ne prikazuje različite zadatke u zapisu člana tima.
- Dodate su nove poruke za proveru valjanosti i poruke greške zbog izuzetka prazne reference u dodatnoj komponenti **PreProjectTaskDelete**.

**Sales**

Popravljeni su sledeći problemi:

- Prilikom izbora stavke zasnovane na projektu u ponudu ili ugovoru, dugme **Predlog** bi trebalo da bude vidljivo samo pri odabiru linije zasnovane na proizvodu povezane sa postojećim proizvodom.
- Podelite privilegiju **Create_Product** iz privilegije **Create_ProjectContract**.
- Brisanje stavke u faktoru dovodi do neuspele prazne reference na **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]