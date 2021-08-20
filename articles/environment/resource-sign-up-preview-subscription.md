---
title: Prijavljivanje za pretplate na verziju za pregled usluge Project Operations za scenarije resursa / bez zaliha
description: Ova tema pruža informacije o načinu pretplate i primene usluge Project Operations za scenarije zasnovane na resursima / bez zaliha.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 75ee31e67018fe2a7655d8a8f11e40b433a9a5db6f8f2addac27844f18fffe8d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007883"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Prijavljivanje za pretplate na verziju za pregled usluge Project Operations za scenarije resursa / bez zaliha

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Ova tema objašnjava kako da se pretplatite na ponudu probne verzije i primeniti Project Operations okruženje za scenarije zasnovane na resursima / bez zaliha.

## <a name="prerequisites"></a>Preduslovi
- Korisnik koji primeni verziju za pregled mora da ima globalna administratorska prava u Azure zakupcu. Zakupca možete kreirati tokom prvog iskorišćavanja ponude. 
- Za primenu Finance okruženja potrebna je važeća Azure pretplata koja će se naplaćivati po okruženju. Možete da koristite postojeću pretplatu u svojim organizacijama ili da koristite [Azure probnu verziju](https://azure.microsoft.com/en-us/free/) da biste započeli. CDS okruženje će biti besplatno za ograničen period od 30 dana.

> [!IMPORTANT]
> Samo jedna osoba, administrator zakupca, u organizaciji treba da izvršava ovaj zadatak. Ako niste pretplatnik na ovo izdanje, sačekajte dok se vaša organizacija ne registruje i ne primite svoje korisničke akreditive.
> 
> Probne verzije se koriste jednokratno u zakupcu. Probnu verziju možete pokrenuti samo jednom. Preporučujemo vam da kreirate novog zakupca u svrhu probne verzije.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE) – Probna verzija za pregled 

Pre nego što započnete, uverite se da ste prijavljeni u pregledač sa korisničkim poslovnim nalogom u zakupcu gde želite pregled usluge Project Operations.

1. Iskoristite prvu šifru ponude, **Dynamics 365 Project Operations** ovde [Project Operations probna verzija](https://aka.ms/try-po).
2. Potvrdite porudžbinu.

  Videćete da je ponuda za potvrdu uspešno iskorišćena.

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance probna verzija za pregled

Idite na [probnu verziju za pregled usluge Dynamics 365 for Finance](https://aka.ms/trypoche) i ponovite korake iz prethodnog odeljka sa ponudom, Prijavite se za okruženje koje se hostuje u oblaku.  

## <a name="assign-licenses"></a>Dodeljivanje licenci

> [!IMPORTANT]
> Trebaće vam administrativni pristup Microsoft 365 portalu vaše organizacije da biste izvršili sledeće korake.

1. Idite u [Microsoft 365 centar administracije](https://portal.office.com/) da dodelite licence svojim korisnicima.

2. Na stranici **Aktivni korisnici**, izaberite korisnike kojima želite da dodelite licencu.

3. Proverite da li je izabrana licenca **Dynamics 365 Project Operations**, pa izaberite **Sačuvaj promene**.

> [!NOTE]
> Ponudu za probnu verziju usluge Finance ne treba dodeliti korisniku.

## <a name="start-a-new-project-in-lcs"></a>Započnite novi projekat u LCS

Napravite novi LCS projekat kako je opisano u temi [Započnite novi projekat u LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Dodajte Azure pretplatu u LCS projekat

Da biste dovršili ovaj zadatak, sledite korake u temi [Dodavanje Azure pretplate u LCS projekat](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Primenite Finance demo okruženje sa uslugom Project Operations za scenarije resursa / bez zaliha

Sledite smernice u temi [Obezbeđenje novog okruženja](resource-provision-new-environment.md) da biste završili primenu. Koristite tip primene [demo okruženje](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) za pregled. 

## <a name="install-cds-setup-and-configuration-data"></a>Instalirajte podatke o podešavanju i konfiguraciji CDS

Instalirajte podatke o podešavanju i konfiguraciji CDS kako je opisano u temi [Podesite i primenite podatke o konfiguraciji u usluzi Common Data Service](resource-apply-pro-setup-config-data.md).
Dovršite ovaj korak tek nakon što se primeni demo okruženje usluge Finance i demo podaci budu spremni.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
