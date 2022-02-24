---
title: Grupe jedinica i jedinice
description: Ova tema pruža informacije o grupama jedinica i jedinicama.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
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
ms.openlocfilehash: 6620c99563394d1f3881d6bfdb72d01c1c4e8d6f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145600"
---
# <a name="unit-groups-and-units"></a>Grupe jedinica i jedinice

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Grupe jedinica i jedinice su osnovni entiteti u sistemu Microsoft Dynamics 365. Jedinica je jedinica mere, a više jedinica može biti grupisano u grupe jedinica. Grupa jedinica se ponekad zove raspored jedinice u Dynamics 365 korisničkom sistemu. 

Evo nekoliko primera jedinica i grupa jedinica:
 
- **Grupa jedinica**: Razdaljina 
    - **Jedinice**: Milja, kilometar itd.
- **Grupa jedinica**: Vreme
    - **Jedinice**: Čas, dan, sedmica i tako dalje. 

Kada podesite više jedinica u grupi jedinica, morate podesiti i faktor konverzije između njih tako što ćete označiti prvu jedinicu koju ste podesili kao podrazumevanu ili primarnu jedinicu za grupu jedinica. 

Na primer, u grupi jedinica **Vreme**, ako podesite **Čas** kao prvu jedinicu, sistem određuje **Čas** kao podrazumevanu jedinicu. Ako je **Dan** sledeća jedinica koju podesite, morate podesiti faktor konverzije za jedinicu **Dan** na **Čas.** Ako zatim dodate treću jedinicu **Sedmica**, morate da podesite faktor konverzije za jedinicu **Sedmica** u odnosu na **Dan** ili **Čas**. 

Sledeća slika prikazuje primer podešavanja jedinice **Dan**, pri čemu polje **Količina** prikazuje broj časova u danu, i **Sedmica**, gde polje **Količina** prikazuje broj dana u nedelji.

> ![Grupa jedinica: stranica sa informacijama](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a>Korišćenje jedinica i grupa jedinica

Dynamics 365 Project Service Automation koristi jedinice i grupe jedinica za obradu procena i stavki za troškove i vreme. 

Za troškove, svaka kategorija troška ima podrazumevanu grupu jedinica i jedinicu. Ove vrednosti se unose kao podrazumevane vrednosti u stavkama cenovnika za kategorije troškova. 

Na primer, imate kategoriju troška koja se zove **Kilometraža**. Ona ima grupu jedinica pod nazivom **Razdaljina** i podrazumevanu jedinicu koja se zove **Kilometar**. Ako podesite grupu jedinica **Rastojanje** tako da ima dve jedinice (**Milja** i **Kilometar**), možete podesiti dve cene za kategoriju **Kilometraža** za jedan cenovnik: cena po milji i ceni po kilometru.

| Kategorija troška  | Grupa jedinica  | Jedinica      | Način određivanja cena  | Cena po jedinici  |
|-------------------|---------------|-----------|-------------------|-------------------|
| Kilometraža           | Udaljenost      | Milja      | Cena po jedinici    | 10 USD            |
| Kilometraža           | Udaljenost      | Kilometar | Cena po jedinici    |  6 USD            |

Kada unesete trošak za projekat, sistem određuje cenu kroz kombinaciju kategorije i jedinice po trošku. 

| Opis troška        | Kategorija troška  | Jedinica  | Količina  | Cena po jedinici   |
|----------------------------|---------------------|-------|-----------|----------------|
| Vožnja do lokacije klijenta | Kilometraža             | Milja  | 10        | 10 USD         |

Za vreme, svako zaglavlje cenovnika ima polje **Podrazumevana jedinica za vreme**. Vrednost se podešava kada kreirate zaglavlje cenovnika. Ova jedinica se zatim koristi za podešavanje svih cena zasnovanih na ulogama u tom cenovniku.

Stavke procene za polje **Vreme za ponudu** mogu se izraziti u bilo kojoj jedinici vremena. Međutim, stavke procene u projektima i stavke vremena za projekte mogu da koriste samo jedinicu vremena **Čas**. Ako se jedinica u redu "Stavka vremena" ili "Stavka procene" ne podudara sa jedinicom u redu cenovnika za tu ulogu, sistem konvertuje cenu u jedinice koje su definisane u proceni projekta ili u transakciji stvarnih vrednosti projekta.

Sledeći primer prikazuje kako PSA koristi grupu jedinica, jedinice i faktore konverzije.
- Jedinice

   - **Grupa jedinica**: Vreme 
   - **Jedinice**: čas 
    
    - **Dan** - Faktor konverzije: 8 časova       
    - **Sedmica** - Faktor konverzije: 40 časova  
        
- Podešavanje cenovnika za projekat A:

    - **Naziv**: Prodajne cene u UK za 2016 
    - **Podrazumevana jedinica vremena**: dan 
    - **Valuta**: GBP

| Uloga      | Grupa jedinica | Jedinica | Organizaciona jedinica | Cena   |
|-----------|------------|------|---------------------|---------|
| Programer | Time       | Day  | Contoso UK          | 800 GBP |

### <a name="time-entry"></a>Stavka vremena

Sledeća tabela prikazuje krajnju transakciju na strani prodaje koju je kreirao PSA za trosatni projekat.


| Projekat   | Zadatak    | Uloga      | Količina | Jedinica  | Cena po jedinici | Nenaplaćen iznos prodaje |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| Projekat A | Dizajn  | Programer | 3        | Hour  | 100 GBP    | 300 GBP               |

## <a name="time-unit-faq"></a>Najčešća pitanja o jedinici vremena

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a>Da li PSA obavlja konverziju u različite jedinice u slučaju troška?
Ne. Konverzija jedinice funkcioniše samo za vreme. Za troškove, ako sistem ne može da pronađe cenu za kombinaciju kategorije troška i jedinice, cena je podrazumevano podešena na 0,00.

### <a name="why-does-psa-convert-time-units"></a>Zašto PSA konvertuje jedinice vremena?
U nekim zemljama ili regionima postoji zakonski uslov da se stope naplate podešavaju u danima. Pregovaranje oko cene i popusti tokom ciklusa ponude se obavljaju korišćenjem dnevnih cena za svaku ulogu koju je moguće naplatiti. Procena rasporeda i stavke vremena se unose u časovima. Da bi podržao ovu razliku u jedinicama vremena, PSA ih konvertuje.

### <a name="can-time-units-be-changed-on-project-estimates"></a>Da li se jedinice vremena mogu menjati u zavisnosti od procena za projekat?
Ne. Procena rasporeda je trenutno ograničena na časove i ne može se promeniti.

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a>Da li jedinice i grupe jedinica mogu da se uređuju, brišu i dodaju?
Da. Sa izuzetkom grupa jedinica **Vreme** i **Čas**, sve jedinice mogu da se brišu ili uređuju i mogu da se dodaju nove jedinice. U aplikaciji PSA nije moguće izbrisati grupu jedinica **Vreme** i **Čas**. Međutim, one mogu da se ažuriraju prevedenim tekstom za polje **Ime**.
