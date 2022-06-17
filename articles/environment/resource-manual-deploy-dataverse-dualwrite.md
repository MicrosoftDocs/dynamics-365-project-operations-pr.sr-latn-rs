---
title: Ručno raspoređivanje Project Operations Dataverse aplikacije sa podrškom za dvostruko upisivanje
description: Ovaj članak sadrži objašnjenja o tome kako da ručno primenite aplikaciju "Operacije Dataverse projekta" tako da podržava dvostruko pisanje.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: be80ea3956fbf0264c2eeb7a5e30dd50b77e3c78
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912027"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Ručno raspoređivanje Project Operations Dataverse aplikacije sa podrškom za dvostruko upisivanje

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ovaj članak sadrži objašnjenja o tome kako da ručno primenite Dynamics 365 Project Operations Microsoft Microsoft Dataverse tako da podržava dvostruko pisanje. Project Operations otkriva konfiguraciju okruženja i dodaje dodatnu podršku za dvostruko upisivanje ako su ispunjeni preduslovi.

Tokom primene Microsoft Dynamics putem usluga životnog ciklusa (LCS), ako ste sledili uputstva iz ovog članka, možete da preskočite primenu Microsoft Power Platform integracije (ranije poznate kao Common Data Service okruženje).

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
6. Potvrdite jezik, a zatim potvrdite da se valuta podudara sa valutom za aplikacije "Finansije i operacije".
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

Nakon što je Dataverse okruženje raspoređeno, možete da podesite vezu u aplikacijama za finansije i operacije. Sledite korake u članku [Korišćenje čarobnjaka za dvostruko upisivanje radi povezivanja okruženja](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).
