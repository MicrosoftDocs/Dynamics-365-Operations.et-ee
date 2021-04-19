---
title: Hooldustöötajad ja töötajate rühmad
description: Selles teemas selgitatakse hooldustöötajaid ja töötajate rühmi varahalduses.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetWorkerGroupCopyFromResourceGroup, EntAssetWorkerGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 553dce8df5e91cce58b64e340d8ff72586d8d46d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838558"
---
# <a name="maintenance-workers-and-worker-groups"></a><span data-ttu-id="18527-103">Hooldustöötajad ja töötajate rühmad</span><span class="sxs-lookup"><span data-stu-id="18527-103">Maintenance workers and worker groups</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="18527-104">Selles teemas selgitatakse hooldustöötajaid ja töötajate rühmi varahalduses.</span><span class="sxs-lookup"><span data-stu-id="18527-104">This topic explains maintenance workers and worker groups in Asset Management.</span></span> <span data-ttu-id="18527-105">Varahalduses saate ühendada hooldustöötajaid funktsionaalsete asukohtadega.</span><span class="sxs-lookup"><span data-stu-id="18527-105">In Asset Management, you can connect maintenance workers to functional locations.</span></span> <span data-ttu-id="18527-106">(Lisateavet funktsionaalsete asukohtade kohta leiate jaotisest [Funktsionaalsete asukohtade loomine](../functional-locations/create-functional-locations.md).)See funktsioon võib olla kasulik, kui näiteks plaanite hooldustöid masinas, mis asub funktsionaalses asukohas 01 ja soovite selle töö jaoks eraldada samast asukohast hooldustöötajad.</span><span class="sxs-lookup"><span data-stu-id="18527-106">(For more information about functional locations, see [Create functional locations](../functional-locations/create-functional-locations.md).) This functionality might be useful if, for example, you're scheduling a maintenance job on a machine that is located in functional location 01, and you want to allocate maintenance workers from the same location to perform the job.</span></span>

<span data-ttu-id="18527-107">Saate luua ka hooldustöötajate rühmi ja seostada nendega hooldustöötajaid.</span><span class="sxs-lookup"><span data-stu-id="18527-107">You can also create maintenance worker groups and associate maintenance workers with them.</span></span> <span data-ttu-id="18527-108">See funktsioon on kasulik siis, kui teete lihtsat töökäsu planeerimist ja soovite planeerida töökäsule hooldustöötajate rühma.</span><span class="sxs-lookup"><span data-stu-id="18527-108">This functionality is useful when you do simple work order scheduling, and you want to schedule a group of maintenance workers on a work order.</span></span> <span data-ttu-id="18527-109">Võite kasutada hooldustöötajaid ja hooldustöötajate rühmi eelistatud hooldustöötajate ja vastutavate hooldustöötajate seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="18527-109">You can use maintenance workers and maintenance worker groups to set up preferred maintenance workers and responsible maintenance workers.</span></span> 


## <a name="create-workers"></a><span data-ttu-id="18527-110">Töötajate loomine</span><span class="sxs-lookup"><span data-stu-id="18527-110">Create workers</span></span>

1. <span data-ttu-id="18527-111">Valige **Varahaldus**\>**Häälestus**\>**Töötajad**\>**Töötajad**.</span><span class="sxs-lookup"><span data-stu-id="18527-111">Select **Asset management** \> **Setup** \> **Workers** \> **Workers**.</span></span>
2. <span data-ttu-id="18527-112">Töötaja loendisse lisamiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="18527-112">Select **New** to add a worker to the list.</span></span>
3. <span data-ttu-id="18527-113">Valige töötaja väljal **Töötaja**.</span><span class="sxs-lookup"><span data-stu-id="18527-113">In the **Worker** field, select the worker.</span></span>
4. <span data-ttu-id="18527-114">Seadistage suvand **Aktiivne** olekusse **Jah**, et planeerida töötaja töökäskudele.</span><span class="sxs-lookup"><span data-stu-id="18527-114">Set the **Active** option to **Yes** to schedule the worker on work orders.</span></span>

    <span data-ttu-id="18527-115">Kiirkaardil **Üldine** täidetakse väljad **Ressurss** ja **Kirjeldus** automaatselt, kui töötajale on ressurss valitud.</span><span class="sxs-lookup"><span data-stu-id="18527-115">On the **General** FastTab, the **Resource** and **Description** fields are automatically filled in if a resource has been selected for the worker.</span></span> <span data-ttu-id="18527-116">Väli **Kalender** täidetakse samuti automaatselt, kui olete töötaja ressursina seadistanud ja sellele ressursile lehel **Ressursid** kalendri eraldanud (**Organisatsiooni haldamine**\>**Ressursid**\>**Ressursid**).</span><span class="sxs-lookup"><span data-stu-id="18527-116">The **Calendar** field is also automatically filled in, provided that you've set up the worker as a resource and allocated a calendar to that resource on the **Resources** page (**Organization administration** \> **Resources** \> **Resources**).</span></span>

5. <span data-ttu-id="18527-117">Valige kiirkaardil **Rühmad** suvand **Lisa** ja seejärel valige töötajale hooldustöötajate rühm.</span><span class="sxs-lookup"><span data-stu-id="18527-117">On the **Groups** FastTab, select **Add**, and then select a maintenance worker group for the worker.</span></span> <span data-ttu-id="18527-118">Töötaja võib olla seotud rohkem kui ühe rühmaga.</span><span class="sxs-lookup"><span data-stu-id="18527-118">A worker can be affiliated with more than one group.</span></span>
6. <span data-ttu-id="18527-119">Tavapärase häälestuse korral hakkab töötaja seotus rühmaga kehtima kuupäevast, millal te rühma lisate, ja see ei aegu kunagi.</span><span class="sxs-lookup"><span data-stu-id="18527-119">In the standard setup, a worker's affiliation with a group is effective from the date when you add the group, and it never expires.</span></span> <span data-ttu-id="18527-120">See kuupäev on näidatud väljal **Tõhus**.</span><span class="sxs-lookup"><span data-stu-id="18527-120">This date is shown in the **Effective** field.</span></span> <span data-ttu-id="18527-121">Välja **Tõhus** nägemiseks valige **Kuva**\>**kõik**.</span><span class="sxs-lookup"><span data-stu-id="18527-121">To see the **Effective** field, select **View** \> **All**.</span></span> <span data-ttu-id="18527-122">Kui töötaja seotus rühmaga peaks piirduma konkreetse ajaperioodiga, kasutage perioodi määramiseks välju **Tõhus** ja **Aegumine**.</span><span class="sxs-lookup"><span data-stu-id="18527-122">If the worker's affiliation with a group should be limited to a specific period, use the **Effective** and **Expiration** fields to define the period.</span></span>
7. <span data-ttu-id="18527-123">Valige kiirkaardil **Funktsionaalsed asukohad** suvand **Lisa** ja seejärel vali hooldustöötajale funktsionaalne asukoht.</span><span class="sxs-lookup"><span data-stu-id="18527-123">On the **Functional locations** FastTab, select **Add**, and then select a functional location for the maintenance worker.</span></span> <span data-ttu-id="18527-124">Määratlege ka see, milline asukoht on töötaja peamine funktsionaalne asukoht.</span><span class="sxs-lookup"><span data-stu-id="18527-124">Also specify which location is the primary functional location for the worker.</span></span>

    > [!NOTE]
    > <span data-ttu-id="18527-125">Kui lisate töötajale funktsionaalseid asukohti, kuvatakse kõiki nende funktsionaalsete asukohtadega seotud aktiivseid varasid mitmetes menüü-üksustes, nagu näiteks **Minu aktiivsed varad** ja **Minu aktiivsed funktsionaalsed asukohad**.</span><span class="sxs-lookup"><span data-stu-id="18527-125">When you add functional locations to a worker, all active assets that are related to those functional locations appear on various menu items, such as **My active assets** and **My active functional locations**.</span></span> <span data-ttu-id="18527-126">Neid kuvatakse ka varade otsingutes, mida kuvatakse siis, kui loote uue vara, hooldustaotluse või töökäsu.</span><span class="sxs-lookup"><span data-stu-id="18527-126">They also appear in the asset lookups that are shown when you create a new asset, maintenance request, or work order.</span></span>

    <span data-ttu-id="18527-127">Väljad kiirkaardil **Üksikasjad** näitavad mitmeid hooldustöötajate rühmi ja funktsionaalseid asukohti, millega valitud hooldustöötajad seotud on.</span><span class="sxs-lookup"><span data-stu-id="18527-127">The fields on the **Details** FastTab show the number of maintenance worker groups and functional locations that the selected maintenance worker is related to.</span></span>

## <a name="create-worker-groups"></a><span data-ttu-id="18527-128">Töötajate rühmade loomine</span><span class="sxs-lookup"><span data-stu-id="18527-128">Create worker groups</span></span>

1. <span data-ttu-id="18527-129">Valige **Varahaldus**\>**Häälestus**\>**Töötajad**\>**Hooldustöötajate rühmad**.</span><span class="sxs-lookup"><span data-stu-id="18527-129">Select **Asset management** \> **Setup** \> **Workers** \> **Maintenance worker groups**.</span></span>
2. <span data-ttu-id="18527-130">Töötajate rühma loendisse lisamiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="18527-130">Select **New** to add a worker group to the list.</span></span>
3. <span data-ttu-id="18527-131">Sisestage väljale **Hooldustöötajate rühm** rühma ID.</span><span class="sxs-lookup"><span data-stu-id="18527-131">In the **Maintenance worker group** field, enter a group ID.</span></span>
4. <span data-ttu-id="18527-132">Väljale **Nimi** sisestage nimi.</span><span class="sxs-lookup"><span data-stu-id="18527-132">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="18527-133">Valige kiirkaardil **Töötajad** suvand **Lisa** ja seejärel valige töötajate rühmale hooldustöötaja.</span><span class="sxs-lookup"><span data-stu-id="18527-133">On the **Workers** FastTab, select **Add**, and then select a maintenance worker for the worker group.</span></span> <span data-ttu-id="18527-134">Lisainfot väljade **Tõhus** ja **Aegumine** kohta leiate eelneva protseduuri 6. etapist.</span><span class="sxs-lookup"><span data-stu-id="18527-134">For information about the **Effective** and **Expiration** fields, see step 6 in the previous procedure.</span></span>
6. <span data-ttu-id="18527-135">Kui valitud hooldustöötajate rühmaga peaks olema seotud ressursirühm, valige **Kopeeri ressursirühmast**.</span><span class="sxs-lookup"><span data-stu-id="18527-135">If a resource group should be related to the selected maintenance worker group, select **Copy from resource group**.</span></span> <span data-ttu-id="18527-136">Väljal **Rühjm** valige ressursirühm kalendri sätete kopeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="18527-136">In the **Group** field, select the resource group to copy calendar settings from.</span></span> <span data-ttu-id="18527-137">Seejärel valige väljal **Töötajate rühm** töötajate rühm ressursirühma kalendri sätete kopeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="18527-137">Then, in the **Worker group** field, select the worker group to copy the resource group's calendar settings to.</span></span> <span data-ttu-id="18527-138">See etapp on asjakohane ainult siis, kui soovite, et hooldustöötajad kasutaksid töökäsu plaanimisel ressursiga (töökeskus) seotud kalendrit.</span><span class="sxs-lookup"><span data-stu-id="18527-138">This step is relevant only if you want maintenance workers to use the calendar that is related to a resource (work center) during work order scheduling.</span></span>

    <span data-ttu-id="18527-139">Kiirkaart **Üksikasjad** kuvab nende hooldustöötajate arvu, kes on määratud valitud hooldustöötajate rühma.</span><span class="sxs-lookup"><span data-stu-id="18527-139">The field on the **Details** FastTab shows the number of maintenance workers that have been set up on the selected maintenance worker group.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]