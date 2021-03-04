---
title: Konfigurisanje predložaka troškova
description: Ova tema pruža informacije o tome kako da kreirate i koristite predloške troškova u usluzi Project Operations.
author: sigitac
manager: tfehr
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 786b2b9b140f82d406044c2ed05761d7f46ee9e0
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642740"
---
# <a name="set-up-cost-templates"></a>Konfigurisanje predložaka troškova

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_


Ova tema pruža informacije o tome kako da kreirate i koristite predloške troškova u usluzi Project Operations. Predložak troškova određuje:

- Kategorije projekata za predviđanje i stvarne transakcije koje treba da budu uključene u nekom procentu obračuna dovršenosti projekta. Vrednost procenta dovršenosti se zatim koristi za izračunavanje koliki je prihod prepoznat.
- Da li procenat dovršenosti može biti izmenjen ako se automatski izračunava.
- Da li se procenat dovršenosti izračunava na osnovu iznosa ili jedinica.

## <a name="cost-template-example"></a>Primer predloška troškova

Radite na projektu dizajniranja veb-sajta za klijenta u kojem naplaćujete fiksnu naknadu od 10.000 dolara. Predviđate da će za završetak projekta trebati 100 sati (5.000 dolara). Takođe predviđate dve avionske karte i četiri noćenja u hotelu za putovanja do lokacije klijenta (1.800 dolara). To rezultira ukupnim predviđenim troškovima od 6.800 dolara.

Kada pokrenete postupak prepoznavanja prihoda sa fiksnom cenom da biste kreirali procenu na kraju meseca, saznaćete da ste na projektu radili 35 sati. Ovo još ne uključuje letove ili hotelske troškove. Takođe ste imali pomoćnika koji je pet sati istraživao za projekat po ceni od 100 dolara, koje niste planirali.

Kada izračunate vrednost procenta dovršenosti za ovaj projekat, morate da napravite sledeće izbore:

- Da li želite da uključite sve troškove (sate i troškove) ili samo sate?
- Da li želite da uključite sve sate i samo planirane sate?
- Da li želite da izračunate procenat dovršenosti na osnovu troška planiranih sati u dolarima (5.000 dolara) ili samo na osnovu broja sati (100)?

Vaši odgovori na ova pitanja određuju opcije koje ste postavili na predlošku troškova i kategorije koje ste izabrali u redovima predloška troškova.

Sledeća tabela ilustruje rezultate različitih metoda izračunavanja vrednosti procentualnog dovršetka za ovaj scenario.

| Dovršenost na osnovu | Cene u dolarima ili jedinicama | Procenti dovršenosti | Računanje |
| --- | --- | --- | --- |
| Svi sati, bez troškova | Trošak u dolarima | 37% 35 x USD 50 + USD 100 = USD 1.850 USD 1.850/USD 5.000 |
| Svi sati, bez troškova | Jedinice | 40% | 40 sati/100 sati (uključujući pet neplaniranih sati) |
| Planirani sati, bez troškova | Cena u dolarima ili jedinici | 35% | 35/100 sati ili 35 x USD 50/5.000 |
| Svi sati i troškovi | Trošak u dolarima | 27,2% | USD 1.850/USD 6.800 |

Odlučivanje o potrebnom pristupu za kreiranje predloška troškova može zavisiti od nekoliko razloga:

- Ako u obrazac predložak troškova uvrstite neplanirano radno vreme, rizikujete da dovršite 100 posto pre završetka projekta. To je zato što će stvarni sati biti veći od planiranih. Ako koristite bilo koji od prva dva metoda navedena u tabeli, trebalo bi da promenite plan (predviđene jedinice) kada saznate za odstupanja. U ovom slučaju dodali biste ili oduzeli sate na osnovu vašeg znanja o tome šta je potrebno za završetak projekta. Ako će za projekat biti potrebno dodatnih 65 sati, u plan biste dodali pet sati za ukupno 105. Ako znate da će vaš pomoćnik izvršiti još pet sati istraživanja, ukupno će postati 110 sati.
- Ako koristite treću metodu navedenu u tabeli, planirane sate biste ažurirali samo za svoje vreme kako biste održali tačnu kalkulaciju procenta dovršenosti. Vaša profitabilnost će se promeniti kada se evidentiraju neplanirani sati, ali vi ćete ostati na poznatoj putanji procenta dovršenosti.
- Ako koristite četvrti metod naveden u tabeli, rizik je da će se troškovi pojavljivati neredovno i možda se neće odraziti na tok dovršenosti. Stoga, ako su troškovi uključeni, oni mogu dovesti do toga da procenat dovršenja fluktuira više nego što je poželjno. Na primer, jer još uvek niste leteli, procenat dovršenosti iznosio je 27 procenata umesto 35 procenata ili 37 procenata ako biste izračunavanje zasnovali samo na vremenu. Daste išli na jedan put na dve noći i precizno predvideli troškove leta i hotela, procenat dovršenosti bi bio 40,4 procenata (1850 dolara za rad i 900 dolara za troškove = USD 2.750/USD 6.800 = 40,4 procenata). Stoga bi nastajanje troškova za samo jedno avionsko putovanje promenilo procenat dovršenosti sa 27 na 40 procenata.

## <a name="create-cost-templates"></a>Kreiranje predložaka troškova
Da biste kreirale predloške troškova, sledite ove korake:

1. Da biste pristupili predlošcima troškova, u Dynamics 365 Finance okruženju idite na **Upravljanje projektima i računovodstvo** > **Podešavanje** > **Procene** > **Predložak troškova**.
2. Izaberite **Novo** da biste kreirali novi predložak troškova. Unesite naziv i opis.
3. Navedite ID linije troškova za svaki tip transakcije.
4. Izaberite podrazumevani metod dovršenja:

  - **Automatski**: procenat dovršenja se automatski izračunava na projektu. Nije moguće promeniti nastalu vrednost.
  - **Ručno**: procenat dovršenja se automatski izračunava na projektu. Možete promeniti nastalu vrednost.

  > [!NOTE]
  > Za ručne proračune, procenat dovršenosti se održava u **Ručno izračunavanje** na kartici **Opšti podaci** na stranici **Procena**.

5. U **Dovršenost zasnovana na**, izaberite jednu od sledećih vrednosti:

  - **Iznos**: iznos u računovodstvenoj valuti izračunava procenat dovršenosti.
  - **Jedinica**: količina izračunava procenat dovršenosti.
  - **Prava linija**: sistem izračunava procenat dovršenosti proporcionalno koristeći datume početka i završetka projekta da bi odredio dužinu projekta.

6. Izaberite **Linije troškova** da biste pregledali linije troškova u predlošku troškova. Za svaku vrstu transakcije potrebna je najmanje jedna linija troškova. Međutim, možete kreirati više linija troškova za iste tipove transakcija i postaviti željene atribute za te linije.
7. Na kartici **Kategorije** izaberite kategorije projekata koje će biti uključene u red predloška troškova.
8. Na kartici **Opšti podaci**, izaberite da li će ova linija biti uključena u procenat izračunavanja dovršenosti.
9. Izaberite metod cene za dovršetak koji ćete koristiti pri izračunavanju procenta dovršenja.


[!INCLUDE[footer-include](../includes/footer-banner.md)]