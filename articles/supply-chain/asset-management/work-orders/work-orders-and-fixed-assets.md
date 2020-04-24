---
title: Töökäsud ja põhivarad
description: Selles teemas selgitatakse töökäske ja põhivarasid varahalduses.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ca7a5d88de4308d7be9c1bc749b9dbf1da027c2c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208819"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="6d712-103">Töökäsud ja põhivarad</span><span class="sxs-lookup"><span data-stu-id="6d712-103">Work orders and fixed assets</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="6d712-104">Varahalduses võivad varad olla seotud põhivaradega ja te saate luua nende varade jaoks töökäske.</span><span class="sxs-lookup"><span data-stu-id="6d712-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="6d712-105">Selle funktsiooni kasutamisel saate täieliku ülevaate põhivaradest, seotud investeerimisprojektidest ja investeerimisprojektide kohta registreeritud kuludest moodulites **Projektihaldus ja -arvestus** ning **Põhivarad** rakenduses Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6d712-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs that are registered on the investment projects in the **Project management and accounting** and **Fixed assets** modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

>[!NOTE]
><span data-ttu-id="6d712-106">Väli **Põhivara kood** seatakse töökäsu tööprojektis ainult juhul, kui töökäsu tööprojektis on projektitüübiks valitud **Investeering**.</span><span class="sxs-lookup"><span data-stu-id="6d712-106">The **Fixed asset number** field on the work order job project is set only if **Investment** is selected as the project type on the work order job project.</span></span>

<span data-ttu-id="6d712-107">Alltoodud joonis näitab mooduli **Projektihaldus ja -arvestus** investeerimisprojekti ja töökäsu tööprojekti vahelist seost.</span><span class="sxs-lookup"><span data-stu-id="6d712-107">The illustration below shows the relation between an investment project in the **Project management and accounting** module and a work order job project.</span></span>

![Joonis 1](media/24-work-orders.png)

<span data-ttu-id="6d712-109">Järgmises toimingus kirjeldatakse varade, töökäskude, töökäskude tööprojektide ja põhivarade vahelist seost.</span><span class="sxs-lookup"><span data-stu-id="6d712-109">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="6d712-110">Loote vara, mille seostate mõne põhivaraga.</span><span class="sxs-lookup"><span data-stu-id="6d712-110">You create an asset that you relate to a fixed asset.</span></span>

![Joonis 2](media/25-work-orders.png)

2. <span data-ttu-id="6d712-112">Kui seadistate töökäsu tüüpe lehel **Töökäsu tüübid** (**Varahaldus** > **Seadistus** > **Töökäsud** > **Töökäsu tüübid**), loote investeeringute käitlemiseks töökäsu tüübi.</span><span class="sxs-lookup"><span data-stu-id="6d712-112">When you set up work order types on the **Work order types** page (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="6d712-113">Vt ka [Töökäskude tüübid](../setup-for-work-orders/work-order-types.md).</span><span class="sxs-lookup"><span data-stu-id="6d712-113">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![Joonis 3](media/26-work-orders.png)

3. <span data-ttu-id="6d712-115">Kui seadistate Töökäskude projektigrupid lehe **Töökäsu projekti seadistamine** vahekaardil **Projektigrupp** (**Varahaldus** > **Seadistus** > **Töökäsud** > **Projekti seadistus**), loote seose investeeringuteks kasutatava töökäsu tüübi ja projektigrupi, mis on investeeringuteks loodud mooduli **Projektihaldus ja -arvestus** lehel **Projektigrupid** (**Projektihaldus ja -arvestus** > **Seadistus** > **Sisestamine** > **Projektigrupid**).</span><span class="sxs-lookup"><span data-stu-id="6d712-115">When you set up work order project groups on the **Project group** tab of the **Work order project setup** page (**Asset management** > **Setup** > **Work orders** > **Project setup**), you create a relation between the work order type that is used for investments and the project group that was created for investments on the **Project groups** page in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![Joonis 4](media/27-work-orders.png)

4. <span data-ttu-id="6d712-117">Kui loote töökäsu, mis on seotud põhivaraga, valite investeeringute käitlemiseks kasutatava töökäsu tüübi, näiteks **Investeering**.</span><span class="sxs-lookup"><span data-stu-id="6d712-117">When you create a work order that is related to a fixed asset, you select the work order type that is used to handle investments, such as **Investment**.</span></span>

5. <span data-ttu-id="6d712-118">Töökäsu loomisel kuvatakse seotud töökäsu tüüp lehel **Kõik töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="6d712-118">When the work order is created, the related work order type is shown on the **All work orders** page.</span></span>

![Joonis 5](media/28-work-orders.png)

6. <span data-ttu-id="6d712-120">Kui töökäsk on loodud, siis luuakse töökäsuga seotud projekt mooduli **Projektihaldus ja -arvestus** lehel **Kõik projektid** (**Projektihaldus ja -arvestus** > **Projektid** > **Kõik projektid**).</span><span class="sxs-lookup"><span data-stu-id="6d712-120">When the work order is created, the project that is related to the work order is created on the **All projects** page in the **Project management and accounting** module (**Project management and accounting** > **Projects** > **All projects**).</span></span> <span data-ttu-id="6d712-121">Projektiga seotud teabe vaatamiseks valige mooduli **Varahaldus** lehe **Kõik töökäsud** üksikasjade vaates kiirkaardi **Rea üksikasjad** vahekaardi **Üldine** väljal **Projekti ID** kuvatud link (**Varahaldus** > **Üldine** > **Töökäsud** > **Kõik töökäsud**).</span><span class="sxs-lookup"><span data-stu-id="6d712-121">To view project-related information, select the link in the **Project ID** field on the **General** tab on the **Line details** FastTab in the details view of the **All work orders** page in the **Asset management** module (**Asset management** > **Commom** > **Work orders** > **All work orders**).</span></span>

![Joonis 6](media/29-work-orders.png)

7. <span data-ttu-id="6d712-123">Põhivaraga seotud projektide ülevaate vaatamiseks valige **Põhivarad** > **Põhivarad** > **Põhivarad**, seejärel valige väljal **Põhivara kood** üksikasjade vaate avamiseks soovitud põhivara link.</span><span class="sxs-lookup"><span data-stu-id="6d712-123">To see an overview of the projects associated with a fixed asset, select **Fixed assets** > **Fixed assets** > **Fixed assets**, and then, in the **Fixed asset number** field, select the link for the fixed asset to open the details view.</span></span> <span data-ttu-id="6d712-124">Laiendage lehe paremas servas paan **Seostuv teave** ja valige kiirkaart **Seotud projektid**.</span><span class="sxs-lookup"><span data-stu-id="6d712-124">Expand the **Related information** pane on the right side of the page, and select the **Associated projects** FastTab.</span></span>

