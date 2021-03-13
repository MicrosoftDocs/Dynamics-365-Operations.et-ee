---
title: Mitmetasandiline vara
description: Selles teemas selgitatakse, kuidas luua ja kustutada mitmetasandilist vara.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd4da57c3849095909226db53c23b3c25301acdc
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021318"
---
# <a name="multi-level-assets"></a><span data-ttu-id="21857-103">Mitmetasandiline vara</span><span class="sxs-lookup"><span data-stu-id="21857-103">Multi-level assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="21857-104">Selles teemas selgitatakse, kuidas luua ja kustutada mitmetasandilist vara.</span><span class="sxs-lookup"><span data-stu-id="21857-104">This topic explains how to create and delete multi-level assets.</span></span> <span data-ttu-id="21857-105">Hierarhilises puustruktuuris saate luua varasid ja seotud allvarasid.</span><span class="sxs-lookup"><span data-stu-id="21857-105">You can create assets and related sub-assets in a hierarchical tree structure.</span></span> <span data-ttu-id="21857-106">Sel viisil saate kuvada varade vahelisi suhteid ja sõltuvusi.</span><span class="sxs-lookup"><span data-stu-id="21857-106">In this way, you can show relations and dependencies among assets.</span></span> <span data-ttu-id="21857-107">Hooldustöid saab seostada kõigil puustruktuuri tasemetel.</span><span class="sxs-lookup"><span data-stu-id="21857-107">Maintenance jobs can be related to all levels of the tree structure.</span></span> <span data-ttu-id="21857-108">Statistikat saab luua ka üksiku taseme või kõigi alamvarade tasemete summana.</span><span class="sxs-lookup"><span data-stu-id="21857-108">Statistics can also be created for an individual level or as a sum of all sub-asset levels.</span></span>

<span data-ttu-id="21857-109">Loendilehel **Kõik varad** (**Varahaldus**\>**Ühised**\>**Varad**\>**Kõik varad**), loendab veerg **Vara** varad hierarhilises järjestuses.</span><span class="sxs-lookup"><span data-stu-id="21857-109">On the **All Assets** list page (**Asset management** \> **Common** \> **Assets** \> **All assets**), the **Asset** column lists assets in hierarchical order.</span></span> <span data-ttu-id="21857-110">**Emaveerg** näitab seostuvat vanemat.</span><span class="sxs-lookup"><span data-stu-id="21857-110">The **Parent** column shows the related parent.</span></span> <span data-ttu-id="21857-111">Lisaks, kui varad ja allvarad on juba loodud kuvatakse jaotise **Vara puu** paanil **Seotud teave** varad puustruktuuris.</span><span class="sxs-lookup"><span data-stu-id="21857-111">Additionally, if assets and sub-assets have already been created, the **Asset tree** section in the **Related information** pane shows the assets in a tree structure.</span></span>

<span data-ttu-id="21857-112">Teabe saamiseks vara loomise kohta vt teemat [Vara loomine](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="21857-112">For information about how to create an asset, see [Create an asset](../objects/create-an-object.md).</span></span> <span data-ttu-id="21857-113">Alamvara loomiseks valige emavara väli **Ema** kiirkaardil **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="21857-113">To create a sub-asset, select the parent asset in the **Parent** field on the **General** FastTab.</span></span>

## <a name="copy-an-asset-or-asset-structure"></a><span data-ttu-id="21857-114">Vara või vara struktuuri kopeerimine</span><span class="sxs-lookup"><span data-stu-id="21857-114">Copy an asset or asset structure</span></span>

<span data-ttu-id="21857-115">Kui teie ettevõttel on mitu sarnast varade struktuuri, saate nende kiireks loomiseks kasutada funktsiooni Kopeeri varahalduses.</span><span class="sxs-lookup"><span data-stu-id="21857-115">If your company has several similar asset structures, you can use the Copy function in Asset Management to quickly create them.</span></span>

1. <span data-ttu-id="21857-116">Valige **Varahaldus**\>**Ühised**\>**Varad**\>**Kõik varad**.</span><span class="sxs-lookup"><span data-stu-id="21857-116">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="21857-117">Leheloendis **Kõik varad** valige kopeeritav vara.</span><span class="sxs-lookup"><span data-stu-id="21857-117">On the **All assets** list page, select the asset to copy.</span></span> <span data-ttu-id="21857-118">Näiteks kui soovite kopeerida kogu vara struktuuri (sh alamvarasid), valige emavara.</span><span class="sxs-lookup"><span data-stu-id="21857-118">For example, if you want to copy the whole asset structure, including sub-assets, select a parent asset.</span></span>
3. <span data-ttu-id="21857-119">Valige **Kopeeri vara**.</span><span class="sxs-lookup"><span data-stu-id="21857-119">Select **Copy asset**.</span></span> <span data-ttu-id="21857-120">Jaotises **Kopeeri asukohast** on välja **Vara** väärtuseks sätestatud vara, mille valisite loendilehelt.</span><span class="sxs-lookup"><span data-stu-id="21857-120">In the **Copy from** section, the **Asset** field is set to the asset that you selected on the list page.</span></span>
4. <span data-ttu-id="21857-121">Jaotise **Kopeeri asukohta** väljale **Vara** sisestage uue vara nimi.</span><span class="sxs-lookup"><span data-stu-id="21857-121">In the **Copy to** section, in the **Asset** field, enter the name of the new asset.</span></span>
5. <span data-ttu-id="21857-122">Kui loodava vara väärtus peaks olema osa olemasolevast varastruktuurist valige jaotise **Emavara** välja **Vara** jaoks emavara ID.</span><span class="sxs-lookup"><span data-stu-id="21857-122">If the asset that you're creating should be part of an existing asset structure, in the **Parent asset** section, in the **Asset** field, select a parent ID.</span></span>
6. <span data-ttu-id="21857-123">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="21857-123">Select **OK**.</span></span> <span data-ttu-id="21857-124">Uus varade struktuur kuvatakse loendilehel **Kõik varad**.</span><span class="sxs-lookup"><span data-stu-id="21857-124">The new asset structure is shown on the **All assets** list page.</span></span> <span data-ttu-id="21857-125">Kõik kopeeritud varaga seotud vara atribuudid, hooldusplaanid ja hooldusringid kantakse üle uuele varale või vara struktuurile.</span><span class="sxs-lookup"><span data-stu-id="21857-125">All asset attributes, maintenance plans, and maintenance rounds that are related to the asset that you copied are transferred to the new asset or asset structure.</span></span>

<span data-ttu-id="21857-126">Vara struktuuri kopeerimisel on uue struktuuri alamvaradel kopeeritud alamvaradega sama nimi.</span><span class="sxs-lookup"><span data-stu-id="21857-126">When you copy an asset structure, the sub-assets in the new structure have the same name as the sub-assets that you copied.</span></span> <span data-ttu-id="21857-127">Kui kopeerimisprotseduur on lõpule viidud, saate hõlpsalt muuta vara nime ja muid sätteid.</span><span class="sxs-lookup"><span data-stu-id="21857-127">After the copy procedure is completed, you can easily change the name and other settings for an asset.</span></span> <span data-ttu-id="21857-128">Valige loendilehel **Kõik varad** ja seejärel valige nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="21857-128">Select the asset on the **All assets** list page, and then select the **Edit** button.</span></span>

> [!NOTE]
> <span data-ttu-id="21857-129">Vara või vara struktuuri kopeerimisel lähtestatakse uue vara elutsükli olek mis tahes olekusse, mille määratlete varade algse elutsükli olekuna.</span><span class="sxs-lookup"><span data-stu-id="21857-129">When you copy an asset or asset structure, the lifecycle state of the new assets is reset to whatever state you defined as the initial lifecycle state for assets.</span></span> <span data-ttu-id="21857-130">Funktsionaalne asukoht lähtestatakse vaikimisi funktsionaalsele asukohale.</span><span class="sxs-lookup"><span data-stu-id="21857-130">The functional location is reset to the default functional location.</span></span>

## <a name="delete-an-asset-or-asset-structure"></a><span data-ttu-id="21857-131">Vara või vara struktuuri kustutamine</span><span class="sxs-lookup"><span data-stu-id="21857-131">Delete an asset or asset structure</span></span>

<span data-ttu-id="21857-132">Kui varal on seotud alamvara, saate selle kustutada ainult siis, kui ühegi vara kohta pole registreeritud ühtegi hooldustaotlust, töötellimuse tööd, puuduste registreerimist ega seisundi hindamist.</span><span class="sxs-lookup"><span data-stu-id="21857-132">If an asset has related sub-assets, you can delete it only if no maintenance requests, work order jobs, fault registrations, or condition assessments are registered on any of the assets.</span></span>

1. <span data-ttu-id="21857-133">Valige loendilehel **Kõik varad** vara, mida soovite kustutada.</span><span class="sxs-lookup"><span data-stu-id="21857-133">On the **All assets** list page, select the asset to delete.</span></span>
2. <span data-ttu-id="21857-134">Valige **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="21857-134">Select **Delete**.</span></span>

> [!NOTE]
> <span data-ttu-id="21857-135">Kui te ei saa seda protseduuri kasutades vara kustutada, on teine viis kustutamise käsitlemiseks luua selleks otstarbeks vara elutsükli olek.</span><span class="sxs-lookup"><span data-stu-id="21857-135">If you can't delete an asset by using this procedure, another way to handle deletion is to set up an asset lifecycle state for this purpose.</span></span> <span data-ttu-id="21857-136">Näiteks saate seadistada elutsükli olekuks **Mahakantud** või **Kustutatud** lehel **Vara elutsükli olekud**.</span><span class="sxs-lookup"><span data-stu-id="21857-136">For example, you can set up a **Scrapped** or **Deleted** lifecycle state on the **Asset lifecycle states** page.</span></span>
