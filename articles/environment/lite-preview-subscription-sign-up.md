---
title: Upisivanje za pretplatu na verziju za pregled – jednostavno
description: Ovaj članak pruža informacije o tome kako da se pretplatite i primenite uslugu Project Operations jednostavna primena – od pogodbe do profakture.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 29bf31cd1bc9c1c5ac757de989154b4c7acc53fe
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410093"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Upisivanje za pretplatu na verziju za pregled – jednostavno 

Ovaj članak objašnjava kako da se pretplatite na ponudu probne verzije i primeniti Dynamics 365 Project Operations jednostavnu primenu – od pogodbe do profakture.

> [!NOTE]
> Ovaj postupak će se promeniti u predstojećim izdanjima usluge Project Operations.

## <a name="prerequisites"></a>Preduslovi
- Korisnik koji primeni verziju za pregled mora da ima globalna administratorska prava u Azure zakupcu. Zakupca možete kreirati tokom prvog iskorišćavanja ponude.

> [!IMPORTANT]
> Samo jedna osoba, administrator zakupca, u organizaciji treba da izvršava ovaj zadatak. Ako niste pretplatnik na ovo izdanje, sačekajte dok se vaša organizacija ne registruje i ne primite svoje korisničke akreditive.
> 
> Probne verzije se koriste jednokratno u zakupcu. Probnu verziju možete pokrenuti samo jednom. Preporučujemo vam da kreirate novog zakupca u svrhu probne verzije.

### <a name="dynamics-365-project-operations-trial"></a>Dynamics 365 Project Operations probna verzija 

Pre nego što započnete, uverite se da ste prijavljeni u pregledač sa korisničkim poslovnim nalogom u zakupcu gde želite pregled usluge Project Operations.

1. Idite na [probnu verziju usluge Project Operations](https://aka.ms/try-po) da biste iskoristili kôd za prvu ponudu, **Dynamics 365 Project Operations**.
2. Potvrdite porudžbinu.

  Videćete potvrdu da je ponuda uspešno iskorišćena.

## <a name="assign-licenses"></a>Dodeljivanje licenci

> [!IMPORTANT]
> Trebaće vam administrativni pristup Microsoft 365 portalu vaše organizacije da biste izvršili sledeće korake.


1. Idite u [Microsoft 365 centar administracije](https://portal.office.com/) da dodelite licence svojim korisnicima.
2. Na stranici **Aktivni korisnici**, izaberite korisnike kojima želite da dodelite licencu.
3. Proverite da li je izabrana licenca za **Dynamics 365 Project Operations**. 
4. Izaberite **Sačuvaj promene**.

## <a name="create-a-new-dataverse-environment"></a>Napravite novo Dataverse okruženje

1. Obezbedite novo okruženje za primenu usluge Project Operations Dataverse prateći uputstva u članku [Model primene za Dataverse](lite-deployment.md). Kada odaberete tip okruženja, obavezno koristite **probnu verziju (zasnovano na pretplati)**.

  ![Novo okruženje.](./media/19CreateEnvironment.png)

2. Izaberite podešavanje **Omogućite Dynamics 365 aplikacije** i ostavite **Automatski primeni ove aplikacije** prazno.  
3. Izaberite **Sačuvaj** da biste kreirali okruženje.

  ![Dodaj bazu podataka.](./media/20CreateEnvironment1.png)

4. Kada kreirate okruženje, instalirajte **Microsoft Dynamics 365 Project Operations** rešenje. 

![Instaliranje rešenja.](./media/21InstallSolution.png)

## <a name="set-up-demo-data"></a>Konfigurisanje demonstracionih podataka

Konfigurišite demonstracione podatke prateći uputstva u članku [Primenite demo podešavanja i podataka o konfiguraciji](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
