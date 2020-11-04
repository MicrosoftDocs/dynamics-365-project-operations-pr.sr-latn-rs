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
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="43695-103">Primena prilagođenih polja za Microsoft Dynamics 365 Project Timesheet aplikaciju za mobilne uređaje na platformama iOS i Android</span><span class="sxs-lookup"><span data-stu-id="43695-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43695-104">Ova tema pruža uobičajene obrasce za korišćenje ekstenzija za primenu prilagođenih polja.</span><span class="sxs-lookup"><span data-stu-id="43695-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="43695-105">Obuhvaćene su sledeće teme:</span><span class="sxs-lookup"><span data-stu-id="43695-105">The following topics are covered:</span></span>

- <span data-ttu-id="43695-106">Različiti tipovi podataka koje prilagođeni okvir polja podržava</span><span class="sxs-lookup"><span data-stu-id="43695-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="43695-107">Kako na unosima vremenskog rasporeda prikazati polja samo za čitanje ili uređivanje i sačuvati vrednosti koje su obezbedili korisnici nazad u bazu podataka</span><span class="sxs-lookup"><span data-stu-id="43695-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="43695-108">Kako prikazati polja samo za čitanje u zaglavlju vremenskog rasporeda</span><span class="sxs-lookup"><span data-stu-id="43695-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="43695-109">Kako integrisati drugu prilagođenu poslovnu logiku za unos podrazumevanih vrednosti u polja i izvršiti dodatnu proveru valjanosti</span><span class="sxs-lookup"><span data-stu-id="43695-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="43695-110">Korisnici</span><span class="sxs-lookup"><span data-stu-id="43695-110">Audience</span></span>

<span data-ttu-id="43695-111">Ova tema je namenjena programerima koji integrišu prilagođena polja u Microsoft Dynamics 365 Project Timesheet aplikaciju za mobilne uređaje koja je dostupna za Apple iOS i Google Android.</span><span class="sxs-lookup"><span data-stu-id="43695-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="43695-112">Pretpostavlja se da su čitaoci upoznati sa X++ razvojem i funkcionalnošću vremenskog rasporeda projekta.</span><span class="sxs-lookup"><span data-stu-id="43695-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="43695-113">Ugovor o podacima – TSTimesheetCustomField X++ klasa</span><span class="sxs-lookup"><span data-stu-id="43695-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="43695-114">Klasa **TSTimesheetCustomField** je X++ klasa ugovora podataka koja predstavlja informacije o prilagođenom polju za funkciju vremenskog rasporeda.</span><span class="sxs-lookup"><span data-stu-id="43695-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="43695-115">Liste prilagođenih objekata polja prosleđuju se i u TSTimesheetDetails ugovoru podataka i u TSTimesheetEntry ugovoru podataka da bi se prikazala prilagođena polja u aplikaciji za mobilne uređaje.</span><span class="sxs-lookup"><span data-stu-id="43695-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="43695-116">**TSTimesheetDetails** – Ugovor za zaglavlje vremenskog lista.</span><span class="sxs-lookup"><span data-stu-id="43695-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="43695-117">**TSTimesheetEntry** – Ugovor o transakciji vremenskog rasporeda.</span><span class="sxs-lookup"><span data-stu-id="43695-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="43695-118">Grupe ovih objekata koje imaju iste informacije o projektu i vrednost **timesheetLineRecId** čine liniju.</span><span class="sxs-lookup"><span data-stu-id="43695-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="43695-119">fieldBaseType (Tipovi)</span><span class="sxs-lookup"><span data-stu-id="43695-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="43695-120">Svojstvo **FieldBaseType** na objektu **TsTimesheetCustom** određuje tip polja koje se prikazuje u aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="43695-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="43695-121">Sledeće vrednosti **Tipova** koje su podržane.</span><span class="sxs-lookup"><span data-stu-id="43695-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="43695-122">Vrednosti tipova</span><span class="sxs-lookup"><span data-stu-id="43695-122">Types value</span></span> | <span data-ttu-id="43695-123">Tip</span><span class="sxs-lookup"><span data-stu-id="43695-123">Type</span></span>              | <span data-ttu-id="43695-124">Napomene</span><span class="sxs-lookup"><span data-stu-id="43695-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="43695-125">0</span><span class="sxs-lookup"><span data-stu-id="43695-125">0</span></span>           | <span data-ttu-id="43695-126">Niska (i numerička vrednost)</span><span class="sxs-lookup"><span data-stu-id="43695-126">String (and Enum)</span></span> | <span data-ttu-id="43695-127">Polje se prikazuje kao tekstualno polje.</span><span class="sxs-lookup"><span data-stu-id="43695-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="43695-128">1</span><span class="sxs-lookup"><span data-stu-id="43695-128">1</span></span>           | <span data-ttu-id="43695-129">Integer</span><span class="sxs-lookup"><span data-stu-id="43695-129">Integer</span></span>           | <span data-ttu-id="43695-130">Vrednost se prikazuje kao broj bez decimalnih mesta.</span><span class="sxs-lookup"><span data-stu-id="43695-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="43695-131">2</span><span class="sxs-lookup"><span data-stu-id="43695-131">2</span></span>           | <span data-ttu-id="43695-132">Realni broj</span><span class="sxs-lookup"><span data-stu-id="43695-132">Real</span></span>              | <span data-ttu-id="43695-133">Vrednost se prikazuje kao broj koji ima decimalna mesta.</span><span class="sxs-lookup"><span data-stu-id="43695-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="43695-134">Da biste prikazali stvarnu vrednost kao valutu u aplikaciji, koristite svojstvo **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="43695-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="43695-135">Možete koristiti svojstvo **numberOfDecimals** za podešavanje broja decimalnih mesta koja su prikazana.</span><span class="sxs-lookup"><span data-stu-id="43695-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="43695-136">3</span><span class="sxs-lookup"><span data-stu-id="43695-136">3</span></span>           | <span data-ttu-id="43695-137">Datum</span><span class="sxs-lookup"><span data-stu-id="43695-137">Date</span></span>              | <span data-ttu-id="43695-138">Formati datuma se određuju prema korisnikovom podešavanju **Datum, vreme i format broja** koje je navedeno u odeljku **Željene opcije jezika i zemlje/regiona** u delu **Korisničke opcije**.</span><span class="sxs-lookup"><span data-stu-id="43695-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="43695-139">4</span><span class="sxs-lookup"><span data-stu-id="43695-139">4</span></span>           | <span data-ttu-id="43695-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="43695-140">Boolean</span></span>           | |
| <span data-ttu-id="43695-141">15</span><span class="sxs-lookup"><span data-stu-id="43695-141">15</span></span>          | <span data-ttu-id="43695-142">GUID</span><span class="sxs-lookup"><span data-stu-id="43695-142">GUID</span></span>              | |
| <span data-ttu-id="43695-143">16</span><span class="sxs-lookup"><span data-stu-id="43695-143">16</span></span>          | <span data-ttu-id="43695-144">Int64</span><span class="sxs-lookup"><span data-stu-id="43695-144">Int64</span></span>             | |

- <span data-ttu-id="43695-145">Ako je svojstvo **stringOptions** nije navedeno na objektu **TSTimesheetCustomField** , korisniku se pruža polje slobodnog teksta.</span><span class="sxs-lookup"><span data-stu-id="43695-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="43695-146">Svojstvo **stringLength** se može koristiti za podešavanje maksimalne dužine niza koju korisnici mogu uneti.</span><span class="sxs-lookup"><span data-stu-id="43695-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="43695-147">Ako je svojstvo **stringOptions** navedeno na objektu **TSTimesheetCustomField** , ti elementi liste su jedine vrednosti koje korisnici mogu da izaberu pomoću dugmadi sa opcijama (radio dugmad).</span><span class="sxs-lookup"><span data-stu-id="43695-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="43695-148">U ovom slučaju, polje niza može delovati kao numerička vrednost u svrhu unosa korisnika.</span><span class="sxs-lookup"><span data-stu-id="43695-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="43695-149">Da biste sačuvali vrednost u bazi podataka kao nabrajanje, ručno mapirajte vrednost niza na vrednost nabrajanja pre nego što je sačuvate u bazi podataka pomoću lanca komandi (kao primer, pogledajte odeljak „Upotreba lanca komandi u klasi TSTimesheetEntryService radi čuvanja stavke vremenskog rasporeda iz aplikacije nazad u bazu podataka“ kasnije u ovoj temi).</span><span class="sxs-lookup"><span data-stu-id="43695-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="43695-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="43695-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="43695-151">Ovo svojstvo možete koristiti za formatiranje stvarnih vrednosti kao valute.</span><span class="sxs-lookup"><span data-stu-id="43695-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="43695-152">Ovaj pristup je primenljiv samo kada **fieldBaseType** ima vrednost **Realni broj**.</span><span class="sxs-lookup"><span data-stu-id="43695-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="43695-153">**TSCustomFieldExtendedType:None** – Nije primenjeno formatiranje.</span><span class="sxs-lookup"><span data-stu-id="43695-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="43695-154">**TSCustomFieldExtendedType::Currency** – Formatirajte vrednost kao valutu.</span><span class="sxs-lookup"><span data-stu-id="43695-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="43695-155">Kada je formatiranje valuta aktivno, polje **stringValue** se može koristiti za dodavanje koda valute koji bi trebalo da bude prikazan u aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="43695-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="43695-156">Ta vrednost je samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="43695-156">The value is a read-only value.</span></span>

    <span data-ttu-id="43695-157">Polje **realValue** sadrži iznos novca koji treba sačuvati u bazi podataka.</span><span class="sxs-lookup"><span data-stu-id="43695-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="43695-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="43695-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="43695-159">Ovim svojstvom možete da odredite gde bi prilagođeno polje trebalo da se pojavi u aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="43695-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="43695-160">**TSCustomFieldSection::Header** – Polje će se prikazati u odeljku **Pogledajte više detalja** u aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="43695-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="43695-161">Ova polja su uvek samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="43695-161">These fields are always read-only.</span></span>
- <span data-ttu-id="43695-162">**TSCustomFieldSection::Line** – Polje će se prikazati nakon svih unapred pripremljenih polja reda u vremenskom rasporedu.</span><span class="sxs-lookup"><span data-stu-id="43695-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="43695-163">Ova polja mogu biti za uređivanje ili samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="43695-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="43695-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="43695-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="43695-165">Ovo svojstvo identifikuje polje kada se vrednosti koje aplikacija pruža ponovo sačuvaju u bazi podataka.</span><span class="sxs-lookup"><span data-stu-id="43695-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="43695-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="43695-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="43695-167">Ovo svojstvo identifikuje polje kada se vrednosti koje aplikacija pruža ponovo sačuvaju u bazi podataka.</span><span class="sxs-lookup"><span data-stu-id="43695-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="43695-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="43695-168">isEditable (NoYes)</span></span>

<span data-ttu-id="43695-169">Podesite ovo svojstvo na **Da** kako biste naveli da korisnici mogu da uređuju polje u odeljku stavke vremenskog rasporeda.</span><span class="sxs-lookup"><span data-stu-id="43695-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="43695-170">Podesite svojstvo na **Ne** kako bi polje bilo samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="43695-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="43695-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="43695-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="43695-172">Podesite ovo svojstvo na **Da** kako biste naveli da polje u odeljku stavke vremenskog rasporeda treba da bude obavezno.</span><span class="sxs-lookup"><span data-stu-id="43695-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="43695-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="43695-173">label (str)</span></span>

<span data-ttu-id="43695-174">Ovo svojstvo navodi oznaku koja se prikazuje pored polja u aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="43695-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="43695-175">stringOptions (List of Strings)</span><span class="sxs-lookup"><span data-stu-id="43695-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="43695-176">Ovo svojstvo je primenljivo samo kada se **fieldBaseType** podesi na **Niz**.</span><span class="sxs-lookup"><span data-stu-id="43695-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="43695-177">Ako je **stringOptions** postavljeno, vrednosti niza koje su dostupne za izbor preko opcionalnih dugmadi (radio dugmadi) određene su nizovima na listi.</span><span class="sxs-lookup"><span data-stu-id="43695-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="43695-178">Ako nisu obezbeđene niske, dozvoljen je unos slobodnog teksta u polje niske (kao primer, pogledajte odeljak „Upotrebite lanac komandi u klasi TSTimesheetEntryService da biste sačuvali stavku vremenskog rasporeda iz aplikacije nazad u bazu podataka“, kasnije u ovoj temi).</span><span class="sxs-lookup"><span data-stu-id="43695-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="43695-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="43695-179">stringLength (int)</span></span>

<span data-ttu-id="43695-180">Ovo svojstvo navodi maksimalnu dužinu polja niske.</span><span class="sxs-lookup"><span data-stu-id="43695-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="43695-181">Ovo svojstvo je primenljivo samo kada se **fieldBaseType** podesi na **Niska**.</span><span class="sxs-lookup"><span data-stu-id="43695-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="43695-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="43695-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="43695-183">Ovo svojstvo navodi broj decimalnih mesta koja su prikazana za stvarno polje.</span><span class="sxs-lookup"><span data-stu-id="43695-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="43695-184">Ovo svojstvo je primenljivo samo kada se **fieldBaseType** podesi na **Realni broj**.</span><span class="sxs-lookup"><span data-stu-id="43695-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="43695-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="43695-185">orderSequence (int)</span></span>

<span data-ttu-id="43695-186">Ovo svojstvo kontroliše redosled prikazivanja prilagođenih polja u aplikaciji kada je navedeno više od jednog prilagođenog polja.</span><span class="sxs-lookup"><span data-stu-id="43695-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="43695-187">Prvo se prikazuju polja koja imaju manje brojeve.</span><span class="sxs-lookup"><span data-stu-id="43695-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="43695-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="43695-188">booleanValue (boolean)</span></span>

<span data-ttu-id="43695-189">Za polja tipa **Logička vrednost** , ovo svojstvo prenosi logičku vrednost polja između servera i aplikacije.</span><span class="sxs-lookup"><span data-stu-id="43695-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="43695-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="43695-190">guidValue (guid)</span></span>

<span data-ttu-id="43695-191">Za polja tipa **GUID** , ovo svojstvo prenosi vrednost globalnog jedinstvenog identifikatora (GUID) između servera i aplikacije.</span><span class="sxs-lookup"><span data-stu-id="43695-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="43695-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="43695-192">int64Value (int64)</span></span>

<span data-ttu-id="43695-193">Za polja tipa **Int64** , ovo svojstvo prenosi int64 vrednost polja između servera i aplikacije.</span><span class="sxs-lookup"><span data-stu-id="43695-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="43695-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="43695-194">intValue (int)</span></span>

<span data-ttu-id="43695-195">Za polja tipa **Int** , ovo svojstvo prenosi int vrednost polja između servera i aplikacije.</span><span class="sxs-lookup"><span data-stu-id="43695-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="43695-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="43695-196">realValue (real)</span></span>

<span data-ttu-id="43695-197">Za polja tipa **Realni broj** , ovo svojstvo prenosi realnu vrednost polja između servera i aplikacije.</span><span class="sxs-lookup"><span data-stu-id="43695-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="43695-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="43695-198">stringValue (str)</span></span>

<span data-ttu-id="43695-199">Za polja tipa **Niska** , ovo svojstvo prenosi vrednost niske polja između servera i aplikacije.</span><span class="sxs-lookup"><span data-stu-id="43695-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="43695-200">Takođe se koristi za polja tipa **Realni broj** koji su formatirani kao valuta.</span><span class="sxs-lookup"><span data-stu-id="43695-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="43695-201">Za ta polja, svojstvo se koristi za prosleđivanje koda valute aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="43695-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="43695-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="43695-202">dateValue (date)</span></span>

<span data-ttu-id="43695-203">Za polja tipa **Datum** , ovo svojstvo prenosi vrednost datuma polja između servera i aplikacije.</span><span class="sxs-lookup"><span data-stu-id="43695-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="43695-204">Prikažite i sačuvajte prilagođeno polje u odeljku stavke vremenskog rasporeda</span><span class="sxs-lookup"><span data-stu-id="43695-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="43695-205">U nastavku se nalazi snimak ekrana iz aplikacije za mobilne uređaje gde se kreira stavka vremenskog rasporeda.</span><span class="sxs-lookup"><span data-stu-id="43695-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="43695-206">Pokazuje unapred pripremljena polja i prilagođena polja u odeljku „Stavka vremena“ pod nazivom „Test niska“ sa već postavljenom numeričkom vrednošću „Druga opcija“.</span><span class="sxs-lookup"><span data-stu-id="43695-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Prilagođeno polje za testiranje niski u aplikaciji](media/timesheet-entry.jpg)



<span data-ttu-id="43695-208">U nastavku se nalazi snimak ekrana iz aplikacije za mobilne uređaje korisnika koji bira jednu od opcija nabrajanja dostupnih za prilagođeno polje „Test niska“.</span><span class="sxs-lookup"><span data-stu-id="43695-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="43695-209">Dve opcije su „Prva opcija“ i „Druga opcija“, prikazane kao radio dugmad.</span><span class="sxs-lookup"><span data-stu-id="43695-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="43695-210">Trenutno je izabrana druga opcija.</span><span class="sxs-lookup"><span data-stu-id="43695-210">The second option is currently selected.</span></span>

![Dugmad sa opcijama (radio dugmad) za prilagođeno polje Test niska](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="43695-212">Proširite tabelu TSTimesheetLine tako da ima prilagođeno polje</span><span class="sxs-lookup"><span data-stu-id="43695-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="43695-213">U tipičnim scenarijima, verovatno će podaci za prilagođeno polje u odeljku stavke vremenskog rasporeda biti sačuvani u tabeli TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="43695-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="43695-214">Međutim, druge tabele se mogu koristiti ako se podaci mogu dobiti na osnovu TSTimesheetTrans zapisa koji je naveden ili ako nema određeni kontekst zapisa (na primer, ako je polje postavljeno kao samo za čitanje u parametrima projekta).</span><span class="sxs-lookup"><span data-stu-id="43695-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="43695-215">Imajte na umu da prilagođena polja ne moraju imati nikakve prateće zapise baze podataka.</span><span class="sxs-lookup"><span data-stu-id="43695-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="43695-216">Mogu se dinamički generisati na osnovu X++ logike.</span><span class="sxs-lookup"><span data-stu-id="43695-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="43695-217">Ovaj pristup može biti koristan u scenarijima samo za čitanje (pogledajte odeljak „Koristite lanac komandi na klasi TSTimesheetDetails, metodi buildCustomFieldListForHeader za popunjavanje detalja vremenskog rasporeda“ za primer dinamički generisanih vrednosti prilagođenih polja.)</span><span class="sxs-lookup"><span data-stu-id="43695-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="43695-218">U nastavku se nalazi snimak ekrana sa Visual Studio stablom objekata aplikacije.</span><span class="sxs-lookup"><span data-stu-id="43695-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="43695-219">Prikazuje se proširenje tabele TSTimesheetLine sa poljem TestLineString koje je dodato kao prilagođeno polje.</span><span class="sxs-lookup"><span data-stu-id="43695-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Niska linije](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="43695-221">Koristite lanac komandi na metodi buildCustomFieldList klase TSTimesheetSettings da biste prikazali polje u odeljku stavke vremenskog rasporeda</span><span class="sxs-lookup"><span data-stu-id="43695-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="43695-222">Ovaj kôd kontroliše postavke prikaza za polje u aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="43695-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="43695-223">Na primer, kontroliše tip polja, oznaku, da li je polje obavezno i u kom odeljku se polje prikazuje.</span><span class="sxs-lookup"><span data-stu-id="43695-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="43695-224">Sledeći primer prikazuje polje niza za stavke vremena.</span><span class="sxs-lookup"><span data-stu-id="43695-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="43695-225">Ovo polje ima dve opcije, **Prva opcija** i **Druga opcija** , koje su dostupne preko dugmadi opcija (radio dugmadi).</span><span class="sxs-lookup"><span data-stu-id="43695-225">This field has two options, **First option** and **Second option** , that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="43695-226">Polje u aplikaciji je povezano sa poljem **TestLineString** koje se dodaje u tabelu TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="43695-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="43695-227">Obratite pažnju na upotrebu metode **TSTimesheetCustomField::newFromMetatdata()** za pojednostavljivanje inicijalizacije svojstava prilagođenog polja: **fieldBaseType** , **tableName** , **fieldname** , **label** , **isEditable** , **isMandatory** , **stringLength** i **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="43695-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType** , **tableName** , **fieldname** , **label** , **isEditable** , **isMandatory** , **stringLength** , and **numberOfDecimals**.</span></span> <span data-ttu-id="43695-228">Ove parametre možete takođe ručno da podesite kako želite.</span><span class="sxs-lookup"><span data-stu-id="43695-228">You can also set these parameters manually, as you prefer.</span></span>

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="43695-229">Koristite lanac komandi na metodi buildCustomFieldListForEntry klase TSTimesheetEntry da biste unosili vrednosti u stavku vremenskog rasporeda</span><span class="sxs-lookup"><span data-stu-id="43695-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="43695-230">Metoda **buildCustomFieldListForEntry** se koristi za unos vrednosti u sačuvane redove vremenskog rasporeda u aplikaciji za mobilne uređaje.</span><span class="sxs-lookup"><span data-stu-id="43695-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="43695-231">Kao parametar uzima se zapis TSTimesheetTrans.</span><span class="sxs-lookup"><span data-stu-id="43695-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="43695-232">Polja iz tog zapisa mogu se koristiti za popunjavanje vrednosti prilagođenog polja u aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="43695-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

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

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="43695-233">Upotreba lanca komandi u klasi TSTimesheetEntryService radi čuvanja stavke vremenskog rasporeda iz aplikacije nazad u bazu podataka</span><span class="sxs-lookup"><span data-stu-id="43695-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="43695-234">Da biste sačuvali prilagođeno polje u bazu podataka u uobičajenoj upotrebi, morate proširiti više metoda:</span><span class="sxs-lookup"><span data-stu-id="43695-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="43695-235">Metoda **timesheetLineNeedsUpdating** se koristi da bi se utvrdilo da li je korisnik u aplikaciji promenio zapis linije i da li zapis mora da bude sačuvan u bazi podataka.</span><span class="sxs-lookup"><span data-stu-id="43695-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="43695-236">Ako performanse nisu problem, ova metoda se može pojednostaviti tako da se uvek vraća **tačno**.</span><span class="sxs-lookup"><span data-stu-id="43695-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="43695-237">Metode **populateTimesheetLineFromEntryDuringCreate** i **populateTimesheetLineFromEntryDuringUpdate** se mogu proširiti tako da unose vrednosti u zapis baze podataka TSTimesheetLine iz obezbeđenog zapisa TSTimesheetEntry ugovora podataka.</span><span class="sxs-lookup"><span data-stu-id="43695-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="43695-238">U primeru koji sledi obratite pažnju kako se preko X++ koda obavlja ručno mapiranje između polja baze podataka i polja stavke.</span><span class="sxs-lookup"><span data-stu-id="43695-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="43695-239">Metoda **populateTimesheetWeekFromEntry** se takođe može proširiti ako se prilagođeno polje koje se mapira na objekat **TSTimesheetEntry** mora upisati nazad u tabelu baze podataka TSTimesheetLineweek.</span><span class="sxs-lookup"><span data-stu-id="43695-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="43695-240">Sledeći primer čuva vrednost **firstOption** ili **secondOption** koju korisnik bira u bazu podataka kao sirovu vrednost niza.</span><span class="sxs-lookup"><span data-stu-id="43695-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="43695-241">Ako je polje baze podataka polje **Nabrajanje** , te vrednosti se mogu ručno mapirati na vrednost nabrajanja, a zatim sačuvati u polju nabrajanja u tabeli baze podataka.</span><span class="sxs-lookup"><span data-stu-id="43695-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

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

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="43695-242">Prikažite prilagođeno polje u odeljku zaglavlja vremenskog rasporeda</span><span class="sxs-lookup"><span data-stu-id="43695-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="43695-243">U nastavku se nalazi snimak ekrana iz aplikacije za mobilne uređaje gde korisnik pregleda vremenski raspored.</span><span class="sxs-lookup"><span data-stu-id="43695-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="43695-244">U gornjem desnom uglu je izabrano dugme „Više informacija“ da bi se prikazala opcija „Prikaži više detalja“.</span><span class="sxs-lookup"><span data-stu-id="43695-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Komanda Prikaži više detalja](media/show-more.png)

<span data-ttu-id="43695-246">U nastavku se nalazi snimak ekrana iz aplikacije za mobilne uređaje gde se prikazuje odeljak „Još“ vremenskog rasporeda.</span><span class="sxs-lookup"><span data-stu-id="43695-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="43695-247">Prilagođeno polje pod nazivom „Stopa iskorišćenosti ovog vremenskog rasporeda (izračunato prilagođeno polje)“ dodato je u odeljak zaglavlja vremenskog rasporeda.</span><span class="sxs-lookup"><span data-stu-id="43695-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="43695-248">Vrednost samo za čitanje „0,667“ postavljena je u prilagođenom polju.</span><span class="sxs-lookup"><span data-stu-id="43695-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Odeljak „Još“](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="43695-250">Proširite tabelu TSTimesheetTable tako da ima prilagođeno polje</span><span class="sxs-lookup"><span data-stu-id="43695-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="43695-251">U tipičnim scenarijima, verovatno će podaci za prilagođeno polje u odeljku zaglavlja biti povučeni iz tabele TSTimesheetHeader.</span><span class="sxs-lookup"><span data-stu-id="43695-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="43695-252">Međutim, druge tabele se mogu koristiti ako se podaci mogu dobiti na osnovu zapisa TSTimesheetTable koji je naveden ili ako nema određeni kontekst zapisa (na primer, ako je polje postavljeno kao samo za čitanje u parametrima projekta).</span><span class="sxs-lookup"><span data-stu-id="43695-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="43695-253">Imajte na umu da prilagođena polja ne moraju imati nikakve prateće zapise baze podataka.</span><span class="sxs-lookup"><span data-stu-id="43695-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="43695-254">Mogu se dinamički generisati na osnovu X++ logike.</span><span class="sxs-lookup"><span data-stu-id="43695-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="43695-255">Primer koji sledi pokazuje ovaj pristup.</span><span class="sxs-lookup"><span data-stu-id="43695-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="43695-256">Polja u odeljku zaglavlja u aplikaciji su uvek samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="43695-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="43695-257">Koristite lanac komandi na metodi buildCustomFieldList klase TSTimesheetSettings da biste prikazali polje u odeljku zaglavlja vremenskog rasporeda</span><span class="sxs-lookup"><span data-stu-id="43695-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="43695-258">Ovaj kôd kontroliše postavke prikaza za polje u aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="43695-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="43695-259">Na primer, kontroliše tip polja, oznaku, da li je polje obavezno i u kom odeljku se polje prikazuje.</span><span class="sxs-lookup"><span data-stu-id="43695-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="43695-260">Sledeći primer prikazuje izračunatu vrednost u odeljku zaglavlja u aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="43695-260">The following example shows a computed value in the header section in the app.</span></span>

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="43695-261">Koristite lanac komandi na metodi buildCustomFieldListForHeader klase TSTimesheetDetails da biste popunjavali detalje vremenskog rasporeda</span><span class="sxs-lookup"><span data-stu-id="43695-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="43695-262">Metoda **buildCustomFieldListForHeader** se koristi za popunu detalja zaglavlja vremenskog rasporeda u aplikaciji za mobilne uređaje.</span><span class="sxs-lookup"><span data-stu-id="43695-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="43695-263">Kao parametar se uzima zapis TSTimesheetTable.</span><span class="sxs-lookup"><span data-stu-id="43695-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="43695-264">Polja iz tog zapisa mogu se koristiti za popunjavanje vrednosti prilagođenog polja u aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="43695-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="43695-265">Sledeći primer ne čita nijednu vrednost iz baze podataka.</span><span class="sxs-lookup"><span data-stu-id="43695-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="43695-266">Umesto toga, koristi X++ logiku za generisanje izračunate vrednosti koja se zatim prikazuje u aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="43695-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


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

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="43695-267">Ostale mogućnosti prilagodljivosti/proširivosti</span><span class="sxs-lookup"><span data-stu-id="43695-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="43695-268">Dodavanje dodatne provere za aplikaciju</span><span class="sxs-lookup"><span data-stu-id="43695-268">Adding additional validation for the app</span></span>

<span data-ttu-id="43695-269">Postojeća logika za funkcionalnost vremenskog lista na nivou baze podataka i dalje će raditi kako se očekivalo.</span><span class="sxs-lookup"><span data-stu-id="43695-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="43695-270">Da biste prekinuli dovršavanje operacija čuvanja ili slanja i prikazali određenu poruku o grešci, možete da dodate **throw error("poruka korisniku")** u kôd preko lanca dodatka komandi.</span><span class="sxs-lookup"><span data-stu-id="43695-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="43695-271">Slede tri primera korisnih proširivih metoda:</span><span class="sxs-lookup"><span data-stu-id="43695-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="43695-272">Ako **validateWrite** na tabeli TSTimesheetLine vrati **netačno** tokom operacije čuvanja za red vremenskog rasporeda, poruka o grešci se prikazuje u aplikaciji za mobilne uređaje.</span><span class="sxs-lookup"><span data-stu-id="43695-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="43695-273">Ako **validateSubmit** na tabeli TSTimesheetTable vrati **netačno** tokom prosleđivanja vremenskog rasporeda u aplikaciji, korisniku se prikazuje poruka o grešci.</span><span class="sxs-lookup"><span data-stu-id="43695-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="43695-274">Logika koja popunjava polja (na primer, **Svojstvo reda** ) tokom metode **insert** na tabeli TSTimesheetLine i dalje će biti aktivna.</span><span class="sxs-lookup"><span data-stu-id="43695-274">Logic that fills in fields (for example, **Line Property** ) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="43695-275">Sakrivanje i označavanje polja izvan okvira kao samo za čitanje putem konfiguracije</span><span class="sxs-lookup"><span data-stu-id="43695-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="43695-276">Iz parametara projekta možete da napravite unapred pripremljena polja koja su samo za čitanje ili skrivena u aplikaciji za mobilne uređaje.</span><span class="sxs-lookup"><span data-stu-id="43695-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="43695-277">Postavite opcije u odeljku **Mobilni vremenski rasporedi** na kartici **Vremenski raspored** na stranici **Parametri upravljanja projektom i računovodstvom**.</span><span class="sxs-lookup"><span data-stu-id="43695-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Parametri projekta](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="43695-279">Promena aktivnosti koje su dostupne za izbor putem dodataka</span><span class="sxs-lookup"><span data-stu-id="43695-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="43695-280">Aktivnosti koje su na raspolaganju za odabir za projekat popunjavaju se putem metoda **getActivitiesForProject()** i **getActivityQuery()** u klasi **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="43695-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="43695-281">Možete da koristite lanac komandi da biste ovo ponašanje promenili tako da odgovara vašem poslovnom scenariju za aktivnosti koje su dostupne za odabir za određeni projekat.</span><span class="sxs-lookup"><span data-stu-id="43695-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="43695-282">Unos podrazumevane kategorije projekta u stavke vremenskog rasporeda</span><span class="sxs-lookup"><span data-stu-id="43695-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="43695-283">Unos podrazumevane kategorije projekta u stavke vremenskog rasporeda odvija se na tri nivoa.</span><span class="sxs-lookup"><span data-stu-id="43695-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="43695-284">Možete koristiti lanac komandi da proširite ponašanje na bilo kom ili svim ovim nivoima kako biste postigli željeno ponašanje.</span><span class="sxs-lookup"><span data-stu-id="43695-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="43695-285">Koristi se sledeća hijerarhija:</span><span class="sxs-lookup"><span data-stu-id="43695-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="43695-286">Aplikacija pokušava da postavi podrazumevanu kategoriju iz resursa projekta.</span><span class="sxs-lookup"><span data-stu-id="43695-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="43695-287">Ova podrazumevana kategorija je podešena u metodama **getCurrentUserResource** i **getDelegatedResourcesForCurrentUser** u klasi **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="43695-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="43695-288">Ako podrazumevana kategorija nije navedena na nivou resursa projekta, aplikacija pokušava da je povuče iz aktivnosti projekta.</span><span class="sxs-lookup"><span data-stu-id="43695-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="43695-289">Ova podrazumevana kategorija je postavljena u metodi **getActivitiesForProject** u klasi **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="43695-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="43695-290">Ako podrazumevana kategorija nije navedena na nivou aktivnosti projekta, podrazumevana kategorija se preuzima iz parametara projekta.</span><span class="sxs-lookup"><span data-stu-id="43695-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="43695-291">Ova podrazumevana kategorija se postavlja u metodi **getProjectDetailsbyRule** u klasi **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="43695-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
