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
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483965"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="de436-103">Napomene programera za odobrenja</span><span class="sxs-lookup"><span data-stu-id="de436-103">Developer notes for Approvals</span></span>

<span data-ttu-id="de436-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="de436-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="de436-105">Dynamics 365 Project Operations uključuje logiku provere koja osigurava tačan prelaz zapisa kroz faze odobrenja.</span><span class="sxs-lookup"><span data-stu-id="de436-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="de436-106">Tačni prelazi zapisa osiguravaju:</span><span class="sxs-lookup"><span data-stu-id="de436-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="de436-107">Svi podržani redovi se kreiraju u povezanim tabelama, kao što su dnevnici i stvarne vrednosti.</span><span class="sxs-lookup"><span data-stu-id="de436-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="de436-108">Davalac odobrenja se označava kao **Davalac odobrenja za projekat** u projektu pre nego što nastavite.</span><span class="sxs-lookup"><span data-stu-id="de436-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>
