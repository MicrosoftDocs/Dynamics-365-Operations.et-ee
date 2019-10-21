---
title: Töökäsud ja põhivarad
description: Selles teemas selgitatakse töökäske ja põhivarasid varahalduses.
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
ms.openlocfilehash: 95fe394d22f9fe81511c230a2cf7b8ddf00d896f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250825"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="f16d0-103">Töökäsud ja põhivarad</span><span class="sxs-lookup"><span data-stu-id="f16d0-103">Work orders and fixed assets</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="f16d0-104">Varahalduses võivad varad olla seotud põhivaradega ja te saate luua nende varade jaoks töökäske.</span><span class="sxs-lookup"><span data-stu-id="f16d0-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="f16d0-105">Selle funktsiooni kasutamisel saate täieliku ülevaate põhivaradest, seotud investeerimisprojektidest ja investeerimisprojektide kohta registreeritud kuludest moodulis **Projekti haldus-ja raamatupidamine** ning moodulis **Põhivarad rakenduses**.</span><span class="sxs-lookup"><span data-stu-id="f16d0-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs registered on the investment projects in the **Project management and accounting** module and the **Fixed assets** module.</span></span>

>[!NOTE]
><span data-ttu-id="f16d0-106">Väli **Põhivara number** täidetakse ainult töökäsu tööprojektis, kui projektitüübiks on töökäsu projektis valitud "Investeering".</span><span class="sxs-lookup"><span data-stu-id="f16d0-106">The **Fixed asset number** field is only filled out on the work order job project if type "Investment" is selected as the project type on the work order job project.</span></span>

![Joonis 1](media/24-work-orders.png)

<span data-ttu-id="f16d0-108">Järgmises toimingus kirjeldatakse varade, töökäskude, töökäskude tööprojektide ja põhivarade vahelist seost.</span><span class="sxs-lookup"><span data-stu-id="f16d0-108">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="f16d0-109">Loote vara, mis on seotud põhivaraga, nagu näidatud alloleval joonisel.</span><span class="sxs-lookup"><span data-stu-id="f16d0-109">You create an asset that you relate to a fixed asset, as shown in the figure below.</span></span>

![Joonis 2](media/25-work-orders.png)

2. <span data-ttu-id="f16d0-111">Kui seadistate töötellimuse tüüpe (**Varahaldus** > **Seadistus** > **Töökäsud** > **Töökäskude tüübid**), loote investeeringute käsitlemiseks töökäsu tüübi.</span><span class="sxs-lookup"><span data-stu-id="f16d0-111">When you set up work order types (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="f16d0-112">Vt ka [Töökäskude tüübid](../setup-for-work-orders/work-order-types.md).</span><span class="sxs-lookup"><span data-stu-id="f16d0-112">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![Joonis 3](media/26-work-orders.png)

3. <span data-ttu-id="f16d0-114">Kui seadistate Töökäskude projektigrupid (**Varahaldus** > **Seadistus** > **Töökäsud** > **Projekti seadistus** > **Projektigrupp** link), loote seose investeeringuteks kasutatava töökäsu tüübi ja projektigrupi, mis on loodud investeeringuteks moodulis **Projektihaldus ja raamatupidamine**, vahel (**Projektihaldus ja raamatupidamine** > **Seadistus** > **Postitamine** > **Projektigrupid**).</span><span class="sxs-lookup"><span data-stu-id="f16d0-114">When you set up work order project groups (**Asset management** > **Setup** > **Work orders** > **Project setup** > **Project group** link), you create a relation between the work order type used for investments and the project group created for investments in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![Joonis 4](media/27-work-orders.png)

4. <span data-ttu-id="f16d0-116">Kui loote töökäsu, mis on seotud põhivara objektiga, valite investeeringute käsitlemiseks kasutatava töökäsu tüübi (nt "Investeering").</span><span class="sxs-lookup"><span data-stu-id="f16d0-116">When you create a work order that relates to a fixed asset object, you select the work order type used for handling investments, for example, "Investment".</span></span>

5. <span data-ttu-id="f16d0-117">Töökäsu loomisel kuvatakse seotud töökäsu tüüp kaardil **Kõik töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="f16d0-117">When the work order is created, the related work order type is shown in **All work orders**.</span></span>

![Joonis 5](media/28-work-orders.png)

6. <span data-ttu-id="f16d0-119">Kui töökäsk on loodud, luuakse töökäsuga seotud projekt kaardil **Projektihaldus ja raamatupidamine** > **Kõik projektid**.</span><span class="sxs-lookup"><span data-stu-id="f16d0-119">When the work order is created, the project related to the work order is created in **Project management and accounting** > **All projects**.</span></span> <span data-ttu-id="f16d0-120">Projektiga seotud teavet saate vaadata, kui klõpsate töökäsu lingil **Projekti ID** ( **Varahaldus**, avage töökäsk üksikasjade vaates > **Rea üksikasjad** FastTab > vahekaart **Üldine** > väli **Projekti ID**).</span><span class="sxs-lookup"><span data-stu-id="f16d0-120">You can see project-related information by clicking the **Project ID** link on the work order (in **Asset management**, open the work order in Details view > **Line details** FastTab > **General** tab > **Project ID** field).</span></span>

![Joonis 6](media/29-work-orders.png)

7. <span data-ttu-id="f16d0-122">Vahekaardil **Põhivarad** saate vaadata põhivaraga seotud projektide ülevaadet (**Põhivarad** > **Põhivarad** > **Põhivarad** > klõpsake väljal **Põhivara number** põhivaral > vaadake sisu paneelil **Seotud teave** > jaotises **Seotud projektid**).</span><span class="sxs-lookup"><span data-stu-id="f16d0-122">In **Fixed assets**, you are able to see an overview of the projects associated with a fixed asset (**Fixed assets** > **Fixed assets** > **Fixed assets** > click on the fixed asset in the **Fixed asset number** field > view the contents in the **Related information** pane > **Associated projects** section).</span></span>

