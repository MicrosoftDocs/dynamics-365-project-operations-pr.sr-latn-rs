---
title: Valuta
description: Ova tema pruža informacije o tome kako da dodate i uklonite tipove valuta u projektnim operacijama.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8d4e1d73dc183ed572fb5099d055d2fbe0c08746
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121235"
---
# <a name="currency"></a>Valuta

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Valute određuju cene za proizvode u katalogu proizvoda i troškove transakcija, kao što su ulazne porudžbine. Ako se vaši klijenti nalaze u različitim geografskim oblastima, dodajte njihove valute da biste upravljali transakcijama. Dodajte valute koje najviše odgovaraju trenutnim i budućim poslovnim potrebama.  

> [!NOTE]
> Ako je vaše okruženje Common Data Service okruženje, nalazite se u Power Platform centru administracije i izabrali ste stranicu **Valute** (**Okruženja** > [izaberite okruženje] > **Podešavanja** > **Posao** > **Valute**), stranica će biti prazna. To je zato što podešavanje valute nije podržano u Common Data Service okruženjima.

## <a name="add-a-currency"></a>Dodavanje valute  
Pre nego što započnete ovaj postupak, proverite da li vaša bezbednosna uloga uključuje dozvole administratora sistema. 

1. Izaberite okruženje u Power Platform centru administracije. 
2. Izaberite **Podešavanja** > **Posao**.
3. Izaberite **Valute**.  
4. Izaberite **Novo**.  
5. Popunite informacije po potrebi.  


   |          Polje          |                                                                                                                                                                                                                                                                                                                                                                            Opis                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **Tip valute**    | - **Sistemski** – Izaberite ovu opciju ako želite da koristite valute dostupne u aplikacijama zasnovanim na modelu u sistemu Dynamics 365. Da biste potražili valutu, izaberite **Potraži**. Kada izaberete šifru valute, **Naziv valute** i **Simbol valute** se automatski dodaju izabranoj valuti.<br />- **Prilagođeno** – Izaberite ovu opciju ako želite da dodate valutu koja nije dostupna u aplikacijama zasnovanim na modelu u sistemu Dynamics 365. U ovom slučaju morate ručno da unesete vrednosti za **Šifru valute**, **Preciznost valute**, **Naziv valute**, **Simbol valute** i **Konverziju valute**. |
   |    **Šifra valute**    |                                                                                                                                                                                                                                                                                                                                            Kratak oblik valute. Na primer **USD** za SAD dolar.                                                                                                                                                                                                                                                                                                                                            |
   | **Preciznost valute**  |                                                                                                                                                                                  Unesite broj decimala koje želite da koristite za valutu.  Možete da dodate vrednost između 0 i 4. **Napomena:** Ako ste podesili vrednost preciznosti u dijalogu **Podešavanja sistema**, ta vrednost će se prikazivati ovde.                                                                                                                                                                                  |
   |    **Ime valute**    |                                                                                                                                                                                                                                         Ako ste izabrali šifru valute sa liste dostupnih valuta u aplikacijama zasnovanim na modelu u sistemu Dynamics 365, naziv valute za izabranu šifru je prikazan ovde. Ako ste izabrali **Prilagođeni** za tip valute, nesite naziv valute.                                                                                                                                                                                                                                          |
   |   **Simbol valute**   |                                                                                                                                                                                                                                                                      Ako ste izabrali šifru valute sa liste dostupnih valuta u sistemu , simbol za izabranu valutu je prikazan ovde. Ako ste izabrali **Prilagođeni** za tip valute, unesite simbol za novu valutu.                                                                                                                                                                                                                                                                       |
   | **Konverzija valuta** |                                                                                                                                                                                                                                     Unesite vrednost izabrane valute u odnosu jednog SAD dolara. Ovo je iznos na koji se izabrana valuta konvertuje u osnovnu valutu. **Važno:** Uverite se da ste ažurirali ovu vrednost koliko često je potrebno da biste izbegli bilo koja neprecizna izračunavanja u transakcijama.                                                                                                                                                                                                                                      |


6. Kada završite, na komandnoj traci izaberite stavku **Sačuvaj** ili **Sačuvaj i zatvori**.  

   > [!TIP]
   >  Da biste uredili valutu, izaberite valutu, a zatim unesite ili izaberite nove vrednosti.  

## <a name="delete-a-currency"></a>Brisanje valute  

1. Izaberite okruženje u Power Platform centru administracije. 
2. Izaberite **Podešavanja** > **Posao**.
3. Izaberite **Valute**.  
4. Sa prikazane liste valuta, izaberite valutu koju treba izbrisati.  
5. Izaberite **Izbriši**.  
6. Potvrdite brisanje.  

> [!IMPORTANT]
>  Ne možete da izbrišete valute koje koriste drugi zapisi. Možete samo da ih deaktivirate. Deaktiviranjem zapisa o valuti ne uklanjaju se informacije o valuti uskladištene u postojeće zapise, kao što su mogućnosti za poslovanje ili porudžbine. Međutim, nećete moći da izaberete deaktiviranu valutu za nove transakcije.  
