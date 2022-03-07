---
title: Konfigurisanje naplativih komponenti za predmet ugovora zasnovan na projektu
description: Ova tema pruža informacije o tome kako dodati naplative komponente u predmete ugovora u usluzi Project Operations.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d18e56f29457151e07636b67ff8d9b184bf5014ef0ceeef9bb9d322672be4335
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003473"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Konfigurisanje naplativih komponenti za predmet ugovora zasnovan na projektu

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture, Project Operations za scenarije zasnovane na resursima / bez zaliha_

Predmet ugovora zasnovan na projektu ima *uključene* komponente i *naplative* komponente.

Uključene komponente su komponente koje podležu:

  - Načinu naplate i podelama klijenata
  - Ograničenja koja ne smeju da se prekorače 
  - Postavke učestalosti fakture definisane u predmetu ugovora zasnovanog na projektu

Podskup uključenih komponenti može se označiti kao naplativ pomoću polja **Tip obračuna**. Polje **Tip obračuna** je skup opcija koji omogućava sledeće vrednosti u kontekstu predmeta ugovora:

  - Naplativo
  - Nenaplativo

Komponente koje se naplaćuju mogu se definisati na zadacima, ulogama i kategorijama transakcija.

Naplativost je definisana na zadacima za predmet ugovora o projektu i odnosi se na sve klase transakcija uključene u liniju. Ako je polje **Uključi zadatke** na predmetu ugovora prazno ili postavljeno na **Čitav projekat**, kartica **Zadaci koji se naplaćuju** neće biti dostupna.

Naplativost definisana u ulogama za predmet ugovora o projektu odnosi se samo na klasu transakcija **Vreme**. Ako je polje **Uključi vreme** na predmetu ugovora postavljeno na **Ne**, kartica **Uloge koje se naplaćuju** neće biti dostupna.

Naplativost definisana u kategorijama transakcija za predmet ugovora o projektu odnosi se samo na klasu transakcija **Trošak**. Ako je polje **Uključi troškove** postavljeno na **Ne**, kartica **Kategorije koje se naplaćuju** neće biti dostupna.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Ažurirajte projektni zadatak kao naplativi ili nenaplativi

Projektni zadatak može biti naplativ ili nenaplativ na određenom predmetu ugovora, što omogućava sledeće podešavanje:

Ako predmet ugovora zasnovan na projektu uključuje **Vreme** i određeni zadatak, **T1** je povezan sa njim kao naplativ. Ako postoji drugi predmet ugovora koji uključuje **Trošak**, zadatak T1 na predmetu ugovora liniji možete povezati kao nenaplativ. Rezultat je da je sve vreme evidentirano u zadatku naplativo, a svi troškovi nenaplativi.

Tip naplate zadatka može se konfigurisati na kartici **Zadaci koji se naplaćuju** predmeta ugovora ažuriranjem polja **Tip naplate** na podformi zadataka predmeta ugovora. Pored toga, možete da ažurirate polje **Tip naplate** na podformi zadatka Postavljanje obračuna projekta koje prikazuje predmete ugovora povezane sa zadatkom.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Ažurirajte ulogu kao naplativu ili nenaplativu

Uloga može biti naplativa ili nenaplativa na određenom predmetu ugovora.

Tip obračuna uloge može se konfigurisati na kartici **Uloge koje se naplaćuju** predmeta ugovora. Da biste to uradili, ažurirajte polje **Tip naplate** na podformi **Naplative uloge**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Ažurirajte kategoriju transakcija kao naplativu ili nenaplativu

Kategorija transakcija može biti naplativa ili nenaplativa na određenom predmetu ugovora.

Tip obračuna transakcije može se konfigurisati na kartici **Kategorije koje se naplaćuju** predmeta ugovora zasnovanom na projektu. Da biste to uradili, ažurirajte polje **Tip naplate** na podformi **Naplative kategorije**.

### <a name="resolve-chargeability"></a>Rešite naplativost

Procena ili stvarna vrednost kreirana za vreme smatra se naplativom samo ako važi sledeće:

   - **Vreme** je uključeno u predmet ugovora.
   - **Uloga** je konfigurisana kao naplativa u predmetu ugovora.
   - **Obuhvaćeni zadaci** su podešeni na vrednost **Izabrani zadaci** u predmetu ugovora.
 
 Ako su ove tri stvari tačne, zadatak se konfiguriše kao naplativ. 

Procena ili stvarna vrednost za trošak smatra se naplativom samo ako važi sledeće:

   - **Trošak** je uključen u predmet ugovora
   - **Kategorija transakcije** je konfigurisana kao naplativa u predmetu ugovora
   - **Obuhvaćeni zadaci** su podešeni na vrednost **Izabrani zadatak** u predmetu ugovora
  
 Ako su ove tri stvari tačne, **Zadatak** se konfiguriše kao naplativ. 

Procena ili stvarna vrednost za materijal smatra se naplativom samo ako važi sledeće:

   - **Materijali** su uključeni u predmet ugovora
   - **Obuhvaćeni zadaci** su podešeni na vrednost **Izabrani zadaci** u predmetu ugovora

Ako su ove dve stvari tačne, **Zadatak** se konfiguriše kao naplativ. 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Sadrži vreme</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Sadrži trošak</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Sadrži materijale</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>Obuhvaćeni zadaci</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Uloga</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Kategorija</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Zadatak</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>Uticaj naplativosti</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Čitav projekat </p>
            </td>
            <td width="65" valign="top">
                <p>
Naplativo </p>
            </td>
            <td width="70" valign="top">
                <p>
Naplativo </p>
            </td>
            <td width="65" valign="top">
                <p>
Nije moguće podesiti </p>
            </td>
            <td width="350" valign="top">
                <p>
Obračun u stvarnom vremenu: <strong>Naplativo</strong>
                </p>
                <p>
Tip obračuna na stvarnom trošku: <strong>Naplativo</strong>
                </p>
                <p>
Tip obračuna na stvarnom materijalu: <strong>Naplativo</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Samo izabrani zadaci </p>
            </td>
            <td width="65" valign="top">
                <p>
Naplativo </p>
            </td>
            <td width="70" valign="top">
                <p>
Naplativo </p>
            </td>
            <td width="65" valign="top">
                <p>
Naplativo </p>
            </td>
            <td width="350" valign="top">
                <p>
Obračun u stvarnom vremenu: <strong>Naplativo</strong>
                </p>
                <p>
Tip obračuna na stvarnom trošku: <strong>Naplativo</strong>
                </p>
                <p>
Tip obračuna na stvarnom materijalu: <strong>Naplativo</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Samo izabrani zadaci </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nenaplativo</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Naplativo </p>
            </td>
            <td width="65" valign="top">
                <p>
Naplativo </p>
            </td>
            <td width="350" valign="top">
                <p>
Obračun u stvarnom vremenu: <strong>Nenaplativo</strong>
                </p>
                <p>
Tip obračuna na stvarnom trošku: Naplativo </p>
                <p>
Tip obračuna na stvarnom materijalu: Naplativo </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Samo izabrani zadaci </p>
            </td>
            <td width="65" valign="top">
                <p>
Naplativo </p>
            </td>
            <td width="70" valign="top">
                <p>
Naplativo </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nenaplativo</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Obračun u stvarnom vremenu: <strong>Nenaplativo</strong>
                </p>
                <p>
Tip obračuna na stvarnom trošku: <strong>Nenaplativo</strong>
                </p>
                <p>
Tip obračuna na stvarnom materijalu: <strong>Nenaplativo</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Samo izabrani zadaci </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nenaplativo</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Naplativo </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nenaplativo</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Obračun u stvarnom vremenu: <strong>Nenaplativo</strong>
                </p>
                <p>
Tip obračuna na stvarnom trošku: <strong>Nenaplativo</strong>
                </p>
                <p>
Tip obračuna na stvarnom materijalu: <strong> Nenaplativo</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Samo izabrani zadaci </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nenaplativo</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Nenaplativo</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Naplativo </p>
            </td>
            <td width="350" valign="top">
                <p>
Obračun u stvarnom vremenu: <strong>Nenaplativo</strong>
                </p>
                <p>
Tip obračuna na stvarnom trošku: <strong> Nenaplativo</strong>
                </p>
                <p>
Tip obračuna na stvarnom materijalu: Naplativo </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Čitav projekat </p>
            </td>
            <td width="65" valign="top">
                <p>
Nije moguće podesiti </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Naplativo</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Nije moguće podesiti </p>
            </td>
            <td width="350" valign="top">
                <p>
Obračun u stvarnom vremenu: <strong>Nije dostupno</strong>
                </p>
                <p>
Tip obračuna na stvarnom trošku: Naplativo </p>
                <p>
Tip obračuna na stvarnom materijalu: Naplativo </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Čitav projekat </p>
            </td>
            <td width="65" valign="top">
                <p>
Nije moguće podesiti </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Nenaplativo</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Nije moguće podesiti </p>
            </td>
            <td width="350" valign="top">
                <p>
Obračun u stvarnom vremenu: <strong>Nije dostupno</strong>
                </p>
                <p>
Tip obračuna na stvarnom trošku: <strong> Nenaplativo</strong>
                </p>
                <p>
Tip obračuna na stvarnom materijalu: Naplativo </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Čitav projekat </p>
            </td>
            <td width="65" valign="top">
                <p>
Naplativo </p>
            </td>
            <td width="70" valign="top">
                <p>
Nije moguće podesiti </p>
            </td>
            <td width="65" valign="top">
                <p>
Nije moguće podesiti </p>
            </td>
            <td width="350" valign="top">
                <p>
Obračun u stvarnom vremenu: Naplativo </p>
                <p>
Tip obračuna na stvarnom trošku: <strong>Nije dostupno</strong>
                </p>
                <p>
Tip obračuna na stvarnom materijalu: Naplativo </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Čitav projekat </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nenaplativo</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Nije moguće podesiti </p>
            </td>
            <td width="65" valign="top">
                <p>
Nije moguće podesiti </p>
            </td>
            <td width="350" valign="top">
                <p>
Obračun u stvarnom vremenu: <strong>Nenaplativo</strong>
                </p>
                <p>
Tip obračuna na stvarnom trošku: <strong>Nije dostupno</strong>
                </p>
                <p>
Tip obračuna na stvarnom materijalu: Naplativo </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Čitav projekat </p>
            </td>
            <td width="65" valign="top">
                <p>
Naplativo </p>
            </td>
            <td width="70" valign="top">
                <p>
Naplativo </p>
            </td>
            <td width="65" valign="top">
                <p>
Nije moguće podesiti </p>
            </td>
            <td width="350" valign="top">
                <p>
Obračun u stvarnom vremenu: Naplativo </p>
                <p>
Tip obračuna na stvarnom trošku: Naplativo </p>
                <p>
Tip obračuna na stvarnom materijalu: <strong> Nije dostupno</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Čitav projekat </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nenaplativo</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Nenaplativo</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Nije moguće podesiti </p>
            </td>
            <td width="350" valign="top">
                <p>
Obračun u stvarnom vremenu: <strong>Nenaplativo</strong>
                </p>
                <p>
Tip obračuna na stvarnom trošku:<strong> Nenaplativo </strong>
                </p>
                <p>
Tip obračuna na stvarnom materijalu:<strong> Nije dostupno</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
