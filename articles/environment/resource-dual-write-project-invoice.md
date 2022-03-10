---
title: Integracija faktura projekta
description: Ova tema pruža informacije o integraciji fakturisanja klijenta u Project Operations pomoću dvostrukog upisivanja.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 37549080d76e3bffd7cb002aee8e3c46b9eeb18e3cec915cd971881b69747534
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993258"
---
# <a name="project-invoice-integration"></a>Integracija faktura projekta

Ova tema pruža informacije o integraciji fakturisanja klijenta u Project Operations pomoću dvostrukog upisivanja.

U Project Operations, menadžer projekta upravlja zaostatkom u fakturisanju projekata i kreira predračun za klijenta u Microsoft Dataverse. Na osnovu ove predračune, službenik za potraživanja ili knjigovođa na projektu kreira fakturu prema klijentima. Integracija dvostrukog pisanja osigurava da se detalji predračuna sinhronizuju sa Finance and Operations aplikacijama. Nakon što se knjiži faktura za klijenta, sistem ažurira relevantne činjenice o projektu u Dataverse sa detaljima računovodstva. Sledeća grafika daje konceptualni pregled ove integracije na visokom nivou.

   ![Integracija faktura projekta.](./media/DW5Invoicing.png)

Nakon što menadžer projekta potvrdi predračun u Dataverse, informacije o zaglavlju predračuna se sinhronizuju sa Finance and Operations aplikacijama koje koriste mapu tabela dvostrukog upisivanja, **Predlog projektne fakture V2 (fakture)**. Ovo je jednosmerna integracija iz Dataverse do Finance and Operations aplikacija. Kreiranje ili brisanje predloga projektnih faktura direktno u Finance and Operations aplikacijama nije podržano.

Potvrda računa u Dataverse takođe pokreće poslovnu logiku za kreiranje zapisa povezanih sa naplatom u entitetu **Stvarni podaci**. Ovi zapisi se sinhronizuju sa Finance and Operations aplikacijama koje koriste mapu **Stvarni podaci o Project Operations integraciji (msdyn\_actuals).** Više informacija potražite u članku [Procene i stvarne vrednosti](resource-dual-write-estimates-actuals.md). 

Redovi za predlog fakture za projekat kreiraju se periodičnim procesom, **Postupak uvoza obrasca**. Ovaj proces se zasniva na stvarnim detaljima fakturisane prodaje u tabeli **Priprema stvarnih podataka**. Za više informacija pogledajte [Upravljajte predlozima faktura za projekat](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
