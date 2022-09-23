---
title: Skupovi odobrenja
description: Ovaj članak sadrži objašnjenja o tome kako se radi sa skupovima odobravanja, zahtevima i podskupovima tih operacija.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: ca205073edbce2b399aab3ae273d635c8af96765
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524934"
---
# <a name="approval-sets"></a>Skupovi odobrenja

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Skupovi odobrenja grupišu zahteve za odobrenje zajedno u manje podskupove operacija. Ovo grupisanje omogućava da se odobrenja obrađuju prema određenom redosledu po projektu i omogućava ponovni pokušaj i sekvenciranje. Grupisanje zahteva za odobrenje poboljšava pouzdanost i mogućnost praćenja obrade odobrenja za velike brojeve odobrenja.

Skupovi odobrenja ukazuju na celokupni status obrade njihovih povezanih zapisa. Kada se zapis o odobrenju obradi pomoću skupa odobrenja, status zapis se pomera sa **Prosleđen** do **Odobren** i više nije povezan sa skupom odobrenja. Ako zapis ne uspe kada se podnese na odobrenje, ostaće u statusu **Prosleđeno**, a skup odobrenja se označava kao neuspešan. Skup odobrenja evidentira poruku o grešci neuspeha.

## <a name="processing-approvals-and-approval-sets"></a>Obrada odobrenja i skupova odobrenja
Odobrenja koja su u redu za obradu vidljiva su u prikazu **Odobrenja obrade**. Sistem obrađuje sve unose više puta asinhrono, uključujući ponovni pokušaj odobrenja ako prethodni pokušaji nisu uspeli.

Polje **Trajanje skupa odobrenja** evidentira broj pokušaja obrade skupa pre nego što se označi kao neuspešan.

Skupovi odobravanja se obrađuju kroz periodičnu aktivaciju na osnovu Cloud Flow-a **·** **pod imenom Project Service - Periodično planiranje skupova odobravanja projekta**. Ovo se nalazi u rešenju nazvanom **"** Operacije **projekta"**. 

Uverite se da je tok aktiviran dovršavanjem sledećih koraka.

1. Kao administrator, prijavite se na [flow.microsoft.com](https://powerautomate.microsoft.com).
2. U gornjem desnom uglu prebacite se na okruženje koje koristite za Dynamics 365 Project Operations.
3. Izaberite **rešenja** da biste nabrajali rešenja koja su instalirana u okruženju.
4. Sa liste rešenja izaberite stavku Operacije **projekta**.
5. Promenite filter iz "Sve **"** u tokove **oblaka**.
6. Proverite da li **je tok projekta – periodično planiranje skupova odobravanja** projekta podešen na " **Dalje"**. Ako nije, izaberite tok, a zatim izaberite **Uključi**.
7. Proverite da li se obrada odvija svakih pet minuta tako što ćete pregledati listu **sistemskih** poslova u oblasti "Postavke **"** u okviru okruženja "Operacije Dataverse projekta".

## <a name="failed-approvals-and-approval-sets"></a>Neuspela odobrenja i skupovi odobrenja
Prikaz **Neuspela odobrenja** sadrži sva odobrenja koja zahtevaju intervenciju korisnika. Otvorite povezane evidencije skupova odobrenja da biste identifikovali uzrok neuspeha.
Izbor **Pokušaj ponovo** povećava trajni broj skupova odobrenja, vraća skup odobrenja natrag u status **Obrada** i pokušava da obradi preostale zapise.

## <a name="configure-approval-sets"></a>Konfigurisanje skupova odobrenja

### <a name="enable-the-approval-sets-feature"></a>Omogućavanje funkcije skupova odobrenja
Da biste omogućili funkciju Skupovi odobrenja, uverite se da trenutno nema odobrenja koja se obrađuju. Kada je ova funkcija omogućena, ne može se onemogućiti.

- Idite na stranicu **Parametri projekta** i izaberite **Kontrola funkcija** > **Omogućavanje modernih odobrenja**.

### <a name="configuring-the-asynchronous-threshold"></a>Konfigurisanje asinhrone granične vrednosti 
Kada se kreiraju skupovi odobrenja, obrada se premešta u pozadinu kada izabrani broj zapisa za odobrenje pređe naznačenu graničnu vrednost. Koristite polje **Asinhrona granična vrednost** da konfigurišete kada obradu odobrenja treba izvoditi sinhrono ili asinhrono. Izaberite jednu od sledećih vrednosti:

  - Nula: Svi zahtevi treba da se obrađuju asinhrono. 
  - Brojevi veći od nule: Odobrenja se obrađuju asinhrono samo kada prijavljeni broj odobrenja premaši ovu vrednost.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
