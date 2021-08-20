---
title: Kreirajte predložak projekta
description: Kako da kreirate predložak za projekat u aplikaciji Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 1423dfedccfdc471662581707b4441c9ed477f7c0811ccf3905af8c59f774f77
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990873"
---
# <a name="create-a-project-template-project-service"></a>Kreiranje predloška za projekat (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Predlošci projekta vam štede vreme ako vaše preduzeće redovno licitira za slične tipove projekata. Oni obezbeđuju standardni skup uloga i procenjenih časova za tip projekta. Menadžeri poslovnog kontakta i menadžeri projekta mogu da kreiraju projekte na osnovu predloška projekta ili mogu da kopiraju predložak i naprave svoj sopstveni.  
  
## <a name="components-of-project-template"></a>Komponente predloška projekta
 Predložak projekta se sastoji od tri komponente:  
  
- **Strukturna analiza posla**: Strukturna analiza posla u predlošku projekta ima isti skup elemenata kao i projekat. Možete da kreirate hijerarhiju zadatka, povezujete uloge sa zadatkom, definišete raspored atributa, postavljate zavisnosti i pregledate sve podatke u gantogramu. Strukturna analiza posla u predlošcima projekta takođe podržava režime zadataka za svaki zadatak. Nema razlike između predloška projekta i projekta prilikom kreiranja radnog rasporeda.  
  
- **Procene za projekat**: Procene za projekat u predlošcima funkcionišu na isti način kao u projektima, osim što su cenovnici sa podrazumevanim cenama troškova i prodajnim cenama uvek podrazumevani cenovnici troškova i prodaje definisani u [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parametrima. Ostale funkcionalnosti su iste kao u projektu.  
  
- **Formiranje projektnog tima**: Kada formirate projektni tim za predložak projekta, ne možete rezervisati imenovani resurs u predlošku. Možete da koristite **Generisanje projektnog tima** u strukturnoj analizi posla da biste generisali skup generičkih resursa. Takođe možete navesti potrebne veštine i stručnosti za generičke resurse. U predlošcima projekta nije moguće zameniti generički resurs resursom koji može da se rezerviše.  
  
## <a name="create-a-project-from-a-template"></a>Kreiranje projekta iz predloška  
 Projekat iz predloška možete da kreirate na sledeće načine:  
  
-   Kada kreirate projekat iz ponude, možete odabrati predložak projekta u obrascu za brzo kreiranje projekta.  
  
-   Prilikom kreiranja projekta klikom na **Novi projekat**, obrazac projekta se prikazuje pre nego što sačuvate zapis. Odavde, možete da kliknete na polje **Izaberite predložak** da biste odabrali iz liste unapred definisanih predložaka projekata u vašoj organizaciji.  
  
-   Kliknite na **Kreiraj projekat iz predloška** na stranici **Predložak projekta** da biste kreirali projekat iz predloška.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Kreiranje komponenti predloška u projekat  
 Kada kopirate komponente predloška u projekat, ima nekoliko stvari o kojima bi trebalo da znate.  
  
 **Kopiranje strukturne analize posla**: Kada kopirate strukturnu analizu posla iz predloška projekta, ako projekat ima drugačiji kalendar projekta nego predložak, radno vreme iz kalendara projekta će biti primenjeno na raspored zadataka. Ovim se raspored prilagođava kalendaru koji podržava projekat. Slično, prvi zadatak u strukturnoj analizi posla počinje na datum početka projekta, tako da se ostatak rasporeda hijerarhije zadataka ažurira na osnovu trajanja i zavisnosti navedene u strukturnoj analizi posla za predložak.  
  
 **Kopiranje procena za projekat**: Kada kopirate u sve stavke procene projekta, cenovnici se ažuriraju na osnovu vlasničke jedinice projekta za cenovnik troškova i klijenta za prodajni cenovnik. Troškovi po jedinici i prodajne cene se utvrđuju iz ovih cenovnika na projektima koji su povezani sa entitetom prodaje.  
  
 **Kopiranje projektnog tima**: Kada kopirate projektni tim iz predloška u projekat, kopiraju se svi generički resursi, zajedno sa veštinama i stručnošću definisanim u predlošku. Dodele generičkih resursa takođe se održavaju kao predložak projekta.  
  
### <a name="see-also"></a>Takođe pogledajte  
 [Vodič za menadžera projekta](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]