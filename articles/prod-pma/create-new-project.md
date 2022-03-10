---
title: Kreirajte novi projekat
description: Ova tema pruža informacije o tome kako da kreirate nov projekat.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5aa5e00252697f91a585eaaa83a0c8a39b315cc1b25fcbf6343fdf2ce31a824e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985968"
---
# <a name="create-a-new-project"></a>Kreirajte novi projekat

[!include [banner](../includes/banner.md)]

Obavite sledeće korake da biste kreirali novi projekat.

1. Na stranici **Menadžment projekta** izaberite **Novi projekat** i unesite sledeće vrednosti:

    - **Tip projekta:** Vreme i materijal
    - **Naziv projekta:** Nadogradnja XYZ faza 2
    - **Grupa projekata:** TM\_WIP
    - **ID ugovora o projektu:** 00000002

2. Izaberite **Kreirajte projekat**.

## <a name="assign-a-resource-to-a-project"></a>Dodeljivanje resursa projektu

1. Na stranici **Radnici**, na listi **Radnici**, izaberite zapis za radnika za kojeg ste prethodno podesili kompetencije i otvorite zapis radnika.
2. U oknu radnji, na kartici **Projekat**, u grupi **Podešavanje** izaberite **Dodeli projekte**.
3. Na stranici **Dodele projekata za validaciju resursa**, na kartici **Projekti**, u polju **Dodaj projekat izabranim projektima**, filtrirajte prema projektu **Nadogradnja XYZ faza 2**.
4. U oknu **Preostali projekti**, izaberite projekat, a zatim izaberite dugme sa strelicom da biste ga dodali u okno **Izabrani projekti**.

Takođe možete da dodelite kategorije za resurs po potrebi. Tip kategorije je ili **Trošak** ili **Prihod**. Tip kategorije određuje vaša organizacija. Ako za resurs nisu dodeljene kategorije, Finance traži podrazumevanu kategoriju cena po satu za troškove i prihod.

## <a name="set-up-project-resource-and-role-characteristics"></a>Podešavanje karakteristika i uloga resursa projekta

Menadžer projekta može koristiti funkcionalnost resursa za projekat da bi kreirao uloge potrebne za projekat. Uloge se mogu koristiti ako su potvrđeni resursi i dalje nepoznati kada se resursi rezervišu. Uloge se mogu privremeno rezervisati kao planirani resursi, tako da možete nastaviti faze planiranja projekta.

[![Primer uloge.](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenario:** Contoso je angažovan da završi projekat „Vreme i materijal“ koji ima odobrenu povelju projekta. Mlađi menadžer projekta još uvek dovršava opseg projekta. Menadžer resursa trenutno identifikuje određene resurse koji će biti rezervisani za rad na novom projektu. Zbog kritične prirode projekta, sponzor projekta zatražio je starijeg menadžera projekta kao jednu od uloga. Menadžer resursa mora nabaviti novi resurs i definisati ulogu u sistemu u slučaju da mlađi menadžer projekta zahteva informacije o resursima tokom planiranja projekta.

Sledeći koraci pokazuju kako menadžer resursa može da postavi ulogu višeg menadžera projekta i poveže karakteristike resursa sa njom. Kasnije se uloga može koristiti za traženje dostupnih resursa koji odgovaraju traženim kompetencijama resursa.

1. Na stranici **Podešavanje uloga** izaberite **Nova** i unesite sledeće vrednosti:

    - **ID uloge:** Viši menadžer projekta
    - **Opis:** Viši menadžer projekta

2. Izaberite **Kreiraj**.
3. Izaberite ulogu **Viši menadžer projekta**, a zatim izaberite **Konfiguriši karakteristike**.
4. U polju **Tip karakteristike**, izaberite **Veština**.
5. U polju **Dostupne karakteristike**, unesite veštinu za traženje.
6. U polju **Tip karakteristike**, izaberite **Certifikat**.
7. U polju **Dostupne karakteristike**, unesite tip certifikata za traženje.

## <a name="assign-a-project-resource-to-a-project"></a>Dodeljivanje resursa projektu

1. Na stranici **Svi projekti** izaberite projekat **Nadogradnja XYZ faza 2**.
2. Na kartici **Projektni tim i raspoređivanje**, izaberite **Dodaj**.
3. U polju **Uloga** izaberite **Član tima**.
4. Izaberite **Rezerviši iz kalendara**.
5. Na stranici **Dostupnost resursa** izaberite **Pogledajte podešavanja**.
6. Na stranici **Prilagodite postavke prikaza**, unesite sledeće vrednosti:

    - **Format za prikaz opsega datuma:** Dan
    - **Prikaži opise dostupnosti:** Da
    - **Prikaži preostali kapacitet:** Da

7. Izaberite resurs u listi resursa.
8. Izaberite **Fiksna rezervacija** i **Puni kapacitet**.

## <a name="assign-a-resource-to-a-default-role"></a>Dodeljivanje resursa podrazumevanoj ulozi

Da bi pomogli menadžerima projekata ili resursa da dalje dubinski pretražuju resurse koji mogu biti rezervisani za projekat. Podrazumevanu ulogu možete povezati sa postojećim ili novostečenim resursom. Na primer, kada je Danijel zaposlen, imao je iskustvo i veštine da popuni ulogu poslovnog analitičara. Menadžer resursa dodelio je ovu ulogu Danijelu kao podrazumevanu. Stoga je menadžer resursa dodao Danijela u skup poslovnih analitičara koji su dostupni za rad na projektima.

Tokom rezervacije resursa, menadžeri projekata mogu filtrirati resurse uloga koji su dostupni za rad na projektima. Ove informacije mogu da koriste kao jedan kriterijum kada obavljaju analizu odluka prema više kriterijuma tokom popunjavanja resursa. Oni takođe mogu da dodaju druge karakteristike resursa u filter za traženje resursa koji imaju specifične veštine, obrazovanje i iskustvo za dati projekat.

**Scenario:** Odobreni projekat je započeo, a uloga višeg menadžera projekta bila je rezervisana kao planirani resurs tokom faze planiranja projekta. Menadžer resursa je sada nabavio resurs za ispunjavanje uloge višeg menadžera projekta.

1. Na stranici **Lista resursa**, izaberite **Danijel Goldšmit**.
2. Na stranici **Uloga resursa** izaberite **Nova** i unesite sledeće vrednosti:

    - **Stupa na snagu:** Unesite trenutni datum.
    - **Isticanje:** Unesite **Nikad**.
    - **Uloga:** Unesite **Viši menadžer projekta**.

3. Izaberite **Sačuvaj**, a zatim zatvorite stranicu.
4. Na kartici **Kompetencije**, dodajte veštinu **Menadžment projekta** i **PMP** certifikat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]