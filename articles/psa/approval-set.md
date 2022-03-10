---
title: Skupovi odobrenja u aplikaciji Project Service Automation
description: Ova tema pruža informacije o skupu odobrenja, zahtevima i podskupovima tih operacija.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9a7a9efbd8615f4923c6795a16c9cf98a40362b6
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323568"
---
# <a name="approval-sets-in-project-service-automation"></a>Skupovi odobrenja u aplikaciji Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Skupovi odobrenja grupišu zahteve za odobrenje zajedno u manje podskupove operacija. Ovo grupisanje omogućava obradu odobrenja u redosledu po projektu i omogućava ponovne pokušaje i sekvenciranja. Grupisanje poboljšava pouzdanost i sledljivost obrade odobrenja za velike količine odobrenja.

Skupovi odobrenja ukazuju na celokupni status obrade njihovih povezanih zapisa. Kada se zapis o odobrenju obrađuje pomoću skupa odobrenja, zapis se premešta sa **Prosleđeno** na **Odobreno** i raskida se njegova veza sa skupom odobrenja. Ako zapis ne uspe kada se podnese na odobrenje, ostaće u statusu **Prosleđeno**, a skup odobrenja se označava kao neuspešan. Skup odobrenja evidentira poruku o grešci neuspeha.

## <a name="processing-approvals-and-approval-sets"></a>Obrada odobrenja i skupova odobrenja
Odobrenja koja su u redu za obradu vidljiva su u prikazu **Odobrenja obrade**. Sistem pokušava da obradi sve stavke više puta asinhrono, uključujući ponovni pokušaj odobrenja ako prethodni pokušaji nisu uspeli.

Polje **Trajanje skupa odobrenja** evidentira broj pokušaja obrade skupa pre nego što se označi kao neuspešan.

## <a name="failed-approvals-and-approval-sets"></a>Neuspela odobrenja i skupovi odobrenja
Prikaz **Neuspela odobrenja** navodi sva odobrenja koja zahtevaju intervenciju korisnika. Otvorite povezane evidencije skupova odobrenja da biste identifikovali uzrok neuspeha.
Izbor **Pokušaj ponovo** povećava trajni broj skupova odobrenja, vraća skup odobrenja natrag u status **Obrada** i pokušava da obradi preostale zapise.

## <a name="configure-approval-sets"></a>Konfigurisanje skupova odobrenja

###  <a name="enable-the-approval-sets-feature"></a>Omogućavanje funkcije skupova odobrenja
Da biste omogućili funkciju Skupovi odobrenja, uverite se da trenutno nema odobrenja koja se obrađuju.

- Idite na stranicu **Parametri projekta** i izaberite **Kontrola funkcija** > **Omogućavanje modernih odobrenja**.

### <a name="turn-off-the-approval-sets-feature"></a>Isključivanje funkcije skupova odobrenja
Da biste isključili funkciju Skupovi odobrenja, uverite se da trenutno nema odobrenja koja se obrađuju.

- Idite na stranicu **Parametri projekta** i izaberite **Kontrola funkcija** > **Onemogućavanje modernih odobrenja**.

### <a name="configuring-the-asynchronous-threshold"></a>Konfigurisanje asinhrone granične vrednosti 
Kada se kreiraju skupovi odobrenja, obrada se premešta u pozadinu kada izabrani broj zapisa za odobrenje pređe naznačenu graničnu vrednost. Koristite polje **Asinhrona granična vrednost** da konfigurišete kada obradu odobrenja treba izvoditi sinhrono ili asinhrono.
Važeće vrednosti su:

  - Nula: Svi zahtevi treba da se obrađuju asinhrono. 
  - Brojevi veći od nule: Odobrenja se obrađuju asinhrono samo kada prijavljeni broj odobrenja premaši ovu vrednost.

[!INCLUDE[footer-include](../includes/footer-banner.md)]