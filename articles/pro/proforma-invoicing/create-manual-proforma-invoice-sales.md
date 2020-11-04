---
title: Kreiranje ručnog predračuna
description: Ova tema pruža informacije o kreiranju ručnog predračuna u usluzi Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/20/2020
ms.locfileid: "4083809"
---
# <a name="creating-a-manual-proforma-invoice"></a>Kreiranje ručnog predračuna

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

U usluzi Dynamics 365 Project Operations, predračuni se po potrebi mogu kreirati ručno. Možete ručno da kreirate predračun sa stranice lista **Ugovori o projektu** ili sa stranice sa detaljima **Ugovor o projektu**.

##  <a name="project-contracts-list-page"></a>Stranica liste ugovora za projekat

Sa stranice liste **Ugovori o projektu** odaberite jedan ili više projektnih ugovora i kreirajte fakture za sve izabrane zapise.

Sistem proverava koji od izabranih projektnih ugovora ima zaostatak **Spremno za fakturisanje** datiran pre današnjeg datuma. Od tih ugovora sistem kreira radne verzije predračuna. Ako projektni ugovor ima više klijenata, može se kreirati jedna faktura po klijentu i više faktura po ugovoru o projektu.

Sve kreirane fakture projekta su dostupne na stranici **Faktura** u odeljku **Naplata** oblasti **Prodaja**.

## <a name="project-contract-details-page"></a>Stranica sa detaljima ugovora za projekat

Predfaktura se takođe može kreirati sa stranice sa detaljima **Ugovor o projektu** , koja kreira fakturu za taj konkretni ugovor o projektu. Sistem proverava da projektni ugovor ima zaostatak **Spremno za fakturisanje** datiran pre današnjeg datuma. Od ovih ugovora sistem kreira radne verzije predračuna na osnovu broja klijenata u svakom predmetu ugovora.

Kada se kreira jedan predračun, otvara se stranica **Faktura**. Ako je za taj ugovor o projektu kreirano više faktura, otvara se stranica liste **Fakture** sa prikazom svih kreiranih faktura.
