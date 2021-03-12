---
title: Automaatne kinnitamine planeerimise optimeerimisega
description: Selles teemas selgitatakse, kuidas kasutada automaatkinnitamist koos planeerimise optimeerimisega.
author: ChristianRytt
manager: tfehr
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: d014fcd542462e092f6e88232dff8fd5ee2253c1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963456"
---
# <a name="autofirming-with-planning-optimization"></a><span data-ttu-id="2b1d0-103">Automaatne kinnitamine planeerimise optimeerimisega</span><span class="sxs-lookup"><span data-stu-id="2b1d0-103">Autofirming with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2b1d0-104">Automaatkinnitamine võimaldab teil kinnitada (st vabastada) plaanitud tellimused koondplaneerimise protsessi osana.</span><span class="sxs-lookup"><span data-stu-id="2b1d0-104">Automatic firming lets you firm (that is, release) planned orders as part of the master planning process.</span></span> <span data-ttu-id="2b1d0-105">Kui plaanitud tellimused on kinnitatud, teisendatakse need tegelikeks ostutellimusteks, üleviimistellimuseks või tootmistellimuseks.</span><span class="sxs-lookup"><span data-stu-id="2b1d0-105">When planned orders are firmed, they are transformed into actual purchase orders, transfer orders, or production orders.</span></span> <span data-ttu-id="2b1d0-106">Optimeerimise planeerimise kasutamisel kinnitatakse tellimused koondplaneerimise käitamise ajal, kui tellimuse kuupäev (st alguskuupäev) on kinnitamise ajapiiris.</span><span class="sxs-lookup"><span data-stu-id="2b1d0-106">When Planning Optimization is used, planned orders are firmed during a master planning run when the order date (that is, the start date) is within the time fence for firming.</span></span>

> [!NOTE]
> <span data-ttu-id="2b1d0-107">Plaanitud ostutellimuse automaatkinnitamine saab aset leida ainult siis, kui üksus on hankijaga seostatud.</span><span class="sxs-lookup"><span data-stu-id="2b1d0-107">Auto-firming of a planned purchase order can occur only if the item is associated with a vendor.</span></span>

## <a name="turn-on-autofirming"></a><span data-ttu-id="2b1d0-108">Automaatkinnitamise sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="2b1d0-108">Turn on autofirming</span></span>

<span data-ttu-id="2b1d0-109">Automaatkinnitamise sisselülitamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="2b1d0-109">To turn on autofirming, follow these steps.</span></span>

1. <span data-ttu-id="2b1d0-110">Valige tööruumis **Funktsiooni haldus** vahekaardil **Uus** loendist suvand **Automaatkinnitus planeerimise optimeerimine**.</span><span class="sxs-lookup"><span data-stu-id="2b1d0-110">In the **Feature management** workspace, on the **New** tab, select **Auto-firming for Planning Optimization** in the list.</span></span> <span data-ttu-id="2b1d0-111">Kui funktsioon vahekaardile **Uus** ei ilmu, vaadake vahekaartidelt **Pole lubatud** ja **Kõik**.</span><span class="sxs-lookup"><span data-stu-id="2b1d0-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="2b1d0-112">Valige **Luba kohe**.</span><span class="sxs-lookup"><span data-stu-id="2b1d0-112">Select **Enable now**.</span></span> <span data-ttu-id="2b1d0-113">Teise võimalusena valige **Graafik** ja seejärel valige kellaaeg, millal soovite funktsiooni sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="2b1d0-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

## <a name="set-up-the-firming-time-fence"></a><span data-ttu-id="2b1d0-114">Kinnitamise ajalimiidi häälestamine</span><span class="sxs-lookup"><span data-stu-id="2b1d0-114">Set up the firming time fence</span></span>

<span data-ttu-id="2b1d0-115">Kinnitamise ajapiir arvutatakse koondplaneerimise käivitamise kuupäevast edasi.</span><span class="sxs-lookup"><span data-stu-id="2b1d0-115">The firming time fence is calculated forward from the master planning run date.</span></span> <span data-ttu-id="2b1d0-116">See määratletakse sisestatud päevase arvu järgi.</span><span class="sxs-lookup"><span data-stu-id="2b1d0-116">It's defined by the number of days that you enter.</span></span> <span data-ttu-id="2b1d0-117">Saate kinnitamise ajapiiri juhtida järgmistel viisidel.</span><span class="sxs-lookup"><span data-stu-id="2b1d0-117">You can control the firming time fence in the following ways:</span></span>

- <span data-ttu-id="2b1d0-118">Katvusgrupi vaikimisi kinnitamise ajapiiri määramiseks avage **Koondplaneerimine** \> **Seadistus** \> **Laovarud** \> **Katvusgrupid** ja valige katvusgrupp.</span><span class="sxs-lookup"><span data-stu-id="2b1d0-118">To define the default firming time fence for a coverage group, go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**, and select a coverage group.</span></span> <span data-ttu-id="2b1d0-119">Seejärel sisestage kiirkaardil **Muu** väljale **Automaatse kinnitamise ajapiir (päevades)** päevade arv.</span><span class="sxs-lookup"><span data-stu-id="2b1d0-119">Then, on the **Other** FastTab, in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="2b1d0-120">Konkreetse kauba katvusgrupi jaoks märatud kinnitamise ajapiiri ülekirjutamiseks avage **Tooteteabe haldus** \> **Väljastatud tooted**, seejärel valige Toimingupaanil **Plaan** ja valige seejärel **Kauba laovarud**.</span><span class="sxs-lookup"><span data-stu-id="2b1d0-120">To overwrite the firming time fence that is defined for the coverage group for a specific item, go to **Product information management** \> **Released products**, then from the Action Pane select **Plan** and then select **Item coverage**.</span></span> <span data-ttu-id="2b1d0-121">Seejärel valige vahekaardil **Üldine** suvand **Ajapiiride alistamine** ja sisestage väljale **Automaatse kinnitamise ajapiir (päevad)** päevade arv.</span><span class="sxs-lookup"><span data-stu-id="2b1d0-121">Then, on the **General** tab, select **Override time fence** and in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="2b1d0-122">Konkreetse koondplaani katvusgrupi ja laovarude haldamise jaoks määratletud kinnitamise ajapiiri ülekirjutamiseks avage **Koondplaneerimine** \> **Seadistus** \> **Koonplaanid** ja valige koondplaan.</span><span class="sxs-lookup"><span data-stu-id="2b1d0-122">To overwrite the firming time fence that is defined for the coverage group and item coverage for a specific master plan, go to **Master planning** \> **Setup** \> **Master plans**, and select a Master plan.</span></span> <span data-ttu-id="2b1d0-123">Seejärel määrake kiirkaardil **Ajapiir päevades** suvand **Kinnitamine** olekusse **Jah** ja sisestage päevade arv.</span><span class="sxs-lookup"><span data-stu-id="2b1d0-123">Then, on the **Time fence in days** FastTab, set **Firming** to **Yes**, and enter the number of days.</span></span>

<span data-ttu-id="2b1d0-124">Kui planeerimise optimeerimist kasutava koondplaneerimise käivitamise automaatne kinnitamine on sisse lülitatud, tehakse automaatse kinnitamise protsess vastavalt automaatse kinnitamise häälestusele.</span><span class="sxs-lookup"><span data-stu-id="2b1d0-124">If autofirming is turned on for a master planning run that uses Planning Optimization, the autofirming process is done according to the autofirming setup.</span></span> <span data-ttu-id="2b1d0-125">Kui automaatne kinnitamine ei ole sisse lülitatud või kui planeerimine käivitatakse lehelt **Netonõuded**, jäetakse automaatse kinnitamise protsess vahele.</span><span class="sxs-lookup"><span data-stu-id="2b1d0-125">If autofirming isn't turned on, or if planning is started from the **Net requirements** page, the autofirming process is skipped.</span></span>

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a><span data-ttu-id="2b1d0-126">Planeerimise optimeerimine vs. sisseehitatud tarneahela halduse planeerimismootor.</span><span class="sxs-lookup"><span data-stu-id="2b1d0-126">Planning Optimization vs. the built-in Supply Chain Management planning engine</span></span>

<span data-ttu-id="2b1d0-127">Nii planeerimise optimeerimine kui ka rakendusse Microsoft Dynamics 365 Supply Chain Management sisseehitatud planeerimismootorit saab kasutada planeeritud tellimuste automaatseks kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="2b1d0-127">Both Planning Optimization and the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management can be used to autofirm planned orders.</span></span> <span data-ttu-id="2b1d0-128">Kuid on ka olulisi erinevusi.</span><span class="sxs-lookup"><span data-stu-id="2b1d0-128">However, there are some important differences.</span></span> <span data-ttu-id="2b1d0-129">Näiteks kui planeerimise optimeerimine kasutab tellimuse kuupäeva (s.o alguskuupäev), et määrata, millised plaanitud tellimused kinnitada, siis sisseehitatud tarneahela halduse planeerimismootor kasutab vajaduse kuupäeva (s.o lõppkuupäev).</span><span class="sxs-lookup"><span data-stu-id="2b1d0-129">For example, whereas Planning Optimization uses the order date (that is, the start date) to determine which planned orders to firm, the built-in Supply Chain Management planning engine uses the requirement date (that is, the end date).</span></span> <span data-ttu-id="2b1d0-130">Siin on erinevuste kokkuvõte.</span><span class="sxs-lookup"><span data-stu-id="2b1d0-130">Here is a summary of the differences.</span></span>

<span data-ttu-id="2b1d0-131">**Planeerimise optimeerimine**</span><span class="sxs-lookup"><span data-stu-id="2b1d0-131">**Planning Optimization**</span></span>

- <span data-ttu-id="2b1d0-132">Automaatne kinnitamine põhineb tellimuse kuupäeval (alguskuupäev).</span><span class="sxs-lookup"><span data-stu-id="2b1d0-132">Autofirming is based on the order date (start date).</span></span>
- <span data-ttu-id="2b1d0-133">Kuna tellimuse kuupäev (alguskuupäev) käivitab kinnituse, ei pea te täitmisaega kinnitamise aja osana arvestama.</span><span class="sxs-lookup"><span data-stu-id="2b1d0-133">Because the order date (start date) triggers the firming, you don't have to consider the lead time as part of the firming time fence.</span></span>
- <span data-ttu-id="2b1d0-134">Kui soovite kinnitada kõik tellimused, mis peavad jooksval nädalal algama, peab kinnitamise ajapiir olema üks nädal.</span><span class="sxs-lookup"><span data-stu-id="2b1d0-134">If you want to firm all orders that must start during the current week, the firming time fence must be one week.</span></span>

<span data-ttu-id="2b1d0-135">**Sisseehitatud tarneahela halduse planeerimismootor**</span><span class="sxs-lookup"><span data-stu-id="2b1d0-135">**Built-in Supply Chain Management planning engine**</span></span>

- <span data-ttu-id="2b1d0-136">Automaatne kinnitamine põhineb nõude kuupäeval (lõppkuupäev).</span><span class="sxs-lookup"><span data-stu-id="2b1d0-136">Autofirming is based on the requirement date (end date).</span></span>
- <span data-ttu-id="2b1d0-137">Tellimuste tähtajaks kinnitamise tagamiseks peab kinnitamise ajapiir olema pikem kui täitmisaeg.</span><span class="sxs-lookup"><span data-stu-id="2b1d0-137">To help guarantee that orders are firmed in due time, the firming time fence must be longer than the lead time.</span></span>
- <span data-ttu-id="2b1d0-138">Kui soovite kinnitada kõik tellimused, mis peavad jooksval nädalal algama, peab kinnitamise ajapiir olema täitmisaeg pluss üks nädal.</span><span class="sxs-lookup"><span data-stu-id="2b1d0-138">If you want to firm all orders that must start during the current week, the firming time fence must be the lead time plus one week.</span></span>
