---
title: Konfigurišite naplative komponente stavke ponude
description: Ova tema pruža informacije o podešavanju naplativih i nenaplativih komponenata na liniji ponude zasnovanoj na projektu.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ec8a999142fd9960c79ef981e499ae840642e57b269c83d201d2db006179de09
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996003"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Konfigurišite naplative komponente stavke ponude 

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture, Project Operations za scenarije zasnovane na resursima / bez zaliha_

Linija ponude zasnovana na projektu ima koncept *uključenih* komponenti i *naplativih* komponenti.

Uključene komponente podležu:

  - Načinu naplate i podelama klijenata
  - Ograničenja koja ne smeju da se prekorače 
  - Podešavanja učestalosti fakture definisane u liniji ponude zasnovane na projektu

Podskup uključenih komponenti može se označiti kao naplativ pomoću polja **Tip obračuna**. Polje **Tip obračuna** je skup opcija koji omogućava sledeće vrednosti u kontekstu linije ponude:

  - Naplativo
  - Nenaplativo

Komponente koje se naplaćuju mogu se definisati na zadacima, ulogama i kategorijama transakcija.

Naplativost je definisana na zadacima za liniju ponude i odnosi se na sve klase transakcija uključene u tu liniju. Ako je polje **Uključi zadatke** prazno ili postavljeno na **Čitav projekat**, kartica **Zadaci koji se naplaćuju** neće biti dostupna.

Naplativost je definisana u ulogama za liniju ponude i odnosi se samo na klasu transakcija **Vreme**. Ako je polje **Uključi vreme** postavljeno na **Ne** na liniji ponude projekta, kartica **Uloge koje se naplaćuju** neće biti dostupna.

Naplativost je definisana u kategorijama transakcija za liniju ponude i odnosi se samo na klasu transakcija **Trošak**. Ako je polje **Uključi troškove** postavljeno na **Ne** na liniji ponude projekta, kartica **Kategorije koje se naplaćuju** neće biti dostupna.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Ažurirajte projektni zadatak tako da bude naplativ ili nenaplativ

Projektni zadatak može biti naplativ ili nenaplativ u kontekstu određene linije ponude zasnovane na projektu, što omogućava sledeće podešavanje.

Ako linija ponude zasnovana na projektu uključuje **Vreme** i zadatak **T1**, zadatak je povezan sa linijom ponude kao naplativ. Ako postoji druga linija ponude koja uključuje **Troškove**, zadatak **T1** na liniji ponude možete povezati kao nenaplativ. Rezultat je da je sve vreme evidentirano u zadatku naplativo, a svi troškovi evidentirani u zadatku nenaplativi.

Tip naplate zadatka može se konfigurisati na kartici **Naplativi zadaci** stavke ponude zasnovane na projektu ažuriranjem polja **Tip naplate** na podformi **Zadaci stavke ponude**. Pored toga, možete da ažurirate tip naplate za projektni zadatak u polju **Tip naplate** na podformi zadatka Postavljanje obračuna projekta koje prikazuje stavke ponude povezane sa zadatkom.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Ažurirajte ulogu da bude naplativa ili nenaplativa

Uloga može biti naplativa ili nenaplativa u kontekstu određene linije ponude zasnovane na projektu.

Tip naplate uloge se može konfigurisati na kartici **Naplativi zadaci** stavke ponude zasnovane na projektu ažuriranjem polja **Tip naplate** na podformi **Zadaci stavke ponude**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Ažurirajte kategoriju transakcija da bude naplativa ili nenaplativa

Kategorija transakcija može biti naplativa ili nenaplativa na određenoj liniji ponude.

Tip naplate transakcije se može konfigurisati na kartici **Naplative kategorije** stavke ponude zasnovane na projektu ažuriranjem polja **Tip naplate** na podformi **Naplative kategorije**.

### <a name="resolve-chargeability"></a>Rešite naplativost
Procena ili stvarna vrednost kreirana za vreme smatraće se naplativom samo ako važi sledeće:

   - **Vreme** je uključeno u stavku ponude.
   - **Uloga** je konfigurisana kao naplativa u stavki ponude.
   - **Obuhvaćeni zadaci** su podešeni na vrednost **Izabrani zadaci** u stavki ponude. 

Ako su ove tri stvari tačne, **Zadatak** se takođe konfiguriše kao naplativ. 

Procena ili stvarna vrednost za trošak smatra se naplativom samo ako važi sledeće: 

   - **Trošak** je uključen u stavku ponude.
   - **Kategorija transakcije** je konfigurisana kao naplativa u stavki ponude.
   - **Obuhvaćeni zadaci** su podešeni na vrednost **Izabrani zadaci** u stavki ponude.

Ako su ove tri stvari tačne, **Zadatak** se takođe konfiguriše kao naplativ. 

Procena ili stvarna vrednost kreirana za materijal smatraće se naplativom samo ako važi sledeće:

   - **Materijali** su uključeni u stavku ponude.
   - **Obuhvaćeni zadaci** su podešeni na vrednost **Izabrani zadaci** u stavki ponude.

Ako su ove dve stvari tačne, **Zadatak** bi takođe trebalo da se konfiguriše kao naplativ. 


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
Ne može da se podesi </p>
            </td>
            <td width="350" valign="top">
                <p>
Obračun u stvarnom vremenu: Naplativo </p>
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
Naplativo </p>
            </td>
            <td width="350" valign="top">
                <p>
Obračun u stvarnom vremenu: Naplativo </p>
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
Ne može da se podesi </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Naplativo</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Ne može da se podesi </p>
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
Ne može da se podesi </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Nenaplativo</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Ne može da se podesi </p>
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
Ne može da se podesi </p>
            </td>
            <td width="65" valign="top">
                <p>
Ne može da se podesi </p>
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
Ne može da se podesi </p>
            </td>
            <td width="65" valign="top">
                <p>
Ne može da se podesi </p>
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
Ne može da se podesi </p>
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
Ne može da se podesi </p>
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
