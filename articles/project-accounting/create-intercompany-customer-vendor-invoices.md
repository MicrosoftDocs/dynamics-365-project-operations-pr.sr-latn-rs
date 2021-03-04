---
title: Kreiranje internih faktura klijenta i dobavljača u okviru preduzeća
description: Ova tema pruža informacije o tome kako da kreirate fakture klijenta i dobavljača u okviru preduzećima.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f1560469d2bdbb8e81dc26c16b272c44446ab20a
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595544"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a>Kreiranje internih faktura klijenta i dobavljača u okviru preduzeća

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Projektni računovođa u pravnom licu koje pozajmljuje kreira fakturu klijentu u okviru preduzeća za troškove projekta koji se prenose na entitet koji se zadužuje. Nakon što se odobri i proknjiži faktura klijentu u okviru preduzeća, pravno lice koje pozajmljuje šalje fakturu u okviru preduzeća pravnom licu koje se zadužuje.

Projektni računovođa za pravno lice koje pozajmljuje može redovno da podešava grupni postupak za generiranje faktura u okviru preduzeća. Računovođa projekta određuje kriterijume, kao što su specifični projekti, za kreiranje grupnih faktura u okviru preduzeća.

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a>Ručno kreirajte fakturu klijentu u okviru preduzeća za projektne transakcije 

Koristite ovu proceduru da biste ručno kreirajte fakturu klijentu u okviru preduzeća za projektne transakcije. Potražite sate koje su radnici prijavili na projektima u pravnim licima koja se zadužuju i troškove koje je vaše pravno lice imalo u ime pravnih lica koja zadužuju. Možete pretraživati po nazivu pravnog lica, broju projektnog ugovora, broju projekta, rasponu datuma ili bilo kojoj kombinaciji ovih opcija. U rezultatima pretrage izaberite transakcije koje ćete dodati na fakturu u okviru preduzeća.

1. U usluzi Dynamics 365 Finance, idite na **Upravljanje projektima i računovodstvo** > **Fakture za projekat** > **Fakture za klijente u okviru preduzeća**. Na stranici sa listom **Fakture za klijente u okviru preduzeća**, u oknu Radnja izaberite **Novo.**
2. Na stranici **Kreiranje fakture u okviru preduzeća**, u polju **Pravno lice**, izaberite pravno lice koje se zadužuje.
3. Opciono: Unesite određeni projektni ugovor i broj projekta.
4. Suzite pretragu izborom vremenskog perioda. Unesite određene datume u polja **Datum početka** i **Datum završetka**. U rezultatima pretrage prikazuju se samo transakcije u okviru preduzeća koje su objavljene u ovom vremenskom periodu.
5. Podesite **Parametar napredne stavke u glavnoj knjizi za projekat** na **Da** i izaberite **Pretraga**.
6. U rezultatima pretrage izaberite transakcije koje ćete uključiti u predlog fakture u okviru preduzeća, a zatim izaberite **U redu**.
7. Na stranici **Faktura za klijenta u okviru preduzeća**, prikazuju se transakcije projekata u okviru preduzeća koje ste izabrali iz rezultata pretrage. Da biste izmenili transakcije pre nego što fakturu pošaljete pravnom licu koje se zadužuje, uradite sledeće:
  
    1. Otvorite stranicu **Kreiranje predloga fakture**. Izaberite dodatne transakcije u okviru preduzeća za trenutnu fakturu, a zatim izaberite **Dodaj liniju**.
    2. Da biste uklonili liniju, izaberite je, a zatim izaberite **Ukloni**.
    3. Prikazujte komentare, razloge, finansijske aspekte i druge informacije o izabranoj liniji na brzoj kartici **Linije na fakturi**.
    
8. Da biste proknjižili fakturu za klijenta u okviru preduzeća, u oknu Radnja izaberite **Proknjiži**.

> [!NOTE]
> Ako vaša organizacija zahteva da se fakture u okviru preduzeća pregledaju pre nego knjiženja, administrator sistema može postaviti tok rada za fakture u okviru preduzeća. Ako tok posla nije podešen za fakture u okviru preduzeća, možete da knjižite fakturu u okviru preduzeća.

## <a name="create-a-batch-job-for-intercompany-invoices"></a>Kreiranje grupnog posla za fakture u okviru preduzeća

Možete istovremeno kreirati više faktura mu okviru preduzeća za sva pravna lica koja se zadužuju. Koristeći funkcionalnost pretraživanja, možete, na primer, pretraživati sve transakcije koje su knjižili pozajmljeni radnici i koje su povezane sa projektima kojima upravljaju druga pravna lica. Zatim, za svako pravno lice koje se zadužuje, možete kreirati fakturu u okviru preduzeća za transakcije date u rezultatima pretrage.

1. Idite na **Upravljanje projektima i računovodstvo** > **Periodično** > **Fakture za projekat** > **Kreiranje faktura za klijente u okviru preduzeća**.
2. Na stranici **Kreiranje faktura za klijente u okviru preduzeća**, u polju **Preduzeće**, izaberite pravno lice za fakturisanje. Ako ne izaberete preduzeće, sve transakcije koje ispunjavaju kriterijume pretrage prikazuju se za sva pravna lica koja se zadužuju.
3. U okviru **Kreiraj jednu fakturu po**, izaberite da li ćete kreirati fakturu za transakcije u okviru preduzeća na osnovu projekta ili na osnovu pravnog lica koje se zadužuje.
4. Opciono: da biste izabrali određeni projekat i projektni ugovor za koji ćete kreirati fakture u okviru preduzeća, kliknite na **Izaberi**. Na stranici **Upit**, u polju **Kriterijumi**, izaberite projektni ugovor, broj projekta ili oboje, a zatim izaberite **U redu**.
5. Na kartici **Grupno**, podesite grupni postupak za kreiranje faktura u okviru preduzeća koji će se redovno ponavljati. Za više informacija pogledajte [Slanje posla grupne obrade iz obrasca](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).
6. Da biste proknjižili fakture za klijenta u okviru preduzeća, u oknu Radnja izaberite **Proknjiži**.

> [!NOTE]
> Ako vaša organizacija zahteva da se fakture u okviru preduzeća pregledaju pre nego knjiženja, administrator sistema može postaviti tok rada za fakture u okviru preduzeća. Ako tok posla nije podešen za fakture u okviru preduzeća, možete da knjižite fakture u okviru preduzeća.

## <a name="post-the-intercompany-vendor-invoice"></a>Knjiženje fakture dobavljača u okviru preduzeća

Računovođa projekta u pravnom licu koje se zadužuje može da pregleda fakture dobavljača u okviru preduzeća na čekanju kada je proknjižena odgovarajuća faktura klijenta u okviru preduzeća. U modulu Finance, u pravnom licu koje se zadužuje, idite na **Dugovanja** > **Fakture** > **Faktura dobavljača na čekanju**. Broj fakture na čekanju podudaraće se sa brojem fakture klijenta u okviru preduzeća. Proverite da li je faktura ispravna, a zatim je proknjižite. Knjiženjem fakture dobavljača u okviru preduzeća kreiraju se potknjiga projekta i transakcija glavne knjige koji odražavaju transakcione troškove pravnog lica koje se zadužuje.


[!INCLUDE[footer-include](../includes/footer-banner.md)]