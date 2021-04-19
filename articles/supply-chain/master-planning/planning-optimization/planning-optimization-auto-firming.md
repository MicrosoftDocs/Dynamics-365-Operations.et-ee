---
title: Automaatne kinnitamine planeerimise optimeerimisega
description: Selles teemas selgitatakse, kuidas kasutada automaatkinnitamist koos planeerimise optimeerimisega.
author: ChristianRytt
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: 3542e343de29c9fd9d19ed99cab4b4eebacd2899
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812999"
---
# <a name="autofirming-with-planning-optimization"></a><span data-ttu-id="069ba-103">Automaatne kinnitamine planeerimise optimeerimisega</span><span class="sxs-lookup"><span data-stu-id="069ba-103">Autofirming with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="069ba-104">Automaatkinnitamine võimaldab teil kinnitada (st vabastada) plaanitud tellimused koondplaneerimise protsessi osana.</span><span class="sxs-lookup"><span data-stu-id="069ba-104">Automatic firming lets you firm (that is, release) planned orders as part of the master planning process.</span></span> <span data-ttu-id="069ba-105">Kui plaanitud tellimused on kinnitatud, teisendatakse need tegelikeks ostutellimusteks, üleviimistellimuseks või tootmistellimuseks.</span><span class="sxs-lookup"><span data-stu-id="069ba-105">When planned orders are firmed, they are transformed into actual purchase orders, transfer orders, or production orders.</span></span> <span data-ttu-id="069ba-106">Optimeerimise planeerimise kasutamisel kinnitatakse tellimused koondplaneerimise käitamise ajal, kui tellimuse kuupäev (st alguskuupäev) on kinnitamise ajapiiris.</span><span class="sxs-lookup"><span data-stu-id="069ba-106">When Planning Optimization is used, planned orders are firmed during a master planning run when the order date (that is, the start date) is within the time fence for firming.</span></span>

> [!NOTE]
> <span data-ttu-id="069ba-107">Plaanitud ostutellimuse automaatkinnitamine saab aset leida ainult siis, kui üksus on hankijaga seostatud.</span><span class="sxs-lookup"><span data-stu-id="069ba-107">Auto-firming of a planned purchase order can occur only if the item is associated with a vendor.</span></span>
> 
> <span data-ttu-id="069ba-108">Kui juhtumi muudatuste jälgimine on lubatud, kuvatakse kindlad tuletatud tellimused (allhanke ostutellimused) olekuks *Ülevaatus*.</span><span class="sxs-lookup"><span data-stu-id="069ba-108">Firmed derived orders (subcontract purchase orders) will show a status of *In-review* when case change tracking is enabled.</span></span>

## <a name="turn-on-autofirming"></a><span data-ttu-id="069ba-109">Automaatkinnitamise sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="069ba-109">Turn on autofirming</span></span>

<span data-ttu-id="069ba-110">Automaatkinnitamise sisselülitamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="069ba-110">To turn on autofirming, follow these steps.</span></span>

1. <span data-ttu-id="069ba-111">Valige tööruumis **Funktsiooni haldus** vahekaardil **Uus** loendist suvand **Automaatkinnitus planeerimise optimeerimine**.</span><span class="sxs-lookup"><span data-stu-id="069ba-111">In the **Feature management** workspace, on the **New** tab, select **Auto-firming for Planning Optimization** in the list.</span></span> <span data-ttu-id="069ba-112">Kui funktsioon vahekaardile **Uus** ei ilmu, vaadake vahekaartidelt **Pole lubatud** ja **Kõik**.</span><span class="sxs-lookup"><span data-stu-id="069ba-112">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="069ba-113">Valige **Luba kohe**.</span><span class="sxs-lookup"><span data-stu-id="069ba-113">Select **Enable now**.</span></span> <span data-ttu-id="069ba-114">Teise võimalusena valige **Graafik** ja seejärel valige kellaaeg, millal soovite funktsiooni sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="069ba-114">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

## <a name="set-up-the-firming-time-fence"></a><span data-ttu-id="069ba-115">Kinnitamise ajalimiidi häälestamine</span><span class="sxs-lookup"><span data-stu-id="069ba-115">Set up the firming time fence</span></span>

<span data-ttu-id="069ba-116">Kinnitamise ajapiir arvutatakse koondplaneerimise käivitamise kuupäevast edasi.</span><span class="sxs-lookup"><span data-stu-id="069ba-116">The firming time fence is calculated forward from the master planning run date.</span></span> <span data-ttu-id="069ba-117">See määratletakse sisestatud päevase arvu järgi.</span><span class="sxs-lookup"><span data-stu-id="069ba-117">It's defined by the number of days that you enter.</span></span> <span data-ttu-id="069ba-118">Saate kinnitamise ajapiiri juhtida järgmistel viisidel.</span><span class="sxs-lookup"><span data-stu-id="069ba-118">You can control the firming time fence in the following ways:</span></span>

- <span data-ttu-id="069ba-119">Katvusgrupi vaikimisi kinnitamise ajapiiri määramiseks avage **Koondplaneerimine** \> **Seadistus** \> **Laovarud** \> **Katvusgrupid** ja valige katvusgrupp.</span><span class="sxs-lookup"><span data-stu-id="069ba-119">To define the default firming time fence for a coverage group, go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**, and select a coverage group.</span></span> <span data-ttu-id="069ba-120">Seejärel sisestage kiirkaardil **Muu** väljale **Automaatse kinnitamise ajapiir (päevades)** päevade arv.</span><span class="sxs-lookup"><span data-stu-id="069ba-120">Then, on the **Other** FastTab, in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="069ba-121">Konkreetse kauba katvusgrupi jaoks märatud kinnitamise ajapiiri ülekirjutamiseks avage **Tooteteabe haldus** \> **Väljastatud tooted**, seejärel valige Toimingupaanil **Plaan** ja valige seejärel **Kauba laovarud**.</span><span class="sxs-lookup"><span data-stu-id="069ba-121">To overwrite the firming time fence that is defined for the coverage group for a specific item, go to **Product information management** \> **Released products**, then from the Action Pane select **Plan** and then select **Item coverage**.</span></span> <span data-ttu-id="069ba-122">Seejärel valige vahekaardil **Üldine** suvand **Ajapiiride alistamine** ja sisestage väljale **Automaatse kinnitamise ajapiir (päevad)** päevade arv.</span><span class="sxs-lookup"><span data-stu-id="069ba-122">Then, on the **General** tab, select **Override time fence** and in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="069ba-123">Konkreetse koondplaani katvusgrupi ja laovarude haldamise jaoks määratletud kinnitamise ajapiiri ülekirjutamiseks avage **Koondplaneerimine** \> **Seadistus** \> **Koonplaanid** ja valige koondplaan.</span><span class="sxs-lookup"><span data-stu-id="069ba-123">To overwrite the firming time fence that is defined for the coverage group and item coverage for a specific master plan, go to **Master planning** \> **Setup** \> **Master plans**, and select a Master plan.</span></span> <span data-ttu-id="069ba-124">Seejärel määrake kiirkaardil **Ajapiir päevades** suvand **Kinnitamine** olekusse **Jah** ja sisestage päevade arv.</span><span class="sxs-lookup"><span data-stu-id="069ba-124">Then, on the **Time fence in days** FastTab, set **Firming** to **Yes**, and enter the number of days.</span></span>

<span data-ttu-id="069ba-125">Kui planeerimise optimeerimist kasutava koondplaneerimise käivitamise automaatne kinnitamine on sisse lülitatud, tehakse automaatse kinnitamise protsess vastavalt automaatse kinnitamise häälestusele.</span><span class="sxs-lookup"><span data-stu-id="069ba-125">If autofirming is turned on for a master planning run that uses Planning Optimization, the autofirming process is done according to the autofirming setup.</span></span> <span data-ttu-id="069ba-126">Kui automaatne kinnitamine ei ole sisse lülitatud või kui planeerimine käivitatakse lehelt **Netonõuded**, jäetakse automaatse kinnitamise protsess vahele.</span><span class="sxs-lookup"><span data-stu-id="069ba-126">If autofirming isn't turned on, or if planning is started from the **Net requirements** page, the autofirming process is skipped.</span></span>

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a><span data-ttu-id="069ba-127">Planeerimise optimeerimine vs. sisseehitatud tarneahela halduse planeerimismootor.</span><span class="sxs-lookup"><span data-stu-id="069ba-127">Planning Optimization vs. the built-in Supply Chain Management planning engine</span></span>

<span data-ttu-id="069ba-128">Nii planeerimise optimeerimine kui ka rakendusse Microsoft Dynamics 365 Supply Chain Management sisseehitatud planeerimismootorit saab kasutada planeeritud tellimuste automaatseks kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="069ba-128">Both Planning Optimization and the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management can be used to autofirm planned orders.</span></span> <span data-ttu-id="069ba-129">Kuid on ka olulisi erinevusi.</span><span class="sxs-lookup"><span data-stu-id="069ba-129">However, there are some important differences.</span></span> <span data-ttu-id="069ba-130">Näiteks kui planeerimise optimeerimine kasutab tellimuse kuupäeva (s.o alguskuupäev), et määrata, millised plaanitud tellimused kinnitada, siis sisseehitatud tarneahela halduse planeerimismootor kasutab vajaduse kuupäeva (s.o lõppkuupäev).</span><span class="sxs-lookup"><span data-stu-id="069ba-130">For example, whereas Planning Optimization uses the order date (that is, the start date) to determine which planned orders to firm, the built-in Supply Chain Management planning engine uses the requirement date (that is, the end date).</span></span> <span data-ttu-id="069ba-131">Siin on erinevuste kokkuvõte.</span><span class="sxs-lookup"><span data-stu-id="069ba-131">Here is a summary of the differences.</span></span>

<span data-ttu-id="069ba-132">**Planeerimise optimeerimine**</span><span class="sxs-lookup"><span data-stu-id="069ba-132">**Planning Optimization**</span></span>

- <span data-ttu-id="069ba-133">Automaatne kinnitamine põhineb tellimuse kuupäeval (alguskuupäev).</span><span class="sxs-lookup"><span data-stu-id="069ba-133">Autofirming is based on the order date (start date).</span></span>
- <span data-ttu-id="069ba-134">Kuna tellimuse kuupäev (alguskuupäev) käivitab kinnituse, ei pea te täitmisaega kinnitamise aja osana arvestama.</span><span class="sxs-lookup"><span data-stu-id="069ba-134">Because the order date (start date) triggers the firming, you don't have to consider the lead time as part of the firming time fence.</span></span>
- <span data-ttu-id="069ba-135">Kui soovite kinnitada kõik tellimused, mis peavad jooksval nädalal algama, peab kinnitamise ajapiir olema üks nädal.</span><span class="sxs-lookup"><span data-stu-id="069ba-135">If you want to firm all orders that must start during the current week, the firming time fence must be one week.</span></span>

<span data-ttu-id="069ba-136">**Sisseehitatud tarneahela halduse planeerimismootor**</span><span class="sxs-lookup"><span data-stu-id="069ba-136">**Built-in Supply Chain Management planning engine**</span></span>

- <span data-ttu-id="069ba-137">Automaatne kinnitamine põhineb nõude kuupäeval (lõppkuupäev).</span><span class="sxs-lookup"><span data-stu-id="069ba-137">Autofirming is based on the requirement date (end date).</span></span>
- <span data-ttu-id="069ba-138">Tellimuste tähtajaks kinnitamise tagamiseks peab kinnitamise ajapiir olema pikem kui täitmisaeg.</span><span class="sxs-lookup"><span data-stu-id="069ba-138">To help guarantee that orders are firmed in due time, the firming time fence must be longer than the lead time.</span></span>
- <span data-ttu-id="069ba-139">Kui soovite kinnitada kõik tellimused, mis peavad jooksval nädalal algama, peab kinnitamise ajapiir olema täitmisaeg pluss üks nädal.</span><span class="sxs-lookup"><span data-stu-id="069ba-139">If you want to firm all orders that must start during the current week, the firming time fence must be the lead time plus one week.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
