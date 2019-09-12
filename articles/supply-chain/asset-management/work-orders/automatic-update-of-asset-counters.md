---
title: Varaloendurite automaatne värskendus
description: Selles teemas kirjeldatakse varaloendurite automaatset värskendust varahalduses.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 97e6912cd37d6f82d8bf022141f04645a3364ee1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875616"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="9c5de-103">Varaloendurite automaatne värskendus</span><span class="sxs-lookup"><span data-stu-id="9c5de-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="9c5de-104">Eelmises jaotises kirjeldatakse varaloendurite käsitsi registreerimist.</span><span class="sxs-lookup"><span data-stu-id="9c5de-104">In the previous section, manual registration of asset counters is described.</span></span> <span data-ttu-id="9c5de-105">Varaloendurite seadistamist kirjeldatakse jaotises [Loendurid](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="9c5de-105">Setup of asset counters is described in [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="9c5de-106">Loenduri väärtuseid saab automaatselt värskendada ka tootmise registreeringutest tootmise tundide ja tootmise koguse alusel.</span><span class="sxs-lookup"><span data-stu-id="9c5de-106">Counter values can also be automatically updated from production registrations, based on production hours or production quantity.</span></span> <span data-ttu-id="9c5de-107">Seda saab teha suvandis **Värskenda varaloendurid**.</span><span class="sxs-lookup"><span data-stu-id="9c5de-107">This is done in **Update asset counters**.</span></span> <span data-ttu-id="9c5de-108">Saate värskendada ühe või mitu vara, sisestades ühe parameetri väljal **Kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="9c5de-108">You can update one or several assets by inserting one parameter, **From date**.</span></span> <span data-ttu-id="9c5de-109">See parameeter määratleb tootmise registreeringute (tundide või toodetud koguse kohta) alguskuupäeva, mis tähendab alguskuupäeva, millest alates peaks loenduri väärtusi värskendama.</span><span class="sxs-lookup"><span data-stu-id="9c5de-109">This parameter specifies the start date for production registrations (hours or quantity produced), meaning the start date from which counter values should be updated.</span></span>

<span data-ttu-id="9c5de-110">Kõik varad, mis on seotud ressursiga *ja* millel on varaloendurid, mis on seadistatud värskendusele toodetud koguse või tootmise tundide põhjal, kaastakse automaatsesse värskendusse ja luuakse uued loenduri väärtused.</span><span class="sxs-lookup"><span data-stu-id="9c5de-110">All assets that are related to a resource *and* have asset counters, which are set up to be updated based on produced quantity or production hours, will be included in an automatic update, and new counter values will be created.</span></span>

<span data-ttu-id="9c5de-111">Tootmiskogusel põhinevate loendurite puhul kaasatakse loendusse nii registreeritud õige kogus kui ka veakogus.</span><span class="sxs-lookup"><span data-stu-id="9c5de-111">Regarding counters based on production quantity, good quantity as well as error quantity registered are included in the count.</span></span> <span data-ttu-id="9c5de-112">Kui toodetud koguse registreerimise ühik erineb loenduri kasutatavast ühikust, teisendatakse kogus, et see vastaks loenduri ühikule.</span><span class="sxs-lookup"><span data-stu-id="9c5de-112">If the unit used for produced quantity registration is different from the unit used on the counter, quantity is converted to correspond with the counter unit.</span></span>

<span data-ttu-id="9c5de-113">Nagu ülal mainitud, saab loenduri väärtuseid automaatselt värskendada tootmise registreeringutest.</span><span class="sxs-lookup"><span data-stu-id="9c5de-113">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="9c5de-114">Seetõttu peab vara, mille kohta soovite automaatse värskenduse loendureid, olema seotud ressursiga (masin).</span><span class="sxs-lookup"><span data-stu-id="9c5de-114">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="9c5de-115">Järgnevad kirjeldused annavad tootmistellimuste seadistamise ja töötlemise kohta ülevaate (moodulis **Tootmise juhtimine**), mida kasutatakse vara loendurite automaatse värskendamise alusena moodulis **Varahaldus**.</span><span class="sxs-lookup"><span data-stu-id="9c5de-115">The following descriptions provide an overview of the setup and processing of production orders (in the **Production control** module), which is used as a basis for automatic update of counters on an asset in the **Asset management** module.</span></span>

<span data-ttu-id="9c5de-116">Kui toodetud kogused ja tootmise tunnid on ressursile registreeritud, saate värskendada seotud varaloendureid.</span><span class="sxs-lookup"><span data-stu-id="9c5de-116">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="9c5de-117">Klõpsake **Varahaldus** > **Perioodiline** > **Varad** > **Värskenda varaloendurid**.</span><span class="sxs-lookup"><span data-stu-id="9c5de-117">Click **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="9c5de-118">Valige väljalt **Alguskuupäev** automaatse värskenduse alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="9c5de-118">Select the start date of the automatic update in the **From date** field.</span></span>

>[!NOTE]
><span data-ttu-id="9c5de-119">Kuupäev sellel väljal on "poolelioleva töö" kuupäev suvandi **Protsessikanded** (**Tootmise juhtimine** > **Päringud ja aruanded** > **Tootmine** > **Protsessikanded** > väljal **Füüsiline kuupäev**).</span><span class="sxs-lookup"><span data-stu-id="9c5de-119">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="9c5de-120">Kui soovite automaatse värskenduse jaoks valida konkreetseid varasid, vara tüüpe või ressursse, klõpsake vahekaardil **Kaasatavad kirjed** nuppu **Filtreeri** ja tehke sobivad valikud.</span><span class="sxs-lookup"><span data-stu-id="9c5de-120">If you want to select specific assets, asset types, or resources for the automatic update, click **Filter** on the **Records to include** FastTab, and make the relevant selections.</span></span>

4. <span data-ttu-id="9c5de-121">Vajadusel saate seadistada automaatse värskenduse pakett-tööna kiirkaardil **Taustal käitamine**.</span><span class="sxs-lookup"><span data-stu-id="9c5de-121">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

![Joonis 1](media/12-work-orders.png)

5. <span data-ttu-id="9c5de-123">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="9c5de-123">Click **OK**.</span></span> <span data-ttu-id="9c5de-124">Kui automaatne vara loenduri värskendus on tehtud, näete varaga seotud loenduri registreeringuid lehel **Varaloendurid** (**Varahaldus** > **Ühine** > **Varad** > **Kõik varad** > vali vara > nupul **Loendurid**).</span><span class="sxs-lookup"><span data-stu-id="9c5de-124">When the automatic asset counter update is done, you can see the counter registrations related to the asset in **Asset counters** (**Asset management** > **Common** > **Assets** > **All assets** > select asset > **Counters** button).</span></span>

<span data-ttu-id="9c5de-125">Lehel **Varaloenduri kokkuvõte** saate ülevaate viimastest registreeringutest, mis on tehtud kõigi loenduri tüüpide kohta kõigile varadele.</span><span class="sxs-lookup"><span data-stu-id="9c5de-125">In **Asset counter totals**, you can get an overview of the latest registration made on all counter types on all assets.</span></span> <span data-ttu-id="9c5de-126">Klõpsake **Varahaldus** > **Päringud** > **Varad** > **Vara koondväärtus**.</span><span class="sxs-lookup"><span data-stu-id="9c5de-126">Click **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="9c5de-127">See vaade on väga sarnane lehe **Varaloendurid** vaatega, kui lehel **Vara koondväärtus** ei saa lisada registreeringuid ega neid redigeerida.</span><span class="sxs-lookup"><span data-stu-id="9c5de-127">The view is very similar to **Asset counters**, but you cannot add or edit registrations in **Asset aggregated value**.</span></span> <span data-ttu-id="9c5de-128">See on ainult ülevaate jaoks.</span><span class="sxs-lookup"><span data-stu-id="9c5de-128">It is for overview only.</span></span>

![Joonis 2](media/13-work-orders.png)


- <span data-ttu-id="9c5de-130">Automaatselt värskendatud loenduri tüüpide jaoks on siiski võimalik luua käsitsi loenduri väärtuse registreeringuid.</span><span class="sxs-lookup"><span data-stu-id="9c5de-130">It is still possible to create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="9c5de-131">Lisateabe saamiseks vaadake jaotist "Varaloendurite käsitsi värskendamine".</span><span class="sxs-lookup"><span data-stu-id="9c5de-131">Refer to the "Manual update of asset counters" section for more information.</span></span>
- <span data-ttu-id="9c5de-132">Saate luua teise loenduriga seotud loendureid, mis tähendab seda, et loenduri värskendamisel värskendatakse samal ajal automaatselt ka seotud loendurid.</span><span class="sxs-lookup"><span data-stu-id="9c5de-132">You can set up counters related to another counter, which means that when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="9c5de-133">Seotud loendurite seadistamiseks vaadake jaotist [Loendurid](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="9c5de-133">Refer to [Counters](../setup-for-objects/counters.md) regarding setup of related counters.</span></span>
