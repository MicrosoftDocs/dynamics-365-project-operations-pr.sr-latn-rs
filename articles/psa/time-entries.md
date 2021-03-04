---
title: Kreiranje stavki vremena
description: Ova tema pruža informacije o tome kako da kreirate stavke vremena.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
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
ms.openlocfilehash: 520d3a6e6cc3d486d778c66c2ef7fd3ff20cd582
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149695"
---
# <a name="create-time-entries"></a>Kreiranje stavki vremena

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

U prethodnim verzijama aplikacije Dynamics 365 Project Service Automation, stavke vremena su unošene jednom nedeljno. U verziji 3 aplikacije Project Service Automation, unose se svakodnevno. Međutim, nakon što je kreirano nekoliko stavki, možete ih grupno kreirati ili kopirati.

## <a name="create-a-time-entry"></a>Kreiranje stavke vremena

Sledite ove korake za kreiranje stavke vremena.

1. Na stranici **Stavke vremena** izaberite **Novo**.
2. U dijalog **Brzo kreiranje stavke vremena** unesite trajanje stavke u minutima, satima ili danima. Trajanje mora da se unese u nekom od ovih formata: *x* minuta, *x* sati ili *x* dana. Sati i dani takođe mogu da se unose kao decimalne vrednosti, na primer *x.x* sati ili *x.x* dana.
3. Izaberite vrstu stavke vremena i projekat za koji je unosite.
4. U polju **Projektni zadatak** pronađite zadatak za ovu stavku.

    > [!NOTE]
    > Ako kreirate stavku vremena za zadatak koji nije dodeljen korisniku, u polju **Projektni zadatak** izaberite dugme **Pretraži**, odaberite **Promeni prikaz**, a zatim **Svi aktivni zadaci projekta** da biste videli listu svih zadataka.

5. Unesite opis, ako je potreban opis, a zatim izaberite **Sačuvaj i zatvori**.

Nakon što je stavka vremena kreirana i sačuvana, možete je urediti u mreži za stavke vremena. Mreža za stavke vremena podržava dva formata:

- Možete uneti stavke vremena u formatu **hh:mm**. Ovaj format se zatim pretvara u sate i decimalne vrednosti.
- Možete direktno uneti sate i decimalne vrednosti.

Imajte na umu da decimalne vrednosti sata nisu minuti. Stoga 1,5 sat predstavlja 1 sat i 30 minuta. Isto pravilo važi za decimalne vrednosti dana. Jedan dan ima 24 sata, pa 0,5 dana predstavlja 12 sati.

## <a name="bulk-create-time-entries"></a>Grupno kreiranje stavki vremena

Nakon kreiranja nekoliko stavki vremena, možete ih kopirati da biste grupno kreirali dodatne stavke vremena.

1. Na stranici **Stavke vremena** izaberite **Kopiraj nedelju**.
2. U grupi polja **Iz perioda** u poljima **Datum početka** i **Datum završetka** definišite opseg datuma iz kojeg treba kopirati stavke vremena.
3. U grupi polja **U period**, u okviru polja **Datum početka**, odredite datum za koji ćete kreirati stavke vremena.
4. Izaberite **Kopiraj** da biste kreirali kopiju stavki vremena koja odgovara danu u nedelji koji je naveden u grupi polja **U period**. Na primer, stavka vremena za ponedeljak iz prošle nedelje se kopira u ponedeljak one sedmice koja je navedena u grupi polja **U period**.

## <a name="import-data-for-time-entries"></a>Uvoz podataka za stavke vremena

Možete da uvezete podatke iz rezervacija i zadataka za projekte. Kada uvezete podatke, možete odrediti opseg datuma rezervacija za uvoz, a zatim eksplicitno odabrati rezervacije koje bi trebalo da budu kreirane kao stavke vremena **Radna verzija**.

## <a name="group-by-sort-search-and-filter-capabilities"></a>Mogućnosti grupisanja prema, sortiranja, pretrage i filtriranja

Možete grupisati i filtrirati stavke vremena prema dimenzijama koje su navedene u kolonama. U polju **Grupiraj prema** odaberite dimenziju za filtriranje stavki vremena. Takođe možete sortirati zapise stavki vremena rastućim ili opadajućim redosledom koristeći strelicu za sortiranje u nazivima kolona. Pored toga, stavke možete prikazati ili sakriti tako što ćete kliknuti na dugme **Filter** u nazivu kolone, a zatim u polje **Pretraga** uneti tekst koji treba da se koristi za pretragu stavki vremena prema nazivu projekta, projektnom zadatku, stavci vremena ili resursu.
