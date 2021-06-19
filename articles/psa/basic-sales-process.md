---
title: Procesi prodaje
description: Ova tema pruža informacije o osnovnim procesima prodaje.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 5f01ba14baa0a2378b0a230a46aed3a682342ce6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014223"
---
# <a name="sales-processes"></a>Procesi prodaje

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Procesi prodaje koji se koriste u organizaciji zasnovanoj na projektima razlikuju se od procesa prodaje koji se koriste u organizaciji zasnovanoj na proizvodima. Ova razlika se javlja zato što su ciklusi prodaje za organizacije zasnovane na projektima duži i zahtevaju prilagođene tehnike procena za analiziranje i kreiranje ponuda za svaku pogodbu. Dynamics 365 Project Service Automation koristi neka od istih funkcionalnosti koje se koristi u procesu prodaje za Dynamics 365 Sales. U nastavku su navedeni neki primeri:

- Entitet Potencijalni klijent se koristi za praćenje procesa prodaje.
- Kvalifikovani potencijalni klijenti se prate kao mogućnosti za poslovanje. Proces prodaje takođe može da započne mogućnošću za poslovanje.
- Pristupa se svim srodnim artefaktima za mogućnost za poslovanje. U ove artefakte spadaju prodajni tim, zainteresovani, verovatnoća, ocena, faze prodaje i poslovni procesi.
- Za mogućnost za poslovanje kreira se više ponuda.
- Ponuda je označena kao **Zatvorena kao dobijena** kako bi se kreirala ulazna porudžbina. U aplikaciji PSA, ulazna porudžbina je prilagođena i zove se ugovor o projektu.

Sledeća ilustracija prikazuje tipičan proces prodaje u organizaciji zasnovanoj na projektima.

> ![Proces prodaje u organizaciji zasnovanoj na projektima](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a>Procena prodaje
Vrednost prodaje se može procenjivati na osnovu projekata koji su prethodno isporučeni i kompleksnosti projekata. Kod projekata koji podrazumevaju proširenja prethodnih projekata ili onih za koje je stručnost prodavca izuzetna i dobro poznata, koriste se obrasci posla. Vi možete da koristite jednostavniji proces procene. Složeniji projekti obično imaju duži način kupovine. Zbog toga u procesu procene prodaje postoji više faza. Početkom procesa prodajni tim koristi informacije menadžera za poslovne kontakte i stručnjaka za određenu temu da bi počeo da kreira procenu na visokom nivou za svaku pojedinačnu komponentu rada koji se nudi. Ove komponente rada su predstavljene u stavkama ponude. 

Možete da kreirate procenu visokog nivoa za ponudu. Na kraju, ova procena na visokom nivou biće zamenjena detaljnijom procenom koja se zasniva na planu projekta koji se kreira korišćenjem standardizovanih predložaka projekta. Ovi predlošci pomažu pri izradi rasporeda i određivanju novčanih vrednosti za ponudu i njene komponente (stavke ponude). 

Možete kreirati više ponuda za projekat i grupisati ih pod jednim tipom entiteta sa mogućnošću za poslovanje. Na kraju, jedna od tih ponuda je označena kao **Zatvorena kao dobijena**, a kreira se ugovor o projektu ili izjava o radu. Ugovor o projektu čuva ugovorenu vrednost za svaku komponentu (predmet ugovora) koju klijent prihvati za isporuku. Izjava o radu se obično kreira kao Microsoft Word dokument. Sve fakture koje se šalju klijentu u toku isporuke projekta upućuju na ugovor o projektu ili izjavu o radu.

Takođe možete da kreirate alternativne ponude pod jednim tipom entiteta mogućnosti za poslovanje ili da podesite sistem tako da se kreira ugovor o projektu kada dobijete ponudu. U tom slučaju, možete priložiti Word dokument koji predstavlja izjavu o radu u zapis ugovora o projektu.

![Zatvaranje ponude radi kreiranja ugovora o projektu](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a>Konfigurisanje procesa prodaje
Možete da koristite tokove poslovnih procesa u sistemu Microsoft Dynamics 365 da biste konfigurisali proces prodaje. Tokovi poslovnih procesa vašem prodajnom osoblju daju navođeni vizuelni interfejs koji može da se koristi za pomeranje pogodbi unapred kroz faze koje su tipične za vaše preduzeće.

Na primer, vaše preduzeće može imati sledećih šest faza u procesu prodaje:

1. Kvalifikuj
2. Procena
3. Interna revizija
4. Ugovor
5. Isporuka
6. Zatvori

Ovih šest faza predstavljaju ševroni (\>) koje birate da proširite u svakom tipu entiteta mogućnosti za poslovanje koji kreirate.

![Konfiguracija poslovnog procesa u sistemu Dynamics 365](media/basic-guide-3.png)
 
Vaša organizacija može da koristi različite entitete za predstavljanje iste pogodbe tokom svog razvoja. Početkom procesa prodaje, pogodbu predstavlja entitet Mogućnost za poslovanje. Kako vreme prolazi i pojavljuje se više detalja, možda ćete koristiti procene visokog nivoa da biste kreirali jednu ili više ponuda. Ako jednu od ovih ponuda pregledaju interno zainteresovani i zainteresovani na strani klijenta, entitet ponude predstavlja pogodbu. Nakon što klijent prihvati ponudu, ugovor o projektu ili izjava o radu predstavlja pogodbu. Da bi podržali ovo ponašanje, tokovi poslovnih procesa su strukturirani tako da je svaka faza u procesu povezana sa drugom tabelom baze podataka.

Fazu **Kvalifikovanje** u procesu prodaje može da podrži entitet mogućnosti za poslovanje. Faze **Procena** i **Interna revizija** može da podržava entitet Ponuda. Faze **Ugovor**, **Isporuka** i **Zatvaranje** može da podrži entitet ugovora o projektu.

Dok pomerate pogodbe kroz faze, od vas će se zatražiti da kreirate odgovarajući zapis entiteta koji će vam pomoći i voditi vas kroz proces. Faze mogu biti uslovne. Na primer, ako zahtevate internu reviziju ponude samo ako ponuda koristi prilagođeni cenovnik, taj uslov možete da konfigurišete u odgovarajućoj fazi poslovnog procesa. Faza **Interna revizija** se zatim prikazuje samo za ponude koje koriste prilagođeni cenovnik. Za sve ostale ponude i pogodbe, fazu **Procena** prati faza **Ugovor**.

> [!NOTE]
> PSA ima određene stranice za entitete Mogućnost za poslovanje, Ponuda, Porudžbina i Faktura. Za ove entitete morate kreirati Project Service mogućnosti za poslovanje, ponude, porudžbine i fakture pomoću stranica sa informacijama o projektima. Ako koristite drugu stranicu za kreiranje zapisa, nećete moći da otvorite zapis sa stranice sa **informacijama o projektu**. Ako želite da otvorite zapis sa stranice sa **informacijama o projektu**, morate da izbrišete zapis i da ga ponovo kreirate koristeći stranicu sa **informacijama o projektu**. Na stranici sa **informacijama o projektu**, poslovna logika za svaki od ovih tipova entiteta osigurava da je polje **Tip** zapisa ispravno podešeno, a svi obavezni koncepti pravilno pokrenuti.

> ![Informacije o projektu za novu porudžbinu](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a>Razlike između aplikacije Project Service Automation i usluge Sales
Iako proces prodaje u aplikaciji PSA koristi osnovne mogućnosti prodajnog procesa u usluzi Sales, on ima neke ključne razlike zbog razlika u poslovnoj praksi organizacija zasnovanih na projektima. U nastavku su navedeni neki primeri:

- **Ponude projekta** – u okviru aplikacije Project Service Automation, ponuda se zatvara nakon kreiranja ugovora o projektu iz ponude. U usluzi Sales ponuda može da ostane otvorena nakon što ste je dobili. Razlog ove razlike je to što je podudaranje između ponude i ugovora o projektu bolje za organizacije zasnovane na projektima. 
- **Aktivacija i revizije** – u aplikaciji PSA, aktivacija i revizije nisu podržani za projektne ponude. U usluzi Sales, ponuda može biti zaključana da bi se sprečila dalja uređivanja.
- **Zatvaranje ponude kao izgubljene ili dobijene** – u aplikaciji PSA, kada je ponuda za projekat zatvorena kao dobijena ili izgubljena, mogućnost za poslovanje ostaje otvorena. Sve ostale ponude za mogućnost za poslovanje se zatvaraju kao izgubljene. U usluzi Sales, kada je ponuda zatvorena kao dobijena ili izgubljena, od korisnika se traži da preduzme radnju za mogućnost za poslovanje. U zavisnosti od korisničkog unosa, osnovna mogućnost za poslovanje je možda zatvorena ili je otvorena.

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Praćenje revizija ponuda i planova projekta u ciklusu prodaje
U aplikaciji PSA, ne možete da pratite revizije ponude. Umesto toga, morate označiti postojeću ponudu kao **Zatvorena kao izgubljena**, a zatim kreirati novu ponudu. Možete kopirati ponudu ili klonirati ponudu zasnovanu na projektu koristeći PSA.

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a>Praćenje komentara za ponude i odobrenja ponuda i projektnih ugovora
Redigovanjima i odobrenjima ponuda i ugovora o projektima možete da upravljate pomoću Zida za zapise i objava. Vaša organizacija može da kreira prilagođene tokove posla i dodatne komponente za dodeljivanje, preusmeravanje i eskaliranje obaveštenja o radnim stavkama pregleda i odobrenja, kao i da upravlja njima.


[!INCLUDE[footer-include](../includes/footer-banner.md)]