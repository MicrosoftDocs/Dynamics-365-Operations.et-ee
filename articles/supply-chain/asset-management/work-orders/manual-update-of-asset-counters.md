---
title: Varaloendurite käsitsi värskendamine
description: Selles teemas kirjeldatakse varaloendurite käsitsi värskendust varahalduses.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23a94415a662059ddbd41cc6a0ba9dab24aae44e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426076"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="a32e3-103">Varaloendurite käsitsi värskendamine</span><span class="sxs-lookup"><span data-stu-id="a32e3-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="a32e3-104">Loendureid kasutatakse vara registreeringute loomiseks, nt registreeringud tundide arvu kohta, mille jooksul vara oli töös või toodetud koguse kohta.</span><span class="sxs-lookup"><span data-stu-id="a32e3-104">Counters are used to create registrations on an asset, such as registrations about the number of hours that the asset has been in operation or the quantity that has been produced.</span></span>

<span data-ttu-id="a32e3-105">Loenduri jaoks valitud loenduri tüüp võib olla seatud loenduri väärtusi pärima.</span><span class="sxs-lookup"><span data-stu-id="a32e3-105">The counter type that is selected for a counter might be set to inherit counter values.</span></span> <span data-ttu-id="a32e3-106">Teiste sõnadega on valiku **Päri vara loenduri väärtused** seatud väärtusele **Jah** lehe **Loendurid** (**Varahaldus** > **Seadistus** > **Varatüübid** > **Loendurid**) kiirkaardil **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="a32e3-106">In other words, the **Inherit asset counter values** option is set to **Yes** on the **General** FastTab of the **Counters** page (**Asset management** > **Setup** > **Asset types** > **Counters**).</span></span> <span data-ttu-id="a32e3-107">Sel juhul, kui loote uue seda tüüpi loenduri, uuendatakse iga alamvara, mis kasutab sama loenduri tüüpi, automaatselt.</span><span class="sxs-lookup"><span data-stu-id="a32e3-107">In this case, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="a32e3-108">Lehel **Kõik varad** saate luua varale tundide või koguse loenduri registreeringud vara näitude põhjal.</span><span class="sxs-lookup"><span data-stu-id="a32e3-108">On the **All assets** page, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="a32e3-109">Valige **Varahaldus** > **Ühised** > **Varad** > **Kõik varad**.</span><span class="sxs-lookup"><span data-stu-id="a32e3-109">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="a32e3-110">Valige vara ja seejärel tehke vahekaardi **Vara** jaotise **Ennetav** tegumiribal valik **Loendurid**.</span><span class="sxs-lookup"><span data-stu-id="a32e3-110">Select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span> <span data-ttu-id="a32e3-111">Lehel **Vara loendurid** kuvatakse loend kõigist valitud vara eelmistest loenduri registreeringust.</span><span class="sxs-lookup"><span data-stu-id="a32e3-111">The **Asset counters** page shows a list of all previous counter registrations that have been made on the selected asset.</span></span>

3. <span data-ttu-id="a32e3-112">Valige uue registreeringu loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a32e3-112">Select **New** to create a registration.</span></span> <span data-ttu-id="a32e3-113">Vara ID sisestatakse automaatselt väljale **Vara**.</span><span class="sxs-lookup"><span data-stu-id="a32e3-113">The asset ID is automatically entered in the **Asset** field.</span></span>

4. <span data-ttu-id="a32e3-114">Valige asjakohane loendur väljal **Loendur**.</span><span class="sxs-lookup"><span data-stu-id="a32e3-114">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="a32e3-115">Valimiseks on saadaval ainult varale valitud vara tüübiga seotud loendurid.</span><span class="sxs-lookup"><span data-stu-id="a32e3-115">Only counters that are related to the asset type selected on the asset are available for selection.</span></span> <span data-ttu-id="a32e3-116">Seotud ühik sisestatakse automaatselt väljale **Ühik**.</span><span class="sxs-lookup"><span data-stu-id="a32e3-116">The related unit is automatically entered in the **Unit** field.</span></span>

5. <span data-ttu-id="a32e3-117">Valige väljal **Registreeritud** loenduri registreeringu kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="a32e3-117">In the **Registered** field, select the date and time for the counter registration.</span></span>

6. <span data-ttu-id="a32e3-118">Sisestage väljale **Väärtus** arv eelmisest loenduri registreeringust.</span><span class="sxs-lookup"><span data-stu-id="a32e3-118">In the **Value** field, enter the number since the last counter registration.</span></span> <span data-ttu-id="a32e3-119">Teise võimalusena sisestage väljale **Koondväärtus** loenduri koguarv.</span><span class="sxs-lookup"><span data-stu-id="a32e3-119">Alternatively, in the **Aggregated value** field, enter the total count number.</span></span>

<span data-ttu-id="a32e3-120">Pidage meeles järgmiseid punkte.</span><span class="sxs-lookup"><span data-stu-id="a32e3-120">Note the following points:</span></span>

- <span data-ttu-id="a32e3-121">Kui paigaldate füüsiliselt varale uue loenduri, peate registreerima vara muudatuse lehel **Vara loendurid**.</span><span class="sxs-lookup"><span data-stu-id="a32e3-121">If you physically install a new counter on an asset, you must register the change on the asset on the **Asset counters** page.</span></span> <span data-ttu-id="a32e3-122">Järgmisena peate looma kaks identsete ajatemplitega registreeringurida.</span><span class="sxs-lookup"><span data-stu-id="a32e3-122">Next, you must create two registration lines that have identical timestamps.</span></span> <span data-ttu-id="a32e3-123">Esimene rida peab olema loenduri jaoks, mille asendate.</span><span class="sxs-lookup"><span data-stu-id="a32e3-123">The first line must be for the counter that you're replacing.</span></span> <span data-ttu-id="a32e3-124">Uue loenduriga seotud real märkige ruut **Loenduri lähtestamine**.</span><span class="sxs-lookup"><span data-stu-id="a32e3-124">On the line that is related to the new counter, select the **Counter reset** check box.</span></span> <span data-ttu-id="a32e3-125">Väljal **Kogusummad** on loenduri koguarvuks kõigi selle loenduritüübi registreeritud väärtuste loenduri kogusumma.</span><span class="sxs-lookup"><span data-stu-id="a32e3-125">In the **Totals** field, the total count number is the sum of the counter totals of all registered values on that counter type.</span></span>

- <span data-ttu-id="a32e3-126">Kui varale on valitud märkeruut **Loenduri lähtestamine** kasutades hoolduskava intervallitüübiga "Üks kord alates..." või "Üks kord ületades...", on loendur uuel loenduri real ikka aktiivne, sest loote eraldi loenduri rea ja alustate uue loenduriga algusest peale.</span><span class="sxs-lookup"><span data-stu-id="a32e3-126">If the **Counter reset** check box is selected on an asset using a maintenance plan that has a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line, because you create a separate counter line and start over with a new counter.</span></span>

<span data-ttu-id="a32e3-127">Alloleval joonisel on esitatud lehe **Varaloendurid** näide.</span><span class="sxs-lookup"><span data-stu-id="a32e3-127">The illustration below shows an example of the **Asset counters** page.</span></span>

![Joonis 1](media/11-work-orders.png)

<span data-ttu-id="a32e3-129">Lehel **Varaloendurid** (**Varahaldus** > **Päringud** > **Varad** > **Varaloendurid**), saate vajadusel korraga teha mitme vara loenduri registreeringuid.</span><span class="sxs-lookup"><span data-stu-id="a32e3-129">On the **Asset counters** page (**Asset management** > **Inquiries** > **Assets** > **Asset counters**), you can make counter registrations on several assets at the same time, as you require.</span></span>

>[!NOTE]
><span data-ttu-id="a32e3-130">Saate seadistada vahemiku, et määratleda hälbed käsitsi loenduri registreeringutes.</span><span class="sxs-lookup"><span data-stu-id="a32e3-130">You can set up a range to define deviations in manual counter registrations.</span></span> <span data-ttu-id="a32e3-131">Samuti saate määrata teate tüübi, mis kuvatakse, kui registreeringud jäävad väljapoole määratletud vahemikku.</span><span class="sxs-lookup"><span data-stu-id="a32e3-131">You can also specify the type of message that is shown if registrations are outside the defined range.</span></span> <span data-ttu-id="a32e3-132">Teavet loendurite häälestamise kohta leiate jaotisest [Loendurid](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="a32e3-132">For more information about how to set up counters, see [Counters](../setup-for-objects/counters.md).</span></span>

