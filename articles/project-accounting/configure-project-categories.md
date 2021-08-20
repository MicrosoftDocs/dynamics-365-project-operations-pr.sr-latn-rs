---
title: Konfigurisanje kategorija projekta
description: Ova tema pruža informacije o podešavanju kategorija projekata.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: cea43422469adf12f336f7686814a8199717090c18804d3d0a7509452349566e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997128"
---
# <a name="configure-project-categories"></a>Konfigurisanje kategorija projekta

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Usluga Project Operations nudi snažne mogućnosti za kategorizaciju prihoda i troškova na projektima. Kategorije pružaju mogućnost izveštavanja o projektnim transakcijama i sprovode knjiženje u glavnu knjigu.

Sledeći dijagram ilustruje korelaciju između kategorija transakcija, deljenih kategorija i kategorija projekata. 

Kategorije transakcija su osnovno grupisanje za projektne transakcije. Unutar te grupacije postoji skup deljenih kategorija koje se mogu deliti između aplikacija i modula. Ulazeći još dalje u detalje, kategorije projekata su najosnovniji nivo kategorija. Kategorije projekata su specifične za pravno lice, modul i aplikaciju.

![Korelacija između kategorija transakcija, deljenih kategorija i kategorija projekata.](media/project-categories.png)

## <a name="transaction-categories"></a>Kategorije transakcija

Kategorije transakcija predstavljaju osnovno grupisanje za projektne transakcije i nisu specifične za preduzeće ili tip transakcije. Na primer, Contoso Robotics koristi kategorije Dizajn, Putovanje, Instalacija i Uslužne transakcije za grupisanje projektnih transakcija.

Kategorije transakcija definisane su u modulu usluge Project Operations. 
1. Idite na **Podešavanja** \> **Kategorije transakcija** da otvorite obrazac. 
2. Kreirajte novu kategoriju transakcija bilo izborom **Nova** ili izborom **Uvezi iz Excel tabele**.

## <a name="shared-categories"></a>Deljene kategorije

Dynamics 365 koristi koncept deljenih kategorija za kategorizaciju troškova u različitim aplikacijama, kao što su Dynamics 365 Finance, Dynamics 365 Supply Chain i Dynamics 365 Project Operations. Za svaku kreiranu kategoriju transakcija, Project Operations automatski kreira četiri povezane deljene kategorije: Sati, Troškovi, Naknade i Stavka. Možete da pregledate i prilagodite deljene kategorije tako što ćete otići na **Upravljanje projektima i računovodstvo** \> **Podešavanje** \> **Kategorije** \> **Deljene kategorije**.

## <a name="project-categories"></a>Kategorije projekata

Kategorije projekata predstavljaju najosnovniji nivo konfiguracije kategorija i moraju se konfigurisati odvojeno i za svako preduzeće, po računovođi projekta.

1. Idite na **Upravljanje projektima i računovodstvo** \> **Podešavanje** \> **Kategorije** \> **Kategorije projekata**.
2. Izaberite **Novo**.
3. Izaberite **ID kategorije** deljene kategorije koju ste kreirali u prethodnom odeljku. Project Operations omogućava upotrebu samo onih zajedničkih kategorija koje su povezane sa kategorijama transakcija.
4. Izaberite grupu kategorija.

## <a name="category-groups"></a>Grupe kategorija

Grupe kategorija koriste se za deljenje svojstava, pre svega profila za knjiženje, između povezanih kategorija projekta. Za svaku vrstu transakcije mora postojati najmanje jedna grupa kategorija, a svakoj kategoriji projekta dodeljena je grupa.

Specifikacije knjiženja u usluzi Project Operations definisane su pravilima profila troškova i prihoda projekta, kategorijama projekata i grupama kategorija. Možete da podesite grupe kategorija ako odete na **Upravljanje projektima i računovodstvo** \> **Podešavanje** \> **Kategorije** \> **Grupe kategorija**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]