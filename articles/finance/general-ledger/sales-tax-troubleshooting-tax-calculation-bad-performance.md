---
title: Maksuarvestuse jõudlus mõjutab kandeid
description: See teema pakub tõrkeotsingu teavet, mis on seotud maksuarvestuse jõudlusega ja selle mõju kannetele.
author: shtao
manager: beya
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7ff9d9b80172c3b337737b1cd53b4c56d1befe57
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947629"
---
# <a name="tax-calculation-performance-affects-transactions"></a><span data-ttu-id="aa6c2-103">Maksuarvestuse jõudlus mõjutab kandeid</span><span class="sxs-lookup"><span data-stu-id="aa6c2-103">Tax calculation performance affects transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa6c2-104">Mõnikord mõjutavad kannet jõudlusprobleemid, mis maksuarvestuses tekivad.</span><span class="sxs-lookup"><span data-stu-id="aa6c2-104">Sometimes, a transaction is affected by performance issues that tax calculation is having.</span></span> <span data-ttu-id="aa6c2-105">Selle probleemi tõrkeotsinguks järgige vastavalt järgmistele jaotistele juhiseid.</span><span class="sxs-lookup"><span data-stu-id="aa6c2-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="review-the-transaction-line-count"></a><span data-ttu-id="aa6c2-106">Vaadake üle tehingu ridade arv</span><span class="sxs-lookup"><span data-stu-id="aa6c2-106">Review the transaction line count</span></span>

<span data-ttu-id="aa6c2-107">Määrake, kas kandel on suur hulk ridu (nt üle mitmesaja).</span><span class="sxs-lookup"><span data-stu-id="aa6c2-107">Determine whether the transaction has a large number of lines (for example, more than several hundred).</span></span> <span data-ttu-id="aa6c2-108">Kui ei, liigu edasi järgmise jaotise juurde.</span><span class="sxs-lookup"><span data-stu-id="aa6c2-108">If it doesn't, move on to the next section.</span></span> <span data-ttu-id="aa6c2-109">Kui kandel on mitusada rida, viivitage maksuarvestusega.</span><span class="sxs-lookup"><span data-stu-id="aa6c2-109">If the transaction does have several hundred lines, delay the tax calculation.</span></span> <span data-ttu-id="aa6c2-110">Lisateavet vt teemast [Luba maksuarvestuse viivitus päevaraamatutes](enable-delayed-tax-calculation.md).</span><span class="sxs-lookup"><span data-stu-id="aa6c2-110">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span> 

<span data-ttu-id="aa6c2-111">Järgmisena saate kindlaks teha, kas mõni järgmistest tingimustest on täidetud:</span><span class="sxs-lookup"><span data-stu-id="aa6c2-111">Next, you can determine whether any of the following conditions are met:</span></span>

- <span data-ttu-id="aa6c2-112">Imporditehinguid tehakse suurtest failidest.</span><span class="sxs-lookup"><span data-stu-id="aa6c2-112">There are import transactions from large files.</span></span>
- <span data-ttu-id="aa6c2-113">Mitu seanssi töötleb sama kande maksuarvestust samal ajal.</span><span class="sxs-lookup"><span data-stu-id="aa6c2-113">Multiple sessions process the same transaction tax calculation at the same time.</span></span>
- <span data-ttu-id="aa6c2-114">Kandel on mitu rida ja vaadet uuendatakse reaalajas.</span><span class="sxs-lookup"><span data-stu-id="aa6c2-114">The transaction has multiple lines, and the views are updated in real time.</span></span> <span data-ttu-id="aa6c2-115">Näiteks välja **Arvutatud käibemaksusumma** lehel **Pearaamat** uuendatakse reaalaja jooksul rea väljade muutudes.</span><span class="sxs-lookup"><span data-stu-id="aa6c2-115">For example, the **Calculated sales tax amount** field on the **General journal** page is updated in real time when a line's fields are changed.</span></span>

   <span data-ttu-id="aa6c2-116">[![Arvutatud käibemaksusumma väli päevaraamatu kviitungi lehel](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="aa6c2-116">[![Calculated sales tax amount field on the Jounal voucher page](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span></span>

<span data-ttu-id="aa6c2-117">Kui mis tahes tingimus on täidetud, viivitage maksuarvestusega.</span><span class="sxs-lookup"><span data-stu-id="aa6c2-117">If any of these conditions are met, delay the tax calculation.</span></span>

## <a name="review-the-call-stack"></a><span data-ttu-id="aa6c2-118">Väljakutsete pinu ülevaatamine</span><span class="sxs-lookup"><span data-stu-id="aa6c2-118">Review the call stack</span></span>

<span data-ttu-id="aa6c2-119">Vaadake väljakutsete pinu üle määramaks, kas maksuarvestust kutsutakse välja mitu korda.</span><span class="sxs-lookup"><span data-stu-id="aa6c2-119">Review the call stack to determine whether tax calculation is called multiple times.</span></span> <span data-ttu-id="aa6c2-120">Kui ei, liigu edasi järgmise jaotise juurde.</span><span class="sxs-lookup"><span data-stu-id="aa6c2-120">If it isn't, move on to the next section.</span></span> <span data-ttu-id="aa6c2-121">Kui väljakutsete pinu on alustatakse mitu korda, järgige neid samme, et vähendada maksuarvestuse aega.</span><span class="sxs-lookup"><span data-stu-id="aa6c2-121">If the call stack is called multiple times, follow these steps to help reduce the tax calculation times.</span></span>

1. <span data-ttu-id="aa6c2-122">Kui päevaraamat on kannet arvesse võtnud, viivitage maksuarvestusega.</span><span class="sxs-lookup"><span data-stu-id="aa6c2-122">If the journal has considered the transaction, delay the tax calculation.</span></span> <span data-ttu-id="aa6c2-123">Lisateavet vt teemast [Luba maksuarvestuse viivitus päevaraamatutes](enable-delayed-tax-calculation.md).</span><span class="sxs-lookup"><span data-stu-id="aa6c2-123">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span>
2. <span data-ttu-id="aa6c2-124">Kui kanne on ostutellimus ja rakenduse versioon on hilisem kui 10.0.15, võite maksuarvestamisega viivitada kuni lõpliku arvestamiseni lubades flighting **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch** jaoks.</span><span class="sxs-lookup"><span data-stu-id="aa6c2-124">If the transaction is a purchase order, and the application version is later than 10.0.15, you can delay the tax calculation until the final calculation by enabling the flighting for **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.</span></span>

## <a name="review-the-call-stack-timeline"></a><span data-ttu-id="aa6c2-125">Väljakutsete pinu ajajoone ülevaatamine</span><span class="sxs-lookup"><span data-stu-id="aa6c2-125">Review the call stack timeline</span></span>

<span data-ttu-id="aa6c2-126">Vaadake üle väljakutsepinu ajajoon, et teada saada, kas järgmised probleemid on olemas.</span><span class="sxs-lookup"><span data-stu-id="aa6c2-126">Review the call stack timeline to determine whether the following issues exist.</span></span> <span data-ttu-id="aa6c2-127">Kui jah, lubage flighting **TaxUncommittedDoIsolateScopeFlighting** probleemi lahendamiseks.</span><span class="sxs-lookup"><span data-stu-id="aa6c2-127">If they do, enable the flighting for **TaxUncommittedDoIsolateScopeFlighting** to fix the issue.</span></span>

- <span data-ttu-id="aa6c2-128">Kande tulemusena lõpetab süsteem vastamise, kuni seanss lõpeb.</span><span class="sxs-lookup"><span data-stu-id="aa6c2-128">The transaction causes the system to stop responding until the session ends.</span></span> <span data-ttu-id="aa6c2-129">Seetõttu ei saa kanne maksutulemust arvutada.</span><span class="sxs-lookup"><span data-stu-id="aa6c2-129">Therefore, the transaction can't calculate the tax result.</span></span> <span data-ttu-id="aa6c2-130">Järgmine näide näitab teateboksi "Sessioon lõpetatud", mille te saate.</span><span class="sxs-lookup"><span data-stu-id="aa6c2-130">The following illustration shows the "Session ended" message box that you receive.</span></span>

    <span data-ttu-id="aa6c2-131">[![Sessioon lõpetatud teade](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="aa6c2-131">[![Session ended message](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span></span>

- <span data-ttu-id="aa6c2-132">Meetod **TaxUncommitted** võtab rohkem aega kui teised meetodid.</span><span class="sxs-lookup"><span data-stu-id="aa6c2-132">The **TaxUncommitted** methods take more time than other methods.</span></span> <span data-ttu-id="aa6c2-133">Näiteks järgmisel joonisel võtab meetod **TaxUncommitted::updateTaxUncommitted()** aega 43 347,42 sekundit, kuid teiste meetodite puhul kulub 0,09 sekundit.</span><span class="sxs-lookup"><span data-stu-id="aa6c2-133">For example, in the following illustration, the **TaxUncommitted::updateTaxUncommitted()** method takes 43,347.42 seconds, but other methods take 0.09 seconds.</span></span>

    <span data-ttu-id="aa6c2-134">[![Meetodite kestused](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="aa6c2-134">[![Method durations](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span></span>

## <a name="customizing-and-calling-tax-calculation"></a><span data-ttu-id="aa6c2-135">Maksuarvestuse kohandamine ja kutsumine</span><span class="sxs-lookup"><span data-stu-id="aa6c2-135">Customizing and calling tax calculation</span></span>

<span data-ttu-id="aa6c2-136">Kohandamisel ärge kutsuge iga rea puhul meetodile **sisesta()** või **värskenda()** maksuarvestust.</span><span class="sxs-lookup"><span data-stu-id="aa6c2-136">When you customize, don't call tax calculation at the **insert()** or **update()** method for each line.</span></span> <span data-ttu-id="aa6c2-137">Maksuarvestus tuleks kutsuda kande tasemel.</span><span class="sxs-lookup"><span data-stu-id="aa6c2-137">Tax calculation should be called at the transaction level.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="aa6c2-138">Kohanduse olemasolu tuvastamine</span><span class="sxs-lookup"><span data-stu-id="aa6c2-138">Determine whether customization exists</span></span>

<span data-ttu-id="aa6c2-139">Kui olete eelmistes jaotistes kirjeldatud toimingud teinud, kuid pole probleemi lahendada õnnestunud, tehke kindlaks, kas kohandamine on võimalik.</span><span class="sxs-lookup"><span data-stu-id="aa6c2-139">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="aa6c2-140">Kui kohandust ei ole, looge Microsofti teenusetaotlus edasise toe saamiseks.</span><span class="sxs-lookup"><span data-stu-id="aa6c2-140">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
