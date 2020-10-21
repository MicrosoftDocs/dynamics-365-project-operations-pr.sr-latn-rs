---
title: Pregled procesa prodaje
description: Ova tema pruža informacije o osnovnim procesima prodaje.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 09/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app: ''
ms.openlocfilehash: e66d96a940f3b22d5d1f3372d2b6767a4482d925
ms.sourcegitcommit: 7750485f8685a2ca5e1b3c165ead24a3b583c447
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/25/2020
ms.locfileid: "3892132"
---
# <a name="sales-processes-overview"></a>Pregled procesa prodaje

Procesi prodaje koji se koriste u organizaciji zasnovanoj na projektima razlikuju se od procesa prodaje koji se koriste u organizaciji zasnovanoj na proizvodima. To je zato što su ciklusi prodaje za organizacije zasnovane na projektima duži i zahtevaju prilagođene tehnike procena za analiziranje i kreiranje ponuda za svaku pogodbu. Dynamics 365 Project Operations koristi neke od sledećih funkcionalnosti koje se koriste u procesu prodaje.

- Zapis Potencijalni klijent se koristi za praćenje procesa prodaje.
- Kvalifikovani potencijalni klijenti se prate kao mogućnosti za poslovanje.
- Pristupa se svim srodnim artefaktima za mogućnost za poslovanje. U ove artefakte spadaju prodajni tim, zainteresovani, verovatnoća, ocena, faze prodaje i poslovni procesi.
- Za mogućnost za poslovanje kreira se više ponuda.
- Ponuda je ima status **Zatvorena kao dobijena** kako bi se kreirala ulazna porudžbina. U aplikaciji Project Operations, ulazna porudžbina je prilagođena i zove se ugovor o projektu.

## <a name="estimate-a-sale"></a>Procena prodaje
Vrednost prodaje se može procenjivati na osnovu projekata koji su prethodno isporučeni i kompleksnosti projekata. Kod projekata koji podrazumevaju proširenja prethodnih projekata ili onih za koje je stručnost prodavca izuzetna i dobro poznata, koriste se obrasci posla. Vi možete da koristite jednostavniji proces procene. Složeniji projekti obično imaju duži način kupovine. Zbog toga u procesu procene prodaje postoji više faza. Početkom procesa prodajni tim koristi informacije menadžera za poslovne kontakte i stručnjaka za određenu temu da bi kreirao procenu na visokom nivou za svaku pojedinačnu komponentu rada koji se nudi. Ove komponente rada su predstavljene u stavkama ponude. 

Možete da kreirate procenu visokog nivoa za ponudu. Na kraju, ova procena na visokom nivou biće zamenjena detaljnijom procenom koja se zasniva na planu projekta koji se kreira korišćenjem standardizovanih predložaka projekta. Ovi predlošci pomažu pri izradi rasporeda i određivanju novčanih vrednosti za ponudu i njene komponente (stavke ponude). 

Možete kreirati više ponuda za projekat i grupisati ih pod jednim zapisom sa mogućnošću za poslovanje. Na kraju, jedna od tih ponuda je označena kao **Zatvorena kao dobijena**, a kreira se ugovor o projektu ili izjava o radu. Ugovor o projektu čuva ugovorenu vrednost za svaku komponentu (predmet ugovora) koju klijent prihvati za isporuku. Izjava o radu se obično kreira kao Microsoft Word dokument. Sve fakture koje se šalju klijentu u toku isporuke projekta upućuju na ugovor o projektu ili izjavu o radu.

Takođe možete da kreirate alternativne ponude pod jednim zapisom mogućnosti za poslovanje ili da podesite sistem tako da se kreira ugovor o projektu kada dobijete ponudu. U tom slučaju, možete priložiti Word dokument koji predstavlja izjavu o radu u zapis ugovora o projektu.

## <a name="configure-the-sales-process"></a>Konfigurisanje procesa prodaje
Možete da koristite tokove poslovnih procesa da biste konfigurisali proces prodaje. Ovi tokovi pružaju vođeni vizuelni interfejs za pomeranje poslova napred kroz faze procesa prodaje.

Na primer, vaše preduzeće može imati sledećih šest faza u procesu prodaje:

1. Kvalifikuj
2. Procena
3. Interna revizija
4. Ugovor
5. Isporuka
6. Zatvaranje
 
Vaša organizacija može da koristi različite entitete za predstavljanje iste pogodbe tokom svog razvoja. Početkom procesa prodaje, pogodbu predstavlja entitet Mogućnost za poslovanje. Kako vreme prolazi i pojavljuje se više detalja, možda ćete koristiti procene visokog nivoa da biste kreirali jednu ili više ponuda. Ako jednu od ovih ponuda pregledaju interno zainteresovani i zainteresovani na strani klijenta, entitet ponude predstavlja pogodbu. Nakon što klijent prihvati ponudu, ugovor o projektu ili izjava o radu predstavlja pogodbu. Da bi podržali ovo ponašanje, tokovi poslovnih procesa su strukturirani tako da je svaka faza u procesu povezana sa drugom tabelom baze podataka.

Fazu **Kvalifikovanje** u procesu prodaje može da podrži entitet mogućnosti za poslovanje. Faze **Procena** i **Interna revizija** može da podržava entitet Ponuda. Faze **Ugovor**, **Isporuka** i **Zatvaranje** može da podrži entitet ugovora o projektu.

Dok pomerate pogodbe kroz faze, od vas će se zatražiti da kreirate odgovarajući zapis entiteta koji će vam pomoći i voditi vas kroz proces. Faze mogu biti uslovne. Na primer, ako zahtevate internu reviziju ponude samo ako ponuda koristi prilagođeni cenovnik, taj uslov možete da konfigurišete u odgovarajućoj fazi poslovnog procesa. Faza **Interna revizija** se zatim prikazuje samo za ponude koje koriste prilagođeni cenovnik. Za sve ostale ponude i pogodbe, fazu **Procena** prati faza **Ugovor**.

> [!NOTE]
> Project Operations ima određene stranice za evidenciju entiteta Mogućnost za poslovanje, Ponuda, Porudžbina i Faktura. Ove zapise morate kreirati koristeći stranice sa informacijama o projektu za ove entitete. U suprotnom, nećete moći da otvorite zapise na stranici **Informacije o projektu**. Ako želite da otvorite zapis sa stranice **Informacije o projektu**, morate izbrisati zapis i ponovo ga kreirati pomoću stranice **Informacije o projektu** na kojoj poslovna logika za svaki od ovih tipova entiteta osigurava da je polje zapisa **Tip** pravilno postavljeno i da su svi obavezni koncepti su pravilno pokrenuti.


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Praćenje revizija ponuda i planova projekta u ciklusu prodaje
U Project Operations ne možete da pratite revizije ponude. Umesto toga, morate označiti postojeću ponudu kao **Zatvorena kao izgubljena**, a zatim kreirati novu ponudu. Možete kopirati ponudu ili klonirati ponudu zasnovanu na projektu.

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a>Praćenje komentara za ponude i odobrenja ponuda i projektnih ugovora
Redigovanjima i odobrenjima ponuda i ugovora o projektima možete da upravljate pomoću Zida za zapise i objava. Vaša organizacija može da kreira prilagođene tokove posla i dodatne komponente za dodeljivanje, preusmeravanje i eskaliranje obaveštenja o radnim stavkama pregleda i odobrenja, kao i da upravlja njima.
