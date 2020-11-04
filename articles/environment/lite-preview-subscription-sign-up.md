---
title: Prijavite se za pretplatu na pregled
description: Ova tema pruža informacije o tome kako da se pretplatite i primenite uslugu Project Operations Lite – od pogodbe do profakture.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5342466f308ab62a9f73a85fbd838d7c33bb1f47
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083443"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>Prijavite se za pretplatu na verziju za pregled za laganu primenu – od pogodbe do profakture

Ova tema objašnjava kako da se pretplatite na partnersku ponudu za verziju za pregled i primenite uslugu Dynamics 365 Project Operations Lite u jednostavnoj primeni – od pogodbe do profakture.

> [!NOTE]
> Ovaj postupak će se promeniti u predstojećim izdanjima usluge Project Operations.

## <a name="prerequisites"></a>Preduslovi

- Dobićete e-poruku sa pozivom da učestvujete u pregledu. Možete zatražiti verziju za pregled na [Project Operations veb-lokaciji](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Korisnik koji primeni verziju za pregled mora da ima globalna administratorska prava u Azure zakupcu.
- Pregledajte sve uslove i odredbe.

## <a name="subscribe"></a>Pretplati se

Kada dobijete [zahtev za pregled](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) odobrenje, dobićete dve ponude od kompanije Microsoft e-poštom. Ove ponude vam omogućavaju da primenite verziju za pregled usluge Project Operations:

- Dynamics 365 Project Operations (CRM) – Probna verzija za pregled
- Office 365 Project Operations – Probna verzija za pregled

> [!IMPORTANT]
> Samo jedna osoba, administrator zakupca, u organizaciji treba da izvršava ovaj zadatak. Ako niste pretplatnik na ovo izdanje, sačekajte dok se vaša organizacija ne registruje i ne primite svoje korisničke akreditive.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) – Probna verzija za pregled 

Pre nego što započnete, uverite se da ste prijavljeni u pregledač sa korisničkim poslovnim nalogom u zakupcu gde želite pregled usluge Project Operations.

1. Iskoristite prvu šifru ponude, **Dynamics 365 Project Operations (CRM) – Probna verzija za pregled** njenim lepljenjem u URL pregledača.

![Iskoristite ponudu](./media/16RedeemFirstOfferNew.png)

2. Potvrdite porudžbinu.
![Potvrdite porudžbinu](./media/17ConfirmOrderNew.png)

Videćete da je ponuda za potvrdu uspešno iskorišćena.

![Potvrda](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations – Probna verzija za pregled

Ponovite iste korake kao kod prve šifre ponude. Obavezno dodajte drugu šifru ponude koristeći isti korisnički nalog koji je korišćen sa prvom šifrom ponude.

## <a name="assign-licenses"></a>Dodeljivanje licenci

> [!IMPORTANT]
> Trebaće vam administrativni pristup Microsoft 365 portalu vaše organizacije da biste izvršili sledeće korake.


1. Idite u [Microsoft 365 centar administracije](https://portal.office.com/) da dodelite licence svojim korisnicima.

![Početna stranica centra administracije](./media/14AdminPortal.png)

2. Na stranici **Aktivni korisnici** , izaberite korisnike kojima želite da dodelite licencu.

![Dodeljivanje licenci](./media/15AssignLicenses.png)

3. Proverite da li su izabrane licence za **Dynamics 365 Project Operations (CRM) verziju za pregled** i **Office 365 Project Operations – verziju za pregled**. 
4. Izaberite **Sačuvaj promene**.

## <a name="create-a-new-cds-environment"></a>Napravite novo CDS okruženje

1. Obezbedite novo okruženje za primenu usluge Project Operations CDS prateći uputstva u temi [Model primene CDS-a](lite-deployment.md). Kada odaberete tip okruženja, obavezno koristite **probnu verziju (zasnovano na pretplati)**.
![Novo okruženje](./media/19CreateEnvironment.png)

2. Izaberite podešavanje **Omogućite Dynamics 365 aplikacije** i ostavite **Automatski primeni ove aplikacije** prazno.  
3. Izaberite **Sačuvaj** da biste kreirali okruženje.

![Dodaj bazu podataka](./media/20CreateEnvironment1.png)

4. Nakon kreiranja okruženja, instalirajte rešenje **Microsoft Dynamics 365 Project Operations**. 

![Instaliranje rešenja](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Instaliranje CDS konfiguracije i podešavanje demo podataka

Instalirajte CDS konfiguraciju i podesite demo podatke prateći uputstva u temi [Primenite demo podešavanja i podataka o konfiguraciji](lite-apply-demo-setup-config-data.md).
