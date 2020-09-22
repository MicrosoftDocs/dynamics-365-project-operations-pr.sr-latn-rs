---
title: Promene entiteta, kontrola i korisničkog interfejsa (Project Service Automation 3.x)
description: Ova tema opisuje promene rešenja za Microsoft Dynamics Project Service Automation 3.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 9f8828c6-541c-4945-8c99-5785118e191d
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
ms.openlocfilehash: 56aa0bb8272b886bcd15dadd0f74fff3bc43e26b
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755195"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Promene entiteta, kontrola i korisničkog interfejsa (Project Service Automation 3.x)
Uz izdanje Microsoft Dynamics Project Service Automation (PSA) 3.x, izvršene su mnoge promene u entitetima, kontrolama, prikazima i korisničkom interfejsu. Ova tema pruža informacije o ovim važnim promenama.

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>Odnosi nadređenih i podređenih entiteta za dokument prodaje, stavku dokumenta prodaje, detalji stavke dokumenta prodaje
U verzijama aplikacije Dynamics 365 Project Service Automation (PSA) koje su objavljene pre verzije 3.0, neki od odnosa između entiteta dokumenata prodaje, stavki dokumenata prodaje i detalja stavke dokumenata prodaje implementirani su kroz polja niske koja su evidentirala prikaz niske za GUID povezanog entiteta. Do ovoga je dolazilo zbog ograničenja platforme koja je zahtevala značajni deo prilagođenog koda na strani servera, kao i na strani klijenta rešenja da bi ti odnosi radili slično tipičnom odnosu između Dynamics CRM entiteta i da bi se polja niske ponašala kao polja za pronalaženje.

PSA 3.0 je ažuriran tako da koristi nove odnose između entiteta dokumenata prodaje i stavke dokumenta prodaje.

S obzirom na to da polja za pronalaženje mogu da se koriste za označavanje referenci na entitete, polja koja su skladištila vrednost niske za GUID povezanog entiteta u prethodnim verzijama više nisu potrebna i zato su zastarela. Prilagođeni kôd na strani klijenta i servera koji rukuje odnosima definisanim u zastarelim poljima niske takođe je zastareo.

### <a name="entity-schema-changes"></a>Promene šema entiteta
Sledeća tabela pruža listu „jedan na jedan“ zastarelih polja niske i novih polja za pronalaženje entiteta. 

 Entitet |   Zastarelo polje (niska) | Novo polje (pronalaženje)
--- | --- | ---
invoicedetail (stavka fakture) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (stvarna vrednost) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (Raspored fakturisanja za predmet ugovora za projekat) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (Kontrolna tačka predmeta ugovora za projekat) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (činjenica) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (Detalj stavke fakture) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (stavka u glavnoj knjizi) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (Kategorija resursa za predmet ugovora za projekat) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (Detalj predmeta ugovora za projekat) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (Kategorija transakcije za predmet ugovora za projekat) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (Klasifikacija transakcija za predmet ugovora za projekat) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (Raspored fakturisanja stavki ponude) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (Kategorija resursa stavke ponude) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (Kontrolna tačka stavke ponude) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (Detalj stavke ponude) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (Kategorija transakcije stavke ponude) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (Klasifikacija transakcije stavke ponude) |  msdyn_quoteline |   msdyn_quotelineid
Detalj ulazne porudžbine (stavka porudžbine) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Zastareli prilagođeni prikazi i kontrole
Sledeći prilagođeni prikazi i kontrole i njihovi povezani artefakti su zastareli.

- Prikaz naplativosti.
- Prilagođene kontrole mreže za prikazivanje detalja stavke ponude na stranici sa **informacijama o projektu** za stavku ponude.
- Prilagođene kontrole mreže za prikazivanje detalja predmeta ugovora o projektu na stranici sa **informacijama o projektu** za stavku ulazne porudžbine.

> [!NOTE]
> Za kompletnu listu zastarelih resursa, pogledajte [Zastareli veb-resursi u aplikaciji Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md)

## <a name="unified-client-interface-app-module"></a>Modul aplikacije za objedinjeni klijentski interfejs
Uz uvođenje modula za aplikacije objedinjenog klijentskog interfejsa, PSA unosi o mapi lokacije su uklonjeni iz sistema.  
Funkcionalnost koja se odnosi na prebacivanje obrazaca za entitete Mogućnost za poslovanje, Ponuda, Porudžbina, Faktura je zastarela pošto više nije potrebna, jer modul za aplikaciju objedinjenog klijentskog interfejsa uključuje samo PSA verzije obrazaca.  

Sledeći veb-resursi su zastareli:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\Dokument prodaje\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> Za kompletnu listu zastarelih resursa, pogledajte [Zastareli veb-resursi u aplikaciji Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md).


