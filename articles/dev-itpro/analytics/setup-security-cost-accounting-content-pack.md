---
title: "Kuluarvestuse analüüsi Power BI sisu jaoks turbe seadistamine"
description: "Selles teemas selgitatakse, kuidas saate kuluarvestuses juurdepääsutaseme turbe Microsoft Power BI-s reatasemel turbeks muuta. See funktsioon aitab tagada, et kasutajad näevad ainult Power BI andmeid, millele neil on juurdepääs."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e0c0faf0b12368273decacfae88c57707b350bf4
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a><span data-ttu-id="e9304-104">Kuluarvestuse analüüsi Power BI sisu jaoks turbe seadistamine</span><span class="sxs-lookup"><span data-stu-id="e9304-104">Set up security for the Cost accounting analysis Power BI content</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e9304-105">Selles teemas selgitatakse, kuidas saate kuluarvestuses juurdepääsutaseme turbe Microsoft Power BI-s reatasemel turbeks muuta.</span><span class="sxs-lookup"><span data-stu-id="e9304-105">This topic explains how you can propagate the access-level security in Cost accounting to row-level security in Microsoft Power BI.</span></span> <span data-ttu-id="e9304-106">See funktsioon aitab tagada, et kasutajad näevad ainult Power BI andmeid, millele neil on juurdepääs.</span><span class="sxs-lookup"><span data-stu-id="e9304-106">This functionality helps guarantee that users see only Power BI data that they are granted access to.</span></span>

<a name="overview"></a><span data-ttu-id="e9304-107">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="e9304-107">Overview</span></span>
--------

<span data-ttu-id="e9304-108">**Kuluarvestuse analüüsi** Microsoft Power BI sisu kasutab Power BI reatasemel turvet kasutaja juurdepääsu piiramiseks.</span><span class="sxs-lookup"><span data-stu-id="e9304-108">The **Cost accounting analysis** Microsoft Power BI content uses Power BI row-level security to limit a user's access.</span></span> <span data-ttu-id="e9304-109">Turve põhineb juurdepääsutaseme organisatsioonihierarhial, mis seadistatakse kuluarvestuse parameetrites.</span><span class="sxs-lookup"><span data-stu-id="e9304-109">Security is based on the access-level organizational hierarchy that is set up in the Cost accounting parameters.</span></span> <span data-ttu-id="e9304-110">**Kuluarvestuse analüüsi** Power BI sisu kohta lisateabe saamiseks vaadake teemat [Kuluarvestuse analüüs Power BI sisu](cost-accounting-analysis-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="e9304-110">For more information about the **Cost accounting analysis** Power BI content, see [Cost accounting analysis Power BI content](cost-accounting-analysis-content-pack.md).</span></span>

## <a name="setup"></a><span data-ttu-id="e9304-111">Häälestus</span><span class="sxs-lookup"><span data-stu-id="e9304-111">Setup</span></span>
<span data-ttu-id="e9304-112">Power BI-le juurdepääsutaseme turbe levitamiseks peab Power BI sisu omanik järgima neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="e9304-112">To propagate access-level security to Power BI, the owner of the Power BI content must follow these steps.</span></span> <span data-ttu-id="e9304-113">**Märkus.** **Kuluarvestuse analüüsi** Power BI sisu avaldav kasutaja muutub automaatselt omanikuks.</span><span class="sxs-lookup"><span data-stu-id="e9304-113">**Note:** The user who publishes the **Cost accounting analysis** Power BI content automatically becomes the owner.</span></span> <span data-ttu-id="e9304-114">Ainult omanik saab Power BI-s turvet seadistada.</span><span class="sxs-lookup"><span data-stu-id="e9304-114">Only an owner can set up security in Power BI.</span></span> <span data-ttu-id="e9304-115">Lisaks ei saa mitte keegi peale omaniku näha **Kuluarvestuse analüüsi** Power BI sisus olevaid andmeid, kuni omanik lisab veebisaidile PowerBI.com teised kasutajad.</span><span class="sxs-lookup"><span data-stu-id="e9304-115">Additionally, until an owner adds other users on PowerBI.com, no one except the owner can see any data in the **Cost accounting analysis** Power BI content.</span></span>

1.  <span data-ttu-id="e9304-116">Definitsioonifaili avaldamine Power BI-sse.</span><span class="sxs-lookup"><span data-stu-id="e9304-116">Publish the definition file to Power BI.</span></span>
2.  <span data-ttu-id="e9304-117">Logige saidile PowerBI.com sisse.</span><span class="sxs-lookup"><span data-stu-id="e9304-117">Sign in to PowerBI.com.</span></span>
3.  <span data-ttu-id="e9304-118">Leidke **kuluarvestuse analüüsi** Power BI sisu jaoks andmekogum.</span><span class="sxs-lookup"><span data-stu-id="e9304-118">Find the dataset for the **Cost accounting analysis** Power BI content.</span></span>
4.  <span data-ttu-id="e9304-119">Avage turbe leht.</span><span class="sxs-lookup"><span data-stu-id="e9304-119">Open the security page.</span></span> 

    ![Turbelehe avamine](./media/CA-picture-1.png)

5.  <span data-ttu-id="e9304-121">Roll **Kuluobjekti kontroller** on juba loodud.</span><span class="sxs-lookup"><span data-stu-id="e9304-121">The **Cost object controller** role is already created.</span></span> <span data-ttu-id="e9304-122">Lisage teisi liikmeid, kes kuuluvad kuluarvestuse juurdepääsutaseme organisatsioonihierarhiasse.</span><span class="sxs-lookup"><span data-stu-id="e9304-122">Add other members who are part of the Cost accounting access-level organizational hierarchy.</span></span> 

    ![Liikmete lisamine](./media/CA-picture-2.png)

<span data-ttu-id="e9304-124">Kasutajad, kes lisatakse rollile **Kuluobjekti kontroller**, näevad ainult neid andmeid, mida neil on kuluarvestuse juurdepääsutaseme organisatsioonihierarhia määratluse järgi lubatud näha.</span><span class="sxs-lookup"><span data-stu-id="e9304-124">Users who are added to the **Cost object controller** role will see only the data that they are allowed to see, according to the definition in the Cost accounting access-level organizational hierarchy.</span></span> <span data-ttu-id="e9304-125">**Märkus** Reatasemel turve kehtib rakenduses Microsoft Dynamics 365 for Finance and Operations olevatele paanidele ja aruannetele, mis manustatakse Power BI kaudu.</span><span class="sxs-lookup"><span data-stu-id="e9304-125">**Note:** Row-level security applies to tiles and reports in Microsoft Dynamics 365 for Finance and Operations that are embedded from Power BI.</span></span>

## <a name="updating-security"></a><span data-ttu-id="e9304-126">Turbe värskendamine</span><span class="sxs-lookup"><span data-stu-id="e9304-126">Updating security</span></span>
<span data-ttu-id="e9304-127">Kui värskendused tehakse kuluarvestuses juurdepääsutasemel turbele ja soovite, et Power BI kajastaks neid värskendusi, peate värskendama kogu kauplust **kuluarvestuse analüüsi** Power BI sisu jaoks.</span><span class="sxs-lookup"><span data-stu-id="e9304-127">If updates are made to access-level security in Cost accounting, and you want Power BI to reflect those updates, you must update the entity store for the **Cost accounting analysis** Power BI content.</span></span> <span data-ttu-id="e9304-128">Pärast rakenduse Finance and Operations kaudu üksuse kaupluse uuenduse lõpuleviimist peate uuendama artefaktid saidil PowerBI.com. Üksuse kaupluse värskenduse kohta lisateabe saamiseks vaadake teemat [Üksuse kaupluse värskendamine](power-bi-integration-entity-store.md#update-entity-store).</span><span class="sxs-lookup"><span data-stu-id="e9304-128">After you complete the entity store update from Finance and Operations, you must update the artifacts on PowerBI.com. For more information about how to do an entity store update, see [Update entity store](power-bi-integration-entity-store.md#update-entity-store).</span></span> <span data-ttu-id="e9304-129">Kui uutele kasutajatele antakse juurdepääs organisatsioonihierarhiale, peab **kuluarvestuse analüüsi** Power BI sisu omanik tegema ka üksuse kaupluse värskenduse.</span><span class="sxs-lookup"><span data-stu-id="e9304-129">The owner of the **Cost accounting analysis** Power BI content must also do an entity store update if new users are granted access to the organizational hierarchy.</span></span> <span data-ttu-id="e9304-130">Lisaks peab omanik saidil PowerBI.com lisama rollile **Kuluobjekti kontroller** uusi kasutajaid, et neile rakendataks reatasemel turvet.</span><span class="sxs-lookup"><span data-stu-id="e9304-130">Additionally, the owner must add the new users to the **Cost object controller** role on PowerBI.com, so that row-level security is applied for them.</span></span>

## <a name="disabling-security"></a><span data-ttu-id="e9304-131">Turbe keelamine</span><span class="sxs-lookup"><span data-stu-id="e9304-131">Disabling security</span></span>
<span data-ttu-id="e9304-132">Eeldame, et teie organisatsioon soovib andmetele juurdepääsu piirata.</span><span class="sxs-lookup"><span data-stu-id="e9304-132">We assume that your organization wants to restrict data access.</span></span> <span data-ttu-id="e9304-133">Kui turbeparameetrid mingil põhjusel kuluaruandluse käitamisel keelatakse, peab omanik Power BI-s rollile **Kuluarvestaja** kasutajaid lisama.</span><span class="sxs-lookup"><span data-stu-id="e9304-133">If, for some reason, the security parameters are disabled when you run Cost accounting, the owner must add users to the **Cost accountant** role in Power BI instead.</span></span> <span data-ttu-id="e9304-134">Kui muudate turbe lubatud olekust keelatud olekusse, on mõttekas eemaldada kasutajad rollist **Kuluobjekti kontroller**.</span><span class="sxs-lookup"><span data-stu-id="e9304-134">If you change security from an enabled state to a disabled state, it’s a good idea to remove users from the **Cost object controller** role.</span></span> <span data-ttu-id="e9304-135">Ja vastupidi, kui turbe uuesti lubate.</span><span class="sxs-lookup"><span data-stu-id="e9304-135">And vice versa if you re-enable security.</span></span> <span data-ttu-id="e9304-136">Kasutajad saavad mõlemasse rolli kuuluda.</span><span class="sxs-lookup"><span data-stu-id="e9304-136">Users can belong to both roles.</span></span> <span data-ttu-id="e9304-137">Ühine juurdepääs on mõlema rolli liit.</span><span class="sxs-lookup"><span data-stu-id="e9304-137">Joint access is the union of both roles.</span></span> <span data-ttu-id="e9304-138">**Kuluarvestuse analüüsi** Power BI sisu korral on ühise juurdepääsuga kasutajatel piiramatu andmetele juurdepääs.</span><span class="sxs-lookup"><span data-stu-id="e9304-138">In the case of the **Cost accounting analysis** Power BI content, users who have joint access have unrestricted data access.</span></span> <span data-ttu-id="e9304-139">Kui teie eesmärk on rakendada piiratud juurdepääsu, tuleb kasutajad määrata ainult rollile **Kuluobjekti kontroller**.</span><span class="sxs-lookup"><span data-stu-id="e9304-139">If your goal is to apply restricted access, users must be assigned only to the **Cost object controller** role.</span></span> <span data-ttu-id="e9304-140">Need reatasemel turbevärskendused jõustuvad koheselt.</span><span class="sxs-lookup"><span data-stu-id="e9304-140">These row-level security updates take effect immediately.</span></span> <span data-ttu-id="e9304-141">Asjassepuutuvad kasutajad peaksid värskendama oma brausereid.</span><span class="sxs-lookup"><span data-stu-id="e9304-141">Affected users should refresh their browsers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e9304-142">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="e9304-142">Additional resources</span></span>
<span data-ttu-id="e9304-143">Power BI reatasemel turbe kohta lisateabe saamiseks vaadake teemat [Turbe haldamine teie Power BI mudelis](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span><span class="sxs-lookup"><span data-stu-id="e9304-143">To learn more about Power BI row-level security, see [Manage security on your model in Power BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span></span>




