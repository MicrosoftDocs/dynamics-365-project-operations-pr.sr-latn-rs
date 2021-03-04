---
title: Kreirajte napredne ugovore za naplatu na osnovu napretka
description: Ova tema objašnjava kako se kreiraju projektni ugovori tako da možete generisati fakture za klijente na osnovu procenta završenog posla.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1a83785a9db4dffc4585acf11ef971c08594f312
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083709"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Kreirajte napredne ugovore za naplatu na osnovu napretka
[!include [banner](../includes/banner.md)]

Ova tema objašnjava kako se kreiraju projektni ugovori tako da možete kreirati fakture za klijente na osnovu procenta završenog posla. Iznosi faktura se automatski izračunavaju za budžetske kategorije posla koje ste postavili za projekat. Vreme na fakturi se postavlja kada pregovarate sa klijentom o ugovoru o projektu.

Koristite procedure u ovoj temi za postavljanje ugovora, pridruženog projekta i pravila obračuna koji izračunavaju iznose faktura za budžetske kategorije posla koje ste postavili za projekat.

Nakon što napravite ugovor i projekat, možete da podesite detalje o projektu. Na primer, možete definisati aktivnosti i dodeliti radnike projektu.

## <a name="example"></a>Primer

Vaša organizacija je firma za razvoj softvera. Pristajete da razvijete paket za obračun zarada za klijenta za ukupnu naknadu od 20.000 američkih dolara (USD). Vaša organizacija pristaje da fakturiše klijentu kako dovršavate određene procente projekta. Za rad postavljate sledeće kategorije projekata kako biste ih mogli koristiti u procesu naplate:

- Konsultantske usluge
- Dizajn
- Instalacija

Postavljate i pravila naplate koja automatski izračunavaju iznose faktura za procenat završenog posla na projektu za svaku kategoriju.

Menadžer budžeta kreira budžet za kategorije projekata. Količina obavljenog posla automatski se izračunava kao procenat stvarnog posla u poređenju sa planiranim iznosima.

## <a name="prerequisites"></a>Preduslovi

Pre nego što kreirate projekat koji koristi pravila naplate, morate podesiti sekvence brojeva za pravila naplate i dnevnik naknada koji se koristi za knjiženje napredovanja.

1. Idite na **Upravljanje projektima i računovodstvo** \> **Podešavanje** \> **Upravljanje projektom i računovodstveni parametri**.
2. Na stranici **Upravljanje projektom i računovodstveni parametri** , na kartici **Brojčane sekvence** podesite redosled brojeva koji želite da koristite prilikom kreiranja pravila za obračun.
3. Idite na **Upravljanje projektima i računovodstvo** \> **Dnevnici** \> **Naknada**.
4. Na stranici **Dnevnik naknada** , izaberite **Novo** i unesite naziv dnevnika.

## <a name="create-a-contract-for-progress-billings"></a>Napravite ugovor za napredak fakturisanja

Koristite ovaj postupak za kreiranje ugovora o projektu za projekat sa fiksnom cenom. Fakturu za projekat kreirate kada posao koji je završen na projektu dostigne određeni procenat.

1. Idite na **Upravljanje projektima i računovodstvo** \> **Projekti** \> **Ugovori projekata**.
2. Na stranici **Ugovori projekata** izaberite **Novo**.
3. U dijalogu **Novi ugovor o projektu** postavite sledeća polja:

    - **Ime**
    - **Tip finansiranja**
    - **Izvor finansiranja**
    - **Valuta prodaje** - Ova valuta se podrazumevano koristi za račune kupaca koji su povezani sa projektnim ugovorom. Međutim, valutu prodaje možete promeniti na određenoj fakturi kupca.

4. Izaberite **U redu**. Podaci se kopiraju u zaglavlje stranice **Projektni ugovori**.
5. Na stranici **Projektni ugovori** , popunite ostatak potrebnih podataka za projekat.

## <a name="create-a-project-for-progress-billings"></a>Napravite projekat za napredak fakturisanja

Sledite ove korake da biste kreirali projekat i sve potprojekte koji su povezani sa projektnim ugovorom.

1. Idite na **Upravljanje projektima i računovodstvo** \> **Projekti** \> **Svi projekti**.
2. Na stranici **Svi ugovori** izaberite **Novo**.
3. U dijalogu **Novi projekat** , u polju **Tip projekta** izaberite **Vreme i materijal**.
4. Izaberite grupu projekata. Projektna grupa definiše informacije o objavljivanju za projekte koji su dodeljeni grupi.
5. Izaberite **Kreirajte projekat**.
6. Nakon kreiranja projekta, postavite fazu projekta na **U toku**.

## <a name="create-a-budget-for-a-project"></a>Kreiranje budžeta za projekat

Kategorije budžeta se koriste za automatsko izračunavanje iznosa faktura za procenat završenog posla za svaku kategoriju. Sledite ove korake da biste kreirali budžetske kategorije za procenjene troškove.

1. Idite na **Upravljanje projektima i računovodstvo** \> **Projekti** \> **Svi projekti**.
2. Na stranici **Svi projekti** izaberite i otvorite projekat koji želite.
3. Na stranici **Projekti** , u oknu akcija, na kartici **Plan** , u grupi **Budžet** izaberite **Budžet projekta**.
4. Na stranici **Budžet projekta** unesite procenjeni trošak za svaku kategoriju u projektu.

## <a name="create-billing-rules-for-progress-billings"></a>Kreirajte pravila naplate za napredovanje računa

1. Idite na **Upravljanje projektima i računovodstvo** \> **Projekti** \> **Ugovori projekata**.
2. Na stranici **Ugovori o projektima** izaberite i otvorite ugovor o projektu.
3. Na stranici ugovora o projektu, na brzoj kartici **Pravila za naplatu** izaberite **Dodaj**.
4. Na stranici **Pravilo za obračun** , u polju **Tip linije** izaberite **Napredak**.
5. Na brzoj kartici **Detalji linije pravila za obračun** , u polju **Vrednost ugovora** unesite ukupnu vrednost ugovora.
6. U polju **Kategorija** odaberite kategoriju u kojoj ćete objaviti transakciju naknade.
7. U polju **Projekat** izaberite projekat koji koristi ovo pravilo naplate.
8. Opcionalno: Dodelite pravilo naplate dodatnim projektima. Na brzoj kartici **Projekat** , u odeljku **Dostupni projekti** izaberite projekat, a zatim pritisnite dugme sa strelicom udesno da biste dodali projekat u odeljak **Odabrani projekti**.
9. Opcionalno: Izračunajte procentualni iznos koji kupac zadržava od plaćanja na računu. Na brzoj kartici **Uslovi zadržavanja plaćanja** izaberite izvor finansiranja, a zatim u polju **Procenat zadržavanja** unesite procenat zadržavanja.
10. Ponovite ove korake da biste kreirali dodatna pravila za obračun za projektni ugovor.


[!INCLUDE[footer-include](../includes/footer-banner.md)]