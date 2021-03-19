---
title: Napomene programera za odobrenja
description: U ovoj temi se pružaju dodatne informacije programera o radu sa odobrenjima.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290286"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="5d503-103">Napomene programera za odobrenja</span><span class="sxs-lookup"><span data-stu-id="5d503-103">Developer notes for Approvals</span></span>

<span data-ttu-id="5d503-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="5d503-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5d503-105">Dynamics 365 Project Operations uključuje logiku provere koja osigurava tačan prelaz zapisa kroz faze odobrenja.</span><span class="sxs-lookup"><span data-stu-id="5d503-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="5d503-106">Tačni prelazi zapisa osiguravaju:</span><span class="sxs-lookup"><span data-stu-id="5d503-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="5d503-107">Svi podržani redovi se kreiraju u povezanim tabelama, kao što su dnevnici i stvarne vrednosti.</span><span class="sxs-lookup"><span data-stu-id="5d503-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="5d503-108">Davalac odobrenja se označava kao **Davalac odobrenja za projekat** u projektu pre nego što nastavite.</span><span class="sxs-lookup"><span data-stu-id="5d503-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]