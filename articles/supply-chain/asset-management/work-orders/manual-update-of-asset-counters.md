---
title: Varaloendurite käsitsi värskendamine
description: Selles teemas kirjeldatakse varaloendurite käsitsi värskendust varahalduses.
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
ms.openlocfilehash: 1e7c5ec288404c18b00f9dcd0e66f50744d0aa2f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875611"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="30019-103">Varaloendurite käsitsi värskendamine</span><span class="sxs-lookup"><span data-stu-id="30019-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="30019-104">Loendureid kasutatakse vara registreeringute loomiseks näiteks seoses töös olnud tundide või toodetud koguste arvuga.</span><span class="sxs-lookup"><span data-stu-id="30019-104">Counters are used to create registrations on an asset regarding, for example, number of hours in operation, or the number of quantities produced.</span></span>

<span data-ttu-id="30019-105">Kui loendurile valitud loenduri tüüp on määratud loenduri väärtusi pärima (**Varahaldus** > **Seadistus** > **Vara tüübid** > **Loendurid** > **Üldine** kiirkaart > tumblernupp **Päri vara loenduri väärtused** määratud väärtusele "Jah"), siis värskendatakse automaatselt iga sama loenduri tüüpi kasutav alamvara, kui loote uue sama tüüpi loenduri rea.</span><span class="sxs-lookup"><span data-stu-id="30019-105">If the counter type selected for a counter is set to inherit counter values (**Asset management** > **Setup** > **Asset types** > **Counters** > **General** FastTab > **Inherit asset counter values** toggle button set to "Yes"), then, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="30019-106">Jaotises **Kõik varad** loote varale tundide või koguse loenduri registreeringud vara näitude põhjal.</span><span class="sxs-lookup"><span data-stu-id="30019-106">In **All assets**, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="30019-107">Klõpsake **Varahaldus** > **Üldine** > **Varad** > **Kõik varad**.</span><span class="sxs-lookup"><span data-stu-id="30019-107">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="30019-108">Valige loendist vara ja klõpsake valikul **Loendurid**.</span><span class="sxs-lookup"><span data-stu-id="30019-108">Select the asset in the list, and click **Counters**.</span></span> <span data-ttu-id="30019-109">Vormil **Vara loendurid** näete loendit kõigist valitud vara eelmistest loenduri registreeringust.</span><span class="sxs-lookup"><span data-stu-id="30019-109">In the **Asset counters** form, you see a list of all previous counter registrations on the selected asset.</span></span>

3. <span data-ttu-id="30019-110">Uue registreeringu loomiseks klõpsake **Uus**.</span><span class="sxs-lookup"><span data-stu-id="30019-110">Click **New** to create a new registration.</span></span> <span data-ttu-id="30019-111">Vara ID sisestatakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="30019-111">The asset ID is automatically inserted.</span></span>

4. <span data-ttu-id="30019-112">Valige asjakohane loendur väljal **Loendur**.</span><span class="sxs-lookup"><span data-stu-id="30019-112">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="30019-113">Saadaval on ainult varale valitud vara tüübiga seotud loendurid.</span><span class="sxs-lookup"><span data-stu-id="30019-113">Only counters related to the asset type selected on the asset are available.</span></span> <span data-ttu-id="30019-114">Seotud ühik sisestatakse automaatselt väljale **Ühik**.</span><span class="sxs-lookup"><span data-stu-id="30019-114">The related unit is automatically inserted in the **Unit** field.</span></span>

5. <span data-ttu-id="30019-115">Valige loenduri registreeringuks kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="30019-115">Select date and time for the counter registration.</span></span>

6. <span data-ttu-id="30019-116">Sisestage väljale **Väärtus** arv alates viimasest loenduri registreeringust või sisestage loenduri koguarv väljale **Koondväärtus**.</span><span class="sxs-lookup"><span data-stu-id="30019-116">In the **Value** field, insert the number since the last counter registration, or, in the **Aggregated value** field, insert the total count number.</span></span>

- <span data-ttu-id="30019-117">Kui paigaldate füüsiliselt varale uue loenduri, peate registreerima vara muudatuse jaotises **Vara loendurid**.</span><span class="sxs-lookup"><span data-stu-id="30019-117">If you physically install a new counter on an asset, you need to register the change on the asset in **Asset counters**.</span></span> <span data-ttu-id="30019-118">Järgmisena peate looma kaks registreeringu rida identsete ajatemplitega ja uue loenduriga seotud reale valite märkeruudu **Loenduri lähtestamine**.</span><span class="sxs-lookup"><span data-stu-id="30019-118">Next, you must create two registration lines with identical timestamps, and on the line regarding the new counter, you select the **Counter reset** check box.</span></span> <span data-ttu-id="30019-119">Kahe registreeringurea loomisel peab esimene rida olema asendatavale loendurile.</span><span class="sxs-lookup"><span data-stu-id="30019-119">When you create the two registration lines, the first line must be for the counter that you are replacing.</span></span> <span data-ttu-id="30019-120">Väljal **Kogusummad** on loenduri koguarvuks kõigi selle loenduritüübi registreeritud väärtuste loenduri kogusumma.</span><span class="sxs-lookup"><span data-stu-id="30019-120">In the **Totals** field, the total count number is the sum of the counter total of all registered values on that counter type.</span></span>  
- <span data-ttu-id="30019-121">Kui varale on valitud märkeruut **Loenduri lähtestamine** kasutades hoolduskava invervallitüübiga "Üks kord alates..." või "Üks kord ületades...", on loendur uuel loenduri real ikka aktiivne, sest loote eraldi loenduri rea ja alustate uue loenduriga algusest peale.</span><span class="sxs-lookup"><span data-stu-id="30019-121">If the **Counter reset** check box is selected on an asset using a maintenance plan with a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line because you create a separate counter line and start over with a new counter.</span></span>

![Joonis 1](media/11-work-orders.png)


<span data-ttu-id="30019-123">Kui peate tegema loenduri registreeringuid mitmele varale, saab seda teha jaotises **Varahaldus** > **Päringud** > **Varad** > **Vara loendurid**.</span><span class="sxs-lookup"><span data-stu-id="30019-123">If you need to make counter registrations on several assets, that can be done in **Asset management** > **Inquiries** > **Assets** > **Asset counters**.</span></span>

>[!NOTE]
><span data-ttu-id="30019-124">Võite seadistada vahemiku kõrvalekallete määraltemiseks käsitsi loenduri registreeringutele ja selle, millist sõnumit kuvatakse, kui registreering on määratud vahemikust väljaspool.</span><span class="sxs-lookup"><span data-stu-id="30019-124">You can set up a range to define deviations in manual counter registrations, and the type of message that should be displayed if registrations are outside the defined range.</span></span> <span data-ttu-id="30019-125">Loendurite seadistamise kohta vaadake teemat [Loendurid](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="30019-125">Refer to the [Counters](../setup-for-objects/counters.md) topic regarding setup of counters.</span></span>
