---
title: Kreiranje ad-hok avansne uplate za ugovor
description: Ova tema pruža informacije o kreiranju avansa za ugovor po potrebi.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 790a0281f72eff5f241d11da025b5b4af643a567
ms.sourcegitcommit: 250270409412ba4cad95fbd4c345a80d3d2b3e53
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/21/2020
ms.locfileid: "4596028"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract"></a>Kreiranje ad-hok avansne uplate za ugovor

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Microsoft Dynamics 365 Project Operations podržava scenarije fakturisanja koji uključuju pretplatu i avanse. Proces korišćenja **Avansa** u usluzi **Project Operations** je sličan **avansnim** ugovorima. 

Dovršite sledeće korake da biste klijentu fakturisali avans.

1. Idite na stranicu **Ugovor za projekat**, a zatim izaberite karticu **Akontacije i avansi**.
2. U podformi koja sadrži spisak svih prethodno zabeleženih avansa i avansnih plaćanja, izaberite **+ Avans na ugovor za novi projekat**. 

    Otvoriće se obrazac **Brzo kreiranje** za evidentiranje pretplate ili avansa.
    
3. U tabeli u nastavku navedena su polja za beleženje avansa i razmatranja koja treba imati na umu prilikom kreiranja novih:

    | Polje | Opis | Posledični uticaj |
    | --- | --- | --- |
    | **Klijent ugovora za projekat** | Ovo polje označava kojem klijentu na ugovoru će se fakturisati za ovu akontaciju. | Ako imate više klijenata na ugovoru i želite da fakturišete svakom od njih za određenu akontaciju ili avansni iznos, ručno kreirajte avans za svakog klijenta ponaosob. |
    | **Opis** | Opis svrhe ili vremena avansa koji će vam pomoći da ga identifikujete. | Ovaj opis se prikazuje u stavki fakture za ovaj avans. |
    | **Iznos** | Iznos pretplate ili avansa. | Ovaj iznos se prikazuje u stavki fakture za ovaj avans. |
    | **Datum fakture** | Datum na koji se klijentu fakturiše ovaj avans. | Ovo je datum za postupak automatskog kreiranja fakture za kreiranje stavke fakture za ovaj avans. |
    | **Status fakture** | Ovo je podešavanje opcije koje pokazuje da li je ovaj avans dodat radnoj verziji fakture za ovog klijenta. Moguće vrednosti su sledeće:</br>- **Nije spremno za fakturisanje**</br>- **Spremno za fakturisanje** | Kada se avans ili pretplata označi kao **Spremno za fakturisanje**, dodaje se kao vreme stavke na radnoj verziji fakture. Samo potpuno fakturisani avans se može koristiti za usaglašavanje sa projektnim troškovima za sledeći period fakturisanja. |

4. Izaberite **Sačuvaj i zatvori** u dijalogu za brzo kreiranje za beleženje avansa ili pretplate.
