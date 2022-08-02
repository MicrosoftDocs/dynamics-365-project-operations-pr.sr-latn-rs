---
title: Prijavite se za probnu verziju aplikacije Project Operations
description: Ovaj članak pruža informacije o primeni probne verzije programa Dynamics 365 Project Operations.
author: ruhercul
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 6a6986cfd6c01d1c22d37a10c8d824730fad2e9e
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029317"
---
# <a name="sign-up-for-project-operations-trials"></a>Prijavite se za probnu verziju aplikacije Project Operations 

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/nepostojanju zaliha, jednostavna primena – od pogodbe do profakture, Project Operations za scenarije zasnovane na zalihama/proizvodnji_ 



Ovaj članak sadrži objašnjenja o tome kako da se pretplatite na ponudu partnera za pregled i primenite Dynamics 365 Project Operations okruženje.

Uz novu probnu verziju aplikacije Project Operations, možete automatski primeniti bilo koji od tri podržana scenarija primene popunjavanjem upitnika koji preporučuje najbolji pristup primene. Ovaj članak pruža informacije o tome kako da:

- Iskoristite probnu ponudu.
- Pokrenete obezbeđivanje.
- Konfigurišete dvostruko upisivanje.
- Saznate više o aplikaciji Project Operations. 

Sledeća tabela prikazuje detalje nove probne ponude.

| **Stavka ponude**               | **Detalji**                                  |
|------------------------------|----------------------------------------------|
| Tip ponude                   | Ovaj tip ponude je vodeći za administratore, pa je za iskorišćavanje potreban administrator zakupca. |
| Upotreba ponude                    | Jednom po zakupcu                          |
| Trajanje ponude               | 30 kalendarskih dana                             |
| Iskorišćavanja po zakupcu       | 1                                            |
| Ekstenzija                    | 1 produžetak, 30 kalendarskih dana               |
| Broj probnih okruženja | 3                                            |


## <a name="admin-trial-details"></a>Detalji probnoj verziji za administratora
U sledećoj tabeli navedeni su detalji probne verzije i načina na koji se oni primenjuju na svaki tip primene.

| **Stavka**                      | **Jednostavna**                                     | **Materijali koji nisu na zalihama** | **Materijali na zalihama** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| Podaci o podešavanju su dati           | Da                                          | Da                       | Da (USSI)            |
| Transakcioni podaci            | No                                           | No                        | No                    |
| Vreme obezbeđivanja u minutima  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>Preduslovi
Da biste primenili probnu verziju aplikacije Dynamics 365 Project Operations, neophodno je ispuniti sledeće preduslove.

- Registrujte se za [Dynamics 365 Project Operations – probnu verziju](https://www.aka.ms/try-po).
- Korisnik koji primeni verziju za pregled mora da ima globalna administratorska prava u Azure zakupcu.

> [!IMPORTANT]
> Samo jedna osoba u organizaciji, administrator zakupca, treba da izvrši ovaj zadatak. Ako niste pretplatnik na ovo izdanje, sačekajte dok se vaša organizacija ne registruje i ne primite svoje korisničke akreditive.

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations – probna verzija za pregled 

Pre nego što započnete, prijavite se u pregledaču pomoću korisničkog radnog naloga u zakupcu na kom želite da instalirate verziju za pregled aplikacije Project Operations.

1. Iskoristite prvi kôd ponude, **Dynamics 365 Project Operations – pregled probne verzije** tako što ćete ga nalepiti u URL pregledača.

    ![Iskoristite ponudu](./media/16RedeemFirstOfferNew.png)

2. Potvrdite porudžbinu.

    ![Potvrdite porudžbinu](./media/17ConfirmOrderNew.png)

  Videćete potvrdu da je ponuda uspešno iskorišćena.

   ![Potvrda](./media/18OrderConfirmationNew.png)

  Bićete preusmereni na [Power Platform centar administracije](https://admin.powerplatform.microsoft.com/projectoperationstrial).

## <a name="questionnaire-and-provisioning"></a>Upitnik i obezbeđivanje

1.  Idite u [Power Platform centar administracije](https://admin.powerplatform.com/projectoperationstrial) i dovršite upitnik.  
2.  Pregledajte preporučeni tip primene i izaberite **Započni podešavanje** za pokretanje obezbeđivanja.
3.  Pregledajte uslove i odredbe, a zatim izaberite **Pokreni**.

   Nakon pokretanja obezbeđivanja, bićete preusmereni na listu okruženja u Power Platform centru administracije. Dok je obezbeđivanje u toku, status vašeg okruženja je **PreparingInstance**.
 
  Kada se obezbeđivanje dovrši, status vašeg okruženja je **Spremno**. Obezbeđivanje okruženja uključuje primenu demo podataka.
 
4.  Izaberite odgovarajuće Microsoft Dataverse URL adrese i URL adrese aplikacija za finansije i operacije da biste proverili valjanost primene.

## <a name="configuring-dual-write"></a>Konfigurisanje dvostrukog upisivanja
- Da biste konfigurisali bezbednosne uloge za dvostruko pisanje, pogledajte ažuriranje [bezbednosnih postavki za operacije projekta u programu Dataverse](resource-provision-new-environment.md#update-security-settings-on-project-operations-on-dataverse).
- Da biste pristupili konfiguraciji dvostrukog upisivača, dođite do instance finansiranja i operacija, a zatim se krećite **do dualnog pisanja** > **upravljanja podacima**.
- Da biste konfigurisali mape sa dva pisanja, pogledajte mape [dvostrukog pisanja "Pokreni operacije projekta"](resource-provision-new-environment.md#run-project-operations-dual-write-maps).

## <a name="assign-licenses"></a>Dodela licenci

Trebaće vam administrativni pristup Microsoft 365 portalu vaše organizacije da biste izvršili sledeće korake.

1. Idite u [Microsoft 365 administrativni centar](https://portal.office.com/) da biste dodelili licence korisnicima.

   ![Početna stranica centra administracije](./media/14AdminPortal.png)

2. Na stranici **Aktivni korisnici**, izaberite korisnike kojima želite da dodelite licencu.

   ![Dodeljivanje licenci](./media/15AssignLicenses.png)

3. Proverite da li je izabrana licenca za **Dynamics 365 Project Operations verziju za pregled**, pa izaberite **Sačuvaj promene**.

## <a name="additional-resources"></a>Dodatni resursi

Sledeći resursi pružaju korisne smernice dok započinjete svoje putovanje sa aplikacijom Project Operations:

- [Video serija – pregled aplikacije Project Operations, sadrži detaljne analize i plan](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [Određivanje vrste primene](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Najčešća pitanja

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>Šta ako zahtevam ALM ili ELM za okruženje aplikacija za finansije i operacije?

- Za partnere kojima su potrebne pune mogućnosti upravljanja životnim ciklusom okruženja, pogledajte [Zahtev za licencu za Sandbox partnera](https://experience.dynamics.com/requestlicense) da biste pregledali novu ponudu partnera. 
- Za partnere koji traže više informacija o pravima interne upotrebe, pogledajte [Pogodnosti oblaka i softvera za prava interne upotrebe (microsoft.com](https://partner.microsoft.com/membership/internal-use-software).

### <a name="can-i-extend-my-trial-beyond-30-days"></a>Mogu li produžiti probni period duže od 30 dana?
Da biste produžili probni period, dovršite sledeće korake.

1. U Administrativnom **Microsoft 365 centru idite** na **naplatu** > **Vaši proizvodi**.
2. Izaberite **Dynamics 365 Project Operations (CE) – Probna verzija za pregled**.
3. U odeljku **Datum isteka**, izaberite **Produži datum**.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>Mogu li nadograditi sa jednostavne implementacije na implementaciju scenarija zasnovanog na resursima/materijalima koji nisu na zalihama?
Trenutno ne postoji podrška za nadogradnju okruženja iz jednostavnog na primenu materijala koji nisu na zalihama.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Mogu li pristupiti usluzi Lifecycle Services (LCS) za svoja finansijska okruženja?  
Ne. Za ove probne verzije, primenom se upravlja putem Power Platform centra administracije. Pristup finansijskom okruženju je ograničen.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>Mogu li instalirati probnu verziju u postojećem okruženju?
Ako imate postojeće okruženje, biće vam dozvoljeno da instalirate jednostavnu implementaciju u postojećem prodajnom Dataverse okruženju iz Power Platform centra administracije.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
