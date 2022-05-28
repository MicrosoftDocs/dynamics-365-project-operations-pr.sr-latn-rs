---
title: Konfigurišite materijale koji nisu na zalihama i fakture dobavljača na čekanju
description: Ova tema objašnjava kako da omogućite materijale koji nisu na zalihama i fakture dobavljača na čekanju.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1b14ab17a317e7082bc9c24709590745a5c48ea8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592985"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>Konfigurišite materijale koji nisu na zalihama i fakture dobavljača na čekanju

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

## <a name="minimum-version-requirement"></a>Minimalan zahtev verzije

Korišćenje materijala koji nisu na zalihama i faktura dobavljača na čekanju za Dynamics 365 Project Operations scenarije bez zaliha/na osnovu resursa zahtevaju sledeće verzije:

Dynamics 365 Dataverse rešenja:

- Project Operations – 4.9.0.221 ili noviji
- Rešenje za orkestraciju dvostrukog pisanja – 2.2.2.23 ili novije

Dynamics 365 Finance:
- 10.0.18 (10.0.793.52) ili noviji. Uverite se da je vaše Finance okruženje aktuelno i da se primenjuju sva ažuriranja kvaliteta kako bi se ispunili minimalni zahtevi za verziju.

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>Pokrenite mape dvostrukog pisanja za neskladištene materijale i integraciju računa dobavljača

Ovaj odeljak pruža informacije o određenim mapama potrebnim za materijal koji nije na zalihama i fakture dobavljača. Proverite da li su neophodne mape navedene u temi [Obezbedite novo okruženje](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) pokrenute u vašem okruženju.

1. Idite na Lifecycle Services (LCS), dođite do LCS projekta i idite na stranicu **Detalji okruženja**.
2. U odeljku Informacije o **Common Data Service okruženju**, izaberite **Veza do usluge CDS za aplikacije**. Kada izaberete vezu, bićete preusmereni na listu entiteta u mapiranjima.
3. Obavezno pokrenite sledeće mape. Ako se ne pokreću, pokrenite ih i pobrinite se da uključite sve povezane mape tabela.

    - CDS je objavio različite proizvode (proizvodi)
    - Prodavci v2 (msdyn_vendors)
    - Project Operations tabela za procene materijala (msdyn_estimatelines)
    - Project Operations entitet izvoza fakture prodavca (msdyn_projectvendorinvoices)
    - Project Operations entitet izvoza reda fakture prodavca (msdyn_projectvendorinvoicelines)
    - Project Operations stvarne vrednosti integracije (msdyn_actuals). Obavezno pokrenite verziju mape 1.0.0.14 ili noviju. Aktivnu verziju mape možete videti u koloni **Verzija** na stranici **Dvostruko upisivanje**. Možete aktivirati novu verziju mape ako izaberete **Verzija tabele mape**, a zatim sačuvajte izabranu verziju.

Ako koristite standardne demo podatke, možda ćete takođe morati da zaustavite i ponovo pokrenete sledeće mape entiteta sa početnom sinhronizacijom:
  - Dani plaćanja CDS V2 (msdyn_paymentdays)
  - Raspored plaćanja (msdyn_paymentschedules)
  - Uslovi plaćanja (msdyn_paymentterms)
  - Grupe dobavljača (msdyn_vendorgroups)
  - Jedinice (uom)

> [!NOTE]
> Početna sinhronizacija za grupe dobavljača i jedinice možda neće uspeti za nekoliko zapisa u postojećem demo skupu podataka. Greške možete zanemariti jer vas one neće sprečiti da koristite demo podatke sa Project Operations.

## <a name="configure-prerequisites-in-dataverse"></a>Konfigurišite preduslove u Dataverse

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>Aktivirajte tok posla da biste kreirali naloge na osnovu entiteta dobavljača

Rešenje za orkestraciju dvostrukog upisivanja pruža [dobavljačima glavnu integraciju](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping). Kao preduslov za ovu funkciju, podaci dobavljača moraju se kreirati u entitetu **Nalozi**. Aktivirajte proces toka posla šablona da biste kreirali dobavljače u tabeli **Nalozi** kako je opisano u [Prebacujte se između dizajna dobavljača](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch).

### <a name="set-products-to-be-created-as-active"></a>Podesite proizvode koji će se kreirati kao aktivni

Materijali van zaliha moraju biti konfigurisani kao **Objavljeni proizvodi** u Finance. Rešenje za orkestraciju dvostrukog upisivanja pruža gotovu [Katalog proizvoda integracija objavljenih proizvoda u Dataverse](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping). Podrazumevano se proizvodi iz Finance sinhronizuju sa Dataverse u statusu radne verzije. Da biste sinhronizovali proizvod u aktivno stanje, tako da se može direktno koristiti u dokumentima o upotrebi materijala ili na fakturama dobavljača na čekanju, idite na **Sistem** > **Administracija** > **Administracija sistema** > **Podešavanja sistema** i na kartici **Prodaja** podesite **Kreirajte proizvode u aktivnom stanju** na **Da**.

## <a name="configure-prerequisites-in-finance"></a>Konfigurišite preduslove u Finance

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>Omogućite taster funkcije za fakture dobavljača na čekanju

Dovršite sledeće korake da biste omogućili funkcionalnost za dodavanje detalja o projektu u redove faktura dobavljača na čekanju.

1. U Finance idite u radni prostor **Upravljanje funkcijama**.
2. Na listi funkcija pronađite funkciju **Omogućite fakture dobavljača na čekanju u Project Operations za resurs/scenarije koji nisu zasnovani na zalihama** i izaberite **Omogući**.

### <a name="define-category-groups-and-project-categories-for-items"></a>Definišite grupe kategorija i kategorije projekata za stavke

Konfigurišite najmanje jednu grupu kategorija za tip transakcije **Stavka** i najmanje jednu kategoriju projekta koja koristi ovu grupu. Za više informacija, pogledajte odeljak [Konfigurisanje kategorija projekata](../project-accounting/configure-project-categories.md#category-groups).

Pregledajte profile troškova i prihoda projekta i konfigurišite podešavanje glavne knjige za transakcije stavki. Za više informacija pogledajte [Konfigurišite računovodstvo za projekte koje treba naplatiti](../project-accounting/configure-accounting-billable-projects.md).

### <a name="set-up-a-write-in-product"></a>Podesite ručno dodat proizvod

U Project Operations možete da zabeležite procene i upotrebu materijala za kataloške proizvode koji su konfigurisani u izdatom katalogu proizvoda i za ručno dodate proizvode. Korišćenje ručno dodatih proizvoda zahteva jedan objavljen proizvod koji je u tu svrhu konfigurisan u Finance. Dovršite sledeće korake za konfigurisanje ručno dodatog proizvoda. Ponovite ove korake u svakom pravnom licu koje koristi Project Operations za scenarije sa resursima/materijalima koji nisu na zalihama.

1. U Finance idite na **Upravljanje informacijama o proizvodu** > **Proizvodi** > **Objavljeni proizvodi** i izaberite **Novo**.
2. U polju **Vrsta proizvoda** izaberite **Stavka** i u polju **Podtip proizvoda** izaberite **Proizvod**.
3. Unesite broj proizvoda (WRITEIN) i naziv proizvoda (ručno dodat proizvod).
4. Izaberite grupu modela stavki. Uverite se da izabrana grupa modela stavki ima polje **Politika zaliha Proizvod na zalihama** postavljeno na **Netačno**.
5. Izaberite vrednosti u poljima **Grupa predmeta**, **Grupa dimenzija skladišta** i **Grupa dimenzija praćenja**. Koristite **Dimenziju skladišta** samo za **Lokaciju**, a u polju **Dimenzije za praćenje** izaberite **Nijedna**.
6. Izaberite vrednosti u poljima **Jedinica zaliha**, **Jedinica kupovine** i **Jedinica prodaje**, a zatim sačuvajte promene.
7. Na kartici **Plan**, postavite podrazumevane postavke redosleda i na kartici **Inventar** postavite podrazumevanu lokaciju i skladište.
8. Idite u **Upravljanje projektima i računovodstvo** > **Podešavanje** > **Parametri upravljanja projektom i računovodstveni parametri** i otvorite **Project Operations u usluzi Dynamics 365 Dataverse**. 
9. Na kartici **Materijali** u polju **Ručno dodat proizvod** izaberite proizvod koji ste kreirali.
10. U vašem Dataverse okruženju, na mapi lokacije otvorite entitet **Proizvodi** i pronađite zapis ručno dodatog proizvoda. 
11. Otvorite detalje o zapisu i podesite status proizvoda na **Povučen**. Ovaj status proizvoda sprečava bilo koga da slučajno koristi ovaj zapis direktno u procenama materijala i dokumentima o upotrebi.

### <a name="set-up-a-procurement-integration-account"></a>Podesite nalog za integraciju nabavki

Nalog za integraciju nabavke koristi se kao nalog za obračun prilikom knjiženja fakture dobavljača na čekanju sa redovima dodeljenim projektu.

Kada sistem knjiži fakturu dobavljača na čekanju, ovaj nalog se koristi za iznos troškova projekta. Podaci o fakturi dobavljača se obrađuju u Dataverse i kreira se odgovarajući stvarni projekat. Informacije iz stvarnog projekta dodaju se u dnevnik Project Operations integracije. Kada objavite dnevnik integracije, iznos se briše sa naloga integracije nabavki i evidentira na trošku projekta.

1. Da biste podesili nalog integracije nabavke, idite u **Upravljanje projektima i računovodstvo** > **Podešavanje** > **Parametri upravljanja projektom i računovodstveni parametri** i otvorite **Project Operations u usluzi Dynamics 365 Dataverse**. 
2. Izaberite karticu **Materijali** i izaberite vrednost u polju **Nalog za integraciju nabavki**.

#### <a name="set-up-project-category-defaults-for-an-item"></a>Podesite podrazumevane kategorije projekta za stavku

1. U Finance, idite u **Upravljanje projektima i računovodstvo** > **Podešavanje** > **Parametri upravljanja projektom i računovodstveni parametri** i otvorite **Project Operations u usluzi Dynamics 365 Dataverse**. 
2. Na kartici **Podrazumevane kategorije projekata** u polju **Stavka** izaberite vrednost. Ova kategorija projekta koristi se za materijalne transakcije ako kategorija projekta nije postavljena u evidenciji stvarnih podataka o projektu.
