---
title: Zahtevi artikala za ugovore za projekte sa više izvora finansiranja
description: Ovaj članak pruža informacije o konfigurisanju i korišćenju zahteva za stavke sa više izvora finansiranja.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 079856e7cf2ffa9b80ab31ebad1c1b5dbe36a4ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028505"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Zahtevi artikala za ugovore za projekte sa više izvora finansiranja

_**Odnosi se na:** Project Operations za scenarije zasnovane na zalihama/proizvodnji_

Neki ugovorni sporazumi za isporuke zasnovane na projektu mogu zahtevati više izvora finansiranja. Ovaj članak sadrži objašnjenja o tome kako da izaberete i konfigurišete željene izvore finansiranja kada je potrebno više izvora za projekat ili projektni ugovor.

## <a name="terminology"></a>Terminologija

- **Izvor finansiranja** – Entitet koji finansira ugovoreni rad na projektu. Ovaj entitet može biti interna organizacija ili spoljni poslovni kontakt na fakturi (klijent ili grant).
- **Klijent projekta** – Entitet kome se dostavlja rad na projektu.
- **Poslovni kontakt na fakturi** – Spoljni entitet koji plaća za rad na projektu.

## <a name="example"></a>Primer

Contoso je dobio ugovor o obnavljanju opreme sa dva svoja klijenta: Adatum US i Adatum Corporate. Ugovor obuhvata hardver i instalacione usluge koje će biti isporučene kompaniji Adatum US (klijentu na projektu). Hardver će finansirati Adatum Corporate (poslovni kontakt na fakturi 1), a radove na instalaciji finansiraće Adatum US (poslovni kontakt na fakturi 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Podešavanje pravila podrazumevanih vrednosti poslovnog kontakt na fakturi za zahteve za stavke

### <a name="prerequisites"></a>Preduslovi

- Microsoft Dynamics 365 Finance **u verziji 10.0.27 ili noviji** je potreban za korišćenje zahteva za stavke koje imaju više poslovnih kontakata za fakturu.
- Administrator sistema mora da omogući **Dozvoli zahteve za stavke sa više izvora finansiranja za Project Operations scenarije na zalihama/zasnovanim na proizvodnji** u radnom prostoru za **Upravljanje funkcijama**.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Podešavanje pravila za podrazumevane vrednosti poslovnog kontakta na fakturi

Da biste podesili podrazumevana pravila za poslovni kontakt na fakturi, pratite ove korake.

1. Idite na **Upravljanje projektima i računovodstvo** \> **Podešavanje** \> **Upravljanje projektom i računovodstveni parametri**.
1. Na kartici **Opšti podaci**, u odeljku **Ulazne porudžbine i zahtevi za artikle** postavite opciju **Dozvoli projekte sa više izvora finansiranja** na **Da**.
1. U polju **Podrazumevani klijent** navedite odakle podrazumevano potiče klijent za isporuku projekta na zahtevu za stavku:

    - **Iz izvora finansiranja** – Podrazumevani klijent za isporuku projekta potiče iz izvora finansiranja. Ako je više izvora finansiranja povezano sa ugovorom za projekat, koristiće se prvi izvor finansiranja na listi.
    - **Iz projekta** – Podrazumevani klijent za isporuku projekta potiče od klijenta koji je izabran u polju **Poslovni kontakt zapisa na projektu**.

1. Opciono: Postavite ili promenite podrazumevani poslovni kontakt na fakturi u zapisima projekta:

    1. Idite na **Upravljanje projektima i računovodstvo** \> **Projekti** \> **Svi projekti** i otvorite detalje o evidenciji projekta.
    2. Na kartici **Opšti podaci** podesite ili ažurirajte polje **Podrazumevani poslovni kontakt na fakturi** . Poslovni kontakt koji navedete biće korišćen kao podrazumevani poslovni kontakt na fakturi za nove zahteve za stavke koji su kreirani za projekat. Ako polje ostavite prazno, poslovni kontakt na fakturi prvog izvora finansiranja ugovora za projekat će podrazumevano biti korišćen. Međutim, korisnici će moći da promene poslovni kontakt kada sačuvaju zapis.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Izaberite poslovni kontakt na fakturi koji ćete koristiti prilikom kreiranja zahteva za stavke

Da biste izabrali poslovni kontakt na fakturi koji ćete koristiti prilikom kreiranja zahteva za stavke, pratite ove korake.

1. Idite na **Upravljanje projektima i računovodstvo** \> **Projekti** \> **Svi projekti** i izaberite zapis.
1. Na kartici **Plan** izaberite **Zahtevi za stavku**.
1. Kreirajte novi zapis zahteva za stavku.

    - Podrazumevano, polje **Poslovni kontakt na fakturi** u zapisu postavlja se na poslovni kontakt na fakturi koji je podešen za projekat. Možete promeniti vrednost polja **Poslovni kontakt na fakturi**, a zatim sačuvati zapis. Nakon što sačuvate zapis, više ne možete ažurirati vrednost za **Poslovni kontakt na fakturi**. Ako morate ažurirati vrednost za **Poslovni kontakt na fakturi** za zahtev za stavkom, izbrišite postojeći zahtev za stavkom, a zatim kreirajte novi koji ima željenu vrednost.
    - Podrazumevano, polje **Klijent** za zahtev za stavkom je postavljeno na osnovu vrednosti **Podrazumevani klijent** koja je postavljena na stranici **Upravljanje projektima i računovodstvenim parametrima**.

    Kada se zapis zahteva za stavkom sačuva, sistem ga povezuje sa zapisom zaglavlja **Ulazne porudžbine zahteva za stavkom**. Ako nijedno zaglavlje otvorene ulazne porudžbine nema izabrani poslovni kontakt na fakturi, sistem će ga kreirati i sa njim povezati red zahteva za stavkom.

> [!NOTE]
> Zahtevi za stavku se uvek u potpunosti fakturišu na poslovni kontakt na fakturi koji je podešen u zapisu. Sistem trenutno ne podržava pravila dodele sredstava koja imaju zahteve za stavke i neće podeliti knjiženje na osnovu podešavanja pravila dodele finansijskih sredstava.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Kreiranje zahteva za stavku iz zapisa predviđanja stavke

Da biste kreirali zahtev za stavku iz zapisa predviđanja stavke, pratite ove korake.

1. Idite na **Upravljanje projektima i računovodstvo** \> **Projekti** \> **Svi projekti** i izaberite zapis.
1. Na kartici **Plan** izaberite **Predviđanja za stavku**.
1. Kreirajte novi zapis predviđanja za stavku.
1. Opciono: Na kartici **Projekat**, u polju **Izvor finansiranja** izaberite željeni poslovni kontakt na fakturi.
1. Izaberite **Kreiraj zahtev za stavku** i potvrdite poruku koju dobijate.

    > [!NOTE]
    > Sistem kopira vrednost za **Izvor finansiranja** iz zapisa predviđanja za stavku u novokreirani zapis zahteva za stavku.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Podrazumevani poslovni kontakt na fakturi kada sistem automatski kreira zahtev za stavku iz reda izlazne porudžbine

Ako je opcija **Kreiranje zahteva za stavku** postavljena na vrednost **Da** na stranici **Upravljanje projektima i računovodstvenim parametrima**, sistem automatski kreira zahtev za stavkom kada se sačuva novi red izlazne porudžbine projekta. Podrazumevano, polja **Poslovni kontakt na fakturi** i **Zahtev za stavku** su podešena na vrednost polja **Podrazumevani poslovni kontakt na fakturi** u zapisu projekta. Sistem trenutno ne podržava ažuriranje ili promenu poslovnog kontakta na fakturi za zapise ovog tipa.
