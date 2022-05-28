---
title: Upravljanje podugovorima u aplikaciji Project Operations
description: Ova tema pruža pregled procesa upravljanja podizvođačima od početka do kraja obično u projektnim organizacijama.
author: rumant
ms.date: 08/02/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d595e948b7be9a6822827f4841e737d3c0e1476b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593031"
---
# <a name="subcontract-management-in-project-operations"></a>Upravljanje podugovorima u aplikaciji Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Ova tema pruža pregled procesa upravljanja podizvođačima od početka do kraja u projektnim organizacijama. Podugovaranje usluga obično sledi nakon toka poslovnog procesa koji je prikazan na sledećem dijagramu.

![Tok procesa podugovaranja](../media/SubcontractingProcessFlow.png)

Sledeća lista pruža detaljan opis procesa podugovaranja.

1. Rukovodilac projekta sklapa podugovor sa dobavljačem. Podrazumevano se cenovnici koji su priloženi evidenciji dobavljača koriste za podugovor. Račun dobavljača ima vrstu odnosa **Dobavljač** ili **Dobavljač**.
2. Rukovodilac projekta može da raščlani sve kupovine i stavi ih kao stavke u podugovoru. Stavke podugovora mogu da budu vezane za vreme, troškove ili proizvode. Klasa transakcije koja je izabrana za predmet podugovora određuje čemu ta stavka služi.
3. Menadžer poslovnog kontakta dobavljača i rukovodilac projekta mogu da ponavljaju podugovor. Cene mogu da se prilagode u cenovnicima za kupovinu koji su priloženi podugovoru.
4. U ovom trenutku ili kasnije u toku procesa, ako se stavka podugovora odnosi na vreme, menadžer poslovnog kontakta dobavljača povezuje kontakte sa svakim predmetom podugovora. Ovo povezivanje pruža informacije rukovodiocu projekta koji radi na podugovoru. Kada je kontakt prodavca povezan sa stavkom podugovora, sistem automatski kreira resurs koji može da se rezerviše od kontakta, ako resurs koji može da se rezerviše već ne postoji.
5. Način naplate na svakoj stavci podugovora može da bude **Fiksna cena** ili **Vreme i materijal**. Za predmete podugovora sa fiksnom cenom podešen je raspored faktura na osnovu kontrolnih tačaka.
6.  Nakon što se sklopi podugovor i završe pregovori, on se potvrđuje. Potvrđeni podugovori se ne mogu uređivati, ali ako dođe do promena, podugovor se može „ponovo otvoriti za izmene“, čime se status postavlja iz **Potvrđeno** nazad na **Radna verzija** i pregovori se mogu ponovo otvoriti. 
7.  Prilikom stvaranja generičkog člana tima na projektu, član tima može biti povezan sa predmetom podugovora. Ovo ukazuje na potrebu da se generičkom članu tima pridruže kapaciteti podizvođača.
8.  Imenovani članovi tima mogu se kreirati direktno na projektu ili kreirati rezervisanjem koristeći funkcije planiranja resursa. Ako je imenovani član projektnog tima ugovorni radnik, to je moguće povezati sa predmetom podugovora. Ovo će smanjiti raspoloživ kapacitet na predmetu podugovora.
9.  Resursi podizvođača mogu evidentirati vreme, troškove i potrošnju materijala na projektima i projektnim zadacima, a zatim se mogu podneti na odobrenje. Slično je i sa zaposlenima. Prilikom evidentiranja vremena, radnik po ugovoru može izabrati određeni podugovor i predmet podugovora.
10. Nakon odobrenja, vreme odobreno podugovorima evidentiraće stvarne troškove projekta na osnovu kupovne cene ugovornog radnika ili uloge koje je imao na projektu.
11. Fakture dobavljača i stavke predmeta fakture dobavljača mogu se evidentirati u sistemu za posao koji obavljaju resursi dobavljača ili proizvodi koje dobavljač isporučuje. Redovi fakture dobavljača moraju biti specifični za projekat i za klasu transakcije: vreme, trošak, proizvod/materijal, kontrolna tačka ili naknada. Opciono, redovi fakture dobavljača mogu upućivati na predmet podugovora.
12. Sistem će automatski povezati sve stvarne troškove koji odgovaraju predmetu podugovora i projektu sa fakturom dobavljača. Ovo će olakšati trosmerno podudaranje i proces verifikacije.
13. Menadžer projekta tada može pregledati automatski usklađene stvarne podatke projekta, ukloniti ili dodati druge stvarne podatke o ceni projekta i dovršiti proces verifikacije.
14. Dovršenje procesa verifikacije na svim predmetima označiće fakturu dobavljača kao **Spremno za plaćanje**. U ovoj fazi, faktura dobavljača i predmeti mogu se preneti u sistem Računovodstvo ili Dugovanja radi obrade plaćanja dobavljaču. Prethodno evidentirani troškovi projekta će se poništiti, a stvarni troškovi iz fakture dobavljača će se evidentirati na projektu.

## <a name="quantity-based-subcontract-lines-and-work-based-subcontract-lines"></a>Predmeti podugovora zasnovani na količini i predmeti podugovora zasnovani na poslu

Predmet podugovora može da se zasniva na količini ili na poslu. 

Kada je predmet podugovora **zasnovan na količini**, količina koja se kupuje na predmetu podugovarača za vreme, troškove ili materijal može se koristiti na bilo kojem projektu.

Kada je predmet podugovora **zasnovan na poslu**, predmet podugovora se preslikava na posao koji predstavlja čvor u planu projekta. Vrednost predmeta podugovora je zbir svih komponenti koje su potrebne za isporuku tog dela posla. Oni su modelirani kao detalji o predmetima podugovora i mogu biti skup vremena, troškova ili materijala. Za predmet podugovora zasnovan na poslu, predmet podugovora je takođe posvećen jednom projektu. Operacije projekta ne podržavaju ove tipove podizvođači.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

