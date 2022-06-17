---
title: Ažuriranje atributa dodatnih komponenti sa novim aspektima za određivanje cena
description: Ovaj članak pruža informacije o ažuriranju atributa dodatne komponente za dimenzije cena.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2ae502fea533d9f199ef5ee1cc85b623f08cbd84
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920031"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Ažurirajte atribute dodatnih komponenti sa novim aspektima za određivanje cena

Ovaj članak pruža informacije o ažuriranju atributa dodatne komponente za dimenzije cena.

> [!NOTE]
> Ovaj članak je primenljiv samo na funkcije ponude i ugovora u programu Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Preduslovi
Pre nego što dovršite korake iz ovog članka, morate dovršiti procedure u sledećim člancima:

  - [Kreiranje prilagođenih polja i entiteta](create-custom-fields-entities-pricing-dimensions.md) 
  - [Dodavanje prilagođenih polja u podešavanje cena i entitete transakcije ](add-custom-fields-price-setup-transactional-entities.md)
  - [Podešavanje prilagođenih polja kao dimenzija za određivanje cena](set-up-custom-fields-pricing-dimensions.md). 
  
Ako niste dovršili te procedure, dovršite ih, a zatim se vratite na ovaj članak.

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