---
title: Integracija faktura projekta
description: Ova tema pruža informacije o integraciji fakturisanja klijenta u Project Operations pomoću dvostrukog upisivanja.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1e7294360f041b030efca225c6754fe3bbc0eadf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581255"
---
# <a name="project-invoice-integration"></a>Integracija faktura projekta

Ova tema pruža informacije o integraciji fakturisanja klijenta u Project Operations pomoću dvostrukog upisivanja.

U Project Operations, menadžer projekta upravlja zaostatkom u fakturisanju projekata i kreira predračun za klijenta u Microsoft Dataverse. Na osnovu ove predračune, službenik za potraživanja ili knjigovođa na projektu kreira fakturu prema klijentima. Integracija sa dva pisanja obezbeđuje da se detalji proforma fakture sinhronizuju sa aplikacijama za finansije i operacije. Nakon što se knjiži faktura za klijenta, sistem ažurira relevantne činjenice o projektu u Dataverse sa detaljima računovodstva. Sledeća grafika daje konceptualni pregled ove integracije na visokom nivou.

   ![Integracija faktura projekta.](./media/DW5Invoicing.png)

Nakon što menadžer projekta potvrdi proforma fakturu Dataverse u programu, informacije o zaglavlju proforma fakture sinhronizuju se sa aplikacijama za finansije i operacije koristeći mapu tabele za dvostruko pisanje, **predlog fakture projekta V2 (fakture)**. Ovo je jednosmerna integracija iz aplikacija Dataverse za finansije i operacije. Kreiranje ili brisanje predloga faktura projekta direktno u aplikacijama za finansije i operacije nije podržano.

Potvrda računa u Dataverse takođe pokreće poslovnu logiku za kreiranje zapisa povezanih sa naplatom u entitetu **Stvarni podaci**. Ovi zapisi se sinhronizuju sa "Finansije" i "Operacije" koristeći mapu tabele sa dva pisanja, **stvarne integracije projektnih operacija (msdyn\_ stvarne).** Više informacija potražite u članku [Procene i stvarne vrednosti](resource-dual-write-estimates-actuals.md). 

Redovi za predlog fakture za projekat kreiraju se periodičnim procesom, **Postupak uvoza obrasca**. Ovaj proces se zasniva na stvarnim detaljima fakturisane prodaje u tabeli **Priprema stvarnih podataka**. Za više informacija pogledajte [Upravljajte predlozima faktura za projekat](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
