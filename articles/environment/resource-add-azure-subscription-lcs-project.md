---
title: Dodajte Azure pretplatu u LCS projekat
description: Ova tema pruža informacije o tome kako da povežete svoju Azure pretplatu sa LCS projektom.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e4502c1dec3bfeed083186b2d053549fefc9339609946c8da919b46e0e56cc79
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986688"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a>Dodajte Azure pretplatu u LCS projekat

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Okruženja u hostu u oblaku moraju se primeniti pomoću postojeće Azure pretplate. Ova tema objašnjava kako da povežete svoju postojeću Azure pretplatu sa LCS projektom. 

## <a name="grant-admin-consent"></a>Dajte pristanak administratora

1. U vašem LCS projektu, u odeljku **Okruženja**, izaberite **Microsoft Azure podešavanja**.

![Podešavanja programa Microsoft Azure.](./media/1MicrosoftAzureSettings.png)

2. Na stranici **Podešavanja projekta**, na kartici **Azure konektori**, izaberite **Odobri**. To omogućava da se okruženja primene na ovaj projekat.

![Azure konektori.](./media/2AzureConnectors.png)

3. Ponovo izaberite **Odobri** da biste pružili pristanak administratora.

![Dajte pristanak administratora.](./media/3GrantAdminConsent.png)

4. Prihvatite zahtev za dozvole.

![Prihvatite zahtev za dozvole.](./media/4AcceptPermissionRequest.png)

Ovlašćenje je sada završeno. 

![Odobrenje je uspešno.](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Omogućite pristup usluge Dynamics Deployment Services vašoj Azure pretplati

1. Idite na [Microsoft Azure obračun](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) i izaberite svoju pretplatu. Usluga Dynamics Deployment Services treba da pristupi ovoj pretplati da bi mogla da primeni okruženja.

![Detalji Azure pretplate.](./media/6AzureSubscription.png)

2. Izaberite **Kontrola pristupa (IAM)** u oknu za navigaciju, a zatim izaberite **Dodajte dodeljivanje uloga**.
3. U klizaču sa desne strane izaberite **Uloga saradnika** i na priloženoj listi pronađite i izaberite **Dynamics Deployment Services**. 
4. Izaberite stavku **Sačuvaj**.

![Pristup pretplati.](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Dodavanje konektora za pretplatu u LCS projekat

1. U vašem LCS projektu, na stranici **Microsoft Azure podešavanja** izaberite **Dodaj** da biste dodali novi konektor.
2. Unesite svoj ID Azure pretplate. ID Azure pretplate možete pronaći u [Azure portalu](https://ms.portal.azure.com/), u odeljku  **Podešavanja**  u donjem levom uglu ekrana.
3. U polju **Konfiguriši da se koristi Azure Resource Manager**, izaberite **Da**.
4. Uverite se da se Azure domen zakupca AAD pretplate podudara sa Azure pretplatom u vlasništvu domena koju koristite, pa izaberite **Sledeći**.
5. Na ekranu **Microsoft Azure podešavanje**, izaberite **Sledeći** za potvrdu. Ako na ovom ekranu dobijete grešku, vratite se u odeljak [Omogućite pristup usluzi Dynamics Deployment Services u Azure pretplatu](#provide) u ovoj temi i uverite se da ste završili sve korake.
6. Preuzmite Azure certifikat za upravljanje u lokalnu fasciklu na računaru. Zamolite administratora pretplate za Azure da otpremi sertifikat na portal za upravljanje uslugom Azure tako što će odabrati pretplatu i otići na **Podešavanja** > **Sertifikati o upravljanju**. Ovaj sertifikat omogućava LCS-u da u vaše ime komunicira sa uslugom Azure. Ovaj korak možete preskočiti ako vaš korisnik ima pristup pretplati.
7. Izaberite **Sledeće**.
8. Izaberite Azure region za primenu i izaberite centar podataka koji je blizu mesta gde planirate da koristite ovaj sistem.
9.  Izaberite **Poveži se**.

Uspešno ste povezali svoju Azure pretplatu. Sada možete da primenite Dynamics 365 Finance okruženja hostovana u oblaku.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
