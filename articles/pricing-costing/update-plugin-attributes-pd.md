---
title: Ažuriranje atributa dodatnih komponenti sa novim aspektima za određivanje cena
description: Ova tema pruža informacije o tome kako da ažurirate atribute dodatnih komponenti za dimenzije određivanja cena.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b3b441b9ea0418e10db80a86613b2c41ea2c4673
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575045"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Ažurirajte atribute dodatnih komponenti sa novim aspektima za određivanje cena

Ova tema pruža informacije o tome kako da ažurirate atribute dodatnih komponenti za dimenzije određivanja cena.

> [!NOTE]
> Ova tema je primenljiva samo na funkcije ponude i ugovora u usluzi Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Preduslovi
Pre nego što dovršite korake u ovoj temi, morate dovršiti procedure u sledećim temama:

  - [Kreiranje prilagođenih polja i entiteta](create-custom-fields-entities-pricing-dimensions.md) 
  - [Dodavanje prilagođenih polja u podešavanje cena i entitete transakcije ](add-custom-fields-price-setup-transactional-entities.md)
  - [Podešavanje prilagođenih polja kao dimenzija za određivanje cena](set-up-custom-fields-pricing-dimensions.md). 
  
Ako niste dovršili te procedure, dovršite ih, a zatim se vratite na ovu temu.

## <a name="register-a-plug-in"></a>Registrovanje dodatne komponente
Kada kreirate detalj stavke ponude na stranici **Stavka ponude** za stavku ponude projekta, sistem kreira dve stavke procene. Jedna stavka je za troškovnu stranu procene, a druga stavka za prodajnu stranu. Ovo je isto za predmete ugovora o projektu.

Kada promenite količinu ili polje na strani troškova, ta promena se vrši i na strani prodaje. To je moguće jer dodatne komponente PreOperation na Quotelinedetail i stavkama detalja za contractline povezuju određene atribute na troškovnoj strani sa prodajnom stranom transakcije. Ako su vam potrebne izmene vrednosti dimenzija formiranja cena na prodajnoj strani da bi se izvršile i na troškovnoj strani, sledeće dodatne komponente moraju da se ponovo registruju nakon unošenja promena u dimenziju formiranja cene.

Ovo su dodatne komponente za ažuriranje i ponovnu registraciju:

- PreOperationContractLineDetailUpdate – **Update msdyn_orderlinetransaction**
- PreOperationQuoteLineDetailUpdate – **Updates msdyn_quotelinetransaction**

Dovršite sledeće korake da biste ažurirali i ponovo registrovali dodatne komponente.

1. Otvorite **PluginRegistrationTool** i povežite se sa svojim Project Operations Dataverse okruženjem.
2. Izaberite **Pretraga** i otkucajte prvih nekoliko slova dodatne komponente koji treba da se ažurira.
3. Nakon što pronađete dodatnu komponentu, izaberite je, a zatim izaberite **Izaberi u glavnom obrascu**.
4. Izaberite korak **Ažuriraj msdyn_orderlinetransaction**, kliknite desnim tasterom i izaberite **Ažuriraj**.
5. Na stranici sa dijalogom **Ažuriraj** , izaberite tri tačke (**...**) u atributima filtriranja.
6. Otvara se prozor filtriranja atributa i navodi spisak svih atributa u entitetu i dimenzijama formiranja cena. Izaberite polja za potvrdu za atribute dimenzije formiranja cena.
7. Izaberite **U redu** da zatvorite stranicu, a zatim izaberite **Ažuriraj korak**.
8. Ponovite korake od 2-7 za drugu dodatnu komponentu, **PreOperationQuoteLineDetail**. Za ovu dodatnu komponentu, morate da ažurirate korak **Update of msdyn_quotelinetransaction**.
9. Zatvorite **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]