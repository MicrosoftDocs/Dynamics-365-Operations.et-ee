---
title: Varaloendurite automaatne värskendus
description: Selles teemas kirjeldatakse varaloendurite automaatset värskendust varahalduses.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d51b9a7684e460d555632c3896e9dd8a4e10d92c
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626174"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="5a760-103">Varaloendurite automaatne värskendamine</span><span class="sxs-lookup"><span data-stu-id="5a760-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5a760-104">Teavet varaloendurite käsitsi registreerimise kohta leiate jaotisest [Varaloendurite käsitsi värskendamine](../work-orders/manual-update-of-asset-counters.md).</span><span class="sxs-lookup"><span data-stu-id="5a760-104">For information about manual registration of asset counters, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span> <span data-ttu-id="5a760-105">Teavet varaloendurite häälestamise kohta leiate jaotisest [Loendurid](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="5a760-105">For information on how to set up asset counters, see [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="5a760-106">Loenduri väärtusi saab automaatselt värskendada ka tootmise registreeringutest tootmistundide ja tootmiskoguse (s.t toodetava koguse) alusel.</span><span class="sxs-lookup"><span data-stu-id="5a760-106">Counter values can also be automatically updated from production registrations, based on the production hours or production quantity (that is, the quantity that is produced).</span></span> <span data-ttu-id="5a760-107">See värskendus tehakse lehel **Varaloendurite värskendamine**.</span><span class="sxs-lookup"><span data-stu-id="5a760-107">This update is done on the **Update asset counters** page.</span></span> <span data-ttu-id="5a760-108">Saate värskendada ühe või mitu vara, määrates ühe parameetri väljal **Kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="5a760-108">You can update one or several assets by setting one parameter, **From date**.</span></span> <span data-ttu-id="5a760-109">See parameeter määrab toodangu registreerimiste alguskuupäeva (tootmistunnid või tootmiskogused).</span><span class="sxs-lookup"><span data-stu-id="5a760-109">This parameter specifies the start date for production registrations (production hours or production quantities).</span></span> <span data-ttu-id="5a760-110">Teisisõnu määrab see kuupäeva, millest alates tuleb loenduri väärtusi värskendada.</span><span class="sxs-lookup"><span data-stu-id="5a760-110">In other words, it specifies the date that counter values should be updated from.</span></span>

<span data-ttu-id="5a760-111">Kõik varad, mis on seotud ressursiga *ja* millel on varaloendurid, mis on seadistatud värskendamisele tootmistundide või toodangu koguse põhjal, kaasatakse automaatsesse värskendusse.</span><span class="sxs-lookup"><span data-stu-id="5a760-111">All assets that are related to a resource, *and* that have asset counters that are set up to be updated based on the production hours or production quantity, will be included in an automatic update.</span></span> <span data-ttu-id="5a760-112">Luuakse uued loenduri väärtused.</span><span class="sxs-lookup"><span data-stu-id="5a760-112">New counter values will be created.</span></span>

<span data-ttu-id="5a760-113">Nende loendurite puhul, mis põhinevad toodangu kogusel, hõlmab arv nii õiget kogust kui ka registreeritud veakogust.</span><span class="sxs-lookup"><span data-stu-id="5a760-113">For counters that are based on the production quantity, the count includes both the good quantity and the error quantity that are registered.</span></span> <span data-ttu-id="5a760-114">Kui toodangu koguse registreerimise ühik erineb loenduri kasutatavast ühikust, teisendatakse kogus nii, et see vastaks loenduri ühikule.</span><span class="sxs-lookup"><span data-stu-id="5a760-114">If the unit that is used for production quantity registration differs from the unit that is used for the counter, the quantity is converted so that it corresponds to the counter unit.</span></span>

<span data-ttu-id="5a760-115">Nagu ülal mainitud, saab loenduri väärtuseid automaatselt värskendada tootmise registreeringutest.</span><span class="sxs-lookup"><span data-stu-id="5a760-115">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="5a760-116">Seetõttu peab vara, mille kohta soovite automaatse värskenduse loendureid, olema seotud ressursiga (masin).</span><span class="sxs-lookup"><span data-stu-id="5a760-116">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="5a760-117">Kui toodetud kogused ja tootmise tunnid on ressursile registreeritud, saate värskendada seotud varaloendureid.</span><span class="sxs-lookup"><span data-stu-id="5a760-117">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="5a760-118">Valige **Varahaldus** > **Perioodiline** > **Varad** > **Värskenda varaloendurid**.</span><span class="sxs-lookup"><span data-stu-id="5a760-118">Select **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="5a760-119">Valige väljalt **Alguskuupäev** automaatse värskenduse alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="5a760-119">In the **From date** field, select the start date of the automatic update.</span></span>

>[!NOTE]
><span data-ttu-id="5a760-120">Kuupäev sellel väljal on "poolelioleva töö" kuupäev suvandi **Protsessikanded** (**Tootmise juhtimine** > **Päringud ja aruanded** > **Tootmine** > **Protsessikanded** > väljal **Füüsiline kuupäev**).</span><span class="sxs-lookup"><span data-stu-id="5a760-120">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="5a760-121">Kiirkaardil **Kaasatavad kirjed** saate valida kindlad varad, varatüübid või ressursid automaatseks värskendamiseks.</span><span class="sxs-lookup"><span data-stu-id="5a760-121">On the **Records to include** FastTab, you can select specific assets, asset types, or resources for the automatic update.</span></span> <span data-ttu-id="5a760-122">Valige **Filter** ja tehke vajalikud valikud.</span><span class="sxs-lookup"><span data-stu-id="5a760-122">Select **Filter**, and make the relevant selections.</span></span>

4. <span data-ttu-id="5a760-123">Vahekaardil **Taustal käitamine** saate vastavalt vajadusele seadistada automaatse värskenduse pakett-tööna.</span><span class="sxs-lookup"><span data-stu-id="5a760-123">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

<span data-ttu-id="5a760-124">Alloleval joonisel on esitatud dialoogi **Varaloendurite värskendamine** näide.</span><span class="sxs-lookup"><span data-stu-id="5a760-124">The illustration below shows an example of the **Update asset counters** dialog.</span></span>

![Joonis 1](media/12-work-orders.png)

5. <span data-ttu-id="5a760-126">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="5a760-126">Select **OK**.</span></span> 

<span data-ttu-id="5a760-127">Pärast seda, kui varaloenduri automaatne värskendamine on tehtud, saate vaadata varaga seotud loenduri registreerimisi lehel **Varaloendurid**.</span><span class="sxs-lookup"><span data-stu-id="5a760-127">After the automatic asset counter update is done, you can view the counter registrations that are related to the asset on the **Asset counters** page.</span></span> <span data-ttu-id="5a760-128">Valige **Varahaldus** > **Üldine** > **Varad** > **Kõik varad**, valige vara ja seejärel valige toimingupaani vahekaardil **Vara** grupist **Ennetav** üksus **Loendurid**.</span><span class="sxs-lookup"><span data-stu-id="5a760-128">Select **Asset management** > **Common** > **Assets** > **All assets**, select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span>

<span data-ttu-id="5a760-129">Lehel **Vara koondväärtus** saate ülevaate viimasest registreeringust, mis on tehtud kõigi varade kõigi loenduritüüpide kohta.</span><span class="sxs-lookup"><span data-stu-id="5a760-129">On the **Asset aggregated value** page, you can get an overview of the latest registration that have been made on all counter types on all assets.</span></span> <span data-ttu-id="5a760-130">Valige **Varahaldus** > **Päringud** > **Varad** > **Vara koondväärtus**.</span><span class="sxs-lookup"><span data-stu-id="5a760-130">Select **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="5a760-131">See lehekülg meenutab lehte **Varaloendurid**, kuid registreerimisi ei saa lisada ega redigeerida.</span><span class="sxs-lookup"><span data-stu-id="5a760-131">This page resembles the **Asset counters** page, but you can't add or edit registrations.</span></span> <span data-ttu-id="5a760-132">See on ainult ülevaate jaoks.</span><span class="sxs-lookup"><span data-stu-id="5a760-132">It's for overview only.</span></span>

<span data-ttu-id="5a760-133">Alloleval joonisel on esitatud lehe **Vara koondväärtus** näide.</span><span class="sxs-lookup"><span data-stu-id="5a760-133">The illustration below shows an example of the **Asset aggregated value** page.</span></span>

![Joonis 2](media/13-work-orders.png)

<span data-ttu-id="5a760-135">Pidage meeles järgmiseid punkte.</span><span class="sxs-lookup"><span data-stu-id="5a760-135">Note the following points:</span></span>

- <span data-ttu-id="5a760-136">Automaatselt värskendatud loenduritüüpide jaoks saab siiski luua käsitsi loenduri väärtuse registreeringuid.</span><span class="sxs-lookup"><span data-stu-id="5a760-136">You can still create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="5a760-137">Lisateabe saamiseks vaadake jaotist [Varaloendurite käsitsi värskendamine](../work-orders/manual-update-of-asset-counters.md).</span><span class="sxs-lookup"><span data-stu-id="5a760-137">For more information, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span>

- <span data-ttu-id="5a760-138">Saate häälestada loendurid, mis on seotud mõne muu loenduriga.</span><span class="sxs-lookup"><span data-stu-id="5a760-138">You can set up counters that are related to another counter.</span></span> <span data-ttu-id="5a760-139">Sel juhul värskendatakse ühe loenduri värskendamisel samaaegselt ka seotud loendureid.</span><span class="sxs-lookup"><span data-stu-id="5a760-139">In this case, when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="5a760-140">Teavet seotud loendurite häälestamise kohta leiate jaotisest [Loendurid](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="5a760-140">For more information about how to set up related counters, see [Counters](../setup-for-objects/counters.md).</span></span>

