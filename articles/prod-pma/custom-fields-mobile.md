---
title: Primena prilagođenih polja za Microsoft Dynamics 365 Project Timesheet aplikaciju za mobilne uređaje na platformama iOS i Android
description: Ova tema pruža uobičajene obrasce za korišćenje ekstenzija za primenu prilagođenih polja.
author: Yowelle
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 1ea1ca002a8f68f86808831b398e452244471322
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083634"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Primena prilagođenih polja za Microsoft Dynamics 365 Project Timesheet aplikaciju za mobilne uređaje na platformama iOS i Android

[!include [banner](../includes/banner.md)]

Ova tema pruža uobičajene obrasce za korišćenje ekstenzija za primenu prilagođenih polja. Obuhvaćene su sledeće teme:

- Različiti tipovi podataka koje prilagođeni okvir polja podržava
- Kako na unosima vremenskog rasporeda prikazati polja samo za čitanje ili uređivanje i sačuvati vrednosti koje su obezbedili korisnici nazad u bazu podataka
- Kako prikazati polja samo za čitanje u zaglavlju vremenskog rasporeda
- Kako integrisati drugu prilagođenu poslovnu logiku za unos podrazumevanih vrednosti u polja i izvršiti dodatnu proveru valjanosti

## <a name="audience"></a>Korisnici

Ova tema je namenjena programerima koji integrišu prilagođena polja u Microsoft Dynamics 365 Project Timesheet aplikaciju za mobilne uređaje koja je dostupna za Apple iOS i Google Android. Pretpostavlja se da su čitaoci upoznati sa X++ razvojem i funkcionalnošću vremenskog rasporeda projekta.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Ugovor o podacima – TSTimesheetCustomField X++ klasa

Klasa **TSTimesheetCustomField** je X++ klasa ugovora podataka koja predstavlja informacije o prilagođenom polju za funkciju vremenskog rasporeda. Liste prilagođenih objekata polja prosleđuju se i u TSTimesheetDetails ugovoru podataka i u TSTimesheetEntry ugovoru podataka da bi se prikazala prilagođena polja u aplikaciji za mobilne uređaje.

- **TSTimesheetDetails** – Ugovor za zaglavlje vremenskog lista.
- **TSTimesheetEntry** – Ugovor o transakciji vremenskog rasporeda. Grupe ovih objekata koje imaju iste informacije o projektu i vrednost **timesheetLineRecId** čine liniju.

### <a name="fieldbasetype-types"></a>fieldBaseType (Tipovi)

Svojstvo **FieldBaseType** na objektu **TsTimesheetCustom** određuje tip polja koje se prikazuje u aplikaciji. Sledeće vrednosti **Tipova** koje su podržane.

| Vrednosti tipova | Tip              | Napomene |
|-------------|-------------------|-------|
| 0           | Niska (i numerička vrednost) | Polje se prikazuje kao tekstualno polje. |
| 1           | Integer           | Vrednost se prikazuje kao broj bez decimalnih mesta. |
| 2           | Realni broj              | Vrednost se prikazuje kao broj koji ima decimalna mesta.<p>Da biste prikazali stvarnu vrednost kao valutu u aplikaciji, koristite svojstvo **fieldExtenededType**. Možete koristiti svojstvo **numberOfDecimals** za podešavanje broja decimalnih mesta koja su prikazana.</p> |
| 3           | Datum              | Formati datuma se određuju prema korisnikovom podešavanju **Datum, vreme i format broja** koje je navedeno u odeljku **Željene opcije jezika i zemlje/regiona** u delu **Korisničke opcije**. |
| 4           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Ako je svojstvo **stringOptions** nije navedeno na objektu **TSTimesheetCustomField** , korisniku se pruža polje slobodnog teksta.

    Svojstvo **stringLength** se može koristiti za podešavanje maksimalne dužine niza koju korisnici mogu uneti.

- Ako je svojstvo **stringOptions** navedeno na objektu **TSTimesheetCustomField** , ti elementi liste su jedine vrednosti koje korisnici mogu da izaberu pomoću dugmadi sa opcijama (radio dugmad).

    U ovom slučaju, polje niza može delovati kao numerička vrednost u svrhu unosa korisnika. Da biste sačuvali vrednost u bazi podataka kao nabrajanje, ručno mapirajte vrednost niza na vrednost nabrajanja pre nego što je sačuvate u bazi podataka pomoću lanca komandi (kao primer, pogledajte odeljak „Upotreba lanca komandi u klasi TSTimesheetEntryService radi čuvanja stavke vremenskog rasporeda iz aplikacije nazad u bazu podataka“ kasnije u ovoj temi).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Ovo svojstvo možete koristiti za formatiranje stvarnih vrednosti kao valute. Ovaj pristup je primenljiv samo kada **fieldBaseType** ima vrednost **Realni broj**.

- **TSCustomFieldExtendedType:None** – Nije primenjeno formatiranje.
- **TSCustomFieldExtendedType::Currency** – Formatirajte vrednost kao valutu.

    Kada je formatiranje valuta aktivno, polje **stringValue** se može koristiti za dodavanje koda valute koji bi trebalo da bude prikazan u aplikaciji. Ta vrednost je samo za čitanje.

    Polje **realValue** sadrži iznos novca koji treba sačuvati u bazi podataka.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Ovim svojstvom možete da odredite gde bi prilagođeno polje trebalo da se pojavi u aplikaciji.

- **TSCustomFieldSection::Header** – Polje će se prikazati u odeljku **Pogledajte više detalja** u aplikaciji. Ova polja su uvek samo za čitanje.
- **TSCustomFieldSection::Line** – Polje će se prikazati nakon svih unapred pripremljenih polja reda u vremenskom rasporedu. Ova polja mogu biti za uređivanje ili samo za čitanje.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Ovo svojstvo identifikuje polje kada se vrednosti koje aplikacija pruža ponovo sačuvaju u bazi podataka.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Ovo svojstvo identifikuje polje kada se vrednosti koje aplikacija pruža ponovo sačuvaju u bazi podataka.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Podesite ovo svojstvo na **Da** kako biste naveli da korisnici mogu da uređuju polje u odeljku stavke vremenskog rasporeda. Podesite svojstvo na **Ne** kako bi polje bilo samo za čitanje.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Podesite ovo svojstvo na **Da** kako biste naveli da polje u odeljku stavke vremenskog rasporeda treba da bude obavezno.

### <a name="label-str"></a>label (str)

Ovo svojstvo navodi oznaku koja se prikazuje pored polja u aplikaciji.

### <a name="stringoptions-list-of-strings"></a>stringOptions (List of Strings)

Ovo svojstvo je primenljivo samo kada se **fieldBaseType** podesi na **Niz**. Ako je **stringOptions** postavljeno, vrednosti niza koje su dostupne za izbor preko opcionalnih dugmadi (radio dugmadi) određene su nizovima na listi. Ako nisu obezbeđene niske, dozvoljen je unos slobodnog teksta u polje niske (kao primer, pogledajte odeljak „Upotrebite lanac komandi u klasi TSTimesheetEntryService da biste sačuvali stavku vremenskog rasporeda iz aplikacije nazad u bazu podataka“, kasnije u ovoj temi).

### <a name="stringlength-int"></a>stringLength (int)

Ovo svojstvo navodi maksimalnu dužinu polja niske. Ovo svojstvo je primenljivo samo kada se **fieldBaseType** podesi na **Niska**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Ovo svojstvo navodi broj decimalnih mesta koja su prikazana za stvarno polje. Ovo svojstvo je primenljivo samo kada se **fieldBaseType** podesi na **Realni broj**.

### <a name="ordersequence-int"></a>orderSequence (int)

Ovo svojstvo kontroliše redosled prikazivanja prilagođenih polja u aplikaciji kada je navedeno više od jednog prilagođenog polja. Prvo se prikazuju polja koja imaju manje brojeve.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

Za polja tipa **Logička vrednost** , ovo svojstvo prenosi logičku vrednost polja između servera i aplikacije.

### <a name="guidvalue-guid"></a>guidValue (guid)

Za polja tipa **GUID** , ovo svojstvo prenosi vrednost globalnog jedinstvenog identifikatora (GUID) između servera i aplikacije.

### <a name="int64value-int64"></a>int64Value (int64)

Za polja tipa **Int64** , ovo svojstvo prenosi int64 vrednost polja između servera i aplikacije.

### <a name="intvalue-int"></a>intValue (int)

Za polja tipa **Int** , ovo svojstvo prenosi int vrednost polja između servera i aplikacije.

### <a name="realvalue-real"></a>realValue (real)

Za polja tipa **Realni broj** , ovo svojstvo prenosi realnu vrednost polja između servera i aplikacije.

### <a name="stringvalue-str"></a>stringValue (str)

Za polja tipa **Niska** , ovo svojstvo prenosi vrednost niske polja između servera i aplikacije. Takođe se koristi za polja tipa **Realni broj** koji su formatirani kao valuta. Za ta polja, svojstvo se koristi za prosleđivanje koda valute aplikaciji.

### <a name="datevalue-date"></a>dateValue (date)

Za polja tipa **Datum** , ovo svojstvo prenosi vrednost datuma polja između servera i aplikacije.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Prikažite i sačuvajte prilagođeno polje u odeljku stavke vremenskog rasporeda

U nastavku se nalazi snimak ekrana iz aplikacije za mobilne uređaje gde se kreira stavka vremenskog rasporeda. Pokazuje unapred pripremljena polja i prilagođena polja u odeljku „Stavka vremena“ pod nazivom „Test niska“ sa već postavljenom numeričkom vrednošću „Druga opcija“.

![Prilagođeno polje za testiranje niski u aplikaciji](media/timesheet-entry.jpg)



U nastavku se nalazi snimak ekrana iz aplikacije za mobilne uređaje korisnika koji bira jednu od opcija nabrajanja dostupnih za prilagođeno polje „Test niska“.  Dve opcije su „Prva opcija“ i „Druga opcija“, prikazane kao radio dugmad. Trenutno je izabrana druga opcija.

![Dugmad sa opcijama (radio dugmad) za prilagođeno polje Test niska](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Proširite tabelu TSTimesheetLine tako da ima prilagođeno polje

U tipičnim scenarijima, verovatno će podaci za prilagođeno polje u odeljku stavke vremenskog rasporeda biti sačuvani u tabeli TSTimesheetLine. Međutim, druge tabele se mogu koristiti ako se podaci mogu dobiti na osnovu TSTimesheetTrans zapisa koji je naveden ili ako nema određeni kontekst zapisa (na primer, ako je polje postavljeno kao samo za čitanje u parametrima projekta).

Imajte na umu da prilagođena polja ne moraju imati nikakve prateće zapise baze podataka. Mogu se dinamički generisati na osnovu X++ logike. Ovaj pristup može biti koristan u scenarijima samo za čitanje (pogledajte odeljak „Koristite lanac komandi na klasi TSTimesheetDetails, metodi buildCustomFieldListForHeader za popunjavanje detalja vremenskog rasporeda“ za primer dinamički generisanih vrednosti prilagođenih polja.)

U nastavku se nalazi snimak ekrana sa Visual Studio stablom objekata aplikacije. Prikazuje se proširenje tabele TSTimesheetLine sa poljem TestLineString koje je dodato kao prilagođeno polje.

![Niska linije](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Koristite lanac komandi na metodi buildCustomFieldList klase TSTimesheetSettings da biste prikazali polje u odeljku stavke vremenskog rasporeda

Ovaj kôd kontroliše postavke prikaza za polje u aplikaciji. Na primer, kontroliše tip polja, oznaku, da li je polje obavezno i u kom odeljku se polje prikazuje.

Sledeći primer prikazuje polje niza za stavke vremena. Ovo polje ima dve opcije, **Prva opcija** i **Druga opcija** , koje su dostupne preko dugmadi opcija (radio dugmadi). Polje u aplikaciji je povezano sa poljem **TestLineString** koje se dodaje u tabelu TSTimesheetLine.

Obratite pažnju na upotrebu metode **TSTimesheetCustomField::newFromMetatdata()** za pojednostavljivanje inicijalizacije svojstava prilagođenog polja: **fieldBaseType** , **tableName** , **fieldname** , **label** , **isEditable** , **isMandatory** , **stringLength** i **numberOfDecimals**. Ove parametre možete takođe ručno da podesite kako želite.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Koristite lanac komandi na metodi buildCustomFieldListForEntry klase TSTimesheetEntry da biste unosili vrednosti u stavku vremenskog rasporeda

Metoda **buildCustomFieldListForEntry** se koristi za unos vrednosti u sačuvane redove vremenskog rasporeda u aplikaciji za mobilne uređaje. Kao parametar uzima se zapis TSTimesheetTrans. Polja iz tog zapisa mogu se koristiti za popunjavanje vrednosti prilagođenog polja u aplikaciji.

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Upotreba lanca komandi u klasi TSTimesheetEntryService radi čuvanja stavke vremenskog rasporeda iz aplikacije nazad u bazu podataka

Da biste sačuvali prilagođeno polje u bazu podataka u uobičajenoj upotrebi, morate proširiti više metoda:

- Metoda **timesheetLineNeedsUpdating** se koristi da bi se utvrdilo da li je korisnik u aplikaciji promenio zapis linije i da li zapis mora da bude sačuvan u bazi podataka. Ako performanse nisu problem, ova metoda se može pojednostaviti tako da se uvek vraća **tačno**.
- Metode **populateTimesheetLineFromEntryDuringCreate** i **populateTimesheetLineFromEntryDuringUpdate** se mogu proširiti tako da unose vrednosti u zapis baze podataka TSTimesheetLine iz obezbeđenog zapisa TSTimesheetEntry ugovora podataka. U primeru koji sledi obratite pažnju kako se preko X++ koda obavlja ručno mapiranje između polja baze podataka i polja stavke.
- Metoda **populateTimesheetWeekFromEntry** se takođe može proširiti ako se prilagođeno polje koje se mapira na objekat **TSTimesheetEntry** mora upisati nazad u tabelu baze podataka TSTimesheetLineweek.

> [!NOTE]
> Sledeći primer čuva vrednost **firstOption** ili **secondOption** koju korisnik bira u bazu podataka kao sirovu vrednost niza. Ako je polje baze podataka polje **Nabrajanje** , te vrednosti se mogu ručno mapirati na vrednost nabrajanja, a zatim sačuvati u polju nabrajanja u tabeli baze podataka.

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Prikažite prilagođeno polje u odeljku zaglavlja vremenskog rasporeda

U nastavku se nalazi snimak ekrana iz aplikacije za mobilne uređaje gde korisnik pregleda vremenski raspored. U gornjem desnom uglu je izabrano dugme „Više informacija“ da bi se prikazala opcija „Prikaži više detalja“.  

![Komanda Prikaži više detalja](media/show-more.png)

U nastavku se nalazi snimak ekrana iz aplikacije za mobilne uređaje gde se prikazuje odeljak „Još“ vremenskog rasporeda. Prilagođeno polje pod nazivom „Stopa iskorišćenosti ovog vremenskog rasporeda (izračunato prilagođeno polje)“ dodato je u odeljak zaglavlja vremenskog rasporeda. Vrednost samo za čitanje „0,667“ postavljena je u prilagođenom polju.

![Odeljak „Još“](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Proširite tabelu TSTimesheetTable tako da ima prilagođeno polje

U tipičnim scenarijima, verovatno će podaci za prilagođeno polje u odeljku zaglavlja biti povučeni iz tabele TSTimesheetHeader. Međutim, druge tabele se mogu koristiti ako se podaci mogu dobiti na osnovu zapisa TSTimesheetTable koji je naveden ili ako nema određeni kontekst zapisa (na primer, ako je polje postavljeno kao samo za čitanje u parametrima projekta).

Imajte na umu da prilagođena polja ne moraju imati nikakve prateće zapise baze podataka. Mogu se dinamički generisati na osnovu X++ logike. Primer koji sledi pokazuje ovaj pristup.

Polja u odeljku zaglavlja u aplikaciji su uvek samo za čitanje.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Koristite lanac komandi na metodi buildCustomFieldList klase TSTimesheetSettings da biste prikazali polje u odeljku zaglavlja vremenskog rasporeda

Ovaj kôd kontroliše postavke prikaza za polje u aplikaciji. Na primer, kontroliše tip polja, oznaku, da li je polje obavezno i u kom odeljku se polje prikazuje.

Sledeći primer prikazuje izračunatu vrednost u odeljku zaglavlja u aplikaciji.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Koristite lanac komandi na metodi buildCustomFieldListForHeader klase TSTimesheetDetails da biste popunjavali detalje vremenskog rasporeda

Metoda **buildCustomFieldListForHeader** se koristi za popunu detalja zaglavlja vremenskog rasporeda u aplikaciji za mobilne uređaje. Kao parametar se uzima zapis TSTimesheetTable. Polja iz tog zapisa mogu se koristiti za popunjavanje vrednosti prilagođenog polja u aplikaciji. Sledeći primer ne čita nijednu vrednost iz baze podataka. Umesto toga, koristi X++ logiku za generisanje izračunate vrednosti koja se zatim prikazuje u aplikaciji.


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Ostale mogućnosti prilagodljivosti/proširivosti

### <a name="adding-additional-validation-for-the-app"></a>Dodavanje dodatne provere za aplikaciju

Postojeća logika za funkcionalnost vremenskog lista na nivou baze podataka i dalje će raditi kako se očekivalo. Da biste prekinuli dovršavanje operacija čuvanja ili slanja i prikazali određenu poruku o grešci, možete da dodate **throw error("poruka korisniku")** u kôd preko lanca dodatka komandi. Slede tri primera korisnih proširivih metoda:

- Ako **validateWrite** na tabeli TSTimesheetLine vrati **netačno** tokom operacije čuvanja za red vremenskog rasporeda, poruka o grešci se prikazuje u aplikaciji za mobilne uređaje.
- Ako **validateSubmit** na tabeli TSTimesheetTable vrati **netačno** tokom prosleđivanja vremenskog rasporeda u aplikaciji, korisniku se prikazuje poruka o grešci.
- Logika koja popunjava polja (na primer, **Svojstvo reda** ) tokom metode **insert** na tabeli TSTimesheetLine i dalje će biti aktivna.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Sakrivanje i označavanje polja izvan okvira kao samo za čitanje putem konfiguracije

Iz parametara projekta možete da napravite unapred pripremljena polja koja su samo za čitanje ili skrivena u aplikaciji za mobilne uređaje. Postavite opcije u odeljku **Mobilni vremenski rasporedi** na kartici **Vremenski raspored** na stranici **Parametri upravljanja projektom i računovodstvom**.

![Parametri projekta](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Promena aktivnosti koje su dostupne za izbor putem dodataka

Aktivnosti koje su na raspolaganju za odabir za projekat popunjavaju se putem metoda **getActivitiesForProject()** i **getActivityQuery()** u klasi **TsTimesheetProjectService**. Možete da koristite lanac komandi da biste ovo ponašanje promenili tako da odgovara vašem poslovnom scenariju za aktivnosti koje su dostupne za odabir za određeni projekat.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Unos podrazumevane kategorije projekta u stavke vremenskog rasporeda

Unos podrazumevane kategorije projekta u stavke vremenskog rasporeda odvija se na tri nivoa. Možete koristiti lanac komandi da proširite ponašanje na bilo kom ili svim ovim nivoima kako biste postigli željeno ponašanje. Koristi se sledeća hijerarhija:

1. Aplikacija pokušava da postavi podrazumevanu kategoriju iz resursa projekta. Ova podrazumevana kategorija je podešena u metodama **getCurrentUserResource** i **getDelegatedResourcesForCurrentUser** u klasi **TSTimesheetSettingsService**.
2. Ako podrazumevana kategorija nije navedena na nivou resursa projekta, aplikacija pokušava da je povuče iz aktivnosti projekta. Ova podrazumevana kategorija je postavljena u metodi **getActivitiesForProject** u klasi **TSTimesheetProjectService**.
3. Ako podrazumevana kategorija nije navedena na nivou aktivnosti projekta, podrazumevana kategorija se preuzima iz parametara projekta. Ova podrazumevana kategorija se postavlja u metodi **getProjectDetailsbyRule** u klasi **TSTimesheetProjectService**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]