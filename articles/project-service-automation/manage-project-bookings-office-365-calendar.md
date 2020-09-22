---
title: Upravljanje projektima i rezervacijama u Office 365 kalendaru
description: Kako da upravljate projektima i rezervacijama u Office 365 kalendaru
author: ruhercul
manager: kfend
ms.service: dynamics-365-projectservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 92428956-1058-4490-934f-907fbbdc8f25
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 5c075e0b63db35c1e189a62a6b5b00f5bcb7ea97
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755082"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>Upravljanje projektima i rezervacijama u kalendaru (Project Service)

> [!Note]
> ZASTARELO: Ova funkcija je zastarela i nije više dostupna.

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

Prikažite lične zakazane obaveze, rezervacije projekata i posla, kao i dodele radnih naloga u aplikaciji field service korišćenjem [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] kalendara.  
  
 Kada je sve na jednom mestu, lako je upravljati vašim danom. Vaši sastanci, zakazane obaveze, rezervacije i zadaci su svi dostupni u vašem [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] kalendaru.  
  
 Ako koristite [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], možete uneti i vaše lične zakazane obaveze u prikazu unosa vremena za Project Service. Na taj način menadžeri projekta i resursa znaju vašu dostupnost za projekte. To vam štedi i vreme, jer ne morate da unosite informacije o vašim ličnim zakazanim obavezama dvaput. Možete jednostavno da uvezete lične zakazane obaveze iz kalendara u prikaz unosa vremena u aplikaciji Project Service.  
  
 Vaš kalendara će sinhronizovati projekat i rezervacije radnih naloga od danas do predstojeće četiri nedelje. Ovo podešavanje ne može da se promeni.  
  
 Sinhronizacija je podržana samo u jednom smeru, iz PSA na vaš [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] kalendar. Možete da sinhronizujete obrnutim redosledom. 
  
 Da biste saznali kako da koristite [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] kalendar, pogledajte [Kalendar u programu Outlook na vebu za preduzeća](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936)  
  
## <a name="setup"></a>Instalacija  
 Pre nego što možete da vidite i upravljate rezervacijama u vašem [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] kalendaru, morate da podesite nekoliko stvari.  
  
- Biće vam potrebni akreditivi [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] globalnog administratora ili administratora sistema.  
  
- Vaš administrator će morati da konfiguriše profilu servera e-pošte i svaki korisnik će morati da konfiguriše svoje poštansko sanduče. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Podešavanje obrade e-pošte putem sinhronizacije na strani servera](../admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks.md)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>Uključite sinhronizaciju za organizaciju (zadatak administratora)  
  
1.  U glavnom meniju kliknite na **Podešavanja** > **Administracija**.  
  
2.  Kliknite na **Sistemska podešavanja**.  
  
3.  Kliknite na karticu **Sinhronizacija**.  
  
4.  U okviru opcije **Izaberite da li želite da omogućite sinhronizaciju rezervacije resursa sa** označite **Sinhronizuj rezervaciju resursa sa programom Outlook**.  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>Uključite sinhronizaciju za vaš korisnički profil (zadatak korisnika)  
  
1.  Kliknite na dugme **Podešavanja** u gornjem desnom uglu ekrana.  
  
2.  Kliknite na dugme **Opcije**.  
  
3.  Kliknite na karticu **Sinhronizacija**.  
  
4.  U okviru **Sinhronizacija rezervacije resursa sa programom Outlook**, označite **Sinhronizacija rezervacije resursa sa programom Outlook**.  
  
## <a name="import-your-personal-appointments-user-task"></a>Uvezite vaše lične zakazane obaveze (zadatak korisnika)  
 Možete da uvezete lične zakazane obaveze iz kalendara u prikaz unosa vremena u aplikaciji Project Service Automation.  
  
1. Otvorite [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] kalendar i kliknite na **Uvoz podataka**.  
  
2. Na ekranu Filteri izaberite **Zakazane obaveze iz usluge Exchange**, a zatim kliknite na **Primeni**.  
  
3. Sistem će izvući zakazane obaveze u prikazu unosa vremena kao predloženim unosima za trenutnu nedelju. Da biste dodali stavke za drugu nedelju, kliknite na dugme **Prethodno** ili **Sledeće**.  
  
4. Izaberite zakazanu obavezu koju želite da dodate u prikaz unosa vremena u aplikaciji Project Service Automation.  
  
5. U iskačućem polju **Unos vremena** izaberite odgovarajuće opcije za konvertovanje zakazane obaveze u prikaz unosa vremena u aplikaciji Project Service Automation.  
  
6. Kliknite na **Sačuvaj**.  
  
### <a name="see-also"></a>Takođe pogledajte  
 [Vodič za vreme, trošak i saradnju](../project-service/time-expense-collaboration-guide.md)
