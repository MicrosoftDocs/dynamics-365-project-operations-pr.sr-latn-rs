---
title: Naručivanje materijala koji nisu na zalihama za projekat pomoću narudžbenica projekata
description: Ova tema objašnjava kako možete da naručite materijale koji nisu na zalihama za projekat pomoću narudžbenica projekata.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 2aa8fb94e2f9cbf91182f3f169339284d3eb9f44
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612720"
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
