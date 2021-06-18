---
title: Upravljanje predlozima projektnih faktura
description: Ova tema pruža detalje o obradi faktura za klijente pomoću usluge Project Operations za resurs/scenarije koji nisu zasnovani na zalihama.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7e6d060c1cca08f86e2d04ca96c9315a17316d11
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001488"
---
# <a name="manage-project-invoice-proposals"></a>Upravljanje predlozima projektnih faktura

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Predloge projektnih faktura može obrađivati odeljenje za obračun kada su ispunjena sledeća dva uslova:

  - Menadžer projekta potvrdi predračun u usluzi Microsoft Dataverse.
  - Sve nenaplaćene transakcije prodaje vremena i materijala obuhvaćene predračunom su proknjižene pomoću Dynamics 365 **Project Operations** dnevnik integracije.

Koristite sledeće korake da biste dovršili predlog fakture za projekat u usluzi Dynamics 365 Finance.

1. Pregledajte informacije o naplati za transakcije vremena i materijala i objavite **Project Operations dnevnik integracije**.
2. Pregledajte informacije o naplati za kontrolne tačke naplate sa fiksnom cenom.
3. Pregledajte i oblikujte predlog projektne fakture.
4. Objavite i odštampjte projektne fakture.

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a>Upravljanje informacijama o naplati u Project Operations dnevniku integracije

Računovođa projekta u usluzi Finance pregleda i objavljuje stvarne podatke o projektu kreirane u usluzi Dataverse. Više informacija o radu sa dnevnikom integracije potražite u članku [Dnevnik integracije u usluzi Project Operations](../project-accounting/project-operations-integration-journal.md).

Stvarni podaci o ceni i stvarne vrednosti nenaplaćene prodaje dodaju se u dnevnik integracije u zasebne redove:

  - Jedinična cena koštanja i iznos troškova u odeljku „Stvarna vrednost troškova“ podrazumevano se dobijaju iz stvarnih troškova transakcije za projekat u usluzi Dataverse.
  - Jedinična prodajna cena i iznos prodaje u odeljku „Nenaplaćena prodajna transakcija“ podrazumevano se dobijaju iz stvarne nenaplaćene prodajne transakcije projekta u usluzi Dataverse.

### <a name="billing-sales-tax"></a>Naplata poreza na promet

Obračun poreza na promet za naplatu određuje se pomoću kombinacije polja **Grupa za naplatu poreza na promet** i **Grupa za porez na promet stavki na računu** u zapisu nenaplaćene prodaje u stavki u glavnoj knjizi **Project Operations integracije**. Sistem podrazumevano podešava ove vrednosti polja na osnovu podešavanja na kartici **Finansije** na stranici **Parametri upravljanja projektom i računovodstvom**.

- **Metod grupe za porez na promet** određuje podrazumevanu logiku grupe za naplatu poreza na promet:
  
  - **Projekat**: Uvek podrazumevano podešava grupu za naplatu poreza na promet iz projekta. Možete da pregledate ili promenite podrazumevanu grupu za naplatu poreza na promet u projektu izborom stavke **Prikaži podrazumevano računovodstvo** na stranici **Svi projekti**.
  - **Ugovor za projekat**: Uvek podrazumevano podešava grupu za naplatu poreza na promet iz ugovora za projekat. Možete da pregledate ili promenite podrazumevanu grupu za naplatu poreza na promet u ugovoru za projekat izborom stavke **Prikaži podrazumevano računovodstvo** na stranici **Ugovori za projekte**.
  - **Klijent**: Uvek podrazumevano podešava grupu za naplatu poreza na promet iz klijenta.
  - **Pretraga**: Pretražiće sve gorenavedene entitete i odabrati prvu dostupnu vrednost. Pretraga počinje entitetom **Projekat**, zatim sledi entitet **Ugovor o projektu** i na kraju entitet **Klijent**.

- **Metod grupe za porez na promet stavki** određuje podrazumevanu logiku grupe za porez na promet stavki na računu:
  
  - Za vrste transakcija vremena, troškova i naknada, grupa za porez na promet stavki na računu se uvek podrazumevano podešava iz entiteta **Kategorija projekta**.
  - Za vrste transakcija materijala, grupa za porez na promet stavki na računu se podrazumevano podešava na osnovu podešavanja **Metod grupe za porez na promet stavki** u delu **Parametri upravljanja projektom i računovodstvom**. Broj stavki podrazumevano podešava grupu za porez na promet stavki iz entiteta **Objavljeni proizvod**. Kategorija podrazumevano podešava grupu za porez na promet stavki iz entiteta **Kategorija projekta**.

### <a name="financial-dimensions"></a>Finansijski aspekti

Finansijski aspekti za zapise nenaplaćene prodaje u **Project Operations dnevniku integracije** se podrazumevano podešavaju iz entiteta **Projekat**. Finansijski aspekti se mogu pregledati i prilagoditi izborom stavke **Raspodeli iznose**. Ako morate da promenite finansijske aspekte zapisa nenaplaćene prodaje nakon objavljivanja dnevnika integracije, ali pre nego što se potvrdi profaktura, idite na **Svi projekti** > **Upravljaj** > **Proknjižene transakcije**, izaberite transakciju, a zatim izaberite **Proces** > **Prilagodi računovodstvo**.

### <a name="exchange-rates"></a>Kursne liste

Valuta nenaplaćene transakcije u usluzi Dataverse koristi se kao valuta transakcije u usluzi Finance i konvertuje se u računovodstvenu valutu kompanije koristeći devizne kurseve definisane u usluzi Finance.


## <a name="manage-the-financial-attributes-of-billing-milestones"></a>Upravljanje finansijskim atributima kontrolnih tačaka naplate 

Predmeti ugovora projekta koji koriste metodu naplate sa fiksnom cenom se fakturišu preko [kontrolnih tačaka sa fiksnom cenom](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line). Računovođa projekta može pregledati kontrolne tačke naplate u usluzi Finance tako što će otići na **Upravljanje projektima i računovodstvo** > **Svi projekti** > **Upravljaj** > **Transakcije za poslovnog klijenta**.

### <a name="billing-sales-tax"></a>Naplata poreza na promet

Vrednosti **Grupa za porez na promet** i **Grupa za porez na promet stavki** podrazumevano se podešavaju iz podešavanja kada se kreira nova kontrolna tačka naplate u usluzi Dataverse. Sistem podrazumevano podešava vrednosti u ovim poljima na osnovu podešavanja na kartici **Finansije** na stranici **Parametri upravljanja projektom i računovodstvom**.

- **Metod grupe za porez na promet** određuje podrazumevanu logiku stavke **Grupa za naplatu poreza na promet**:

    - **Projekat**: Uvek podrazumevano podešava grupu za naplatu poreza na promet iz projekta. Možete da pregledate ili promenite podrazumevanu grupu poreza na promet u projektu izborom stavke **Prikaži podrazumevano računovodstvo** na stranici **Svi projekti**.
    - **Ugovor za projekat**: Uvek podrazumevano podešava grupu za naplatu poreza na promet iz ugovora za projekat. Možete da pregledate ili promenite podrazumevanu grupu za naplatu poreza na promet u ugovoru za projekat izborom stavke **Prikaži podrazumevano računovodstvo** na stranici **Ugovori za projekte**.
    - **Klijent**: Uvek podrazumevano podešava grupu za naplatu poreza na promet iz klijenta.
    - **Pretraga**: Pretražiće sve entitete u ovoj listi i odabrati prvu dostupnu vrednost. Pretraga počinje entitetom **Projekat**, zatim sledi entitet **Ugovor o projektu** i onda entitet **Klijent**.

- **Grupa poreza na promet ključnih stavki sa fiksnim cenama** se koristi kao podrazumevana vrednost u polju **Grupa poreza na promet stavke** za kontrolnu tačku fakturisanja. Računovođa može pregledati i izmeniti ovu vrednost na stranici **Transakcije na računu**. Sistem koristi vrednost iz transakcije na računu prilikom kreiranja linije predloga fakture za projekat.
 

### <a name="financial-dimensions"></a>Finansijski aspekti

Podrazumevani finansijski aspekti za kontrolnu tačku naplate sa fiksnom cenom se podešavaju u predmetima ugovora za projekat. Idite na **Projektni ugovori** > **Prikaži podrazumevano računovodstvo** i na kartici **Predmeti ugovora** izaberite **predmet ugovora za cenu**, a zatim podesite vrednosti finansijskih aspekata koje želite da koristite kao podrazumevane.

Računovođa projekta može uređivati informacije o porezu na promet i finansijskim aspektima u kontrolnim tačkama fakture dok se ne kreira predlog fakture projekta.


## <a name="create-project-invoice-proposals"></a>Kreiranje predloga projektnih faktura

Predlozi projektnih faktura mogu se pregledati u modulu **Upravljanje projektima i računovodstvo** odlaskom na **Projektne fakture** > **Predlozi projektnih faktura**.

Zaglavlje predloga projektne fakture kreira se u usluzi Finance kada se profaktura potvrdi u usluzi Dataverse. Radi lakšeg svođenja stanja, sistem podešava broj predloga projektne fakture u usluzi Finance na isti broj kao i ID profakture u usluzi Dataverse. Budući da se profakture ne potvrđuju nužno istim redosledom kojim su kreirane, redosled brojeva predloga projektnih faktura u usluzi Finance mora omogućiti promene na manje i veće brojeve. Konfigurišite sekvence brojeva koristeći sledeće korake:

1. U usluzi Finance idite na **Administracija organizacije** > **Sekvence brojeva** > **Sekvence brojeva**.
2. U filteru **Oblast** izaberite **Projekti**.
3. U filteru **Referenca** izaberite **Predlog fakture**.
4. Koristiti polje **Kompanija** za filtriranje svakog pravnog lica za koje je omogućena Project Operations Dataverse integracija.
5. Otvorite **Detalji sekvence brojeva** i na kartici **Opšti podaci** podesite:

    - **Dozvoli korisničke promene: na niži broj** = **Da**
    - **Dozvoli korisničke promene: na veći broj** = **Da**

Redove za predloge projektnih faktura dodaje sistem periodičnim procesom **Uvoz iz pripremne tabele** (**Upravljanje projektima i računovodstvo** > **Periodično** > **Project Operations integracija** > **Uvoz iz pripremne tabele**). Ovaj proces možete ručno da pokrenete ili korišćenjem periodičnog rasporeda. Sistem neće dodavati redove u dokument predloga fakture dok svi redovi ne budu spremni za fakturisanje. Transakcije vremena i materijala su spremne za fakturisanje samo kada su proknjižene pomoću **Project Operations dnevnika integracije**.

## <a name="format-and-print-invoice-proposals"></a>Oblikovanje i štampanje predloga faktura

Računovođa projekta može prilagoditi otisak fakture projekta koristeći mogućnosti na stranici **Oblikovanje predlog fakture** i upravljanja štampanjem.

### <a name="format-invoice-proposals"></a>Oblikovanje predloga faktura

Stranica **Oblikovanje predloga faktura** omogućava prikazivanje prilagođenog grupisanja transakcija na fakturi projekta klijenta.

1. Na stranici **Predlog fakture projekta** izaberite **Štampaj** > **Oblikuj predlog fakture**.
2. Izaberite **Novo** da biste kreirali novo grupisanje za otisak fakture projekta.
3. U polju **Detalji/Rezime** izaberite opcije za ovo grupisanje:

    - Izaberite **Detalji** za štampanje detalja transakcije fakture klijenta.
    - Izaberite **Rezime** za štampanje rezimea transakcije fakture klijenta.

> [!NOTE]
> Izbor u polju **Detalji/Rezime** na stranici **Oblikovanje predloga fakture** zamenjuje opciju odabranu u polju **Format fakture** na stranici **Predlozi fakture** za štampanje detaljne fakture ili sažete fakture.

- Izaberite redove transakcija koje ćete uključiti u ovaj odeljak na kartici **Dostupne transakcije** i izaberite **Uvrsti transakcije** da ih premestite na karticu **Izabrane transakcije**.
- Izaberite **Pomeri gore** i **Pomeri dole** za promenu redosleda odeljaka.
- Izaberite **Prikaz za štampanje** za pregled formatirane fakture.

### <a name="print-management"></a>Upravljanje štampanjem

Upravljanje štampanjem koristi različite datoteke izveštaja za štampanje, određivanje odredišta i prilagođavanje teksta podnožja za fakturu. Upravljanje štampanjem se može podesiti na nivou modula, međutim, ova podešavanja mogu biti zamenjena za određenog klijenta, ugovor ili predlog fakture. Da biste pristupili ovoj funkciji na stranici **Predlog fakture projekta**, izaberite **Štampaj** > **Upravljanje štampanjem**.

Podešavanje upravljanja štampanjem prikazuje se u obliku stabla, gde svaki nivo čvora prikazuje dostupne dokumente za prilagođavanje. Možete dodeliti prilagođene otiske na nivou modula, klijenta, ugovora ili dokumenta predloga fakture. Da biste izmenili otisak originalnog dokumenta, proširite željeni čvor i izaberite **Originalna stavka**. U polju **Format izveštaja** izaberite format izveštaja koji će se koristiti za štampanje. Možete koristiti prilagođene formate izveštaja pomoću [okvira za upravljanje poslovnim dokumentima](/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).

## <a name="post-invoice-proposals"></a>Knjiženje predloga faktura

Nakon što je faktura pregledana i uređena, a redovi predloga fakture zadovoljavajući, proverite ukupne iznose fakture i porez na promet. U grupi **Detalji** izaberite **Ukupan iznos**, a zatim izaberite **Knjiži** da proknjižite fakturu.

Da biste pregledali fakturu pre knjiženja, obrišite znak u polju za potvrdu **Knjiženje**. **Profaktura** će biti odštampano na fakturi da bi se označilo da je reč o primeru fakture. Da biste odštampali fakturu, označite polje za potvrdu **Odštampaj fakturu**.

Osim na stranici **Predlog fakture**, predlozi fakture mogu da se knjiže i pokretanjem periodičnog posla **Knjiženje predloga faktura**. Da biste pronašli ovaj posao, idite na **Upravljanje projektima i računovodstvo** > **Periodično** > **Projektne fakture** > **Knjiženje predloga faktura**.

Ova stranica prikazuje sve predloge faktura koji su spremni za knjiženje. Možete da zakažete knjiženje predloga faktura odabirom stavke **Grupno**. Podesite **Parametar grupne obrade** na **Da** i podesite ponavljanje grupne obrade izborom stavke **Ponavljanje**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
