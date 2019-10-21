---
title: Kuluarvestuse analüüsi Power BI sisu jaoks turbe seadistamine
description: Selles teemas selgitatakse, kuidas saate kuluarvestuses juurdepääsutaseme turbe Microsoft Power BI-s reatasemel turbeks muuta. See funktsioon aitab tagada, et kasutajad näevad ainult Power BI andmeid, millele neil on juurdepääs.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b0f7dffd85dc1c7a58a3e1f55eaa26ecbf6e8360
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185171"
---
# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a><span data-ttu-id="88ce0-104">Kuluarvestuse analüüsi Power BI sisu jaoks turbe seadistamine</span><span class="sxs-lookup"><span data-stu-id="88ce0-104">Set up security for the Cost accounting analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88ce0-105">Selles teemas selgitatakse, kuidas saate kuluarvestuses juurdepääsutaseme turbe Microsoft Power BI-s reatasemel turbeks muuta.</span><span class="sxs-lookup"><span data-stu-id="88ce0-105">This topic explains how you can propagate the access-level security in Cost accounting to row-level security in Microsoft Power BI.</span></span> <span data-ttu-id="88ce0-106">See funktsioon aitab tagada, et kasutajad näevad ainult Power BI andmeid, millele neil on juurdepääs.</span><span class="sxs-lookup"><span data-stu-id="88ce0-106">This functionality helps guarantee that users see only Power BI data that they are granted access to.</span></span>

## <a name="overview"></a><span data-ttu-id="88ce0-107">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="88ce0-107">Overview</span></span>

<span data-ttu-id="88ce0-108">**Kuluarvestuse analüüsi** Microsoft Power BI sisu kasutab Power BI reatasemel turvet kasutaja juurdepääsu piiramiseks.</span><span class="sxs-lookup"><span data-stu-id="88ce0-108">The **Cost accounting analysis** Microsoft Power BI content uses Power BI row-level security to limit a user's access.</span></span> <span data-ttu-id="88ce0-109">Turve põhineb juurdepääsutaseme organisatsioonihierarhial, mis seadistatakse kuluarvestuse parameetrites.</span><span class="sxs-lookup"><span data-stu-id="88ce0-109">Security is based on the access-level organizational hierarchy that is set up in the Cost accounting parameters.</span></span> <span data-ttu-id="88ce0-110">**Kuluarvestuse analüüsi** Power BI sisu kohta lisateabe saamiseks vaadake teemat [Kuluarvestuse analüüsi Power BI sisu](cost-accounting-analysis-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="88ce0-110">For more information about the **Cost accounting analysis** Power BI content, see [Cost accounting analysis Power BI content](cost-accounting-analysis-content-pack.md).</span></span>

## <a name="setup"></a><span data-ttu-id="88ce0-111">Seadistus</span><span class="sxs-lookup"><span data-stu-id="88ce0-111">Setup</span></span>
<span data-ttu-id="88ce0-112">Power BI-le juurdepääsutaseme turbe levitamiseks peab Power BI sisu omanik järgima neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="88ce0-112">To propagate access-level security to Power BI, the owner of the Power BI content must follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="88ce0-113">**Kuluarvestuse analüüsi** Power BI sisu avaldanud kasutaja muutub automaatselt omanikuks.</span><span class="sxs-lookup"><span data-stu-id="88ce0-113">The user who publishes the **Cost accounting analysis** Power BI content automatically becomes the owner.</span></span> <span data-ttu-id="88ce0-114">Ainult omanik saab Power BI-s turvet seadistada.</span><span class="sxs-lookup"><span data-stu-id="88ce0-114">Only an owner can set up security in Power BI.</span></span> <span data-ttu-id="88ce0-115">Peale selle ei saa mitte keegi peale omaniku näha **kuluarvestuse analüüsi** Power BI sisus olevaid andmeid, kuni omanik lisab veebisaidile PowerBI.com teised kasutajad.</span><span class="sxs-lookup"><span data-stu-id="88ce0-115">Additionally, until an owner adds other users on PowerBI.com, no one except the owner can see any data in the **Cost accounting analysis** Power BI content.</span></span>

1. <span data-ttu-id="88ce0-116">Definitsioonifaili avaldamine Power BI-sse.</span><span class="sxs-lookup"><span data-stu-id="88ce0-116">Publish the definition file to Power BI.</span></span>
2. <span data-ttu-id="88ce0-117">Logige saidile PowerBI.com sisse.</span><span class="sxs-lookup"><span data-stu-id="88ce0-117">Sign in to PowerBI.com.</span></span>
3. <span data-ttu-id="88ce0-118">Leidke **kuluarvestuse analüüsi** Power BI sisu jaoks andmekogum.</span><span class="sxs-lookup"><span data-stu-id="88ce0-118">Find the dataset for the **Cost accounting analysis** Power BI content.</span></span>
4. <span data-ttu-id="88ce0-119">Avage turbe leht.</span><span class="sxs-lookup"><span data-stu-id="88ce0-119">Open the security page.</span></span>

    ![Turbelehe avamine](./media/CA-picture-1.png)

5. <span data-ttu-id="88ce0-121">Roll **Kuluobjekti kontroller** on juba loodud.</span><span class="sxs-lookup"><span data-stu-id="88ce0-121">The **Cost object controller** role is already created.</span></span> <span data-ttu-id="88ce0-122">Lisage teisi liikmeid, kes kuuluvad kuluarvestuse juurdepääsutaseme organisatsioonihierarhiasse.</span><span class="sxs-lookup"><span data-stu-id="88ce0-122">Add other members who are part of the Cost accounting access-level organizational hierarchy.</span></span>

    ![Liikmete lisamine](./media/CA-picture-2.png)

<span data-ttu-id="88ce0-124">Kasutajad, kes lisatakse rollile **Kuluobjekti kontroller**, näevad ainult neid andmeid, mida neil on kuluarvestuse juurdepääsutaseme organisatsioonihierarhia määratluse järgi lubatud näha.</span><span class="sxs-lookup"><span data-stu-id="88ce0-124">Users who are added to the **Cost object controller** role will see only the data that they are allowed to see, according to the definition in the Cost accounting access-level organizational hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="88ce0-125">Reatasemel turve kohaldub paanidele ja aruannetele, mis on manustatud Power BI-st.</span><span class="sxs-lookup"><span data-stu-id="88ce0-125">Row-level security applies to tiles and reports that are embedded from Power BI.</span></span>

## <a name="updating-security"></a><span data-ttu-id="88ce0-126">Turbe värskendamine</span><span class="sxs-lookup"><span data-stu-id="88ce0-126">Updating security</span></span>
<span data-ttu-id="88ce0-127">Kui värskendused tehakse kuluarvestuses juurdepääsutasemel turbele ja soovite, et Power BI kajastaks neid värskendusi, peate värskendama kogu kauplust **kuluarvestuse analüüsi** Power BI sisu jaoks.</span><span class="sxs-lookup"><span data-stu-id="88ce0-127">If updates are made to access-level security in Cost accounting, and you want Power BI to reflect those updates, you must update the entity store for the **Cost accounting analysis** Power BI content.</span></span> <span data-ttu-id="88ce0-128">Pärast üksuse kaupluse uuenduse lõpuleviimist peate uuendama artefaktid saidil PowerBI.com.</span><span class="sxs-lookup"><span data-stu-id="88ce0-128">After you complete the entity store update you must update the artifacts on PowerBI.com.</span></span> <span data-ttu-id="88ce0-129">Üksuse kaupluse värskenduse kohta lisateabe saamiseks vaadake teemat [Üksuse kaupluse värskendamine](power-bi-integration-entity-store.md#update-entity-store).</span><span class="sxs-lookup"><span data-stu-id="88ce0-129">For more information about how to do an entity store update, see [Update entity store](power-bi-integration-entity-store.md#update-entity-store).</span></span> <span data-ttu-id="88ce0-130">Kui uutele kasutajatele antakse juurdepääs organisatsioonihierarhiale, peab **kuluarvestuse analüüsi** Power BI sisu omanik tegema ka üksuse kaupluse värskenduse.</span><span class="sxs-lookup"><span data-stu-id="88ce0-130">The owner of the **Cost accounting analysis** Power BI content must also do an entity store update if new users are granted access to the organizational hierarchy.</span></span> <span data-ttu-id="88ce0-131">Lisaks peab omanik saidil PowerBI.com lisama rollile **Kuluobjekti kontroller** uusi kasutajaid, et neile rakendataks reatasemel turvet.</span><span class="sxs-lookup"><span data-stu-id="88ce0-131">Additionally, the owner must add the new users to the **Cost object controller** role on PowerBI.com, so that row-level security is applied for them.</span></span>

## <a name="disabling-security"></a><span data-ttu-id="88ce0-132">Turbe keelamine</span><span class="sxs-lookup"><span data-stu-id="88ce0-132">Disabling security</span></span>
<span data-ttu-id="88ce0-133">Eeldame, et teie organisatsioon soovib andmetele juurdepääsu piirata.</span><span class="sxs-lookup"><span data-stu-id="88ce0-133">We assume that your organization wants to restrict data access.</span></span> <span data-ttu-id="88ce0-134">Kui turbeparameetrid mingil põhjusel kuluaruandluse käitamisel keelatakse, peab omanik Power BI-s rollile **Kuluarvestaja** kasutajaid lisama.</span><span class="sxs-lookup"><span data-stu-id="88ce0-134">If, for some reason, the security parameters are disabled when you run Cost accounting, the owner must add users to the **Cost accountant** role in Power BI instead.</span></span> <span data-ttu-id="88ce0-135">Kui muudate turbe lubatud olekust keelatud olekusse, on mõttekas eemaldada kasutajad rollist **Kuluobjekti kontroller**.</span><span class="sxs-lookup"><span data-stu-id="88ce0-135">If you change security from an enabled state to a disabled state, it's a good idea to remove users from the **Cost object controller** role.</span></span> <span data-ttu-id="88ce0-136">Ja vastupidi, kui turbe uuesti lubate.</span><span class="sxs-lookup"><span data-stu-id="88ce0-136">And vice versa if you re-enable security.</span></span> <span data-ttu-id="88ce0-137">Kasutajad saavad mõlemasse rolli kuuluda.</span><span class="sxs-lookup"><span data-stu-id="88ce0-137">Users can belong to both roles.</span></span> <span data-ttu-id="88ce0-138">Ühine juurdepääs on mõlema rolli liit.</span><span class="sxs-lookup"><span data-stu-id="88ce0-138">Joint access is the union of both roles.</span></span> <span data-ttu-id="88ce0-139">**Kuluarvestuse analüüsi** Power BI sisu korral on ühise juurdepääsuga kasutajatel piiramatu andmetele juurdepääs.</span><span class="sxs-lookup"><span data-stu-id="88ce0-139">In the case of the **Cost accounting analysis** Power BI content, users who have joint access have unrestricted data access.</span></span> <span data-ttu-id="88ce0-140">Kui teie eesmärk on rakendada piiratud juurdepääsu, tuleb kasutajad määrata ainult rollile **Kuluobjekti kontroller**.</span><span class="sxs-lookup"><span data-stu-id="88ce0-140">If your goal is to apply restricted access, users must be assigned only to the **Cost object controller** role.</span></span> <span data-ttu-id="88ce0-141">Need reatasemel turbevärskendused jõustuvad koheselt.</span><span class="sxs-lookup"><span data-stu-id="88ce0-141">These row-level security updates take effect immediately.</span></span> <span data-ttu-id="88ce0-142">Asjassepuutuvad kasutajad peaksid värskendama oma brausereid.</span><span class="sxs-lookup"><span data-stu-id="88ce0-142">Affected users should refresh their browsers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="88ce0-143">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="88ce0-143">Additional resources</span></span>
<span data-ttu-id="88ce0-144">Power BI reatasemel turbe kohta lisateabe saamiseks vaadake teemat [Turbe haldamine teie Power BI mudelis](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span><span class="sxs-lookup"><span data-stu-id="88ce0-144">To learn more about Power BI row-level security, see [Manage security on your model in Power BI](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span></span>
