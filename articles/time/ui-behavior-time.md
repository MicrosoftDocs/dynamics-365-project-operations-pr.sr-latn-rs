---
title: Ponašanje korisničkog interfejsa za stavku vremena
description: Ovaj članak pruža informacije o ponašanju korisničkog interfejsa za stavku vremena.
author: stsporen
ms.date: 03/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: b39f182901681875eb90f17d9421bcad63762f54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918191"
---
# <a name="time-entry-ui-behavior"></a>Ponašanje korisničkog interfejsa za stavku vremena

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_


Mreža **Sedmična stavka vremena** je prilagođena kontrola koja sadrži dva glavna odeljka, **Dimenzije** i **Trajanje**.

## <a name="keyboard-shortcuts"></a>Tasterske prečice
| Akcija        | Prečica                  |
|------------   |------------------------   |
| Nova           | Alt + Shift + n           |
| Kopiraj red      | Alt + Shift + c           |
| Uredi stavku    | Alt + Shift + e           |
| Uredi red      | Alt + Shift + Ctrl + e    |
| Otvori stavku    | Alt + Shift + o           |
| Prosleđivanje        | Alt + Shift + s           |
| Opozovi        | Alt + Shift + r           |
| Delete        | Alt + Shift + d           |
| Kopiraj sedmicu     | Alt + Shift + w           |

## <a name="dimensions"></a>Dimenzije
Odeljak **Dimenzije** prikazuje dimenzije za koje se vreme može uneti. Sledeće dimenzije su podržane kao unapred definisane:

  - Project
  - Projektni zadatak
  - Uloga
  - Tip
  - Status stavke

Odeljak **Dimenzije** ne dozvoljava unutrašnje uređivanje. Ovaj odeljak je podržan prikazom koji omogućava da se prilagođena polja dodaju u mrežu sedmičnih stavki vremena.

## <a name="duration"></a>Trajanje
Odeljak Trajanje prikazuje dane u nedelji kao zaglavlja kolona. Ovaj odeljak omogućava unutrašnje uređivanje. Kada se kreira red za stavku vremena sa odgovarajućim dimenzijama, korisnici mogu brzo uneti količinu vremena koju su utrošili za te dimenzije.

## <a name="create-a-new-time-entry"></a>Kreiranje nove stavke vremena

1. U mreži stavke vremena, izaberite **Novo**. 
2. U dijalogu **Brzo kreiranje stavke vremena** izaberite datum stavke vremena.
3. Unesite podatke za dimenzije **Projekat**, **Projektni zadatak**, **Uloga** i **Trajanje**. Ove informacije treba dodavati za minute, sate ili dane kucanjem **h**, **m** ili **d**, zajedno sa brojem. 
4. Unesite opis za stavku i sve komentare koji se mogu deliti eksterno u vezi sa stavkom vremena. 

Kada sačuvate stavku, unete vrednosti se prikazuju u odeljku **Dimenzije**. Informacije unete u polje **Trajanje** se pojavljuju za datum za koji je kreirana stavka vremena.

Polja za pronalaženje podržavaju sistemski prikazi. Na primer, nakon što korisnik unese projekat, polje **Projektni zadatak** se podrazumevano podešava na prikaz **Kopiranje**. Da biste kreirali stavke vremena za zadatke koji nisu dodeljeni korisniku, izaberite **Promeni prikaz** u dijalogu za pretraživanje, a zatim izaberite **Svi zadaci aktivnog projekta**.

## <a name="edit-a-time-entry"></a>Uređivanje stavke vremena 
Detalji iz nekih polja na stranici za stavku vremena, kao što su **Opis** i **Spoljni komentari**, nisu prikazani u mreži sedmičnih stavki vremena. Umesto toga, u ćelijama **Trajanje** prikazuje se mali trouglasti indikator koji ima ove dodatne detalje. 

1. Da biste uredili stavku vremena, izaberite ćeliju koju želite da ažurirate u stavci vremena.
2. Izaberite **Uredi detalje** da biste ažurirali podatke u oknu **Glavni obrazac za unos vremena**. 

## <a name="copy-a-time-entry-row"></a>Kopiranje reda stavke vremena
Kada se kreira prvi red, možete izabrati **Kopiraj red** da biste iskopirali ceo red u novi red. Kada se red kopira na ovaj način, dimenzije i trajanje se takođe kopiraju. Takođe možete da izaberete **Izmeni red** da biste ažurirali vrednosti dimenzija i trajanja u odeljku **Trajanje**.

## <a name="open-a-time-entry-behavior"></a>Otvaranje ponašanja stavke vremena
Da bi se podržao optimalan i brz unos u najistaknutija polja, mreža sedmičnih stavki vremena pokazuje podskup izabranih dimenzija i trajanja vremena. Da biste videli sve detalje jedne stavke vremena, u delu **Izmena stavke** odaberite **Otvori**.

## <a name="submit-a-time-entry"></a>Prosleđivanje stavke vremena
Možete proslediti jednu stavku vremena ili grupu stavki vremena izborom bloka ćelija ili celog reda stavke vremena, a zatim izborom opcije **Prosledi**. Prosleđene stavke vremena pojavljuju se kao stavke koje čekaju odobrenje na stranici davaoca odobrenja **Odobrenje**. Nakon uspešnog prosleđivanja stavki vremena, one se ne mogu uređivati.

## <a name="recall-a-time-entry"></a>Opozivanje stavke vremena
Možete opozvati stavke vremena koje ste prosledili. Možete da opozovete jednu stavku vremena, blok stavki vremena ili čitav red stavki vremena. Opozvane stavke vremena možete uređivati.

## <a name="time-entry-status"></a>Status stavke vremena

- **Radna verzija**: Novim stavkama vremena automatski se dodeljuje status **Radna verzija**. Samo stavke vremena koje imaju status **Radna verzija** možete da izbrišete.
- **Prosleđeno**: Kada se prosledi stavka vremena, status se ažurira na **Prosleđeno**. 
- **Odobreno**: Kada se prosleđena stavka vremena odobri, status se ažurira na **Odobreno**. 
- **Vraćeno**: Ako je stavka vremena odbijena, status se ažurira na **Vraćeno** i stavka postaje dostupna za ispravku i ponovno prosleđivanje. 

## <a name="view-rejection-comments"></a>Pregled komentara o odbacivanju
Kada davalac odobrenja odbaci stavku vremena, može da doda komentare o kako bi pomogao resursu da shvati razlog odbacivanja. Da biste videli komentare o odbacivanju stavke vremena, izaberite **Otvori stavku**. Komentari o odbacivanju biće prikazani na vremenskoj osi. Korisnik može odgovoriti na komentare o odbijanju pre nego što ponovo pošalje stavku.

## <a name="copy-week"></a>Kopiraj sedmicu
Nakon kreiranja nekoliko stavki vremena, korisnici mogu istovremeno kreirati više stavki vremena.

1. U obrascu **Stavke vremena** izaberite **Kopiraj nedelju** da biste grupno kreirali dodatne stavke vremena. 
2. U dijalogu **Kopiranje**, u odeljku **Od perioda** koristite polja **Datum početka** i **Datum završetka** da definišete opseg datuma iz kojeg treba kopirati stavke vremena. 
3. U odeljku **U period**, u polju **Datum početka**, odredite datum za koji ćete kreirati stavke vremena. 
4. Izaberite **Kopiraj**. Za određeni datum u odeljku **Do perioda**, kreira se kopija stavki vremena za odgovarajući dan u nedelji u odeljku **Od perioda**. Na primer, stavka vremena za ponedeljak iz prošle nedelje se kopira u ponedeljak one sedmice koja je navedena kao **Do perioda**.

## <a name="import"></a>Uvoz
Isti osnovni postupak koristi se za uvoz iz rezervacija, dodela i razmena. Možete odrediti opseg datuma rezervacija za uvoz, a zatim eksplicitno izabrati rezervacije koje bi trebalo da budu kreirane kao radne verzije stavki vremena. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
