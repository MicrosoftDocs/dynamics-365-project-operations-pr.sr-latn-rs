---
title: Integracija faktura projekta
description: Ovaj članak pruža informacije o integraciji fakturisanja klijenta u Project Operations pomoću dvostrukog upisivanja.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61f16ebdbabd6545c09d8d7bd82d99b85dc09975
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029041"
---
# <a name="project-invoice-integration"></a>Integracija faktura projekta

Ovaj članak pruža informacije o integraciji fakturisanja klijenta u Project Operations pomoću dvostrukog upisivanja.

U Project Operations, menadžer projekta upravlja zaostatkom u fakturisanju projekata i kreira predračun za klijenta u Microsoft Dataverse. Na osnovu ove predračune, službenik za potraživanja ili knjigovođa na projektu kreira fakturu prema klijentima. Integracija dvostrukog pisanja osigurava da se detalji predračuna sinhronizuju sa aplikacijama za finansije i aplikacije. Nakon što se knjiži faktura za klijenta, sistem ažurira relevantne činjenice o projektu u Dataverse sa detaljima računovodstva. Sledeća grafika daje konceptualni pregled ove integracije na visokom nivou.

   ![Integracija faktura projekta.](./media/DW5Invoicing.png)

Nakon što menadžer projekta potvrdi predračun u Dataverse, informacije o zaglavlju predračuna se sinhronizuju sa aplikacijama za finansije i operacije koje koriste mapu tabela dvostrukog upisivanja, **Predlog projektne fakture V2 (fakture)**. Ovo je jednosmerna integracija iz usluge Dataverse u aplikacije za finansije i operacije. Kreiranje ili brisanje predloga projektnih faktura direktno u aplikacijama za finansije i operacije nije podržano.

Potvrda računa u Dataverse takođe pokreće poslovnu logiku za kreiranje zapisa povezanih sa naplatom u entitetu **Stvarni podaci**. Ovi zapisi se sinhronizuju sa aplikacijama za finansije i aplikacijekkoje koriste mapu **Stvarni podaci o Project Operations integraciji (msdyn\_actuals).** Više informacija potražite u članku [Procene i stvarne vrednosti](resource-dual-write-estimates-actuals.md). 

Redovi za predlog fakture za projekat kreiraju se periodičnim procesom, **Postupak uvoza obrasca**. Ovaj proces se zasniva na stvarnim detaljima fakturisane prodaje u tabeli **Priprema stvarnih podataka**. Za više informacija pogledajte [Upravljajte predlozima faktura za projekat](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
