---
title: Procena prodaje i troškova projekta kada resurs koji može da se rezerviše ispunjava više uloga u projektu
description: U ovoj temi se pružaju informacije o tome kako se dimenzije cene mogu koristiti za podršku određivanju cena i troškova za resurs koji ispunjava više uloga u projektu.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083632"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a>Procena prodaje i troškova projekta kada resurs koji može da se rezerviše ispunjava više uloga u projektu 

Kompanije zasnovane na projektu često imaju potrebu da jedan resurs obavlja više uloga na projektu. Cene i troškovi za svaku od ovih uloga mogu se različito odrediti, što znači da vreme istog resursa na projektu može dobiti različitu finansijsku procenu u zavisnosti od naplate i stope troškova za svaku od uloga. Project Service Automation omogućava podešavanje vrednosti u zapisu člana tima za imenovani resurs i omogućava različite zamene za svaki od zadataka kojima je dodeljen član tima.

Sledeći primer objašnjava kako jednostavna izmena ove vrednosti omogućava resursu da ima više uloga u projektu sa različitim troškovima i stopama naplate.

## <a name="create-tasks"></a>Kreiranje zadataka
Napravite dva projektna zadatka po 40 sati, zadatak A i zadatak B. Izaberite zadatak A kao prethodnika zadatka B.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Podešavanje uloge i organizacione jedinice za generičkog člana projektnog tima

1. Na stranici **Raspored** izaberite red **Zadatak** za zadatak A. 
2. U polju **Resursi** izaberite **Kreiraj** u padajućoj listi.
3. Na stranici **Brzo kreiranje člana tima** , navedite atribute generičkog člana tima koji može da izvrši ovaj zadatak.
4. Izaberite odgovarajuću ulogu i organizacionu jedinicu, a zatim izaberite **Sačuvaj i zatvori**. Generički član tima se kreira i dodeljuje ovom zadatku. 

Ponovite ove korake za zadatak B i uverite se da se uloga i organizaciona jedinica generičkog člana tima kreiranog za zadatak B razlikuje od zadatka A. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Podešavanje uloge i organizacione jedinice za projektni zadatak

1. Kada kreirate zadatak A, izaberite zadatak, a zatim izaberite **Uređuj zadatak**.
2. Na stranici **Detalji zadatka** pronađite polja **Uloga** i **Organizaciona jedinica** , dodajte vrednosti potrebne za resurs koji bi izvršio ovaj zadatak. 

  > [!NOTE]
  > Ako dovršavate ove scenarije koristeći Project Service Automation demo podatke, izaberite **Vođa konsultanata** za ulogu i **Fabrikam US** kao organizacionu jedinicu.

3. Izaberite zadatak B, a zatim izaberite **Uredi zadatak**.
4. Na stranici **Detalji zadatka** pronađite polja **Uloga** i **Organizaciona jedinica** , dodajte vrednosti potrebne za resurs koji bi izvršio ovaj zadatak. Uverite se da se vrednosti u poljima **Uloga** i **Organizaciona jedinica** za zadatak B razlikuju od onih za zadatak A. 

  > [!NOTE]
  > Ako dovršavate ove scenarije koristeći Project Service Automation demo podatke, izaberite **Tehničar mreže** za ulogu i **Fabrikam US** kao organizacionu jedinicu.

5. Sačuvajte i zatvorite stranicu **Detalji zadatka**. 

## <a name="team-member-and-estimates-behaviour"></a>Član tima i procena ponašanja 

1. Na stranici **Detalji zadatka** , u odeljku **Član tima** , izaberite dva člana generičkog tima, a zatim izaberite **Generiši zahteve**. Tako ćete generisati zahteve za resursima. 
2. Izaberite red člana tima za **Vođa konsultanata** , a zatim izaberite **Rezerviši**. Tabela rasporeda se otvara i rezerviše resurs za taj zahtev.
3. Izaberite red člana tima za **Tehničar mreže** , a zatim izaberite **Rezerviši**. Tabela rasporeda se otvara i rezerviše isti resurs za taj zahtev.

### <a name="team-member-grid"></a>Mreža člana tima 
Na mreži **Član tima** , uočite da su dva generička zapisa članova tima izbrisana i da su zamenjena jednim resursom. Postoji jedan skup vrednosti za taj resurs koji prikazuje zadati skup vrednosti za **ulogu** i **organizacionu jedinicu**.
Kada proširite red tog zapisa člana tima, na zapisu člana tima možete videti različite zadatke za oba ta zadatka. Svaki red zadatka ima vrednosti specifične za zadatak za **ulogu** i **organizacionu jedinicu**. 

### <a name="estimates-grid"></a>Mreža procena 
Kada odete na mrežu **Procene** , primetićete da obe dodele za isti resurs imaju različito određene cene.
Cena dodele resursa zadatku A određuje se korišćenjem vrednosti atributa **Uloga** za **vođu konsultanata**. Cena dodele istog resursa zadatku B određuje se korišćenjem vrednosti atributa **Uloga** za **tehničara mreže**.




