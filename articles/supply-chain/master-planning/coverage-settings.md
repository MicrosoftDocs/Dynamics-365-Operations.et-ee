---
title: Laovarude sätted
description: Selles teemas on teave laovarude sätete kohta, mida Koondplaneerimises kasutatakse kaubavajaduse arvutamiseks.
author: roxanadiaconu
manager: tfehr
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard, ReqItemTableSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0aaacf28701542d329afedd8206a12f7c11b7ac7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999977"
---
# <a name="coverage-settings"></a><span data-ttu-id="78fc2-103">Laovarude sätted</span><span class="sxs-lookup"><span data-stu-id="78fc2-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="78fc2-104">Koondplaneerimine kasutab laovarude sätteid, et arvutada kaubavajadusi.</span><span class="sxs-lookup"><span data-stu-id="78fc2-104">Master scheduling uses coverage settings to calculate item requirements.</span></span>

<span data-ttu-id="78fc2-105">saate määratleda laovarude sätteid mitmel viisil:</span><span class="sxs-lookup"><span data-stu-id="78fc2-105">You can specify coverage settings in several ways:</span></span>

- <span data-ttu-id="78fc2-106">Määrake laovarude grupi laovarude sätted.</span><span class="sxs-lookup"><span data-stu-id="78fc2-106">Specify coverage settings for a coverage group.</span></span>

    <span data-ttu-id="78fc2-107">Saate luua laovarude grupi, mis sisaldab kõigi laovarude grupiga lingitud toodete sätteid.</span><span class="sxs-lookup"><span data-stu-id="78fc2-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="78fc2-108">Klõpsake laovarude grupi loomiseks valikuid **Koondplaneerimine &gt; Seadistus &gt; Laovarud &gt; Laovarude grupid**.</span><span class="sxs-lookup"><span data-stu-id="78fc2-108">To create a coverage group, go to **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups**.</span></span> <span data-ttu-id="78fc2-109">Saate linkida tootega laovarude grupi.</span><span class="sxs-lookup"><span data-stu-id="78fc2-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="78fc2-110">Kui link on tegevuskoha-, lao- või tootedimensiooni kohane, kasutage lehel **Kauba laovarud** välja **Laovarude grupp**.</span><span class="sxs-lookup"><span data-stu-id="78fc2-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="78fc2-111">Kui link on üldine olenemata tootedimensioonidest kasutage välja **Toote üksikasjad** kiirkaardi **Plaan** lehte **Laovarude grupp**.</span><span class="sxs-lookup"><span data-stu-id="78fc2-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** field on the **Plan** FastTab of the **Product details** page.</span></span> <span data-ttu-id="78fc2-112">Kui te ei lingi laovarude gruppi tootega, kasutab koondplaneerimine vaikesättena suvandit Üldine laovarude grupp, mis on määratud lehel **Koondplaneerimise parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="78fc2-112">By default, if you don't link a coverage group to a product, master planning uses the general coverage group that is specified on the **Master planning parameters** page.</span></span>

- <span data-ttu-id="78fc2-113">Määrake toote laovarude sätted.</span><span class="sxs-lookup"><span data-stu-id="78fc2-113">Specify coverage settings for a product.</span></span>

    <span data-ttu-id="78fc2-114">Saate luua laovarude sätted kindlale tootele.</span><span class="sxs-lookup"><span data-stu-id="78fc2-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="78fc2-115">Avage **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="78fc2-115">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="78fc2-116">Valige toode ja klõpsake toimingupaanil vahekaardi **Plaan** jaotises **Laovarude** grupp valikut **Kauba laovarud**, et avada leht **Kauba laovarud**.</span><span class="sxs-lookup"><span data-stu-id="78fc2-116">Select the product, and then, on the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="78fc2-117">Kui toode on laovarude grupiga juba lingitud, saate laovarude grupi sätted tühistada, kasutades välja **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="78fc2-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="78fc2-118">Laovarude sätted lehel **Kauba laovarud** alistavad lehel **Laovarude grupp** olevad sätted.</span><span class="sxs-lookup"><span data-stu-id="78fc2-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

- <span data-ttu-id="78fc2-119">Määrake toote laovarude sätted viisardi abil.</span><span class="sxs-lookup"><span data-stu-id="78fc2-119">Specify coverage settings for a product by using a wizard.</span></span>

    <span data-ttu-id="78fc2-120">Viisard juhendab teid sammhaaval läbi esmase kauba laovarude seadistamise protsessi.</span><span class="sxs-lookup"><span data-stu-id="78fc2-120">The wizard guides you step by step through the process of setting up the primary item coverage parameters.</span></span> <span data-ttu-id="78fc2-121">Klõpsake lehel **Kauba laovarud**, Toimingupaanil valige suvand **Viisard**, et avada leht **Kauba laovarude viisard**.</span><span class="sxs-lookup"><span data-stu-id="78fc2-121">On the **Item coverage** page, on the Action Pane, select **Wizard** to open the **Item Coverage Wizard**.</span></span>

- <span data-ttu-id="78fc2-122">Määrake dimensioonigrupi kaubavarude sätted.</span><span class="sxs-lookup"><span data-stu-id="78fc2-122">Specify coverage settings for a dimension group.</span></span>

    <span data-ttu-id="78fc2-123">Avage **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="78fc2-123">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="78fc2-124">Klõpsake lehe **Väljastatud toote üksikasjad** kiirkaardil **Üldine**, jaotises **Administreerimine** valige link **Laoala dimensioonigrupp**.</span><span class="sxs-lookup"><span data-stu-id="78fc2-124">On the **Released product details** page, on the **General** FastTab, in the **Administration** section, select the link in the **Storage dimension group** field.</span></span> <span data-ttu-id="78fc2-125">Valige lehel **Laoala dimensioonigrupid** märkeruut **Laovarude planeerimine dimensiooni järgi**, et luua laovarude sätted laoala dimensioonigrupi dimensiooni jaoks.</span><span class="sxs-lookup"><span data-stu-id="78fc2-125">On the **Storage dimension groups** page, select the **Coverage plan by dimension** check box to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="78fc2-126">Kõigi tootedimensioonide, nagu konfiguratsioon, värv, suurus, stiil, puhul peab olema väli **Laovarude planeerimine dimensiooni järgi** valitud.</span><span class="sxs-lookup"><span data-stu-id="78fc2-126">The **Coverage plan by dimension** field must be selected for all product dimensions, such as configuration, color, size, and style.</span></span>


## <a name="coverage-codes"></a><span data-ttu-id="78fc2-127">Planeerimise koodid</span><span class="sxs-lookup"><span data-stu-id="78fc2-127">Coverage codes</span></span>

<span data-ttu-id="78fc2-128">Koondplaneerimise konfigureerimise abil saab kasutada erinevaid täiendamise meetodeid.</span><span class="sxs-lookup"><span data-stu-id="78fc2-128">Master planning can be configured to use different replenishment methods.</span></span> <span data-ttu-id="78fc2-129">Täiendamise meetodid või saatepartii mõõtmise meetodid on need tehnikad, mille abil süsteem määratleb ostetud või toodetud kaupade partii suuruse.</span><span class="sxs-lookup"><span data-stu-id="78fc2-129">The replenishment methods or lot-sizing methods are the techniques used by the system to determine the batch size for purchased or produced items.</span></span> 

<span data-ttu-id="78fc2-130">Igale täiendamise meetodile määratakse üks allolevatest laovarude koodidest.</span><span class="sxs-lookup"><span data-stu-id="78fc2-130">Each replenishment method is assigned one of the following coverage codes:</span></span>

- <span data-ttu-id="78fc2-131">**Käsitsi** – saatepartii mõõtmise meetod, mille puhul süsteem ei soovita kaubale ostu-, edastamis- või tootmistellimusi.</span><span class="sxs-lookup"><span data-stu-id="78fc2-131">**Manual** - The lot-sizing method where the system does not suggest purchased, transfer, or production orders for the item.</span></span> <span data-ttu-id="78fc2-132">Kauba plaanija vastutab kauba täiendamiseks nõutavate tellimuste loomise eest.</span><span class="sxs-lookup"><span data-stu-id="78fc2-132">The planner for the item will be in charge of creating the required orders for the replenishment of the item.</span></span>
- <span data-ttu-id="78fc2-133">**Vastavalt nõudele** – saatepartii mõõtmise meetod, mille puhul süsteem loob kaubale vajaduse korral plaanitud ostu-, edastamis- või tootmistellimuse.</span><span class="sxs-lookup"><span data-stu-id="78fc2-133">**Per requirement** - The lot-sizing method in which the system creates a planned purchase, transfer, or production order per requirement for the item.</span></span> <span data-ttu-id="78fc2-134">Seda kasutatakse tavaliselt hootise nõudlusega kulukate kaupade puhul.</span><span class="sxs-lookup"><span data-stu-id="78fc2-134">This is generally used for expensive items with intermittent demand.</span></span>  
- <span data-ttu-id="78fc2-135">**Vastavalt perioodile** – saatepartii mõõtmise meetod, mis koondab kauba nõudluse teatud perioodi jooksul ühte tellimusse.</span><span class="sxs-lookup"><span data-stu-id="78fc2-135">**Per period** - The lot-sizing method that combines all the demand for a period into one order for the item.</span></span> <span data-ttu-id="78fc2-136">Tellimus planeeritakse perioodi esimesele päevale ja selle kogus vastab netosummale määratud perioodi jooksul.</span><span class="sxs-lookup"><span data-stu-id="78fc2-136">The order will be planned for the first day of the period and its quantity will fulfill the net requirements during the established period.</span></span> <span data-ttu-id="78fc2-137">Periood algab kauba esimese nõudega ja katab määratud pikkusega aja jooksul.</span><span class="sxs-lookup"><span data-stu-id="78fc2-137">The period starts with the first demand of the item and covers the defined length in time.</span></span> <span data-ttu-id="78fc2-138">Järgmine periood algab kauba järgmiste nõuetega.</span><span class="sxs-lookup"><span data-stu-id="78fc2-138">The next period will start with the next requirements of the item.</span></span>
- <span data-ttu-id="78fc2-139">**Min/maks** – saatepartii mõõtmise meetod, mis hõlmab varude täiendamist teatud tasemeni, kui ennustatud laoseis on väiksem kui seatud lävi.</span><span class="sxs-lookup"><span data-stu-id="78fc2-139">**Min/Max** - The lot-sizing method that contains the replenishment of inventory up to a certain level when the predicted on-hand is below a threshold.</span></span> <span data-ttu-id="78fc2-140">Varude täiendamise kogus on maksimaalse taseme ja prognoositava vaba taseme vaheline erinevus.</span><span class="sxs-lookup"><span data-stu-id="78fc2-140">The replenishment quantity will be the difference between the maximum level and the predicted on-hand level.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="78fc2-141">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="78fc2-141">Additional resources</span></span>

[<span data-ttu-id="78fc2-142">Koondplaanide ülevaade</span><span class="sxs-lookup"><span data-stu-id="78fc2-142">Master plans overview</span></span>](master-plans.md)
