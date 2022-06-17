---
title: Integracija faktura projekta
description: Ovaj članak pruža informacije o integraciji dvostrukog pisanja operacija projekta za fakturisanje klijenata.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ee2d78f1ca1d78f6909d9995a92ac301f06d6a6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912119"
---
# <a name="project-invoice-integration"></a>Integracija faktura projekta

Ovaj članak pruža informacije o integraciji dvostrukog pisanja operacija projekta za fakturisanje klijenata.

U Project Operations, menadžer projekta upravlja zaostatkom u fakturisanju projekata i kreira predračun za klijenta u Microsoft Dataverse. Na osnovu ove predračune, službenik za potraživanja ili knjigovođa na projektu kreira fakturu prema klijentima. Integracija sa dva pisanja obezbeđuje da se detalji proforma fakture sinhronizuju sa aplikacijama za finansije i operacije. Nakon što se knjiži faktura za klijenta, sistem ažurira relevantne činjenice o projektu u Dataverse sa detaljima računovodstva. Sledeća grafika daje konceptualni pregled ove integracije na visokom nivou.

   ![Integracija faktura projekta.](./media/DW5Invoicing.png)

Nakon što menadžer projekta potvrdi proforma fakturu Dataverse u programu, informacije o zaglavlju proforma fakture sinhronizuju se sa aplikacijama za finansije i operacije koristeći mapu tabele za dvostruko pisanje, **predlog fakture projekta V2 (fakture)**. Ovo je jednosmerna integracija iz aplikacija Dataverse za finansije i operacije. Kreiranje ili brisanje predloga faktura projekta direktno u aplikacijama za finansije i operacije nije podržano.

Potvrda računa u Dataverse takođe pokreće poslovnu logiku za kreiranje zapisa povezanih sa naplatom u entitetu **Stvarni podaci**. Ovi zapisi se sinhronizuju sa "Finansije" i "Operacije" koristeći mapu tabele sa dva pisanja, **stvarne integracije projektnih operacija (msdyn\_ stvarne).** Više informacija potražite u članku [Procene i stvarne vrednosti](resource-dual-write-estimates-actuals.md). 

Redovi za predlog fakture za projekat kreiraju se periodičnim procesom, **Postupak uvoza obrasca**. Ovaj proces se zasniva na stvarnim detaljima fakturisane prodaje u tabeli **Priprema stvarnih podataka**. Za više informacija pogledajte [Upravljajte predlozima faktura za projekat](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
