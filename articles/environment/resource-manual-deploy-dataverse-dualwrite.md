---
title: Ručno raspoređivanje Project Operations Dataverse aplikacije sa podrškom za dvostruko upisivanje
description: Ova tema objašnjava kako da ručno primenite Project Operations Dataverse aplikaciju tako da podržava dvostruko upisivanje.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 06325a9a9f9084d1f506f2493c32565fe7b7c52ae6fe22c81339b9c1d632e688
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986463"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Ručno raspoređivanje Project Operations Dataverse aplikacije sa podrškom za dvostruko upisivanje

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ova tema objašnjava kako da ručno primenite aplikaciju Microsoft Dynamics 365 Project Operations na platformi Microsoft Dataverse tako da podržava dvostruko upisivanje. Project Operations otkriva konfiguraciju okruženja i dodaje dodatnu podršku za dvostruko upisivanje ako su ispunjeni preduslovi.

Tokom primene preko usluge Microsoft Dynamics Lifecycle Services (LCS), ako ste sledili uputstva u ovoj temi, možete preskočiti primenu Microsoft Power Platform integracije (ranije poznate kao Common Data Service okruženje).

Proces primene usluge Project Operations na platformi Dataverse tako da podržava dvostruko upisivanje ima četiri glavna koraka:

1. [Kreiranje novog okruženja na platformi Dataverse koje podržava dvostruko upisivanje](#create).
2. [Dodavanje preduslova za dvostruko upisivanje u okruženje](#prerequisites).
3. [Dodavanje aplikacije Project Operations Dataverse](#dataverse).
4. [Povezivanje okruženja](#link).

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>Kreiranje novog okruženja na platformi Dataverse koje podržava dvostruko upisivanje

Da biste dovršili ovu proceduru, morate se prijaviti kao administrator.

1. Otvorite [Power Platform centar administracije](https://admin.powerplatform.com) i prijavite se kao administrator.
2. Kreirajte novo okruženje i imenujte ga.
3. Izaberite tip okruženja. Ako ste se prijavili za ponudu probne verzije, izaberite **Probna verzija (zasnovana na pretplati)**.
4. Potvrdite region primene.
5. Omogućite opciju **Kreiranje baze podataka za ovo okruženje**. 
6. Potvrdite jezik, a zatim potvrdite da se valuta podudara sa valutom za vaše Finance and Operations aplikacije.
7. Omogućite **Dynamics 365 aplikacije** i potvrdite da je polje **Automatski primeni ove aplikacije** podešeno na **Nijedna**.
8. Dodajte bezbednosnu grupu ako je potrebna bezbednosna grupa.
9. Izaberite **Sačuvaj** da biste kreirali okruženje.
10. Sačekajte dok se primena ne završi i okruženje ne dostigne status **Spremno**.

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>Dodavanje preduslova za dvostruko upisivanje u okruženje

Podrška za dvostruko upisivanje uključuje dodatna polja koja se dodaju ključnim entitetima, kao što je entitet **Preduzeće**. Ako dodajete podršku za dvostruko upisivanje u postojeće okruženje, možda ćete morati da ažurirate podatke da biste ga omogućili. Za informacije o načinu pokretanja podataka, pogledajte članak [Podaci za pokretanje preduzeća](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data). Za više informacija o dvostrukom upisivanju, pogledajte članak [Sistemski zahtevi za dvostruko upisivanje](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).

Dovršite ovaj postupak da biste dodali preduslove za dvostruko upisivanje u svoje okruženje.

1. Otvorite okruženje koje ste upravo kreirali, a zatim idite u **Resurs** \> **Dynamics 365 aplikacije**.
2. Izaberite **Osnovno rešenje sa dvostrukim upisivanjem** na listi aplikacija i instalirajte ga.
3. Sačekajte dok se instalacija ne završi. Zatim izaberite **Rešenje orkestracije aplikacije sa dvostrukim upisivanjem** na listi aplikacija i instalirajte ga.

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>Dodavanje Project Operations Dataverse aplikacije

Ovu proceduru možete dovršiti samo ako ste završili prethodne procedure pre nego što ste instalirali Project Operations. Tokom instalacije, sistem analizira konfiguraciju okruženja i dodaje podršku za dvostruko upisivanje ako je potrebno.

1. Otvorite okruženje koje ste ranije kreirali, a zatim idite u **Resurs** \> **Dynamics 365 aplikacije**.
2. Izaberite **Microsoft Dynamics 365 Project Operations** na listi aplikacija i instalirajte je.

## <a name="link-your-environments"></a><a name="link"></a>Povezivanje okruženja

Kada se Dataverse okruženje primeni, možete podesiti vezu u svojim Finance and Operations aplikacijama. Sledite korake u članku [Korišćenje čarobnjaka za dvostruko upisivanje radi povezivanja okruženja](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).
