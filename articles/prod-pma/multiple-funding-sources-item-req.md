---
title: Zahtevi artikala za ugovore za projekte sa više izvora finansiranja
description: Ovaj članak pruža informacije o konfigurisanju i korišćenju zahteva artikala sa više izvora finansiranja.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: a54ca1ec5e78d9d0af7b67914f6a63154c7347d3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931209"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Zahtevi artikala za ugovore za projekte sa više izvora finansiranja

_**Odnosi se na:** Project Operations za scenarije zasnovane na zalihama/proizvodnji_

Neki ugovorni ugovori za isporuke zasnovane na projektu mogu zahtevati više izvora finansiranja. Ovaj članak sadrži objašnjenja o tome kako da izaberete i konfigurišete željene izvore finansiranja kada je potrebno više izvora za projekat ili projektni ugovor.

## <a name="terminology"></a>Terminologija

- **Izvor finansiranja** – Entitet koji finansira rad na ugovoru o projektu. Ovaj entitet može biti interna organizacija ili konto eksterne fakture (kupac ili grant).
- **Kupac projekta** – Entitet kome se dostavlja rad na projektu.
- **Konto** fakture – Eksterni entitet koji plaća za rad na projektu.

## <a name="example"></a>Primer

Contoso je dobio ugovor o obnovi opreme sa dva svoja klijenta: Adatum US i Adatum Corporate. Ugovor uključuje hardverske i instalacione usluge koje će biti isporučene Adatumu US (kupcu projekta). Hardver će finansirati Adatum Corporate (račun fakture 1), a radove na instalaciji finansiraće Adatum US (račun fakture 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Podešavanje pravila podrazumevanog iznosa konta fakture za zahteve artikla

### <a name="prerequisites"></a>Preduslovi

- Microsoft Dynamics 365 Finansije i operacije verzija **10.0.27 ili novija je** potrebna za korišćenje zahteva artikala koji imaju više konta fakture.
- Administrator sistema mora da omogući zahteve artikla **sa više izvora finansiranja za opciju "Operacije projekta" na zalihama** /scenarijima zasnovanim na proizvodnji u **radnom prostoru za** upravljanje funkcijama.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Podešavanje pravila podrazumevanog vrednosti konta fakture

Da biste podesili podrazumevana pravila za konto fakture, sledite ove korake.

1. Idite na **Upravljanje projektima i računovodstvo** \> **Podešavanje** \> **Upravljanje projektom i računovodstveni parametri**.
1. Na kartici **Opšte** postavke, u odeljku Ulazne **porudžbine i zahtevi artikla** postavite **opciju Dozvoli projekte sa više izvora finansiranja na** "Da **"**.
1. U polju **Podrazumevani kupac** navedite odakle podrazumevano potiče kupac isporuke projekta na zahtev artikla:

    - **Iz izvora finansiranja** – Podrazumevani kupac isporuke projekta dolazi iz izvora finansiranja. Ako je više izvora finansiranja povezano sa ugovorom o projektu, koristiće se prvi izvor finansiranja na listi.
    - **Iz projekta** – Podrazumevani kupac isporuke projekta potiče od kupca koji je izabran u polju Nalog **zapisa** projekta.

1. Opcionalno: Postavite ili promenite podrazumevani nalog fakture u zapisima projekta:

    1. Idite na **Project management i knjigovodstvene** \> **·** \> **projekte** Svi projekti i otvorite detalje zapisa projekta.
    2. Na kartici **Opšte** postavke postavite ili ažurirajte polje Podrazumevani **konto fakture**. Konto koji navedete će biti korišćen kao podrazumevani konto fakture za nove zahteve artikala koji su kreirani za projekat. Ako polje ostavite prazno, konto fakture prvog izvora finansiranja ugovora o projektu će podrazumevano biti korišćen. Međutim, korisnici će moći da promene nalog kada sačuvaju zapis.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Izaberite konto fakture koji ćete koristiti prilikom kreiranja zahteva artikla

Da biste izabrali konto fakture koji ćete koristiti prilikom kreiranja zahteva artikla, sledite ove korake.

1. Idite na **Project management i knjigovodstvene** \> **·** \> **projekte** Svi projekti i izaberite zapis projekta.
1. Na kartici **Plan** izaberite zahteve **artikla**.
1. Kreirajte novi zapis zahteva artikla.

    - Polje "Konto fakture **"** u zapisu je podrazumevano podešeno na konto fakture koji je podešen za projekat. Možete promeniti vrednost polja Konto **fakture**, a zatim sačuvati zapis. Nakon što sačuvate zapis, više ne možete ažurirati vrednost konta **fakture**. Ako morate ažurirati vrednost konta **fakture** za zahtev artikla, izbrišite postojeći zahtev artikla, a zatim kreirajte novi koji ima željenu vrednost.
    - Podrazumevano, polje Kupac **za** zahtev artikla je postavljeno na osnovu podrazumevane **vrednosti kupca** koja je postavljena na stranici **"Upravljanje projektima i računovodstvenim parametrima** ".

    Kada se zapis zahteva artikla sačuva, sistem ga povezuje sa zapisom zaglavlja ulazne **porudžbine zahteva za** artikal. Ako nijedno zaglavlje otvorene ulazne porudžbine nema izabrani konto fakture, sistem će ga kreirati i sa njim povezati red zahteva artikla.

> [!NOTE]
> Zahtevi artikla se uvek u potpunosti fakturiše na konto fakture koji je podešen u zapisu. Sistem trenutno ne podržava pravila dodele sredstava koja imaju zahteve za artikle i neće podeliti knjiženje na osnovu podešavanja pravila dodele finansijskih sredstava.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Kreiranje zahteva artikla iz zapisa predviđanja artikla

Da biste kreirali zahtev artikla iz zapisa predviđanja artikla, sledite ove korake.

1. Idite na **Project management i knjigovodstvene** \> **·** \> **projekte** Svi projekti i izaberite zapis projekta.
1. Na kartici **Plan** izaberite predviđanja **artikla**.
1. Kreirajte novi zapis predviđanja artikla.
1. Opcionalno: Na **kartici** Projekat, u **polju Izvor finansiranja** izaberite željeni konto fakture.
1. Izaberite **stavku Kreiraj zahtev** za artikle i potvrdite poruku koju dobijate.

    > [!NOTE]
    > Sistem kopira vrednost izvora finansiranja **iz zapisa** predviđanja artikla u novokreiran zapis zahteva artikla.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Podrazumevani konto fakture kada sistem automatski kreira zahtev artikla iz reda izlazne porudžbine

Ako je opcija **"Kreiranje zahteva artikla** " postavljena na vrednost " **Da** " na stranici **"Upravljanje projektima i računovodstvenim parametrima** ", sistem automatski kreira zahtev artikla kada se sačuva novi red izlazne porudžbine projekta. Polja Konto fakture **i Zahtev** za **artiklom podrazumevano** su postavljena na vrednost polja Podrazumevani **konto fakture** u zapisu projekta. Sistem trenutno ne podržava ažuriranje ili promenu konta fakture za zapise ovog tipa.
