---
title: Skupovi odobrenja
description: Ova tema objašnjava kako se radi sa skupovima odobrenja, zahtevima i podskupinama tih operacija.
author: stsporen
manager: tfehr
ms.date: 08/10/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 1d9333033eb2b03966c6531d0fd6ad5b878acd93
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323253"
---
# <a name="approval-sets"></a>Skupovi odobrenja

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Skupovi odobrenja grupišu zahteve za odobrenje zajedno u manje podskupove operacija. Ovo grupisanje omogućava da se odobrenja obrađuju prema određenom redosledu po projektu i omogućava ponovni pokušaj i sekvenciranje. Grupisanje zahteva za odobrenje poboljšava pouzdanost i mogućnost praćenja obrade odobrenja za velike brojeve odobrenja.

Skupovi odobrenja ukazuju na celokupni status obrade njihovih povezanih zapisa. Kada se zapis o odobrenju obradi pomoću skupa odobrenja, status zapis se pomera sa **Prosleđen** do **Odobren** i više nije povezan sa skupom odobrenja. Ako zapis ne uspe kada se podnese na odobrenje, ostaće u statusu **Prosleđeno**, a skup odobrenja se označava kao neuspešan. Skup odobrenja evidentira poruku o grešci neuspeha.

## <a name="processing-approvals-and-approval-sets"></a>Obrada odobrenja i skupova odobrenja
Odobrenja koja su u redu za obradu vidljiva su u prikazu **Odobrenja obrade**. Sistem obrađuje sve unose više puta asinhrono, uključujući ponovni pokušaj odobrenja ako prethodni pokušaji nisu uspeli.

Polje **Trajanje skupa odobrenja** evidentira broj pokušaja obrade skupa pre nego što se označi kao neuspešan.

## <a name="failed-approvals-and-approval-sets"></a>Neuspela odobrenja i skupovi odobrenja
Prikaz **Neuspela odobrenja** sadrži sva odobrenja koja zahtevaju intervenciju korisnika. Otvorite povezane evidencije skupova odobrenja da biste identifikovali uzrok neuspeha.
Izbor **Pokušaj ponovo** povećava trajni broj skupova odobrenja, vraća skup odobrenja natrag u status **Obrada** i pokušava da obradi preostale zapise.

## <a name="configure-approval-sets"></a>Konfigurisanje skupova odobrenja

### <a name="enable-the-approval-sets-feature"></a>Omogućavanje funkcije skupova odobrenja
Da biste omogućili funkciju Skupovi odobrenja, uverite se da trenutno nema odobrenja koja se obrađuju.

- Idite na stranicu **Parametri projekta** i izaberite **Kontrola funkcija** > **Omogućavanje modernih odobrenja**.

### <a name="turn-off-the-approval-sets-feature"></a>Isključivanje funkcije skupova odobrenja
Da biste isključili funkciju Skupovi odobrenja, uverite se da trenutno nema odobrenja koja se obrađuju.

- Idite na stranicu **Parametri projekta** i izaberite **Kontrola funkcija** > **Onemogućavanje modernih odobrenja**.

### <a name="configuring-the-asynchronous-threshold"></a>Konfigurisanje asinhrone granične vrednosti 
Kada se kreiraju skupovi odobrenja, obrada se premešta u pozadinu kada izabrani broj zapisa za odobrenje pređe naznačenu graničnu vrednost. Koristite polje **Asinhrona granična vrednost** da konfigurišete kada obradu odobrenja treba izvoditi sinhrono ili asinhrono. Izaberite jednu od sledećih vrednosti:

  - Nula: Svi zahtevi treba da se obrađuju asinhrono. 
  - Brojevi veći od nule: Odobrenja se obrađuju asinhrono samo kada prijavljeni broj odobrenja premaši ovu vrednost.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
