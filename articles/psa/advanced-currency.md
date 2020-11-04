---
title: Scenariji sa više valuta (verzija 3.x)
description: Ova tema pruža informacije o scenarijima sa više valuta.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 7be029eeca3129d30f4bec1bf9b180a0a5122a86
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083690"
---
# <a name="multiple-currency-scenarios"></a>Scenariji sa više valuta

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 ima dva koncepta valute:

- **Valuta transakcije** - Valuta u kojoj se događa transakcija. 
- **Osnovna valuta** - Valuta Dynamics 365 instance. Ova valuta se podešava posle obezbeđivanja Dynamics 365 instance. Ne može da se promeni.

Na primer, Contoso US je prodao 100 majici klijentu u Velikoj Britaniji za po 15 funti (GBP). Sledeća tabela prikazuje kako se ova transakcija beleži u entitetu proizvoda porudžbine.

| Proizvod | Količina | Cena po jedinici | Valuta | Iznos | Kurs valute | Cena po jedinici (osnovna)| Iznos (osnovni)|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| Majica | 100.      | 15             | GBP      | 1500   | 0.94          | 17,25 USD               | 1725 USD       |

U koloni **Valuta** se prikazuje valuta transakcije, tj. valuta u kojoj je obavljena prodaja. Kolona **Kurs valute** prikazuje kurs valute transakcije u odnosu na osnovnu valutu. Osnovna valuta je američki dolar (USD). Osnovna valuta je podešena posle obezbeđivanja Dynamics 365 instance.
Kao što tabela pokazuje, svaka transakcija se evidentira u valuti transakcije i osnovnoj valuti. Dynamics 365 koristi kurs valute za izračunavanje iznosa osnovne valute.

## <a name="project-service-automation-extensions"></a>Project Service Automation proširenja

Dynamics 365 Project Service Automation utiče na valutu transakcije jer poslovne transakcije obično imaju dva aspekta: troškove i prodaju.

Za poslovne transakcije smatraju se sledeći entiteti:

- Detalj stavke ponude
- Detalj predmeta ugovora za projekat
- Stavka procene
- Stavka u glavnoj knjizi
- Detalj stavke fakture
- Stvarno

U svakom od ovih entiteta postoji zapis koji predstavlja iznos troškova ili iznos prodaje. Kao i za svaki Dynamics 365 entitet koji ima polje **Iznos** , svaki zapis uključuje iznose u valuti transakcije i osnovnoj valuti. 

PSA širi koncept valute transakcije za troškove i prodaju na sledeće načine:

- Valuta transakcije troškova za transakcije vremena uvek dolazi iz valute organizacione jedinice koja je vlasnik projekta ili upravlja projektom. Ova organizaciona jedinica poznata je kao ugovorna jedinica.
- Valuta prodajne transakcije za transakcije vremena i troškova uvek dolazi iz valute projektnog ugovora.
- Valuta troškova transakcije za troškove dolazi iz valute u kojoj je kreirana stavka troška.

## <a name="multiple-currency-scenario"></a>Scenario sa više valuta

Ovaj odeljak opisuje primer projekta koji Contoso UK isporučuje klijentu Fabrikam iz Japana. Evo kako je podešen scenario:

1. GBP i japanski jen (JPY) su podešeni u delu **Podešavanja** \> **Upravljanje poslovanjem** \> **Valute**. 
2. Poslovni kontakt klijenta pod nazivom **Fabrikam - Japan** se podešava i JPY se bira kao valuta poslovnog kontakta.
3. Organizaciona jedinica koja se zove **Contoso UK** se podešava i GBP se bira kao valuta.
4. Kreira se projektni ugovor, gde se **Contoso UK** navodi kao ugovorna jedinica, a **Fabrikam - Japan** kao klijent.
5. Predmet ugovora o projektu se kreiraju na osnovu aranžmana naplate za različite klase transakcija na projektu, kao što su naplata vremena u odnosu na naplatu troškova.
6. Projekat se kreira, a **Contoso UK** se navodi kao ugovorna jedinica. Ovaj projekat je kreiran i mapiran u predmetu ugovora za projekat.


Tokom procene koja koristi detalj stavke ponude, detalj predmeta ugovora za projekat ili stavku procene rasporeda, u entitetu se uvek kreiraju dva zapisa. Jedan zapis je za troškove, a drugi za prodaju.

- Podrazumevano se valuta transakcije u zapisu troškova podešava na valutu ugovorne jedinice projekta. U ovom primeru, valuta je GBP.
- Podrazumevano se valuta transakcije u zapisu prodaje podešava na valutu ugovora za projekat. U ovom primeru, valuta je JPY.

Kada se stvarne vrednosti kreiraju za vreme pomoću stavke vremena ili stavke u glavnoj knjizi, dolazi do sledećeg ponašanja:

- Podrazumevano se valuta transakcije u zapisu troškova podešava na valutu ugovorne jedinice projekta.
- Podrazumevano se valuta transakcije u zapisu prodaje podešava na valutu ugovora za projekat.

Kada stavka troška ili stavka u glavnoj knjizi kreira stvarne vrednosti za troškove, dolazi do sledećeg ponašanja:

- Iznos troškova možete zabeležiti u bilo kojoj valuti. Izaberite valutu koristeći birač valuta na stranici **Stavka troškova** ili **Stavka u glavnoj knjizi**. Podrazumevano se valuta transakcije za zapis troškova podešava na valutu u stavke troška. 
- Valuta transakcije za zapis prodaje je podrazumevano valuta ugovora za projekat. Da bi podesio ovu valutu, sistem prvo konvertuje iznos transakcije u valutu koju je korisnik uneo u osnovnu valutu. Zatim konvertuje iznos u valutu projektnog ugovora. 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>Izračunavanje zbirnih vrednosti prilikom evidentiranja stvarnih vrednosti projekta u više valuta transakcije

Dynamics 365 automatski upravlja zbirnim iznosima u različitim valutama. Evo primera.

| Klasa transakcije | Tip transakcije| Date   | Resurs | Kategorija transakcije | Količina | Cena po jedinici | Iznos      | Kurs valute | Iznos (u osnovnoj valuti) |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Time              | Nenaplaćena prodaja   | 14. jun | Dobrilo  |                      | 8 časova    | 20.000 JPY    | 160.000 JPY | 123           | 1300,81 USD    |
| Time              | Nenaplaćena prodaja   | 15. jun | Dobrilo  |                      | 8 časova    | 20.000 JPY    | 160.000 JPY | 123           | 1300,81 USD    |
| Trošak           | Nenaplaćena prodaja   | 16. jun | Dobrilo  | Hotel                | 1 ea     | 250 EUR      | 250 EUR     | 0.94          | 265,95 USD     |
| Trošak           | Nenaplaćena prodaja   | 17. jun | Dobrilo  | Iznajmljivanje automobila           | 1 ea     | 150 EUR      | 150 EUR     | 0.94          | 159,57 USD     |

Da biste izračunali ukupnu nenaplaćenu prodajnu vrednost za projekat, možete da kreirate polje zbirne vrednosti za polje **Iznos** za sve povezane nenaplaćene stvarne vrednosti prodaje. Polje zbirne vrednosti je konstrukcija sistema Dynamics 365 koja omogućava brze formule za povezane zapise.
