---
title: Lao partii tõrkeotsing ja seeria reserveerimise hierarhiad
description: Selles teemas kirjeldatakse, kuidas lahendada reserveerimise hierarhiatega töötamisel tekkivaid probleeme, mis kasutavad partii või seeria dimensioone.
author: perlynne
ms.date: 3/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 3/12/2021
ms.openlocfilehash: 1cd4883cdd95a97f821e0103da910e2c0346a08d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022542"
---
# <a name="troubleshoot-warehouse-batch-and-serial-reservation-hierarchies"></a><span data-ttu-id="b237d-103">Lao partii tõrkeotsing ja seeria reserveerimise hierarhiad</span><span class="sxs-lookup"><span data-stu-id="b237d-103">Troubleshoot warehouse batch and serial reservation hierarchies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b237d-104">Selles teemas kirjeldatakse, kuidas lahendada reserveerimise hierarhiatega töötamisel tekkivaid probleeme, mis kasutavad partii või seeria dimensioone.</span><span class="sxs-lookup"><span data-stu-id="b237d-104">This topic describes how to fix common issues that you might encounter while you work with reservation hierarchies that use batch or serial dimensions.</span></span>

<span data-ttu-id="b237d-105">Lisateavet vt [Paindlik dimensiooni broneerimise poliitika laotasemel](flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="b237d-105">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>

<span data-ttu-id="b237d-106">Kauba broneerimishierarhia dikteerib nõuded salvestusmõõtmetele, mis peavad olema täidetud nõudetellimuse asukoha määramiseks.</span><span class="sxs-lookup"><span data-stu-id="b237d-106">The reservation hierarchy of an item dictates the requirement of storage dimensions that must be fulfilled to assign a location to a demand order.</span></span> <span data-ttu-id="b237d-107">Neid dimensioone saab kirjeldada kui *asukohast ülalpool dimensioone* kõikide dimensioonide puhul, mis peavad olema täidetud enne asukoha määramist, ja *dimensioonid allpool asukohta* dimensioonide puhul, mida saab eraldada pärast asukoha määramist nõudlustellimusele.</span><span class="sxs-lookup"><span data-stu-id="b237d-107">These dimensions can be described as *dimensions above location*, for all the dimensions that must be fulfilled before a location is assigned, and *dimensions below location*, for dimensions that can be allocated after a location has been assigned to the demand order.</span></span> <span data-ttu-id="b237d-108">Neid reserveerimishierarhiaid nimetatakse ka *partii-ülevaks* ja *partii-aluseks* reserveerimishierarhiaks või reserveerimishierarhiate *ülaseeriaks* ja *alaseeriaks*.</span><span class="sxs-lookup"><span data-stu-id="b237d-108">These reservation hierarchies are also known as *batch-above* and *batch-below* reservation hierarchies, or *serial-above* and *serial-below* reservation hierarchies.</span></span>

<span data-ttu-id="b237d-109">Laovarusid saab edukalt eraldada ainult juhul, kui asukohaülestes dimensioonides ei ole erinevusi.</span><span class="sxs-lookup"><span data-stu-id="b237d-109">Inventory can be successfully allocated only if there are no gaps in the dimensions above location.</span></span> <span data-ttu-id="b237d-110">Näiteks reserveerimishierarhias *partiiülese* puhul saab eeldada, et nõudetellimusel tuleb määrata **piirkonna**, **lao** ja **partiinumbri** dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="b237d-110">For example, in a *batch-above* reservation hierarchy, you expect **Site,** **Warehouse,** and **Batch number** dimensions to be specified on the demand order.</span></span> <span data-ttu-id="b237d-111">Kui mõni neist dimensioonidest puudub, siis eraldusprotsess nurjub.</span><span class="sxs-lookup"><span data-stu-id="b237d-111">If any of these dimensions are missing, the allocation process will fail.</span></span> <span data-ttu-id="b237d-112">Vastandina võib *partiialuses* või *seeriaaluses* reserveerimishierarhias määrata nõudlustellimusel partii- või seerianumbri, kuid eraldamisprotsess seda ei nõua.</span><span class="sxs-lookup"><span data-stu-id="b237d-112">By contrast, in a *batch-below* or *serial-below* reservation hierarchy, a batch or serial number might be specified on the demand order, but the allocation process doesn't require it.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="b237d-113">Kuvatakse järgmine tõrketeade: "Kui soovite määrata voo, peavad koorma read määrama dimensioonid asukoha kohal.</span><span class="sxs-lookup"><span data-stu-id="b237d-113">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="b237d-114">Nende dimensioonide määramiseks broneerige ja looge uuesti koorma rida."</span><span class="sxs-lookup"><span data-stu-id="b237d-114">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="b237d-115">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b237d-115">Issue description</span></span>

<span data-ttu-id="b237d-116">Kui kasutate kaupa, millel on *partii eespool* broneerimise hierarhia, ei tööta lehekülje **Koormuse planeerimise töökoht** käsk **Väljasta laole**, kui üritada väljastada koormat osalise kogusega.</span><span class="sxs-lookup"><span data-stu-id="b237d-116">When you use an item that has a *batch-above* reservation hierarchy, the **Release to warehouse** command on the **Load planning workbench** page doesn't work if you try to release a load for a partial quantity.</span></span> <span data-ttu-id="b237d-117">Te saate selle tõrketeate ja ükski töö ei ole loodud osalise koguse jaoks.</span><span class="sxs-lookup"><span data-stu-id="b237d-117">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="b237d-118">Kui aga kasutate kaupa, millel on *partii allpool* broneerimise hierarhia, saate väljastada osalise kogusega koormat lehelt **Koormuse planeerimise töökoht**.</span><span class="sxs-lookup"><span data-stu-id="b237d-118">However, when you use an item that has a *batch-below* reservation hierarchy, you can release a load for a partial quantity from the **Load planning workbench** page.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="b237d-119">Väljastamise põhjus</span><span class="sxs-lookup"><span data-stu-id="b237d-119">Issue cause</span></span>

<span data-ttu-id="b237d-120">Kui broneerimise hierarhias on dimensioon **Asukoha** dimensioonist ettepool, peab see olema määratud enne lattu väljastamist.</span><span class="sxs-lookup"><span data-stu-id="b237d-120">When a dimension is above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="b237d-121">Osalisi koguseid ei saa väljastada, kui ühe või mitme dimensiooni **Asukoht** on määramata.</span><span class="sxs-lookup"><span data-stu-id="b237d-121">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

## <a name="the-auto-reservation-prompt-for-a-batch-number-is-triggered-even-though-there-is-available-inventory"></a><span data-ttu-id="b237d-122">Partii numbri automaatse broneerimise viip käivitatakse, isegi kui inventar on saadaval.</span><span class="sxs-lookup"><span data-stu-id="b237d-122">The auto-reservation prompt for a batch number is triggered even though there is available inventory.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b237d-123">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b237d-123">Issue description</span></span>

<span data-ttu-id="b237d-124">Kui kasutate kaupa, mille reserveerimishierarhia on laos *partiiülene*, kus pole lubatud laoprotsessid ja automaatne reserveerimine on lubatud, kuvatakse partiinumbri automaatse reserveerimise viip isegi siis, kui komplekteerimiseks on saadaval ainult üks partii.</span><span class="sxs-lookup"><span data-stu-id="b237d-124">When you use an item that has a *batch-above* reservation hierarchy in a warehouse that hasn't enabled warehouse processes, and automatic reservation is enabled, the auto-reservation prompt for a batch number is shown even if only one batch is available for picking.</span></span>

<span data-ttu-id="b237d-125">Kuid kui kasutate sama kaupa laos, kus laoprotsessid on lubatud, ei kuvata automaatse reserveerimise viipa.</span><span class="sxs-lookup"><span data-stu-id="b237d-125">However, when you use the same item in a warehouse where warehouse processes are enabled, the auto-reservation prompt isn't shown.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="b237d-126">Väljastamise põhjus</span><span class="sxs-lookup"><span data-stu-id="b237d-126">Issue cause</span></span>

<span data-ttu-id="b237d-127">Kui reserveerimishierarhia on määratletud *partiiülese* või *seeriaülesena*, peab viidatud dimensioon (**partiinumber** või **seerianumber**) alati olema määratud nõudlustellimustel.</span><span class="sxs-lookup"><span data-stu-id="b237d-127">If a reservation hierarchy is defined as *batch-above* or *serial-above*, the referenced dimension (**Batch number** or **Serial number**) must always be specified on demand orders.</span></span> <span data-ttu-id="b237d-128">Laoprotsessid võivad teabe lõpule viia, kui saadaval on üks partii- või seerianumber.</span><span class="sxs-lookup"><span data-stu-id="b237d-128">Warehouse processes might be able to complete the information if a single batch or serial number is available.</span></span> <span data-ttu-id="b237d-129">Kuna ladu ei ole laoprotsesside jaoks lubatud, peab kasutaja alati määrama kõik **asukohast** ülalnimetatud dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="b237d-129">However, because the warehouse isn't enabled for warehouse processes, the user must always specify all the dimensions above **Location**.</span></span>

## <a name="slotting-templates-that-have-the-consider-on-hand-slot-criterion-dont-consider-current-on-hand-inventory-for-batch-enabled-items"></a><span data-ttu-id="b237d-130">Pesade mallid, mille puhul on kriteerium Arvesta vaba pesa, ei arvesta partiiga lubatud kaupade praegust vaba kaubavaru.</span><span class="sxs-lookup"><span data-stu-id="b237d-130">Slotting templates that have the Consider on-hand slot criterion don't consider current on-hand inventory for batch-enabled items.</span></span>

<span data-ttu-id="b237d-131">Lisateavet vt teemast [Laoruumi leidmine](warehouse-slotting.md).</span><span class="sxs-lookup"><span data-stu-id="b237d-131">For more information, see [Warehouse slotting](warehouse-slotting.md).</span></span>

### <a name="issue-description"></a><span data-ttu-id="b237d-132">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b237d-132">Issue description</span></span>

<span data-ttu-id="b237d-133">Pesade mallid, mille puhul on kriteerium *Arvesta vaba* pesa, ei arvesta *partiiüleste* kaupade praegust vaba kaubavaru.</span><span class="sxs-lookup"><span data-stu-id="b237d-133">Slotting templates that have the *Consider on-hand* slot criterion don't consider current on-hand inventory for *batch-above* items.</span></span> <span data-ttu-id="b237d-134">Nad arvestavad seda ainult juhul, kui partiinumber on müügitellimuse real määratud.</span><span class="sxs-lookup"><span data-stu-id="b237d-134">They consider it only if the batch number is specified on the sales order line.</span></span>

<span data-ttu-id="b237d-135">Kui kasutate aga *partiialuseid* kaupu, loetakse praegune vaba kaubavaru nii nagu on.</span><span class="sxs-lookup"><span data-stu-id="b237d-135">However, when you use *batch-below* items, the current on-hand inventory is considered as expected.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="b237d-136">Väljastamise põhjus</span><span class="sxs-lookup"><span data-stu-id="b237d-136">Issue cause</span></span>

<span data-ttu-id="b237d-137">Pesastatud malli päise saab määrata nõudetrateegiatele *Tellitud*, *Reserveeritud* või *Välja antud*.</span><span class="sxs-lookup"><span data-stu-id="b237d-137">The slotting template header can be defined for the *Ordered,* *Reserved*, or *Released* demand strategy.</span></span> <span data-ttu-id="b237d-138">*Tellitud* nõudlusstrateegia puhul kehtivad samad reserveerimishierarhia nõuded, mis rakenduvad reserveeringutele või laoprotsesside väljaandmisele.</span><span class="sxs-lookup"><span data-stu-id="b237d-138">For the *Ordered* demand strategy, the same reservation hierarchy requirements apply that apply to reservation or release to warehouse processes.</span></span> <span data-ttu-id="b237d-139">Seetõttu peab *partiialuse* või *seeriaaluste* kaupade puhul, mille reserveerimise hierarhiad on partii- või seerianumbrid määratud nõudlustellimusel (müük või ülekanne).</span><span class="sxs-lookup"><span data-stu-id="b237d-139">Therefore, for items that have *batch-above* and *serial-below* reservation hierarchies, the batch or serial number must be specified on the demand order (sales or transfer).</span></span> <span data-ttu-id="b237d-140">Teise võimalusena saab nõudlusstrateegiat *Reserveeritud* kasutada partii või seerianumbri valimiseks enne lao täitmisnõudluse loomist.</span><span class="sxs-lookup"><span data-stu-id="b237d-140">Alternatively, the *Reserved* demand strategy can be used to select the batch or serial number before the warehouse slotting demand is generated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
