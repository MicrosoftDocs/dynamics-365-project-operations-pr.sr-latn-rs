---
title: Kreiranje ručnog predračuna – jednostavno
description: Ova tema pruža informacije o kreiranju ručnog predračuna u usluzi Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274205"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Kreiranje ručnog predračuna – jednostavno

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

U usluzi Dynamics 365 Project Operations, profakture se po potrebi mogu kreirati ručno. Možete ručno da kreirate predračun sa stranice lista **Ugovori o projektu** ili sa stranice sa detaljima **Ugovor o projektu**.

##  <a name="project-contracts-list-page"></a>Stranica liste ugovora za projekat

Sa stranice liste **Ugovori o projektu** odaberite jedan ili više projektnih ugovora i kreirajte fakture za sve izabrane zapise.

Sistem proverava koji od izabranih projektnih ugovora ima zaostatak **Spremno za fakturisanje** datiran pre današnjeg datuma. Od tih ugovora sistem kreira radne verzije predračuna. Ako projektni ugovor ima više klijenata, može se kreirati jedna faktura po klijentu i više faktura po ugovoru o projektu.

Sve kreirane fakture projekta su dostupne na stranici **Faktura** u odeljku **Naplata** oblasti **Prodaja**.

## <a name="project-contract-details-page"></a>Stranica sa detaljima ugovora za projekat

Profaktura se takođe može kreirati na stranici sa detaljima **Ugovor o projektu**. Sistem proverava da li projektni ugovor ima zaostatak **Spremno za fakturisanje** datiran pre današnjeg datuma. Od ovih ugovora sistem kreira radne verzije predračuna na osnovu broja klijenata u svakom predmetu ugovora.

Kada se kreira jedan predračun, otvara se stranica **Faktura**. Ako se kreira više faktura za taj ugovor o projektu, otvara se stranica lista **Fakture** sa prikazom svih kreiranih faktura.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]