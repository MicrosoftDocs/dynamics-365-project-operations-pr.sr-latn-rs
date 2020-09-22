---
title: Podešavanja projekta
description: Ova tema pruža informacije o podešavanjima upravljanja projektima.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 7c5be6ff-8f92-4dfc-9f9d-4abc76f96638
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 843192092598fd713b3bc59bf90c5362d0dad8b4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755141"
---
# <a name="project-settings"></a>Podešavanja projekta

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Za pristup funkcijama planiranja projekata koristite sledeća podešavanja.

## <a name="work-template"></a>Radni predložak

Da biste kreirali raspored projekta, kreirajte predložak kalendara projekta koji definiše broj radnih sati po danu i sve prekide poslovnih aktivnosti. Da biste kreirali predložak kalendara projekta, radni predložak povezujete sa poljem **Predložak kalendara** za projekat. Sledite ove korake za kreiranje radnog predloška.

1. U aplikaciji PSA, u levom navigacionom oknu, kliknite na **Resursi**. 
2. Na stranici liste **Resursi** otvorite zapis korisnika, a zatim izaberite **Prikaži radno vreme**.

  > [!NOTE]
  > Obavezno dozvolite iskačuće prozore na stranici pregledača. Ovo vam omogućava da vidite radno vreme podešeno za resurs.
  
3. Na kartici **Mesečni prikaz** kliknite na **Podešavanje**. Pojaviće se lista sa tri opcije: 

  - Novi sedmični raspored
  - Raspored posla za jedan dan
  - Slobodni dani

> ![Podešavanje opcija](media/project-13.png)

4. Izaberite **Novi sedmični raspored**, a zatim podesite opcije za ovaj raspored resursa. Možete podesiti periodični sedmični raspored, parametre sata u danu, prekid poslovnih aktivnosti i još mnogo toga.
5. Podesite opseg datuma, izaberite **Sačuvaj**, a zatim kliknite na **Zatvori**. 
6. Vratite se na stranicu liste **Resursi** i odaberite resurs za koji ste odredili radno vreme. 
7. Izaberite **Podesite kalendar kao** da podesite radni predložak. 
8. U dijalog **Radni predložak** unesite ime radnog predloška, a zatim izaberite **Primeni**. 

Sada možete povezati radni predložak sa predloškom kalendara projekta.

## <a name="resource-roles"></a>Uloge resursa

Termin *uloga resursa* odnosi se na skup veština, kompetencija i certifikacije koje osoba mora imati da bi mogla da obavlja određeni skup zadataka u projektu. PSA vam omogućava da odredite troškove i naplatite vreme resursa na osnovu uloge sa kojom je resurs povezan. Svaka organizacija mora podesiti ove uloge koristeći levu navigaciju u meniju **Project Service**.

Svaka organizacija mora podesiti ove uloge na stranici **Aktivne kategorije resursa**. Da biste otvorili ovu stranicu, u levom navigacionom oknu izaberite **Uloge resursa**.

## <a name="price-lists"></a>Cenovnici

Cenovnici vam omogućavaju da podesite cene koštanja i prodajne cene za uloge resursa, kategorije troškova, proizvode i druge elemente u organizaciji. Da biste mogli da podesite finansijske procene za posao koji mora da se obavi za projekat, treba da kreirate odgovarajuću listu troškova i cenovnik prodaje. U odeljku sa parametrima treba da podesite i podrazumevani cenovnik troškova i prodajni cenovnik koji se odnosi na sve projekte kreirane u organizaciji. Na stranici **Aktivni parametri projekta** proverite da li ste podesili podrazumevani cenovnik troškova i prodajni cenovnik.
