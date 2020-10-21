---
title: Prijavljivanje za pretplate na verziju za pregled usluge Project Operations za scenarije resursa / bez zaliha
description: Ova tema pruža informacije o načinu pretplate i primene usluge Project Operations za scenarije zasnovane na resursima / bez zaliha.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949052"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Prijavljivanje za pretplate na verziju za pregled usluge Project Operations za scenarije resursa / bez zaliha

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ova tema objašnjava kako se pretplatiti na verziju za pregled / partnersku ponudu i primenu Project Operations okruženja za scenarije zasnovane na resursima / bez zaliha.

## <a name="prerequisites"></a>Preduslovi

- Dobićete e-poruku sa pozivom da učestvujete u pregledu. Možete zatražiti verziju za pregled na [Project Operations veb-lokaciji](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Korisnik koji primeni verziju za pregled mora da ima globalna administratorska prava u Azure zakupcu.
- Za primenu Finance okruženja potrebna je važeća Azure pretplata koja će se naplaćivati po okruženju. Možete da koristite postojeću pretplatu u svojim organizacijama ili da koristite [Azure probnu verziju](https://azure.microsoft.com/en-us/free/) da biste započeli. CDS okruženje će biti besplatno za ograničen period od 30 dana.

## <a name="subscribe"></a>Pretplati se

Kada vaš [zahtev za pregled](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) bude odobren, dobićete dve ponude od kompanije Microsoft e-poštom. Ove ponude vam omogućavaju da primenite verziju za pregled usluge Project Operations:

- Dynamics 365 Project Operations – Probna verzija za pregled
- Dynamics 365 for Finance and Operations probna verzija za pregled.

> [!IMPORTANT]
> Samo jedna osoba, administrator zakupca, u organizaciji treba da izvršava ovaj zadatak. Ako niste pretplatnik na ovo izdanje, sačekajte dok se vaša organizacija ne registruje i ne primite svoje korisničke akreditive.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – Probna verzija za pregled

1. Iskoristite prvu ponudu, **Probna verzija usluge Dynamics 365 Project Operations**, sa URL-om navedenim u e-poruci dobrodošlice.

![Prva ponuda](./media/1FirstOffer.png)

2. Potvrdite da ste prijavljeni kao korisnik koji pripada organizaciji koja će se pretplatiti na uslugu.
3. Nastavite sa iskorišćavanjem ponude. 
4. Izaberite **Da, dodaj na moj nalog**.

![Iskoristite ponudu](./media/2RedeemFirstOffer.png)

![Potvrdite ponudu](./media/3ConfirmFirstOffer.png)

![Ponuda je iskorišćena](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance probna verzija za pregled

Ponovite iste korake sa drugom ponudom iz e-poruke dobrodošlice.

## <a name="assign-licenses"></a>Dodeljivanje licenci

> [!IMPORTANT]
> Trebaće vam administrativni pristup Office 365 portalu vaše organizacije da biste izvršili sledeće korake.

1. Idite u [Microsoft 365 centar administracije](https://portal.office.com/) da dodelite licence svojim korisnicima.

![Office portal za administraciju](./media/5OfficeAdminPortal.png)

2. Na stranici **Aktivni korisnici**, izaberite korisnike kojima želite da dodelite licencu.

![Dodeljivanje licenci](./media/6AssignLicenses.png)

3. Proverite da li je izabrana Project Operations licenca i izaberite **Sačuvaj promene**. 

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

