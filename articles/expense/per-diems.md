---
title: Dnevnice
description: Ova tema pruža informacije o pravilima dnevnica koja se koriste u upravljanju troškovima.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 7d1c4ac7781cb711e2cc0d09606d422b4dd554f3
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908542"
---
# <a name="per-diems"></a><span data-ttu-id="c0203-103">Dnevnice</span><span class="sxs-lookup"><span data-stu-id="c0203-103">Per diems</span></span>

<span data-ttu-id="c0203-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="c0203-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="c0203-105">Dnevnica je nadoknada koja se isplaćuje radniku koji putuje zbog posla.</span><span class="sxs-lookup"><span data-stu-id="c0203-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="c0203-106">U upravljanju troškovima možete kreirati pravila za dnevnice za različite situacije putovanja.</span><span class="sxs-lookup"><span data-stu-id="c0203-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="c0203-107">Iznosi dnevnica mogu se zasnivati na dobu godine, lokaciji putovanja ili oboje.</span><span class="sxs-lookup"><span data-stu-id="c0203-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="c0203-108">Kada kreirate pravilo za dnevnicu, možete da odredite da se procenat dnevnice zadržava ako radnik dobije besplatne obroke ili usluge.</span><span class="sxs-lookup"><span data-stu-id="c0203-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="c0203-109">Takođe možete da odredite minimalni i maksimalni broj sati za koji dnevnica može da se primenjuje na putovanje radnika.</span><span class="sxs-lookup"><span data-stu-id="c0203-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="c0203-110">Konfigurisanje</span><span class="sxs-lookup"><span data-stu-id="c0203-110">Configuration</span></span> 

1. <span data-ttu-id="c0203-111">Da biste dodali lokacije za dnevnice, idite na **Podešavanje** > **Proračuni i šifre** > **Lokacije za dnevnice**.</span><span class="sxs-lookup"><span data-stu-id="c0203-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="c0203-112">Za svaku od gore dodatih lokacija izaberite iznos dnevnice i valutu koja važi između određenog datuma početka i završetka za hotel, obroke i ostale troškove.</span><span class="sxs-lookup"><span data-stu-id="c0203-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="c0203-113">Stope dnevnica i valute su konfigurisane u odeljku **Podešavanje** > **Proračuni i šifre** > **Dnevnice**.</span><span class="sxs-lookup"><span data-stu-id="c0203-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="c0203-114">Na stranici **Lokacije za dnevnice**, konfigurišite nivoe iznosa dnevnica.</span><span class="sxs-lookup"><span data-stu-id="c0203-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="c0203-115">Nivoi iznosa dnevnica omogućavaju vam da definišete procentualnu podelu dnevne nadoknade za hotel, obroke i druge troškove.</span><span class="sxs-lookup"><span data-stu-id="c0203-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="c0203-116">Da biste odredili smanjenje procenta obroka za doručak, ručak ili večeru, ažurirajte polja na stranici **Parametri upravljanja troškovima** na kartici **Dnevnice**.</span><span class="sxs-lookup"><span data-stu-id="c0203-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="c0203-117">Prosleđivanje troškova korišćenjem dnevnica</span><span class="sxs-lookup"><span data-stu-id="c0203-117">Submit expenses using per diem</span></span>
<span data-ttu-id="c0203-118">Da biste prosledili troškove koristeći dnevnice, koristite kategoriju troška **Dnevnica** kada kreirate izveštaj o troškovima.</span><span class="sxs-lookup"><span data-stu-id="c0203-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="c0203-119">Unesite **početni datum dnevnice**, **krajnji datum dnevnice** i **lokaciju dnevnice**.</span><span class="sxs-lookup"><span data-stu-id="c0203-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="c0203-120">Iznos će se izračunati na osnovu iznosa dnevnice za izabranu lokaciju, a smanjenje obroka na osnovu nivoa dnevnica.</span><span class="sxs-lookup"><span data-stu-id="c0203-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>
