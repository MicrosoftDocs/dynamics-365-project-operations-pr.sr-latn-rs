---
title: Planiranje rada u programu Microsoft Project pomoću programskog dodatka za Project Service
description: Ova tema pruža informacije o tome kako da koristite programski dodatak Microsoft Project u programu Microsoft Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 01/07/2021
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
ms.openlocfilehash: 0c0ea75d34047f7145466ab427d213c5df27fbed
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014583"
---
# <a name="plan-your-work-in-microsoft-project-with-the-project-service-add-in"></a>Planiranje rada u programu Microsoft Project pomoću programskog dodatka za Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3x](../includes/cc-applies-to-psa-app-3x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] vam olakšava da obavljate planiranje projekata, uključujući procene. Možete da definišete rad tako da troškovi, angažovanje i prodajna vrednost budu jasni kada konačan predlog bude prosleđen.  

Možete da instalirate sistem [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] i da poslove planiranja obavljate u poznatom okruženja programa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Koristite robusne mogućnosti planiranja i upravljanja programa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], a zatim ažurirajte plan projekta u programu Project Service Automation.  

> [!IMPORTANT]
> - Da biste koristili SharePoint upravljanje dokumentima za skladištenje u vašim [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] datotekama za [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projekte, vaš [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] administrator će morati da uključi upravljanje dokumentima. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] je kompatibilan samo sa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional izdanjem.  

## <a name="download-and-install-the-add-in"></a>Preuzmite i instalirajte programski dodatak  
 Pripremite vaše informacije za prijavljivanje u [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Te informacije će vam biti potrebne da biste se povezali sa programa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] na funkciju [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  Iz centra za preuzimanje preuzmite programski dodatak za podržanu verziju usluge of Project Service, verzije [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) ili [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Izaberite vezu za preuzimanje.  

3.  Nakon preuzimanja, izaberite **Da** da biste instalirali programski dodatak.  

## <a name="configure-the-add-in"></a>Konfigurišite programski dodatak  

1. Otvorite [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i izaberite karticu **Project Service**.  

2. Izaberite **Poveži se**.  

3. Unesite informacije za prijavljivanje, a zatim izaberite **Prijavi se**.  

   Sada možete početi sa korišćenjem programskog dodatka.  

## <a name="read-from-a-template"></a>Čitanje iz predloška  
 Čitajte iz predloška koji ste kreirali u funkciji [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] i kopirali u program [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] da biste započeli planiranje projekta. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Kreiranje predloška za projekat (Project Service Automation)](../psa/create-project-template.md)  

1.  Sa kartice **Project Service** izaberite **Čitanje** > **Predložak Project Service Automation projekta**.  

2.  Sa liste izaberite predložak projekta, a zatim izaberite **Otvori**.  

    > [!NOTE]
    >  Podrazumevano, zadaci koji su kopirani iz predloška u projekat su podešeni kao ručno zakazani.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Dodeljivanje [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] uloga resursima projekta  

1.  Otvorite projekat i izaberite traku **Zadatak**.  

2. Izaberite meni **Gantov grafikon**, a zatim izaberite **Lista resursa**.  

3. Na listi resursa izaberite padajući meni **Uloga resursa za Project Service** i odaberite ulogu za Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Obezbedite radnu snagu za projekat pomoću resursa  

1.  Na kartici „Project Service“ izaberite red, pa izaberite **Pronađi resurse**.  

2.  Na ekranu **Rezervacija resursa** izaberite resurs koji želite da koristite za projekat.  

3.  Izaberite **Rezerviši**, a zatim izaberite **U redu**.  

## <a name="publish-your-project"></a>Objavite vaš projekat  
Kada se planiranje projekta završi, sledeći korak je uvoz i objavljivanje projekta u funkciji [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Projekat će se uvesti u funkciju [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Primenjuju se procesi određivanja cena i generisanja tima. Otvorite projekat u funkciji [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] da biste videli da li su tim, procene za projekat i strukturna analiza posla generisani. U sledećoj tabeli je prikazano gde da pronađete rezultate.


|              Microsoft Project                                                           |                      Project Service Automation                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Gantogram**   | Uvozi u [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ekran **Strukturna analiza posla**. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Lista resursa** |   Uvozi u [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ekran **Članovi projektnog tima**.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Koristite upotrebu**    |    Uvozi u [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ekran **Procene projekta**.     |

**Da biste uvozili i objavljivali projekte**  
1. Na kartici **Project Service** dođite do **Objavi** > **Novi Project Service Automation projekat**.  

2. U dijalogu **Objavljivanje u novi projekat u programu Project Service** unesite **Ime projekta** i izaberite **Klijent**.  

3. Opcionalno izaberite **Poveži plan projekta sa funkcijom Project Service Automation** da biste povezali datoteku projekta plana sa funkcijom Project Service Automation.  

4. Izaberite **Objavi**.  

   Povezivanje datoteke projekta sa funkcijom [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] od datoteke projekta pravi glavnu datoteku i podešava strukturnu analizu posla u funkciji [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] na samo za čitanje.  Da biste uneli izmene u plan projekta, potrebno je da ih napravite u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i da ih objavite kao ispravke za funkciju [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Uredite projekat koji je uvezen  
 Da biste uneli promene u plan projekta koji je uvezen u funkciju [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], imate dve opcije:  

- Otvorite glavnu datoteku i izmenite je u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Opozovite vezu datoteke i uredite je direktno u funkciji Project Service. Podrazumevano, projekat koji je bio otpremljen iz programa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] je zaključan i može se uređivati samo u funkciji Project. Da biste uredili datoteku u funkciji [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], potrebno je opozvati vezu datoteke.  

### <a name="edit-in-pn_microsoft_project"></a>Uredite u usluzi [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. U glavnom meniju idite na **Project Service** > **Projekti**.  

2. Sa liste projekata otvorite onaj koji ste kreirali u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Izaberite **Otvori u programu MS Project** sa trake. To će otvoriti povezanu glavnu datoteku u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Raskinite vezu datoteke i uredite je u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. U glavnom meniju idite na **Project Service** > **Projekti**.  

2. Sa liste projekata otvorite onaj koji ste kreirali u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Izaberite **Raskini vezu sa programom MS Project** sa trake.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Otpremanje datoteke projekta u SharePoint ili Office grupe  
 Datoteku projekta možete da otpremite u SharePoint i da je pronađete u okviru opcije „Povezani dokumenti“ za [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projekat.  Administrator mora da konfiguriše SharePoint upravljanje dokumentima i da ga uključite za entitet Projekat. 

 Možete i da otpremite datoteku projekta u [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] ako imate podešenu opciju Office grupe.

### <a name="upload-a-file-for-sharepoint"></a>Otpremanje datoteke za SharePoint  

1. U glavnom meniju idite na **Project Service** > **Otpremi**.  

2. Izaberite **U dokumenta projekta Project Service Automation**.  

3. U dijalogu **Omogući otvaranje u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** izaberite **Da** ili **Ne**.  

   - Ako izaberete **Da**, moći ćete da izaberete **Otvori u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** u rešenju Project Service Automation i da pokrenete [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i učitate datoteku projekta iz SharePoint biblioteke dokumenata.  

   - Ako odaberete **Ne**, veza **Otvori u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** neće funkcionisati.  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] datoteku možete da pronađete u funkciji [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] u okviru opcije **Dokumenti** za određeni [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projekat.  

### <a name="upload-a-file-for-office-groups"></a>Otpremanje datoteke za Office grupe  

1. U glavnom meniju idite na **Project Service** > **Otpremi**.  

2. Izaberite **U dokumenta projekta Project Service Automation**.  

3. U dijalogu **Omogući otvaranje u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** izaberite **Da** ili **Ne**.  

   - Ako izaberete **Da**, moći ćete da izaberete **Otvori u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** u rešenju Project Service Automation, pokrenete [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i učitate datoteku projekta iz SharePoint biblioteke dokumenata.  

   - Ako odaberete **Ne**, veza **Otvori u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** neće funkcionisati.  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] datoteku možete da pronađete u funkciji [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] u okviru opcije **Dokumenti** za određeni [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projekat.  

## <a name="publish--your-project-as-a-template"></a>Objavite svoje projekte kao predložak  
 Možete da sačuvate vaš projekat i da ga ponovo upotrebite tako što ćete ga sačuvati ka predložak projekta u funkciji [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Predlošci projekata su planovi projekta koji mogu ponovo da se koriste u funkciji [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Za više informacija pogledajte [Kreiranje predloška projekta (Project Service Automation)](../psa/create-project-template.md). 

1. Na kartici **Project Service** dođite do **Objavi** > **Novi Project Service Automation predložak**.  

2. U dijalogu **Objavnjivanje u novi projekat u predlošku Project Service** unesite **Ime predloška projekta**.  

3. Opcionalno izaberite **Poveži plan projekta sa funkcijom Project Service Automation** da biste povezali datoteku projekta funkcijom [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Izaberite **Objavi**.  

Povezivanje datoteke projekta sa funkcijom [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] od datoteke projekta pravi glavnu datoteku i podešava strukturnu analizu posla u predlošku za [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] na samo za čitanje.  Da biste uneli izmene u plan projekta, potrebno je da ih napravite u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i da ih objavite kao ispravke za funkciju [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Pročitajte raspored kog je učitao resurs

Kada čitate projekat iz usluge Project Service Automation, kalendar resursa nije sinhronizovan sa klijentom za računare. Ako postoje razlike u trajanju zadatka, naporu ili završetku, to je verovatno zato što resursi i klijent računara nemaju isti kalendar predloška radnih sati primenjen na projekat.


## <a name="data-synchronization"></a>Sinhronizacija podataka
Tabele u ovom odeljku pružaju informacije o sinhronizaciji podataka entiteta između funkcije Project Service Automation i programskog dodatka Microsoft Project za računare.

### <a name="project-task-entity-table"></a>Tabela entiteta projektnog zadatka
Sledeća tabela opisuje kako se podaci entiteta projektnog zadatka sinhronizuju između usluge Project Service Automation i programskog dodatka za računare usluge Microsoft Project.

| **Entitet** | **Polje** | **Microsoft Project sa uslugom Project Service Automation** | **Project Service Automation sa uslugom Microsoft Project** |
| --- | --- | --- | --- |
| Projektni zadatak | Krajnji rok | Synchronized | Nije sinhronizovano |
| Projektni zadatak | Procenjeno angažovanje | Synchronized | Nije sinhronizovano |
| Projektni zadatak | ID MS Project klijenta | Synchronized | Nije sinhronizovano |
| Projektni zadatak | Nadređeni zadatak | Synchronized | Nije sinhronizovano |
| Projektni zadatak | Project | Synchronized | Nije sinhronizovano |
| Projektni zadatak | Projektni zadatak | Synchronized | Nije sinhronizovano |
| Projektni zadatak | Ime projektnog zadatka | Synchronized | Nije sinhronizovano |
| Projektni zadatak | Jedinica za određivanje resursa (neodobreno u verziji 3.0) | Synchronized | Nije sinhronizovano |
| Projektni zadatak | Zakazano trajanje | Synchronized | Nije sinhronizovano |
| Projektni zadatak | Datum početka | Synchronized | Nije sinhronizovano |
| Projektni zadatak | ID za SAP | Synchronized | Nije sinhronizovano |

### <a name="team-member-entity-table"></a>Tabela entiteta člana tima
Sledeća tabela opisuje kako se podaci entiteta člana tima sinhronizuju između usluge Project Service Automation i Micros

| **Entitet** | **Polje** | **Microsoft Project sa uslugom Project Service Automation** | **Project Service Automation sa uslugom Microsoft Project** |
| --- | --- | --- | --- |
| Član tima | ID MS Project klijenta | Synchronized | Nije sinhronizovano |
| Član tima | Ime položaja | Synchronized | Nije sinhronizovano |
| Član tima | projekat | Synchronized | Synchronized |
| Član tima | Projektni tim | Synchronized | Synchronized |
| Član tima | Jedinica za određivanje resursa | Nije sinhronizovano | Synchronized |
| Član tima | Uloga | Nije sinhronizovano | Synchronized |
| Član tima | Časovi radnog vremena | Nije sinhronizovano | Nije sinhronizovano |

### <a name="resource-assignment-entity-table"></a>Tabela entiteta dodele resursa
Sledeća tabela opisuje kako se podaci entiteta dodele resursa sinhronizuju između usluge Project Service Automation i Micros

| **Entitet** | **Polje** | **Microsoft Project sa uslugom Project Service Automation** | **Project Service Automation sa uslugom Microsoft Project** |
| --- | --- | --- | --- |
| Dodela resursa | Datum „Od“ | Synchronized | Nije sinhronizovano |
| Dodela resursa | Čas(ov)a | Synchronized | Nije sinhronizovano |
| Dodela resursa | ID MS Project klijenta | Synchronized | Nije sinhronizovano |
| Dodela resursa | Planirani rad | Synchronized | Nije sinhronizovano |
| Dodela resursa | Project | Synchronized | Nije sinhronizovano |
| Dodela resursa | Projektni tim | Synchronized | Nije sinhronizovano |
| Dodela resursa | Dodela resursa | Synchronized | Nije sinhronizovano |
| Dodela resursa | Zadatak | Synchronized | Nije sinhronizovano |
| Dodela resursa | Datum „Do“ | Synchronized | Nije sinhronizovano |

### <a name="project-task-dependencies-entity-table"></a>Tabela entiteta zavisnih elemenata projektnog zadatka
Sledeća tabela opisuje kako se podaci entiteta zavisnih elemenata projektnog zadatka sinhronizuju između usluge Project Service Automation i Micros

| **Entitet** | **Polje** | **Microsoft Project sa uslugom Project Service Automation** | **Project Service Automation sa uslugom Microsoft Project** |
| --- | --- | --- | --- |
| Zavisnosti projektnih zadataka | Zavisnost projektnog zadatka | Synchronized | Nije sinhronizovano |
| Zavisnosti projektnih zadataka | Tip veze | Synchronized | Nije sinhronizovano |
| Zavisnosti projektnih zadataka | Prethodni zadatak | Synchronized | Nije sinhronizovano |
| Zavisnosti projektnih zadataka | Project | Synchronized | Nije sinhronizovano |
| Zavisnosti projektnih zadataka | Sledeći zadatak | Synchronized | Nije sinhronizovano |

### <a name="additional-resources"></a>Dodatni resursi
 [Vodič za menadžera projekta](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]