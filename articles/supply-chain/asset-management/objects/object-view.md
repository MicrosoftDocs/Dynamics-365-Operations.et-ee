---
title: Vara vaade
description: Selles teemas kirjeldatakse vara vaadet varahalduses.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectTree, EntAssetFunctionalLocationTree
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0256cc86dc306c8addb37d2c8f335470b19177a
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019400"
---
# <a name="asset-view"></a><span data-ttu-id="ef27b-103">Vara vaade</span><span class="sxs-lookup"><span data-stu-id="ef27b-103">Asset view</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="ef27b-104">Selles teemas kirjeldatakse vara vaadet varahalduses.</span><span class="sxs-lookup"><span data-stu-id="ef27b-104">This topic describes the asset view in Asset Management.</span></span> <span data-ttu-id="ef27b-105">Lehel **Vara vaade** kuvatakse puuvaates aktiivsed varad ja funktsionaalsed asukohad.</span><span class="sxs-lookup"><span data-stu-id="ef27b-105">The **Asset view** page shows active assets and functional locations in a tree view.</span></span> <span data-ttu-id="ef27b-106">Seetõttu saate kergesti ülevaate varade suhetest funktsionaalsete asukohtade suhtes.</span><span class="sxs-lookup"><span data-stu-id="ef27b-106">Therefore, you can easily get an overview of asset relations to functional locations.</span></span> <span data-ttu-id="ef27b-107">Lisaks saate vaadata üksikasjalikku teavet funktsionaalsete asukohtade, varade ja seotud koosluste (BOM-ide) kohta.</span><span class="sxs-lookup"><span data-stu-id="ef27b-107">Additionally, you can view detailed information about functional locations, assets, and related bills of materials (BOMs).</span></span> <span data-ttu-id="ef27b-108">Samuti saate kiire ülevaate aktiivsete hooldustaotluste ja varaga seotud töökäskude kohta.</span><span class="sxs-lookup"><span data-stu-id="ef27b-108">You can also get a quick overview of active maintenance requests and work orders that are related to an asset.</span></span>

1. <span data-ttu-id="ef27b-109">Valige **Varahaldus**\>**Ühised**\>**Varad**\>**Varavaade**.</span><span class="sxs-lookup"><span data-stu-id="ef27b-109">Select **Asset management** \> **Common** \> **Assets** \> **Asset view**.</span></span>
2. <span data-ttu-id="ef27b-110">Lehel kuvatava vaate muutmiseks valige uus väärtus väljal **Vaade**.</span><span class="sxs-lookup"><span data-stu-id="ef27b-110">To change the view that is shown on the page, select a new value in the **View** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef27b-111">Vaikevaade, mis kuvatakse lehe **Vara vaade** avamisel, sõltub sellest väärtusest, mis on valitud väljal **Vaade** vahekaardil **Varad** lehel **Varahalduse parameetrid** e (**Varahaldus**\>**Häälestus**\>**Varahalduse parameetrid**).</span><span class="sxs-lookup"><span data-stu-id="ef27b-111">The default view that is shown when you open the **Asset view** page depends on the value that is selected in the **View** field on the **Assets** tab of the **Asset management parameters** page (**Asset management** \> **Setup** \> **Asset management parameters**).</span></span>

<span data-ttu-id="ef27b-112">Lehe parempoolses servas kuvab kiirkaart valitud vaate üksikasju.</span><span class="sxs-lookup"><span data-stu-id="ef27b-112">On the right side of the page, FastTabs shows details of the selected view.</span></span>

<span data-ttu-id="ef27b-113">Puustruktuuri kohal kuvatav lingirea rada näitab praegust valikut puuvaates.</span><span class="sxs-lookup"><span data-stu-id="ef27b-113">The breadcrumb trail that appears above the tree view shows the current selection in the tree view.</span></span> <span data-ttu-id="ef27b-114">See lingirea rada kasutab järgmist vormingut.</span><span class="sxs-lookup"><span data-stu-id="ef27b-114">This breadcrumb trail uses the following format:</span></span>

<span data-ttu-id="ef27b-115">Funktsionaalse asukoha ID / funktsionaalse asukoha ID (kui on rohkem kui üks funktsionaalne asukoht) \> Vara ID / Vara ID (kui on rohkem kui üks vara) – kaubakood.</span><span class="sxs-lookup"><span data-stu-id="ef27b-115">Functional location ID / Functional location ID (if there is more than one functional location) \> Asset ID / Asset ID (if there is more than one asset) - Item number.</span></span>

<span data-ttu-id="ef27b-116">Kui valisite vara puuvaates, saate valida kas **Aktiivsed taotlused** või **Aktiivsed töökäsud**, et vaadata varaga seotud hooldustaotlusi või töökäske.</span><span class="sxs-lookup"><span data-stu-id="ef27b-116">If you've selected an asset in the tree view, you can select **Active requests** or **Active work orders** to view the maintenance requests or work orders that are related to the asset.</span></span> <span data-ttu-id="ef27b-117">Seotud vaate avamiseks saate valida **Ava**\>**Funktsionaalne asukoht**, **Vara** või **Vara kooslus**.</span><span class="sxs-lookup"><span data-stu-id="ef27b-117">You can also select **Open** \> **Functional location**, **Asset**, or **Asset BOM** to open the related view.</span></span>

<span data-ttu-id="ef27b-118">Suvand **Vara funktsionaalsed asukohad**, mille saate valida väljal **Vaade**, on saadaval ka mis tahes vara otsingus, kus saate valida vara.</span><span class="sxs-lookup"><span data-stu-id="ef27b-118">The **Asset functional locations** option that you can select in the **View** field is also available in any asset lookup where you can select an asset.</span></span> <span data-ttu-id="ef27b-119">Puuvaade kuvatakse vahekaardil **Vara vaade**, näiteks kui [loote vara](../objects/create-an-object.md), loote hooldustaotluse või loote töökäsu.</span><span class="sxs-lookup"><span data-stu-id="ef27b-119">The tree view is shown on an **Asset view** tab, for example, where you [create an asset](../objects/create-an-object.md), create a maintenance request, or create a work order.</span></span>
