---
title: Odredite vrstu primene
description: Ova tema pruža informacije koje vam pomažu da utvrdite pravilan tip primene usluge Project Operations za vaše preduzeće.
author: stsporen
ms.date: 03/15/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 4be8e69c5b6ff1ed65e9484a9b427bb428f7ff3e6dc597c615d5586da52867ef
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994653"
---
# <a name="determine-your-deployment-type"></a>Odredite vrstu primene

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

> [!IMPORTANT]
> Nakon kupovine licence, počnite ovde da biste utvrdili najbolji model primene za Dynamics 365 Project Operations pomoću [Vođenog toka instalacije](https://aka.ms/provisionprojectoperations).
> Kada dovršite vođeni tok instalacije, bićete preusmereni na pravi portal za upravljanje da biste dovršili instalaciju. Pogledajte detalje o primeni da biste dovršili instalaciju.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Postojeći klijenti sistema Dynamics koji koriste Dynamics 365 Project Service Automation
Project Operations uključuje mogućnosti koje su isporučene sa uslugom Project Service Automation. Putanja nadogradnje će biti objavljena za ove klijente u 1. talasu izdanja za 2021. godinu.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Postojeći klijenti usluge Dynamics 365 Finance koji koriste upravljanje projektima i računovodstvo 

Postojeći klijenti usluge Finance koji koriste funkcionalnost upravljanja projektima i računovodstva mogu da nastave da je koriste onakvu kakva jeste. Pogledajte [Project Operations za scenarije zasnovane na zalihama/proizvodnji](#pma).


## <a name="deployment-regions"></a>Regioni primene
Da biste utvrdili koji regioni podržavaju primenu usluge Project Operations, pogledajte odeljak [Geografska dostupnost za Dynamics 365 i Power Platform izveštaj](https://dynamics.microsoft.com/en-us/geographic-availability/). Izaberite **Prikaži izveštaj** i proširite odeljak **Dynamics 365 > Operations Apps > Dynamics 365 Project Operations** da biste videli podržane regione.

## <a name="deployment-types"></a>Tipovi primene
Project Operations podržava više mogućnosti primene u skladu sa vašim zahtevima. Bez obzira na to da li ste novi ili postojeći klijent sistema Dynamics 365, Project Operations može podržati vaše potrebe.

Naš [upitnik za primenu](https://aka.ms/provisionprojectoperations) će vam pomoći da odredite odgovarajuću primenu. Rezultati će vas voditi prema jednom od sledećih tipova primene:

- [Jednostavna primena – od pogodbe do profakture](#lite)
- [Project Operations za scenarije sa resursima/materijalima koji nisu na zalihama](#integrated)
- [Project Operations za scenarije sa materijalima na zalihama/porudžbinama za proizvodnju](#pma)

Project Operations podržavaju scenarije zaliha / proizvodnih naloga i scenarije zasnovane na resursima / bez zaliha u istom okruženju putem konfiguracija na nivou pravnog lica. Na primer, Contoso može da koristi mogućnosti skladištenja / narudžbine za proizvodnju u svom proizvodnom pogonu u SAD (pravno lice = Contoso Manufacturing United States). Contoso može da koristi mogućnosti bez zaliha / zasnovane na resursima u svom Contoso objektu za servisiranje robotičkog oružja u Ujedinjenom Kraljevstvu (pravno lice = Contoso Robotics United Kingdom).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Jednostavna primena – od pogodbe do profakture

Jednostavna primena uključuje sledeće mogućnosti:

- Proces prodaje za projekte koji proširuju iskustva aplikacije Dynamics 365 Sales
- Planiranje projekata koristeći Microsoft Project za veb
- Višedimenzionalno određivanje cena
- Objedinjeno upravljanje resursima
- Praćenje vremena
- Osnovni trošak
- Predračun za pregled i izmene od strane rukovodioca projekta 

#### <a name="deployment-steps"></a>Koraci primene
Odredite najbolji model primene usluge Project Operations pomoću [upitnika za primenu](https://aka.ms/provisionprojectoperations).

Za ovo raspoređivanje, pogledajte članak [Prijava za pretplate na pregled](lite-preview-subscription-sign-up.md) i [Obezbeđivanje novog okruženja](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations za scenarije sa resursima/materijalima koji nisu na zalihama
Project Operations za scenarije resursa / bez zaliha uključuju sledeće mogućnosti:
 
- Proces prodaje za projekte koji proširuju aplikaciju Dynamics 365 Sales
- Planiranje projekata koristeći Microsoft Project za veb
- Višedimenzionalno određivanje cena
- Objedinjeno upravljanje resursima
- Praćenje vremena
- Osnovni trošak
- Puni trošak
- OCR priznanice
- Izdavanje predračuna i faktura u okruženju klijenta 
- Priznavanje prihoda za projekte

#### <a name="deployment-steps"></a>Koraci primene
Odredite najbolji model primene usluge Project Operations pomoću [upitnika za primenu](https://aka.ms/provisionprojectoperations).

Za ovo raspoređivanje, pogledajte članak [Prijava za pretplate na pregled](resource-sign-up-preview-subscription.md) i [Obezbeđivanje novog okruženja](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations za scenarije sa materijalima na zalihama/porudžbinama za proizvodnju

- Planiranje projekta korišćenjem SAP
- Upravljanje resursima
- Praćenje vremena
- Puni trošak
- OCR priznanice
- Potpuno fakturisanje
- Prepoznavanje prihoda
- Nalozi za proizvodnju
- Podrška zaliha materijala sa inventarom

#### <a name="deployment-steps"></a>Koraci primene
Odredite najbolji model primene usluge Project Operations pomoću [upitnika za primenu](https://aka.ms/provisionprojectoperations).

Za ovo raspoređivanje, pogledajte članak [Prijava za pretplate na pregled](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) i [Obezbeđivanje novog okruženja](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]