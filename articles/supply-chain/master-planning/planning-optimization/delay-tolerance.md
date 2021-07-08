---
title: Viivituse kõikumine (negatiivsed päevad)
description: See teema annab teavet viivituse kõikumise arvutamise kohta ja selle kohta, kuidas see mõjutab plaanitud tellimuse loomist planeerimise optimeerimises.
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 748e047e89747f2eabccc04a40c79bcb1e6f3dea
ms.sourcegitcommit: f21659f1c23bc2cd65bbe7fb7210910d5a8e1cb9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/24/2021
ms.locfileid: "6306459"
---
# <a name="delay-tolerance-negative-days"></a><span data-ttu-id="a3878-103">Viivituse kõikumine (negatiivsed päevad)</span><span class="sxs-lookup"><span data-stu-id="a3878-103">Delay tolerance (negative days)</span></span>

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="a3878-104">Viivituse kõikumise funktsioon võimaldab planeerimise optimeerimisel arvestada laovarude gruppidele seatud **negatiivsete päevade** väärtust.</span><span class="sxs-lookup"><span data-stu-id="a3878-104">The delay tolerance functionality enables Planning Optimization to consider the **Negative days** value that is set for coverage groups.</span></span> <span data-ttu-id="a3878-105">Seda kasutatakse koondplaneerimisel rakendatud viivituse kõikumise perioodi pikendamiseks.</span><span class="sxs-lookup"><span data-stu-id="a3878-105">It's used to extend the delay tolerance period that is applied during master planning.</span></span> <span data-ttu-id="a3878-106">Sel viisil saate vältida uute tarnetellimuste loomist, kui olemasolev pakkumine suudab nõudlust pärast lühikest viivitust katta.</span><span class="sxs-lookup"><span data-stu-id="a3878-106">In this way, you can avoid creating new supply orders if existing supply will be able to cover the demand after a short delay.</span></span> <span data-ttu-id="a3878-107">Selle funktsiooni eesmärk on määrata, kas antud nõudlusele on mõtet luua uus tarnetellimus.</span><span class="sxs-lookup"><span data-stu-id="a3878-107">The purpose of the functionality is to determine whether it makes sense to create a new supply order for a given demand.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="a3878-108">Funktsiooni sisselülitamine teie süsteemis</span><span class="sxs-lookup"><span data-stu-id="a3878-108">Turn on the feature in your system</span></span>

<span data-ttu-id="a3878-109">Et teha viivituse kõikumise funktsioon süsteemis kättesaadavaks, minge [Funktsioonihaldus](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)ja lülitage sisse *Planeeritud tellimuste negatiivsete päevade* funktsioon.</span><span class="sxs-lookup"><span data-stu-id="a3878-109">To make the delay tolerance functionality available in your system, go to [Feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Negative days for Planning Optimization* feature.</span></span>

## <a name="delay-tolerance-in-planning-optimization"></a><span data-ttu-id="a3878-110">Viivituse kõikumine plaanimise optimeerimises</span><span class="sxs-lookup"><span data-stu-id="a3878-110">Delay tolerance in Planning Optimization</span></span>

<span data-ttu-id="a3878-111">Viivituse kõikumine näitab nende päevade arvu, mis on pärast täitmisaega, millal soovite enne uue varude täiendamist oodata, kui olemasolev tarne on juba planeeritud.</span><span class="sxs-lookup"><span data-stu-id="a3878-111">Delay tolerance represents the number of days beyond the lead time that you're willing to wait before you order new replenishment when existing supply is already planned.</span></span> <span data-ttu-id="a3878-112">Viivituse kõikumine määratletakse kalendripäevade, mitte tööpäevade abil.</span><span class="sxs-lookup"><span data-stu-id="a3878-112">Delay tolerance is defined by using calendar days, not business days.</span></span>

<span data-ttu-id="a3878-113">Koondplaneerimise ajal, kui süsteem arvutab viivituse kõikumise, arvestab see sätet **Negatiivsed päevad**.</span><span class="sxs-lookup"><span data-stu-id="a3878-113">At the time of master planning, when the system calculates the delay tolerance, it considers the **Negative days** setting.</span></span> <span data-ttu-id="a3878-114">**Negatiivsed päevad** saate määrata lehel **Kauba laovarud** või lehel **Laovarude grupid**.</span><span class="sxs-lookup"><span data-stu-id="a3878-114">You can set the **Negative days** value on either the **Coverage groups** page or the **Item coverage** page.</span></span>

<span data-ttu-id="a3878-115">Süsteem seob viivituse kõikumise arvutamise *varaseima täiendamiskuupäevaga*, mis on võrdne tänase kuupäeva ja täitmisajaga.</span><span class="sxs-lookup"><span data-stu-id="a3878-115">The system links the delay tolerance calculation to the *earliest replenishment date*, which equals today's date plus the lead time.</span></span> <span data-ttu-id="a3878-116">Viivituse kõikumine arvutatakse järgmise valemi abil, kus *max()* leiab kahest väärtusest suurema:</span><span class="sxs-lookup"><span data-stu-id="a3878-116">The delay tolerance is calculated by using following formula, where *max()* finds the larger of two values:</span></span>

<span data-ttu-id="a3878-117">*max(varaseim täienduspäev, nõudetähtaeg)* – *nõudetähtaeg* + *negatiivsed päevad*</span><span class="sxs-lookup"><span data-stu-id="a3878-117">*max(Earliest replenishment date, Demand due date)* – *Demand due date* + *Negative days*</span></span>

<span data-ttu-id="a3878-118">See valem tagab, et koondplaneerimine ei loo uusi tarnetellimusi, kui toote täitmisaja jooksul on piisavalt tarneid.</span><span class="sxs-lookup"><span data-stu-id="a3878-118">This formula ensures that master planning doesn't create new supply orders when enough supply exists during the product lead time.</span></span>

> [!NOTE]
> <span data-ttu-id="a3878-119">Viivituse kõikumise arvutamine plaanimise optimeerimises kasutab alati dünaamilist negatiivsete päevade arvutust integreeritud koondplaneerimisest.</span><span class="sxs-lookup"><span data-stu-id="a3878-119">The delay tolerance calculation in Planning Optimization always uses the dynamic negative days calculation from built-in master planning.</span></span> <span data-ttu-id="a3878-120">Säte **Kasuta dünaamilisi negatiivseid päevi** lehel **koondplaneerimise parameetrite** ei mõjuta seda käitumist.</span><span class="sxs-lookup"><span data-stu-id="a3878-120">The **Use dynamic negative days** setting on the **Master planning parameters** page has no effect on this behavior.</span></span>

<span data-ttu-id="a3878-121">Kui olemasolev pakkumine tähendab nõudluse viivitust, mis on arvutatud viivituse kõikumisest väiksem või sellega võrdne, seob plaanimise optimeerimine olemasoleva pakkumise nõudlusega.</span><span class="sxs-lookup"><span data-stu-id="a3878-121">If the existing supply implies a demand delay that is less than or equal to the calculated delay tolerance, Planning Optimization pegs existing supply with the demand.</span></span> <span data-ttu-id="a3878-122">Mõnel juhul on parem nõudlust edasi lükata, kui lõpetada ülepakkumisega.</span><span class="sxs-lookup"><span data-stu-id="a3878-122">In some cases, it's better to delay the demand than to end up with oversupply.</span></span>

<span data-ttu-id="a3878-123">Järgmised alamjaotised pakuvad näiteid, mis näitavad, kuidas viivituse kõikumine mõjutab planeeritud tellimuste loomist plaanimise optimeerimises.</span><span class="sxs-lookup"><span data-stu-id="a3878-123">The following subsections provide examples that show how delay tolerance affects the creation of planned orders in Planning Optimization.</span></span>

### <a name="example-1"></a><span data-ttu-id="a3878-124">Näide 1</span><span class="sxs-lookup"><span data-stu-id="a3878-124">Example 1</span></span>

<span data-ttu-id="a3878-125">Toote konfiguratsioon on järgmine:</span><span class="sxs-lookup"><span data-stu-id="a3878-125">A product has the following configuration:</span></span>

- <span data-ttu-id="a3878-126">**Täitmisaeg:** *10*</span><span class="sxs-lookup"><span data-stu-id="a3878-126">**Lead time:** *10*</span></span>
- <span data-ttu-id="a3878-127">**Negatiivsed päevad:** *2*</span><span class="sxs-lookup"><span data-stu-id="a3878-127">**Negative days:** *2*</span></span>

<span data-ttu-id="a3878-128">Tootel on järgmine pakkumine ja nõudlus:</span><span class="sxs-lookup"><span data-stu-id="a3878-128">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="a3878-129">**Tänane nõudlus:** müügitellimus kogusele 10</span><span class="sxs-lookup"><span data-stu-id="a3878-129">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="a3878-130">**Tarne 12 päevaga:** ostutellimus kogusele 10</span><span class="sxs-lookup"><span data-stu-id="a3878-130">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="a3878-131">Olemasolev pakkumine võib katta nõudluse 12 päeva jooksul ja see periood võrdub viivituse kõikumisega.</span><span class="sxs-lookup"><span data-stu-id="a3878-131">Existing supply can cover the demand within 12 days, and that period equals the delay tolerance.</span></span> <span data-ttu-id="a3878-132">Seetõttu ei looda koondplaneerimise käitamisel plaanitud tellimusi.</span><span class="sxs-lookup"><span data-stu-id="a3878-132">Therefore, when master planning runs, no planned orders are created.</span></span>

### <a name="example-2"></a><span data-ttu-id="a3878-133">Näide 2</span><span class="sxs-lookup"><span data-stu-id="a3878-133">Example 2</span></span>

<span data-ttu-id="a3878-134">Toote konfiguratsioon on järgmine:</span><span class="sxs-lookup"><span data-stu-id="a3878-134">A product has the following configuration:</span></span>

- <span data-ttu-id="a3878-135">**Täitmisaeg:** *10*</span><span class="sxs-lookup"><span data-stu-id="a3878-135">**Lead time:** *10*</span></span>
- <span data-ttu-id="a3878-136">**Negatiivsed päevad:** *0*</span><span class="sxs-lookup"><span data-stu-id="a3878-136">**Negative days:** *0*</span></span>

<span data-ttu-id="a3878-137">Tootel on järgmine pakkumine ja nõudlus:</span><span class="sxs-lookup"><span data-stu-id="a3878-137">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="a3878-138">**Tänane nõudlus:** müügitellimus kogusele 10</span><span class="sxs-lookup"><span data-stu-id="a3878-138">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="a3878-139">**Tarne 12 päevaga:** ostutellimus kogusele 10</span><span class="sxs-lookup"><span data-stu-id="a3878-139">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="a3878-140">Olemasolev pakkumine saab nõudlust katta alles 12 päeva pärast.</span><span class="sxs-lookup"><span data-stu-id="a3878-140">Existing supply can cover the demand only after 12 days.</span></span> <span data-ttu-id="a3878-141">Kuid viivituse lubatud kõikumine on 10 päeva.</span><span class="sxs-lookup"><span data-stu-id="a3878-141">However, the delay tolerance is 10 days.</span></span> <span data-ttu-id="a3878-142">Seepärast luuakse koondplaneerimise käitamisel plaanitud tellimus kogusele 10.</span><span class="sxs-lookup"><span data-stu-id="a3878-142">Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>

### <a name="example-3"></a><span data-ttu-id="a3878-143">Näide 3</span><span class="sxs-lookup"><span data-stu-id="a3878-143">Example 3</span></span>

<span data-ttu-id="a3878-144">Toote konfiguratsioon on järgmine:</span><span class="sxs-lookup"><span data-stu-id="a3878-144">A product has the following configuration:</span></span>

- <span data-ttu-id="a3878-145">**Täitmisaeg:** *10*</span><span class="sxs-lookup"><span data-stu-id="a3878-145">**Lead time:** *10*</span></span>
- <span data-ttu-id="a3878-146">**Negatiivsed päevad:** *2*</span><span class="sxs-lookup"><span data-stu-id="a3878-146">**Negative days:** *2*</span></span>

<span data-ttu-id="a3878-147">Tootel on järgmine pakkumine ja nõudlus:</span><span class="sxs-lookup"><span data-stu-id="a3878-147">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="a3878-148">**Nõudlus 11 päevale:** müügitellimus kogusele 10</span><span class="sxs-lookup"><span data-stu-id="a3878-148">**Demand in 11 days:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="a3878-149">**Tarne 14 päevaga:** ostutellimus kogusele 10</span><span class="sxs-lookup"><span data-stu-id="a3878-149">**Supply in 14 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="a3878-150">Olemasolev pakkumine saab nõudlust katta alles kolme päeva pärast.</span><span class="sxs-lookup"><span data-stu-id="a3878-150">Existing supply can cover the demand only after three days.</span></span> <span data-ttu-id="a3878-151">Kuid viivituse lubatud kõikumine on kaks päeva.</span><span class="sxs-lookup"><span data-stu-id="a3878-151">However, the delay tolerance is two days.</span></span> <span data-ttu-id="a3878-152">(Sel juhul hõlmab viivituse kõikumine ainult kahte negatiivset päeva.</span><span class="sxs-lookup"><span data-stu-id="a3878-152">(In this case, the delay tolerance includes only the two negative days.</span></span> <span data-ttu-id="a3878-153">Nõudluse kuupäeva ei kaasatud, kuna see on pärast toote täitmisaega.) Seepärast luuakse koondplaneerimise käitamisel plaanitud tellimus kogusele 10.</span><span class="sxs-lookup"><span data-stu-id="a3878-153">The demand date isn't included because it's after the product lead time.) Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>
