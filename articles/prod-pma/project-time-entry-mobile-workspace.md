---
title: Mobilni radni prostor za stavku vremena projekta
description: Ova tema pruža informacije o mobilnom radnom prostoru stavke vremena projekta. Ovaj radni prostor omogućava korisnicima da unesu u sačuvaju vreme u projektu koristeći svoj mobilni uređaj.
author: Yowelle
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 7eae471cf42f02e64844a4682cc8ed02cbb14c34
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288891"
---
# <a name="project-time-entry-mobile-workspace"></a>Mobilni radni prostor za stavku vremena projekta

[!include [banner](../includes/banner.md)]

Ova tema pruža informacije o mobilnom radnom prostoru **stavke vremena projekta**. Ovaj radni prostor omogućava korisnicima da unesu u sačuvaju vreme u projektu koristeći svoj mobilni uređaj.

Ovaj mobilni radni prostor je namenjen za upotrebu zajedno sa Dynamics 365 Unified Ops aplikacijom za mobilne uređaje. 

## <a name="overview"></a>Pregled
Kao deo njihovog svakodnevnog rada, resursi projekta su često na licu mesta ili putuju. Mobilni radni prostor **Stavka vremena projekta** omogućava korisnicima da unose svoje naplativo ili nenaplativo vreme u odnosu na projekat na mobilnom uređaju po svom izboru. Stoga projektni resursi mogu evidentirati vremenske unose bilo kada i bilo gde. Takođe mogu da vide stavke vremena koje su već zabeležene. 

Konkretno, u mobilnom radnom prostoru **Stavka vremena projekta** korisnici mogu da obavljaju sledeće zadatke:

-   Za bilo koji izabrani datum, unesite broj sati koje ste potrošili na određeni zadatak.
-   Pretražite prema nazivu projekta ili klijentu da biste pronašli projekat za koji ćete uneti vreme.
-   Navedite kategoriju i aktivnost za vreme koje ste proveli.
-   Zabeležite vreme kao naplativo ili nenaplativo za projekat.
-   Opcionalno unesite spoljne i interne komentare.

## <a name="prerequisites"></a>Preduslovi
Preduslovi se razlikuju, na osnovu verzije sistema Microsoft Dynamics 365 koji je primenjen za vašu organizaciju.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Preduslovi ako koristite Dynamics 365 Finance
Ako je Finance primenjen u vašoj organizaciji, administrator sistema mora objaviti mobilni radni prostor **Stavka vremena projekta**. Za uputstva pogledajte [Objavljivanje mobilnog radnog prostora](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Preduslovi ako koristite verziju 1611 sa ispravkom 3 platforme ili novijom
Ako je za vašu organizaciju primenjena verzija 1611 sa ispravkom 3 platforme ili novijom, administrator sistema mora da ispuni sledeće preduslove. 

<table>
<thead>
<tr class="header">
<th>Preduslov</th>
<th>Uloga</th>
<th>Opis</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>Primena KB 4018050.</td>
<td>Administrator sistema</td>
<td>KB 4018050 je hitna ispravka za X++ ispravku ili metapodatke koja sadrži mobilni radni prostor <strong>Stavka vremena projekta</strong>. Da bi primenio KB 4018050, administrator sistema mora slediti ove korake.
<ol>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Preuzmite hitnu ispravku za metapodatke iz usluge Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Instalirajte hitnu ispravku za metapodatke</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Kreirajte paket koji se može primeniti</a> koji sadrži modele <strong>ApplicationSuite</strong> i <strong>ProjectMobile</strong>, a zatim otpremni paket koji se može primeniti na LCS.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Primenite paket koji se može primeniti</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Objavite mobilni radni prostor za <strong>stavku vremena projekta</strong>.</td>
<td>Administrator sistema</td>
<td>Pogledajte <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Objavljivanje mobilnog radnog prostora</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Preuzmite i instalirajte aplikaciju za mobilne uređaje

Preuzmite i instalirajte Finance and Operations aplikaciju za mobilne uređaje:

-   [Za Android telefone](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Za iPhone uređaje](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Prijavite se u aplikaciju za mobilne uređaje
1.  Pokrenite aplikaciju na mobilnom uređaju.
2.  Unesite svoj Dynamics 365 URL.
3.  Kada se prvi put prijavite, od vas će se zatražiti korisničko ime i lozinka. Unesite akreditive.
4.  Kada se prijavite, prikazuju se dostupni radni prostori za vašu kompaniju. Imajte na umu da ako administrator sistema kasnije objavi novi radni prostor, moraćete da osvežite listu mobilnih radnih prostora.

[![Povucite da osvežite](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Unesite vreme pomoću mobilnog radnog prostora za stavku vremena projekta
1.  Na mobilnom uređaju, izaberite radni prostor **Stavka vremena projekta**.
2.  Izaberite **Stavka vremena**. Prikazani su datumi kalendara za tekuću nedelju.
3.  Za izabrani datum izaberite **Radnje** &gt; **Nova stavka**.
4.  Unesite broj sati za evidentiranje.
5.  Izaberite projekat za stavku vremena. Lista prikazuje projekte koji su učitani u vašu aplikaciju za korišćenje van mreže. Podrazumevano se učitava 50 stavki, ali programer može promeniti ovaj broj. Za više informacija pogledajte članak [Mobilna platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
6.  Ako vaš projekat nije na listi, izaberite **Pretraga**. Pretražujte po imenu ili pređite na pretragu po nazivu projekta ili klijentu.
7.  Izaberite kategoriju. Lista prikazuje kategorije koje su učitane u vašu aplikaciju za korišćenje van mreže. Podrazumevano se učitava 50 stavki, ali programer može promeniti ovaj broj. Za više informacija pogledajte članak [Mobilna platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
8.  Ako vaša kategorija nije na listi, izaberite **Pretraga**. Pretražujte po kategoriji ili se prebacite na pretragu po nazivu kategorije.
9.  Izaberite aktivnost. Lista prikazuje aktivnosti koje su učitane u vašu aplikaciju za korišćenje van mreže. Podrazumevano se učitava 50 stavki, ali programer može promeniti ovaj broj. Za više informacija pogledajte članak [Mobilna platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
10. Ako vaša aktivnost nije na listi, izaberite **Pretraga**. Pretražujte prema broju aktivnosti ili se prebacite na pretragu po nameni.

11. Izaberite svojstvo reda.
12. Opcionalno: Unesite sve spoljne i interne komentare.
13. Izaberite **Gotovo**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]