---
title: Prijavljivanje za pretplate na verziju za pregled usluge Project Operations za scenarije resursa / bez zaliha
description: Ova tema pruža informacije o načinu pretplate i primene usluge Project Operations za scenarije zasnovane na resursima / bez zaliha.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4c2cd4c5d4dfbb95398932d432864cf0d4d5d54d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276860"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Prijavljivanje za pretplate na verziju za pregled usluge Project Operations za scenarije resursa / bez zaliha

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Ova tema objašnjava kako se pretplatiti na verziju za pregled / partnersku ponudu i primenu Project Operations okruženja za scenarije zasnovane na resursima / bez zaliha.

## <a name="prerequisites"></a>Preduslovi

- Dobićete e-poruku sa pozivom da učestvujete u pregledu. Možete zatražiti verziju za pregled na [Project Operations veb-lokaciji](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Korisnik koji primeni verziju za pregled mora da ima globalna administratorska prava u Azure zakupcu.
- Za primenu Finance okruženja potrebna je važeća Azure pretplata koja će se naplaćivati po okruženju. Možete da koristite postojeću pretplatu u svojim organizacijama ili da koristite [Azure probnu verziju](https://azure.microsoft.com/en-us/free/) da biste započeli. CDS okruženje će biti besplatno za ograničen period od 30 dana.

## <a name="subscribe"></a>Pretplati se

Kada vaš [zahtev za pregled](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) bude odobren, dobićete tri ponude od kompanije Microsoft e-poštom. Ove ponude vam omogućavaju da primenite verziju za pregled usluge Project Operations:

- Dynamics 365 Project Operations (CRM) – probna verzija za pregled
- Office 365 Project Operations – Probna verzija za pregled
- Dynamics 365 Finance – Probna verzija za pregled

> [!IMPORTANT]
> Samo jedna osoba, administrator zakupca, u organizaciji treba da izvršava ovaj zadatak. Ako niste pretplatnik na ovo izdanje, sačekajte dok se vaša organizacija ne registruje i ne primite svoje korisničke akreditive.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) – probna verzija za pregled 

Pre nego što započnete, uverite se da ste prijavljeni u pregledač sa korisničkim poslovnim nalogom u zakupcu gde želite pregled usluge Project Operations.

1. Iskoristite prvi kôd ponude, **Dynamics 365 Project Operations (CRM) – pregled probne verzije** tako što ćete ga nalepiti u URL pregledača.

![Iskoristite ponudu](./media/16RedeemFirstOfferNew.png)

2. Potvrdite porudžbinu.

![Potvrdite porudžbinu](./media/17ConfirmOrderNew.png)

Videćete da je ponuda za potvrdu uspešno iskorišćena.

![Potvrda](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations – Probna verzija za pregled

Ponovite iste korake kao kod prve šifre ponude. Obavezno dodajte drugu šifru ponude koristeći isti korisnički nalog koji je korišćen sa prvom šifrom ponude.

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance probna verzija za pregled

Ponovite iste korake sa poslednjom ponudom iz e-poruke dobrodošlice.

## <a name="assign-licenses"></a>Dodeljivanje licenci

> [!IMPORTANT]
> Trebaće vam administrativni pristup Microsoft 365 portalu vaše organizacije da biste izvršili sledeće korake.

1. Idite u [Microsoft 365 centar administracije](https://portal.office.com/) da dodelite licence svojim korisnicima.

![Početna stranica centra administracije](./media/14AdminPortal.png)

2. Na stranici **Aktivni korisnici**, izaberite korisnike kojima želite da dodelite licencu.

![Dodeljivanje licenci](./media/15AssignLicenses.png)

3. Proverite da li su licence za **Dynamics 365 Project Operations (CRM) verzija za pregled** i **Office 365 Project Operations – verzija za pregled** izabranae i izaberite **Sačuvaj promene**.

> [!NOTE]
> Ponudu za probnu verziju usluge Finance ne treba dodeliti korisniku.

## <a name="start-a-new-project-in-lcs"></a>Započnite novi projekat u LCS

Napravite novi LCS projekat kako je opisano u temi [Započnite novi projekat u LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Dodajte Azure pretplatu u LCS projekat

Da biste dovršili ovaj zadatak, sledite korake u temi [Dodavanje Azure pretplate u LCS projekat](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Primenite Finance demo okruženje sa uslugom Project Operations za scenarije resursa / bez zaliha

Sledite smernice u temi [Obezbeđenje novog okruženja](resource-provision-new-environment.md) da biste završili primenu. Koristite tip primene [demo okruženje](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) za pregled. 

## <a name="install-cds-setup-and-configuration-data"></a>Instalirajte podatke o podešavanju i konfiguraciji CDS

Instalirajte podatke o podešavanju i konfiguraciji CDS kako je opisano u temi [Podesite i primenite podatke o konfiguraciji u usluzi Common Data Service](resource-apply-pro-setup-config-data.md).
Dovršite ovaj korak tek nakon što se primeni demo okruženje usluge Finance i demo podaci u FO budu spremni.


[!INCLUDE[footer-include](../includes/footer-banner.md)]