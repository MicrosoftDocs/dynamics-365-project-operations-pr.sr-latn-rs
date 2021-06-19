---
title: Organizacione jedinice
description: Ova tema pruža informacije o organizacionim jedinicama u aplikaciji Dynamics 365 Project Service Automation.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/04/2019
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
ms.openlocfilehash: 3be18adfa1d346bdabae7e89375ca2c5a2dbda95
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009633"
---
# <a name="organizational-units"></a>Organizacione jedinice 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation, organizaciona jedinica je zasebna grupa ili odeljenje u preduzeću koje pruža profesionalne usluge i zapošljava resurse koje treba naplatiti cenama.

Za kompanije koje pružaju profesionalne usluge i zapošljavaju tehničke resurse u različitim oblastima ili linijama poslovanja, troškovi popunjavanja uloge u jednoj oblasti ili liniji poslovanja mogu se razlikovati od takvih troškova za drugu oblast ili liniju poslovanja. Koncept organizacionih jedinica u ovom scenariju pomaže tako što pruža način za grupisanje skupa uloga koji mogu da se naplatite u odeljenja preduzeća koje ima različitu strukturu troškova za te uloge.

## <a name="key-attributes-and-associations-of-organizational-units"></a>Ključni atributi i udruženja organizacionih jedinica

U aplikaciji PSA, organizaciona jedinica ima posebnu valutu i cenovnike troškova.

Valuta organizacione jedinice je primarna valuta koja se koristi za praćenje troškova.

Neke cenovnike troškova možete da priložite svakoj organizacionoj jedinici. PSA ima sledeća ograničenja za cenovnike koji se mogu priložiti organizacionoj jedinici:

- Cenovnici moraju da budu u valuti organizacione jedinice
- Cenovnici moraju da budu cenovnici troškova

Pored toga, postoji atribut organizacione jedinice u entitetu Resurs. Svaki resurs može biti dodeljen jednoj organizacionoj jedinici.

## <a name="roles-of-organizational-units"></a>Uloge organizacionih jedinica

Organizaciona jedinica ima dve uloge u aplikaciji PSA:

- **Ugovorna jedinica** – organizaciona jedinica koja predstavlja grupu ili odeljenje preduzeća koje je prvenstveno odgovorno za povećanje prodaje i upravljanje isporukom posla i usluga klijentu. Ugovornu jedinicu identifikujete u polju **Ugovorna jedinica** u odeljku zaglavlja stranice **Mogućnost za poslovanje**, **Ponuda**, **Ugovor o projektu** i **Projekat**.
- **Jedinica za obezbeđivanje resursa** – organizaciona jedinica kojoj resurs pripada ili kojoj je dodeljen. Ova organizaciona jedinica može da obezbedi svoje resurse za neke uloge u izjavama o radu i projektima koji su u vlasništvu ugovorne jedinice.

> ![Jedinice ugovaranja i jedinice za obezbeđivanje resursa](media/advanced-1.png)

## <a name="organizational-unit-faqs"></a>Najčešća pitanja o organizacionim jedinicama

Slede odgovori na nekoliko najčešćih pitanja o organizacionim jedinicama:

### <a name="how-is-the-organizational-unit-entity-in-psa-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Kako je entitet organizacione jedinice u aplikaciji PSA povezan sa organizacionim entitetom koji već postoji u sistemu Dynamics 365?

Entitet organizacije u sistemu Microsoft Dynamics 365 predstavlja ime globalne Dynamics 365 instance. Ovo ime je obično ime globalnog preduzeća.

Entitet organizacione jedinice predstavlja grupu ili odeljenje u globalnom preduzeću. Ova grupa ili odeljenje ima skup uloga i cenovnik troškova za njih, a te uloge i cenovnici se razlikuju od uloga i cenovnika ostalih grupa ili odeljenja u preduzeću.

Kada se PSA instalira, kreira se podrazumevana organizaciona jedinica na osnovu organizacije. Svi postojeći resursi dodeljuju se podrazumevanoj organizacionoj jedinici. Ako se neki novi korisnici ili resursi usluge Active Directory uvezu u Dynamics 365, postupak uvoza korisnika dodeljuje ih podrazumevanoj organizacionoj jedinici u aplikaciji PSA.
 
### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Po čemu se entitet organizacione jedinice razlikuje od entiteta poslovne jedinice?

U sistemu Dynamics 365, entitet poslovne jedinice je bezbednosni konstrukt. Udruživanje korisnika sa poslovnom jedinicom određuje entitete i evidencije entiteta kojima korisnik ima pristup. Takođe određuje dozvole (za kreiranje, čitanje, pisanje, brisanje, prilaganje, prilaganje u, dodeljivanje ili deljenje) koje korisnik ima za te zapise entiteta.

Entitet organizacione jedinice predstavlja grupu ili odeljenje kompanije koja ima različite stope troškova za zaposlene koji su joj dodeljeni. Povezanost resursa sa organizacionom jedinicom određuje troškove resursa za angažovanje na projektu.

Kada implementirate Dynamics 365, optimizirajte sigurnosna ovlašćenja za hijerarhiju poslovnih jedinica i dodeljivanje korisnika poslovnim jedinicama. Dodelite istoj poslovnoj jedinici sve korisnike koji obično moraju pristupati istom skupu zapisa. Organizaciona jedinica nema uticaja na bezbednosna ovlašćenja ni na pristup.

#### <a name="example-of-organizational-units-and-business-units"></a>Primer organizacionih jedinica i poslovnih jedinica

Contoso, Ltd. napredno koristi Microsoft tehnologiju. Dobrilo i Danica su C\# programeri, ali Danica je u Sjedinjenim Državama, dok je Dobrilo u Indiji. Većina angažmana na projektu zahteva resurse iz kompanija Contoso India i Contoso US, a Dobrilo i Danica zahtevaju isti nivo bezbednosnog pristupa projektima u ovoj oblasti. Međutim, troškovi programera iz kompanije Contoso India značajno se razlikuju od troškova programera iz kompanije Contoso US.

Evo optimalnog načina za dizajn ovog scenarija korišćenjem sistema Dynamics 365 i PSA.

1. Kreirajte poznavanje Microsoft tehnologije kao poslovnu jedinicu i sa njom povežite Dobrila i Danicu. Na ovaj način garantujete da će oba zaposlenika imati isti nivo bezbednosnog pristupa bilo kojim projektima u toj oblasti. Oboje će moći da provere napredak i izveštavaju o vremenu, troškovima i ažuriranjima zadataka. 
2. Kreirajte dve organizacione jedinice kao garanciju da su troškovi za projekat tačno izraženi. 
3. Povežite Danicu sa kompanijom Contoso US i povežite Dobrila sa kompanijom Contoso India.
4. Dodelite odgovarajuće cenovnike troškova obema organizacionim jedinicama. Na ovaj način garantujete da troškovi koji se evidentiraju za projekat za Dobrila i Danicu tačno odražavaju razliku u troškovima između kompanija Contoso US i Contoso India.

### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Da li su organizacione jedinice povezane sa prodajnim teritorijama u sistemu Dynamics 365?

Ne postoji povezanost niti bilo kakav odnos između prodajnih teritorija i organizacionih jedinica. Prodajna teritorija je obično geografsko područje gde se nešto prodaje. Prodajni cenovnik može se povezati sa svakom prodajnom teritorijom.

Organizaciona jedinica je interna grupa ili odeljenje u kompaniji koja prati troškove za skup uloga koje prodaje drugim odeljenjima ili spoljašnjim klijentima.

#### <a name="example-of-organizational-units-and-sales-territories"></a>Primer organizacionih jedinica i prodajnih teritorija

Contoso, Ltd. ima dva razvojna centra: Contoso US i Contoso India. Troškovi resursa znatno se razlikuju između ova dva razvojna centra.

Contoso prodaje svoje IT usluge na mnogim međunarodnim tržištima, kao što su Latinska Amerika, Severna Amerika, Azijsko-pacifička oblast, zapadna Evropa i Bliski Istok. Stope naplate za iste uloge na projektu mogu se značajno razlikovati na ovim tržištima.

Contoso US i Contoso India trebalo bi da budu podešene kao organizacione jedinice, a svaka organizaciona jedinica treba da ima svoj cenovnik troškova. Azija-Pacifik, Latinska Amerika, Severna Amerika, zapadna Evropa i Bliski Istok trebalo bi da budu podešeni kao prodajne teritorije, a svaka prodajna teritorija treba da ima svoj prodajni cenovnik.

### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Zašto postoji ograničenje povezivanja cenovnika sa organizacionim jedinicama? 

Određivanje prodajnih cena je obično jedinstveno za geografska područja ili tržišta na kojima se usluge prodaju. Unutrašnja odeljenja kompanije obično ne određuju sopstvene prodajne cene za iste vrste usluga. Međutim, unutrašnja odeljenja imaju različitu cenu prodate robe, u zavisnosti od veština ljudi koje zapošljavaju i uslova rada u regionu u kojem posluju. Pošto su organizacione jedinice modelirane kao interna odeljenja kompanije, one mogu imati samo cenovnike troškova.

### <a name="why-cant-we-associate-sales-price-lists-to-organizational-units"></a>Zašto ne možemo da povežemo prodajne cenovnike sa organizacionim jedinicama?

U aplikaciji PSA, prodajni cenovnici mogu se povezati sa klijentima i prodajnim teritorijama. Transakcioni entiteti, kao što su Mogućnosti za poslovanje, Ponuda, Ugovor o projektu i Projekat, koriste prodajne cenovnike priložene poslovnom kontaktu klijenta ili prodajnoj teritoriji kako bi odredili stope naplate i potencijalni prihod od angažovanja na projektu.

Cenovnici troškova povezani su sa organizacionim jedinicama. Transakcioni entiteti, kao što su Mogućnosti za poslovanje, Ponuda, Ugovor o projektu i Projekat, koriste cenovnike troškova koji su priloženi ugovornoj jedinici kako bi odredili troškove za angažovanje na projektu.

### <a name="are-organizational-units-hierarchical-in-psa"></a>Da li postoji hijerarhija organizacionih jedinica u aplikaciji PSA?

Ne. U trenutnom izdanju aplikacije PSA, organizacione jedinice nisu u hijerarhijskoj vezi. To znači da ne možete da:

- Konfigurišete obrazac za određivanje podrazumevanih cena koštanja koji može da se koristi na višem nivou hijerarhije. 
- Izveštavate o ukupnim prihodima ili troškovima na različitim nivoima hijerarhije organizacione jedinice.

### <a name="were-a-big-multinational-firm-with-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-make-the-best-use-of-the-organizational-unit-concept-in-this-version-of-the-project-service-app"></a>Mi smo velika multinacionalna kompanija sa složenom hijerarhijom na više nivoa koja se odnosi na centre troškova, odeljenja i kancelarije za naplatu. Kako možemo najbolje iskoristiti koncept organizacione jedinice u ovoj verziji aplikacije Project Service?

Kada imate složenu hijerarhiju centara troškova, odeljenja, kancelarija za naplatu itd., podesite čvorove lista te hijerarhije kao posebne organizacione jedinice.
Sledeći primer prikazuje tipičnu hijerarhiju:

**ContosoIndija**

  - SAP poslovi 

    - Tehnički konsultanti 
    - Funkcionalni konsultanti 
    
  - Poznavanje Microsoft tehnologije 

    - Tehnički konsultanti
    - Funkcionalni konsultanti 
    
**Contoso US**

 - SAP poslovi 

    - Tehnički konsultanti 
    - Funkcionalni konsultanti 
    
 - Poznavanje Microsoft tehnologije 

    - Tehnički konsultanti 
    - Funkcionalni konsultanti 
 
Ako je vaša hijerarhija slična, morate je podesiti kao bazičnu listu, kao što je ovde prikazano:
- Contoso India – SAP poslovi – Tehnički konsultanti 
- Contoso India – SAP poslovi – Funkcionalni konsultanti       
- Contoso India – Funkcionalni konsultanti u oblasti korišćenja Microsoft tehnologije 
- Contoso India – Funkcionalni konsultanti u oblasti korišćenja Microsoft tehnologije 
- Contoso US – SAP poslovi – Tehnički konsultanti  
- Contoso US – SAP poslovi – Funkcionalni konsultanti  
- Contoso US – Korišćenje Microsoft tehnologije – Tehnički konsultanti 
- Contoso US – Korišćenje Microsoft tehnologije – Funkcionalni konsultanti

### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-organizational-unit-concept-in-the-current-version-of-psa"></a>Mi smo mala kompanija za profesionalne usluge koja posluje kao samo jedno odeljenje. Kako najbolje možemo da koristimo koncept organizacione jedinice u trenutnoj verziji aplikacije PSA?

Ako vaša kompanija posluje kao jedna jedinica koja ima jedan cenovnik troškova, ne morate podešavati nijednu organizacionu jedinicu. Tokom PSA instalacije, Dynamics 365 kreira jednu podrazumevanu organizacionu jedinicu koja ima isti naziv kao i organizacija. Svi korisnici se podrazumevano dodeljuju ovoj organizacionoj jedinici. Kad god sistem zahteva da se izabere organizaciona jedinica, ova organizaciona jedinica se podrazumevano bira.

### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract-what-is-the-default-contracting-unit"></a>Kada se projekat kreira iz stavke ponude ili predmeta ugovora, podrazumevana ugovorna jedinica dolazi iz ponude ili ugovora o projektu. Ako se projekat kreira pre prodajnih entiteta, poput ponude ili ugovora o projektu, šta je podrazumevana ugovorna jedinica?

Kada se projekat kreira samostalno, podrazumevana ugovorna jedinica projekta zasniva se na korisniku koji je kreira. Taj korisnik je i podrazumevani menadžer projekata. Ako je projekat mapiran na prodajni entitet, poput ponude ili ugovora o projektu, ugovorna jedinica za projekat se onda zasniva na prodajnom entitetu. U ovom slučaju mogu se ponovo izračunati procene projekata jer se cenovnik troškova koristi za izračunavanje promena u proceni troškova ako se promeni ugovorna jedinica. Prodajni cenovnik koristi se za izračunavanje prodajnih procena koje će se promeniti tako da budu sinhronizovane sa cenovnikom projekta u ponudi.

Polja **Jedinica ugovaranja** i **Valuta** za projekat su zaključana za uređivanje jer moraju biti sinhronizovana sa vrednostima u prodajnom entitetu (ponuda ili ugovor o projektu) na koji je projekat mapiran.


[!INCLUDE[footer-include](../includes/footer-banner.md)]