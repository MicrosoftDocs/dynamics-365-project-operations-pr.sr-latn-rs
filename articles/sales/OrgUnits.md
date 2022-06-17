---
title: Organizacione jedinice
description: Ovaj članak opisuje koncept organizacionih jedinica i objašnjava kako se kreiraju i održavaju organizacione jedinice u korporaciji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 1/31/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: a20a37b61db68d70869a11e10bef5d30c422b1eb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921641"
---
# <a name="organizational-units-overview"></a>Pregled organizacionih jedinica

U korporaciji Microsoft Dynamics 365 Project Operations, organizaciona *jedinica je* posebna grupa ili odeljenje u preduzeću za profesionalne usluge koje koristi resurse koji se mogu naplatiti i koji imaju stope troškova.

Za preduzeća za profesionalne usluge koja zapošljavaju tehničke resurse u različitim oblastima prakse ili poslovnim linijama, troškovi popunjavanja uloge mogu da se razlikuju, u zavisnosti od oblasti prakse ili poslovne linije u kojoj je uloga popunjena. U ovom scenariju, koncept organizacionih jedinica pomaže tako što obezbeđuje način grupisanja skupa uloga koje se mogu naplatiti u podeli preduzeća koje ima izrazitu strukturu troškova za te uloge.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>Koncept organizacionih jedinica u projektnim operacijama

U operacijama projekta organizaciona jedinica ima određenu valutu i određene cenovnike troškova.

Valuta organizacione jedinice je primarna valuta koja se koristi za praćenje troškova.

Neke cenovnike troškova možete da priložite svakoj organizacionoj jedinici. Operacije projekta stavljaju sledeća ograničenja na cenovnike koji se mogu priložiti organizacionoj jedinici:

- Cenovnici moraju biti u valuti organizacione jedinice.
- Cenovnici moraju biti cenovnici troškova.

Pored toga, entitet resursa sadrži atribut organizacione jedinice. Svaki resurs može biti dodeljen jednoj organizacionoj jedinici.

### <a name="roles-of-organizational-units"></a>Uloge organizacionih jedinica

Organizaciona jedinica igra dve uloge u operacijama projekta:

- **Ugovorna jedinica** – organizaciona jedinica koja predstavlja grupu ili odeljenje preduzeća koje je prvenstveno odgovorno za povećanje prodaje i upravljanje isporukom posla i usluga klijentu. Ugovornu jedinicu identifikujete u polju **Ugovorna jedinica** u odeljku zaglavlja stranice **Mogućnost za poslovanje**, **Ponuda**, **Ugovor o projektu** i **Projekat**.
- **Jedinica za obezbeđivanje resursa** – organizaciona jedinica kojoj resurs pripada ili kojoj je dodeljen. Ova organizaciona jedinica može da obezbedi svoje resurse za neke uloge u izjavama o radu i projektima koji su u vlasništvu ugovorne jedinice.

![Jedinice ugovaranja i jedinice za obezbeđivanje resursa.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>Najčešća pitanja o organizacionoj jedinici

Slede odgovori na nekoliko najčešćih pitanja o organizacionim jedinicama:

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Kako je entitet organizacione jedinice u operacijama projekta povezan sa entitetom organizacije koji već postoji u sistemu Dynamics 365?

Entitet organizacije u sistemu Dynamics 365 predstavlja ime globalne Dynamics 365 instance. Ovo ime je obično ime globalnog preduzeća.

Entitet organizacione jedinice predstavlja grupu ili odeljenje u globalnom preduzeću. Ova grupa ili odeljenje ima skup uloga i cenovnik troškova za njih, a te uloge i cenovnici se razlikuju od uloga i cenovnika ostalih grupa ili odeljenja u preduzeću.

Kada se operacije projekta instaliraju, kreira se podrazumevana organizaciona jedinica zasnovana na organizaciji. Svi postojeći resursi dodeljuju se podrazumevanoj organizacionoj jedinici. Ako se neki novi korisnici ili resursi aktivnog direktorijuma uvezu u Dynamics 365, proces uvoza korisnika ih dodeljuje podrazumevanoj organizacionoj jedinici u operacijama projekta.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Po čemu se entitet organizacione jedinice razlikuje od entiteta poslovne jedinice?

U sistemu Dynamics 365, entitet poslovne jedinice je bezbednosni konstrukt. Udruživanje korisnika sa poslovnom jedinicom određuje entitete i evidencije entiteta kojima korisnik ima pristup. Takođe određuje dozvole (za kreiranje, čitanje, pisanje, brisanje, prilaganje, prilaganje u, dodeljivanje ili deljenje) koje korisnik ima za te zapise entiteta.

Entitet organizacione jedinice predstavlja grupu ili odeljenje kompanije koja ima različite stope troškova za zaposlene koji su joj dodeljeni. Povezanost resursa sa organizacionom jedinicom određuje troškove resursa za angažovanje na projektu.

Kada implementirate Dynamics 365, optimizirajte sigurnosna ovlašćenja za hijerarhiju poslovnih jedinica i dodeljivanje korisnika poslovnim jedinicama. Dodelite istoj poslovnoj jedinici sve korisnike koji obično moraju pristupati istom skupu zapisa. Organizaciona jedinica nema uticaja na bezbednosna ovlašćenja ni na pristup.

**Primer koji pokazuje jednu potencijalnu razliku u modelovanja organizacionih jedinica i poslovnih jedinica**

Contoso, Ltd. ima napredno poznavanje Microsoft tehnologije. Dobrilo i Danica su C\# programeri, ali Danica je u Sjedinjenim Državama, dok je Dobrilo u Indiji. Većina angažmana na projektu zahteva resurse i iz Contoso Indije i Contoso SAD, a Prakaš i Triša zahtevaju isti nivo bezbednosnog pristupa projektima u ovoj oblasti prakse. Međutim, troškovi programera iz kompanije Contoso India značajno se razlikuju od troškova programera iz kompanije Contoso US.

Evo optimalnog načina za dizajniranje ovog scenarija pomoću sistema Dynamics 365 i Projektnih operacija.

1. Kreirajte poznavanje Microsoft tehnologije kao poslovnu jedinicu i sa njom povežite Dobrila i Danicu. Na taj način ćete obezbediti da oba zaposlena imaju isti nivo bezbednosnog pristupa svim projektima u toj oblasti prakse. Obojica će moći da provere napredak i prijave vreme, troškove, upotrebu materijala i ispravke zadataka.
2. Kreirajte dve organizacione jedinice da biste se uverili da se trošak projekta ispravno odražava.
3. Povežite Trišu Contoso SAD i Prakaša sa Contoso Indijom.
4. Dodelite odgovarajuće cenovnike troškova obema organizacionim jedinicama. Na taj način pomažete da se osigura da troškovi koji su zabeleženi na projektu za Prakaš i Trišu tačno odražavaju razliku u troškovima između SAD i Contoso i Contoso Indije.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Da li su organizacione jedinice povezane sa prodajnim teritorijama u sistemu Dynamics 365?

Ne postoji povezanost niti bilo kakav odnos između prodajnih teritorija i organizacionih jedinica. Prodajna teritorija je obično geografsko područje gde se nešto prodaje. Prodajni cenovnik može se povezati sa svakom prodajnom teritorijom.

Organizaciona jedinica je interna grupa ili odeljenje u kompaniji koja prati troškove za skup uloga koje prodaje drugim odeljenjima ili spoljašnjim klijentima.

**Primer koji pokazuje jednu potencijalnu razliku u modelovanja organizacionih jedinica i teritorija prodaje**

Contoso, Ltd. ima dva razvojna centra: Contoso US i Contoso India. Troškovi resursa se umnogome razlikuju između ova dva razvojna centra. Contoso prodaje svoje usluge informacione tehnologije (IT) na mnogim međunarodnim tržištima, kao što su Latinska Amerika, Severna Amerika, Azija-Pacifik, Zapadna Evropa i Bliski istok. Stope naplate za iste uloge na projektu mogu se značajno razlikovati na ovim tržištima. Contoso US i Contoso India trebalo bi da budu podešene kao organizacione jedinice, a svaka organizaciona jedinica treba da ima svoj cenovnik troškova. Azija-Pacifik, Latinska Amerika, Severna Amerika, zapadna Evropa i Bliski Istok trebalo bi da budu podešeni kao prodajne teritorije, a svaka prodajna teritorija treba da ima svoj prodajni cenovnik.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Zašto postoji ograničenje povezivanja cenovnika sa organizacionim jedinicama?

Određivanje prodajnih cena je obično jedinstveno za geografska područja ili tržišta na kojima se usluge prodaju. Unutrašnja odeljenja kompanije obično ne određuju sopstvene prodajne cene za iste vrste usluga. Međutim, unutrašnja odeljenja imaju različitu cenu prodate robe, u zavisnosti od veština ljudi koje zapošljavaju i uslova rada u regionu u kojem posluju. Pošto su organizacione jedinice modelirane kao interna odeljenja kompanije, one mogu imati samo cenovnike troškova.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Zašto ne možemo da povežemo prodajne cenovnike sa organizacionim jedinicama?

U operacijama projekta, prodajni cenovnici se mogu povezati sa kupcima i teritorijama prodaje. Transakcioni subjekti kao što su prilika, ponuda, ugovor o projektu i Projekat koriste prodajne cenovnike koji su priloženi kontou kupca ili teritoriji prodaje da bi odredili stope fakture i potencijalni prihod za angažovanje projekta.

Cenovnici troškova povezani su sa organizacionim jedinicama. Transakcioni subjekti kao što su prilika, ponuda, Ugovor o projektu i Cenovnici troškova projekta koji su priloženi jedinici za ugovaranje da bi odredili troškove za angažovanje projekta.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>Da li su organizacione hijerarhijski u projektnim operacijama?

Ne. U trenutnom izdanju operacija projekta, organizacione jedinice se ne hijerarhijski. Zbog toga ne možete da izvršite sledeće zadatke:

- Konfigurišite obrazac za unos podrazumevanih cena troškova koji prelazi na hijerarhiju.
- Prijavite prihod ili trošak koji je sabran na različitim nivoima hijerarhije organizacionih jedinica.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Mi smo velika multinacionalna firma koja ima složenu, višestruku hijerarhiju centara troškova, odeljenja i kancelarija za naplatu. Kako najbolje možemo da koristimo koncept organizacionih jedinica u trenutnoj verziji projektnih operacija?

Kada imate složenu hijerarhiju centara troškova, odeljenja, kancelarija za naplatu i tako dalje, podesite čvorove listova te hijerarhije kao različite organizacione jedinice.

Sledeći primer prikazuje tipičnu hijerarhiju.

**Contoso India**

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

Ako hijerarhija liči na ovaj primer, morate je podesiti kao ravnu listu, kao što je ovde prikazano:

- Contoso India - SAP poslovi - Tehnički konsultanti
- Contoso India - SAP poslovi - Funkcionalni konsultanti
- Contoso India - Poznavanje Microsoft tehnologije - Funkcionalni konsultanti
- Contoso India - Poznavanje Microsoft tehnologije - Funkcionalni konsultanti
- Contoso US - SAP poslovi - Tehnički konsultanti
- Contoso US - SAP poslovi - Funkcionalni konsultanti
- Contoso US - Poznavanje Microsoft tehnologije - Tehnički konsultanti
- Contoso US - Poznavanje Microsoft tehnologije - Funkcionalni konsultanti

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Mi smo mala kompanija za profesionalne usluge koja posluje kao samo jedno odeljenje. Kako najbolje možemo da koristimo koncept organizacionih jedinica u trenutnoj verziji projektnih operacija?

Ako vaša kompanija posluje kao jedna jedinica koja ima jedan cenovnik troškova, ne morate podešavati nijednu organizacionu jedinicu. Instalacija operacija projekta kreira jednu podrazumevanu organizacionu jedinicu koja ima isto ime kao organizacija. Svi korisnici se podrazumevano dodeljuju ovoj organizacionoj jedinici. Kad god sistem zahteva da se izabere organizaciona jedinica, ova organizaciona jedinica se podrazumevano bira.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Kada se projekat kreira iz stavke ponude ili predmeta ugovora, podrazumevana ugovorna jedinica dolazi iz ponude ili ugovora o projektu. Koja je podrazumevana jedinica za ugovaranje ako je projekat kreiran pre entiteta prodaje kao što su "Ponuda" ili "Ugovor o projektu"?

Kada se projekat kreira samostalno, podrazumevana ugovorna jedinica projekta zasniva se na korisniku koji je kreira. Taj korisnik je i podrazumevani menadžer projekata. Ako je projekat mapiran u entitet prodaje kao što je ponuda ili ugovor o projektu, jedinica ugovora projekta se umesto toga zasniva na entitetu prodaje. U ovom slučaju mogu se ponovo izračunati procene projekata jer se cenovnik troškova koristi za izračunavanje promena u proceni troškova ako se promeni ugovorna jedinica. Prodajni cenovnik se koristi za izračunavanje procena prodaje koje će biti promenjene tako da se sinhronizuju sa cenovnicima projekta ponude.

Polja **Jedinica za ugovaranje** **i** valuta projekta su zaključana za uređivanje jer moraju biti sinhronizovana sa vrednostima entiteta prodaje (ponude ili ugovora o projektu) na koje je projekat mapiran.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Kreiranje i održavanje organizacionih jedinica u projektnim operacijama

Da biste kreirali organizacionu jedinicu u operacijama projekta, sledite ove korake.

1. Idite na **organizacione \> jedinice postavki**.
2. Izaberite **Novo**.
3. U polje **Opšte** postavke, u **polje** Ime unesite ime organizacione jedinice. Zatim postavite ostala polja po potrebi.
4. Kliknite **na dugme** "Sačuvaj" da biste kreirali zapis tako da možete da nastavite sa uređivanjem.
5. U **okviru Cenovnici** troškova izaberite znak plus (**+**) da biste dodali cenovnik. Ovde možete dodati samo cenovnike koji imaju **kontekst** "Trošak".
6. U polju **Ime** izaberite dugme Pretraži **i** izaberite cenovnik koji želite da učinite dostupnim organizacionoj jedinici. Nastavite da dodajete cenovnike po potrebi.
7. Kada završite sa dodavanjem cenovnika, u donjem **desnom** uglu stranice izaberite stavku Sačuvaj.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
