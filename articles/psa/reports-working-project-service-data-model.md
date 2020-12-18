---
title: Rad sa Project Service Automation modelom podataka
description: Ova tema pruža informacije o tome kako raditi sa modelom podataka.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 9bceb96153f0e9f5c0d40478baf691220de95f27
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642695"
---
# <a name="working-with-the-project-service-automation-data-model"></a>Rad sa Project Service Automation modelom podataka

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Service Automation proširuje druge entitete aplikacija i uvodi svoje entitete u Common Data Service model podataka. Ova tema opisuje neke od entiteta sa kojima ćete se susresti u tipičnim PSA scenarijima izveštavanja.

## <a name="reporting-on-opportunities"></a>Izveštavanje o mogućnostima za poslovanje

Project Service Automation proširuje Dynamics 365 Sales entitet **Mogućnost za poslovanje** dodavanjem polja koja omogućuju scenarije zasnovane na projektu. Ova polja su identifikovana imenom šeme ispred koje stoji prefiks **msdyn\_**. Jedno novo polje koje je važno za izveštavanje o PSA mogućnostima za poslovanje je **Vrsta porudžbine**. Vrednost **Zasnovano na radu** za ovo polje ukazuje da je mogućnost za poslovanje zapravo PSA mogućnost za poslovanje. Ostala polja koja su dodata u entitet uključuju polja **Ugovorna organizacija**, sa organizacijom koja sadrži mogućnost za poslovanje i **Menadžer za poslovne kontakte**, koje beleži ime menadžera za poslovne kontakte koji je odgovoran za mogućnost za poslovanje.

Entitet **Predmet mogućnosti za poslovanje** takođe obuhvata polja koja su povezana sa uslugom Project Service. **Način naplate** naznačuje da li predmet mogućnosti za poslovanje treba naplaćivati na osnovu vremena i materijala ili na osnovu fiksne cene, a **Projekat** beleži naziv projekta koji podržava mogućnost za poslovanje. Ostala polja za koja možete da izveštavate sadrže iznose troškova i budžeta klijenta za stavku predmeta.

## <a name="reporting-on-quotes"></a>Izveštavanje o ponudama

PSA proširuje entitet Prodaje **Ponuda** dodavanjem polja koja se odnose na projekat. **Vrsta porudžbine** razlikuje PSA ponude od ponuda koje nisu deo aplikacije PSA. Vrednost **Zasnovano na radu** za ovo polje ukazuje da je ponuda zapravo PSA ponuda. Ostala polja koja mogu biti relevantna za izveštavanje o PSA ponudama uključuju polja sa iznosima, kao što su **Naplativi troškovi**, **Nenaplativi troškovi**, **Bruto marža**, **Procene** i **Budžet**. Ostala korisna polja pokazuju da li je ponuda profitabilna, da li će biti izvršena prema rasporedu i ispunjava li očekivanja klijenta u vezi sa budžetom.

PSA takođe proširuje entitet Prodaje **Stavka ponude**. Jedno polje koje PSA dodaje je **Način naplate**, što pokazuje kako će se naplaćivati stavka ponude (prema vremenu i materijalu ili fiksnoj ceni). Ostala polja koja su dodata entitetu evidentiraju povezani projekat koji podržava stavku ponude, fakturisanje, troškove i budžet.

PSA takođe dodaje nove entitete povezane sa ponudom u Dynamics 365 model podataka. U nastavku su navedeni neki primeri:

- **Detalj stavke ponude** – Ovaj entitet sadrži detalje procene projekta u stavci ponude. Ima dva zapisa za svaku stavku ponude. Jedan zapis čuva troškove i detalje troškova stavke ponude, a drugi zapis čuva iznos prodaje i detalje prodaje stavke ponude.
- **Raspored fakturisanja stavki ponude** – Ovaj entitet sadrži raspored naplate za stavku ponude. Ovaj raspored se generiše na osnovu učestalosti fakturiranja koja je dodeljena stavci ponude.
- **Kontrolna tačka stavke ponude** – Ovaj entitet sadrži kontrolne tačke za naplatu za stavke ponude sa fiksnom cenom.
- **Analitički pregled stavki ponude** – Ovaj entitet sadrži finansijske detalje u stavci ponude. Ovi detalji mogu biti korisni za izveštaje o prodaji iz ponude i procenjenih iznosa troškova po raznim dimenzijama.

Ostali entiteti koje PSA dodaje u ponudu su **Cenovnik projekta u stavci ponude**, **Kategorija resursa stavke ponude** i **Kategorija transakcije stavke ponude**.

![Dijagram koji prikazuje ponude, stavke ponude i odnose između projekata](media/PS-Reporting-image2.png "Dijagram koji prikazuje ponude, stavke ponude i odnose između projekata")

## <a name="reporting-on-project-contracts"></a>Izveštavanje o projektnim ugovorima

PSA proširuje entitet Prodaje **Porudžbina** koji se koristi kada se projektni ugovori evidentiraju. Dodaje novo važno polje **Vrsta porudžbine**, koje identifikuje ugovor kao PSA ugovor o projektu umesto ulazne porudžbine. Vrednost **Zasnovano na radu** za ovo polje ukazuje da je porudžbina zapravo PSA ugovor o projektu. Ostala nova polja koja su dodata u entitet **Porudžbina** evidentiraju detalje o troškovima, statusu PSA ugovora i organizaciju koja je vlasnik ugovora.

PSA takođe proširuje entitet **Stavka ulazne porudžbine**. Među poljima koja dodaje su polja koja sadrže način naplate (prema vremenu i materijalu ili fiksnoj ceni), iznose budžeta klijenta i temeljni projekat.

PSA takođe dodaje nove entitete koji su dizajnirani za projektne ugovore. U nastavku su navedeni neki primeri:

- **Detalj predmeta ugovora za projekat** – Ovaj entitet sadrži detalje na nivou stavke koji su sabrani u iznos predmeta ugovora. One mogu biti detaljne kao stavke porudžbina koje su generisane iz rasporeda projekata na nivou zadatka.
- **Raspored fakturisanja za predmet ugovora** – Ovaj entitet sadrži raspored obračuna koji se generiše na osnovu učestalosti fakturisanja koja je dodeljena predmetu ugovora.
- **Kontrolna tačka ugovora** – Ovaj entitet sadrži kontrolne tačke naplate za predmete ugovora koji imaju rok naplate sa fiksnom cenom.

Ostali entiteti koje PSA dodaje u ugovor su **Cenovnik projekta za predmet ugovora za projekat**, **Kategorija resursa za predmet ugovora za projekat** i **Kategorija transakcije za predmet ugovora za projekat**.

![Dijagram koji prikazuje porudžbine, stavke porudžbina i odnose između projekata](media/PS-Reporting-image3.png "Dijagram koji prikazuje porudžbine, stavke porudžbina i odnose između projekata")

## <a name="reporting-on-projects"></a>Izveštavanje o projektima

Entitet **Projekti** i sa njim povezani entiteti ekskluzivni su za PSA. **Projekat** je entitet najvišeg nivoa koji se koristi za evidentiranje posla i troškova poslovnih operacija. Evo liste povezanih entiteta:

- **Član projektnog tima** – Ovaj entitet sadrži detalje o resursima koji mogu da se dodele i dodeljeni su projektu. Ti resursi mogu biti generički ili imenovani resursi koji mogu da se dodele i koje unosi menadžer projekta ili se generišu iz rasporeda projekta.
- **Projektni zadatak** – Ovaj entitet sadrži zadatke koji čine plan ili raspored projekta.
- **Dodela resursa** – Ovaj entitet sadrži dodelu zadatka za resurs koji se može rezervisati.
- **Potreba za resursom** – Ovaj entitet sadrži potrebe za svim članovima tima sa generičkim resursima.
- **Procena** i **Stavka procene** – Ovi entiteti imaju odnos između zaglavlja i stavke i sadrže procene troškova za projekat. Procene zadataka skladište se u entitet **Procene resursa**.

![Dijagram koji prikazuje zahteve za resursom i odnose između projekata](media/PS-Reporting-image4.png "Dijagram koji prikazuje zahteve za resursom i odnose između projekata")

## <a name="reporting-on-resources"></a>Izveštavanje o resursima

Resursi projekta koriste entitete **Resurs koji se može rezervisati** iz rešenja Universal Resource Scheduling (URS) koji se dele sa drugim aplikacijama, kao što je Microsoft Dynamics 365 Field Service. Evo liste entiteta koje biste mogli koristiti prilikom izveštavanja o projektnim resursima:

- **Resurs koji se može rezervisati** – Ovaj entitet predstavlja korisnika, kontakt, generički resurs, poslovni kontakt, grupu ili opremu koja se koristi u projektnom timu.
- **Karakteristike resursa koji se može rezervisati** -– Ovaj entitet uključuje veštine, certifikacije ili obrazovanje resursa. Karakteristike mogu imati vrednosti ocena koje su definisane modelom ocena.
- **Kategorija resursa koji se može rezervisati** – Ovaj entitet predstavlja ulogu resursa koji se može rezervisati.
- **Rezervacije resursa koji se može rezervisati** – Ovaj entitet predstavlja vreme resursa koje je rezervisano za projekte. Svaka rezervacija ima zaglavlja entiteta i entitete stavke, a svaka stavka ima status koji predstavlja status rezervacije.

![Dijagram koji prikazuje odnose karakteristika resursa koji mogu da se rezervišu](media/PS-Reporting-image5.png "Dijagram koji prikazuje odnose karakteristika resursa koji mogu da se rezervišu")

## <a name="reporting-on-actual-transactions"></a>Izveštavanje o stvarnim transakcijama

Kada odobrite vremenski raspored ili trošak ili fakturišete ugovor u aplikaciji PSA, poslovna transakcija se evidentira u entitetu **Stvarna vrednost**. Ovaj entitet može poslužiti kao osnova za gotovo sve izveštaje koji se odnose na finansije u aplikaciji PSA. Entitet **Stvarna vrednost** evidentira transakcione i prodajne transakcije poslovnog događaja. Takođe evidentira mnoge relevantne atribute.

Kada radite sa entitetom **Stvarne vrednosti**, važno je da shvatite koja se transakcija ili transakcije evidentiraju u entitetu i kada. Evo tipičnog toka kada radite sa stavkama vremena (tok za stavke troškova je sličan):

1. Kada se stavka vremena sačuva, u entitetu **Stvarna vrednost** se ne kreiraju zapisi.
2. Kada se stavka vremena prosledi, u entitetu **Stvarna vrednost** se ne kreiraju zapisi.
3. Kada se stavka vremena odobren, kreiraće se jedan zapis u entitetu **Stvarna vrednost**, a može se kreirati i drugi zapis. Prvi zapis skladišti troškove stavke vremena. Drugi zapis čuva iznos nenaplaćene prodaje stavke vremena. Drugi zapis zavisi od projekta, pa će mu biti dodeljen klijent, ponuda ili predmet ugovora.

    | Datum dokumenta | Tip transakcije | Klasa transakcije | Klijent         | Ugovor   | Resurs     | Uloga resursa | Tip naplate | Količina | Cena po jedinici | Iznos |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | 3.2.´18.        | Troškovi             | Time              | Planinski skijaški dom | CRM za planinarenje | Pavle Knežević | Menadžer projekta   | Naplativo   | 8.0      | 50.00      | 400.00 |
    | 3.2.´18.        | Nenaplaćena prodaja   | Time              | Planinski skijaški dom | CRM za planinarenje | Pavle Knežević | Menadžer projekta   | Naplativo   | 8.0      | 100.00     | 800.00 |

    Ova dva zapisa su zasebni, ali povezani zapisi. To nisu ni dugovanja ni potraživanja.

4. Ako je ugovor povezan sa projektom, kada se fakturiše stavka vremena, kreiraju se još dva zapisa u entitetu **Stvarna vrednost**. Prvo se kreira negativni iznos za zapis nenaplaćene prodaje. Ovaj zapis u suštini stornira nenaplaćenu prodaju. Drugo, kreira se transakcija za naplaćenu prodaju. Još jednom, ovi zapisi su zasebni, ali povezani i nisu ni dugovanja ni potraživanja.

    | Datum dokumenta | Tip transakcije | Klasa transakcije | Klijent         | Ugovor   | Resurs     | Uloga resursa | Tip naplate | Količina | Cena po jedinici | Iznos   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | 4.2´18.        | Nenaplaćena prodaja   | Time              | Planinski skijaški dom | CRM za planinarenje | Pavle Knežević | Menadžer projekta   | Naplativo   | - 8,0    | 100.00     | - 800,00 |
    | 4.2´18.        | Naplaćena prodaja     | Time              | Planinski skijaški dom | CRM za planinarenje | Pavle Knežević | Menadžer projekta   | Naplativo   | 8.0      | 100.00     | 800.00   |

Entitet **Poreklo transakcije** beleži poreklo zapisa **Stvarna vrednost**, a entitet **Veza transakcije** beleži povezane zapise za zapis **Stvarna vrednost**. Pored toga, zapis **Stvarna vrednost** sadrži reference na projekat, ugovor o projektu (porudžbinu), resurs koji se može rezervisati i klijenta.

![Dijagram koji prikazuje transakcionu vezu, poreklo i stvarne odnose](media/PS-Reporting-image6.png "Dijagram koji prikazuje transakcionu vezu, poreklo i stvarne odnose")
