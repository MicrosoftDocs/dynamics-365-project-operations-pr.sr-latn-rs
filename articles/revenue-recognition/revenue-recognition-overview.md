---
title: Pregled prepoznavanja prihoda
description: Ova tema pruža informacije o prepoznavanju prihoda u usluzi Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f5f962572c6ec0298d2d91d33f83e4120a498a6f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013773"
---
# <a name="revenue-recognition-overview"></a>Pregled prepoznavanja prihoda

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

U usluzi Dynamics 365 Project Operations, principi prepoznavanja prihoda variraju u zavisnosti od izabranog načina obračuna za projekat ili deo projekta. Ova tema pruža informacije o prepoznavanju prihoda u usluzi Project Operations.

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>Preuzete transakcije koristeći način naplate za vreme i materijal

- Povezani su prepoznavanje troškova i prihoda. Troškovi transakcije i nefakturisane prodaje knjiže se pomoću [Project Operations dnevnika integracije](../project-accounting/project-operations-integration-journal.md).
- Profil troškova i prihoda projekta određuje da li se nefakturisane prodajne transakcije knjiže u glavnu knjigu. Ako je izabran **Pripadajući prihod**, sistem koristi konta za **WIP prodajnu vrednost** i **Vrednost prodaje ostvarenog prihoda** tokom knjiženja. Sledeće je primer ovog načina.  

  | Tip transakcije | Zaduženje/Odobrenje | Iznos |
  | --- | --- | --- |
  | Prodajna vrednost za rad na projektu | Zaduženje | 100 |
  | Vrednost prodaje za obračunati prihod | Odobrenje | 100 |

- Prihod se prepoznaje pri fakturisanju. Sistem koristi konto **Fakturisani prihod** tokom knjiženja. Sledeće je primer ovog načina.  

  | Tip transakcije | Zaduženje/Odobrenje | Iznos |
  | --- | --- | --- |
  | Bilans klijenta | Zaduženje | 120 |
  | Dugovani porez na promet | Odobrenje | 20 |
  | Fakturisani prihod | Odobrenje | 100 |

- Ako je prihod nastao prilikom knjiženja nefakturisane prodaje, sistem će stornirani ostvareni prihod prilikom fakturisanja.

  | Tip transakcije | Zaduženje/Odobrenje | Iznos |
  | --- | --- | --- |
  | Prodajna vrednost za rad na projektu | Odobrenje | 100 |
  | Vrednost prodaje za obračunati prihod | Zaduženje | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>Preuzete transakcije koristeći način naplate fiksne cene

- Prepoznavanje troškova i prihoda su zasebni. Trošak transakcije se knjiži pomoću [Project Operations dnevnika integracije](../project-accounting/project-operations-integration-journal.md). Nefakturisane prodajne transakcije se ne kreiraju.
- Prihod može biti prepoznat tokom fakturisanja ako trošak proizvoda i profil prihoda imaju **Princip korišćen za izračunavanja dovršetka projekta** podešen na **Nije rad na projektu**. Ovaj način koristite samo za kratkoročne, jednostavne projekte.
- Prihod možete priznati pomoću procene prihoda sa fiksnom cenom, bilo sa načinom **Završen ugovor** ili **Priznavanje prihoda po procentu dovršenja**.

## <a name="additional-resources"></a>Dodatni resursi
[Članak o konfigurisanju računovodstva za naplative projekte](../project-accounting/configure-accounting-billable-projects.md)

[Procena prihoda projekata sa fiksnom cenom](rev-rec-percentage-completion-method.md)

[Upravljanje procenama prihoda](rev-rec-completed-contract-method.md)

[Metodi od troška do dovršetka](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]