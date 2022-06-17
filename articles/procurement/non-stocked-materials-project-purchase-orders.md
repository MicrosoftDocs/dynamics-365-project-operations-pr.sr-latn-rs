---
title: Naručivanje materijala koji nisu na zalihama za projekat pomoću narudžbenica projekata
description: Ovaj članak sadrži objašnjenja o tome kako možete da poručite materijale koji nisu snabdeveni za projekat pomoću izlaznih porudžbina projekta.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fe24faa143869af2396f3b0f28aae31417cadda7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929829"
---
# <a name="order-procurement-categories-or-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Naručite kategorije nabavki ili materijale koji nisu snabdeveni za projekat koristeći izlazne porudžbine projekta

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Odeljenje za nabavke u vašoj organizaciji moglo bi da koristi [narudžbenice](/dynamics365/supply-chain/procurement/purchase-order-overview) za praćenje narudžbina roba i usluga. Izlazne porudžbine za kategorije nabavki ili materijale koji nisu na berzi mogu se pripisati projektu. Fakturisanje ovih narudžbenica beleži troškove za projekat.

## <a name="prerequisites"></a>Preduslovi
Dovršite sledeće korake da biste omogućili funkcionalnost narudžbenica za projekat.

1. U Dynamics 365 Finance, idite na radni **prostor za upravljanje** funkcijama.
2. Na listi funkcija pronađite i izaberite funkciju **Omogući narudžbenice za projekte u usluzi Project Operations za scenarije zasnovane na resursima/bez zaliha**.
3. Izaberite dugme **Omogući**.
4. Konfigurišite zalihe materijala i zalihe dobavljača na čekanju kao što je opisano u članku [Konfigurisanje materijala bez zaliha i fakture dobavljača na čekanju](configure-materials-nonstocked.md).
5. Konfigurišite kategorije nabavki kao što je opisano u kategorijama [korišćenja nabavki sa izlaznim porudžbinama projekta i neobrađenim fakturama dobavljača](configure-procurement-categories.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Napravite narudžbenicu za projekat sa liste narudžbenica za projekte

1. U odeljku „Finansije“ idite na **Upravljanje projektima i računovodstvo** > **Projekti** > **Svi projekti** i izaberite projekat.
2. Na oknu sa radnjama, na kartici **Upravljanje**, u grupi **Novo** izaberite **Zadatak stavke** > **Narudžbina**.
3. Na stranici **Kreiranje narudžbenice** izaberite dobavljača za kojeg želite da podesite narudžbenicu, unesite ostale podatke prema potrebi, a zatim izaberite **U redu**.
4. Na stranici **Narudžbenica** u mreži **Stavke narudžbenice** izaberite **Dodaj stavku**.
5. Unesite broj artikla ili kategoriju nabavke, količinu, jedinicu, jediničnu cenu i druge informacije na odgovarajući način.

    > [!NOTE]
    > Samo kategorije nabavki, artikli koji nisu snabdeveni i usluge mogu se koristiti sa izlaznim porudžbinama projekta. Snabdevene stavke nisu podržane.

6. Nastavite da dodajete artikle ili kategorije nabavki po potrebi i potvrdite izlaznu porudžbinu.

    Prijem robe i usluga može se evidentirati kreiranjem i objavljivanjem priznanice za proizvod.

    > [!NOTE]
    > Priznanice za proizvode ne evidentiraju se u aktuelnim podacima za projekat u usluzi Microsoft Dataverse i ne utiču na podknjigu projekta.

    Nakon što dobavljač pošalje fakturu za artikle i usluge na narudžbenici, odeljenje za nabavku može da generiše fakturu za narudžbenicu tako što će otići na odeljak **Faktura** > **Generiši** > **Faktura** na oknu sa radnjama. Za više informacija o fakturama dobavljača na čekanju pogledajte članak [Kupovina materijala koji nisu na zalihama koristeći fakturu dobavljača na čekanju](pending-vendor-invoices.md).
